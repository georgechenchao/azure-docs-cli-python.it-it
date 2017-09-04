---
title: Interfaccia della riga di comando di Azure 2.0
description: Panoramica sull&quot;interfaccia della riga di comando di Azure 2.0.
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
ms.openlocfilehash: 2f4f9950dd663ae85f41bf4efe114b15770ace5d
ms.sourcegitcommit: bcf93ad8ed8802072249cd8187cd4420da89b4c6
ms.translationtype: HT
ms.contentlocale: it-IT
---
# <a name="azure-cli-20"></a><span data-ttu-id="dd3d1-104">Interfaccia della riga di comando di Azure 2.0</span><span class="sxs-lookup"><span data-stu-id="dd3d1-104">Azure CLI 2.0</span></span>

<span data-ttu-id="dd3d1-105">L'interfaccia della riga di comando di Azure 2.0 è la nuova esperienza della riga di comando di Azure per gestire le risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="dd3d1-105">The Azure CLI 2.0 is Azure's new command-line experience for managing Azure resources.</span></span>  <span data-ttu-id="dd3d1-106">Può essere usata in macOS, Linux e Windows.</span><span class="sxs-lookup"><span data-stu-id="dd3d1-106">It can be used on macOS, Linux, and Windows.</span></span> 

<span data-ttu-id="dd3d1-107">L'interfaccia della riga di comando di Azure 2.0 è ottimizzata per la gestione e l'amministrazione delle risorse di Azure dalla riga di comando e per la creazione di script di automazione che funzionano con Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="dd3d1-107">Azure CLI 2.0 is optimized for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="dd3d1-108">Usando l'interfaccia della riga di comando di Azure 2.0, è possibile creare macchine virtuali in Azure semplicemente digitando i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="dd3d1-108">Using the Azure CLI 2.0, you can create VMs within Azure as easily as typing the following command:</span></span>

```azurecli
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

<span data-ttu-id="dd3d1-109">Per installare l'interfaccia di comando di Azure 2.0 sul proprio sistema, vedere l'[articolo relativo all'installazione](install-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="dd3d1-109">Review the [Install article](install-azure-cli.md) to get Azure CLI 2.0 up and running on your system.</span></span> <span data-ttu-id="dd3d1-110">Quindi leggere l'articolo relativo all'[introduzione](get-started-with-azure-cli.md) per iniziare a usarla.</span><span class="sxs-lookup"><span data-stu-id="dd3d1-110">Then read the [Get Started](get-started-with-azure-cli.md) article to begin using it.</span></span>
<span data-ttu-id="dd3d1-111">Per informazioni sulla versione più recente, vedere le [note sulla versione](release-notes-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="dd3d1-111">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

<span data-ttu-id="dd3d1-112">Gli esempi seguenti aiutano a eseguire scenari comuni con l'interfaccia della riga di comando di Azure 2.0:</span><span class="sxs-lookup"><span data-stu-id="dd3d1-112">The following samples can help you learn how to perform common scenarios with Azure CLI 2.0:</span></span>
- [<span data-ttu-id="dd3d1-113">Macchine virtuali Linux</span><span class="sxs-lookup"><span data-stu-id="dd3d1-113">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="dd3d1-114">Macchine virtuali Windows</span><span class="sxs-lookup"><span data-stu-id="dd3d1-114">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="dd3d1-115">App Web</span><span class="sxs-lookup"><span data-stu-id="dd3d1-115">Web Apps</span></span>](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="dd3d1-116">Database SQL</span><span class="sxs-lookup"><span data-stu-id="dd3d1-116">SQL Database</span></span>](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

<span data-ttu-id="dd3d1-117">È inoltre disponibile un [riferimento](/cli/azure/) dettagliato che documenta come utilizzare ogni singolo comando dell'interfaccia della riga di comando di Azure 2.0.</span><span class="sxs-lookup"><span data-stu-id="dd3d1-117">A detailed [reference](/cli/azure/) is also available that documents how to use each individual Azure CLI 2.0 command.</span></span>

<span data-ttu-id="dd3d1-118">[Introduzione](get-started-with-azure-cli.md) all'interfaccia della riga di comando di Azure 2.0.</span><span class="sxs-lookup"><span data-stu-id="dd3d1-118">[Get started](get-started-with-azure-cli.md) with Azure CLI 2.0 now.</span></span>


> [!NOTE]
> <span data-ttu-id="dd3d1-119">Se si usa la versione precedente dell'interfaccia della riga di comando (Interfaccia della riga di comando di Azure), si può continuare a usarla.</span><span class="sxs-lookup"><span data-stu-id="dd3d1-119">If you use the previous version of the CLI (Azure CLI), you can continue to use it.</span></span>
> <span data-ttu-id="dd3d1-120">Se si utilizzano entrambe le interfacce della riga di comando, tenere presente che `azure` è la versione precedente (Interfaccia della riga di comando di Azure) e che `az` è la nuova versione (Interfaccia della riga di comando di Azure 2.0).</span><span class="sxs-lookup"><span data-stu-id="dd3d1-120">If you use both CLIs, remember that `azure` is the old CLI - Azure CLI, and that `az` is the new CLI - Azure CLI 2.0.</span></span> 