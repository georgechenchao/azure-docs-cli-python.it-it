---
title: Accedere con l&quot;interfaccia della riga di comando di Azure 2.0
description: Accedere con l&quot;interfaccia della riga di comando di Azure 2.0 su Linux, Mac o Windows.
keywords: Interfaccia della riga di comando di Azure 2.0, Linux, Mac, Windows, OS X, Ubuntu, Debian, CentOS, RHEL, SUSE, CoreOS, Docker, Windows, Python, PIP
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 65becd3a-9d69-4415-8a30-777d13a0e7aa
ms.openlocfilehash: fea893ebd55811527e0e92375ffc081a52cdbb57
ms.sourcegitcommit: bcf93ad8ed8802072249cd8187cd4420da89b4c6
ms.translationtype: HT
ms.contentlocale: it-IT
---
# <a name="log-in-with-azure-cli-20"></a><span data-ttu-id="8e118-104">Accedere con l'interfaccia della riga di comando di Azure 2.0</span><span class="sxs-lookup"><span data-stu-id="8e118-104">Log in with Azure CLI 2.0</span></span>

<span data-ttu-id="8e118-105">Esistono diversi modi per accedere ed eseguire l'autenticazione con l'interfaccia della riga di comando di Azure.</span><span class="sxs-lookup"><span data-stu-id="8e118-105">There are several ways to log in and authenticate with the Azure CLI.</span></span> <span data-ttu-id="8e118-106">Il modo più semplice per iniziare consiste nell'accedere in modo interattivo tramite il browser o dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="8e118-106">The simplest way to get started is to log in interactively through your browser, or to log in at the command line.</span></span> <span data-ttu-id="8e118-107">L'approccio consigliato consiste nell'usare delle entità di servizio, che consentono di creare account non interattivi da usare per la modifica delle risorse.</span><span class="sxs-lookup"><span data-stu-id="8e118-107">Our recommended approach is to use service principals, which provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="8e118-108">Concedendo a un'entità servizio solo le autorizzazioni appropriate, è possibile garantire che gli script di automazione siano ancora più sicuri.</span><span class="sxs-lookup"><span data-stu-id="8e118-108">By granting just the appropriate permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

<span data-ttu-id="8e118-109">I comandi che si eseguono con l'interfaccia della riga di comando vengono eseguiti sulla sottoscrizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="8e118-109">Commands that you run with the CLI are run against your default subscription.</span></span>  <span data-ttu-id="8e118-110">Se si hanno più sottoscrizioni, può essere opportuno [verificare la sottoscrizione predefinita](manage-azure-subscriptions-azure-cli.md) e modificarla in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="8e118-110">If you have more than one subscription, you may want to [confirm your default subscription](manage-azure-subscriptions-azure-cli.md) and change it appropriately.</span></span>

## <a name="interactive-log-in"></a><span data-ttu-id="8e118-111">Accesso interattivo</span><span class="sxs-lookup"><span data-stu-id="8e118-111">Interactive log-in</span></span>

<span data-ttu-id="8e118-112">Accedere in modo interattivo dal Web browser.</span><span class="sxs-lookup"><span data-stu-id="8e118-112">Log in interactively from your web browser.</span></span>

[!INCLUDE [interactive_login](includes/interactive-login.md)]

## <a name="command-line"></a><span data-ttu-id="8e118-113">Riga di comando</span><span class="sxs-lookup"><span data-stu-id="8e118-113">Command line</span></span>

<span data-ttu-id="8e118-114">Fornire le credenziali dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="8e118-114">Provide your credentials on the command line.</span></span>

> [!Note]
> <span data-ttu-id="8e118-115">Questo approccio non funziona con gli account Microsoft o gli account in cui è abilitata l'autenticazione a due fattori.</span><span class="sxs-lookup"><span data-stu-id="8e118-115">This approach doesn't work with Microsoft accounts or accounts that have two-factor authentication enabled.</span></span>

```azurecli
az login -u <username> -p <password>
```

## <a name="logging-in-with-a-service-principal"></a><span data-ttu-id="8e118-116">Accesso con un'entità servizio</span><span class="sxs-lookup"><span data-stu-id="8e118-116">Logging in with a service principal</span></span>

<span data-ttu-id="8e118-117">Le entità servizio sono analoghe agli account utente a cui è possibile applicare delle regole mediante Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8e118-117">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span>
<span data-ttu-id="8e118-118">L'autenticazione con un'entità servizio rappresenta il modo migliore per proteggere l'utilizzo delle risorse Azure dagli script o dalle applicazioni che modificano le risorse.</span><span class="sxs-lookup"><span data-stu-id="8e118-118">Authenticating with a service principal is the best way to secure the usage of your Azure resources from either your scripts or applications that manipulate resources.</span></span>
<span data-ttu-id="8e118-119">Definire i ruoli che si desidera assegnare agli utenti tramite il set di comandi `az role`.</span><span class="sxs-lookup"><span data-stu-id="8e118-119">You define the roles you want your users to have via the `az role` set of commands.</span></span>
<span data-ttu-id="8e118-120">Per altre informazioni ed esempi di ruoli di entità servizio, vedere gli [articoli di riferimento sul ruolo az](https://docs.microsoft.com/cli/azure/role.md).</span><span class="sxs-lookup"><span data-stu-id="8e118-120">You can learn more and see examples of service principal roles in our [az role reference articles](https://docs.microsoft.com/cli/azure/role.md).</span></span>

1. <span data-ttu-id="8e118-121">Se non si dispone di un'entità servizio, [crearne una](create-an-azure-service-principal-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="8e118-121">If you don't already have a service principal, [create one](create-an-azure-service-principal-azure-cli.md).</span></span>

1. <span data-ttu-id="8e118-122">Accedere con l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="8e118-122">Log in with the service principal.</span></span>

   ```azurecli
   az login --service-principal -u "http://my-app" -p <password> --tenant <tenant>
   ```

   <span data-ttu-id="8e118-123">Per ottenere il proprio tenant, accedere in modo interattivo e ottenere il tenantId dalla sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8e118-123">To get your tenant, log in interactively and then get the tenantId from your subscription.</span></span>

   ```azurecli
   az login
   az account show
   ```

   ```json
   {
       "environmentName": "AzureCloud",
       "id": "********-****-****-****-************",
       "isDefault": true,
       "name": "Pay-As-You-Go",
       "state": "Enabled",
       "tenantId": "********-****-****-****-************",
       "user": {
       "name": "********",
       "type": "user"
       }
   }
   ```