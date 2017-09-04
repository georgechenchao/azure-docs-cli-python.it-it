---
title: Gestire le sottoscrizioni di Azure con l&quot;interfaccia della riga di comando di Azure 2.0
description: Gestire le sottoscrizioni di Azure con l&quot;interfaccia della riga di comando di Azure 2.0 su Linux, Mac o Windows.
keywords: Azure CLI 2.0, Linux, Mac, Windows, OS X, sottoscrizione
author: kamaljit
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 98fb955e-6dbf-47e2-80ac-170d6d95cb70
ms.openlocfilehash: c3538077e05d61f3c40880bb8b804226eb99dc85
ms.sourcegitcommit: bcf93ad8ed8802072249cd8187cd4420da89b4c6
ms.translationtype: HT
ms.contentlocale: it-IT
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="afe5d-104">Gestire più sottoscrizioni di Azure</span><span class="sxs-lookup"><span data-stu-id="afe5d-104">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="afe5d-105">Se si usa Azure da poco, probabilmente si avrà una singola sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="afe5d-105">If you are brand new to Azure, you probably only have a single subscription.</span></span>
<span data-ttu-id="afe5d-106">Tuttavia, se si usa Azure già da tempo, è possibile che si siano create più sottoscrizioni di Azure.</span><span class="sxs-lookup"><span data-stu-id="afe5d-106">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span>
<span data-ttu-id="afe5d-107">In questo caso, è possibile configurare l'interfaccia della riga di comando di Azure 2.0 per eseguire comandi su una determinata sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="afe5d-107">If so, you can configure Azure CLI 2.0 to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="afe5d-108">Ottenere un elenco di tutte le sottoscrizioni dell'account.</span><span class="sxs-lookup"><span data-stu-id="afe5d-108">Get a list of all subscriptions in your account.</span></span>

   ```azurecli
   az account list --output table
   ```

   ```Output
   Name                                         CloudName    SubscriptionId                        State     IsDefault
   -------------------------------------------  -----------  ------------------------------------  --------  -----------
   My Production Subscription                   AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled
   My DevTest Subscription                      AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled   True
   My Demos                                     AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled
   ```

1. <span data-ttu-id="afe5d-109">Impostare il parametro predefinito.</span><span class="sxs-lookup"><span data-stu-id="afe5d-109">Set the default.</span></span>
 
   ```azurecli
   az account set --subscription "My Demos"
   ```

<span data-ttu-id="afe5d-110">È possibile verificare la modifica eseguendo nuovamente il comando `az account list --output table`.</span><span class="sxs-lookup"><span data-stu-id="afe5d-110">You can verify the change by running the `az account list --output table` command again.</span></span>

<span data-ttu-id="afe5d-111">Dopo aver impostato la sottoscrizione predefinita, tutti i successivi comandi della riga di comando di Azure verranno eseguiti con questa sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="afe5d-111">Once you set your default subscription, all subsequent Azure CLI commands run against this subscription.</span></span>