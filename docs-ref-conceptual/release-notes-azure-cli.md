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
ms.openlocfilehash: 56190b653ab9765017fffd1699056de7eae2db77
ms.sourcegitcommit: bcf93ad8ed8802072249cd8187cd4420da89b4c6
ms.translationtype: HT
ms.contentlocale: it-IT
---
# <a name="azure-cli-20-release-notes"></a>Note sulla versione dell'interfaccia della riga di comando di Azure 2.0

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
È possibile segnalare i problemi direttamente al supporto tecnico Microsoft o tramite l'[elenco di problemi github](https://github.com/azure/azure-cli/issues).
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
> Alcuni dei moduli presentano un suffisso "b*n*" o "rc*n*".
> Questi moduli comandi sono ancora in fase di anteprima e saranno disponibili a livello generale in futuro.

Sono anche disponibili build di anteprima notturne dell'interfaccia della riga di comando.
Per informazioni, vedere le istruzioni su come [ottenere le build notturne](https://github.com/Azure/azure-cli#nightly-builds) e le istruzioni sull'[impostazione per gli sviluppatori e sul codice per i collaboratori](https://github.com/Azure/azure-cli#developer-setup).

È possibile segnalare problemi relative alle build di anteprima notturne nei seguenti modi:
- Segnalare i problemi tramite l'[elenco di problemi github](https://github.com/azure/azure-cli/issues)
- Contattare il tema del prodotto all'indirizzo [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).
- Fornire commenti e suggerimenti dalla riga di comando con il comando `az feedback`.

