---
title: Installare l&quot;interfaccia della riga di comando di Azure 2.0.
description: Documenti di riferimento per l&quot;interfaccia della riga di comando di Azure 2.0
keywords: Interfaccia della riga di comando di Azure 2.0, informazioni di riferimento sull&quot;interfaccia della riga di comando di Azure 2.0, installare l&quot;interfaccia della riga di comando di Azure 2.0, interfaccia della riga di comando di Azure con Python, disinstallare l&quot;interfaccia della riga di comando di Azure 2.0
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 04/06/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ea5c0ee1-c530-4a1e-a83f-e1be71f6d416
ms.openlocfilehash: 7065ed5270ef9bfc70beea81d0bc442a7b4df38c
ms.sourcegitcommit: c077bd5cbe07f7225714c41714d3981fa0d9928f
ms.contentlocale: it-IT
ms.lasthandoff: 05/16/2017
---
# <a name="install-azure-cli-20"></a><span data-ttu-id="63286-104">Installare l'interfaccia della riga di comando di Azure 2.0</span><span class="sxs-lookup"><span data-stu-id="63286-104">Install Azure CLI 2.0</span></span>

<span data-ttu-id="63286-105">È possibile installare oggi stesso l'interfaccia della riga di comando di Azure,</span><span class="sxs-lookup"><span data-stu-id="63286-105">Install the new version of the Azure CLI today!</span></span>
<span data-ttu-id="63286-106">che è stata migliorata e aggiornata per offrire un'esperienza ottimale della riga di comando nativa per la gestione delle risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="63286-106">We've improved and updated it to provide a great native command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="63286-107">Può essere usata in macOS, Linux e Windows.</span><span class="sxs-lookup"><span data-stu-id="63286-107">It can be used on macOS, Linux, and Windows.</span></span>
<span data-ttu-id="63286-108">Per informazioni sulla versione più recente, vedere le [note sulla versione](release-notes-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="63286-108">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

> [!NOTE]
> <span data-ttu-id="63286-109">Se è necessaria la versione precedente dell'interfaccia della riga di comando di Azure, vedere [Installare l'interfaccia della riga di comando 1.0 di Azure](/azure/cli-install-nodejs).</span><span class="sxs-lookup"><span data-stu-id="63286-109">If you need the previous version of the Azure CLI, here's how to [install Azure 1.0](/azure/cli-install-nodejs).</span></span>

## <a name="macos"></a><span data-ttu-id="63286-110">macOS</span><span class="sxs-lookup"><span data-stu-id="63286-110">macOS</span></span>

1. <span data-ttu-id="63286-111">Installare l'interfaccia della riga di comando di Azure 2.0 con il solo comando `curl`.</span><span class="sxs-lookup"><span data-stu-id="63286-111">Install Azure CLI 2.0 with one `curl` command.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. <span data-ttu-id="63286-112">Potrebbe essere necessario riavviare la shell dei comandi per rendere effettive alcune modifiche apportate.</span><span class="sxs-lookup"><span data-stu-id="63286-112">You may have to restart your command shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```
   
3. <span data-ttu-id="63286-113">Eseguire l'interfaccia della riga di comando di Azure 2.0 dal prompt dei comandi con il comando `az`.</span><span class="sxs-lookup"><span data-stu-id="63286-113">Run Azure CLI 2.0 from the command prompt with the `az` command.</span></span>

> [!Note]
> <span data-ttu-id="63286-114">Quando si esegue l'installazione con InstallAzureCli, `az component update` non è supportato.</span><span class="sxs-lookup"><span data-stu-id="63286-114">When you install with InstallAzureCli, `az component update` isn't supported.</span></span>
> <span data-ttu-id="63286-115">Per eseguire l'aggiornamento all'interfaccia della riga di comando più recente, eseguire di nuovo `curl -L https://aka.ms/InstallAzureCli | bash`.</span><span class="sxs-lookup"><span data-stu-id="63286-115">To update to the latest CLI, run `curl -L https://aka.ms/InstallAzureCli | bash` again.</span></span>
> 
> <span data-ttu-id="63286-116">Per eseguire la disinstallazione, vedere le [istruzioni per la disinstallazione manuale](#uninstall).</span><span class="sxs-lookup"><span data-stu-id="63286-116">To uninstall, see the [manual uninstall instructions](#uninstall).</span></span>

## <a name="windows"></a><span data-ttu-id="63286-117">Windows</span><span class="sxs-lookup"><span data-stu-id="63286-117">Windows</span></span>

<span data-ttu-id="63286-118">È possibile installare l'interfaccia della riga di comando con MSI e usarla nella riga di comando di Windows, oppure è possibile installare l'interfaccia della riga di comando con apt-get su Bash di Ubuntu in Windows.</span><span class="sxs-lookup"><span data-stu-id="63286-118">You can install the CLI with the MSI and use it in the Windows command-line, or you can install the CLI with apt-get on Bash on Ubuntu on Windows.</span></span>

### <a name="msi-for-the-windows-command-line"></a><span data-ttu-id="63286-119">MSI per la riga di comando di Windows</span><span class="sxs-lookup"><span data-stu-id="63286-119">MSI for the Windows command-line</span></span> 

<span data-ttu-id="63286-120">Per installare l'interfaccia della riga di comando in Windows e usarla nella riga di comando di Windows, scaricare ed eseguire [MSI](https://aka.ms/InstallAzureCliWindows).</span><span class="sxs-lookup"><span data-stu-id="63286-120">To install the CLI on Windows and use it in the Windows command-line, download and run the [msi](https://aka.ms/InstallAzureCliWindows).</span></span>

> [!NOTE]
> <span data-ttu-id="63286-121">Quando si esegue l'installazione con MSI, `az component` non è supportato.</span><span class="sxs-lookup"><span data-stu-id="63286-121">When you install with the msi, `az component` isn't supported.</span></span>
> <span data-ttu-id="63286-122">Per eseguire l'aggiornamento all'interfaccia della riga di comando più recente, eseguire di nuovo [MSI](https://aka.ms/InstallAzureCliWindows).</span><span class="sxs-lookup"><span data-stu-id="63286-122">To update to the latest CLI, run the [msi](https://aka.ms/InstallAzureCliWindows) again.</span></span>
> 
> <span data-ttu-id="63286-123">Per disinstallare l'interfaccia della riga di comando, eseguire di nuovo [MSI](https://aka.ms/InstallAzureCliWindows) e scegliere Disinstalla.</span><span class="sxs-lookup"><span data-stu-id="63286-123">To uninstall the CLI, run the [msi](https://aka.ms/InstallAzureCliWindows) again and choose uninstall.</span></span>

### <a name="apt-get-for-bash-on-ubuntu-on-windows"></a><span data-ttu-id="63286-124">apt-get per Bash in Ubuntu in Windows</span><span class="sxs-lookup"><span data-stu-id="63286-124">apt-get for Bash on Ubuntu on Windows</span></span>

1. <span data-ttu-id="63286-125">Se Bash in Windows non è disponibile, [installarlo](https://msdn.microsoft.com/commandline/wsl/install_guide).</span><span class="sxs-lookup"><span data-stu-id="63286-125">If you don't have Bash on Windows, [install it](https://msdn.microsoft.com/commandline/wsl/install_guide).</span></span>

2. <span data-ttu-id="63286-126">Aprire la shell di Bash.</span><span class="sxs-lookup"><span data-stu-id="63286-126">Open the Bash shell.</span></span>

3. <span data-ttu-id="63286-127">Modificare l'elenco di origini.</span><span class="sxs-lookup"><span data-stu-id="63286-127">Modify your sources list.</span></span>

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. <span data-ttu-id="63286-128">Eseguire i comandi sudo seguenti:</span><span class="sxs-lookup"><span data-stu-id="63286-128">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

> [!NOTE]
> <span data-ttu-id="63286-129">Quando si esegue l'installazione con apt-get, `az component` non è supportato.</span><span class="sxs-lookup"><span data-stu-id="63286-129">When you install with apt-get, `az component` isn't supported.</span></span>
> <span data-ttu-id="63286-130">Per aggiornare l'interfaccia della riga di comando, eseguire di nuovo `sudo apt-get update && sudo apt-get install azure-cli`.</span><span class="sxs-lookup"><span data-stu-id="63286-130">To update the CLI, run `sudo apt-get update && sudo apt-get install azure-cli` again.</span></span>
> 
> <span data-ttu-id="63286-131">Per eseguire la disinstallazione, eseguire `sudo apt-get remove azure-cli`.</span><span class="sxs-lookup"><span data-stu-id="63286-131">To uninstall, run `sudo apt-get remove azure-cli`.</span></span>

## <a name="linux"></a><span data-ttu-id="63286-132">Linux</span><span class="sxs-lookup"><span data-stu-id="63286-132">Linux</span></span>

1. <span data-ttu-id="63286-133">In Linux potrebbe essere necessario installare specifici [prerequisiti](#linux-prerequisites).</span><span class="sxs-lookup"><span data-stu-id="63286-133">On Linux, you may need to install specific [prerequisites](#linux-prerequisites).</span></span>

2. <span data-ttu-id="63286-134">Installare l'interfaccia della riga di comando di Azure 2.0 con il solo comando `curl`.</span><span class="sxs-lookup"><span data-stu-id="63286-134">Install Azure CLI 2.0 with one `curl` command.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. <span data-ttu-id="63286-135">Potrebbe essere necessario riavviare la shell dei comandi per rendere effettive alcune modifiche apportate.</span><span class="sxs-lookup"><span data-stu-id="63286-135">You may have to restart your command shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```

4. <span data-ttu-id="63286-136">Eseguire l'interfaccia della riga di comando di Azure 2.0 dal prompt dei comandi con il comando `az`.</span><span class="sxs-lookup"><span data-stu-id="63286-136">Run Azure CLI 2.0 from the command prompt with the `az` command.</span></span>

> [!Note]
> <span data-ttu-id="63286-137">Quando si esegue l'installazione con InstallAzureCli, `az component update` non è supportato.</span><span class="sxs-lookup"><span data-stu-id="63286-137">When you install with InstallAzureCli, `az component update` isn't supported.</span></span>
> <span data-ttu-id="63286-138">Per eseguire l'aggiornamento all'interfaccia della riga di comando più recente, eseguire di nuovo `curl -L https://aka.ms/InstallAzureCli | bash`.</span><span class="sxs-lookup"><span data-stu-id="63286-138">To update to the latest CLI, run `curl -L https://aka.ms/InstallAzureCli | bash` again.</span></span>
> 
> <span data-ttu-id="63286-139">Per eseguire la disinstallazione, vedere le [istruzioni per la disinstallazione manuale](#uninstall).</span><span class="sxs-lookup"><span data-stu-id="63286-139">To uninstall, see the [manual uninstall instructions](#uninstall).</span></span>

## <a name="docker"></a><span data-ttu-id="63286-140">Docker</span><span class="sxs-lookup"><span data-stu-id="63286-140">Docker</span></span>

<span data-ttu-id="63286-141">È disponibile un'immagine Docker preconfigurata con l'interfaccia della riga di comando di Azure.</span><span class="sxs-lookup"><span data-stu-id="63286-141">We maintain a Docker image preconfigured with the Azure CLI.</span></span>

<span data-ttu-id="63286-142">Installare l'interfaccia della riga di comando di Azure usando `docker run`.</span><span class="sxs-lookup"><span data-stu-id="63286-142">Install the Azure CLI using `docker run`.</span></span>

```bash
docker run azuresdk/azure-cli-python:<version>
```

<span data-ttu-id="63286-143">Per le versioni disponibili, vedere i [tag di Docker](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/).</span><span class="sxs-lookup"><span data-stu-id="63286-143">See our [Docker tags](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) for available versions.</span></span>

> [!NOTE]
> <span data-ttu-id="63286-144">Per acquisire le chiavi SSH dall'ambiente utente, è possibile usare `-v ${HOME}:/root` per montare $HOME come `/root`.</span><span class="sxs-lookup"><span data-stu-id="63286-144">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>
>
> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

> [!NOTE]
> <span data-ttu-id="63286-145">L'immagine Docker non supporta la the [funzionalità `component`](/cli/azure/component).</span><span class="sxs-lookup"><span data-stu-id="63286-145">The Docker image does not support the [`component` feature](/cli/azure/component).</span></span>
> <span data-ttu-id="63286-146">Per aggiornare l'interfaccia della riga di comando di Azure 2.0, usare `docker run` per installare l'immagine più recente o un'immagine specifica.</span><span class="sxs-lookup"><span data-stu-id="63286-146">To update the Azure CLI 2.0, use `docker run` to install the latest image, or the specific image that you want.</span></span>

## <a name="apt-get"></a><span data-ttu-id="63286-147">apt-get</span><span class="sxs-lookup"><span data-stu-id="63286-147">apt-get</span></span>

<span data-ttu-id="63286-148">Per i sistemi basati su Debian/Ubuntu, è possibile installare l'interfaccia della riga di comando di Azure 2.0 tramite `apt-get`.</span><span class="sxs-lookup"><span data-stu-id="63286-148">For Debian/Ubuntu based systems, you can install Azure CLI 2.0 via `apt-get`.</span></span>

1. <span data-ttu-id="63286-149">Modificare l'elenco di origini.</span><span class="sxs-lookup"><span data-stu-id="63286-149">Modify your sources list.</span></span>

   - <span data-ttu-id="63286-150">Sistema a 32 bit</span><span class="sxs-lookup"><span data-stu-id="63286-150">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="63286-151">Sistema a 64 bit</span><span class="sxs-lookup"><span data-stu-id="63286-151">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="63286-152">Eseguire i comandi sudo seguenti:</span><span class="sxs-lookup"><span data-stu-id="63286-152">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

> [!NOTE]
> <span data-ttu-id="63286-153">Quando si esegue l'installazione con apt-get, `az component` non è supportato.</span><span class="sxs-lookup"><span data-stu-id="63286-153">When you install with apt-get, `az component` isn't supported.</span></span>
> <span data-ttu-id="63286-154">Per aggiornare l'interfaccia della riga di comando, eseguire di nuovo `sudo apt-get update && sudo apt-get install azure-cli`.</span><span class="sxs-lookup"><span data-stu-id="63286-154">To update the CLI, run `sudo apt-get update && sudo apt-get install azure-cli` again.</span></span>
> 
> <span data-ttu-id="63286-155">Per eseguire la disinstallazione, eseguire `sudo apt-get remove azure-cli`.</span><span class="sxs-lookup"><span data-stu-id="63286-155">To uninstall, run `sudo apt-get remove azure-cli`.</span></span>

## <a name="linux-prerequisites"></a><span data-ttu-id="63286-156">Prerequisiti per Linux</span><span class="sxs-lookup"><span data-stu-id="63286-156">Linux Prerequisites</span></span>

1. <span data-ttu-id="63286-157">Se [Python](https://www.python.org/downloads) non è disponibile, installarlo.</span><span class="sxs-lookup"><span data-stu-id="63286-157">If you don't have it, install [Python](https://www.python.org/downloads).</span></span>

2. <span data-ttu-id="63286-158">A seconda della distribuzione di Linux, installare i prerequisiti.</span><span class="sxs-lookup"><span data-stu-id="63286-158">Depending on your Linux distribution, install the prerequisites.</span></span>

   ```
   Platform              | Prerequisites
   ----------------------|---------------------------------------------
   Ubuntu 15.10 or 16.04 | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev build-essential
   Ubuntu 12.04 or 14.04 | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev
   Debian 8              | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev build-essential
   Debian 7              | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev
   CentOS 7.1 or 7.2     | sudo yum check-update; sudo yum install -y gcc libffi-devel python-devel openssl-devel
   RedHat 7.2            | sudo yum check-update; sudo yum install -y gcc libffi-devel python-devel openssl-devel
   SUSE OpenSUSE 13.2    | sudo zypper refresh && sudo zypper --non-interactive install gcc libffi-devel python-devel openssl-devel
   ```

## <a name="troubleshooting"></a><span data-ttu-id="63286-159">Risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="63286-159">Troubleshooting</span></span>

### <a name="errors-with-curl-redirection"></a><span data-ttu-id="63286-160">Errori relativi al reindirizzamento di curl</span><span class="sxs-lookup"><span data-stu-id="63286-160">Errors with curl redirection</span></span>

<span data-ttu-id="63286-161">Se si verifica un errore del comando `curl` relativo al parametro `-L` o un errore indicante che l'oggetto è stato spostato, provare a usare l'URL completo invece dell'URL aka.ms:</span><span class="sxs-lookup"><span data-stu-id="63286-161">If you get an error from the `curl` command regarding the `-L` parameter, or an error saying "Object Moved", try using the full url instead of the aka.ms url:</span></span>

```
# If you see this:
curl -L https://aka.ms/InstallAzureCli | bash
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   175  100   175    0     0    562      0 --:--:-- --:--:-- --:--:--   560
bash: line 1: syntax error near unexpected token `<'
'ash: line 1: `<html><head><title>Object moved</title></head><body>

#### Try this instead:
curl https://azurecliprod.blob.core.windows.net/install | bash
```

## <a name="uninstall"></a><span data-ttu-id="63286-162">Disinstallare</span><span class="sxs-lookup"><span data-stu-id="63286-162">Uninstall</span></span>

<span data-ttu-id="63286-163">Se è stato usato lo script all'indirizzo https://aka.ms/InstallAzureCli per installare l'interfaccia della riga di comando, è possibile disinstallarla eseguendo questa procedura.</span><span class="sxs-lookup"><span data-stu-id="63286-163">If you used the script at https://aka.ms/InstallAzureCli to install the CLI, you can uninstall it with these steps.</span></span>

1. <span data-ttu-id="63286-164">Rimuovere i file installati.</span><span class="sxs-lookup"><span data-stu-id="63286-164">Remove the installed files.</span></span>

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. <span data-ttu-id="63286-165">Eliminare la riga `<install location>/lib/azure-cli/az.completion` da `<install location>/.bash_profile`.</span><span class="sxs-lookup"><span data-stu-id="63286-165">Delete the line `<install location>/lib/azure-cli/az.completion` from `<install location>/.bash_profile`.</span></span>

> [!Note]
> <span data-ttu-id="63286-166">Il percorso di installazione predefinito è `/Users/<username>`.</span><span class="sxs-lookup"><span data-stu-id="63286-166">The default install location is `/Users/<username>`.</span></span>

<span data-ttu-id="63286-167">Se è stato usato apt-get, Docker o MSI per installare l'interfaccia della riga di comando, usare lo stesso strumento per disinstallarla.</span><span class="sxs-lookup"><span data-stu-id="63286-167">If you used apt-get, Docker, or the msi to install the CLI, use the same tool to uninstall it.</span></span>

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="63286-168">Segnalazione di problemi e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="63286-168">Reporting issues and feedback</span></span>

<span data-ttu-id="63286-169">Se si rilevano bug con lo strumento, segnalare un problema nella sezione [Issues](https://github.com/Azure/azure-cli/issues) (Problemi) del repository GitHub.</span><span class="sxs-lookup"><span data-stu-id="63286-169">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-cli/issues) section of our GitHub repo.</span></span>
<span data-ttu-id="63286-170">Per fornire commenti e suggerimenti dalla riga di comando, provare a usare il comando `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="63286-170">To provide feedback from the command line, try the `az feedback` command.</span></span>
