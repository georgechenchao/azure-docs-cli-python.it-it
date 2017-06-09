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
# <a name="create-an-azure-service-principal-with-azure-cli-20"></a>Creare un'entità servizio di Azure con l'interfaccia della riga di comando di Azure 2.0

Se si prevede di gestire un'app o un servizio con l'interfaccia della riga di comando di Azure 2.0, sarà necessario eseguirli in un'entità servizio di Azure Active Directory (AAD), anziché con le proprie credenziali.
Questo argomento descrive la creazione di un'entità di sicurezza con l'interfaccia della riga di comando di Azure 2.0.

> [!NOTE]
> È inoltre possibile creare un'entità servizio tramite il portale di Azure.
> Per informazioni dettagliate, vedere [Usare il portale per creare un'applicazione Active Directory e un'entità servizio che accedono alle risorse](/azure/azure-resource-manager/resource-group-create-service-principal-portal).

## <a name="what-is-a-service-principal"></a>Che cos'è un'"entità servizio"?

Un'entità servizio di Azure è un'identità di sicurezza usata da app, servizi e strumenti di automazione creati dall'utente per accedere a risorse di Azure specifiche. Può essere considerata come un'"identità utente" (nome di accesso e password o certificato) con un ruolo specifico e autorizzazioni strettamente controllate per accedere alle risorse. A differenza di un'identità utente generica, essa deve essere in grado di eseguire soltanto operazioni specifiche. Accordandole il livello minimo di autorizzazioni necessarie per eseguire le attività di gestione, un'entità servizio è in grado di migliorare la protezione. 

Al momento, l'interfaccia della riga di comando di Azure 2.0 supporta solo la creazione di credenziali di autenticazione basate su password. Questo argomento illustra la creazione di un'entità servizio con una password specifica e l'assegnazione facoltativa di ruoli a essa.

## <a name="verify-your-own-permission-level"></a>Verificare il proprio livello di autorizzazione

Innanzitutto, è necessario avere autorizzazioni sufficienti sia nell'istanza di Azure Active Directory che nella sottoscrizione di Azure. In particolare, è necessario poter creare un'app in Active Directory e assegnare un ruolo all'entità servizio. 

Il modo più semplice per verificare se l'account dispone delle autorizzazioni appropriate è tramite il portale. Vedere l'articolo su come [controllare le autorizzazioni necessarie nel portale](/azure/azure-resource-manager/resource-group-create-service-principal-portal.md#required-permissions).

## <a name="create-a-service-principal-for-your-application"></a>Creare un'entità servizio per l'applicazione

È necessario disporre di uno dei seguenti elementi per identificare l'app per cui si desidera creare un'entità servizio:

  * Il nome univoco o l'URI dell'app distribuita (quale "MyDemoWebApp" negli esempi) o
  * l'ID dell'applicazione, il GUID univoco associato all'app, il servizio o l'oggetto distribuiti

Questi valori identificano l'applicazione quando si crea un'entità servizio.

### <a name="get-information-about-your-application"></a>Ottenere informazioni sull'applicazione

Ottenere informazioni sull'identità relativamente all'applicazione con `az ad app list`.

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

L'opzione `--display-name` filtra l'elenco restituito di app per mostrare quelle il cui `displayName` che inizia con MyDemoWebApp.

### <a name="create-the-service-principal"></a>Creare l'entità servizio

Usare [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) per creare l'entità servizio. 

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
 > Non creare una password non sicura.  Attenersi alle istruzioni relative a [regole e limitazioni sulle password di Azure AD](/azure/active-directory/active-directory-passwords-policy).

### <a name="get-information-about-the-service-principal"></a>Ottenere informazioni sulle entità servizio

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

### <a name="sign-in-using-the-service-principal"></a>Accedere come entità servizio

È ora possibile accedere come nuova entità servizio per l'app usando *appId* e *password* di `az ad sp show`.  Fornire il valore di *tenant* dai risultati di `az ad sp create-for-rbac`.

```azurecli-interactive
az login --service-principal -u a487e0c1-82af-47d9-9a0b-af184eb87646d --password {password} --tenant {tenant}
``` 

Questo output verrà visualizzato dopo un accesso eseguito correttamente:

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

Usare i valori di `id`, `password` e `tenant` come credenziali per l'esecuzione dell'app. 

## <a name="managing-roles"></a>Gestione dei ruoli 

> [!NOTE]
> Il controllo di accesso in base al ruolo di Azure (Role-Based Access Control - RBAC) è un modello per la definizione e gestione dei ruoli per le entità utente e servizio.
> I ruoli dispongono di set di autorizzazioni associate a essi, che determinano le risorse che un'entità può leggere scrivere o gestire e a cui può accedere.
> Per altre informazioni su ruoli e RBAC, vedere [RBAC: ruoli predefiniti](/azure/active-directory/role-based-access-built-in-roles).

L'interfaccia della riga di comando di Azure 2.0 offre i comandi seguenti per gestire le assegnazioni:

* [az role assignment list](/cli/azure/role/assignment#list)
* [az role assignment create](/cli/azure/role/assignment#create)
* [az role assignment delete](/cli/azure/role/assignment#delete)

Il ruolo predefinito per un'entità servizio è quello di **Collaboratore**. Potrebbe non essere la scelta migliore per le interazioni di un'app con servizi Azure, date le ampie autorizzazioni. Il ruolo **Lettore** è più restrittivo ed è una buona scelta per l'accesso di sola lettura. È possibile visualizzare i dettagli sulle autorizzazioni specifiche del ruolo o crearne di personalizzate tramite il portale di Azure.

In questo esempio, aggiungere il ruolo **Lettore** all'esempio precedente ed eliminare il ruolo **Collaboratore**:

```azurecli-interactive
az role assignment create --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d --role Reader
az role assignment delete --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d --role Contributor
```

Verificare le modifiche elencando i ruoli attualmente assegnati:

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
> Se l'account non ha autorizzazioni sufficienti per assegnare un ruolo, verrà visualizzato un messaggio di errore.
> Il messaggio segnala che l'account non è autorizzato a eseguire l'azione Microsoft.Authorization/roleAssignments/write sull'ambito /subscriptions/{guid}.
   
## <a name="change-the-credentials-of-a-security-principal"></a>Modificare le credenziali di un'entità di sicurezza

È buona norma verificare le autorizzazioni e aggiornare regolarmente le password. È inoltre consigliabile gestire e modificare le credenziali di sicurezza quando si modifica una app.

### <a name="reset-a-service-principal-password"></a>Reimpostare la password di un'entità servizio

Usare `az ad sp reset-credentials` per reimpostare la password corrente dell'entità servizio.

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

L'interfaccia della riga di comando genera una password sicura se si omette l'opzione `--password`.