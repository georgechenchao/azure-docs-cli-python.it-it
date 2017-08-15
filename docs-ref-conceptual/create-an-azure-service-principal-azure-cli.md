---
title: "Creare un&quot;entità servizio di Azure con l&quot;interfaccia della riga di comando di Azure 2.0"
description: "Informazioni su come creare un&quot;entità servizio per un&quot;app o un servizio con l&quot;interfaccia della riga di comando di Azure 2.0."
keywords: Interfaccia della riga di comando di Azure 2.0, Azure Active Directory, Azure Active directory, AD, RBAC
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: fab89cb8-dac1-4e21-9d34-5eadd5213c05
ms.openlocfilehash: 0ee794d5a732c6e8d2d52fca5810a874827930ae
ms.sourcegitcommit: 4fd631a58cf19c494162510d073fbbbdf0524d16
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2017
---
# <a name="create-an-azure-service-principal-with-azure-cli-20"></a><span data-ttu-id="861c6-104">Creare un'entità servizio di Azure con l'interfaccia della riga di comando di Azure 2.0</span><span class="sxs-lookup"><span data-stu-id="861c6-104">Create an Azure service principal with Azure CLI 2.0</span></span>

<span data-ttu-id="861c6-105">Se si prevede di gestire un'app o un servizio con l'interfaccia della riga di comando di Azure 2.0, sarà necessario eseguirli in un'entità servizio di Azure Active Directory (AAD), anziché con le proprie credenziali.</span><span class="sxs-lookup"><span data-stu-id="861c6-105">If you plan to manage your app or service with Azure CLI 2.0, you should run it under an Azure Active Directory (AAD) service principal rather than your own credentials.</span></span>
<span data-ttu-id="861c6-106">Questo argomento descrive la creazione di un'entità di sicurezza con l'interfaccia della riga di comando di Azure 2.0.</span><span class="sxs-lookup"><span data-stu-id="861c6-106">This topic steps you through creating a security principal with Azure CLI 2.0.</span></span>

> [!NOTE]
> <span data-ttu-id="861c6-107">È inoltre possibile creare un'entità servizio tramite il portale di Azure.</span><span class="sxs-lookup"><span data-stu-id="861c6-107">You can also create a service principal through the Azure portal.</span></span>
> <span data-ttu-id="861c6-108">Per informazioni dettagliate, vedere [Usare il portale per creare un'applicazione Active Directory e un'entità servizio che accedono alle risorse](/azure/azure-resource-manager/resource-group-create-service-principal-portal).</span><span class="sxs-lookup"><span data-stu-id="861c6-108">Read [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) for more details.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="861c6-109">Che cos'è un'"entità servizio"?</span><span class="sxs-lookup"><span data-stu-id="861c6-109">What is a 'service principal'?</span></span>

<span data-ttu-id="861c6-110">Un'entità servizio di Azure è un'identità di sicurezza usata da app, servizi e strumenti di automazione creati dall'utente per accedere a risorse di Azure specifiche.</span><span class="sxs-lookup"><span data-stu-id="861c6-110">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="861c6-111">Può essere considerata come un'"identità utente" (nome di accesso e password o certificato) con un ruolo specifico e autorizzazioni strettamente controllate per accedere alle risorse.</span><span class="sxs-lookup"><span data-stu-id="861c6-111">Think of it as a 'user identity' (login and password or certificate) with a specific role, and tightly controlled permissions to access your resources.</span></span> <span data-ttu-id="861c6-112">A differenza di un'identità utente generica, essa deve essere in grado di eseguire soltanto operazioni specifiche.</span><span class="sxs-lookup"><span data-stu-id="861c6-112">It only needs to be able to do specific things, unlike a general user identity.</span></span> <span data-ttu-id="861c6-113">Accordandole il livello minimo di autorizzazioni necessarie per eseguire le attività di gestione, un'entità servizio è in grado di migliorare la protezione.</span><span class="sxs-lookup"><span data-stu-id="861c6-113">It improves security if you only grant it the minimum permissions level needed to perform its management tasks.</span></span> 

<span data-ttu-id="861c6-114">Al momento, l'interfaccia della riga di comando di Azure 2.0 supporta solo la creazione di credenziali di autenticazione basate su password.</span><span class="sxs-lookup"><span data-stu-id="861c6-114">Right now, Azure CLI 2.0 only supports the creation of password-based authentication credentials.</span></span> <span data-ttu-id="861c6-115">Questo argomento illustra la creazione di un'entità servizio con una password specifica e l'assegnazione facoltativa di ruoli a essa.</span><span class="sxs-lookup"><span data-stu-id="861c6-115">In this topic, we cover creating a service principal with a specific password, and optionally assigning specific roles to it.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="861c6-116">Verificare il proprio livello di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="861c6-116">Verify your own permission level</span></span>

<span data-ttu-id="861c6-117">Innanzitutto, è necessario avere autorizzazioni sufficienti sia nell'istanza di Azure Active Directory che nella sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="861c6-117">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="861c6-118">In particolare, è necessario poter creare un'app in Active Directory e assegnare un ruolo all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="861c6-118">Specifically, you must be able to create an app in the Active Directory, and assign a role to the service principal.</span></span> 

<span data-ttu-id="861c6-119">Il modo più semplice per verificare se l'account dispone delle autorizzazioni appropriate è tramite il portale.</span><span class="sxs-lookup"><span data-stu-id="861c6-119">The easiest way to check whether your account has adequate permissions is through the portal.</span></span> <span data-ttu-id="861c6-120">Vedere l'articolo su come [controllare le autorizzazioni necessarie nel portale](/azure/azure-resource-manager/resource-group-create-service-principal-portal.md#required-permissions).</span><span class="sxs-lookup"><span data-stu-id="861c6-120">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal.md#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="861c6-121">Creare un'entità servizio per l'applicazione</span><span class="sxs-lookup"><span data-stu-id="861c6-121">Create a service principal for your application</span></span>

<span data-ttu-id="861c6-122">È necessario disporre di uno dei seguenti elementi per identificare l'app per cui si desidera creare un'entità servizio:</span><span class="sxs-lookup"><span data-stu-id="861c6-122">You must have one of the following to identify the app you want to create a service principal for:</span></span>

  * <span data-ttu-id="861c6-123">Il nome univoco o l'URI dell'app distribuita (quale "MyDemoWebApp" negli esempi) o</span><span class="sxs-lookup"><span data-stu-id="861c6-123">The unique name or URI of your deployed app (such as "MyDemoWebApp" in the examples), or</span></span>
  * <span data-ttu-id="861c6-124">l'ID dell'applicazione, il GUID univoco associato all'app, il servizio o l'oggetto distribuiti</span><span class="sxs-lookup"><span data-stu-id="861c6-124">the Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

<span data-ttu-id="861c6-125">Questi valori identificano l'applicazione quando si crea un'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="861c6-125">These values identify your application when creating a service principal.</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="861c6-126">Ottenere informazioni sull'applicazione</span><span class="sxs-lookup"><span data-stu-id="861c6-126">Get information about your application</span></span>

<span data-ttu-id="861c6-127">Ottenere informazioni sull'identità relativamente all'applicazione con `az ad app list`.</span><span class="sxs-lookup"><span data-stu-id="861c6-127">Get identity information about your application with the `az ad app list`.</span></span>

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

```azurecli-interactive
az ad app list --display-name MyDemoWebApp
```

```json
{
    "appId": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
    "appPermissions": null,
    "availableToOtherTenants": false,
    "displayName": "MyDemoWebApp",
    "homepage": "http://MyDemoWebApp.azurewebsites.net",
    "identifierUris": [
      "http://MyDemoWebApp"
    ],
    "objectId": "bd07205b-629f-4a2e-945e-1ee5dadf610b9",
    "objectType": "Application",
    "replyUrls": []
  }
```

<span data-ttu-id="861c6-128">L'opzione `--display-name` filtra l'elenco restituito di app per mostrare quelle il cui `displayName` che inizia con MyDemoWebApp.</span><span class="sxs-lookup"><span data-stu-id="861c6-128">The `--display-name` option filters the returned list of apps to show those with `displayName` starting with MyDemoWebApp.</span></span>

### <a name="create-the-service-principal"></a><span data-ttu-id="861c6-129">Creare l'entità servizio</span><span class="sxs-lookup"><span data-stu-id="861c6-129">Create the service principal</span></span>

<span data-ttu-id="861c6-130">Usare [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) per creare l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="861c6-130">Use [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) to create the service principal.</span></span> 

```azurecli-interactive
az ad sp create-for-rbac --name {appId} --password "{strong password}" 
``` 

```json
{
  "appId": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
  "displayName": "MyDemoWebApp",
  "name": "http://MyDemoWebApp",
  "password": {strong password},
  "tenant": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
}
```

 > [!WARNING] 
 > <span data-ttu-id="861c6-131">Non creare una password non sicura.</span><span class="sxs-lookup"><span data-stu-id="861c6-131">Don't create an insecure password.</span></span>  <span data-ttu-id="861c6-132">Attenersi alle istruzioni relative a [regole e limitazioni sulle password di Azure AD](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="861c6-132">Follow the [Azure AD password rules and restrictions](/azure/active-directory/active-directory-passwords-policy) guidance.</span></span>

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="861c6-133">Ottenere informazioni sulle entità servizio</span><span class="sxs-lookup"><span data-stu-id="861c6-133">Get information about the service principal</span></span>

```azurecli-interactive
az ad sp show --id a487e0c1-82af-47d9-9a0b-af184eb87646d
```

```json
{
  "appId": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
  "displayName": "MyDemoWebApp",
  "objectId": "0ceae62e-1a1a-446f-aa56-2300d176659bde",
  "objectType": "ServicePrincipal",
  "servicePrincipalNames": [
    "http://MyDemoWebApp",
    "a487e0c1-82af-47d9-9a0b-af184eb87646d"
  ]
}
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="861c6-134">Accedere come entità servizio</span><span class="sxs-lookup"><span data-stu-id="861c6-134">Sign in using the service principal</span></span>

<span data-ttu-id="861c6-135">È ora possibile accedere come nuova entità servizio per l'app usando *appId* e *password* di `az ad sp show`.</span><span class="sxs-lookup"><span data-stu-id="861c6-135">You can now log in as the new service principal for your app using the *appId* and *password* from `az ad sp show`.</span></span>  <span data-ttu-id="861c6-136">Fornire il valore di *tenant* dai risultati di `az ad sp create-for-rbac`.</span><span class="sxs-lookup"><span data-stu-id="861c6-136">Supply the *tenant* value from the results of `az ad sp create-for-rbac`.</span></span>

```azurecli-interactive
az login --service-principal -u a487e0c1-82af-47d9-9a0b-af184eb87646d --password {password} --tenant {tenant}
``` 

<span data-ttu-id="861c6-137">Questo output verrà visualizzato dopo un accesso eseguito correttamente:</span><span class="sxs-lookup"><span data-stu-id="861c6-137">You will see this output after a successful sign-on:</span></span>

```json
[
  {
    "cloudName": "AzureCloud",
    "id": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
    "isDefault": true,
    "state": "Enabled",
    "tenantId": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX",
    "user": {
      "name": "https://MyDemoWebApp",
      "type": "servicePrincipal"
    }
  }
]
```

<span data-ttu-id="861c6-138">Usare i valori di `id`, `password` e `tenant` come credenziali per l'esecuzione dell'app.</span><span class="sxs-lookup"><span data-stu-id="861c6-138">Use the `id`, `password`, and `tenant` values as the credentials for running your app.</span></span> 

## <a name="managing-roles"></a><span data-ttu-id="861c6-139">Gestione dei ruoli</span><span class="sxs-lookup"><span data-stu-id="861c6-139">Managing roles</span></span> 

> [!NOTE]
> <span data-ttu-id="861c6-140">Il controllo di accesso in base al ruolo di Azure (Role-Based Access Control - RBAC) è un modello per la definizione e gestione dei ruoli per le entità utente e servizio.</span><span class="sxs-lookup"><span data-stu-id="861c6-140">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span>
> <span data-ttu-id="861c6-141">I ruoli dispongono di set di autorizzazioni associate a essi, che determinano le risorse che un'entità può leggere scrivere o gestire e a cui può accedere.</span><span class="sxs-lookup"><span data-stu-id="861c6-141">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span>
> <span data-ttu-id="861c6-142">Per altre informazioni su ruoli e RBAC, vedere [RBAC: ruoli predefiniti](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="861c6-142">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="861c6-143">L'interfaccia della riga di comando di Azure 2.0 offre i comandi seguenti per gestire le assegnazioni:</span><span class="sxs-lookup"><span data-stu-id="861c6-143">The Azure CLI 2.0 provides the following commands to manage role assignments:</span></span>

* [<span data-ttu-id="861c6-144">az role assignment list</span><span class="sxs-lookup"><span data-stu-id="861c6-144">az role assignment list</span></span>](/cli/azure/role/assignment#list)
* [<span data-ttu-id="861c6-145">az role assignment create</span><span class="sxs-lookup"><span data-stu-id="861c6-145">az role assignment create</span></span>](/cli/azure/role/assignment#create)
* [<span data-ttu-id="861c6-146">az role assignment delete</span><span class="sxs-lookup"><span data-stu-id="861c6-146">az role assignment delete</span></span>](/cli/azure/role/assignment#delete)

<span data-ttu-id="861c6-147">Il ruolo predefinito per un'entità servizio è quello di **Collaboratore**.</span><span class="sxs-lookup"><span data-stu-id="861c6-147">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="861c6-148">Potrebbe non essere la scelta migliore per le interazioni di un'app con servizi Azure, date le ampie autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="861c6-148">It may not be the best choice for an app's interactions with Azure services, given its broad permissions.</span></span> <span data-ttu-id="861c6-149">Il ruolo **Lettore** è più restrittivo ed è una buona scelta per l'accesso di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="861c6-149">The **Reader** role is more restrictive and is a good choice for read-only access.</span></span> <span data-ttu-id="861c6-150">È possibile visualizzare i dettagli sulle autorizzazioni specifiche del ruolo o crearne di personalizzate tramite il portale di Azure.</span><span class="sxs-lookup"><span data-stu-id="861c6-150">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="861c6-151">In questo esempio, aggiungere il ruolo **Lettore** all'esempio precedente ed eliminare il ruolo **Collaboratore**:</span><span class="sxs-lookup"><span data-stu-id="861c6-151">In this example, add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurecli-interactive
az role assignment create --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d --role Reader
az role assignment delete --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d --role Contributor
```

<span data-ttu-id="861c6-152">Verificare le modifiche elencando i ruoli attualmente assegnati:</span><span class="sxs-lookup"><span data-stu-id="861c6-152">Verify the changes by listing the currently assigned roles:</span></span>

```azurecli-interactive
az role assignment list --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d
```

```json
{
    "id": "/subscriptions/34345f33-0398-4a99-a42b-f6613d1664ac/providers/Microsoft.Authorization/roleAssignments/c27f78a7-9d3b-404b-ab59-47818f9af9ac",
    "name": "c27f78a7-9d3b-404b-ab59-47818f9af9ac",
    "properties": {
      "principalId": "790525226-46f9-4051-b439-7079e41dfa31",
      "principalName": "http://MyDemoWebApp",
      "roleDefinitionId": "/subscriptions/34345f33-0398-4a99-a42b-f6613d1664ac/providers/Microsoft.Authorization/roleDefinitions/acdd72a7-3385-48ef-bd42-f606fba81ae7",
      "roleDefinitionName": "Reader",
      "scope": "/subscriptions/34345f33-0398-4a99-a42b-f6613d1664ac"
    },
    "type": "Microsoft.Authorization/roleAssignments"
}
```

> [!NOTE] 
> <span data-ttu-id="861c6-153">Se l'account non ha autorizzazioni sufficienti per assegnare un ruolo, verrà visualizzato un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="861c6-153">If your account does not have sufficient permissions to assign a role, you see an error message.</span></span>
> <span data-ttu-id="861c6-154">Il messaggio segnala che l'account non è autorizzato a eseguire l'azione Microsoft.Authorization/roleAssignments/write sull'ambito /subscriptions/{guid}.</span><span class="sxs-lookup"><span data-stu-id="861c6-154">The message states your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write' over scope '/subscriptions/{guid}'."</span></span>
   
## <a name="change-the-credentials-of-a-security-principal"></a><span data-ttu-id="861c6-155">Modificare le credenziali di un'entità di sicurezza</span><span class="sxs-lookup"><span data-stu-id="861c6-155">Change the credentials of a security principal</span></span>

<span data-ttu-id="861c6-156">È buona norma verificare le autorizzazioni e aggiornare regolarmente le password.</span><span class="sxs-lookup"><span data-stu-id="861c6-156">It's a good security practice to review permissions and update passwords regularly.</span></span> <span data-ttu-id="861c6-157">È inoltre consigliabile gestire e modificare le credenziali di sicurezza quando si modifica una app.</span><span class="sxs-lookup"><span data-stu-id="861c6-157">You may also want to manage and modify the security credentials as your app changes.</span></span>

### <a name="reset-a-service-principal-password"></a><span data-ttu-id="861c6-158">Reimpostare la password di un'entità servizio</span><span class="sxs-lookup"><span data-stu-id="861c6-158">Reset a service principal password</span></span>

<span data-ttu-id="861c6-159">Usare `az ad sp reset-credentials` per reimpostare la password corrente dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="861c6-159">Use `az ad sp reset-credentials` to reset the current password for the service principal.</span></span>

```azurecli-interactive
az ad sp reset-credentials --name 20bce7de-3cd7-49f4-ab64-bb5b443838c3 --password {new-password}
```

```json
{
  "appId": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
  "name": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
  "password": {new-password},
  "tenant": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
}
```

<span data-ttu-id="861c6-160">L'interfaccia della riga di comando genera una password sicura se si omette l'opzione `--password`.</span><span class="sxs-lookup"><span data-stu-id="861c6-160">The CLI generates a secure password if you leave out the `--password` option.</span></span>