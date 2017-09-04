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
ms.openlocfilehash: 383fb6ebd90ac79f60869187b402d53d4f1791fd
ms.sourcegitcommit: 4fd631a58cf19c494162510d073fbbbdf0524d16
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2017
---
# <a name="manage-multiple-azure-subscriptions"></a>Gestire più sottoscrizioni di Azure

Se si usa Azure da poco, probabilmente si avrà una singola sottoscrizione.
Tuttavia, se si usa Azure già da tempo, è possibile che si siano create più sottoscrizioni di Azure.
In questo caso, è possibile configurare l'interfaccia della riga di comando di Azure 2.0 per eseguire comandi su una determinata sottoscrizione.

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

1. Ottenere un elenco di tutte le sottoscrizioni dell'account.

   ```azurecli-interactive
   az account list --output table
   ```

   ```Output
   Name                                         CloudName    SubscriptionId                        State     IsDefault
   -------------------------------------------  -----------  ------------------------------------  --------  -----------
   My Production Subscription                   AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled
   My DevTest Subscription                      AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled   True
   My Demos                                     AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled
   ```

1. Impostare il parametro predefinito.
 
   ```azurecli-interactive
   az account set --subscription "My Demos"
   ```

   > [!NOTE]
   > Il parametro `--subscription` accetta il nome della sottoscrizione o l'ID sottoscrizione.

È possibile verificare la modifica eseguendo nuovamente il comando `az account list --output table`.

Dopo aver impostato la sottoscrizione predefinita, tutti i successivi comandi della riga di comando di Azure verranno eseguiti con questa sottoscrizione.