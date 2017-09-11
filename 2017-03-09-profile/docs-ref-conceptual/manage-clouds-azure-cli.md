---
title: "Gestione di più cloud con l'interfaccia della riga di comando di Azure 2.0"
description: Creare, accedere e gestire cloud diversi con l'interfaccia della riga di comando di Azure 2.0.
keywords: Interfaccia della riga di comando di Azure 2.0, Azure, cloud, data center, enti pubblici, area, Cina, Germania
author: sptramer
manager: douge
ms.author: sttramer
ms.date: 06/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.openlocfilehash: 0222b7339e46346ef6c7e9ad98616d9b71129942
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/04/2017
---
# <a name="managing-multiple-clouds-with-azure-cli-20"></a><span data-ttu-id="13c6b-104">Gestione di più cloud con l'interfaccia della riga di comando di Azure 2.0</span><span class="sxs-lookup"><span data-stu-id="13c6b-104">Managing multiple clouds with Azure CLI 2.0</span></span>

<span data-ttu-id="13c6b-105">Se sono disponibili più sottoscrizioni associate ad Azure, è possibile che siano disponibili più cloud.</span><span class="sxs-lookup"><span data-stu-id="13c6b-105">If you have multiple subscriptions associated with Azure, you may have more than one cloud available.</span></span> <span data-ttu-id="13c6b-106">A ogni cloud sono associati funzionalità ed endpoint specifici e ogni cloud è spesso associato a una determinata area, con standard o requisiti diversi per la protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="13c6b-106">Each cloud has its own associated endpoints and capabilities, and is often associated with a particular region that has different data protection standards or requirements.</span></span>

<span data-ttu-id="13c6b-107">Per usare in modo efficace più cloud, sarà necessario potere cambiare il cloud attualmente attivo e possibilmente creare nuovi cloud.</span><span class="sxs-lookup"><span data-stu-id="13c6b-107">To effectively work with multiple clouds, you will need to be able to switch between which is currently active, and possibly create new clouds.</span></span>

## <a name="listing-clouds"></a><span data-ttu-id="13c6b-108">Elencare i cloud</span><span class="sxs-lookup"><span data-stu-id="13c6b-108">Listing clouds</span></span>

<span data-ttu-id="13c6b-109">È possibile elencare i cloud disponibili tramite il comando [cloud list](/cli/azure/cloud#list).</span><span class="sxs-lookup"><span data-stu-id="13c6b-109">You may list your available clouds with the [cloud list](/cli/azure/cloud#list) command.</span></span> <span data-ttu-id="13c6b-110">Questo comando indica il cloud attualmente attivo, specifica il profilo corrente e può fornire informazioni sui suffissi e sui nomi host specifici per l'area.</span><span class="sxs-lookup"><span data-stu-id="13c6b-110">This will tell you which cloud is currently active, what its current profile is, and can provide information on regional suffixes and host names.</span></span>

<span data-ttu-id="13c6b-111">Per ottenere un elenco dei cloud disponibili e del cloud attualmente attivo:</span><span class="sxs-lookup"><span data-stu-id="13c6b-111">To get a list of the available clouds and the currently active one:</span></span>

```azurecli
az cloud list --output table
```

```output
IsActive    Name               Profile
----------  -----------------  ---------
True        AzureCloud         latest
            AzureChinaCloud    latest
            AzureUSGovernment  latest
            AzureGermanCloud   latest
```

## <a name="switching-the-active-cloud"></a><span data-ttu-id="13c6b-112">Cambiare il cloud attivo</span><span class="sxs-lookup"><span data-stu-id="13c6b-112">Switching the active cloud</span></span>

<span data-ttu-id="13c6b-113">Per cambiare il cloud attualmente attivo, eseguire il comando [cloud set](/cli/azure/cloud#set).</span><span class="sxs-lookup"><span data-stu-id="13c6b-113">In order to switch the currently active cloud, you run the [cloud set](/cli/azure/cloud#set) command.</span></span> <span data-ttu-id="13c6b-114">Questo comando accetta un argomento obbligatorio, ovvero il nome del cloud.</span><span class="sxs-lookup"><span data-stu-id="13c6b-114">This command takes one required argument, the name of the cloud.</span></span>

```azurecli
az cloud set --name AzureChinaCloud
```

> [!IMPORTANT]
> <span data-ttu-id="13c6b-115">Se non è mai stata eseguita l'autenticazione per il cloud attivo, sarà necessario completare tale operazione prima di eseguire altre operazioni dell'interfaccia della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="13c6b-115">If you have never authenticated for the active cloud, you will need to do so before performing any other CLI operations.</span></span> <span data-ttu-id="13c6b-116">Per istruzioni relative all'autenticazione, vedere [Log in with Azure CLI 2.0](/cli/azure/authenticate-azure-cli) (Accedere con l'interfaccia della riga di comando di Azure 2.0).</span><span class="sxs-lookup"><span data-stu-id="13c6b-116">For instructions on authenticating, see [Log in with Azure CLI 2.0](/cli/azure/authenticate-azure-cli).</span></span>

## <a name="register-or-unregister-a-cloud"></a><span data-ttu-id="13c6b-117">Registrare o annullare la registrazione di un cloud</span><span class="sxs-lookup"><span data-stu-id="13c6b-117">Register or unregister a cloud</span></span>

<span data-ttu-id="13c6b-118">Registrare un nuovo cloud se sono disponibili endpoint personalizzati o è necessario un profilo diverso.</span><span class="sxs-lookup"><span data-stu-id="13c6b-118">Register a new cloud if you have your own endpoints or require a different profile.</span></span> <span data-ttu-id="13c6b-119">Per creare un cloud, usare il comando [cloud register](/cli/azure/cloud#register).</span><span class="sxs-lookup"><span data-stu-id="13c6b-119">Creating a cloud is done with the [cloud register](/cli/azure/cloud#register) command.</span></span> <span data-ttu-id="13c6b-120">Questo comando richiede un nome e, facoltativamente, un set di funzionalità e di designazioni di endpoint.</span><span class="sxs-lookup"><span data-stu-id="13c6b-120">This command requires a name, and optionally a set of capabilities and endpoint designations.</span></span>

<span data-ttu-id="13c6b-121">Per creare un cloud con un endpoint specializzato per lo strumento di gestione delle risorse, con un profilo specifico:</span><span class="sxs-lookup"><span data-stu-id="13c6b-121">To create a cloud with a specialized endpoint for the resource manager, with a specific profile:</span></span>

```azurecli
az cloud register --name MyCloud --endpoint-resource-manager "https://my.endpoint.manager" --profile 2017-03-09-profile
```

<span data-ttu-id="13c6b-122">Viene creato il cloud, che però _non_ viene selezionato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="13c6b-122">This creates the cloud, but does _not_ automatically select it.</span></span>

<span data-ttu-id="13c6b-123">Se il cloud creato non è più necessario, è possibile annullarne la registrazione con il comando [cloud unregister](/cli/azure/cloud#unregister):</span><span class="sxs-lookup"><span data-stu-id="13c6b-123">If you no longer require the created cloud, it can be unregistered with the [cloud unregister](/cli/azure/cloud#unregister) command:</span></span>

```azurecli
az cloud unregister --name MyCloud
```

