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
ms.openlocfilehash: 36a08835b9c4f6e71c5ddadbce8ba946c52a1e9b
ms.sourcegitcommit: 4fd631a58cf19c494162510d073fbbbdf0524d16
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2017
---
# <a name="azure-cli-20"></a><span data-ttu-id="0c228-104">Interfaccia della riga di comando di Azure 2.0</span><span class="sxs-lookup"><span data-stu-id="0c228-104">Azure CLI 2.0</span></span>

<span data-ttu-id="0c228-105">L'interfaccia della riga di comando di Azure 2.0 è la nuova esperienza della riga di comando di Azure per gestire le risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="0c228-105">The Azure CLI 2.0 is Azure's new command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="0c228-106">È possibile usarla nel browser con [Azure Cloud Shell](/azure/cloud-shell/overview) oppure [installarla](install-azure-cli.md) in macOS, Linux e Windows ed eseguirla dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="0c228-106">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can [install](install-azure-cli.md) it on macOS, Linux, and Windows and run it from the command line.</span></span>

<span data-ttu-id="0c228-107">L'interfaccia della riga di comando di Azure 2.0 è ottimizzata per la gestione e l'amministrazione delle risorse di Azure dalla riga di comando e per la creazione di script di automazione che funzionano con Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="0c228-107">Azure CLI 2.0 is optimized for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="0c228-108">Usando l'interfaccia della riga di comando di Azure 2.0, è possibile creare macchine virtuali in Azure semplicemente digitando i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c228-108">Using the Azure CLI 2.0, you can create VMs within Azure as easily as typing the following command:</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

<span data-ttu-id="0c228-109">Usare [Cloud Shell](/azure/cloud-shell/overview) per eseguire l'interfaccia della riga di comando nel browser o [installarla](install-azure-cli.md) in macOS, Linux o Windows.</span><span class="sxs-lookup"><span data-stu-id="0c228-109">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the CLI in your browser, or [install](install-azure-cli.md) it on macOS, Linux, or Windows.</span></span>
<span data-ttu-id="0c228-110">Leggere l'articolo [Introduzione](get-started-with-azure-cli.md) per iniziare a usare l'interfaccia della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="0c228-110">Read the [Get Started](get-started-with-azure-cli.md) article to begin using the CLI.</span></span>
<span data-ttu-id="0c228-111">Per informazioni sulla versione più recente, vedere le [note sulla versione](release-notes-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="0c228-111">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

<span data-ttu-id="0c228-112">Gli esempi seguenti aiutano a eseguire scenari comuni con l'interfaccia della riga di comando di Azure 2.0:</span><span class="sxs-lookup"><span data-stu-id="0c228-112">The following samples can help you learn how to perform common scenarios with Azure CLI 2.0:</span></span>
- [<span data-ttu-id="0c228-113">Macchine virtuali Linux</span><span class="sxs-lookup"><span data-stu-id="0c228-113">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="0c228-114">Macchine virtuali Windows</span><span class="sxs-lookup"><span data-stu-id="0c228-114">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="0c228-115">App Web</span><span class="sxs-lookup"><span data-stu-id="0c228-115">Web Apps</span></span>](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="0c228-116">Database SQL</span><span class="sxs-lookup"><span data-stu-id="0c228-116">SQL Database</span></span>](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

<span data-ttu-id="0c228-117">È inoltre disponibile un [riferimento](/cli/azure/) dettagliato che documenta come utilizzare ogni singolo comando dell'interfaccia della riga di comando di Azure 2.0.</span><span class="sxs-lookup"><span data-stu-id="0c228-117">A detailed [reference](/cli/azure/) is also available that documents how to use each individual Azure CLI 2.0 command.</span></span>

<span data-ttu-id="0c228-118">[Introduzione](get-started-with-azure-cli.md) all'interfaccia della riga di comando di Azure 2.0.</span><span class="sxs-lookup"><span data-stu-id="0c228-118">[Get started](get-started-with-azure-cli.md) with Azure CLI 2.0 now.</span></span>


> [!NOTE]
> <span data-ttu-id="0c228-119">Se si usa la versione precedente dell'interfaccia della riga di comando (Interfaccia della riga di comando di Azure), si può continuare a usarla.</span><span class="sxs-lookup"><span data-stu-id="0c228-119">If you use the previous version of the CLI (Azure CLI), you can continue to use it.</span></span>
> <span data-ttu-id="0c228-120">Se si utilizzano entrambe le interfacce della riga di comando, tenere presente che `azure` è la versione precedente (Interfaccia della riga di comando di Azure) e che `az` è la nuova versione (Interfaccia della riga di comando di Azure 2.0).</span><span class="sxs-lookup"><span data-stu-id="0c228-120">If you use both CLIs, remember that `azure` is the old CLI - Azure CLI, and that `az` is the new CLI - Azure CLI 2.0.</span></span> 