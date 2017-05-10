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
ms.openlocfilehash: b7c0b7c50794333b28c034de9b41f1e506053e25
ms.sourcegitcommit: 663d4188ccc4be425d3d551fe32613fafd05a764
ms.translationtype: HT
ms.contentlocale: it-IT
---
# <a name="install-azure-cli-20"></a>Installare l'interfaccia della riga di comando di Azure 2.0

È possibile installare oggi stesso l'interfaccia della riga di comando di Azure,
che è stata migliorata e aggiornata per offrire un'esperienza ottimale della riga di comando nativa per la gestione delle risorse di Azure.
Può essere usata in macOS, Linux e Windows.
Per informazioni sulla versione più recente, vedere le [note sulla versione](release-notes-azure-cli.md).

> [!NOTE]
> Se è necessaria la versione precedente dell'interfaccia della riga di comando di Azure, vedere [Installare l'interfaccia della riga di comando 1.0 di Azure](/azure/cli-install-nodejs).

## <a name="macos"></a>macOS

1. Installare l'interfaccia della riga di comando di Azure 2.0 con il solo comando `curl`.

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. Potrebbe essere necessario riavviare la shell dei comandi per rendere effettive alcune modifiche apportate.

   ```bash
   exec -l $SHELL
   ```
   
3. Eseguire l'interfaccia della riga di comando di Azure 2.0 dal prompt dei comandi con il comando `az`.

> [!Note]
> Quando si esegue l'installazione con InstallAzureCli, `az component update` non è supportato.
> Per eseguire l'aggiornamento all'interfaccia della riga di comando più recente, eseguire di nuovo `curl -L https://aka.ms/InstallAzureCli | bash`.
> 
> Per eseguire la disinstallazione, vedere le [istruzioni per la disinstallazione manuale](#uninstall).

## <a name="windows"></a>Windows

L'interfaccia della riga di comando di Azure 2.0 supporta la sintassi dei comandi di Bash, facendo di Bash in Ubuntu in Windows un'ottima soluzione per usare l'interfaccia della riga di comando.
Se non si usa Bash, è possibile installare e usare l'interfaccia della riga di comando nella riga di comando di Windows.

### <a name="bash-on-ubuntu-on-windows"></a>Bash in Ubuntu in Windows

1. Se Bash in Windows non è disponibile, [installarlo](https://msdn.microsoft.com/commandline/wsl/install_guide).

2. Aprire la shell di Bash.

3. Se Python non è disponibile, installarlo.

   ```bash
   sudo apt-get install python3
   ```

   > [!NOTE]
   > Per verificare se Python è installato, eseguire `python --version`.

4. Modificare l'elenco di origini.

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

5. Eseguire i comandi sudo seguenti:

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

> [!NOTE]
> Quando si esegue l'installazione con apt-get, `az component` non è supportato.
> Per aggiornare l'interfaccia della riga di comando, eseguire di nuovo `sudo apt-get update && sudo apt-get install azure-cli`.
> 
> Per eseguire la disinstallazione, eseguire `sudo apt-get remove azure-cli`.

### <a name="windows-command-line"></a>Riga di comando di Windows 

1. Visitare il sito Python e [scaricare Python](https://www.python.org/downloads/) per Windows.
   Assicurarsi di installare il componente Pip durante l'installazione di Python.
   Al termine dell'installazione, aggiungere Python alla variabile di ambiente PATH quando viene chiesto dal programma di installazione.

2. Controllare l'installazione di Python da un prompt dei comandi.

   ```bash
   python --version
   ```

3. Installare l'interfaccia della riga di comando di Azure 2.0 usando `pip`.

   ```bash
   pip install --user azure-cli
   ```

4. Aggiungere la cartella che contiene az.bat al percorso.
   Il file `az.bat` dell'interfaccia della riga di comando può essere installato in `%USERPROFILE%\AppData\Roaming\Python\Scripts` o `%USERPROFILE%\AppData\Roaming\Python\PythonXY\Scripts` dove `XY` è la versione di Python in uso, ad esempio `%USERPROFILE%\AppData\Roaming\Python\Python27\Scripts`.
   Aggiungere la cartella che contiene `az.bat` al percorso.
   
4. Eseguire l'interfaccia della riga di comando di Azure 2.0 dal prompt dei comandi con il comando `az`.

> [!NOTE]
> Se l'interfaccia della riga di comando di Azure 2.0 è installata e si vuole verificare se si ha la versione più recente, usare `az --version` per visualizzare la versione in uso.
> Confrontarla con la versione più recente disponibile all'indirizzo [https://pypi.python.org/pypi/azure-cli](https://pypi.python.org/pypi/azure-cli).
> 
> Per eseguire l'aggiornamento all'interfaccia della riga di comando più recente, eseguire `az component update`.
> 
> Per disinstallare l'interfaccia della riga di comando, eseguire `pip uninstall azure-cli`.

## <a name="linux"></a>Linux

1. In Linux potrebbe essere necessario installare specifici [prerequisiti](#linux-prerequisites).

2. Installare l'interfaccia della riga di comando di Azure 2.0 con il solo comando `curl`.

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. Potrebbe essere necessario riavviare la shell dei comandi per rendere effettive alcune modifiche apportate.

   ```bash
   exec -l $SHELL
   ```

4. Eseguire l'interfaccia della riga di comando di Azure 2.0 dal prompt dei comandi con il comando `az`.

> [!Note]
> Quando si esegue l'installazione con InstallAzureCli, `az component update` non è supportato.
> Per eseguire l'aggiornamento all'interfaccia della riga di comando più recente, eseguire di nuovo `curl -L https://aka.ms/InstallAzureCli | bash`.
> 
> Per eseguire la disinstallazione, vedere le [istruzioni per la disinstallazione manuale](#uninstall).

## <a name="docker"></a>Docker

È disponibile un'immagine Docker preconfigurata con l'interfaccia della riga di comando di Azure.

Installare l'interfaccia della riga di comando di Azure usando `docker run`.

```bash
docker run azuresdk/azure-cli-python:<version>
```

Per le versioni disponibili, vedere i [tag di Docker](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/).

> [!NOTE]
> Per acquisire le chiavi SSH dall'ambiente utente, è possibile usare `-v ${HOME}:/root` per montare $HOME come `/root`.
>
> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

> [!NOTE]
> L'immagine Docker non supporta la the [funzionalità `component`](/cli/azure/component).
> Per aggiornare l'interfaccia della riga di comando di Azure 2.0, usare `docker run` per installare l'immagine più recente o un'immagine specifica.

## <a name="apt-get"></a>apt-get

Per i sistemi basati su Debian/Ubuntu, è possibile installare l'interfaccia della riga di comando di Azure 2.0 tramite `apt-get`.

1. Modificare l'elenco di origini.

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

> [!NOTE]
> Quando si esegue l'installazione con apt-get, `az component` non è supportato.
> Per aggiornare l'interfaccia della riga di comando, eseguire di nuovo `sudo apt-get update && sudo apt-get install azure-cli`.
> 
> Per eseguire la disinstallazione, eseguire `sudo apt-get remove azure-cli`.

## <a name="linux-prerequisites"></a>Prerequisiti per Linux

1. Se [Python](https://www.python.org/downloads) non è disponibile, installarlo.

2. A seconda della distribuzione di Linux, installare i prerequisiti.

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

## <a name="troubleshooting"></a>Risoluzione dei problemi
-------------------------------

### <a name="errors-with-curl-redirection"></a>Errori relativi al reindirizzamento di curl

Se si verifica un errore del comando `curl` relativo al parametro `-L` o un errore indicante che l'oggetto è stato spostato, provare a usare l'URL completo invece dell'URL aka.ms:

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


### <a name="errors-on-install-with-cffi-or-cryptography"></a>Errori di installazione con `cffi` o di crittografia

Se si verificano errori di installazione in OS X, aggiornare `pip`.

```bash
pip install --upgrade --force-reinstall pip
```

Se si verificano errori di installazione in **Debian** o in **Ubuntu**, come in questi esempi, installare `libssl-dev` e `libffi-dev`.

```bash
sudo apt-get update
sudo apt-get install -y libssl-dev libffi-dev
```

Installare anche Python Dev per la versione di Python in uso.

Python 2:

```bash
sudo apt-get install -y python-dev
```

Python 3:

```bash
sudo apt-get install -y python3-dev
```

Per Ubuntu 15 potrebbe essere necessario anche `build-essential`:

```bash
sudo apt-get install -y build-essential
```

### <a name="example-errors"></a>Errori di esempio

```
Downloading cffi-1.5.2.tar.gz (388kB)
    100% |################################| 389kB 3.9MB/s
    Complete output from command python setup.py egg_info:

        No working compiler found, or bogus compiler options
        passed to the compiler from Python's distutils module.
        See the error messages above.
        (If they are about -mno-fused-madd and you are on OS/X 10.8,
        see http://stackoverflow.com/questions/22313407/ .)

    ----------------------------------------
Command "python setup.py egg_info" failed with error code 1 in /tmp/pip-build-77i2fido/cffi/
```

```
#include <openssl/e_os2.h>
                            ^
compilation terminated.
error: command 'x86_64-linux-gnu-gcc' failed with exit status 1

Failed building wheel for cryptography
```

Vedere la domanda in Stack Overflow: [Failed to install Python Cryptography package with PIP and setup.py](http://stackoverflow.com/questions/22073516/failed-to-install-python-cryptography-package-with-pip-and-setup-py) (Non è possibile installare il pacchetto Cryptography per Python con PIP e setup.py).

## <a name="uninstall"></a>Disinstallare

Se è stato usato lo script all'indirizzo https://aka.ms/InstallAzureCli per installare l'interfaccia della riga di comando, è possibile disinstallarla eseguendo questa procedura.

1. Rimuovere i file installati.

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. Eliminare la riga `<install location>/lib/azure-cli/az.completion` da `<install location>/.bash_profile`.

> [!Note]
> Il percorso di installazione predefinito è `/Users/<username>`.

Se è stato usato pip, apt-get o Docker per installare l'interfaccia della riga di comando, usare lo stesso strumento per disinstallarla.

## <a name="reporting-issues-and-feedback"></a>Segnalazione di problemi e suggerimenti

Se si rilevano bug con lo strumento, segnalare un problema nella sezione [Issues](https://github.com/Azure/azure-cli/issues) (Problemi) del repository GitHub.
Per fornire commenti e suggerimenti dalla riga di comando, provare a usare il comando `az feedback`.
