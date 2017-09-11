---
title: Note sulla versione dell'interfaccia della riga di comando di Azure 2.0
description: Informazioni sugli ultimi aggiornamenti dell'interfaccia della riga di comando di Azure 2.0
keywords: Interfaccia della riga di comando di Azure 2.0, note sulla versione
author: sptramer
ms.author: sttramer
manager: douge
ms.date: 04/03/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ce0428f7-0a59-4e72-9237-d907b171af51
ms.openlocfilehash: e893b99349bbf2a5eec8af254158eb07001f1da7
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/04/2017
---
# <a name="azure-cli-20-release-notes"></a>Note sulla versione dell'interfaccia della riga di comando di Azure 2.0

## <a name="august-28-2017"></a>28 agosto 2017

Versione 2.0.15

### <a name="cli"></a>CLI

* Aggiunta di una nota legale a `--version`.

### <a name="acs"></a>ACS

* Correzione delle aree di anteprima.
* Formattazione corretta del valore `dns_name_prefix` predefinito.
* Ottimizzazione dell'output del comando di ACS.

### <a name="appservice"></a>Servizio app

* [MODIFICA DI RILIEVO] Correzione di incoerenze nell'output di `az webapp config appsettings [delete|set]`
* Aggiunta di un nuovo alias di `-i` per `az webapp config container set --docker-custom-image-name`
* Esposizione di `az webapp log show`
* Esposizione di nuovi argomenti da `az webapp delete` per mantenere il piano di servizio app, le metriche o la registrazione DNS
* Correzione: Rilevamento corretto delle impostazioni dello slot

### <a name="iot"></a>IoT

* Correzione #3934: La creazione di criteri non cancella più i criteri esistenti

### <a name="network"></a>Rete

* [MODIFICA DI RILIEVO] Ridenominazione di `vnet list-private-access-services` in `vnet list-endpoint-services`
* [MODIFICA DI RILIEVO] Ridenominazione dell'opzione `--private-access-services` in `--service-endpoints` per `vnet subnet [create|update]`
* Aggiunta del supporto per più indirizzi IP e intervalli di porte in `nsg rule [create|update]`
* Aggiunta del supporto per SKU a `lb create`
* Aggiunta del supporto per SKU a `public-ip create`

### <a name="profile"></a>Profilo

* Esposizione di `--msi` e `--msi-port` per l'accesso tramite l'identità della macchina virtuale

### <a name="service-fabric"></a>Service Fabric

* Versione di anteprima
* Semplificazione delle regole relative a utente/password del Registro di sistema per il comando
* Correzione del problema relativo alla richiesta della password per l'utente anche dopo il passaggio del parametro
* Aggiunta del supporto per il valore `registry_cred` vuoto

### <a name="storage"></a>Archiviazione

* Abilitazione della configurazione del livello BLOB
* Aggiunta degli argomenti `--bypass` e `--default-action` a `storage account [create|update]` per supportare il tunneling del servizio
* Aggiunta di comandi per aggiungere regole della rete virtuale e regole basate su indirizzi IP a `storage account network-rule`  
* Abilitazione della crittografia del servizio tramite chiave gestita dal cliente
* [MODIFICA DI RILIEVO] Ridenominazione dell'opzione `--encryption` in `--encryption-services` per il comando `az storage account create and az storage account update`
* Correzione #4220: `az storage account update encryption`: Mancata corrispondenza della sintassi

### <a name="vm"></a>VM

* Risoluzione del problema relativo alla visualizzazione di informazioni aggiuntive errate per `vmss get-instance-view` quando si usa `--instance-id *`
* Aggiunta del supporto per `--lb-sku` a `vmss create`: 
* Rimozione dei nomi di persone dall'elenco di nomi non consentiti dell'amministratore per `[vm|vmss] create` 
* Risoluzione del problema relativo alla generazione di un errore da parte di `[vm|vmss] create` in caso di impossibilità di estrazione delle informazioni del piano da un'immagine
* Risoluzione del problema relativo all'arresto anomalo in caso di creazione di un set di scalabilità vmms con un servizio di bilanciamento del carico interno
* Risoluzione del problema relativo al mancato funzionamento dell'argomento `--no-wait` con `vm availability-set create`


## <a name="august-15-2017"></a>15 agosto 2017

Versione 2.0.14

### <a name="acs"></a>ACS

* Correzione del numero di porta sshMaster0 per kubernetes

### <a name="appservice"></a>Servizio app

* Correzione dell'eccezione generata durante la creazione di una nuova app Web Linux basata su Git

### <a name="event-grid"></a>Griglia di eventi

* Aggiunta di dipendenze di SDK

## <a name="august-11-2017"></a>11 agosto 2017

Versione 2.0.13

### <a name="acs"></a>ACS

* Aggiunta di altre aree di anteprima

### <a name="batch"></a>Batch

* Aggiornamento a Batch SDK 3.1.0 e Batch Management SDK 4.1.0
* Aggiunta di un nuovo comando per visualizzare il numero di attività di un processo
* Correzione di un bug nell'elaborazione dell'URL della firma di accesso condiviso del file di risorse
* L'endpoint dell'account Batch supporta ora il prefisso facoltativo 'https://'
* Supporto per l'aggiunta di elenchi di più di 100 attività a un processo
* Aggiunta della registrazione di debug per il caricamento del modulo di comandi delle estensioni

### <a name="component"></a>Componente

* Aggiunta dell'avviso relativo a elementi deprecati ai comandi 'az component'

### <a name="container"></a>Contenitore

* `create`: risoluzione del problema relativo all'impossibilità di usare il segno di uguale all'interno di una variabile di ambiente


### <a name="data-lake-store"></a>Data Lake Store

* Abilitazione del controllo dell'avanzamento

### <a name="event-grid"></a>Griglia di eventi

* Versione iniziale

### <a name="network"></a>Rete

* `lb`: correzione del problema relativo alla risoluzione non corretta di determinati nomi di risorse figlio in caso di omissione
* `application-gateway {subresource} delete`: correzione del problema relativo al mancato rispetto di `--no-wait`
* `application-gateway http-settings update`: risoluzione del problema relativo all'impossibilità di disattivare `--connection-draining-timeout`
* Risoluzione del problema relativo all'argomento imprevisto `sa_data_size_kilobyes` della parola chiave con `az network vpn-connection ipsec-policy add`

### <a name="profile"></a>Profilo

* `account list`: aggiunta di `--refresh` per la sincronizzazione delle sottoscrizioni più recenti dal server

### <a name="storage"></a>Archiviazione

* Abilitazione dell'aggiornamento dell'account di archiviazione con l'identità assegnata dal sistema

### <a name="vm"></a>VM

* `availability-set`: esposizione del numero di domini di errore in fase di conversione
* Esposizione del comando `list-skus`
* Supporto per l'assegnazione di identità senza la creazione di assegnazioni di ruolo
* Applicazione di SKU di archiviazione in fase di collegamento del dischi dati
* Rimozione del nome del disco del sistema operativo predefinito e dello SKU di archiviazione in caso di uso di Managed Disks


## <a name="july-28-2017"></a>28 luglio 2017

Versione 2.0.12

* Aggiunta di comandi del contenitore
* Aggiunta di moduli relativi a fatturazione e consumo

```
azure-cli (2.0.12)  

acr (2.0.9)  
acs (2.0.11)  
appservice (0.1.11)  
batch (3.0.3)  
billing (0.1.3)  
cdn (0.0.6)  
cloud (2.0.7)  
cognitiveservices (0.1.6)  
command-modules-nspkg (2.0.1)  
component (2.0.6)  
configure (2.0.10)  
consumption (0.1.3)  
container (0.1.7)  
core (2.0.12)  
cosmosdb (0.1.11)  
dla (0.0.10)  
dls (0.0.11)  
feedback (2.0.6)  
find (0.2.6)  
interactive (0.3.7)  
iot (0.1.10)  
keyvault (2.0.8)  
lab (0.0.9)  
monitor (0.0.8)  
network (2.0.11)  
nspkg (3.0.1)  
profile (2.0.9)  
rdbms (0.0.5)  
redis (0.2.7)  
resource (2.0.11)  
role (2.0.9)  
sf (1.0.5)  
sql (2.0.8)  
storage (2.0.11)  
vm (2.0.11) 
```

### <a name="core"></a>Core

* Restituzione di informazioni di autorizzazioni dell'SDK per entità servizio con certificati
* Risoluzione del problema relativo alle eccezioni nell'avanzamento delle distribuzioni
* Uso dell'endpoint ARM dal cloud corrente per la creazione del client di sottoscrizione
* Miglioramento della gestione simultanea del file clouds.config (#3636)
* Aggiornamento dell'ID della richiesta client per ogni esecuzione del comando
* Creazione dei client di sottoscrizione con il profilo SDK corretto (#3635)
* Creazione di report relativi all'avanzamento per le distribuzioni dei modelli (#3510)
* Aggiunta del supporto per la selezione di campi di output della tabella tramite una query jmespath (#3581)
* Miglioramento della disattivazione dell'audio degli argomenti di analisi e dell'aggiunta di cronologia con gesti (#3434)
* Creazione di client di sottoscrizione con il profilo SDK corretto
* Spostamento di tutti i file di registrazione esistenti nella cartella più recente
* Risoluzione del problema relativo all'idempotenza per la creazione di VM/VMSS (#3586)
* I percorsi dei comandi non rispettano più la distinzione tra maiuscole/minuscole
* Alcuni parametri di tipo booleano non rispettano più la distinzione tra maiuscole/minuscole
* Supporto dell'accesso ad AD FS nel server locale come Azure Stack
* Risoluzione del problema relativo alle operazioni di scrittura simultanee nel file clouds.config (#3255)

### <a name="acr"></a>ACR

* Aggiunta del comando `show-usage` per i registri gestiti
* Supporto dell'aggiornamento dello SKU per i registri gestiti
* Aggiunta dei registri gestiti con SKU gestito
* Aggiunta di webhook per registri gestiti con modulo di comandi webhook ACR
* Aggiunta dell'autenticazione AAD con il comando di accesso di ACR
* Aggiunta del comando di eliminazione per repository Docker, manifesti e tag

### <a name="acs"></a>ACS

* Supporto per l'API versione 2017-07-01

### <a name="appservice"></a>Servizio app

* Risoluzione del bug relativo alla mancata restituzione di valori per l'elenco di app Web Linux
* Supporto per il recupero di credenziali da ACR
* Rimozione di tutti i comandi in `appservice web`
* Mascheramento delle password del registro Docker dall'output del comando (#3656)
* Conferma dell'uso del browser predefinito in macOS senza errori (#3623)
* Miglioramento della Guida di `webapp log tail` e `webapp log download` (#3624)
* Esposizione del comando `traffic-routing` per la configurazione del routing statico (#3566)
* Aggiunta di correzioni relative all'affidabilità nella configurazione del controllo del codice sorgente (#3245)
* Rimozione dell'argomento `--node-version` non supportato da `webapp config update` per le app Web Windows. Viene usato `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`

### <a name="batch"></a>Batch

* Aggiornamento a Batch SDK 3.0.0 con supporto per le macchine virtuali a priorità bassa nei pool
* Ridenominazione per `pool create` dell'opzione `--target-dedicated` in `--target-dedicated-nodes`
* Aggiunta in `pool create` delle opzioni `--target-low-priority-nodes` e `--application-licenses`

### <a name="cdn"></a>RETE CDN

* Miglioramento del messaggio di errore per `cdn endpoint list` nel caso in cui il profilo specificato da `--profile-name` non esista.

### <a name="cloud"></a>Cloud

* Modifica della versione dell'API dell'endpoint dei metadati del cloud nel formato AAAA-MM-GG
* L'endpoint della raccolta non è obbligatorio
* Supporto per la registrazione del cloud solo con l'endpoint di gestione delle risorse ARM
* Aggiunta di un'opzione per `cloud set` per la scelta del profilo durante la selezione del cloud corrente
* Esposizione di `endpoint_vm_image_alias_doc`

### <a name="cosmosdb"></a>Cosmos DB

* Correzione dell'errore che consente la creazione di una raccolta con una chiave di partizione personalizzata
* Aggiunta di supporto per la durata TTL predefinita della raccolta.

### <a name="data-lake-analytics"></a>Data Lake Analytics

* Aggiunta di comandi per la gestione dei criteri di calcolo sotto l'intestazione `dla account compute-policy`
* Aggiunta di `dla job pipeline show`
* Aggiunta di `dla job recurrence list`

### <a name="data-lake-store"></a>Data Lake Store

* Aggiunta di supporto per la rotazione delle chiavi dell'insieme di credenziali delle chiavi gestito dall'utente in `dls account update`
* Aggiornamento della versione dell'SDK del file system del Data Lake Store sottostante per risolvere un problema di prestazioni
* Aggiunta del comando `dls enable-key-vault`. Questo comando prova ad abilitare un'istanza di Key Vault fornita dall'utente per l'uso per la crittografia dei dati in un account Data Lake Store

### <a name="interactive"></a>Interattività

* Miglioramento del tempo di avvio tramite i comandi memorizzati nella cache
* Miglioramento della copertura dei test
* Miglioramento del gesto '?' per consentire anche l'inserimento nel comando successivo
* Risoluzione degli errori relativi all'interattività con il profilo 2017-03-09-profile-preview (#3587)
* Autorizzazione di `--version` come parametro per la modalità interattiva (#3645)
* Interruzione della generazione di errori da parte della modalità interattiva relativi al completamento delle convalide (#3570)
* Creazione di report relativi all'avanzamento per le distribuzioni dei modelli (#3510)
* Aggiunta del flag `--progress`
* Rimozione di `--debug` e `--verbose` dai completamenti
* Rimozione di `interactive` dai completamenti (#3324)

### <a name="iot"></a>IoT

* Correzione del problema relativo alla creazione di criteri, che non cancella più i criteri esistenti. (#3934)

### <a name="key-vault"></a>Insieme di credenziali delle chiavi

* Aggiunta di comandi per le funzionalità di ripristino di Key Vault:
  * Sottocomandi di `keyvault`: `purge`, `recover`, `keyvault list-deleted`
  * Sottocomandi di `keyvault secret`: `backup`, `restore`, `purge`, `recover`, `list-deleted`
  * Sottocomandi di `keyvault certificate`: `purge`, `recover`, `list-deleted`
  * Sottocomandi di `keyvault key`: `purge`, `recover`, `list-deleted`
* Aggiunta dell'integrazione dell'insieme di credenziali delle chiavi dell'entità servizio (#3133)
* Aggiornamento del piano dati dell'insieme di credenziali delle chiavi a 0.3.2. (#3307)

### <a name="lab"></a>Lab

* Aggiunta del supporto per la rivendicazione di eventuali macchine virtuali nel laboratorio tramite `az lab vm claim`
* Aggiunta del formattatore dell'output della tabella per `az lab vm list` e `az lab vm show`

### <a name="monitor"></a>Monitorare

* Correzione relativa al file del modello con il comando `monitor autoscale-settings get-parameters-template` (#3349)
* Ridenominazione di `monitor alert-rule-incidents list` in `monitor alert list-incidents`
* Ridenominazione di `monitor alert-rule-incidents show` in `monitor alert show-incident`
* Ridenominazione di `monitor metric-defintions list` in `monitor metrics list-definitions`
* Ridenominazione di `monitor alert-rules` in `monitor alert`
* Modifica di `monitor alert create`:
  * I sottocomandi `condition` e `action` non accettano più JSON
  * Aggiunta di numerosi parametri per la semplificazione del processo di creazione delle regole
  * `location` non è più obbligatorio
  * Aggiunta del supporto di nome ID per la destinazione
  * Rimozione di `--alert-rule-resource-name`
  * Ridenominazione di `is-enabled` in `enabled`, non più obbligatorio
  * I valori predefiniti di `description` sono ora basati sulla condizione specificata
  *  Aggiunta di esempi per illustrare in modo più chiaro il nuovo formato
* Supporto di nomi o ID per i comandi `monitor metric`
* Aggiunta di argomenti ed esempi utili a `monitor alert rule update`

### <a name="network"></a>Rete

* Aggiunta del comando `list-private-access-services`
* Aggiunta dell'argomento `--private-access-services` a `vnet subnet create` e `vnet subnet update`
* Risoluzione del problema relativo all'esito negativo di `application-gateway redirect-config create`
* Risoluzione del problema relativo al mancato funzionamento di `application-gateway redirect-config update` con `--no-wait`
* Risoluzione del bug relativo all'uso dell'argomento `--servers` con `application-gateway address-pool create` e `application-gateway address-pool update`
* Aggiunta dei comandi `application-gateway redirect-config`
* Aggiunta di comandi ad `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`
* Aggiunta di comandi ad `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`
* Aggiunta di argomenti ad `application-gateway http-settings create` e `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`
* Aggiunta di argomenti ad `application-gateway url-path-map create` e `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`
* Aggiunta dell'argomento `--redirect-config` a `application-gateway url-path-map rule create`
* Aggiunta del supporto per `--no-wait` a `application-gateway url-path-map rule delete`
* Aggiunta di argomenti ad `application-gateway probe create` e `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`
* Aggiunta dell'argomento `--redirect-config` a `application-gateway rule create` e `application-gateway rule update`
* Aggiunta del supporto per `--accelerated-networking` a `nic create` e `nic update`
* Rimozione dell'argomento `--internal-dns-name-suffix` da `nic create`
* Aggiunta del supporto per `--dns-servers` a `nic update` e `nic create`: aggiunta del supporto per --dns-servers
* Risoluzione del bug relativo al fatto che `local-gateway create` ignora `--local-address-prefixes`
* Aggiunta del supporto per `--dns-servers` a `vnet update`
* Risoluzione del bug relativo alla creazione di un peering senza filtro delle route con `express-route peering create`
* Risoluzione del bug relativo al mancato funzionamento di `--provider` e `--bandwidth` con `express-route update`
* Risoluzione del bug relativo alla logica delle impostazioni predefinite di `network watcher show-topology`
* Miglioramento della formattazione dell'output per `network list-usages`
* Uso dell'indirizzo IP del front-end predefinito per `application-gateway http-listener create` se ne esiste solo uno
* Uso del pool di indirizzi, delle impostazioni HTTP e del listener HTTP predefiniti per `application-gateway rule create` se ne esiste solo uno
* Uso dell'indirizzo IP del front-end e del pool back-end predefiniti per `lb rule create` se ne esiste solo uno
* Uso dell'indirizzo IP del front-end predefinito per `lb inbound-nat-rule create` se ne esiste solo uno

### <a name="profile"></a>Profilo

* Supporto dell'accesso all'interno di una VM con un'identità gestita
* Supporto dell'output per `account show` nel formato di file di autorizzazione di SDK
* Visualizzazione degli avvisi relativi a elementi deprecati quando si usa '--expanded-view'
* Aggiunta del comando `get-access-token` per fornire il token AAD non elaborato
* Supporto dell'accesso con un account utente senza sottoscrizioni associate

### <a name="rdbms"></a>RDBMS

* Supporto della creazione di elenchi di server in una sottoscrizione (#3417)
* Risoluzione del problema relativo alla mancata elaborazione di `%s` a causa dell'assenza del valore `% server_type` (#3393)
* Risoluzione del problema relativo alla mappa di origine del documento e aggiunta di un'attività di integrazione continua per la verifica (#3361)
* Risoluzione dei problemi della Guida di MySQL e PostgreSQL (#3369)

### <a name="resource"></a>Risorsa

* Miglioramento dei prompt relativi a parametri mancanti per `group deployment create`
* Miglioramento dell'analisi della sintassi di `--parameters KEY=VALUE`
* Risoluzione dei problemi relativi al mancato riconoscimento dei file di parametri di `group deployment create` con la sintassi `@<file>`
* Supporto dell'argomento `--ids` per i comandi `resource` e `managedapp`
* Risoluzione di alcuni messaggi relativi ad analisi ed errori (#3584)
* Risoluzione dei problemi relativi all'analisi di `--resource-type` per consentire al comando `lock` di accettare `<resource-namespace>` e `<resource-type>`
* Aggiunta della verifica del parametro per i modelli di collegamenti ai modelli (#3629)
* Aggiunta del supporto per specificare i parametri di distribuzione tramite la sintassi `KEY=VALUE`

### <a name="role"></a>Ruolo

* Supporto dell'output nel formato del file di autenticazione di SDK per `create-for-rbac`
* Pulizia delle assegnazioni di ruolo e dell'applicazione AAD correlata in caso di eliminazione di un'entità servizio (#3610)
* Inclusione del formato dell'ora negli argomenti `app create` per le descrizioni `--start-date` ed `--end-date`
* Visualizzazione degli avvisi relativi a elementi deprecati quando si usa `--expanded-view`
* Aggiunta dell'integrazione dell'insieme di credenziali delle chiavi ai comandi `create-for-rbac` e `reset-credentials`

### <a name="service-fabric"></a>Service Fabric
* Risoluzione di un problema relativo al troncamento dei file di grandi dimensioni nelle applicazioni in fase di caricamento (#3666)
* Aggiunta dei test per i comandi di Service Fabric (#3424)
* Risoluzione dei problemi di numerosi comandi di Service Fabric (#3234)

### <a name="sql"></a>SQL

* Rimozione del parametro `sql server create` `--identity` non funzionante
* Rimozione dei valori della password dall'output dei comandi `sql server create` e `sql server update`
* Aggiunta dei comandi `sql db list-editions` e `sql elastic-pool list-editions`

### <a name="storage"></a>Archiviazione

* Rimozione dell'opzione `--marker` dai comandi `storage blob list`, `storage container list` e `storage share list` (#3745)
* Abilitazione della creazione di un account di archiviazione solo HTTPS
* Aggiornamento delle metriche di archiviazione, della registrazione e dei comandi CORS (#3495)
* Nuova formulazione del messaggio di eccezione dall'aggiunta di CORS (#3638) (#3362)  
* Conversione del generatore in elenco in modalità di test controllato del comando Batch di download (#3592) 
* Risoluzione del problema relativo al test controllato di Batch del download di BLOB (#3640) (#3592)

### <a name="vm"></a>VM

* Supporto per la configurazione di nsg
* Risoluzione di un bug relativo alla configurazione non corretta del server DNS
* Supporto per le identità del servizio gestito
* Risoluzione del problema relativo al fatto che `cmss create` con un servizio di bilanciamento del carico esistente richiede `--backend-pool-name`.
* I dischi dati creati con LUN `vm image create` iniziano con 0


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
È possibile porre domande su [StackOverflow usando il tag azure-cli](http://stackoverflow.com/questions/tagged/azure-cli) o contattare il team del prodotto all'indirizzo [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). È possibile fornire commenti e suggerimenti dalla riga di comando con il comando `az feedback`.

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

