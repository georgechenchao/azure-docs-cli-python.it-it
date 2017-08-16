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
ms.contentlocale: it-IT
ms.lasthandoff: 05/11/2017
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="bd337-104">Note sulla versione dell'interfaccia della riga di comando di Azure 2.0</span><span class="sxs-lookup"><span data-stu-id="bd337-104">Azure CLI 2.0 release notes</span></span>

## <a name="may-10-2017"></a><span data-ttu-id="bd337-105">10 maggio 2017</span><span class="sxs-lookup"><span data-stu-id="bd337-105">May 10, 2017</span></span>

<span data-ttu-id="bd337-106">Versione 2.0.6</span><span class="sxs-lookup"><span data-stu-id="bd337-106">Version 2.0.6</span></span>

* <span data-ttu-id="bd337-107">documentdb rinominato come cosmosdb</span><span class="sxs-lookup"><span data-stu-id="bd337-107">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="bd337-108">Aggiunge rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="bd337-108">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="bd337-109">Include i moduli di Data Lake Store e Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bd337-109">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="bd337-110">Include i moduli di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="bd337-110">Include Cognitive Services module.</span></span>
* <span data-ttu-id="bd337-111">Include i moduli di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="bd337-111">Include Service Fabric module.</span></span>
* <span data-ttu-id="bd337-112">Include i moduli interattivi e rinomina az-shell.</span><span class="sxs-lookup"><span data-stu-id="bd337-112">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="bd337-113">Aggiunge il supporto per i comandi CDN.</span><span class="sxs-lookup"><span data-stu-id="bd337-113">Add support for CDN commands.</span></span>
* <span data-ttu-id="bd337-114">Rimuove il modulo del contenitore.</span><span class="sxs-lookup"><span data-stu-id="bd337-114">Remove Container module.</span></span>
* <span data-ttu-id="bd337-115">Aggiunge "az -v" come collegamento per "az -- version" ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="bd337-115">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="bd337-116">Migliora le prestazioni di carico del pacchetto e l'esecuzione del comando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="bd337-116">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="bd337-117">Core</span><span class="sxs-lookup"><span data-stu-id="bd337-117">Core</span></span>

* <span data-ttu-id="bd337-118">core: consente di acquisire le eccezioni causate dall'annullamento della registrazione e dalla registrazione automatica del provider</span><span class="sxs-lookup"><span data-stu-id="bd337-118">core: capture exceptions caused by unregistered provider and auto-register it</span></span>   
* <span data-ttu-id="bd337-119">perf: consente di mantenere la cache del token ADAL in memoria fino alla chiusura di processo ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="bd337-119">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="bd337-120">Consente di correggere i byte restituiti da impronta digitale hex -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="bd337-120">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="bd337-121">Download dei certificati del Key Vault e dell'integrazione AAD SP migliorati ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="bd337-121">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="bd337-122">Aggiunge il percorso di Python per "az —version" ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="bd337-122">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="bd337-123">login: supporta l'accesso quando non sono presenti sottoscrizioni ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="bd337-123">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="bd337-124">core: consente di correggere un errore quando si effettua l'accesso usando un'entità servizio due volte ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="bd337-124">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="bd337-125">core: consente al percorso del file accessTokens.json di poter essere configurato tramite un env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="bd337-125">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="bd337-126">core: consente ai valori predefiniti configurati di essere applicati solo ad argomenti facoltativi ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="bd337-126">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="bd337-127">core: prestazioni migliorate</span><span class="sxs-lookup"><span data-stu-id="bd337-127">core: Improved performance</span></span>
* <span data-ttu-id="bd337-128">core: certificati CA personalizzati: supporta l'impostazione della variabile di ambiente REQUESTS_CA_BUNDLE</span><span class="sxs-lookup"><span data-stu-id="bd337-128">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="bd337-129">core: configurazione del cloud: usa l'endpoint "gestione risorse" se l'endpoint "gestione" non è impostato</span><span class="sxs-lookup"><span data-stu-id="bd337-129">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="bd337-130">ACS</span><span class="sxs-lookup"><span data-stu-id="bd337-130">ACS</span></span>

* <span data-ttu-id="bd337-131">consente di correggere il conteggio di master e agenti affinché sia un numero intero anziché una stringa</span><span class="sxs-lookup"><span data-stu-id="bd337-131">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="bd337-132">espone "az acs create --no-wait" e "az acs wait" alla creazione asincrona</span><span class="sxs-lookup"><span data-stu-id="bd337-132">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="bd337-133">espone "az acs create --validate" alle convalide del test controllato</span><span class="sxs-lookup"><span data-stu-id="bd337-133">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="bd337-134">rimuove il profilo di Windows prima di INSERIRE la chiamata del comando scale ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="bd337-134">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="bd337-135">AppService</span><span class="sxs-lookup"><span data-stu-id="bd337-135">AppService</span></span>

* <span data-ttu-id="bd337-136">functionapp: aggiunge supporti functionapp completi, tra cui create, show, list, delete, hostname, ssl e così via</span><span class="sxs-lookup"><span data-stu-id="bd337-136">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="bd337-137">Aggiunta di servizi di Team (vsts) come opzione di consegna continua a "appservice web source-control config"</span><span class="sxs-lookup"><span data-stu-id="bd337-137">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="bd337-138">Consente di creare "az webapp" per sostituire "az appservice web". Per la compatibilità con le versioni precedenti, "az appservice web" viene mantenuta per 2 versioni</span><span class="sxs-lookup"><span data-stu-id="bd337-138">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="bd337-139">Espone gli argomenti per configurare la distribuzione e "stack di runtime" su webapp</span><span class="sxs-lookup"><span data-stu-id="bd337-139">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="bd337-140">Espone "webapp list-runtimes"</span><span class="sxs-lookup"><span data-stu-id="bd337-140">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="bd337-141">supporta le stringhe di connessione per la configurazione ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="bd337-141">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="bd337-142">supporta lo scambio di slot con anteprima</span><span class="sxs-lookup"><span data-stu-id="bd337-142">support slot swap with preview</span></span>
* <span data-ttu-id="bd337-143">Errori di polacco neii comandi appservice ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="bd337-143">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="bd337-144">Usa il gruppo di risorse del piano del servizio app per le operazioni cert ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="bd337-144">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="bd337-145">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="bd337-145">CosmosDB</span></span>

* <span data-ttu-id="bd337-146">Rinomina il modulo documentdb in cosmosdb.</span><span class="sxs-lookup"><span data-stu-id="bd337-146">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="bd337-147">Aggiunto il supporto per le API del piano di dati documentdb: gestione di database e raccolta</span><span class="sxs-lookup"><span data-stu-id="bd337-147">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="bd337-148">Aggiunto il supporto per abilitare il failover automatico negli account del database</span><span class="sxs-lookup"><span data-stu-id="bd337-148">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="bd337-149">Aggiunto il supporto per nuovi criteri di coerenza ConsistentPrefix</span><span class="sxs-lookup"><span data-stu-id="bd337-149">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="bd337-150">Analisi Data Lake</span><span class="sxs-lookup"><span data-stu-id="bd337-150">Data Lake Analytics</span></span>

* <span data-ttu-id="bd337-151">Consente di correggere un bug in cui il filtro dei risultati e lo stato degli elenchi del processo genererebbe un errore.</span><span class="sxs-lookup"><span data-stu-id="bd337-151">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="bd337-152">Aggiunge il supporto per il tipo di elementi del nuovo catalogo: pacchetto.</span><span class="sxs-lookup"><span data-stu-id="bd337-152">Add support for new catalog item type: package.</span></span> <span data-ttu-id="bd337-153">accessibili tramite: `az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="bd337-153">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="bd337-154">È possibile elencare gli elementi seguenti del catalogo da un database, senza necessità delle specifiche dello schema:</span><span class="sxs-lookup"><span data-stu-id="bd337-154">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="bd337-155">Tabella</span><span class="sxs-lookup"><span data-stu-id="bd337-155">Table</span></span>
  * <span data-ttu-id="bd337-156">Funzione con valori di tabella</span><span class="sxs-lookup"><span data-stu-id="bd337-156">Table valued function</span></span>
  * <span data-ttu-id="bd337-157">Visualizza</span><span class="sxs-lookup"><span data-stu-id="bd337-157">View</span></span>
  * <span data-ttu-id="bd337-158">Statistiche tabelle.</span><span class="sxs-lookup"><span data-stu-id="bd337-158">Table Statistics.</span></span> <span data-ttu-id="bd337-159">Questo elemento può essere elencato anche con uno schema, ma senza specificare un nome di tabella.</span><span class="sxs-lookup"><span data-stu-id="bd337-159">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="bd337-160">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="bd337-160">Data Lake Store</span></span>

* <span data-ttu-id="bd337-161">Aggiorna la versione dell'SDK del file system sottostante, che offre un supporto migliore per la gestione di scenari con limitazione lato server.</span><span class="sxs-lookup"><span data-stu-id="bd337-161">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="bd337-162">Migliora le prestazioni di carico del pacchetto e l'esecuzione del comando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="bd337-162">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="bd337-163">guida mancate per la presentazione di accesso.</span><span class="sxs-lookup"><span data-stu-id="bd337-163">missed help for access show.</span></span> <span data-ttu-id="bd337-164">aggiunta.</span><span class="sxs-lookup"><span data-stu-id="bd337-164">adding it.</span></span> <span data-ttu-id="bd337-165">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="bd337-165">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="bd337-166">Find</span><span class="sxs-lookup"><span data-stu-id="bd337-166">Find</span></span>

* <span data-ttu-id="bd337-167">migliora i risultati di ricerca e consente di controllare le versioni dell'indice di ricerca</span><span class="sxs-lookup"><span data-stu-id="bd337-167">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="bd337-168">Insieme di credenziali delle chiavi</span><span class="sxs-lookup"><span data-stu-id="bd337-168">KeyVault</span></span>

* <span data-ttu-id="bd337-169">BC: `az keyvault certificate download` modifica -e dalla stringa o dal binario in PEM o DER per rappresentare meglio le opzioni</span><span class="sxs-lookup"><span data-stu-id="bd337-169">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="bd337-170">BC: rimuove --expires e --not-before da `keyvault certificate create` poiché questi parametri non sono supportati dal servizio.</span><span class="sxs-lookup"><span data-stu-id="bd337-170">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="bd337-171">Aggiunge il parametro --validity a `keyvault certificate create` per eseguire l'override in modo selettivo del valore in --policy</span><span class="sxs-lookup"><span data-stu-id="bd337-171">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="bd337-172">Consente di risolvere i problemi in `keyvault certificate get-default-policy` laddove sono stati esposti "expires" e "not_before", ma non "validity_in_months".</span><span class="sxs-lookup"><span data-stu-id="bd337-172">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="bd337-173">correzione di keyvault per l'importazione di pem e pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="bd337-173">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="bd337-174">Lab</span><span class="sxs-lookup"><span data-stu-id="bd337-174">Lab</span></span>

* <span data-ttu-id="bd337-175">Aggiunta dei comandi create, show, delete e list per l'ambiente nel laboratorio.</span><span class="sxs-lookup"><span data-stu-id="bd337-175">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="bd337-176">Aggiunta di comandi show e list per visualizzare i modelli ARM nel laboratorio.</span><span class="sxs-lookup"><span data-stu-id="bd337-176">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="bd337-177">Aggiunta del flag --environment in `az lab vm list` per filtrare le macchine virtuali in base all'ambiente nel laboratorio.</span><span class="sxs-lookup"><span data-stu-id="bd337-177">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="bd337-178">Aggiunge il comando di convenienza `az lab formula export-artifacts` per esportare lo scaffolding dell'elemento all'interno della formula di Lab.</span><span class="sxs-lookup"><span data-stu-id="bd337-178">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="bd337-179">Aggiunge i comandi per gestire i segreti in Lab.</span><span class="sxs-lookup"><span data-stu-id="bd337-179">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="bd337-180">Monitorare</span><span class="sxs-lookup"><span data-stu-id="bd337-180">Monitor</span></span>

* <span data-ttu-id="bd337-181">Correzione di bug: modellazione di `--actions` in `az alert-rules create` per usare una stringa JSON ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="bd337-181">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="bd337-182">Correzione di bug: diagnostic settings create non accetta i registri/le metriche dei comandi show ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="bd337-182">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="bd337-183">Rete</span><span class="sxs-lookup"><span data-stu-id="bd337-183">Network</span></span>

* <span data-ttu-id="bd337-184">Aggiunge il comando `network watcher test-connectivity`.</span><span class="sxs-lookup"><span data-stu-id="bd337-184">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="bd337-185">Aggiunge il supporto per il parametro `--filters` per `network watcher packet-capture create`.</span><span class="sxs-lookup"><span data-stu-id="bd337-185">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="bd337-186">Aggiunge il supporto per lo svuotamento della connessione del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="bd337-186">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="bd337-187">Aggiunge il supporto per la configurazione dell'insieme di regole WAF del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="bd337-187">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="bd337-188">Aggiunge il supporto per le regole e i filtri di route ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bd337-188">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="bd337-189">Aggiunge il supporto per il routing geografico di TrafficManager.</span><span class="sxs-lookup"><span data-stu-id="bd337-189">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="bd337-190">Aggiunge il supporto per i selettori di traffico basati su criteri di connessione VPN.</span><span class="sxs-lookup"><span data-stu-id="bd337-190">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="bd337-191">Aggiunge il supporto per i criteri IPSec della connessione VPN.</span><span class="sxs-lookup"><span data-stu-id="bd337-191">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="bd337-192">Correzione di bug con `vpn-connection create` quando si usano i parametri `--no-wait` o `--validate`.</span><span class="sxs-lookup"><span data-stu-id="bd337-192">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="bd337-193">Aggiunge il supporto per i gateway di rete virtuale attivo/attivo</span><span class="sxs-lookup"><span data-stu-id="bd337-193">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="bd337-194">Rimuove i valori null i valori dall'output dei comandi `network vpn-connection list/show`.</span><span class="sxs-lookup"><span data-stu-id="bd337-194">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="bd337-195">BC: correzione di bug nell'output di `vpn-connection create`</span><span class="sxs-lookup"><span data-stu-id="bd337-195">BC: Fix bug in the output of `vpn-connection create`</span></span> 
* <span data-ttu-id="bd337-196">Corregge i bug in cui l'argomento "--key-length" di "vpn-connection create"' non è stato analizzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="bd337-196">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="bd337-197">Corregge i bug in `dns zone import` in cui i record non sono stati importati correttamente.</span><span class="sxs-lookup"><span data-stu-id="bd337-197">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="bd337-198">Corregge i bug laddove `traffic-manager endpoint update` non funzionava.</span><span class="sxs-lookup"><span data-stu-id="bd337-198">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="bd337-199">Aggiunge i comandi di anteprima "network watcher".</span><span class="sxs-lookup"><span data-stu-id="bd337-199">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="bd337-200">Profilo</span><span class="sxs-lookup"><span data-stu-id="bd337-200">Profile</span></span>

* <span data-ttu-id="bd337-201">Supporta l'accesso quando non sono state trovate sottoscrizioni ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="bd337-201">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="bd337-202">Supporta l'abbreviazione del nome dei parametri in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="bd337-202">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="bd337-203">Redis</span><span class="sxs-lookup"><span data-stu-id="bd337-203">Redis</span></span>

* <span data-ttu-id="bd337-204">Aggiunta del comando update che offre anche la possibilità di passare alla cache Redis</span><span class="sxs-lookup"><span data-stu-id="bd337-204">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="bd337-205">Il comando "update-settings" viene deprecato.</span><span class="sxs-lookup"><span data-stu-id="bd337-205">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="bd337-206">Risorsa</span><span class="sxs-lookup"><span data-stu-id="bd337-206">Resource</span></span>

* <span data-ttu-id="bd337-207">Aggiunge i comandi managedapp e managedapp definition ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="bd337-207">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="bd337-208">Supporta i comandi "provider operation" ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="bd337-208">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="bd337-209">Supporta la creazione della risorsa generica ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="bd337-209">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="bd337-210">Corregge l'analisi della risorsa e la ricerca della versione API.</span><span class="sxs-lookup"><span data-stu-id="bd337-210">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="bd337-211">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="bd337-211">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="bd337-212">Aggiunge docs ad az lock update.</span><span class="sxs-lookup"><span data-stu-id="bd337-212">Add docs for az lock update.</span></span> <span data-ttu-id="bd337-213">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="bd337-213">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="bd337-214">Genera un errore se si tenta di elencare le risorse per un gruppo che non esiste.</span><span class="sxs-lookup"><span data-stu-id="bd337-214">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="bd337-215">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="bd337-215">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="bd337-216">[Compute] Risolve i problemi con l'aggiornamento dei set di disponibilità VMSS e della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bd337-216">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="bd337-217">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="bd337-217">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="bd337-218">Correzione della creazione e dell'eliminazione del blocco se parent-resource-path è Nessuno ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="bd337-218">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="bd337-219">Ruolo</span><span class="sxs-lookup"><span data-stu-id="bd337-219">Role</span></span>

* <span data-ttu-id="bd337-220">create-for-rbac: assicura che la data di fine di SP non superi la data di scadenza del certificato ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="bd337-220">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="bd337-221">RBAC: aggiunge il supporto completo ad "ad group" ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="bd337-221">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="bd337-222">role: corregge i problemi in role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="bd337-222">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="bd337-223">create-for-rbac: garantisce che venga presa la password indicata</span><span class="sxs-lookup"><span data-stu-id="bd337-223">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="bd337-224">SQL</span><span class="sxs-lookup"><span data-stu-id="bd337-224">SQL</span></span>

* <span data-ttu-id="bd337-225">Aggiunti i comandi az sql server list-usages e az sql db list-usages.</span><span class="sxs-lookup"><span data-stu-id="bd337-225">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="bd337-226">SQL: possibilità di connettersi direttamente al provider di risorse ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="bd337-226">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="bd337-227">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="bd337-227">Storage</span></span>

* <span data-ttu-id="bd337-228">Percorso predefinito al percorso del gruppo di risorse per `storage account create`.</span><span class="sxs-lookup"><span data-stu-id="bd337-228">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="bd337-229">Aggiunge il supporto per la copia di BLOB incrementale</span><span class="sxs-lookup"><span data-stu-id="bd337-229">Add support for incremental blob copy</span></span>
* <span data-ttu-id="bd337-230">Aggiunge il supporto per il upload di BLOB in blocchi di grandi dimensioni</span><span class="sxs-lookup"><span data-stu-id="bd337-230">Add support for large block blob upload</span></span>
* <span data-ttu-id="bd337-231">Modifica le dimensioni del blocco in 100 MB quando il file da caricare supera i 200 GB</span><span class="sxs-lookup"><span data-stu-id="bd337-231">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="bd337-232">VM</span><span class="sxs-lookup"><span data-stu-id="bd337-232">VM</span></span>

* <span data-ttu-id="bd337-233">avail-set: rende facoltativo il conteggio del dominio UD&FD</span><span class="sxs-lookup"><span data-stu-id="bd337-233">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="bd337-234">note: comandi della VM nei cloud sovrani. Evitare le funzionalità correlate al disco gestito, tra cui:</span><span class="sxs-lookup"><span data-stu-id="bd337-234">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="bd337-235">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="bd337-235">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="bd337-236">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="bd337-236">az vm/vmss disk</span></span>
  3. <span data-ttu-id="bd337-237">All'interno di "az vm/vmss create" usare "—use-unmanaged-disk" per evitare che il disco gestito. Funziona anche con altri comandi</span><span class="sxs-lookup"><span data-stu-id="bd337-237">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="bd337-238">vm/vmss: migliora il testo di avviso quando si generano coppie di chiavi SSH</span><span class="sxs-lookup"><span data-stu-id="bd337-238">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="bd337-239">vm/vmss: supporta la creazione da un'immagine del marketplace che richiede informazioni sul piano ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="bd337-239">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="bd337-240">3 aprile 2017</span><span class="sxs-lookup"><span data-stu-id="bd337-240">April 3, 2017</span></span>

<span data-ttu-id="bd337-241">Versione 2.0.2</span><span class="sxs-lookup"><span data-stu-id="bd337-241">Version 2.0.2</span></span>

<span data-ttu-id="bd337-242">In questa versione sono stati rilasciati i componenti ACR, Batch, KeyVault e SQL.</span><span class="sxs-lookup"><span data-stu-id="bd337-242">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="bd337-243">Core</span><span class="sxs-lookup"><span data-stu-id="bd337-243">Core</span></span>

* <span data-ttu-id="bd337-244">Aggiunta dei moduli acr, lab, monitor e find all'elenco predefinito.</span><span class="sxs-lookup"><span data-stu-id="bd337-244">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="bd337-245">Login: esclusione del tenant errato ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="bd337-245">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="bd337-246">login: impostazione della sottoscrizione predefinita su una con lo stato "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="bd337-246">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="bd337-247">Aggiunta di comandi wait e di supporto per --no-wait a più comandi ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="bd337-247">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="bd337-248">core: supporto per accesso mediante entità servizio con un certificato ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="bd337-248">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="bd337-249">Aggiunta della richiesta dei parametri di modello mancanti.</span><span class="sxs-lookup"><span data-stu-id="bd337-249">Add prompting for missing template parameters.</span></span> <span data-ttu-id="bd337-250">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="bd337-250">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="bd337-251">Supporto per l'impostazione di valori predefiniti per argomenti comuni ad esempio gruppo di risorse predefinito, Web predefinito, macchina virtuale predefinita</span><span class="sxs-lookup"><span data-stu-id="bd337-251">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="bd337-252">Supporto per l'accesso al tenant specifico</span><span class="sxs-lookup"><span data-stu-id="bd337-252">Support login to specific tenant</span></span>
 
### <a name="acs"></a><span data-ttu-id="bd337-253">ACS</span><span class="sxs-lookup"><span data-stu-id="bd337-253">ACS</span></span>

* [<span data-ttu-id="bd337-254">ACS] Aggiunta di supporto per la configurazione di un cluster ACS predefinito ([#2554</span><span class="sxs-lookup"><span data-stu-id="bd337-254">ACS] Adding support for configuring a default ACS cluster ([#2554</span></span>](https://github.com/Azure/azure-cli/pull/2554))
* <span data-ttu-id="bd337-255">Aggiunta di supporto per la richiesta di password della chiave SSH.</span><span class="sxs-lookup"><span data-stu-id="bd337-255">Add support for ssh key password prompting.</span></span> <span data-ttu-id="bd337-256">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="bd337-256">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="bd337-257">Aggiunta di supporto per i cluster Windows.</span><span class="sxs-lookup"><span data-stu-id="bd337-257">Add support for windows clusters.</span></span> <span data-ttu-id="bd337-258">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="bd337-258">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="bd337-259">Passaggio dal ruolo Proprietario al ruolo Collaboratore.</span><span class="sxs-lookup"><span data-stu-id="bd337-259">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="bd337-260">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="bd337-260">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>
 
### <a name="appservice"></a><span data-ttu-id="bd337-261">AppService</span><span class="sxs-lookup"><span data-stu-id="bd337-261">AppService</span></span>

* <span data-ttu-id="bd337-262">appservice: supporto per ottenere l'indirizzo IP esterno usato per i record DNS A ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="bd337-262">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="bd337-263">appservice: supporto dell'associazione di certificati jolly ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="bd337-263">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="bd337-264">appservice: supporto dell'elenco di profili di pubblicazione ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="bd337-264">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="bd337-265">AppService - attivazione della sincronizzazione del controllo dopo la configurazione ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="bd337-265">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>
 
### <a name="datalake"></a><span data-ttu-id="bd337-266">DataLake</span><span class="sxs-lookup"><span data-stu-id="bd337-266">DataLake</span></span>

* <span data-ttu-id="bd337-267">Versione iniziale del modulo Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bd337-267">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="bd337-268">Versione iniziale del modulo Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bd337-268">Initial release of Data Lake Store module.</span></span>
 
### <a name="docuemntdb"></a><span data-ttu-id="bd337-269">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="bd337-269">DocuemntDB</span></span>

* <span data-ttu-id="bd337-270">DocumentDB: aggiunta di supporto per l'elenco di stringhe di connessione ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="bd337-270">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="bd337-271">VM</span><span class="sxs-lookup"><span data-stu-id="bd337-271">VM</span></span>

* [<span data-ttu-id="bd337-272">Compute] Aggiunta di supporto per AppGateway alla creazione di set di scalabilità di macchine virtuali ([#2570</span><span class="sxs-lookup"><span data-stu-id="bd337-272">Compute] Add AppGateway support to virtual machine scale set create ([#2570</span></span>](https://github.com/Azure/azure-cli/pull/2570))
* [<span data-ttu-id="bd337-273">VM/VMSS] Miglioramento del supporto per memorizzazione nella cache del disco ([#2522</span><span class="sxs-lookup"><span data-stu-id="bd337-273">VM/VMSS] Improved disk caching support ([#2522</span></span>](https://github.com/Azure/azure-cli/pull/2522))
* <span data-ttu-id="bd337-274">VM/VMSS: inclusione di logica di convalida credenziali usata dal portale ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="bd337-274">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="bd337-275">Aggiunta di comandi wait e di supporto per --no-wait ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="bd337-275">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="bd337-276">Virtual machine scale set: supporto * per elencare le visualizzazioni di istanza tra le macchine virtuali ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="bd337-276">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="bd337-277">Aggiunta di --secrets per la macchina virtuale e il set di scalabilità di macchine virtuali ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="bd337-277">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="bd337-278">Consentita la creazione di macchine virtuali con disco rigido virtuale specializzato ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="bd337-278">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="bd337-279">27 febbraio 2017</span><span class="sxs-lookup"><span data-stu-id="bd337-279">February 27, 2017</span></span>

<span data-ttu-id="bd337-280">Versione 2.0.0</span><span class="sxs-lookup"><span data-stu-id="bd337-280">Version 2.0.0</span></span>

<span data-ttu-id="bd337-281">Questa versione dell'interfaccia della riga di comando di Azure 2.0 è la prima versione disponibile a livello generale.</span><span class="sxs-lookup"><span data-stu-id="bd337-281">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="bd337-282">La disponibilità generale si applica ai moduli comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="bd337-282">General availability applies to these command modules:</span></span>
- <span data-ttu-id="bd337-283">Servizio contenitore (acs)</span><span class="sxs-lookup"><span data-stu-id="bd337-283">Container Service (acs)</span></span>
- <span data-ttu-id="bd337-284">Compute (inclusi Resource Manager, macchina virtuale, set di scalabilità di macchine virtuali, Managed Disks)</span><span class="sxs-lookup"><span data-stu-id="bd337-284">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="bd337-285">Rete</span><span class="sxs-lookup"><span data-stu-id="bd337-285">Networking</span></span>
- <span data-ttu-id="bd337-286">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="bd337-286">Storage</span></span>

<span data-ttu-id="bd337-287">Questi moduli comandi possono essere usati nella produzione e sono supportati dal contratto di servizio Microsoft standard.</span><span class="sxs-lookup"><span data-stu-id="bd337-287">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="bd337-288">È possibile segnalare i problemi direttamente al supporto tecnico Microsoft o tramite l'[elenco di problemi github](https://github.com/azure/azure-cli/issues/).</span><span class="sxs-lookup"><span data-stu-id="bd337-288">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="bd337-289">È possibile porre domande su [StackOverflow usando il tag azure-cli](http://stackoverflow.com/questions/tagged/azure-cli) o contattare il team del prodotto all'indirizzo [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="bd337-289">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
<span data-ttu-id="bd337-290">È possibile fornire commenti e suggerimenti dalla riga di comando con il comando `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="bd337-290">You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="bd337-291">I comandi in questi moduli sono stabili e non si prevede che la sintassi cambi nei prossimi rilasci di questa versione dell'interfaccia della riga di comando di Azure.</span><span class="sxs-lookup"><span data-stu-id="bd337-291">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="bd337-292">Per verificare la versione dell'interfaccia della riga di comando, usare `az --version`.</span><span class="sxs-lookup"><span data-stu-id="bd337-292">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="bd337-293">L'output elenca la versione dell'interfaccia della riga di comando stessa (2.0.0 in questo rilascio), i singoli moduli comandi e le versioni di Python e GCC in uso.</span><span class="sxs-lookup"><span data-stu-id="bd337-293">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="bd337-294">Alcuni dei moduli del comando presentano un suffisso "b*n*" o "rc*n*".</span><span class="sxs-lookup"><span data-stu-id="bd337-294">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="bd337-295">Questi moduli comandi sono ancora in fase di anteprima e saranno disponibili a livello generale in futuro.</span><span class="sxs-lookup"><span data-stu-id="bd337-295">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="bd337-296">Sono anche disponibili build di anteprima notturne dell'interfaccia della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="bd337-296">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="bd337-297">Per informazioni, vedere le istruzioni su come [ottenere le build notturne](https://github.com/Azure/azure-cli#nightly-builds) e le istruzioni sull'[impostazione per gli sviluppatori e sul codice per i collaboratori](https://github.com/Azure/azure-cli#developer-setup).</span><span class="sxs-lookup"><span data-stu-id="bd337-297">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="bd337-298">È possibile segnalare problemi relative alle build di anteprima notturne nei seguenti modi:</span><span class="sxs-lookup"><span data-stu-id="bd337-298">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="bd337-299">Segnalare i problemi tramite l'[elenco di problemi github](https://github.com/azure/azure-cli/issues/)</span><span class="sxs-lookup"><span data-stu-id="bd337-299">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="bd337-300">Contattare il tema del prodotto all'indirizzo [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="bd337-300">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="bd337-301">Fornire commenti e suggerimenti dalla riga di comando con il comando `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="bd337-301">Provide feedback from the command line with the `az feedback` command.</span></span>

