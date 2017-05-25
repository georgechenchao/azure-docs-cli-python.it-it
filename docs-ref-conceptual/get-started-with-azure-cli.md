---
title: Introduzione all&quot;interfaccia della riga di comando di Azure 2.0
description: Introduzione all&quot;interfaccia della riga di comando di Azure 2.0 su Linux Mac o Windows.
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
ms.openlocfilehash: 45e51918ec95494699bf781f66e4cd57bd06fbad
ms.sourcegitcommit: b4cb5c910b2238cba342f70122feb158c4036844
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/18/2017
---
# <a name="get-started-with-azure-cli-20"></a>Introduzione all'interfaccia della riga di comando di Azure 2.0

L'interfaccia della riga di comando di Azure 2.0 è la nuova esperienza della riga di comando di Azure per gestire le risorse di Azure.
Può essere usata in macOS, Linux e Windows. 

L'interfaccia della riga di comando di Azure 2.0 è ottimizzata per la gestione e l'amministrazione delle risorse di Azure dalla riga di comando e per la creazione di script di automazione che funzionano con Azure Resource Manager.
Questo articolo offre un'introduzione all'uso e ne illustra i concetti di base.

Per informazioni sulla versione più recente, vedere le [note sulla versione](release-notes-azure-cli.md).

## <a name="install-azure-cli"></a>Installare l'interfaccia da riga di comando di Azure

Il primo passaggio è verificare di aver installato l'ultima versione dell'interfaccia della riga di comando di Azure:

1. [Installare l'interfaccia della riga di comando di Azure 2.0](install-azure-cli.md) su ogni piattaforma che si usa.

2. Per verificare che l'installazione sia riuscita, eseguire `az --version` dalla riga di comando. 

Verrà visualizzato il numero di versione dell'interfaccia della riga di comando di Azure e delle altre librerie dipendenti installate sul computer.  
  
Se si presenta un errore, è possibile che si sia verificato un problema durante l'installazione dell'interfaccia della riga di comando. Per istruzioni, vedere la sezione relativa alla risoluzione dei problemi di installazione dell'[articolo sull'installazione dell'interfaccia della riga di comando 2.0](install-azure-cli.md#troubleshooting) o pubblicare un commento nella discussione nella parte inferiore della pagina per ottenere assistenza.

> [!Note]
> Se non si desidera installare l'interfaccia della riga di comando di Azure 2.0, è possibile usare [Cloud Shell](/azure/cloud-shell/overview) per eseguirla nel browser.

## <a name="log-in-to-azure"></a>Accedere ad Azure

Dopo aver installato l'interfaccia della riga di comando di Azure 2.0, occorre connetterla in modo sicuro con l'account Azure. A tale fine, usare il comando `az login`.

1. Eseguire il comando seguente dalla riga di comando.

   ```azurecli-interactive
   az login
   ```
   
   Questo comando restituirà un codice da usare nel passaggio successivo. 

2. Usare un Web browser per aprire la pagina [https://aka.ms/devicelogin](https://aka.ms/devicelogin) e immettere il codice.
  
3. Al prompt dei comandi, accedere usando le credenziali di Azure.

Ora è possibile eseguire comandi dall'interfaccia della riga di comando di Azure 2.0 sulle risorse e sui servizi Azure disponibili al proprio account.

## <a name="create-a-resource-group"></a>Creare un gruppo di risorse

Dopo aver eseguito tutte le impostazioni, è possibile usare l'interfaccia della riga di comando di Azure per creare risorse in Azure.

Si crea prima un gruppo di risorse.  I gruppi di risorse di Azure consentono di gestire numero risorse che si desidera raggruppare in modo logico.  Ad esempio, è possibile creare un gruppo di risorse per un'applicazione o un progetto e aggiungere una macchina virtuale, un database e un servizio rete CDN al suo interno.

Creare un gruppo di risorse denominato "MyResourceGroup" nell'area *westus2* di Azure.  A questo scopo, usare il comando seguente:

```azurecli-interactive
az group create -n MyResourceGroup -l westus2 
```

Dopo aver creato il gruppo di risorse, il comando `az group create` restituisce alcune proprietà della risorsa appena creata:

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

## <a name="create-a-linux-virtual-machine"></a>Creare una macchina virtuale Linux

Con un gruppo di risorse disponibile, creare una macchina virtuale Linux contenuta in esso.

È possibile creare una macchina virtuale Linux usando la comune immagine UbuntuTLS con due dischi di archiviazione di 10 GB e 20 GB collegati, mediante il comando seguente:

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS --data-disk-sizes-gb 10 20
```

Quando si esegue il comando precedente, l'interfaccia della riga di comando di Azure 2.0 cerca una coppia di chiavi SSH archiviata nella directory ~/.ssh.  Se non è ancora presente una coppia di chiavi SSH in tale percorso, è possibile richiedere all'interfaccia della riga di comando di Azure di crearne automaticamente una passando il parametro --generate-ssh-keys:

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS --generate-ssh-keys
```

Il comando `az vm create` restituisce l'output una volta che la macchina virtuale è stata creata completamente ed è possibile accedervi e usarla. L'output include varie proprietà della macchina virtuale appena creata tra cui l'indirizzo IP pubblico:

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

Ora che la macchina virtuale è stata creata, è possibile accedere alla nuova macchina virtuale Linux tramite **SSH** con l'indirizzo IP pubblico della macchina virtuale creata:

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

## <a name="create-a-windows-server-virtual-machine"></a>Creare una macchina virtuale Windows Server

Creare ora una macchina virtuale basata su Windows Server 2016 Datacenter usando il comando `az vm create` e aggiungerla allo stesso gruppo di risorse "MyResourceGroup" usato per la macchina virtuale Linux.  Come nell'esempio sulla macchina virtuale Linux, si collegano due dischi di archiviazione usando il parametro `--data-disk-sizes-gb`.

Azure richiede di evitare di usare nomi utente e password facilmente identificabili. Vi sono regole specifiche sui caratteri che possono essere usati nonché sulla lunghezza minima di nome utente e password.  

> [!NOTE]
> Al momento dell'esecuzione di questo comando verrà richiesto di immettere il nome utente e la password.

```azurecli-interactive
az vm create -n MyWinVM -g MyResourceGroup --image Win2016Datacenter
```

Il comando `az vm create` genera i risultati una volta che la macchina virtuale è stata creata completamente ed è possibile accedervi e usarla.

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

Accedere ora alla macchina virtuale Windows Server appena creata tramite desktop remoto, usando l'indirizzo IP pubblico della macchina virtuale (restituito nell'output del comando `az vm create`).  
Se si usa un sistema basato su Windows, è possibile eseguire questa operazione dalla riga di comando usando il comando `mstsc`:

```azurecli-interactive
mstsc /v:xx.xxx.xx.xxx
```

Fornire la stessa combinazione di nome utente/password usata quando si crea la macchina virtuale per l'accesso.

## <a name="creating-other-resources-in-azure"></a>Creazione di altre risorse in Azure

È stato descritto come creare un gruppo di risorse, una macchina virtuale Linux e una macchina virtuale di Windows Server. È possibile creare molti altri tipi di risorse di Azure.  

Tutte le nuove risorse vengono create usando un modello di denominazione `az <resource type name> create` coerente.  Ad esempio, per creare un bilanciamento del carico sulla rete di Azure da associare con le macchine virtuali appena create, è possibile usare il seguente comando:

```azurecli-interactive
az network lb create -n MyLoadBalancer -g MyResourceGroup
```

È inoltre possibile creare una nuova rete virtuale privata (nota come "VNet" all'interno di Azure) per l'infrastruttura usando il comando create seguente:

```azurecli-interactive
az network vnet create -n MyVirtualNetwork -g MyResourceGroup --address-prefix 10.0.0.0/16
```

Azure e l'interfaccia della riga di comando di Azure sono particolarmente efficienti poiché è possibile usarli non solo per ottenere un'infrastruttura basata su cloud, ma anche per creare servizi di piattaforma gestita.  I servizi di piattaforma gestita possono anche essere combinati con l'infrastruttura per creare soluzioni ancora più potenti.

Ad esempio, è possibile usare l'interfaccia della riga di comando di Azure per creare un servizio app di Azure.  Il servizio app di Azure è un servizio di piattaforma gestita che fornisce un ottimo modo per l'hosting di app Web senza doversi preoccupare dell'infrastruttura.  Dopo aver creato il servizio app di Azure, è possibile creare due nuove app Web di Azure all'interno del servizio app usando i comandi create seguenti:

```azurecli-interactive
# Create an Azure AppService that we can host any number of web apps within
az appservice plan create -n MyAppServicePlan -g MyResourceGroup

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
az webapp create -n MyWebApp43432 -g MyResourceGroup --plan MyAppServicePlan 
az webapp create -n MyWebApp43433 -g MyResourceGroup --plan MyAppServicePlan 
```

Dopo aver appreso le nozioni di base sul modello `az <resource type name> create`, risulta facile creare qualsiasi elemento. Di seguito sono riportati alcuni tipi di risorse Azure comuni e i corrispondenti comandi create dell'interfaccia della riga di comando di Azure per crearli:

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

Per altre informazioni su ulteriori parametri specifici delle risorse che è possibile passare a ognuno dei comandi precedenti e sui tipi di risorse che è possibile creare, vedere la [documentazione di riferimento](/cli/azure). 

## <a name="useful-tip-optimizing-create-operations-using---no-wait"></a>Suggerimento utile: ottimizzazione delle operazioni di creazione usando --no-wait

Per impostazione predefinita quando si creano risorse usando l'interfaccia della riga di comando di Azure 2.0, il comando `az <resource type name> create` attende che la risorsa venga creata e sia pronta per l'uso.  Ad esempio, se si crea una macchina virtuale, per impostazione predefinita il comando `az vm create` non restituirà risultati finché la macchina virtuale non sarà creata e non sarà pronta per eseguire una connessione tramite SSH o RDP.

Si usa questo approccio poiché risulta più semplice scrivere script di automazione che contengono più passaggi con dipendenze (e richiedono che venga completata correttamente un'attività precedente prima di continuare).

Se non è necessario attendere la creazione di una risorsa prima di continuare, è possibile usare l'opzione `no-wait` per avviare un'azione di creazione in background. È possibile continuare a usare l'interfaccia della riga di comando per altri comandi.

Ad esempio, l'uso seguente del comando `az vm create` avvia una distribuzione della macchina virtuale e quindi restituisce i risultati molto più rapidamente (prima che la macchina virtuale sia avviata completamente):

```azurecli-interactive
az vm create -n MyLinuxVM2 -g MyResourceGroup --image UbuntuLTS --no-wait
```

L'uso dell'approccio `--no-wait` può consentire di ottimizzare notevolmente le prestazioni degli script di automazione.

## <a name="listing-resources-and-formatting-output"></a>Elenco di risorse e formattazione dell'output

È possibile usare il comando `list` nell'interfaccia della riga di comando di Azure per trovare ed elencare le risorse in esecuzione in Azure. 

Come con il comando create, è possibile elencare le risorse nell'interfaccia della riga di comando di Azure 2.0 usando un modello di denominazione `az <resource type name> list` comune, coerente per tutti i tipi di risorsa.  Sono disponibili vari formati di output e opzioni di query per filtrare e ordinare l'elenco di risorse nel modo in cui si preferisce visualizzarlo.

Ad esempio, `az vm list` mostra l'elenco di tutte le macchine virtuali presenti.   

```azurecli-interactive
az vm list 
```
I valori sono restituiti per impostazione predefinita in JSON (per brevità è riportato solo l'output parziale).

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

Facoltativamente è anche possibile modificare il formato di output usando l'opzione `--output`.  Eseguire il comando `az vm list` per visualizzare entrambe le macchine virtuali Linux e Windows Server create precedentemente, insieme alle proprietà più comuni di una macchina virtuale, usando l'opzione di formato di agevole lettura *table*:

```azurecli-interactive
az vm list --output table
```

```Output
Name       ResourceGroup    Location
---------  ---------------  ----------
MyLinuxVM  MyResourceGroup  westus2
MyWinVM    MyResourceGroup  westus2
```

L'opzione di output *tsv* può essere usata per ottenere un formato di testo separato da tabulazioni senza intestazioni.  Questo formato è utile quando si desidera inviare tramite pipe l'output a un altro strumento basato su testo quale grep. 

```azurecli-interactive
az vm list --output tsv
```

```
None    None            /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyLinuxVM        None    None    westus2 MyLinuxVM                   None        Succeeded       MyResourceGroup None                    Microsoft.Compute/virtualMachines       XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
None    None            /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyWinVM  None    None    westus2 MyWinVM                 None    Succeeded       MyResourceGroup None                    Microsoft.Compute/virtualMachines       XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```
Per altre informazioni su ulteriori modi per elencare risorse e formattare l'output, vedere l'articolo relativo ai [formati di output](format-output-azure-cli.md).

## <a name="querying-resources-and-shaping-outputs"></a>Esecuzione di query su risorse e shaping dell'output

Spesso è necessario eseguire query solo sulle risorse che soddisfano una condizione specifica.  

Il comando `list` include una funzionalità integrata che consente di filtrare agevolmente le risorse per nome del gruppo di risorse.  Ad esempio, è possibile passare un parametro `--ResourceGroup` o `-g` a un comando `list` per recuperare solo le risorse in un gruppo di risorse specifico:


```azurecli
az vm list -g MyResourceGroup --output table
```

```Output
Name       ResourceGroup    Location
---------  ---------------  ----------
MyLinuxVM  MyResourceGroup  westus2
MyWinVM    MyResourceGroup  westus2
```

Per una funzionalità di query ancora più efficace, è possibile usare il parametro `--query` per eseguire una query JMESPath sui risultati di *qualsiasi* comando `az`.  Le query JMESPath possono essere usate sia per filtrare che per lo shaping dell'output dei risultati restituiti.

Ad esempio, eseguire il comando seguente per eseguire query su qualsiasi risorsa di macchina virtuale all'interno di un gruppo di risorse che contenga le lettere "My":

```azurecli-interactive
az vm list --output table --query "[?contains(resourceGroup,'MY')]" 
```

```Output
ResourceGroup    ProvisioningState    Name       Location    VmId
---------------  -------------------  ---------  ----------  ------------------------------------
MYRESOURCEGROUP  Succeeded            MyLinuxVM  westus2     XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
MYRESOURCEGROUP  Succeeded            MyWinVM    westus2     XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

È quindi possibile affinare ulteriormente l'output usando la funzionalità di shaping delle query JMESPath per generare valori diversi.  Ad esempio, il comando seguente recupera il tipo di disco del sistema operativo che la macchina virtuale usa per determinare se il sistema operativo è basato su Linux o Windows:

```azurecli-interactive
az vm list --output table --query "[?contains(resourceGroup,'MY')].{ VMName:name,OSType:storageProfile.osDisk.osType }" 
```

```Output
VMName     OSType
---------  --------
MyLinuxVM  Linux
MyWinVM    Windows
```

Il supporto di JMESPath nell'interfaccia della riga di comando di Azure è notevolmente efficace.  Per altre informazioni su come usarlo vedere l'articolo su [query](query-azure-cli.md).

## <a name="deleting-resources"></a>Eliminazione di risorse

È possibile usare il comando `delete` nell'interfaccia della riga di comando di Azure per eliminare le risorse che non sono più necessarie. È possibile usare il comando `delete` con qualsiasi risorsa in modo analogo al comando `create`.

```azurecli-interactive
az vm delete -n MyLinuxVM -g MyResourceGroup
```

Per impostazione predefinita l'interfaccia della riga di comando richiede di confermare l'eliminazione.  È possibile eliminare questa richiesta per gli script automatici.

```Output
Are you sure you want to perform this operation? (y/n): y
EndTime                           Name                                  StartTime                         Status
--------------------------------  ------------------------------------  --------------------------------  ---------
2017-02-19T02:35:56.678905+00:00  5b74ab80-9b29-4329-b483-52b406583e2f  2017-02-19T02:33:35.372769+00:00  Succeeded
```

È anche possibile usare il comando `delete` per eliminare molte risorse contemporaneamente. Ad esempio, il comando seguente elimina tutte le risorse nel gruppo di risorse "MyResourceGroup" usate per tutti gli esempi in questa esercitazione di introduzione.

```azurecli-interactive
az group delete -n MyResourceGroup
```

```Output
Are you sure you want to perform this operation? (y/n): y
```

## <a name="get-samples"></a>Ottenere gli esempi

Per altre informazioni sull'uso dell'interfaccia della riga di comando di Azure, vedere gli script più comuni per [macchine virtuali Linux](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json), [macchine virtuali Windows](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json), [app Web](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json) e [database SQL](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json).

## <a name="read-the-api-reference-docs"></a>Leggere la documentazione di riferimento sulle API

[Informazioni di riferimento sulle API](/cli/azure)

## <a name="get-help"></a>Ottenere aiuto

L'interfaccia della riga di comando di Azure include una guida incorporata corrispondente alla documentazione Web che è possibile eseguire dalla riga di comando:

```azurecli-interactive
az [command-group [command]] -h
```

Ad esempio, per visualizzare i comandi e i sottogruppi disponibili per le macchine virtuali, usare:

```azurecli-interactive
az vm -h
```

Per ottenere informazioni sul comando per creare una macchina virtuale, usare:

```azurecli-interactive
az vm create -h
```

## <a name="switch-from-azure-cli-10"></a>Passaggio dall'interfaccia della riga di comando di Azure 1.0

Se si ha già familiarità con l'uso dell'interfaccia della riga di comando di Azure 1.0 (azure.js), si noterà che in alcuni casi i comandi sono pressoché uguali.
In altri casi, i comandi per eseguire un'attività sono notevolmente diversi.
Per agevolare il passaggio dall'interfaccia della riga di comando di Azure 1.0 all'interfaccia della riga di comando di Azure 2.0, è stato creato questo [mapping dei comandi](https://github.com/Azure/azure-cli/blob/master/doc/azure2az_commands.rst).

## <a name="send-us-your-feedback"></a>Invio di commenti

```azurecli-interactive
az feedback
```
