---
title: Installare l'interfaccia della riga di comando di Azure 2.0.
description: Documenti di riferimento per l'installazione dell'interfaccia della riga di comando di Azure 2.0
keywords: Interfaccia della riga di comando di Azure 2.0, informazioni di riferimento sull'interfaccia della riga di comando di Azure 2.0, installare l'interfaccia della riga di comando di Azure 2.0, interfaccia della riga di comando di Azure con Python, disinstallare l'interfaccia della riga di comando di Azure 2.0, interfaccia della riga di comando di Azure, installare l'interfaccia della riga di comando di Azure, informazioni di riferimento sull'interfaccia della riga di comando di Azure
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 08/17/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ea5c0ee1-c530-4a1e-a83f-e1be71f6d416
ms.openlocfilehash: 00d5b555975007d7e57f04ce5d69f4f29e6d0219
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/04/2017
---
# <a name="install-azure-cli-20"></a><span data-ttu-id="c2120-104">Installare l'interfaccia della riga di comando di Azure 2.0</span><span class="sxs-lookup"><span data-stu-id="c2120-104">Install Azure CLI 2.0</span></span>

<span data-ttu-id="c2120-105">È possibile installare oggi stesso l'interfaccia della riga di comando di Azure,</span><span class="sxs-lookup"><span data-stu-id="c2120-105">Install the new version of the Azure CLI today!</span></span>
<span data-ttu-id="c2120-106">che è stata migliorata e aggiornata per offrire un'esperienza ottimale della riga di comando nativa per la gestione delle risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="c2120-106">We've improved and updated it to provide a great native command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="c2120-107">Può essere usata in macOS, Linux e Windows.</span><span class="sxs-lookup"><span data-stu-id="c2120-107">It can be used on macOS, Linux, and Windows.</span></span>
<span data-ttu-id="c2120-108">Per informazioni sulla versione più recente, vedere le [note sulla versione](release-notes-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="c2120-108">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

> [!NOTE]
> <span data-ttu-id="c2120-109">Se è necessaria la versione precedente dell'interfaccia della riga di comando di Azure, vedere [Installare l'interfaccia della riga di comando di Azure 1.0](/azure/cli-install-nodejs).</span><span class="sxs-lookup"><span data-stu-id="c2120-109">If you need the previous version of the Azure CLI, here's how to [install Azure CLI 1.0](/azure/cli-install-nodejs).</span></span>

## <a name="a-namemacosinstall-on-macos"></a><span data-ttu-id="c2120-110"><a name="macOS"/>Eseguire l'installazione in macOS</span><span class="sxs-lookup"><span data-stu-id="c2120-110"><a name="macOS"/>Install on macOS</span></span>

1. <span data-ttu-id="c2120-111">Installare l'interfaccia della riga di comando di Azure 2.0 con `curl`.</span><span class="sxs-lookup"><span data-stu-id="c2120-111">Install Azure CLI 2.0 with `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. <span data-ttu-id="c2120-112">Potrebbe essere necessario riavviare la shell per rendere effettive alcune modifiche apportate.</span><span class="sxs-lookup"><span data-stu-id="c2120-112">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```
   
3. <span data-ttu-id="c2120-113">Eseguire l'interfaccia della riga di comando dal prompt dei comandi con il comando `az`.</span><span class="sxs-lookup"><span data-stu-id="c2120-113">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-windows"></a><span data-ttu-id="c2120-114">Eseguire l'installazione in Windows</span><span class="sxs-lookup"><span data-stu-id="c2120-114">Install on Windows</span></span>

<span data-ttu-id="c2120-115">È possibile installare l'interfaccia della riga di comando di Azure 2.0 con MSI e usarla nella riga di comando di Windows, oppure è possibile installare l'interfaccia della riga di comando con `apt-get` su Bash in Ubuntu in Windows.</span><span class="sxs-lookup"><span data-stu-id="c2120-115">You can install Azure CLI 2.0 with the MSI and use it in the Windows command-line, or you can install the CLI with `apt-get` on Bash on Ubuntu on Windows.</span></span>

### <a name="install-with-msi-for-the-windows-command-line"></a><span data-ttu-id="c2120-116">Eseguire l'installazione con MSI per la riga di comando di Windows</span><span class="sxs-lookup"><span data-stu-id="c2120-116">Install with MSI for the Windows command-line</span></span> 

<span data-ttu-id="c2120-117">Per installare l'interfaccia della riga di comando in Windows e usarla nella riga di comando di Windows, scaricare ed eseguire [MSI](https://aka.ms/InstallAzureCliWindows).</span><span class="sxs-lookup"><span data-stu-id="c2120-117">To install the CLI on Windows and use it in the Windows command-line, download and run the [MSI](https://aka.ms/InstallAzureCliWindows).</span></span>

### <a name="install-with-apt-get-for-bash-on-ubuntu-on-windows"></a><span data-ttu-id="c2120-118">Eseguire l'installazione con apt-get per Bash in Ubuntu in Windows</span><span class="sxs-lookup"><span data-stu-id="c2120-118">Install with apt-get for Bash on Ubuntu on Windows</span></span>

1. <span data-ttu-id="c2120-119">Se Bash in Windows non è disponibile, [installarlo](https://msdn.microsoft.com/commandline/wsl/install_guide).</span><span class="sxs-lookup"><span data-stu-id="c2120-119">If you don't have Bash on Windows, [install it](https://msdn.microsoft.com/commandline/wsl/install_guide).</span></span>

2. <span data-ttu-id="c2120-120">Aprire la shell di Bash.</span><span class="sxs-lookup"><span data-stu-id="c2120-120">Open the Bash shell.</span></span>

3. <span data-ttu-id="c2120-121">Modificare l'elenco di origini.</span><span class="sxs-lookup"><span data-stu-id="c2120-121">Modify your sources list.</span></span>

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. <span data-ttu-id="c2120-122">Eseguire i comandi sudo seguenti:</span><span class="sxs-lookup"><span data-stu-id="c2120-122">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

5.  <span data-ttu-id="c2120-123">Eseguire l'interfaccia della riga di comando dal prompt dei comandi con il comando `az`.</span><span class="sxs-lookup"><span data-stu-id="c2120-123">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-debianubuntu-with-apt-get"></a><span data-ttu-id="c2120-124">Eseguire l'installazione in Debian/Ubuntu con apt-get</span><span class="sxs-lookup"><span data-stu-id="c2120-124">Install on Debian/Ubuntu with apt-get</span></span>

<span data-ttu-id="c2120-125">Per i sistemi basati su Debian/Ubuntu, è possibile installare l'interfaccia della riga di comando di Azure 2.0 tramite `apt-get`.</span><span class="sxs-lookup"><span data-stu-id="c2120-125">For Debian/Ubuntu based systems, you can install Azure CLI 2.0 via `apt-get`.</span></span>

1. <span data-ttu-id="c2120-126">Modificare l'elenco di origini.</span><span class="sxs-lookup"><span data-stu-id="c2120-126">Modify your sources list.</span></span>
 
   - <span data-ttu-id="c2120-127">Sistema a 32 bit</span><span class="sxs-lookup"><span data-stu-id="c2120-127">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="c2120-128">Sistema a 64 bit</span><span class="sxs-lookup"><span data-stu-id="c2120-128">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="c2120-129">Eseguire i comandi sudo seguenti:</span><span class="sxs-lookup"><span data-stu-id="c2120-129">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

3.  <span data-ttu-id="c2120-130">Eseguire l'interfaccia della riga di comando dal prompt dei comandi con il comando `az`.</span><span class="sxs-lookup"><span data-stu-id="c2120-130">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-with-docker"></a><span data-ttu-id="c2120-131">Eseguire l'installazione con Docker</span><span class="sxs-lookup"><span data-stu-id="c2120-131">Install with Docker</span></span>

<span data-ttu-id="c2120-132">È disponibile un'immagine Docker preconfigurata con l'interfaccia della riga di comando di Azure 2.0.</span><span class="sxs-lookup"><span data-stu-id="c2120-132">We maintain a Docker image preconfigured with the Azure CLI 2.0.</span></span>

<span data-ttu-id="c2120-133">Installare l'interfaccia della riga di comando con `docker run`.</span><span class="sxs-lookup"><span data-stu-id="c2120-133">Install the CLI using `docker run`.</span></span>

  ```bash
  docker run azuresdk/azure-cli-python:<version>
  ```

<span data-ttu-id="c2120-134">Per le versioni disponibili, vedere i [tag di Docker](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/).</span><span class="sxs-lookup"><span data-stu-id="c2120-134">See our [Docker tags](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) for available versions.</span></span>

<span data-ttu-id="c2120-135">L'interfaccia della riga di comando viene installata nell'immagine come il comando `az` in `/usr/local/bin`.</span><span class="sxs-lookup"><span data-stu-id="c2120-135">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span>

> [!NOTE]
> <span data-ttu-id="c2120-136">Per acquisire le chiavi SSH dall'ambiente utente, è possibile usare `-v ${HOME}:/root` per montare $HOME come `/root`.</span><span class="sxs-lookup"><span data-stu-id="c2120-136">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>

> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

## <a name="a-namelinuxinstall-on-linux-without-apt-get"></a><span data-ttu-id="c2120-137"><a name="Linux"/>Eseguire l'installazione in Linux senza apt-get</span><span class="sxs-lookup"><span data-stu-id="c2120-137"><a name="Linux"/>Install on Linux without apt-get</span></span>

<span data-ttu-id="c2120-138">È consigliabile installare l'interfaccia della riga di comando con `apt-get`, se possibile.</span><span class="sxs-lookup"><span data-stu-id="c2120-138">It is recommended that you install the CLI with `apt-get` if you are able to.</span></span> <span data-ttu-id="c2120-139">Per le distribuzioni che non usano Gestione pacchetti `apt`, è possibile eseguire l'installazione manuale.</span><span class="sxs-lookup"><span data-stu-id="c2120-139">For distributions which do not use the `apt` package manager, you can manually install.</span></span>

1. <span data-ttu-id="c2120-140">Installare i prerequisiti in base alla distribuzione Linux specifica.</span><span class="sxs-lookup"><span data-stu-id="c2120-140">Install the prerequisites based on your Linux distribution.</span></span>

   ```
   Platform              | Prerequisites
   ----------------------|---------------------------------------------
   Ubuntu 15.10 or 16.04 | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev build-essential
   Ubuntu 12.04 or 14.04 | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev
   Debian 8              | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev build-essential
   Debian 7              | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev
   CentOS 7.1 or 7.2     | sudo yum check-update; sudo yum install -y gcc python libffi-devel python-devel openssl-devel
   RedHat 7.2            | sudo yum check-update; sudo yum install -y gcc python libffi-devel python-devel openssl-devel
   SUSE OpenSUSE 13.2    | sudo zypper refresh && sudo zypper --non-interactive install curl gcc python python-xml libffi-devel python-devel openssl-devel
   ```

<span data-ttu-id="c2120-141">Se la distribuzione non è inclusa nell'elenco precedente, sarà necessario installare [Python](https://www.python.org/downloads/), [libffi](https://sourceware.org/libffi/), e [OpenSSL](https://www.openssl.org/source/).</span><span class="sxs-lookup"><span data-stu-id="c2120-141">If your distribution is not listed above, you will need to install [Python](https://www.python.org/downloads/), [libffi](https://sourceware.org/libffi/), and [OpenSSL](https://www.openssl.org/source/).</span></span>

2. <span data-ttu-id="c2120-142">Installare l'interfaccia della riga di comando con `curl`.</span><span class="sxs-lookup"><span data-stu-id="c2120-142">Install the CLI with  `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. <span data-ttu-id="c2120-143">Potrebbe essere necessario riavviare la shell per rendere effettive alcune modifiche apportate.</span><span class="sxs-lookup"><span data-stu-id="c2120-143">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```

4. <span data-ttu-id="c2120-144">Eseguire l'interfaccia della riga di comando dal prompt dei comandi con il comando `az`.</span><span class="sxs-lookup"><span data-stu-id="c2120-144">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="c2120-145">Risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="c2120-145">Troubleshooting</span></span>

<span data-ttu-id="c2120-146">Se si verifica un problema durante l'installazione dell'interfaccia della riga di comando, controllare questa sezione per verificare se include il caso specifico.</span><span class="sxs-lookup"><span data-stu-id="c2120-146">If you encounter an issue during CLI install, check this section to see if your particular case is covered.</span></span> <span data-ttu-id="c2120-147">Se il problema non è incluso in questa sezione, [segnalare il problema su Github](https://github.com/Azure/azure-cli/issues).</span><span class="sxs-lookup"><span data-stu-id="c2120-147">If your issue is not here, please [file a Github issue](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="curl-object-moved-error"></a><span data-ttu-id="c2120-148">Errore curl di tipo "Object Moved"</span><span class="sxs-lookup"><span data-stu-id="c2120-148">curl "Object Moved" error</span></span>

<span data-ttu-id="c2120-149">Se viene restituito da `curl` un errore relativo al parametro `-L` o se viene visualizzato un messaggio di errore che include il testo "Object Moved", provare a usare l'URL completo invece dell'URL di reindirizzamento `aka.ms`:</span><span class="sxs-lookup"><span data-stu-id="c2120-149">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="homebrew-on-macos-installing-older-version"></a><span data-ttu-id="c2120-150">Homebrew in macOS per l'installazione di una versione precedente</span><span class="sxs-lookup"><span data-stu-id="c2120-150">Homebrew on macOS installing older version</span></span>

<span data-ttu-id="c2120-151">La formula `azure-cli` di Homebrew disponibile per macOS è attualmente obsoleta e installerà una versione 1.x dell'interfaccia della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="c2120-151">The Homebrew `azure-cli` formula available for macOS is currently out of date, and will install a 1.x version of the CLI.</span></span> <span data-ttu-id="c2120-152">È possibile verificare quando viene aggiornata controllando `brew info azure-cli`.</span><span class="sxs-lookup"><span data-stu-id="c2120-152">You can see when it is updated by checking `brew info azure-cli`.</span></span>

<span data-ttu-id="c2120-153">Fino all'aggiornamento, [disinstallare la versione precedente](#uninstall_brew) e seguire le [istruzioni di installazione per macOS](#macOS).</span><span class="sxs-lookup"><span data-stu-id="c2120-153">Until then, [uninstall the older version](#uninstall_brew) and follow the [macOS install instructions](#macOS).</span></span>

## <a name="uninstall-cli-1x-versions"></a><span data-ttu-id="c2120-154">Disinstallare le versioni 1.x dell'interfaccia della riga di comando</span><span class="sxs-lookup"><span data-stu-id="c2120-154">Uninstall CLI 1.x versions</span></span>

<span data-ttu-id="c2120-155">Se nel sistema è disponibile una versione 1.x precedente dell'interfaccia della riga di comando, è possibile disinstallarla in base al tipo di installazione usato.</span><span class="sxs-lookup"><span data-stu-id="c2120-155">If you have an earlier CLI 1.x version available on your system, you can uninstall it based upon the type of install used.</span></span>

### <a name="uninstall-with-npm"></a><span data-ttu-id="c2120-156">Eseguire la disinstallazione con npm</span><span class="sxs-lookup"><span data-stu-id="c2120-156">Uninstall with npm</span></span>

<span data-ttu-id="c2120-157">Rimuovere l'interfaccia della riga di comando precedente con `npm uninstall`.</span><span class="sxs-lookup"><span data-stu-id="c2120-157">Remove the older CLI with `npm uninstall`.</span></span>

  ```bash
  npm uninstall -g azure-cli
  ```

### <a name="a-nameuninstallbrewuninstall-with-homebrew-on-macos"></a><span data-ttu-id="c2120-158"><a name="uninstall_brew"/>Eseguire la disinstallazione con Homebrew in macOS</span><span class="sxs-lookup"><span data-stu-id="c2120-158"><a name="uninstall_brew"/>Uninstall with Homebrew on macOS</span></span>

<span data-ttu-id="c2120-159">Rimuovere l'interfaccia della riga di comando precedente con `brew uninstall`.</span><span class="sxs-lookup"><span data-stu-id="c2120-159">Remove the older CLI with `brew uninstall`.</span></span>

```bash
brew uninstall azure-cli
```

### <a name="uninstall-with-distributable"></a><span data-ttu-id="c2120-160">Eseguire la disinstallazione con un file distribuibile</span><span class="sxs-lookup"><span data-stu-id="c2120-160">Uninstall with distributable</span></span>

<span data-ttu-id="c2120-161">Se l'installazione è stata eseguita tramite [MSI](http://aka.ms/webpi-azure-cli) o un [pacchetto macOS](http://aka.ms/mac-azure-cli), usare lo stesso strumento per rimuovere l'installazione.</span><span class="sxs-lookup"><span data-stu-id="c2120-161">If you installed via [MSI](http://aka.ms/webpi-azure-cli) or a [macOS package](http://aka.ms/mac-azure-cli), use the same tool to remove your install.</span></span>

### <a name="uninstall-with-docker"></a><span data-ttu-id="c2120-162">Eseguire la disinstallazione con Docker</span><span class="sxs-lookup"><span data-stu-id="c2120-162">Uninstall with Docker</span></span>

<span data-ttu-id="c2120-163">Se è stata installata un'immagine Docker per usare la versione precedente dell'interfaccia della riga di comando, rimuovere l'immagine ed eventuali contenitori associati.</span><span class="sxs-lookup"><span data-stu-id="c2120-163">If you installed a Docker image to use the earlier CLI version, remove that image and any associated containers.</span></span> <span data-ttu-id="c2120-164">È quindi possibile creare di nuovo i contenitori dopo l'installazione della nuova immagine Docker, come illustrato nelle istruzioni di installazione.</span><span class="sxs-lookup"><span data-stu-id="c2120-164">You can then re-create the containers after installing the new Docker image as described in the install instructions.</span></span>

  ```bash
  docker rmi -f microsoft/azure-cli
  ```

## <a name="update-the-cli"></a><span data-ttu-id="c2120-165">Aggiornare l'interfaccia della riga di comando</span><span class="sxs-lookup"><span data-stu-id="c2120-165">Update the CLI</span></span>

<span data-ttu-id="c2120-166">Per aggiornare l'interfaccia della riga di comando di Azure, usare lo stesso metodo usato per installarla.</span><span class="sxs-lookup"><span data-stu-id="c2120-166">To update the Azure CLI, use the same method that you used to install it.</span></span>

### <a name="update-with-msi"></a><span data-ttu-id="c2120-167">Eseguire l'aggiornamento con MSI</span><span class="sxs-lookup"><span data-stu-id="c2120-167">Update with MSI</span></span>

<span data-ttu-id="c2120-168">Eseguire di nuovo [MSI](https://aka.ms/InstallAzureCliWindows).</span><span class="sxs-lookup"><span data-stu-id="c2120-168">Run the [MSI](https://aka.ms/InstallAzureCliWindows) again.</span></span>

### <a name="update-with-apt-get"></a><span data-ttu-id="c2120-169">Eseguire l'aggiornamento con apt-get</span><span class="sxs-lookup"><span data-stu-id="c2120-169">Update with apt-get</span></span>

<span data-ttu-id="c2120-170">Usare `apt-get upgrade` per aggiornare il pacchetto dell'interfaccia della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="c2120-170">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="c2120-171">Verranno aggiornati tutti i pacchetti installati nel sistema che non hanno subito modifiche relative alle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="c2120-171">This will upgrade all of the installed packages on your system which have not had a dependency change.</span></span>
> <span data-ttu-id="c2120-172">Per eseguire l'aggiornamento solo dell'interfaccia della riga di comando, usare `apt-get install`.</span><span class="sxs-lookup"><span data-stu-id="c2120-172">To upgrade only the CLI, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="update-with-docker"></a><span data-ttu-id="c2120-173">Eseguire l'aggiornamento con Docker</span><span class="sxs-lookup"><span data-stu-id="c2120-173">Update with Docker</span></span>

1. <span data-ttu-id="c2120-174">Aggiornare l'immagine locale con `docker pull`.</span><span class="sxs-lookup"><span data-stu-id="c2120-174">Update your local image with `docker pull`.</span></span>

   ```bash
   docker pull azuresdk/azure-cli-python
   ```

2. <span data-ttu-id="c2120-175">Ottenere i contenitori che usano attualmente l'immagine dell'interfaccia della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="c2120-175">Get the containers currently using the CLI image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

> [!NOTE]
> <span data-ttu-id="c2120-176">Se è stata installata una versione specifica dell'immagine, sarà necessario aggiungere `:<version>` alla fine del nome dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="c2120-176">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

3. <span data-ttu-id="c2120-177">Interrompere e ricreare i contenitori.</span><span class="sxs-lookup"><span data-stu-id="c2120-177">Halt and recreate the containers.</span></span>

   ```bash
   docker stop inspiring_benz
   docker rm inspiring_benz
   docker run azuresdk/azure-cli-python
   ```

### <a name="update-manually"></a><span data-ttu-id="c2120-178">Eseguire l'aggiornamento manualmente</span><span class="sxs-lookup"><span data-stu-id="c2120-178">Update manually</span></span>

<span data-ttu-id="c2120-179">Seguire le istruzioni per l'installazione manuale per [macOS](#macOS) o [Linux](#Linux) per eseguire l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="c2120-179">Follow the manual installation instructions for [macOS](#macOS) or [Linux](#Linux) to update.</span></span>

## <a name="uninstall"></a><span data-ttu-id="c2120-180">Disinstallare</span><span class="sxs-lookup"><span data-stu-id="c2120-180">Uninstall</span></span>

<span data-ttu-id="c2120-181">Se si decide di annullare l'installazione dell'interfaccia della riga di comando,</span><span class="sxs-lookup"><span data-stu-id="c2120-181">If you decide to uninstall the CLI, we're sorry to see you go.</span></span> <span data-ttu-id="c2120-182">eseguire la disinstallazione usando lo stesso metodo usato per installare l'interfaccia della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="c2120-182">You should uninstall using the same method that you used to install the CLI.</span></span>

### <a name="uninstall-with-msi"></a><span data-ttu-id="c2120-183">Eseguire la disinstallazione con MSI</span><span class="sxs-lookup"><span data-stu-id="c2120-183">Uninstall with MSI</span></span>

<span data-ttu-id="c2120-184">Eseguire di nuovo [MSI](https://aka.ms/InstallAzureCliWindows) e scegliere l'opzione per la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="c2120-184">Run the [MSI](https://aka.ms/InstallAzureCliWindows) again and choose uninstall.</span></span>

### <a name="uninstall-with-apt-get"></a><span data-ttu-id="c2120-185">Eseguire la disinstallazione con apt-get</span><span class="sxs-lookup"><span data-stu-id="c2120-185">Uninstall with apt-get</span></span>

<span data-ttu-id="c2120-186">Disinstallare tramite `apt-get remove`:</span><span class="sxs-lookup"><span data-stu-id="c2120-186">Uninstall via `apt-get remove`:</span></span>

  ```bash
  sudo apt-get remove -y azure-cli
  ```

### <a name="uninstall-with-docker"></a><span data-ttu-id="c2120-187">Eseguire la disinstallazione con Docker</span><span class="sxs-lookup"><span data-stu-id="c2120-187">Uninstall with Docker</span></span>

<span data-ttu-id="c2120-188">Se è stata installata un'immagine Docker, sarà necessario rimuovere eventuali contenitori che la eseguono e quindi eliminare l'immagine locale.</span><span class="sxs-lookup"><span data-stu-id="c2120-188">If you installed a docker image, you will need to remove any containers running it, and then delete the local image.</span></span>

1. <span data-ttu-id="c2120-189">Ottenere i contenitori che eseguono l'immagine azure-cli.</span><span class="sxs-lookup"><span data-stu-id="c2120-189">Get the containers which are running the azure-cli image.</span></span>

  ```bash
  docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
  ```

  ```output
  CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
  34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
  ```

2. <span data-ttu-id="c2120-190">Eliminare eventuali contenitori con l'immagine dell'interfaccia della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="c2120-190">Delete any containers with the CLI image.</span></span>

  ```bash
  docker rm 34a868beb2ab
  ```

3. <span data-ttu-id="c2120-191">Rimuovere l'immagine dell'interfaccia della riga di comando installata in locale.</span><span class="sxs-lookup"><span data-stu-id="c2120-191">Remove the locally installed CLI image.</span></span>

  ```bash
  docker rmi azuresdk/azure-cli-python
  ```

> [!NOTE]
> <span data-ttu-id="c2120-192">Se è stata installata una versione specifica dell'immagine, sarà necessario aggiungere `:<version>` alla fine del nome dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="c2120-192">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

### <a name="uninstall-manually"></a><span data-ttu-id="c2120-193">Eseguire la disinstallazione manualmente</span><span class="sxs-lookup"><span data-stu-id="c2120-193">Uninstall manually</span></span>

<span data-ttu-id="c2120-194">Se è stato usato lo script all'indirizzo https://aka.ms/InstallAzureCli per installare l'interfaccia della riga di comando, è possibile disinstallarla eseguendo questa procedura.</span><span class="sxs-lookup"><span data-stu-id="c2120-194">If you used the script at https://aka.ms/InstallAzureCli to install the CLI, you can uninstall it with these steps.</span></span>

1. <span data-ttu-id="c2120-195">Rimuovere i file installati.</span><span class="sxs-lookup"><span data-stu-id="c2120-195">Remove the installed files.</span></span>

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. <span data-ttu-id="c2120-196">Eliminare la riga `<install location>/lib/azure-cli/az.completion` da `<install location>/.bash_profile`.</span><span class="sxs-lookup"><span data-stu-id="c2120-196">Delete the line `<install location>/lib/azure-cli/az.completion` from `<install location>/.bash_profile`.</span></span>

> [!Note]
> <span data-ttu-id="c2120-197">Il percorso di installazione predefinito è `/Users/<username>`.</span><span class="sxs-lookup"><span data-stu-id="c2120-197">The default install location is `/Users/<username>`.</span></span>

## <a name="report-cli-issues-and-feedback"></a><span data-ttu-id="c2120-198">Segnalazione di problemi e suggerimenti relativi all'interfaccia della riga di comando</span><span class="sxs-lookup"><span data-stu-id="c2120-198">Report CLI issues and feedback</span></span>

<span data-ttu-id="c2120-199">Se si rilevano bug con lo strumento, segnalare un problema nella sezione [Issues](https://github.com/Azure/azure-cli/issues) (Problemi) del repository GitHub.</span><span class="sxs-lookup"><span data-stu-id="c2120-199">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-cli/issues) section of our GitHub repository.</span></span>
<span data-ttu-id="c2120-200">Per inserire commenti e suggerimenti dalla riga di comando, usare il comando `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="c2120-200">To provide feedback from the command line, use the `az feedback` command.</span></span>
