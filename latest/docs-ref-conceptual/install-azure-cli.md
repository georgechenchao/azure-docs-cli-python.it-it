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
# <a name="install-azure-cli-20"></a>Installare l'interfaccia della riga di comando di Azure 2.0

È possibile installare oggi stesso l'interfaccia della riga di comando di Azure,
che è stata migliorata e aggiornata per offrire un'esperienza ottimale della riga di comando nativa per la gestione delle risorse di Azure.
Può essere usata in macOS, Linux e Windows.
Per informazioni sulla versione più recente, vedere le [note sulla versione](release-notes-azure-cli.md).

> [!NOTE]
> Se è necessaria la versione precedente dell'interfaccia della riga di comando di Azure, vedere [Installare l'interfaccia della riga di comando di Azure 1.0](/azure/cli-install-nodejs).

## <a name="a-namemacosinstall-on-macos"></a><a name="macOS"/>Eseguire l'installazione in macOS

1. Installare l'interfaccia della riga di comando di Azure 2.0 con `curl`.

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. Potrebbe essere necessario riavviare la shell per rendere effettive alcune modifiche apportate.

   ```bash
   exec -l $SHELL
   ```
   
3. Eseguire l'interfaccia della riga di comando dal prompt dei comandi con il comando `az`.

## <a name="install-on-windows"></a>Eseguire l'installazione in Windows

È possibile installare l'interfaccia della riga di comando di Azure 2.0 con MSI e usarla nella riga di comando di Windows, oppure è possibile installare l'interfaccia della riga di comando con `apt-get` su Bash in Ubuntu in Windows.

### <a name="install-with-msi-for-the-windows-command-line"></a>Eseguire l'installazione con MSI per la riga di comando di Windows 

Per installare l'interfaccia della riga di comando in Windows e usarla nella riga di comando di Windows, scaricare ed eseguire [MSI](https://aka.ms/InstallAzureCliWindows).

### <a name="install-with-apt-get-for-bash-on-ubuntu-on-windows"></a>Eseguire l'installazione con apt-get per Bash in Ubuntu in Windows

1. Se Bash in Windows non è disponibile, [installarlo](https://msdn.microsoft.com/commandline/wsl/install_guide).

2. Aprire la shell di Bash.

3. Modificare l'elenco di origini.

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. Eseguire i comandi sudo seguenti:

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

5.  Eseguire l'interfaccia della riga di comando dal prompt dei comandi con il comando `az`.

## <a name="install-on-debianubuntu-with-apt-get"></a>Eseguire l'installazione in Debian/Ubuntu con apt-get

Per i sistemi basati su Debian/Ubuntu, è possibile installare l'interfaccia della riga di comando di Azure 2.0 tramite `apt-get`.

1. Modificare l'elenco di origini:
 
   - Sistema a 32 bit

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - Sistema a 64 bit

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. Eseguire i comandi sudo seguenti:

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

3.  Eseguire l'interfaccia della riga di comando dal prompt dei comandi con il comando `az`.

## <a name="install-on-rhel-fedora-and-centos-with-yum"></a>Eseguire l'installazione in RHEL, Fedora e CentOS con yum

Per le distribuzioni basate su RedHat e contenenti l'utilità di gestione pacchetti `yum`, è possibile installare l'interfaccia della riga di comando di Azure 2.0 tramite `yum`.

1. Importare la chiave del repository Microsoft:

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. Creare le informazioni del repository `azure-cli` locale:

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. Aggiornare l'indice del pacchetto `yum` ed eseguire l'installazione:

   ```bash
   yum check-update
   sudo yum install azure-cli
   ```

4. Eseguire l'interfaccia della riga di comando dal prompt dei comandi con il comando `az`.

## <a name="install-on-opensuse-and-sle-with-zypper"></a>Eseguire l'installazione in openSUSE e SLE con zypper

1. Importare la chiave del repository Microsoft:

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. Creare le informazioni del repository `azure-cli` locale:

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/azure-cli.repo'
   ```

3. Aggiornare l'indice del pacchetto `zypper` ed eseguire l'installazione:

   ```bash
   sudo zypper refresh
   sudo zypper install azure-cli
   ```

4. Eseguire l'interfaccia della riga di comando dal prompt dei comandi con il comando `az`.

## <a name="install-with-docker"></a>Eseguire l'installazione con Docker

È disponibile un'immagine Docker preconfigurata con l'interfaccia della riga di comando di Azure 2.0.

Installare l'interfaccia della riga di comando con `docker run`.

   ```bash
   docker run azuresdk/azure-cli-python:<version>
   ```

Per le versioni disponibili, vedere i [tag di Docker](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/).

L'interfaccia della riga di comando viene installata nell'immagine come il comando `az` in `/usr/local/bin`.

> [!NOTE]
> Per acquisire le chiavi SSH dall'ambiente utente, è possibile usare `-v ${HOME}:/root` per montare $HOME come `/root`.

> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

## <a name="a-namelinuxinstall-on-linux-without-apt-get"></a><a name="Linux"/>Eseguire l'installazione in Linux senza apt-get

È consigliabile installare l'interfaccia della riga di comando con un'utilità di gestione pacchetti, se possibile. Per le distribuzioni a cui non viene fornito un pacchetto, è possibile eseguire l'installazione manuale.

1. Installare i prerequisiti in base alla distribuzione Linux specifica.

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

Se la distribuzione non è inclusa nell'elenco precedente, sarà necessario installare [Python](https://www.python.org/downloads/), [libffi](https://sourceware.org/libffi/), e [OpenSSL](https://www.openssl.org/source/).

2. Installare l'interfaccia della riga di comando con `curl`.

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. Potrebbe essere necessario riavviare la shell per rendere effettive alcune modifiche apportate.

   ```bash
   exec -l $SHELL
   ```

4. Eseguire l'interfaccia della riga di comando dal prompt dei comandi con il comando `az`.

## <a name="troubleshooting"></a>Risoluzione dei problemi

Se si verifica un problema durante l'installazione dell'interfaccia della riga di comando, controllare questa sezione per verificare se include il caso specifico. Se il problema non è incluso in questa sezione, [segnalare il problema su Github](https://github.com/Azure/azure-cli/issues).

### <a name="curl-object-moved-error"></a>Errore curl di tipo "Object Moved"

Se viene restituito da `curl` un errore relativo al parametro `-L` o se viene visualizzato un messaggio di errore che include il testo "Object Moved", provare a usare l'URL completo invece dell'URL di reindirizzamento `aka.ms`:

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="homebrew-on-macos-installing-older-version"></a>Homebrew in macOS per l'installazione di una versione precedente

La formula `azure-cli` di Homebrew disponibile per macOS è attualmente obsoleta e installerà una versione 1.x dell'interfaccia della riga di comando. È possibile verificare quando viene aggiornata controllando `brew info azure-cli`.

Fino all'aggiornamento, [disinstallare la versione precedente](#uninstall_brew) e seguire le [istruzioni di installazione per macOS](#macOS).

## <a name="uninstall-cli-1x-versions"></a>Disinstallare le versioni 1.x dell'interfaccia della riga di comando

Se nel sistema è disponibile una versione 1.x precedente dell'interfaccia della riga di comando, è possibile disinstallarla in base al tipo di installazione usato.

### <a name="uninstall-with-npm"></a>Eseguire la disinstallazione con npm

Rimuovere l'interfaccia della riga di comando precedente con `npm uninstall`.

  ```bash
  npm uninstall -g azure-cli
  ```

### <a name="a-nameuninstallbrewuninstall-with-homebrew-on-macos"></a><a name="uninstall_brew"/>Eseguire la disinstallazione con Homebrew in macOS

Rimuovere l'interfaccia della riga di comando precedente con `brew uninstall`.

```bash
brew uninstall azure-cli
```

### <a name="uninstall-with-distributable"></a>Eseguire la disinstallazione con un file distribuibile

Se l'installazione è stata eseguita tramite [MSI](http://aka.ms/webpi-azure-cli) o un [pacchetto macOS](http://aka.ms/mac-azure-cli), usare lo stesso strumento per rimuovere l'installazione.

### <a name="uninstall-with-docker"></a>Eseguire la disinstallazione con Docker

Se è stata installata un'immagine Docker per usare la versione precedente dell'interfaccia della riga di comando, rimuovere l'immagine ed eventuali contenitori associati. È quindi possibile creare di nuovo i contenitori dopo l'installazione della nuova immagine Docker, come illustrato nelle istruzioni di installazione.

  ```bash
  docker rmi -f microsoft/azure-cli
  ```

## <a name="update-the-cli"></a>Aggiornare l'interfaccia della riga di comando

Per aggiornare l'interfaccia della riga di comando di Azure, usare lo stesso metodo usato per installarla.

### <a name="update-with-msi"></a>Eseguire l'aggiornamento con MSI

Eseguire di nuovo [MSI](https://aka.ms/InstallAzureCliWindows).

### <a name="update-with-apt-get"></a>Eseguire l'aggiornamento con apt-get

Usare `apt-get upgrade` per aggiornare il pacchetto dell'interfaccia della riga di comando.

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> Verranno aggiornati tutti i pacchetti installati nel sistema che non hanno subito modifiche relative alle dipendenze.
> Per eseguire l'aggiornamento solo dell'interfaccia della riga di comando, usare `apt-get install`.
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="update-with-docker"></a>Eseguire l'aggiornamento con Docker

1. Aggiornare l'immagine locale con `docker pull`.

   ```bash
   docker pull azuresdk/azure-cli-python
   ```

2. Ottenere i contenitori che usano attualmente l'immagine dell'interfaccia della riga di comando.

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

> [!NOTE]
> Se è stata installata una versione specifica dell'immagine, sarà necessario aggiungere `:<version>` alla fine del nome dell'immagine.

3. Interrompere e ricreare i contenitori.

   ```bash
   docker stop inspiring_benz
   docker rm inspiring_benz
   docker run azuresdk/azure-cli-python
   ```

### <a name="update-manually"></a>Eseguire l'aggiornamento manualmente

Seguire le istruzioni per l'installazione manuale per [macOS](#macOS) o [Linux](#Linux) per eseguire l'aggiornamento.

## <a name="uninstall"></a>Disinstallare

Se si decide di annullare l'installazione dell'interfaccia della riga di comando, eseguire la disinstallazione usando lo stesso metodo usato per installare l'interfaccia della riga di comando.

### <a name="uninstall-with-msi"></a>Eseguire la disinstallazione con MSI

Eseguire di nuovo [MSI](https://aka.ms/InstallAzureCliWindows) e scegliere l'opzione per la disinstallazione.

### <a name="uninstall-with-apt-get"></a>Eseguire la disinstallazione con apt-get

Disinstallare tramite `apt-get remove`:

  ```bash
  sudo apt-get remove -y azure-cli
  ```

### <a name="uninstall-with-docker"></a>Eseguire la disinstallazione con Docker

Se è stata installata un'immagine Docker, sarà necessario rimuovere eventuali contenitori che la eseguono e quindi eliminare l'immagine locale.

1. Ottenere i contenitori che eseguono l'immagine azure-cli.

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

2. Eliminare eventuali contenitori con l'immagine dell'interfaccia della riga di comando.

   ```bash
   docker rm 34a868beb2ab
   ```

3. Rimuovere l'immagine dell'interfaccia della riga di comando installata in locale.

   ```bash
   docker rmi azuresdk/azure-cli-python
   ```

> [!NOTE]
> Se è stata installata una versione specifica dell'immagine, sarà necessario aggiungere `:<version>` alla fine del nome dell'immagine.

### <a name="uninstall-manually"></a>Eseguire la disinstallazione manualmente

Se è stato usato lo script all'indirizzo https://aka.ms/InstallAzureCli per installare l'interfaccia della riga di comando, è possibile disinstallarla eseguendo questa procedura.

1. Rimuovere i file installati.

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. Eliminare la riga `<install location>/lib/azure-cli/az.completion` da `<install location>/.bash_profile`.

> [!Note]
> Il percorso di installazione predefinito è `/Users/<username>`.

## <a name="report-cli-issues-and-feedback"></a>Segnalazione di problemi e suggerimenti relativi all'interfaccia della riga di comando

Se si rilevano bug con lo strumento, segnalare un problema nella sezione [Issues](https://github.com/Azure/azure-cli/issues) (Problemi) del repository GitHub.
Per inserire commenti e suggerimenti dalla riga di comando, usare il comando `az feedback`.
