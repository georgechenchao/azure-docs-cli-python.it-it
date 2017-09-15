---
title: Installare l'interfaccia della riga di comando di Azure 2.0.
description: Documenti di riferimento per l'installazione dell'interfaccia della riga di comando di Azure 2.0
keywords: interfaccia della riga di comando di Azure, installare l'interfaccia della riga di comando di Azure, interfaccia della riga di comando di Azure con Python, informazioni di riferimento sull'interfaccia della riga di comando di Azure
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
ms.openlocfilehash: a61f47076854d0ff0a7056f82240794b7533fe3e
ms.sourcegitcommit: 3db5fb207db551a0d3fe0a88fe09e8f5e2ec184d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/14/2017
---
# <a name="install-azure-cli-20"></a><span data-ttu-id="5eddc-104">Installare l'interfaccia della riga di comando di Azure 2.0</span><span class="sxs-lookup"><span data-stu-id="5eddc-104">Install Azure CLI 2.0</span></span>

<span data-ttu-id="5eddc-105">È possibile installare oggi stesso l'interfaccia della riga di comando di Azure,</span><span class="sxs-lookup"><span data-stu-id="5eddc-105">Install the new version of the Azure CLI today!</span></span>
<span data-ttu-id="5eddc-106">che è stata migliorata e aggiornata per offrire un'esperienza ottimale della riga di comando nativa per la gestione delle risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="5eddc-106">We've improved and updated it to provide a great native command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="5eddc-107">Può essere usata in macOS, Linux e Windows.</span><span class="sxs-lookup"><span data-stu-id="5eddc-107">It can be used on macOS, Linux, and Windows.</span></span>
<span data-ttu-id="5eddc-108">Per informazioni sulla versione più recente, vedere le [note sulla versione](release-notes-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="5eddc-108">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

> [!NOTE]
> <span data-ttu-id="5eddc-109">Se è necessaria la versione precedente dell'interfaccia della riga di comando di Azure, vedere [Installare l'interfaccia della riga di comando di Azure 1.0](/azure/cli-install-nodejs).</span><span class="sxs-lookup"><span data-stu-id="5eddc-109">If you need the previous version of the Azure CLI, here's how to [install Azure CLI 1.0](/azure/cli-install-nodejs).</span></span>

## <a name="a-namemacosinstall-on-macos"></a><span data-ttu-id="5eddc-110"><a name="macOS"/>Eseguire l'installazione in macOS</span><span class="sxs-lookup"><span data-stu-id="5eddc-110"><a name="macOS"/>Install on macOS</span></span>

1. <span data-ttu-id="5eddc-111">Installare l'interfaccia della riga di comando di Azure 2.0 con `curl`.</span><span class="sxs-lookup"><span data-stu-id="5eddc-111">Install Azure CLI 2.0 with `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. <span data-ttu-id="5eddc-112">Potrebbe essere necessario riavviare la shell per rendere effettive alcune modifiche apportate.</span><span class="sxs-lookup"><span data-stu-id="5eddc-112">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```
   
3. <span data-ttu-id="5eddc-113">Eseguire l'interfaccia della riga di comando dal prompt dei comandi con il comando `az`.</span><span class="sxs-lookup"><span data-stu-id="5eddc-113">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-windows"></a><span data-ttu-id="5eddc-114">Eseguire l'installazione in Windows</span><span class="sxs-lookup"><span data-stu-id="5eddc-114">Install on Windows</span></span>

<span data-ttu-id="5eddc-115">È possibile installare l'interfaccia della riga di comando di Azure 2.0 con MSI e usarla nella riga di comando di Windows, oppure è possibile installare l'interfaccia della riga di comando con `apt-get` su Bash in Ubuntu in Windows.</span><span class="sxs-lookup"><span data-stu-id="5eddc-115">You can install Azure CLI 2.0 with the MSI and use it in the Windows command-line, or you can install the CLI with `apt-get` on Bash on Ubuntu on Windows.</span></span>

### <a name="install-with-msi-for-the-windows-command-line"></a><span data-ttu-id="5eddc-116">Eseguire l'installazione con MSI per la riga di comando di Windows</span><span class="sxs-lookup"><span data-stu-id="5eddc-116">Install with MSI for the Windows command-line</span></span> 

<span data-ttu-id="5eddc-117">Per installare l'interfaccia della riga di comando in Windows e usarla nella riga di comando di Windows, scaricare ed eseguire [MSI](https://aka.ms/InstallAzureCliWindows).</span><span class="sxs-lookup"><span data-stu-id="5eddc-117">To install the CLI on Windows and use it in the Windows command-line, download and run the [MSI](https://aka.ms/InstallAzureCliWindows).</span></span>

### <a name="install-with-apt-get-for-bash-on-ubuntu-on-windows"></a><span data-ttu-id="5eddc-118">Eseguire l'installazione con apt-get per Bash in Ubuntu in Windows</span><span class="sxs-lookup"><span data-stu-id="5eddc-118">Install with apt-get for Bash on Ubuntu on Windows</span></span>

1. <span data-ttu-id="5eddc-119">Se Bash in Windows non è disponibile, [installarlo](https://msdn.microsoft.com/commandline/wsl/install_guide).</span><span class="sxs-lookup"><span data-stu-id="5eddc-119">If you don't have Bash on Windows, [install it](https://msdn.microsoft.com/commandline/wsl/install_guide).</span></span>

2. <span data-ttu-id="5eddc-120">Aprire la shell di Bash.</span><span class="sxs-lookup"><span data-stu-id="5eddc-120">Open the Bash shell.</span></span>

3. <span data-ttu-id="5eddc-121">Modificare l'elenco di origini.</span><span class="sxs-lookup"><span data-stu-id="5eddc-121">Modify your sources list.</span></span>

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. <span data-ttu-id="5eddc-122">Eseguire i comandi sudo seguenti:</span><span class="sxs-lookup"><span data-stu-id="5eddc-122">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

5.  <span data-ttu-id="5eddc-123">Eseguire l'interfaccia della riga di comando dal prompt dei comandi con il comando `az`.</span><span class="sxs-lookup"><span data-stu-id="5eddc-123">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-debianubuntu-with-apt-get"></a><span data-ttu-id="5eddc-124">Eseguire l'installazione in Debian/Ubuntu con apt-get</span><span class="sxs-lookup"><span data-stu-id="5eddc-124">Install on Debian/Ubuntu with apt-get</span></span>

<span data-ttu-id="5eddc-125">Per i sistemi basati su Debian/Ubuntu, è possibile installare l'interfaccia della riga di comando di Azure 2.0 tramite `apt-get`.</span><span class="sxs-lookup"><span data-stu-id="5eddc-125">For Debian/Ubuntu based systems, you can install Azure CLI 2.0 via `apt-get`.</span></span>

1. <span data-ttu-id="5eddc-126">Modificare l'elenco di origini:</span><span class="sxs-lookup"><span data-stu-id="5eddc-126">Modify your sources list:</span></span>
 
   - <span data-ttu-id="5eddc-127">Sistema a 32 bit</span><span class="sxs-lookup"><span data-stu-id="5eddc-127">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="5eddc-128">Sistema a 64 bit</span><span class="sxs-lookup"><span data-stu-id="5eddc-128">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="5eddc-129">Eseguire i comandi sudo seguenti:</span><span class="sxs-lookup"><span data-stu-id="5eddc-129">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

3.  <span data-ttu-id="5eddc-130">Eseguire l'interfaccia della riga di comando dal prompt dei comandi con il comando `az`.</span><span class="sxs-lookup"><span data-stu-id="5eddc-130">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-rhel-fedora-and-centos-with-yum"></a><span data-ttu-id="5eddc-131">Eseguire l'installazione in RHEL, Fedora e CentOS con yum</span><span class="sxs-lookup"><span data-stu-id="5eddc-131">Install on RHEL, Fedora, and CentOS with yum</span></span>

<span data-ttu-id="5eddc-132">Per le distribuzioni basate su RedHat e contenenti l'utilità di gestione pacchetti `yum`, è possibile installare l'interfaccia della riga di comando di Azure 2.0 tramite `yum`.</span><span class="sxs-lookup"><span data-stu-id="5eddc-132">For any distribution which is based off of RedHat and contains the `yum` package manager, you can install Azure CLI 2.0 via `yum`.</span></span>

1. <span data-ttu-id="5eddc-133">Importare la chiave del repository Microsoft:</span><span class="sxs-lookup"><span data-stu-id="5eddc-133">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="5eddc-134">Creare le informazioni del repository `azure-cli` locale:</span><span class="sxs-lookup"><span data-stu-id="5eddc-134">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="5eddc-135">Aggiornare l'indice del pacchetto `yum` ed eseguire l'installazione:</span><span class="sxs-lookup"><span data-stu-id="5eddc-135">Update the `yum` package index and install:</span></span>

   ```bash
   yum check-update
   sudo yum install azure-cli
   ```

4. <span data-ttu-id="5eddc-136">Eseguire l'interfaccia della riga di comando dal prompt dei comandi con il comando `az`.</span><span class="sxs-lookup"><span data-stu-id="5eddc-136">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-opensuse-and-sle-with-zypper"></a><span data-ttu-id="5eddc-137">Eseguire l'installazione in openSUSE e SLE con zypper</span><span class="sxs-lookup"><span data-stu-id="5eddc-137">Install on openSUSE and SLE with zypper</span></span>

1. <span data-ttu-id="5eddc-138">Importare la chiave del repository Microsoft:</span><span class="sxs-lookup"><span data-stu-id="5eddc-138">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="5eddc-139">Creare le informazioni del repository `azure-cli` locale:</span><span class="sxs-lookup"><span data-stu-id="5eddc-139">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="5eddc-140">Aggiornare l'indice del pacchetto `zypper` ed eseguire l'installazione:</span><span class="sxs-lookup"><span data-stu-id="5eddc-140">Update the `zypper` package index and install:</span></span>

   ```bash
   sudo zypper refresh
   sudo zypper install azure-cli
   ```

4. <span data-ttu-id="5eddc-141">Eseguire l'interfaccia della riga di comando dal prompt dei comandi con il comando `az`.</span><span class="sxs-lookup"><span data-stu-id="5eddc-141">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-with-docker"></a><span data-ttu-id="5eddc-142">Eseguire l'installazione con Docker</span><span class="sxs-lookup"><span data-stu-id="5eddc-142">Install with Docker</span></span>

<span data-ttu-id="5eddc-143">È disponibile un'immagine Docker preconfigurata con l'interfaccia della riga di comando di Azure 2.0.</span><span class="sxs-lookup"><span data-stu-id="5eddc-143">We maintain a Docker image preconfigured with the Azure CLI 2.0.</span></span>

<span data-ttu-id="5eddc-144">Installare l'interfaccia della riga di comando con `docker run`.</span><span class="sxs-lookup"><span data-stu-id="5eddc-144">Install the CLI using `docker run`.</span></span>

   ```bash
   docker run azuresdk/azure-cli-python:<version>
   ```

<span data-ttu-id="5eddc-145">Per le versioni disponibili, vedere i [tag di Docker](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/).</span><span class="sxs-lookup"><span data-stu-id="5eddc-145">See our [Docker tags](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) for available versions.</span></span>

<span data-ttu-id="5eddc-146">L'interfaccia della riga di comando viene installata nell'immagine come il comando `az` in `/usr/local/bin`.</span><span class="sxs-lookup"><span data-stu-id="5eddc-146">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span>

> [!NOTE]
> <span data-ttu-id="5eddc-147">Per acquisire le chiavi SSH dall'ambiente utente, è possibile usare `-v ${HOME}:/root` per montare $HOME come `/root`.</span><span class="sxs-lookup"><span data-stu-id="5eddc-147">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>

> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

## <a name="a-namelinuxinstall-on-linux-without-apt-get"></a><span data-ttu-id="5eddc-148"><a name="Linux"/>Eseguire l'installazione in Linux senza apt-get</span><span class="sxs-lookup"><span data-stu-id="5eddc-148"><a name="Linux"/>Install on Linux without apt-get</span></span>

<span data-ttu-id="5eddc-149">È consigliabile installare l'interfaccia della riga di comando con un'utilità di gestione pacchetti, se possibile.</span><span class="sxs-lookup"><span data-stu-id="5eddc-149">It is recommended that you install the CLI with a package manager if you are able to.</span></span> <span data-ttu-id="5eddc-150">Per le distribuzioni a cui non viene fornito un pacchetto, è possibile eseguire l'installazione manuale.</span><span class="sxs-lookup"><span data-stu-id="5eddc-150">For distributions which do not have a package provided for them, you can manually install.</span></span>

1. <span data-ttu-id="5eddc-151">Installare i prerequisiti in base alla distribuzione Linux specifica.</span><span class="sxs-lookup"><span data-stu-id="5eddc-151">Install the prerequisites based on your Linux distribution.</span></span>

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

<span data-ttu-id="5eddc-152">Se la distribuzione non è inclusa nell'elenco precedente, sarà necessario installare [Python](https://www.python.org/downloads/), [libffi](https://sourceware.org/libffi/), e [OpenSSL](https://www.openssl.org/source/).</span><span class="sxs-lookup"><span data-stu-id="5eddc-152">If your distribution is not listed above, you will need to install [Python](https://www.python.org/downloads/), [libffi](https://sourceware.org/libffi/), and [OpenSSL](https://www.openssl.org/source/).</span></span>

2. <span data-ttu-id="5eddc-153">Installare l'interfaccia della riga di comando con `curl`.</span><span class="sxs-lookup"><span data-stu-id="5eddc-153">Install the CLI with  `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. <span data-ttu-id="5eddc-154">Potrebbe essere necessario riavviare la shell per rendere effettive alcune modifiche apportate.</span><span class="sxs-lookup"><span data-stu-id="5eddc-154">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```

4. <span data-ttu-id="5eddc-155">Eseguire l'interfaccia della riga di comando dal prompt dei comandi con il comando `az`.</span><span class="sxs-lookup"><span data-stu-id="5eddc-155">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="5eddc-156">Risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="5eddc-156">Troubleshooting</span></span>

<span data-ttu-id="5eddc-157">Se si verifica un problema durante l'installazione dell'interfaccia della riga di comando, controllare questa sezione per verificare se include il caso specifico.</span><span class="sxs-lookup"><span data-stu-id="5eddc-157">If you encounter an issue during CLI install, check this section to see if your particular case is covered.</span></span> <span data-ttu-id="5eddc-158">Se il problema non è incluso in questa sezione, [segnalare il problema su Github](https://github.com/Azure/azure-cli/issues).</span><span class="sxs-lookup"><span data-stu-id="5eddc-158">If your issue is not here, please [file a Github issue](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="curl-object-moved-error"></a><span data-ttu-id="5eddc-159">Errore curl di tipo "Object Moved"</span><span class="sxs-lookup"><span data-stu-id="5eddc-159">curl "Object Moved" error</span></span>

<span data-ttu-id="5eddc-160">Se viene restituito da `curl` un errore relativo al parametro `-L` o se viene visualizzato un messaggio di errore che include il testo "Object Moved", provare a usare l'URL completo invece dell'URL di reindirizzamento `aka.ms`:</span><span class="sxs-lookup"><span data-stu-id="5eddc-160">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="homebrew-on-macos-installing-older-version"></a><span data-ttu-id="5eddc-161">Homebrew in macOS per l'installazione di una versione precedente</span><span class="sxs-lookup"><span data-stu-id="5eddc-161">Homebrew on macOS installing older version</span></span>

<span data-ttu-id="5eddc-162">La formula `azure-cli` di Homebrew disponibile per macOS è attualmente obsoleta e installerà una versione 1.x dell'interfaccia della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="5eddc-162">The Homebrew `azure-cli` formula available for macOS is currently out of date, and will install a 1.x version of the CLI.</span></span> <span data-ttu-id="5eddc-163">È possibile verificare quando viene aggiornata controllando `brew info azure-cli`.</span><span class="sxs-lookup"><span data-stu-id="5eddc-163">You can see when it is updated by checking `brew info azure-cli`.</span></span>

<span data-ttu-id="5eddc-164">Fino all'aggiornamento, [disinstallare la versione precedente](#uninstall_brew) e seguire le [istruzioni di installazione per macOS](#macOS).</span><span class="sxs-lookup"><span data-stu-id="5eddc-164">Until then, [uninstall the older version](#uninstall_brew) and follow the [macOS install instructions](#macOS).</span></span>

## <a name="uninstall-cli-1x-versions"></a><span data-ttu-id="5eddc-165">Disinstallare le versioni 1.x dell'interfaccia della riga di comando</span><span class="sxs-lookup"><span data-stu-id="5eddc-165">Uninstall CLI 1.x versions</span></span>

<span data-ttu-id="5eddc-166">Se nel sistema è disponibile una versione 1.x precedente dell'interfaccia della riga di comando, è possibile disinstallarla in base al tipo di installazione usato.</span><span class="sxs-lookup"><span data-stu-id="5eddc-166">If you have an earlier CLI 1.x version available on your system, you can uninstall it based upon the type of install used.</span></span>

### <a name="uninstall-with-npm"></a><span data-ttu-id="5eddc-167">Eseguire la disinstallazione con npm</span><span class="sxs-lookup"><span data-stu-id="5eddc-167">Uninstall with npm</span></span>

<span data-ttu-id="5eddc-168">Rimuovere l'interfaccia della riga di comando precedente con `npm uninstall`.</span><span class="sxs-lookup"><span data-stu-id="5eddc-168">Remove the older CLI with `npm uninstall`.</span></span>

  ```bash
  npm uninstall -g azure-cli
  ```

### <a name="a-nameuninstallbrewuninstall-with-homebrew-on-macos"></a><span data-ttu-id="5eddc-169"><a name="uninstall_brew"/>Eseguire la disinstallazione con Homebrew in macOS</span><span class="sxs-lookup"><span data-stu-id="5eddc-169"><a name="uninstall_brew"/>Uninstall with Homebrew on macOS</span></span>

<span data-ttu-id="5eddc-170">Rimuovere l'interfaccia della riga di comando precedente con `brew uninstall`.</span><span class="sxs-lookup"><span data-stu-id="5eddc-170">Remove the older CLI with `brew uninstall`.</span></span>

```bash
brew uninstall azure-cli
```

### <a name="uninstall-with-distributable"></a><span data-ttu-id="5eddc-171">Eseguire la disinstallazione con un file distribuibile</span><span class="sxs-lookup"><span data-stu-id="5eddc-171">Uninstall with distributable</span></span>

<span data-ttu-id="5eddc-172">Se l'installazione è stata eseguita tramite [MSI](http://aka.ms/webpi-azure-cli) o un [pacchetto macOS](http://aka.ms/mac-azure-cli), usare lo stesso strumento per rimuovere l'installazione.</span><span class="sxs-lookup"><span data-stu-id="5eddc-172">If you installed via [MSI](http://aka.ms/webpi-azure-cli) or a [macOS package](http://aka.ms/mac-azure-cli), use the same tool to remove your install.</span></span>

### <a name="uninstall-with-docker"></a><span data-ttu-id="5eddc-173">Eseguire la disinstallazione con Docker</span><span class="sxs-lookup"><span data-stu-id="5eddc-173">Uninstall with Docker</span></span>

<span data-ttu-id="5eddc-174">Se è stata installata un'immagine Docker per usare la versione precedente dell'interfaccia della riga di comando, rimuovere l'immagine ed eventuali contenitori associati.</span><span class="sxs-lookup"><span data-stu-id="5eddc-174">If you installed a Docker image to use the earlier CLI version, remove that image and any associated containers.</span></span> <span data-ttu-id="5eddc-175">È quindi possibile creare di nuovo i contenitori dopo l'installazione della nuova immagine Docker, come illustrato nelle istruzioni di installazione.</span><span class="sxs-lookup"><span data-stu-id="5eddc-175">You can then re-create the containers after installing the new Docker image as described in the install instructions.</span></span>

  ```bash
  docker rmi -f microsoft/azure-cli
  ```

## <a name="update-the-cli"></a><span data-ttu-id="5eddc-176">Aggiornare l'interfaccia della riga di comando</span><span class="sxs-lookup"><span data-stu-id="5eddc-176">Update the CLI</span></span>

<span data-ttu-id="5eddc-177">Per aggiornare l'interfaccia della riga di comando di Azure, usare lo stesso metodo usato per installarla.</span><span class="sxs-lookup"><span data-stu-id="5eddc-177">To update the Azure CLI, use the same method that you used to install it.</span></span>

### <a name="update-with-msi"></a><span data-ttu-id="5eddc-178">Eseguire l'aggiornamento con MSI</span><span class="sxs-lookup"><span data-stu-id="5eddc-178">Update with MSI</span></span>

<span data-ttu-id="5eddc-179">Eseguire di nuovo [MSI](https://aka.ms/InstallAzureCliWindows).</span><span class="sxs-lookup"><span data-stu-id="5eddc-179">Run the [MSI](https://aka.ms/InstallAzureCliWindows) again.</span></span>

### <a name="update-with-apt-get"></a><span data-ttu-id="5eddc-180">Eseguire l'aggiornamento con apt-get</span><span class="sxs-lookup"><span data-stu-id="5eddc-180">Update with apt-get</span></span>

<span data-ttu-id="5eddc-181">Usare `apt-get upgrade` per aggiornare il pacchetto dell'interfaccia della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="5eddc-181">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="5eddc-182">Verranno aggiornati tutti i pacchetti installati nel sistema che non hanno subito modifiche relative alle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="5eddc-182">This will upgrade all of the installed packages on your system which have not had a dependency change.</span></span>
> <span data-ttu-id="5eddc-183">Per eseguire l'aggiornamento solo dell'interfaccia della riga di comando, usare `apt-get install`.</span><span class="sxs-lookup"><span data-stu-id="5eddc-183">To upgrade only the CLI, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="update-with-docker"></a><span data-ttu-id="5eddc-184">Eseguire l'aggiornamento con Docker</span><span class="sxs-lookup"><span data-stu-id="5eddc-184">Update with Docker</span></span>

1. <span data-ttu-id="5eddc-185">Aggiornare l'immagine locale con `docker pull`.</span><span class="sxs-lookup"><span data-stu-id="5eddc-185">Update your local image with `docker pull`.</span></span>

   ```bash
   docker pull azuresdk/azure-cli-python
   ```

2. <span data-ttu-id="5eddc-186">Ottenere i contenitori che usano attualmente l'immagine dell'interfaccia della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="5eddc-186">Get the containers currently using the CLI image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

> [!NOTE]
> <span data-ttu-id="5eddc-187">Se è stata installata una versione specifica dell'immagine, sarà necessario aggiungere `:<version>` alla fine del nome dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="5eddc-187">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

3. <span data-ttu-id="5eddc-188">Interrompere e ricreare i contenitori.</span><span class="sxs-lookup"><span data-stu-id="5eddc-188">Halt and recreate the containers.</span></span>

   ```bash
   docker stop inspiring_benz
   docker rm inspiring_benz
   docker run azuresdk/azure-cli-python
   ```

### <a name="update-manually"></a><span data-ttu-id="5eddc-189">Eseguire l'aggiornamento manualmente</span><span class="sxs-lookup"><span data-stu-id="5eddc-189">Update manually</span></span>

<span data-ttu-id="5eddc-190">Seguire le istruzioni per l'installazione manuale per [macOS](#macOS) o [Linux](#Linux) per eseguire l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="5eddc-190">Follow the manual installation instructions for [macOS](#macOS) or [Linux](#Linux) to update.</span></span>

## <a name="uninstall"></a><span data-ttu-id="5eddc-191">Disinstallare</span><span class="sxs-lookup"><span data-stu-id="5eddc-191">Uninstall</span></span>

<span data-ttu-id="5eddc-192">Se si decide di annullare l'installazione dell'interfaccia della riga di comando,</span><span class="sxs-lookup"><span data-stu-id="5eddc-192">If you decide to uninstall the CLI, we're sorry to see you go.</span></span> <span data-ttu-id="5eddc-193">eseguire la disinstallazione usando lo stesso metodo usato per installare l'interfaccia della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="5eddc-193">You should uninstall using the same method that you used to install the CLI.</span></span>

### <a name="uninstall-with-msi"></a><span data-ttu-id="5eddc-194">Eseguire la disinstallazione con MSI</span><span class="sxs-lookup"><span data-stu-id="5eddc-194">Uninstall with MSI</span></span>

<span data-ttu-id="5eddc-195">Eseguire di nuovo [MSI](https://aka.ms/InstallAzureCliWindows) e scegliere l'opzione per la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="5eddc-195">Run the [MSI](https://aka.ms/InstallAzureCliWindows) again and choose uninstall.</span></span>

### <a name="uninstall-with-apt-get"></a><span data-ttu-id="5eddc-196">Eseguire la disinstallazione con apt-get</span><span class="sxs-lookup"><span data-stu-id="5eddc-196">Uninstall with apt-get</span></span>

<span data-ttu-id="5eddc-197">Disinstallare tramite `apt-get remove`:</span><span class="sxs-lookup"><span data-stu-id="5eddc-197">Uninstall via `apt-get remove`:</span></span>

  ```bash
  sudo apt-get remove -y azure-cli
  ```

### <a name="uninstall-with-docker"></a><span data-ttu-id="5eddc-198">Eseguire la disinstallazione con Docker</span><span class="sxs-lookup"><span data-stu-id="5eddc-198">Uninstall with Docker</span></span>

<span data-ttu-id="5eddc-199">Se è stata installata un'immagine Docker, sarà necessario rimuovere eventuali contenitori che la eseguono e quindi eliminare l'immagine locale.</span><span class="sxs-lookup"><span data-stu-id="5eddc-199">If you installed a docker image, you will need to remove any containers running it, and then delete the local image.</span></span>

1. <span data-ttu-id="5eddc-200">Ottenere i contenitori che eseguono l'immagine azure-cli.</span><span class="sxs-lookup"><span data-stu-id="5eddc-200">Get the containers which are running the azure-cli image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

2. <span data-ttu-id="5eddc-201">Eliminare eventuali contenitori con l'immagine dell'interfaccia della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="5eddc-201">Delete any containers with the CLI image.</span></span>

   ```bash
   docker rm 34a868beb2ab
   ```

3. <span data-ttu-id="5eddc-202">Rimuovere l'immagine dell'interfaccia della riga di comando installata in locale.</span><span class="sxs-lookup"><span data-stu-id="5eddc-202">Remove the locally installed CLI image.</span></span>

   ```bash
   docker rmi azuresdk/azure-cli-python
   ```

> [!NOTE]
> <span data-ttu-id="5eddc-203">Se è stata installata una versione specifica dell'immagine, sarà necessario aggiungere `:<version>` alla fine del nome dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="5eddc-203">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

### <a name="uninstall-manually"></a><span data-ttu-id="5eddc-204">Eseguire la disinstallazione manualmente</span><span class="sxs-lookup"><span data-stu-id="5eddc-204">Uninstall manually</span></span>

<span data-ttu-id="5eddc-205">Se è stato usato lo script all'indirizzo https://aka.ms/InstallAzureCli per installare l'interfaccia della riga di comando, è possibile disinstallarla eseguendo questa procedura.</span><span class="sxs-lookup"><span data-stu-id="5eddc-205">If you used the script at https://aka.ms/InstallAzureCli to install the CLI, you can uninstall it with these steps.</span></span>

1. <span data-ttu-id="5eddc-206">Rimuovere i file installati.</span><span class="sxs-lookup"><span data-stu-id="5eddc-206">Remove the installed files.</span></span>

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. <span data-ttu-id="5eddc-207">Eliminare la riga `<install location>/lib/azure-cli/az.completion` da `<install location>/.bash_profile`.</span><span class="sxs-lookup"><span data-stu-id="5eddc-207">Delete the line `<install location>/lib/azure-cli/az.completion` from `<install location>/.bash_profile`.</span></span>

> [!Note]
> <span data-ttu-id="5eddc-208">Il percorso di installazione predefinito è `/Users/<username>`.</span><span class="sxs-lookup"><span data-stu-id="5eddc-208">The default install location is `/Users/<username>`.</span></span>

## <a name="report-cli-issues-and-feedback"></a><span data-ttu-id="5eddc-209">Segnalazione di problemi e suggerimenti relativi all'interfaccia della riga di comando</span><span class="sxs-lookup"><span data-stu-id="5eddc-209">Report CLI issues and feedback</span></span>

<span data-ttu-id="5eddc-210">Se si rilevano bug con lo strumento, segnalare un problema nella sezione [Issues](https://github.com/Azure/azure-cli/issues) (Problemi) del repository GitHub.</span><span class="sxs-lookup"><span data-stu-id="5eddc-210">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-cli/issues) section of our GitHub repository.</span></span>
<span data-ttu-id="5eddc-211">Per inserire commenti e suggerimenti dalla riga di comando, usare il comando `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="5eddc-211">To provide feedback from the command line, use the `az feedback` command.</span></span>
