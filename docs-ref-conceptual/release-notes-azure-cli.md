---
title: Note sulla versione dell&quot;interfaccia della riga di comando di Azure 2.0
description: Informazioni sugli ultimi aggiornamenti dell&quot;interfaccia della riga di comando di Azure 2.0
keywords: Interfaccia della riga di comando di Azure 2.0, note sulla versione
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 04/03/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ce0428f7-0a59-4e72-9237-d907b171af51
ms.openlocfilehash: 3bd4b9c059da3b841fc0757a11bc7ce78ec64b08
ms.sourcegitcommit: 66d997a5afcf32143a4d4817ec1608cbdf58a59f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/11/2017
---
# <a name="azure-cli-20-release-notes"></a>Note sulla versione dell'interfaccia della riga di comando di Azure 2.0

## <a name="may-10-2017"></a>10 maggio 2017

Versione 2.0.6

* documentdb rinominato come cosmosdb
* Aggiunge rdbms (mysql, postgres)
* Include i moduli di Data Lake Store e Data Lake Analytics.
* Include i moduli di Servizi cognitivi.
* Include i moduli di Service Fabric.
* Include i moduli interattivi e rinomina az-shell.
* Aggiunge il supporto per i comandi CDN.
* Rimuove il modulo del contenitore.
* Aggiunge "az -v" come collegamento per "az -- version" ([#2926](https://github.com/Azure/azure-cli/issues/2926))
* Migliora le prestazioni di carico del pacchetto e l'esecuzione del comando ([#2819](https://github.com/Azure/azure-cli/issues/2819))

```
azure-cli (2.0.6)

acr (2.0.4)
acs (2.0.6)
appservice (0.1.6)
batch (2.0.4)
cdn (0.0.2)
cloud (2.0.2)
cognitiveservices (0.1.2)
command-modules-nspkg (2.0.0)
component (2.0.4)
configure (2.0.6)
core (2.0.6)
cosmosdb (0.1.6)
dla (0.0.6)
dls (0.0.6)
feedback (2.0.2)
find (0.2.2)
interactive (0.3.1)
iot (0.1.5)
keyvault (2.0.4)
lab (0.0.4)
monitor (0.0.4)
network (2.0.6)
nspkg (3.0.0)
profile (2.0.4)
rdbms (0.0.1)
redis (0.2.3)
resource (2.0.6)
role (2.0.4)
sf (1.0.1)
sql (2.0.3)
storage (2.0.6)
vm (2.0.6)
```

### <a name="core"></a>Core

* core: consente di acquisire le eccezioni causate dall'annullamento della registrazione e dalla registrazione automatica del provider   
* perf: consente di mantenere la cache del token ADAL in memoria fino alla chiusura di processo ([#2603](https://github.com/Azure/azure-cli/issues/2603))
* Consente di correggere i byte restituiti da impronta digitale hex -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))
* Download dei certificati del Key Vault e dell'integrazione AAD SP migliorati ([#3003](https://github.com/Azure/azure-cli/issues/3003))
* Aggiunge il percorso di Python per "az —version" ([#2986](https://github.com/Azure/azure-cli/issues/2986))
* login: supporta l'accesso quando non sono presenti sottoscrizioni ([#2929](https://github.com/Azure/azure-cli/issues/2929))
* core: consente di correggere un errore quando si effettua l'accesso usando un'entità servizio due volte ([#2800](https://github.com/Azure/azure-cli/issues/2800))
* core: consente al percorso del file accessTokens.json di poter essere configurato tramite un env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))
* core: consente ai valori predefiniti configurati di essere applicati solo ad argomenti facoltativi ([#2703](https://github.com/Azure/azure-cli/issues/2703))
* core: prestazioni migliorate
* core: certificati CA personalizzati: supporta l'impostazione della variabile di ambiente REQUESTS_CA_BUNDLE
* core: configurazione del cloud: usa l'endpoint "gestione risorse" se l'endpoint "gestione" non è impostato

### <a name="acs"></a>ACS

* consente di correggere il conteggio di master e agenti affinché sia un numero intero anziché una stringa
* espone "az acs create --no-wait" e "az acs wait" alla creazione asincrona
* espone "az acs create --validate" alle convalide del test controllato
* rimuove il profilo di Windows prima di INSERIRE la chiamata del comando scale ([#2755](https://github.com/Azure/azure-cli/issues/2755))

### <a name="appservice"></a>AppService

* functionapp: aggiunge supporti functionapp completi, tra cui create, show, list, delete, hostname, ssl e così via
* Aggiunta di servizi di Team (vsts) come opzione di consegna continua a "appservice web source-control config"
* Consente di creare "az webapp" per sostituire "az appservice web". Per la compatibilità con le versioni precedenti, "az appservice web" viene mantenuta per 2 versioni
* Espone gli argomenti per configurare la distribuzione e "stack di runtime" su webapp
* Espone "webapp list-runtimes"
* supporta le stringhe di connessione per la configurazione ([#2647](https://github.com/Azure/azure-cli/issues/2647))
* supporta lo scambio di slot con anteprima
* Errori di polacco neii comandi appservice ([#2948](https://github.com/Azure/azure-cli/issues/2948))
* Usa il gruppo di risorse del piano del servizio app per le operazioni cert ([#2750](https://github.com/Azure/azure-cli/issues/2750))

### <a name="cosmosdb"></a>CosmosDB

* Rinomina il modulo documentdb in cosmosdb.
* Aggiunto il supporto per le API del piano di dati documentdb: gestione di database e raccolta
* Aggiunto il supporto per abilitare il failover automatico negli account del database
* Aggiunto il supporto per nuovi criteri di coerenza ConsistentPrefix

### <a name="data-lake-analytics"></a>Analisi Data Lake

* Consente di correggere un bug in cui il filtro dei risultati e lo stato degli elenchi del processo genererebbe un errore.
* Aggiunge il supporto per il tipo di elementi del nuovo catalogo: pacchetto. accessibili tramite: `az dla catalog package`
* È possibile elencare gli elementi seguenti del catalogo da un database, senza necessità delle specifiche dello schema:

  * Tabella
  * Funzione con valori di tabella
  * Visualizza
  * Statistiche tabelle. Questo elemento può essere elencato anche con uno schema, ma senza specificare un nome di tabella.

### <a name="data-lake-store"></a>Data Lake Store

* Aggiorna la versione dell'SDK del file system sottostante, che offre un supporto migliore per la gestione di scenari con limitazione lato server.
* Migliora le prestazioni di carico del pacchetto e l'esecuzione del comando ([#2819](https://github.com/Azure/azure-cli/issues/2819))
* guida mancate per la presentazione di accesso. aggiunta. ([#2743](https://github.com/Azure/azure-cli/issues/2743))

### <a name="find"></a>Find

* migliora i risultati di ricerca e consente di controllare le versioni dell'indice di ricerca

### <a name="keyvault"></a>Insieme di credenziali delle chiavi

* BC: `az keyvault certificate download` modifica -e dalla stringa o dal binario in PEM o DER per rappresentare meglio le opzioni
* BC: rimuove --expires e --not-before da `keyvault certificate create` poiché questi parametri non sono supportati dal servizio.
* Aggiunge il parametro --validity a `keyvault certificate create` per eseguire l'override in modo selettivo del valore in --policy
* Consente di risolvere i problemi in `keyvault certificate get-default-policy` laddove sono stati esposti "expires" e "not_before", ma non "validity_in_months".
* correzione di keyvault per l'importazione di pem e pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))

### <a name="lab"></a>Lab

* Aggiunta dei comandi create, show, delete e list per l'ambiente nel laboratorio.
* Aggiunta di comandi show e list per visualizzare i modelli ARM nel laboratorio.
* Aggiunta del flag --environment in `az lab vm list` per filtrare le macchine virtuali in base all'ambiente nel laboratorio.
* Aggiunge il comando di convenienza `az lab formula export-artifacts` per esportare lo scaffolding dell'elemento all'interno della formula di Lab.
* Aggiunge i comandi per gestire i segreti in Lab.

### <a name="monitor"></a>Monitorare

* Correzione di bug: modellazione di `--actions` in `az alert-rules create` per usare una stringa JSON ([#3009](https://github.com/Azure/azure-cli/issues/3009))
* Correzione di bug: diagnostic settings create non accetta i registri/le metriche dei comandi show ([#2913](https://github.com/Azure/azure-cli/issues/2913))

### <a name="network"></a>Rete

* Aggiunge il comando `network watcher test-connectivity`.
* Aggiunge il supporto per il parametro `--filters` per `network watcher packet-capture create`.
* Aggiunge il supporto per lo svuotamento della connessione del gateway applicazione.
* Aggiunge il supporto per la configurazione dell'insieme di regole WAF del gateway applicazione.
* Aggiunge il supporto per le regole e i filtri di route ExpressRoute.
* Aggiunge il supporto per il routing geografico di TrafficManager.
* Aggiunge il supporto per i selettori di traffico basati su criteri di connessione VPN.
* Aggiunge il supporto per i criteri IPSec della connessione VPN.
* Correzione di bug con `vpn-connection create` quando si usano i parametri `--no-wait` o `--validate`.
* Aggiunge il supporto per i gateway di rete virtuale attivo/attivo
* Rimuove i valori null i valori dall'output dei comandi `network vpn-connection list/show`.
* BC: correzione di bug nell'output di `vpn-connection create` 
* Corregge i bug in cui l'argomento "--key-length" di "vpn-connection create"' non è stato analizzato correttamente.
* Corregge i bug in `dns zone import` in cui i record non sono stati importati correttamente.
* Corregge i bug laddove `traffic-manager endpoint update` non funzionava.
* Aggiunge i comandi di anteprima "network watcher".

### <a name="profile"></a>Profilo

* Supporta l'accesso quando non sono state trovate sottoscrizioni ([#2560](https://github.com/Azure/azure-cli/issues/2560))
* Supporta l'abbreviazione del nome dei parametri in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))

### <a name="redis"></a>Redis

* Aggiunta del comando update che offre anche la possibilità di passare alla cache Redis
* Il comando "update-settings" viene deprecato.

### <a name="resource"></a>Risorsa

* Aggiunge i comandi managedapp e managedapp definition ([#2985](https://github.com/Azure/azure-cli/issues/2985))
* Supporta i comandi "provider operation" ([#2908](https://github.com/Azure/azure-cli/issues/2908))
* Supporta la creazione della risorsa generica ([#2606](https://github.com/Azure/azure-cli/issues/2606))
* Corregge l'analisi della risorsa e la ricerca della versione API. ([#2781](https://github.com/Azure/azure-cli/issues/2781))
* Aggiunge docs ad az lock update. ([#2702](https://github.com/Azure/azure-cli/issues/2702))
* Genera un errore se si tenta di elencare le risorse per un gruppo che non esiste. ([#2769](https://github.com/Azure/azure-cli/issues/2769))
* [Compute] Risolve i problemi con l'aggiornamento dei set di disponibilità VMSS e della macchina virtuale. ([#2773](https://github.com/Azure/azure-cli/issues/2773))
* Correzione della creazione e dell'eliminazione del blocco se parent-resource-path è Nessuno ([#2742](https://github.com/Azure/azure-cli/issues/2742))

### <a name="role"></a>Ruolo

* create-for-rbac: assicura che la data di fine di SP non superi la data di scadenza del certificato ([#2989](https://github.com/Azure/azure-cli/issues/2989))
* RBAC: aggiunge il supporto completo ad "ad group" ([#2016](https://github.com/Azure/azure-cli/issues/2016))
* role: corregge i problemi in role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))
* create-for-rbac: garantisce che venga presa la password indicata

### <a name="sql"></a>SQL

* Aggiunti i comandi az sql server list-usages e az sql db list-usages.
* SQL: possibilità di connettersi direttamente al provider di risorse ([#2832](https://github.com/Azure/azure-cli/issues/2832))

### <a name="storage"></a>Archiviazione

* Percorso predefinito al percorso del gruppo di risorse per `storage account create`.
* Aggiunge il supporto per la copia di BLOB incrementale
* Aggiunge il supporto per il upload di BLOB in blocchi di grandi dimensioni
* Modifica le dimensioni del blocco in 100 MB quando il file da caricare supera i 200 GB

### <a name="vm"></a>VM

* avail-set: rende facoltativo il conteggio del dominio UD&FD

  note: comandi della VM nei cloud sovrani. Evitare le funzionalità correlate al disco gestito, tra cui:
  1. az disk/snapshot/image
  2. az vm/vmss disk
  3. All'interno di "az vm/vmss create" usare "—use-unmanaged-disk" per evitare che il disco gestito. Funziona anche con altri comandi
* vm/vmss: migliora il testo di avviso quando si generano coppie di chiavi SSH
* vm/vmss: supporta la creazione da un'immagine del marketplace che richiede informazioni sul piano ([#1209](https://github.com/Azure/azure-cli/issues/1209))


## <a name="april-3-2017"></a>3 aprile 2017

Versione 2.0.2

In questa versione sono stati rilasciati i componenti ACR, Batch, KeyVault e SQL.

```
azure-cli (2.0.2)
 
acr (2.0.0)
acs (2.0.2)
appservice (0.1.2)
batch (2.0.0)
cloud (2.0.0)
component (2.0.0)
configure (2.0.2)
container (0.1.2)
core (2.0.2)
documentdb (0.1.2)
feedback (2.0.0)
find (0.0.1b1)
iot (0.1.2)
keyvault (2.0.0)
lab (0.0.1)
monitor (0.0.1)
network (2.0.2)
nspkg (2.0.0)
profile (2.0.2)
redis (0.1.1b3)
resource (2.0.2)
role (2.0.1)
sql (2.0.0)
storage (2.0.2)
vm (2.0.2)
```

### <a name="core"></a>Core

* Aggiunta dei moduli acr, lab, monitor e find all'elenco predefinito.
* Login: esclusione del tenant errato ([#2634](https://github.com/Azure/azure-cli/pull/2634))
* login: impostazione della sottoscrizione predefinita su una con lo stato "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))
* Aggiunta di comandi wait e di supporto per --no-wait a più comandi ([#2524](https://github.com/Azure/azure-cli/pull/2524))
* core: supporto per accesso mediante entità servizio con un certificato ([#2457](https://github.com/Azure/azure-cli/pull/2457))
* Aggiunta della richiesta dei parametri di modello mancanti. ([#2364](https://github.com/Azure/azure-cli/pull/2364))
* Supporto per l'impostazione di valori predefiniti per argomenti comuni ad esempio gruppo di risorse predefinito, Web predefinito, macchina virtuale predefinita
* Supporto per l'accesso al tenant specifico
 
### <a name="acs"></a>ACS

* [ACS] Aggiunta di supporto per la configurazione di un cluster ACS predefinito ([#2554](https://github.com/Azure/azure-cli/pull/2554))
* Aggiunta di supporto per la richiesta di password della chiave SSH. ([#2044](https://github.com/Azure/azure-cli/pull/2044))
* Aggiunta di supporto per i cluster Windows. ([#2211](https://github.com/Azure/azure-cli/pull/2211))
* Passaggio dal ruolo Proprietario al ruolo Collaboratore. ([#2321](https://github.com/Azure/azure-cli/pull/2321))
 
### <a name="appservice"></a>AppService

* appservice: supporto per ottenere l'indirizzo IP esterno usato per i record DNS A ([#2627](https://github.com/Azure/azure-cli/pull/2627))
* appservice: supporto dell'associazione di certificati jolly ([#2625](https://github.com/Azure/azure-cli/pull/2625))
* appservice: supporto dell'elenco di profili di pubblicazione ([#2504](https://github.com/Azure/azure-cli/pull/2504))
* AppService - attivazione della sincronizzazione del controllo dopo la configurazione ([#2326](https://github.com/Azure/azure-cli/pull/2326))
 
### <a name="datalake"></a>DataLake

* Versione iniziale del modulo Data Lake Analytics.
* Versione iniziale del modulo Data Lake Store.
 
### <a name="docuemntdb"></a>DocuemntDB

* DocumentDB: aggiunta di supporto per l'elenco di stringhe di connessione ([#2580](https://github.com/Azure/azure-cli/pull/2580))

### <a name="vm"></a>VM

* [Compute] Aggiunta di supporto per AppGateway alla creazione di set di scalabilità di macchine virtuali ([#2570](https://github.com/Azure/azure-cli/pull/2570))
* [VM/VMSS] Miglioramento del supporto per memorizzazione nella cache del disco ([#2522](https://github.com/Azure/azure-cli/pull/2522))
* VM/VMSS: inclusione di logica di convalida credenziali usata dal portale ([#2537](https://github.com/Azure/azure-cli/pull/2537))
* Aggiunta di comandi wait e di supporto per --no-wait ([#2524](https://github.com/Azure/azure-cli/pull/2524))
* Virtual machine scale set: supporto * per elencare le visualizzazioni di istanza tra le macchine virtuali ([#2467](https://github.com/Azure/azure-cli/pull/2467))
* Aggiunta di --secrets per la macchina virtuale e il set di scalabilità di macchine virtuali ([#2212}(https://github.com/Azure/azure-cli/pull/2212))
* Consentita la creazione di macchine virtuali con disco rigido virtuale specializzato ([#2256](https://github.com/Azure/azure-cli/pull/2256))

## <a name="february-27-2017"></a>27 febbraio 2017

Versione 2.0.0

Questa versione dell'interfaccia della riga di comando di Azure 2.0 è la prima versione disponibile a livello generale.
La disponibilità generale si applica ai moduli comandi seguenti:
- Servizio contenitore (acs)
- Compute (inclusi Resource Manager, macchina virtuale, set di scalabilità di macchine virtuali, Managed Disks)
- Rete
- Archiviazione

Questi moduli comandi possono essere usati nella produzione e sono supportati dal contratto di servizio Microsoft standard.
È possibile segnalare i problemi direttamente al supporto tecnico Microsoft o tramite l'[elenco di problemi github](https://github.com/azure/azure-cli/issues/).
È possibile porre domande su [StackOverflow usando il tag azure-cli](http://stackoverflow.com/questions/tagged/azure-cli) o contattare il team del prodotto all'indirizzo [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).
È possibile fornire commenti e suggerimenti dalla riga di comando con il comando `az feedback`.

I comandi in questi moduli sono stabili e non si prevede che la sintassi cambi nei prossimi rilasci di questa versione dell'interfaccia della riga di comando di Azure.

Per verificare la versione dell'interfaccia della riga di comando, usare `az --version`.
L'output elenca la versione dell'interfaccia della riga di comando stessa (2.0.0 in questo rilascio), i singoli moduli comandi e le versioni di Python e GCC in uso.

```
azure-cli (2.0.0)

acs (2.0.0)
appservice (0.1.1b5)
batch (0.1.1b4)
cloud (2.0.0)
component (2.0.0)
configure (2.0.0)
container (0.1.1b4)
core (2.0.0)
documentdb (0.1.1b2)
feedback (2.0.0)
iot (0.1.1b3)
keyvault (0.1.1b5)
network (2.0.0)
nspkg (2.0.0)
profile (2.0.0)
redis (0.1.1b3)
resource (2.0.0)
role (2.0.0)
sql (0.1.1b5)
storage (2.0.0)
vm (2.0.0)
 
Python (Darwin) 2.7.10 (default, Jul 30 2016, 19:40:32) 
[GCC 4.2.1 Compatible Apple LLVM 8.0.0 (clang-800.0.34)]
```

> [!Note]
> Alcuni dei moduli del comando presentano un suffisso "b*n*" o "rc*n*".
> Questi moduli comandi sono ancora in fase di anteprima e saranno disponibili a livello generale in futuro.

Sono anche disponibili build di anteprima notturne dell'interfaccia della riga di comando.
Per informazioni, vedere le istruzioni su come [ottenere le build notturne](https://github.com/Azure/azure-cli#nightly-builds) e le istruzioni sull'[impostazione per gli sviluppatori e sul codice per i collaboratori](https://github.com/Azure/azure-cli#developer-setup).

È possibile segnalare problemi relative alle build di anteprima notturne nei seguenti modi:
- Segnalare i problemi tramite l'[elenco di problemi github](https://github.com/azure/azure-cli/issues/)
- Contattare il tema del prodotto all'indirizzo [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).
- Fornire commenti e suggerimenti dalla riga di comando con il comando `az feedback`.

