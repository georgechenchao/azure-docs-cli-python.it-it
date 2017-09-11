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
# <a name="managing-multiple-clouds-with-azure-cli-20"></a>Gestione di più cloud con l'interfaccia della riga di comando di Azure 2.0

Se sono disponibili più sottoscrizioni associate ad Azure, è possibile che siano disponibili più cloud. A ogni cloud sono associati funzionalità ed endpoint specifici e ogni cloud è spesso associato a una determinata area, con standard o requisiti diversi per la protezione dei dati.

Per usare in modo efficace più cloud, sarà necessario potere cambiare il cloud attualmente attivo e possibilmente creare nuovi cloud.

## <a name="listing-clouds"></a>Elencare i cloud

È possibile elencare i cloud disponibili tramite il comando [cloud list](/cli/azure/cloud#list). Questo comando indica il cloud attualmente attivo, specifica il profilo corrente e può fornire informazioni sui suffissi e sui nomi host specifici per l'area.

Per ottenere un elenco dei cloud disponibili e del cloud attualmente attivo:

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

## <a name="switching-the-active-cloud"></a>Cambiare il cloud attivo

Per cambiare il cloud attualmente attivo, eseguire il comando [cloud set](/cli/azure/cloud#set). Questo comando accetta un argomento obbligatorio, ovvero il nome del cloud.

```azurecli
az cloud set --name AzureChinaCloud
```

> [!IMPORTANT]
> Se non è mai stata eseguita l'autenticazione per il cloud attivo, sarà necessario completare tale operazione prima di eseguire altre operazioni dell'interfaccia della riga di comando. Per istruzioni relative all'autenticazione, vedere [Log in with Azure CLI 2.0](/cli/azure/authenticate-azure-cli) (Accedere con l'interfaccia della riga di comando di Azure 2.0).

## <a name="register-or-unregister-a-cloud"></a>Registrare o annullare la registrazione di un cloud

Registrare un nuovo cloud se sono disponibili endpoint personalizzati o è necessario un profilo diverso. Per creare un cloud, usare il comando [cloud register](/cli/azure/cloud#register). Questo comando richiede un nome e, facoltativamente, un set di funzionalità e di designazioni di endpoint.

Per creare un cloud con un endpoint specializzato per lo strumento di gestione delle risorse, con un profilo specifico:

```azurecli
az cloud register --name MyCloud --endpoint-resource-manager "https://my.endpoint.manager" --profile 2017-03-09-profile
```

Viene creato il cloud, che però _non_ viene selezionato automaticamente.

Se il cloud creato non è più necessario, è possibile annullarne la registrazione con il comando [cloud unregister](/cli/azure/cloud#unregister):

```azurecli
az cloud unregister --name MyCloud
```

