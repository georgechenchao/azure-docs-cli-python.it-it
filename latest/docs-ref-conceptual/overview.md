---
title: Interfaccia della riga di comando di Azure 2.0
description: Panoramica sull'interfaccia della riga di comando di Azure 2.0.
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
ms.assetid: 80ae9f6c-adb7-483c-bfb4-fbb958e075ba
ms.openlocfilehash: 36a08835b9c4f6e71c5ddadbce8ba946c52a1e9b
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/04/2017
---
# <a name="azure-cli-20"></a>Interfaccia della riga di comando di Azure 2.0

L'interfaccia della riga di comando di Azure 2.0 è la nuova esperienza della riga di comando di Azure per gestire le risorse di Azure.
È possibile usarla nel browser con [Azure Cloud Shell](/azure/cloud-shell/overview) oppure [installarla](install-azure-cli.md) in macOS, Linux e Windows ed eseguirla dalla riga di comando.

L'interfaccia della riga di comando di Azure 2.0 è ottimizzata per la gestione e l'amministrazione delle risorse di Azure dalla riga di comando e per la creazione di script di automazione che funzionano con Azure Resource Manager. Usando l'interfaccia della riga di comando di Azure 2.0, è possibile creare macchine virtuali in Azure semplicemente digitando i comandi seguenti:

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

Usare [Cloud Shell](/azure/cloud-shell/overview) per eseguire l'interfaccia della riga di comando nel browser o [installarla](install-azure-cli.md) in macOS, Linux o Windows.
Leggere l'articolo [Introduzione](get-started-with-azure-cli.md) per iniziare a usare l'interfaccia della riga di comando.
Per informazioni sulla versione più recente, vedere le [note sulla versione](release-notes-azure-cli.md).

Gli esempi seguenti aiutano a eseguire scenari comuni con l'interfaccia della riga di comando di Azure 2.0:
- [Macchine virtuali Linux](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [Macchine virtuali Windows](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [App Web](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [Database SQL](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

È inoltre disponibile un [riferimento](/cli/azure/) dettagliato che documenta come utilizzare ogni singolo comando dell'interfaccia della riga di comando di Azure 2.0.

[Introduzione](get-started-with-azure-cli.md) all'interfaccia della riga di comando di Azure 2.0.


> [!NOTE]
> Se si usa la versione precedente dell'interfaccia della riga di comando (Interfaccia della riga di comando di Azure), si può continuare a usarla.
> Se si utilizzano entrambe le interfacce della riga di comando, tenere presente che `azure` è la versione precedente (Interfaccia della riga di comando di Azure) e che `az` è la nuova versione (Interfaccia della riga di comando di Azure 2.0). 