---
title: Introduzione all'interfaccia della riga di comando di Azure 2.0
description: Introduzione all'interfaccia della riga di comando di Azure 2.0 su Linux Mac o Windows.
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
ms.assetid: 85c418a8-6177-4833-bb8d-ff4ce2233c1a
ms.openlocfilehash: 5d6d7abb34fa2be571a9a49f0f84380538592807
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/04/2017
---
# <a name="get-started-with-azure-cli-20"></a><span data-ttu-id="3f5e9-104">Introduzione all'interfaccia della riga di comando di Azure 2.0</span><span class="sxs-lookup"><span data-stu-id="3f5e9-104">Get started with Azure CLI 2.0</span></span>

<span data-ttu-id="3f5e9-105">L'interfaccia della riga di comando di Azure 2.0 è la nuova esperienza della riga di comando di Azure per gestire le risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-105">The Azure CLI 2.0 is Azure's new command line experience for managing Azure resources.</span></span>
<span data-ttu-id="3f5e9-106">È possibile usarla nel browser con [Azure Cloud Shell](/azure/cloud-shell/overview) oppure [installarla](install-azure-cli.md) in macOS, Linux e Windows ed eseguirla dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-106">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can [install](install-azure-cli.md) it on macOS, Linux, and Windows and run it from the command line.</span></span>

<span data-ttu-id="3f5e9-107">L'interfaccia della riga di comando di Azure 2.0 è ottimizzata per la gestione e l'amministrazione delle risorse di Azure dalla riga di comando e per la creazione di script di automazione che funzionano con Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-107">Azure CLI 2.0 is optimized for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span>
<span data-ttu-id="3f5e9-108">Questo articolo offre un'introduzione all'uso e ne illustra i concetti di base.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-108">This article helps get you started using it, and teaches you the core concepts behind it.</span></span>

<span data-ttu-id="3f5e9-109">Per informazioni sulla versione più recente, vedere le [note sulla versione](release-notes-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="3f5e9-109">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

## <a name="connect"></a><span data-ttu-id="3f5e9-110">Connettere</span><span class="sxs-lookup"><span data-stu-id="3f5e9-110">Connect</span></span>

<span data-ttu-id="3f5e9-111">Il modo più semplice per iniziare è [avviare Cloud Shell](/azure/cloud-shell/quickstart).</span><span class="sxs-lookup"><span data-stu-id="3f5e9-111">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="3f5e9-112">Avviare Cloud Shell dal riquadro di spostamento in alto nel portale di Azure.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-112">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Icona di Shell](media/get-started-with-azure-cli/shell-icon.png)

2. <span data-ttu-id="3f5e9-114">Scegliere la sottoscrizione da usare e creare un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-114">Choose the subscription you want to use and create a storage account.</span></span>

   ![Creare un account di archiviazione](media/get-started-with-azure-cli/storage-prompt.png)

<span data-ttu-id="3f5e9-116">È anche possibile [installare](install-azure-cli.md) l'interfaccia della riga di comando ed eseguirla localmente dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-116">You can also [install](install-azure-cli.md) the CLI and run it locally from the command line.</span></span>

## <a name="create-a-resource-group"></a><span data-ttu-id="3f5e9-117">Creare un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3f5e9-117">Create a Resource Group</span></span>

<span data-ttu-id="3f5e9-118">Dopo aver eseguito tutte le impostazioni, è possibile usare l'interfaccia della riga di comando di Azure per creare risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-118">Now that we've got everything set up, let's use the Azure CLI to create resources within Azure.</span></span>

<span data-ttu-id="3f5e9-119">Si crea prima un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-119">First, create a Resource Group.</span></span>  <span data-ttu-id="3f5e9-120">I gruppi di risorse di Azure consentono di gestire numerose risorse che si desidera raggruppare in modo logico.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-120">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group.</span></span>  <span data-ttu-id="3f5e9-121">Ad esempio, è possibile creare un gruppo di risorse per un'applicazione o un progetto e aggiungere una macchina virtuale, un database e un servizio rete CDN al suo interno.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-121">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="3f5e9-122">Creare un gruppo di risorse denominato "MyResourceGroup" nell'area *westus2* di Azure.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-122">Let's create a resource group named "MyResourceGroup" in the *westus2* region of Azure.</span></span>  <span data-ttu-id="3f5e9-123">A questo scopo, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="3f5e9-123">To do so type the following command:</span></span>

```azurecli-interactive
az group create -n MyResourceGroup -l westus2 
```

<span data-ttu-id="3f5e9-124">Dopo aver creato il gruppo di risorse, il comando `az group create` restituisce alcune proprietà della risorsa appena creata:</span><span class="sxs-lookup"><span data-stu-id="3f5e9-124">Once the resource group has been created, the `az group create` command outputs several properties of the newly created resource:</span></span>

```Output
{
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup",
  "location": "westus2",
  "managedBy": null,
  "name": "MyResourceGroup",
  "properties": {
    "provisioningState": "Succeeded"
  },
  "tags": null
}
```

## <a name="create-a-linux-virtual-machine"></a><span data-ttu-id="3f5e9-125">Creare una macchina virtuale Linux</span><span class="sxs-lookup"><span data-stu-id="3f5e9-125">Create a Linux Virtual Machine</span></span>

<span data-ttu-id="3f5e9-126">Con un gruppo di risorse disponibile, creare una macchina virtuale Linux contenuta in esso.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-126">Now that we have our resource group, let's create a Linux VM within it.</span></span>

<span data-ttu-id="3f5e9-127">È possibile creare una macchina virtuale Linux usando la comune immagine UbuntuLTS con due dischi di archiviazione da 10 GB e 20 GB collegati, mediante il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="3f5e9-127">You can create a Linux VM using the popular UbuntuLTS image, with two attached storage disks of 10 GB and 20 GB, with the following command:</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS --data-disk-sizes-gb 10 20
```

<span data-ttu-id="3f5e9-128">Quando si esegue il comando precedente, l'interfaccia della riga di comando di Azure 2.0 cerca una coppia di chiavi SSH archiviata nella directory ~/.ssh.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-128">When you run the preceding command, the Azure CLI 2.0 looks for an SSH key pair stored under your ~/.ssh directory.</span></span>  <span data-ttu-id="3f5e9-129">Se non è ancora presente una coppia di chiavi SSH in tale percorso, è possibile richiedere all'interfaccia della riga di comando di Azure di crearne automaticamente una passando il parametro --generate-ssh-keys:</span><span class="sxs-lookup"><span data-stu-id="3f5e9-129">If you don't already have an SSH key pair stored there, you can ask the Azure CLI to automatically create one for you by passing the --generate-ssh-keys parameter:</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS --data-disk-sizes-gb 10 20 --generate-ssh-keys
```

<span data-ttu-id="3f5e9-130">Il comando `az vm create` restituisce l'output una volta che la macchina virtuale è stata creata completamente ed è possibile accedervi e usarla.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-130">The `az vm create` command returns output once the VM has been fully created and is ready to be accessed and used.</span></span> <span data-ttu-id="3f5e9-131">L'output include varie proprietà della macchina virtuale appena creata tra cui l'indirizzo IP pubblico:</span><span class="sxs-lookup"><span data-stu-id="3f5e9-131">The output includes several properties of the newly created VM including its public IP address:</span></span>

```Output
{
  "fqdns": "",
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyLinuxVM",
  "location": "westus2",
  "macAddress": "xx-xx-xx-xx-xx-xx",
  "powerState": "VM running",
  "privateIpAddress": "xx.x.x.x",
  "publicIpAddress": "xx.xxx.xxx.xx",
  "resourceGroup": "MyResourceGroup"
}
```

<span data-ttu-id="3f5e9-132">Ora che la macchina virtuale è stata creata, è possibile accedere alla nuova macchina virtuale Linux tramite **SSH** con l'indirizzo IP pubblico della macchina virtuale creata:</span><span class="sxs-lookup"><span data-stu-id="3f5e9-132">Now that the VM has been created, you can log on to your new Linux VM using **SSH** with the public IP address of the VM you created:</span></span>

```azurecli-interactive
ssh xx.xxx.xxx.xxx
```

```Output
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 3.19.0-65-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sun Feb 19 00:32:28 UTC 2017

  System load: 0.31              Memory usage: 3%   Processes:       89
  Usage of /:  39.6% of 1.94GB   Swap usage:   0%   Users logged in: 0

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

my-login@MyLinuxVM:~$
```

## <a name="create-a-windows-server-virtual-machine"></a><span data-ttu-id="3f5e9-133">Creare una macchina virtuale Windows Server</span><span class="sxs-lookup"><span data-stu-id="3f5e9-133">Create a Windows Server Virtual Machine</span></span>

<span data-ttu-id="3f5e9-134">Creare ora una macchina virtuale basata su Windows Server 2016 Datacenter usando il comando `az vm create` e aggiungerla allo stesso gruppo di risorse "MyResourceGroup" usato per la macchina virtuale Linux.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-134">Let's now create a Windows Server 2016 Datacenter-based VM using the `az vm create` command and add it to the same "MyResourceGroup" resource group that we used for our Linux VM.</span></span>  <span data-ttu-id="3f5e9-135">Come nell'esempio sulla macchina virtuale Linux, si collegano due dischi di archiviazione usando il parametro `--data-disk-sizes-gb`.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-135">Like the Linux VM example, we'll also attach two storage disks using the `--data-disk-sizes-gb` parameter.</span></span>

<span data-ttu-id="3f5e9-136">Azure richiede di evitare di usare nomi utente e password facilmente identificabili.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-136">Azure requires that you avoid using easily guessed usernames/passwords.</span></span> <span data-ttu-id="3f5e9-137">Vi sono regole specifiche sui caratteri che possono essere usati nonché sulla lunghezza minima di nome utente e password.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-137">There are specific rules for what characters can be used as well as the minimum length of both username and password.</span></span>  

> [!NOTE]
> <span data-ttu-id="3f5e9-138">Al momento dell'esecuzione di questo comando verrà richiesto di immettere il nome utente e la password.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-138">You will be prompted to enter your username and password when running this command.</span></span>

```azurecli-interactive
az vm create -n MyWinVM -g MyResourceGroup --image Win2016Datacenter
```

<span data-ttu-id="3f5e9-139">Il comando `az vm create` genera i risultati una volta che la macchina virtuale è stata creata completamente ed è possibile accedervi e usarla.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-139">The `az vm create` command output results once the VM has been fully created and is ready to be accessed and used.</span></span>

```Output
{
  "fqdns": "",
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyWinVM",
  "location": "westus2",
  "macAddress": "xx-xx-xx-xx-xx-xx",
  "powerState": "VM running",
  "privateIpAddress": "xx.x.x.x",
  "publicIpAddress": "xx.xxx.xx.xxx",
  "resourceGroup": "MyResourceGroup"
}
```

<span data-ttu-id="3f5e9-140">Accedere ora alla macchina virtuale Windows Server appena creata tramite desktop remoto, usando l'indirizzo IP pubblico della macchina virtuale (restituito nell'output del comando `az vm create`).</span><span class="sxs-lookup"><span data-stu-id="3f5e9-140">Now log on to your newly created Windows Server VM using Remote Desktop and the public IP address of the VM (which is returned in the output from `az vm create`).</span></span>  
<span data-ttu-id="3f5e9-141">Se si usa un sistema basato su Windows, è possibile eseguire questa operazione dalla riga di comando usando il comando `mstsc`:</span><span class="sxs-lookup"><span data-stu-id="3f5e9-141">If you are on a Windows-based system, you can do this from the command line using the `mstsc` command:</span></span>

```azurecli-interactive
mstsc /v:xx.xxx.xx.xxx
```

<span data-ttu-id="3f5e9-142">Fornire la stessa combinazione di nome utente/password usata quando si crea la macchina virtuale per l'accesso.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-142">Supply the same username/password combination you used when creating the VM to log in.</span></span>

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="3f5e9-143">Creazione di altre risorse in Azure</span><span class="sxs-lookup"><span data-stu-id="3f5e9-143">Creating other resources in Azure</span></span>

<span data-ttu-id="3f5e9-144">È stato descritto come creare un gruppo di risorse, una macchina virtuale Linux e una macchina virtuale di Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-144">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="3f5e9-145">È possibile creare molti altri tipi di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-145">You can create many other types of Azure resources as well.</span></span>  

<span data-ttu-id="3f5e9-146">Tutte le nuove risorse vengono create usando un modello di denominazione `az <resource type name> create` coerente.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-146">All new resources are created using a consistent `az <resource type name> create` naming pattern.</span></span>  <span data-ttu-id="3f5e9-147">Ad esempio, per creare un bilanciamento del carico sulla rete di Azure da associare con le macchine virtuali appena create, è possibile usare il seguente comando:</span><span class="sxs-lookup"><span data-stu-id="3f5e9-147">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```azurecli-interactive
az network lb create -n MyLoadBalancer -g MyResourceGroup
```

<span data-ttu-id="3f5e9-148">È inoltre possibile creare una nuova rete virtuale privata (nota come "VNet" all'interno di Azure) per l'infrastruttura usando il comando create seguente:</span><span class="sxs-lookup"><span data-stu-id="3f5e9-148">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following create command:</span></span>

```azurecli-interactive
az network vnet create -n MyVirtualNetwork -g MyResourceGroup --address-prefix 10.0.0.0/16
```

<span data-ttu-id="3f5e9-149">Azure e l'interfaccia della riga di comando di Azure sono particolarmente efficienti poiché è possibile usarli non solo per ottenere un'infrastruttura basata su cloud, ma anche per creare servizi di piattaforma gestita.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-149">What makes Azure and the Azure CLI powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span>  <span data-ttu-id="3f5e9-150">I servizi di piattaforma gestita possono anche essere combinati con l'infrastruttura per creare soluzioni ancora più potenti.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-150">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="3f5e9-151">Ad esempio, è possibile usare l'interfaccia della riga di comando di Azure per creare un servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-151">For example, you can use the Azure CLI to create an Azure AppService.</span></span>  <span data-ttu-id="3f5e9-152">Il servizio app di Azure è un servizio di piattaforma gestita che fornisce un ottimo modo per l'hosting di app Web senza doversi preoccupare dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-152">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span>  <span data-ttu-id="3f5e9-153">Dopo aver creato il servizio app di Azure, è possibile creare due nuove app Web di Azure all'interno del servizio app usando i comandi create seguenti:</span><span class="sxs-lookup"><span data-stu-id="3f5e9-153">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following create commands:</span></span>

```azurecli-interactive
# Create an Azure AppService that we can host any number of web apps within
az appservice plan create -n MyAppServicePlan -g MyResourceGroup

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
az webapp create -n MyWebApp43432 -g MyResourceGroup --plan MyAppServicePlan 
az webapp create -n MyWebApp43433 -g MyResourceGroup --plan MyAppServicePlan 
```

<span data-ttu-id="3f5e9-154">Dopo aver appreso le nozioni di base sul modello `az <resource type name> create`, risulta facile creare qualsiasi elemento.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-154">Once you understand the basics of the `az <resource type name> create` pattern, it becomes easy to create anything.</span></span> <span data-ttu-id="3f5e9-155">Di seguito sono riportati alcuni tipi di risorse Azure comuni e i corrispondenti comandi create dell'interfaccia della riga di comando di Azure per crearli:</span><span class="sxs-lookup"><span data-stu-id="3f5e9-155">Following are some popular Azure resource types and the corresponding Azure CLI create commands to create them:</span></span>

```
Resource Type               Azure CLI create command
-------------               ------------------------
Resource Group              az group create
Virtual Machine             az vm create
Virtual Network             az network vnet create
Load Balancer               az network lb create
Managed Disk                az disk create
Storage account             az storage account create
Virtual Machine Scale Set   az vmss create
Azure Container Service     az acs create
Web App                     az webapp create
SQL Database Server         az sql server create
Document DB                 az documentdb create
```

<span data-ttu-id="3f5e9-156">Per altre informazioni su ulteriori parametri specifici delle risorse che è possibile passare a ognuno dei comandi precedenti e sui tipi di risorse che è possibile creare, vedere la [documentazione di riferimento](/cli/azure).</span><span class="sxs-lookup"><span data-stu-id="3f5e9-156">Visit the [Reference documentation](/cli/azure) to learn more about the additional resource-specific parameters that you can pass to each of the preceding commands and the resource types you can create.</span></span> 

## <a name="useful-tip-optimizing-create-operations-using---no-wait"></a><span data-ttu-id="3f5e9-157">Suggerimento utile: ottimizzazione delle operazioni di creazione usando --no-wait</span><span class="sxs-lookup"><span data-stu-id="3f5e9-157">Useful tip: Optimizing create operations using --no-wait</span></span>

<span data-ttu-id="3f5e9-158">Per impostazione predefinita quando si creano risorse usando l'interfaccia della riga di comando di Azure 2.0, il comando `az <resource type name> create` attende che la risorsa venga creata e sia pronta per l'uso.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-158">By default when you create resources using the Azure CLI 2.0, the `az <resource type name> create` command waits until the resource has been created and is ready for you to use.</span></span>  <span data-ttu-id="3f5e9-159">Ad esempio, se si crea una macchina virtuale, per impostazione predefinita il comando `az vm create` non restituirà risultati finché la macchina virtuale non sarà creata e non sarà pronta per eseguire una connessione tramite SSH o RDP.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-159">For example, if you create a VM, the `az vm create` command will, by default, not return until the VM is created and is ready for you to SSH or RDP into it.</span></span>

<span data-ttu-id="3f5e9-160">Si usa questo approccio poiché risulta più semplice scrivere script di automazione che contengono più passaggi con dipendenze (e richiedono che venga completata correttamente un'attività precedente prima di continuare).</span><span class="sxs-lookup"><span data-stu-id="3f5e9-160">We use this approach because it makes it easier to write automation scripts that contain multiple steps with dependencies (and need a prior task to have completed successfully before continuing).</span></span>

<span data-ttu-id="3f5e9-161">Se non è necessario attendere la creazione di una risorsa prima di continuare, è possibile usare l'opzione `no-wait` per avviare un'azione di creazione in background.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-161">If you do not need to wait on creation of a resource before continuing, you can use the `no-wait` option to start a create action in the background.</span></span> <span data-ttu-id="3f5e9-162">È possibile continuare a usare l'interfaccia della riga di comando per altri comandi.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-162">You can continue using the CLI for other commands.</span></span>

<span data-ttu-id="3f5e9-163">Ad esempio, l'uso seguente del comando `az vm create` avvia una distribuzione della macchina virtuale e quindi restituisce i risultati molto più rapidamente (prima che la macchina virtuale sia avviata completamente):</span><span class="sxs-lookup"><span data-stu-id="3f5e9-163">For example, the following usage of the `az vm create` starts a VM deployment and then return much more quickly (and before the VM has fully booted):</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM2 -g MyResourceGroup --image UbuntuLTS --no-wait
```

<span data-ttu-id="3f5e9-164">L'uso dell'approccio `--no-wait` può consentire di ottimizzare notevolmente le prestazioni degli script di automazione.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-164">Using the `--no-wait` approach can help you optimize the performance of your automation scripts considerably.</span></span>

## <a name="listing-resources-and-formatting-output"></a><span data-ttu-id="3f5e9-165">Elenco di risorse e formattazione dell'output</span><span class="sxs-lookup"><span data-stu-id="3f5e9-165">Listing resources and formatting output</span></span>

<span data-ttu-id="3f5e9-166">È possibile usare il comando `list` nell'interfaccia della riga di comando di Azure per trovare ed elencare le risorse in esecuzione in Azure.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-166">You can use the `list` command within the Azure CLI to find and list the resources running in Azure.</span></span> 

<span data-ttu-id="3f5e9-167">Come con il comando create, è possibile elencare le risorse nell'interfaccia della riga di comando di Azure 2.0 usando un modello di denominazione `az <resource type name> list` comune, coerente per tutti i tipi di risorsa.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-167">Like with the create command, you can list resources using the Azure CLI 2.0 using a common `az <resource type name> list` naming pattern that is consistent across all resource types.</span></span>  <span data-ttu-id="3f5e9-168">Sono disponibili vari formati di output e opzioni di query per filtrare e ordinare l'elenco di risorse nel modo in cui si preferisce visualizzarlo.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-168">There are various output formats and query options available to filter and sort the list of resources in the way you prefer to see them.</span></span>

<span data-ttu-id="3f5e9-169">Ad esempio, `az vm list` mostra l'elenco di tutte le macchine virtuali presenti.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-169">For example, `az vm list` shows the list of all VMs you have.</span></span>   

```azurecli-interactive
az vm list 
```
<span data-ttu-id="3f5e9-170">I valori sono restituiti per impostazione predefinita in JSON (per brevità è riportato solo l'output parziale).</span><span class="sxs-lookup"><span data-stu-id="3f5e9-170">The values returned are by default in JSON (only showing partial output for sake of brevity).</span></span>

```json
[
  {
    "availabilitySet": null,
    "diagnosticsProfile": null,
    "hardwareProfile": {
      "vmSize": "Standard_DS1_v2"
    },
    "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010",
    "instanceView": null,
    "licenseType": null,
    "location": "westus2",
    "name": "MyLinuxVM",
    "networkProfile": {
      "networkInterfaces": [
        {
          "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/demorg1/providers/Microsoft.Network/networkInterfaces/DemoVM010VMNic",
          "primary": null,
          "resourceGroup": "MyResourceGroup"
        }
      ]
    },
          ...
          ...
          ...   
]
```

<span data-ttu-id="3f5e9-171">Facoltativamente è anche possibile modificare il formato di output usando l'opzione `--output`.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-171">You can optionally modify the output format using the `--output` option.</span></span>  <span data-ttu-id="3f5e9-172">Eseguire il comando `az vm list` per visualizzare entrambe le macchine virtuali Linux e Windows Server create precedentemente, insieme alle proprietà più comuni di una macchina virtuale, usando l'opzione di formato di agevole lettura *table*:</span><span class="sxs-lookup"><span data-stu-id="3f5e9-172">Run the `az vm list` command to see both the Linux and Windows Server VMs created earlier, along with the most common properties of a VM, using the easy to read *table* format option:</span></span>

```azurecli-interactive
az vm list --output table
```

```Output
Name       ResourceGroup    Location
---------  ---------------  ----------
MyLinuxVM  MyResourceGroup  westus2
MyWinVM    MyResourceGroup  westus2
```

<span data-ttu-id="3f5e9-173">L'opzione di output *tsv* può essere usata per ottenere un formato di testo separato da tabulazioni senza intestazioni.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-173">The *tsv* output option can be used to get a text-based, tab-separated format without any headers.</span></span>  <span data-ttu-id="3f5e9-174">Questo formato è utile quando si desidera inviare tramite pipe l'output a un altro strumento basato su testo quale grep.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-174">This format is useful when you want to pipe the output into another text-based tool like grep.</span></span> 

```azurecli-interactive
az vm list --output tsv
```

```
None    None            /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyLinuxVM        None    None    westus2 MyLinuxVM                   None        Succeeded       MyResourceGroup None                    Microsoft.Compute/virtualMachines       XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
None    None            /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyWinVM  None    None    westus2 MyWinVM                 None    Succeeded       MyResourceGroup None                    Microsoft.Compute/virtualMachines       XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```
<span data-ttu-id="3f5e9-175">Per altre informazioni su ulteriori modi per elencare risorse e formattare l'output, vedere l'articolo relativo ai [formati di output](format-output-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="3f5e9-175">Visit the [output formats](format-output-azure-cli.md) article to learn more about the additional ways to list resources and format the output.</span></span>

## <a name="querying-resources-and-shaping-outputs"></a><span data-ttu-id="3f5e9-176">Esecuzione di query su risorse e shaping dell'output</span><span class="sxs-lookup"><span data-stu-id="3f5e9-176">Querying resources and shaping outputs</span></span>

<span data-ttu-id="3f5e9-177">Spesso è necessario eseguire query solo sulle risorse che soddisfano una condizione specifica.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-177">Often you want to be able to query for only those resources that meet a specific condition.</span></span>  

<span data-ttu-id="3f5e9-178">Il comando `list` include una funzionalità integrata che consente di filtrare agevolmente le risorse per nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-178">The `list` command has built-in support that makes it easy to filter resources by Resource Group name.</span></span>  <span data-ttu-id="3f5e9-179">Ad esempio, è possibile passare un parametro `--ResourceGroup` o `-g` a un comando `list` per recuperare solo le risorse in un gruppo di risorse specifico:</span><span class="sxs-lookup"><span data-stu-id="3f5e9-179">For example, you can pass either a `--ResourceGroup` or `-g` parameter to a `list` command to only retrieve those resources within a specific resource group:</span></span>


```azurecli-interactive
az vm list -g MyResourceGroup --output table
```

```Output
Name       ResourceGroup    Location
---------  ---------------  ----------
MyLinuxVM  MyResourceGroup  westus2
MyWinVM    MyResourceGroup  westus2
```

<span data-ttu-id="3f5e9-180">Per una funzionalità di query ancora più efficace, è possibile usare il parametro `--query` per eseguire una query JMESPath sui risultati di *qualsiasi* comando `az`.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-180">For even more powerful querying support, you can use the `--query` parameter to execute a JMESPath query on the results of *any* `az` command.</span></span>  <span data-ttu-id="3f5e9-181">Le query JMESPath possono essere usate sia per filtrare che per lo shaping dell'output dei risultati restituiti.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-181">JMESPath queries can be used both to filter as well as shape the output of any returned result.</span></span>

<span data-ttu-id="3f5e9-182">Ad esempio, eseguire il comando seguente per eseguire query su qualsiasi risorsa di macchina virtuale all'interno di un gruppo di risorse che contenga le lettere "My":</span><span class="sxs-lookup"><span data-stu-id="3f5e9-182">For example, execute the following command to query for any VM resource within any resource group that contains the letters "My":</span></span>

```azurecli-interactive
az vm list --output table --query "[?contains(resourceGroup,'MY')]" 
```

```Output
ResourceGroup    ProvisioningState    Name       Location    VmId
---------------  -------------------  ---------  ----------  ------------------------------------
MYRESOURCEGROUP  Succeeded            MyLinuxVM  westus2     XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
MYRESOURCEGROUP  Succeeded            MyWinVM    westus2     XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="3f5e9-183">È quindi possibile affinare ulteriormente l'output usando la funzionalità di shaping delle query JMESPath per generare valori diversi.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-183">We could then choose to further refine the output by using the shaping capability of JMESPath queries to output different values as well.</span></span>  <span data-ttu-id="3f5e9-184">Ad esempio, il comando seguente recupera il tipo di disco del sistema operativo che la macchina virtuale usa per determinare se il sistema operativo è basato su Linux o Windows:</span><span class="sxs-lookup"><span data-stu-id="3f5e9-184">For example, the following command retrieves the type of OS disk the VM is using to determine whether the OS is Linux or Windows based:</span></span>

```azurecli-interactive
az vm list --output table --query "[?contains(resourceGroup,'MY')].{ VMName:name,OSType:storageProfile.osDisk.osType }" 
```

```Output
VMName     OSType
---------  --------
MyLinuxVM  Linux
MyWinVM    Windows
```

<span data-ttu-id="3f5e9-185">Il supporto di JMESPath nell'interfaccia della riga di comando di Azure è notevolmente efficace.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-185">The JMESPath support in Azure CLI is powerful.</span></span>  <span data-ttu-id="3f5e9-186">Per altre informazioni su come usarlo vedere l'articolo su [query](query-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="3f5e9-186">Learn more about how to use it in our [query](query-azure-cli.md) article.</span></span>

## <a name="deleting-resources"></a><span data-ttu-id="3f5e9-187">Eliminazione di risorse</span><span class="sxs-lookup"><span data-stu-id="3f5e9-187">Deleting resources</span></span>

<span data-ttu-id="3f5e9-188">È possibile usare il comando `delete` nell'interfaccia della riga di comando di Azure per eliminare le risorse che non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-188">You can use the `delete` command within Azure CLI to delete the resources you no longer need.</span></span> <span data-ttu-id="3f5e9-189">È possibile usare il comando `delete` con qualsiasi risorsa in modo analogo al comando `create`.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-189">You can use the `delete` command with any resource just like you can with the `create` command.</span></span>

```azurecli-interactive
az vm delete -n MyLinuxVM -g MyResourceGroup
```

<span data-ttu-id="3f5e9-190">Per impostazione predefinita l'interfaccia della riga di comando richiede di confermare l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-190">By default the CLI prompts to confirm deletion.</span></span>  <span data-ttu-id="3f5e9-191">È possibile eliminare questa richiesta per gli script automatici.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-191">You can suppress this prompt for automated scripts.</span></span>

```Output
Are you sure you want to perform this operation? (y/n): y
EndTime                           Name                                  StartTime                         Status
--------------------------------  ------------------------------------  --------------------------------  ---------
2017-02-19T02:35:56.678905+00:00  5b74ab80-9b29-4329-b483-52b406583e2f  2017-02-19T02:33:35.372769+00:00  Succeeded
```

<span data-ttu-id="3f5e9-192">È anche possibile usare il comando `delete` per eliminare molte risorse contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-192">You can also use the `delete` command to delete many resources at a time.</span></span> <span data-ttu-id="3f5e9-193">Ad esempio, il comando seguente elimina tutte le risorse nel gruppo di risorse "MyResourceGroup" usate per tutti gli esempi in questa esercitazione di introduzione.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-193">For example, the following command deletes all the resources in the "MyResourceGroup" resource group that we've used for all the samples in this Get Started tutorial.</span></span>

```azurecli-interactive
az group delete -n MyResourceGroup
```

```Output
Are you sure you want to perform this operation? (y/n): y
```

## <a name="get-samples"></a><span data-ttu-id="3f5e9-194">Ottenere gli esempi</span><span class="sxs-lookup"><span data-stu-id="3f5e9-194">Get samples</span></span>

<span data-ttu-id="3f5e9-195">Per altre informazioni sull'uso dell'interfaccia della riga di comando di Azure, vedere gli script più comuni per [macchine virtuali Linux](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json), [macchine virtuali Windows](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json), [app Web](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json) e [database SQL](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="3f5e9-195">To learn more about ways to use the Azure CLI, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json), [Web apps](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json), and [SQL Database](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json).</span></span>

## <a name="read-the-api-reference-docs"></a><span data-ttu-id="3f5e9-196">Leggere la documentazione di riferimento sulle API</span><span class="sxs-lookup"><span data-stu-id="3f5e9-196">Read the API reference docs</span></span>

[<span data-ttu-id="3f5e9-197">Informazioni di riferimento sulle API</span><span class="sxs-lookup"><span data-stu-id="3f5e9-197">API reference</span></span>](/cli/azure)

## <a name="get-help"></a><span data-ttu-id="3f5e9-198">Ottenere aiuto</span><span class="sxs-lookup"><span data-stu-id="3f5e9-198">Get help</span></span>

<span data-ttu-id="3f5e9-199">L'interfaccia della riga di comando di Azure include una guida incorporata corrispondente alla documentazione Web che è possibile eseguire dalla riga di comando:</span><span class="sxs-lookup"><span data-stu-id="3f5e9-199">The Azure CLI has built-in help documentation, which matches our web documentation that you can run from the command line:</span></span>

```azurecli-interactive
az [command-group [command]] -h
```

<span data-ttu-id="3f5e9-200">Ad esempio, per visualizzare i comandi e i sottogruppi disponibili per le macchine virtuali, usare:</span><span class="sxs-lookup"><span data-stu-id="3f5e9-200">For example, to see what commands and subgroups are available for VMs, use:</span></span>

```azurecli-interactive
az vm -h
```

<span data-ttu-id="3f5e9-201">Per ottenere informazioni sul comando per creare una macchina virtuale, usare:</span><span class="sxs-lookup"><span data-stu-id="3f5e9-201">To get help with the command to create a VM, use:</span></span>

```azurecli-interactive
az vm create -h
```

## <a name="switch-from-azure-cli-10"></a><span data-ttu-id="3f5e9-202">Passaggio dall'interfaccia della riga di comando di Azure 1.0</span><span class="sxs-lookup"><span data-stu-id="3f5e9-202">Switch from Azure CLI 1.0</span></span>

<span data-ttu-id="3f5e9-203">Se si ha già familiarità con l'uso dell'interfaccia della riga di comando di Azure 1.0 (azure.js), si noterà che in alcuni casi i comandi sono pressoché uguali.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-203">If you already know how to use Azure CLI 1.0 (azure.js), you'll notice places where the commands aren't quite the same.</span></span>
<span data-ttu-id="3f5e9-204">In altri casi, i comandi per eseguire un'attività sono notevolmente diversi.</span><span class="sxs-lookup"><span data-stu-id="3f5e9-204">Sometimes the commands to perform a task are significantly different.</span></span>
<span data-ttu-id="3f5e9-205">Per agevolare il passaggio dall'interfaccia della riga di comando di Azure 1.0 all'interfaccia della riga di comando di Azure 2.0, è stato creato questo [mapping dei comandi](https://github.com/Azure/azure-cli/blob/master/doc/azure2az_commands.rst).</span><span class="sxs-lookup"><span data-stu-id="3f5e9-205">To help you make the switch from Azure CLI 1.0 to Azure CLI 2.0, we've started this [command mapping](https://github.com/Azure/azure-cli/blob/master/doc/azure2az_commands.rst).</span></span>

## <a name="send-us-your-feedback"></a><span data-ttu-id="3f5e9-206">Invio di commenti</span><span class="sxs-lookup"><span data-stu-id="3f5e9-206">Send us your feedback</span></span>

```azurecli-interactive
az feedback
```
