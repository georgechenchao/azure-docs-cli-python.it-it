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
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="6a47d-104">Note sulla versione dell'interfaccia della riga di comando di Azure 2.0</span><span class="sxs-lookup"><span data-stu-id="6a47d-104">Azure CLI 2.0 release notes</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="6a47d-105">28 agosto 2017</span><span class="sxs-lookup"><span data-stu-id="6a47d-105">August 28, 2017</span></span>

<span data-ttu-id="6a47d-106">Versione 2.0.15</span><span class="sxs-lookup"><span data-stu-id="6a47d-106">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="6a47d-107">CLI</span><span class="sxs-lookup"><span data-stu-id="6a47d-107">CLI</span></span>

* <span data-ttu-id="6a47d-108">Aggiunta di una nota legale a `--version`.</span><span class="sxs-lookup"><span data-stu-id="6a47d-108">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="6a47d-109">ACS</span><span class="sxs-lookup"><span data-stu-id="6a47d-109">ACS</span></span>

* <span data-ttu-id="6a47d-110">Correzione delle aree di anteprima.</span><span class="sxs-lookup"><span data-stu-id="6a47d-110">Corrected preview regions.</span></span>
* <span data-ttu-id="6a47d-111">Formattazione corretta del valore `dns_name_prefix` predefinito.</span><span class="sxs-lookup"><span data-stu-id="6a47d-111">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="6a47d-112">Ottimizzazione dell'output del comando di ACS.</span><span class="sxs-lookup"><span data-stu-id="6a47d-112">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="6a47d-113">Servizio app</span><span class="sxs-lookup"><span data-stu-id="6a47d-113">Appservice</span></span>

* <span data-ttu-id="6a47d-114">[MODIFICA DI RILIEVO] Correzione di incoerenze nell'output di `az webapp config appsettings [delete|set]`</span><span class="sxs-lookup"><span data-stu-id="6a47d-114">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="6a47d-115">Aggiunta di un nuovo alias di `-i` per `az webapp config container set --docker-custom-image-name`</span><span class="sxs-lookup"><span data-stu-id="6a47d-115">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="6a47d-116">Esposizione di `az webapp log show`</span><span class="sxs-lookup"><span data-stu-id="6a47d-116">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="6a47d-117">Esposizione di nuovi argomenti da `az webapp delete` per mantenere il piano di servizio app, le metriche o la registrazione DNS</span><span class="sxs-lookup"><span data-stu-id="6a47d-117">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="6a47d-118">Correzione: Rilevamento corretto delle impostazioni dello slot</span><span class="sxs-lookup"><span data-stu-id="6a47d-118">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="6a47d-119">IoT</span><span class="sxs-lookup"><span data-stu-id="6a47d-119">IoT</span></span>

* <span data-ttu-id="6a47d-120">Correzione #3934: La creazione di criteri non cancella più i criteri esistenti</span><span class="sxs-lookup"><span data-stu-id="6a47d-120">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="6a47d-121">Rete</span><span class="sxs-lookup"><span data-stu-id="6a47d-121">Network</span></span>

* <span data-ttu-id="6a47d-122">[MODIFICA DI RILIEVO] Ridenominazione di `vnet list-private-access-services` in `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="6a47d-122">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="6a47d-123">[MODIFICA DI RILIEVO] Ridenominazione dell'opzione `--private-access-services` in `--service-endpoints` per `vnet subnet [create|update]`</span><span class="sxs-lookup"><span data-stu-id="6a47d-123">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="6a47d-124">Aggiunta del supporto per più indirizzi IP e intervalli di porte in `nsg rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="6a47d-124">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="6a47d-125">Aggiunta del supporto per SKU a `lb create`</span><span class="sxs-lookup"><span data-stu-id="6a47d-125">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="6a47d-126">Aggiunta del supporto per SKU a `public-ip create`</span><span class="sxs-lookup"><span data-stu-id="6a47d-126">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="6a47d-127">Profilo</span><span class="sxs-lookup"><span data-stu-id="6a47d-127">Profile</span></span>

* <span data-ttu-id="6a47d-128">Esposizione di `--msi` e `--msi-port` per l'accesso tramite l'identità della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="6a47d-128">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="6a47d-129">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="6a47d-129">Service Fabric</span></span>

* <span data-ttu-id="6a47d-130">Versione di anteprima</span><span class="sxs-lookup"><span data-stu-id="6a47d-130">Preview release</span></span>
* <span data-ttu-id="6a47d-131">Semplificazione delle regole relative a utente/password del Registro di sistema per il comando</span><span class="sxs-lookup"><span data-stu-id="6a47d-131">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="6a47d-132">Correzione del problema relativo alla richiesta della password per l'utente anche dopo il passaggio del parametro</span><span class="sxs-lookup"><span data-stu-id="6a47d-132">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="6a47d-133">Aggiunta del supporto per il valore `registry_cred` vuoto</span><span class="sxs-lookup"><span data-stu-id="6a47d-133">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="6a47d-134">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="6a47d-134">Storage</span></span>

* <span data-ttu-id="6a47d-135">Abilitazione della configurazione del livello BLOB</span><span class="sxs-lookup"><span data-stu-id="6a47d-135">Enabled setting blob tier</span></span>
* <span data-ttu-id="6a47d-136">Aggiunta degli argomenti `--bypass` e `--default-action` a `storage account [create|update]` per supportare il tunneling del servizio</span><span class="sxs-lookup"><span data-stu-id="6a47d-136">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="6a47d-137">Aggiunta di comandi per aggiungere regole della rete virtuale e regole basate su indirizzi IP a `storage account network-rule`</span><span class="sxs-lookup"><span data-stu-id="6a47d-137">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>  
* <span data-ttu-id="6a47d-138">Abilitazione della crittografia del servizio tramite chiave gestita dal cliente</span><span class="sxs-lookup"><span data-stu-id="6a47d-138">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="6a47d-139">[MODIFICA DI RILIEVO] Ridenominazione dell'opzione `--encryption` in `--encryption-services` per il comando `az storage account create and az storage account update`</span><span class="sxs-lookup"><span data-stu-id="6a47d-139">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="6a47d-140">Correzione #4220: `az storage account update encryption`: Mancata corrispondenza della sintassi</span><span class="sxs-lookup"><span data-stu-id="6a47d-140">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="6a47d-141">VM</span><span class="sxs-lookup"><span data-stu-id="6a47d-141">VM</span></span>

* <span data-ttu-id="6a47d-142">Risoluzione del problema relativo alla visualizzazione di informazioni aggiuntive errate per `vmss get-instance-view` quando si usa `--instance-id *`</span><span class="sxs-lookup"><span data-stu-id="6a47d-142">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="6a47d-143">Aggiunta del supporto per `--lb-sku` a `vmss create`:</span><span class="sxs-lookup"><span data-stu-id="6a47d-143">Added support for `--lb-sku` to `vmss create`:</span></span> 
* <span data-ttu-id="6a47d-144">Rimozione dei nomi di persone dall'elenco di nomi non consentiti dell'amministratore per `[vm|vmss] create`</span><span class="sxs-lookup"><span data-stu-id="6a47d-144">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span> 
* <span data-ttu-id="6a47d-145">Risoluzione del problema relativo alla generazione di un errore da parte di `[vm|vmss] create` in caso di impossibilità di estrazione delle informazioni del piano da un'immagine</span><span class="sxs-lookup"><span data-stu-id="6a47d-145">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="6a47d-146">Risoluzione del problema relativo all'arresto anomalo in caso di creazione di un set di scalabilità vmms con un servizio di bilanciamento del carico interno</span><span class="sxs-lookup"><span data-stu-id="6a47d-146">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="6a47d-147">Risoluzione del problema relativo al mancato funzionamento dell'argomento `--no-wait` con `vm availability-set create`</span><span class="sxs-lookup"><span data-stu-id="6a47d-147">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="6a47d-148">15 agosto 2017</span><span class="sxs-lookup"><span data-stu-id="6a47d-148">August 15, 2017</span></span>

<span data-ttu-id="6a47d-149">Versione 2.0.14</span><span class="sxs-lookup"><span data-stu-id="6a47d-149">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="6a47d-150">ACS</span><span class="sxs-lookup"><span data-stu-id="6a47d-150">ACS</span></span>

* <span data-ttu-id="6a47d-151">Correzione del numero di porta sshMaster0 per kubernetes</span><span class="sxs-lookup"><span data-stu-id="6a47d-151">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="6a47d-152">Servizio app</span><span class="sxs-lookup"><span data-stu-id="6a47d-152">Appservice</span></span>

* <span data-ttu-id="6a47d-153">Correzione dell'eccezione generata durante la creazione di una nuova app Web Linux basata su Git</span><span class="sxs-lookup"><span data-stu-id="6a47d-153">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="6a47d-154">Griglia di eventi</span><span class="sxs-lookup"><span data-stu-id="6a47d-154">Event Grid</span></span>

* <span data-ttu-id="6a47d-155">Aggiunta di dipendenze di SDK</span><span class="sxs-lookup"><span data-stu-id="6a47d-155">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="6a47d-156">11 agosto 2017</span><span class="sxs-lookup"><span data-stu-id="6a47d-156">August 11, 2017</span></span>

<span data-ttu-id="6a47d-157">Versione 2.0.13</span><span class="sxs-lookup"><span data-stu-id="6a47d-157">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="6a47d-158">ACS</span><span class="sxs-lookup"><span data-stu-id="6a47d-158">ACS</span></span>

* <span data-ttu-id="6a47d-159">Aggiunta di altre aree di anteprima</span><span class="sxs-lookup"><span data-stu-id="6a47d-159">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="6a47d-160">Batch</span><span class="sxs-lookup"><span data-stu-id="6a47d-160">Batch</span></span>

* <span data-ttu-id="6a47d-161">Aggiornamento a Batch SDK 3.1.0 e Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="6a47d-161">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="6a47d-162">Aggiunta di un nuovo comando per visualizzare il numero di attività di un processo</span><span class="sxs-lookup"><span data-stu-id="6a47d-162">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="6a47d-163">Correzione di un bug nell'elaborazione dell'URL della firma di accesso condiviso del file di risorse</span><span class="sxs-lookup"><span data-stu-id="6a47d-163">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="6a47d-164">L'endpoint dell'account Batch supporta ora il prefisso facoltativo 'https://'</span><span class="sxs-lookup"><span data-stu-id="6a47d-164">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="6a47d-165">Supporto per l'aggiunta di elenchi di più di 100 attività a un processo</span><span class="sxs-lookup"><span data-stu-id="6a47d-165">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="6a47d-166">Aggiunta della registrazione di debug per il caricamento del modulo di comandi delle estensioni</span><span class="sxs-lookup"><span data-stu-id="6a47d-166">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="6a47d-167">Componente</span><span class="sxs-lookup"><span data-stu-id="6a47d-167">Component</span></span>

* <span data-ttu-id="6a47d-168">Aggiunta dell'avviso relativo a elementi deprecati ai comandi 'az component'</span><span class="sxs-lookup"><span data-stu-id="6a47d-168">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="6a47d-169">Contenitore</span><span class="sxs-lookup"><span data-stu-id="6a47d-169">Container</span></span>

* <span data-ttu-id="6a47d-170">`create`: risoluzione del problema relativo all'impossibilità di usare il segno di uguale all'interno di una variabile di ambiente</span><span class="sxs-lookup"><span data-stu-id="6a47d-170">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="6a47d-171">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="6a47d-171">Data Lake Store</span></span>

* <span data-ttu-id="6a47d-172">Abilitazione del controllo dell'avanzamento</span><span class="sxs-lookup"><span data-stu-id="6a47d-172">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="6a47d-173">Griglia di eventi</span><span class="sxs-lookup"><span data-stu-id="6a47d-173">Event Grid</span></span>

* <span data-ttu-id="6a47d-174">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="6a47d-174">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="6a47d-175">Rete</span><span class="sxs-lookup"><span data-stu-id="6a47d-175">Network</span></span>

* <span data-ttu-id="6a47d-176">`lb`: correzione del problema relativo alla risoluzione non corretta di determinati nomi di risorse figlio in caso di omissione</span><span class="sxs-lookup"><span data-stu-id="6a47d-176">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="6a47d-177">`application-gateway {subresource} delete`: correzione del problema relativo al mancato rispetto di `--no-wait`</span><span class="sxs-lookup"><span data-stu-id="6a47d-177">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="6a47d-178">`application-gateway http-settings update`: risoluzione del problema relativo all'impossibilità di disattivare `--connection-draining-timeout`</span><span class="sxs-lookup"><span data-stu-id="6a47d-178">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="6a47d-179">Risoluzione del problema relativo all'argomento imprevisto `sa_data_size_kilobyes` della parola chiave con `az network vpn-connection ipsec-policy add`</span><span class="sxs-lookup"><span data-stu-id="6a47d-179">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="6a47d-180">Profilo</span><span class="sxs-lookup"><span data-stu-id="6a47d-180">Profile</span></span>

* <span data-ttu-id="6a47d-181">`account list`: aggiunta di `--refresh` per la sincronizzazione delle sottoscrizioni più recenti dal server</span><span class="sxs-lookup"><span data-stu-id="6a47d-181">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="6a47d-182">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="6a47d-182">Storage</span></span>

* <span data-ttu-id="6a47d-183">Abilitazione dell'aggiornamento dell'account di archiviazione con l'identità assegnata dal sistema</span><span class="sxs-lookup"><span data-stu-id="6a47d-183">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="6a47d-184">VM</span><span class="sxs-lookup"><span data-stu-id="6a47d-184">VM</span></span>

* <span data-ttu-id="6a47d-185">`availability-set`: esposizione del numero di domini di errore in fase di conversione</span><span class="sxs-lookup"><span data-stu-id="6a47d-185">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="6a47d-186">Esposizione del comando `list-skus`</span><span class="sxs-lookup"><span data-stu-id="6a47d-186">Exposed `list-skus` command</span></span>
* <span data-ttu-id="6a47d-187">Supporto per l'assegnazione di identità senza la creazione di assegnazioni di ruolo</span><span class="sxs-lookup"><span data-stu-id="6a47d-187">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="6a47d-188">Applicazione di SKU di archiviazione in fase di collegamento del dischi dati</span><span class="sxs-lookup"><span data-stu-id="6a47d-188">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="6a47d-189">Rimozione del nome del disco del sistema operativo predefinito e dello SKU di archiviazione in caso di uso di Managed Disks</span><span class="sxs-lookup"><span data-stu-id="6a47d-189">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="6a47d-190">28 luglio 2017</span><span class="sxs-lookup"><span data-stu-id="6a47d-190">July 28, 2017</span></span>

<span data-ttu-id="6a47d-191">Versione 2.0.12</span><span class="sxs-lookup"><span data-stu-id="6a47d-191">Version 2.0.12</span></span>

* <span data-ttu-id="6a47d-192">Aggiunta di comandi del contenitore</span><span class="sxs-lookup"><span data-stu-id="6a47d-192">Added container commands</span></span>
* <span data-ttu-id="6a47d-193">Aggiunta di moduli relativi a fatturazione e consumo</span><span class="sxs-lookup"><span data-stu-id="6a47d-193">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="6a47d-194">Core</span><span class="sxs-lookup"><span data-stu-id="6a47d-194">Core</span></span>

* <span data-ttu-id="6a47d-195">Restituzione di informazioni di autorizzazioni dell'SDK per entità servizio con certificati</span><span class="sxs-lookup"><span data-stu-id="6a47d-195">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="6a47d-196">Risoluzione del problema relativo alle eccezioni nell'avanzamento delle distribuzioni</span><span class="sxs-lookup"><span data-stu-id="6a47d-196">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="6a47d-197">Uso dell'endpoint ARM dal cloud corrente per la creazione del client di sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="6a47d-197">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="6a47d-198">Miglioramento della gestione simultanea del file clouds.config (#3636)</span><span class="sxs-lookup"><span data-stu-id="6a47d-198">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="6a47d-199">Aggiornamento dell'ID della richiesta client per ogni esecuzione del comando</span><span class="sxs-lookup"><span data-stu-id="6a47d-199">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="6a47d-200">Creazione dei client di sottoscrizione con il profilo SDK corretto (#3635)</span><span class="sxs-lookup"><span data-stu-id="6a47d-200">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="6a47d-201">Creazione di report relativi all'avanzamento per le distribuzioni dei modelli (#3510)</span><span class="sxs-lookup"><span data-stu-id="6a47d-201">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="6a47d-202">Aggiunta del supporto per la selezione di campi di output della tabella tramite una query jmespath (#3581)</span><span class="sxs-lookup"><span data-stu-id="6a47d-202">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="6a47d-203">Miglioramento della disattivazione dell'audio degli argomenti di analisi e dell'aggiunta di cronologia con gesti (#3434)</span><span class="sxs-lookup"><span data-stu-id="6a47d-203">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="6a47d-204">Creazione di client di sottoscrizione con il profilo SDK corretto</span><span class="sxs-lookup"><span data-stu-id="6a47d-204">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="6a47d-205">Spostamento di tutti i file di registrazione esistenti nella cartella più recente</span><span class="sxs-lookup"><span data-stu-id="6a47d-205">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="6a47d-206">Risoluzione del problema relativo all'idempotenza per la creazione di VM/VMSS (#3586)</span><span class="sxs-lookup"><span data-stu-id="6a47d-206">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="6a47d-207">I percorsi dei comandi non rispettano più la distinzione tra maiuscole/minuscole</span><span class="sxs-lookup"><span data-stu-id="6a47d-207">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="6a47d-208">Alcuni parametri di tipo booleano non rispettano più la distinzione tra maiuscole/minuscole</span><span class="sxs-lookup"><span data-stu-id="6a47d-208">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="6a47d-209">Supporto dell'accesso ad AD FS nel server locale come Azure Stack</span><span class="sxs-lookup"><span data-stu-id="6a47d-209">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="6a47d-210">Risoluzione del problema relativo alle operazioni di scrittura simultanee nel file clouds.config (#3255)</span><span class="sxs-lookup"><span data-stu-id="6a47d-210">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="6a47d-211">ACR</span><span class="sxs-lookup"><span data-stu-id="6a47d-211">ACR</span></span>

* <span data-ttu-id="6a47d-212">Aggiunta del comando `show-usage` per i registri gestiti</span><span class="sxs-lookup"><span data-stu-id="6a47d-212">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="6a47d-213">Supporto dell'aggiornamento dello SKU per i registri gestiti</span><span class="sxs-lookup"><span data-stu-id="6a47d-213">Support SKU update for managed registries</span></span>
* <span data-ttu-id="6a47d-214">Aggiunta dei registri gestiti con SKU gestito</span><span class="sxs-lookup"><span data-stu-id="6a47d-214">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="6a47d-215">Aggiunta di webhook per registri gestiti con modulo di comandi webhook ACR</span><span class="sxs-lookup"><span data-stu-id="6a47d-215">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="6a47d-216">Aggiunta dell'autenticazione AAD con il comando di accesso di ACR</span><span class="sxs-lookup"><span data-stu-id="6a47d-216">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="6a47d-217">Aggiunta del comando di eliminazione per repository Docker, manifesti e tag</span><span class="sxs-lookup"><span data-stu-id="6a47d-217">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="6a47d-218">ACS</span><span class="sxs-lookup"><span data-stu-id="6a47d-218">ACS</span></span>

* <span data-ttu-id="6a47d-219">Supporto per l'API versione 2017-07-01</span><span class="sxs-lookup"><span data-stu-id="6a47d-219">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="6a47d-220">Servizio app</span><span class="sxs-lookup"><span data-stu-id="6a47d-220">Appservice</span></span>

* <span data-ttu-id="6a47d-221">Risoluzione del bug relativo alla mancata restituzione di valori per l'elenco di app Web Linux</span><span class="sxs-lookup"><span data-stu-id="6a47d-221">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="6a47d-222">Supporto per il recupero di credenziali da ACR</span><span class="sxs-lookup"><span data-stu-id="6a47d-222">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="6a47d-223">Rimozione di tutti i comandi in `appservice web`</span><span class="sxs-lookup"><span data-stu-id="6a47d-223">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="6a47d-224">Mascheramento delle password del registro Docker dall'output del comando (#3656)</span><span class="sxs-lookup"><span data-stu-id="6a47d-224">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="6a47d-225">Conferma dell'uso del browser predefinito in macOS senza errori (#3623)</span><span class="sxs-lookup"><span data-stu-id="6a47d-225">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="6a47d-226">Miglioramento della Guida di `webapp log tail` e `webapp log download` (#3624)</span><span class="sxs-lookup"><span data-stu-id="6a47d-226">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="6a47d-227">Esposizione del comando `traffic-routing` per la configurazione del routing statico (#3566)</span><span class="sxs-lookup"><span data-stu-id="6a47d-227">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="6a47d-228">Aggiunta di correzioni relative all'affidabilità nella configurazione del controllo del codice sorgente (#3245)</span><span class="sxs-lookup"><span data-stu-id="6a47d-228">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="6a47d-229">Rimozione dell'argomento `--node-version` non supportato da `webapp config update` per le app Web Windows.</span><span class="sxs-lookup"><span data-stu-id="6a47d-229">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="6a47d-230">Viene usato `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span><span class="sxs-lookup"><span data-stu-id="6a47d-230">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="6a47d-231">Batch</span><span class="sxs-lookup"><span data-stu-id="6a47d-231">Batch</span></span>

* <span data-ttu-id="6a47d-232">Aggiornamento a Batch SDK 3.0.0 con supporto per le macchine virtuali a priorità bassa nei pool</span><span class="sxs-lookup"><span data-stu-id="6a47d-232">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="6a47d-233">Ridenominazione per `pool create` dell'opzione `--target-dedicated` in `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="6a47d-233">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="6a47d-234">Aggiunta in `pool create` delle opzioni `--target-low-priority-nodes` e `--application-licenses`</span><span class="sxs-lookup"><span data-stu-id="6a47d-234">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="6a47d-235">RETE CDN</span><span class="sxs-lookup"><span data-stu-id="6a47d-235">CDN</span></span>

* <span data-ttu-id="6a47d-236">Miglioramento del messaggio di errore per `cdn endpoint list` nel caso in cui il profilo specificato da `--profile-name` non esista.</span><span class="sxs-lookup"><span data-stu-id="6a47d-236">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="6a47d-237">Cloud</span><span class="sxs-lookup"><span data-stu-id="6a47d-237">Cloud</span></span>

* <span data-ttu-id="6a47d-238">Modifica della versione dell'API dell'endpoint dei metadati del cloud nel formato AAAA-MM-GG</span><span class="sxs-lookup"><span data-stu-id="6a47d-238">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="6a47d-239">L'endpoint della raccolta non è obbligatorio</span><span class="sxs-lookup"><span data-stu-id="6a47d-239">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="6a47d-240">Supporto per la registrazione del cloud solo con l'endpoint di gestione delle risorse ARM</span><span class="sxs-lookup"><span data-stu-id="6a47d-240">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="6a47d-241">Aggiunta di un'opzione per `cloud set` per la scelta del profilo durante la selezione del cloud corrente</span><span class="sxs-lookup"><span data-stu-id="6a47d-241">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="6a47d-242">Esposizione di `endpoint_vm_image_alias_doc`</span><span class="sxs-lookup"><span data-stu-id="6a47d-242">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="6a47d-243">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="6a47d-243">CosmosDB</span></span>

* <span data-ttu-id="6a47d-244">Correzione dell'errore che consente la creazione di una raccolta con una chiave di partizione personalizzata</span><span class="sxs-lookup"><span data-stu-id="6a47d-244">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="6a47d-245">Aggiunta di supporto per la durata TTL predefinita della raccolta.</span><span class="sxs-lookup"><span data-stu-id="6a47d-245">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="6a47d-246">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="6a47d-246">Data Lake Analytics</span></span>

* <span data-ttu-id="6a47d-247">Aggiunta di comandi per la gestione dei criteri di calcolo sotto l'intestazione `dla account compute-policy`</span><span class="sxs-lookup"><span data-stu-id="6a47d-247">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="6a47d-248">Aggiunta di `dla job pipeline show`</span><span class="sxs-lookup"><span data-stu-id="6a47d-248">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="6a47d-249">Aggiunta di `dla job recurrence list`</span><span class="sxs-lookup"><span data-stu-id="6a47d-249">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="6a47d-250">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="6a47d-250">Data Lake Store</span></span>

* <span data-ttu-id="6a47d-251">Aggiunta di supporto per la rotazione delle chiavi dell'insieme di credenziali delle chiavi gestito dall'utente in `dls account update`</span><span class="sxs-lookup"><span data-stu-id="6a47d-251">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="6a47d-252">Aggiornamento della versione dell'SDK del file system del Data Lake Store sottostante per risolvere un problema di prestazioni</span><span class="sxs-lookup"><span data-stu-id="6a47d-252">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="6a47d-253">Aggiunta del comando `dls enable-key-vault`.</span><span class="sxs-lookup"><span data-stu-id="6a47d-253">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="6a47d-254">Questo comando prova ad abilitare un'istanza di Key Vault fornita dall'utente per l'uso per la crittografia dei dati in un account Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="6a47d-254">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="6a47d-255">Interattività</span><span class="sxs-lookup"><span data-stu-id="6a47d-255">Interactive</span></span>

* <span data-ttu-id="6a47d-256">Miglioramento del tempo di avvio tramite i comandi memorizzati nella cache</span><span class="sxs-lookup"><span data-stu-id="6a47d-256">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="6a47d-257">Miglioramento della copertura dei test</span><span class="sxs-lookup"><span data-stu-id="6a47d-257">Increased test coverage</span></span>
* <span data-ttu-id="6a47d-258">Miglioramento del gesto '?' per consentire anche l'inserimento nel comando successivo</span><span class="sxs-lookup"><span data-stu-id="6a47d-258">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="6a47d-259">Risoluzione degli errori relativi all'interattività con il profilo 2017-03-09-profile-preview (#3587)</span><span class="sxs-lookup"><span data-stu-id="6a47d-259">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="6a47d-260">Autorizzazione di `--version` come parametro per la modalità interattiva (#3645)</span><span class="sxs-lookup"><span data-stu-id="6a47d-260">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="6a47d-261">Interruzione della generazione di errori da parte della modalità interattiva relativi al completamento delle convalide (#3570)</span><span class="sxs-lookup"><span data-stu-id="6a47d-261">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="6a47d-262">Creazione di report relativi all'avanzamento per le distribuzioni dei modelli (#3510)</span><span class="sxs-lookup"><span data-stu-id="6a47d-262">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="6a47d-263">Aggiunta del flag `--progress`</span><span class="sxs-lookup"><span data-stu-id="6a47d-263">Added `--progress` flag</span></span>
* <span data-ttu-id="6a47d-264">Rimozione di `--debug` e `--verbose` dai completamenti</span><span class="sxs-lookup"><span data-stu-id="6a47d-264">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="6a47d-265">Rimozione di `interactive` dai completamenti (#3324)</span><span class="sxs-lookup"><span data-stu-id="6a47d-265">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="6a47d-266">IoT</span><span class="sxs-lookup"><span data-stu-id="6a47d-266">IoT</span></span>

* <span data-ttu-id="6a47d-267">Correzione del problema relativo alla creazione di criteri, che non cancella più i criteri esistenti.</span><span class="sxs-lookup"><span data-stu-id="6a47d-267">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="6a47d-268">(#3934)</span><span class="sxs-lookup"><span data-stu-id="6a47d-268">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="6a47d-269">Insieme di credenziali delle chiavi</span><span class="sxs-lookup"><span data-stu-id="6a47d-269">Key vault</span></span>

* <span data-ttu-id="6a47d-270">Aggiunta di comandi per le funzionalità di ripristino di Key Vault:</span><span class="sxs-lookup"><span data-stu-id="6a47d-270">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="6a47d-271">Sottocomandi di `keyvault`: `purge`, `recover`, `keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="6a47d-271">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="6a47d-272">Sottocomandi di `keyvault secret`: `backup`, `restore`, `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="6a47d-272">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="6a47d-273">Sottocomandi di `keyvault certificate`: `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="6a47d-273">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="6a47d-274">Sottocomandi di `keyvault key`: `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="6a47d-274">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="6a47d-275">Aggiunta dell'integrazione dell'insieme di credenziali delle chiavi dell'entità servizio (#3133)</span><span class="sxs-lookup"><span data-stu-id="6a47d-275">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="6a47d-276">Aggiornamento del piano dati dell'insieme di credenziali delle chiavi a 0.3.2.</span><span class="sxs-lookup"><span data-stu-id="6a47d-276">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="6a47d-277">(#3307)</span><span class="sxs-lookup"><span data-stu-id="6a47d-277">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="6a47d-278">Lab</span><span class="sxs-lookup"><span data-stu-id="6a47d-278">Lab</span></span>

* <span data-ttu-id="6a47d-279">Aggiunta del supporto per la rivendicazione di eventuali macchine virtuali nel laboratorio tramite `az lab vm claim`</span><span class="sxs-lookup"><span data-stu-id="6a47d-279">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="6a47d-280">Aggiunta del formattatore dell'output della tabella per `az lab vm list` e `az lab vm show`</span><span class="sxs-lookup"><span data-stu-id="6a47d-280">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="6a47d-281">Monitorare</span><span class="sxs-lookup"><span data-stu-id="6a47d-281">Monitor</span></span>

* <span data-ttu-id="6a47d-282">Correzione relativa al file del modello con il comando `monitor autoscale-settings get-parameters-template` (#3349)</span><span class="sxs-lookup"><span data-stu-id="6a47d-282">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="6a47d-283">Ridenominazione di `monitor alert-rule-incidents list` in `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="6a47d-283">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="6a47d-284">Ridenominazione di `monitor alert-rule-incidents show` in `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="6a47d-284">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="6a47d-285">Ridenominazione di `monitor metric-defintions list` in `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="6a47d-285">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="6a47d-286">Ridenominazione di `monitor alert-rules` in `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="6a47d-286">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="6a47d-287">Modifica di `monitor alert create`:</span><span class="sxs-lookup"><span data-stu-id="6a47d-287">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="6a47d-288">I sottocomandi `condition` e `action` non accettano più JSON</span><span class="sxs-lookup"><span data-stu-id="6a47d-288">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="6a47d-289">Aggiunta di numerosi parametri per la semplificazione del processo di creazione delle regole</span><span class="sxs-lookup"><span data-stu-id="6a47d-289">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="6a47d-290">`location` non è più obbligatorio</span><span class="sxs-lookup"><span data-stu-id="6a47d-290">`location` no longer required</span></span>
  * <span data-ttu-id="6a47d-291">Aggiunta del supporto di nome ID per la destinazione</span><span class="sxs-lookup"><span data-stu-id="6a47d-291">Add name and ID support for target</span></span>
  * <span data-ttu-id="6a47d-292">Rimozione di `--alert-rule-resource-name`</span><span class="sxs-lookup"><span data-stu-id="6a47d-292">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="6a47d-293">Ridenominazione di `is-enabled` in `enabled`, non più obbligatorio</span><span class="sxs-lookup"><span data-stu-id="6a47d-293">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="6a47d-294">I valori predefiniti di `description` sono ora basati sulla condizione specificata</span><span class="sxs-lookup"><span data-stu-id="6a47d-294">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="6a47d-295">Aggiunta di esempi per illustrare in modo più chiaro il nuovo formato</span><span class="sxs-lookup"><span data-stu-id="6a47d-295">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="6a47d-296">Supporto di nomi o ID per i comandi `monitor metric`</span><span class="sxs-lookup"><span data-stu-id="6a47d-296">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="6a47d-297">Aggiunta di argomenti ed esempi utili a `monitor alert rule update`</span><span class="sxs-lookup"><span data-stu-id="6a47d-297">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="6a47d-298">Rete</span><span class="sxs-lookup"><span data-stu-id="6a47d-298">Network</span></span>

* <span data-ttu-id="6a47d-299">Aggiunta del comando `list-private-access-services`</span><span class="sxs-lookup"><span data-stu-id="6a47d-299">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="6a47d-300">Aggiunta dell'argomento `--private-access-services` a `vnet subnet create` e `vnet subnet update`</span><span class="sxs-lookup"><span data-stu-id="6a47d-300">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="6a47d-301">Risoluzione del problema relativo all'esito negativo di `application-gateway redirect-config create`</span><span class="sxs-lookup"><span data-stu-id="6a47d-301">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="6a47d-302">Risoluzione del problema relativo al mancato funzionamento di `application-gateway redirect-config update` con `--no-wait`</span><span class="sxs-lookup"><span data-stu-id="6a47d-302">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="6a47d-303">Risoluzione del bug relativo all'uso dell'argomento `--servers` con `application-gateway address-pool create` e `application-gateway address-pool update`</span><span class="sxs-lookup"><span data-stu-id="6a47d-303">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="6a47d-304">Aggiunta dei comandi `application-gateway redirect-config`</span><span class="sxs-lookup"><span data-stu-id="6a47d-304">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="6a47d-305">Aggiunta di comandi ad `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span><span class="sxs-lookup"><span data-stu-id="6a47d-305">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="6a47d-306">Aggiunta di comandi ad `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="6a47d-306">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="6a47d-307">Aggiunta di argomenti ad `application-gateway http-settings create` e `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span><span class="sxs-lookup"><span data-stu-id="6a47d-307">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="6a47d-308">Aggiunta di argomenti ad `application-gateway url-path-map create` e `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="6a47d-308">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="6a47d-309">Aggiunta dell'argomento `--redirect-config` a `application-gateway url-path-map rule create`</span><span class="sxs-lookup"><span data-stu-id="6a47d-309">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="6a47d-310">Aggiunta del supporto per `--no-wait` a `application-gateway url-path-map rule delete`</span><span class="sxs-lookup"><span data-stu-id="6a47d-310">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="6a47d-311">Aggiunta di argomenti ad `application-gateway probe create` e `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="6a47d-311">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="6a47d-312">Aggiunta dell'argomento `--redirect-config` a `application-gateway rule create` e `application-gateway rule update`</span><span class="sxs-lookup"><span data-stu-id="6a47d-312">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="6a47d-313">Aggiunta del supporto per `--accelerated-networking` a `nic create` e `nic update`</span><span class="sxs-lookup"><span data-stu-id="6a47d-313">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="6a47d-314">Rimozione dell'argomento `--internal-dns-name-suffix` da `nic create`</span><span class="sxs-lookup"><span data-stu-id="6a47d-314">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="6a47d-315">Aggiunta del supporto per `--dns-servers` a `nic update` e `nic create`: aggiunta del supporto per --dns-servers</span><span class="sxs-lookup"><span data-stu-id="6a47d-315">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="6a47d-316">Risoluzione del bug relativo al fatto che `local-gateway create` ignora `--local-address-prefixes`</span><span class="sxs-lookup"><span data-stu-id="6a47d-316">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="6a47d-317">Aggiunta del supporto per `--dns-servers` a `vnet update`</span><span class="sxs-lookup"><span data-stu-id="6a47d-317">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="6a47d-318">Risoluzione del bug relativo alla creazione di un peering senza filtro delle route con `express-route peering create`</span><span class="sxs-lookup"><span data-stu-id="6a47d-318">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="6a47d-319">Risoluzione del bug relativo al mancato funzionamento di `--provider` e `--bandwidth` con `express-route update`</span><span class="sxs-lookup"><span data-stu-id="6a47d-319">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="6a47d-320">Risoluzione del bug relativo alla logica delle impostazioni predefinite di `network watcher show-topology`</span><span class="sxs-lookup"><span data-stu-id="6a47d-320">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="6a47d-321">Miglioramento della formattazione dell'output per `network list-usages`</span><span class="sxs-lookup"><span data-stu-id="6a47d-321">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="6a47d-322">Uso dell'indirizzo IP del front-end predefinito per `application-gateway http-listener create` se ne esiste solo uno</span><span class="sxs-lookup"><span data-stu-id="6a47d-322">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="6a47d-323">Uso del pool di indirizzi, delle impostazioni HTTP e del listener HTTP predefiniti per `application-gateway rule create` se ne esiste solo uno</span><span class="sxs-lookup"><span data-stu-id="6a47d-323">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="6a47d-324">Uso dell'indirizzo IP del front-end e del pool back-end predefiniti per `lb rule create` se ne esiste solo uno</span><span class="sxs-lookup"><span data-stu-id="6a47d-324">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="6a47d-325">Uso dell'indirizzo IP del front-end predefinito per `lb inbound-nat-rule create` se ne esiste solo uno</span><span class="sxs-lookup"><span data-stu-id="6a47d-325">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="6a47d-326">Profilo</span><span class="sxs-lookup"><span data-stu-id="6a47d-326">Profile</span></span>

* <span data-ttu-id="6a47d-327">Supporto dell'accesso all'interno di una VM con un'identità gestita</span><span class="sxs-lookup"><span data-stu-id="6a47d-327">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="6a47d-328">Supporto dell'output per `account show` nel formato di file di autorizzazione di SDK</span><span class="sxs-lookup"><span data-stu-id="6a47d-328">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="6a47d-329">Visualizzazione degli avvisi relativi a elementi deprecati quando si usa '--expanded-view'</span><span class="sxs-lookup"><span data-stu-id="6a47d-329">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="6a47d-330">Aggiunta del comando `get-access-token` per fornire il token AAD non elaborato</span><span class="sxs-lookup"><span data-stu-id="6a47d-330">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="6a47d-331">Supporto dell'accesso con un account utente senza sottoscrizioni associate</span><span class="sxs-lookup"><span data-stu-id="6a47d-331">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="6a47d-332">RDBMS</span><span class="sxs-lookup"><span data-stu-id="6a47d-332">RDBMS</span></span>

* <span data-ttu-id="6a47d-333">Supporto della creazione di elenchi di server in una sottoscrizione (#3417)</span><span class="sxs-lookup"><span data-stu-id="6a47d-333">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="6a47d-334">Risoluzione del problema relativo alla mancata elaborazione di `%s` a causa dell'assenza del valore `% server_type` (#3393)</span><span class="sxs-lookup"><span data-stu-id="6a47d-334">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="6a47d-335">Risoluzione del problema relativo alla mappa di origine del documento e aggiunta di un'attività di integrazione continua per la verifica (#3361)</span><span class="sxs-lookup"><span data-stu-id="6a47d-335">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="6a47d-336">Risoluzione dei problemi della Guida di MySQL e PostgreSQL (#3369)</span><span class="sxs-lookup"><span data-stu-id="6a47d-336">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="6a47d-337">Risorsa</span><span class="sxs-lookup"><span data-stu-id="6a47d-337">Resource</span></span>

* <span data-ttu-id="6a47d-338">Miglioramento dei prompt relativi a parametri mancanti per `group deployment create`</span><span class="sxs-lookup"><span data-stu-id="6a47d-338">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="6a47d-339">Miglioramento dell'analisi della sintassi di `--parameters KEY=VALUE`</span><span class="sxs-lookup"><span data-stu-id="6a47d-339">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="6a47d-340">Risoluzione dei problemi relativi al mancato riconoscimento dei file di parametri di `group deployment create` con la sintassi `@<file>`</span><span class="sxs-lookup"><span data-stu-id="6a47d-340">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="6a47d-341">Supporto dell'argomento `--ids` per i comandi `resource` e `managedapp`</span><span class="sxs-lookup"><span data-stu-id="6a47d-341">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="6a47d-342">Risoluzione di alcuni messaggi relativi ad analisi ed errori (#3584)</span><span class="sxs-lookup"><span data-stu-id="6a47d-342">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="6a47d-343">Risoluzione dei problemi relativi all'analisi di `--resource-type` per consentire al comando `lock` di accettare `<resource-namespace>` e `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="6a47d-343">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="6a47d-344">Aggiunta della verifica del parametro per i modelli di collegamenti ai modelli (#3629)</span><span class="sxs-lookup"><span data-stu-id="6a47d-344">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="6a47d-345">Aggiunta del supporto per specificare i parametri di distribuzione tramite la sintassi `KEY=VALUE`</span><span class="sxs-lookup"><span data-stu-id="6a47d-345">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="6a47d-346">Ruolo</span><span class="sxs-lookup"><span data-stu-id="6a47d-346">Role</span></span>

* <span data-ttu-id="6a47d-347">Supporto dell'output nel formato del file di autenticazione di SDK per `create-for-rbac`</span><span class="sxs-lookup"><span data-stu-id="6a47d-347">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="6a47d-348">Pulizia delle assegnazioni di ruolo e dell'applicazione AAD correlata in caso di eliminazione di un'entità servizio (#3610)</span><span class="sxs-lookup"><span data-stu-id="6a47d-348">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="6a47d-349">Inclusione del formato dell'ora negli argomenti `app create` per le descrizioni `--start-date` ed `--end-date`</span><span class="sxs-lookup"><span data-stu-id="6a47d-349">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="6a47d-350">Visualizzazione degli avvisi relativi a elementi deprecati quando si usa `--expanded-view`</span><span class="sxs-lookup"><span data-stu-id="6a47d-350">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="6a47d-351">Aggiunta dell'integrazione dell'insieme di credenziali delle chiavi ai comandi `create-for-rbac` e `reset-credentials`</span><span class="sxs-lookup"><span data-stu-id="6a47d-351">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="6a47d-352">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="6a47d-352">Service Fabric</span></span>
* <span data-ttu-id="6a47d-353">Risoluzione di un problema relativo al troncamento dei file di grandi dimensioni nelle applicazioni in fase di caricamento (#3666)</span><span class="sxs-lookup"><span data-stu-id="6a47d-353">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="6a47d-354">Aggiunta dei test per i comandi di Service Fabric (#3424)</span><span class="sxs-lookup"><span data-stu-id="6a47d-354">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="6a47d-355">Risoluzione dei problemi di numerosi comandi di Service Fabric (#3234)</span><span class="sxs-lookup"><span data-stu-id="6a47d-355">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="6a47d-356">SQL</span><span class="sxs-lookup"><span data-stu-id="6a47d-356">SQL</span></span>

* <span data-ttu-id="6a47d-357">Rimozione del parametro `sql server create` `--identity` non funzionante</span><span class="sxs-lookup"><span data-stu-id="6a47d-357">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="6a47d-358">Rimozione dei valori della password dall'output dei comandi `sql server create` e `sql server update`</span><span class="sxs-lookup"><span data-stu-id="6a47d-358">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="6a47d-359">Aggiunta dei comandi `sql db list-editions` e `sql elastic-pool list-editions`</span><span class="sxs-lookup"><span data-stu-id="6a47d-359">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="6a47d-360">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="6a47d-360">Storage</span></span>

* <span data-ttu-id="6a47d-361">Rimozione dell'opzione `--marker` dai comandi `storage blob list`, `storage container list` e `storage share list` (#3745)</span><span class="sxs-lookup"><span data-stu-id="6a47d-361">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="6a47d-362">Abilitazione della creazione di un account di archiviazione solo HTTPS</span><span class="sxs-lookup"><span data-stu-id="6a47d-362">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="6a47d-363">Aggiornamento delle metriche di archiviazione, della registrazione e dei comandi CORS (#3495)</span><span class="sxs-lookup"><span data-stu-id="6a47d-363">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="6a47d-364">Nuova formulazione del messaggio di eccezione dall'aggiunta di CORS (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="6a47d-364">Rephrased exception message from CORS add (#3638) (#3362)</span></span>  
* <span data-ttu-id="6a47d-365">Conversione del generatore in elenco in modalità di test controllato del comando Batch di download (#3592)</span><span class="sxs-lookup"><span data-stu-id="6a47d-365">Converted generator to a list in download batch command dry run mode (#3592)</span></span> 
* <span data-ttu-id="6a47d-366">Risoluzione del problema relativo al test controllato di Batch del download di BLOB (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="6a47d-366">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="6a47d-367">VM</span><span class="sxs-lookup"><span data-stu-id="6a47d-367">VM</span></span>

* <span data-ttu-id="6a47d-368">Supporto per la configurazione di nsg</span><span class="sxs-lookup"><span data-stu-id="6a47d-368">Support configuring nsg</span></span>
* <span data-ttu-id="6a47d-369">Risoluzione di un bug relativo alla configurazione non corretta del server DNS</span><span class="sxs-lookup"><span data-stu-id="6a47d-369">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="6a47d-370">Supporto per le identità del servizio gestito</span><span class="sxs-lookup"><span data-stu-id="6a47d-370">Support managed service identities</span></span>
* <span data-ttu-id="6a47d-371">Risoluzione del problema relativo al fatto che `cmss create` con un servizio di bilanciamento del carico esistente richiede `--backend-pool-name`.</span><span class="sxs-lookup"><span data-stu-id="6a47d-371">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="6a47d-372">I dischi dati creati con LUN `vm image create` iniziano con 0</span><span class="sxs-lookup"><span data-stu-id="6a47d-372">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="6a47d-373">10 maggio 2017</span><span class="sxs-lookup"><span data-stu-id="6a47d-373">May 10, 2017</span></span>

<span data-ttu-id="6a47d-374">Versione 2.0.6</span><span class="sxs-lookup"><span data-stu-id="6a47d-374">Version 2.0.6</span></span>

* <span data-ttu-id="6a47d-375">documentdb rinominato come cosmosdb</span><span class="sxs-lookup"><span data-stu-id="6a47d-375">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="6a47d-376">Aggiunge rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="6a47d-376">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="6a47d-377">Include i moduli di Data Lake Store e Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6a47d-377">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="6a47d-378">Include i moduli di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="6a47d-378">Include Cognitive Services module.</span></span>
* <span data-ttu-id="6a47d-379">Include i moduli di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="6a47d-379">Include Service Fabric module.</span></span>
* <span data-ttu-id="6a47d-380">Include i moduli interattivi e rinomina az-shell.</span><span class="sxs-lookup"><span data-stu-id="6a47d-380">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="6a47d-381">Aggiunge il supporto per i comandi CDN.</span><span class="sxs-lookup"><span data-stu-id="6a47d-381">Add support for CDN commands.</span></span>
* <span data-ttu-id="6a47d-382">Rimuove il modulo del contenitore.</span><span class="sxs-lookup"><span data-stu-id="6a47d-382">Remove Container module.</span></span>
* <span data-ttu-id="6a47d-383">Aggiunge "az -v" come collegamento per "az -- version" ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="6a47d-383">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="6a47d-384">Migliora le prestazioni di carico del pacchetto e l'esecuzione del comando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="6a47d-384">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="6a47d-385">Core</span><span class="sxs-lookup"><span data-stu-id="6a47d-385">Core</span></span>

* <span data-ttu-id="6a47d-386">core: consente di acquisire le eccezioni causate dall'annullamento della registrazione e dalla registrazione automatica del provider</span><span class="sxs-lookup"><span data-stu-id="6a47d-386">core: capture exceptions caused by unregistered provider and auto-register it</span></span>   
* <span data-ttu-id="6a47d-387">perf: consente di mantenere la cache del token ADAL in memoria fino alla chiusura di processo ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="6a47d-387">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="6a47d-388">Consente di correggere i byte restituiti da impronta digitale hex -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="6a47d-388">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="6a47d-389">Download dei certificati del Key Vault e dell'integrazione AAD SP migliorati ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="6a47d-389">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="6a47d-390">Aggiunge il percorso di Python per "az —version" ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="6a47d-390">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="6a47d-391">login: supporta l'accesso quando non sono presenti sottoscrizioni ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="6a47d-391">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="6a47d-392">core: consente di correggere un errore quando si effettua l'accesso usando un'entità servizio due volte ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="6a47d-392">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="6a47d-393">core: consente al percorso del file accessTokens.json di poter essere configurato tramite un env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="6a47d-393">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="6a47d-394">core: consente ai valori predefiniti configurati di essere applicati solo ad argomenti facoltativi ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="6a47d-394">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="6a47d-395">core: prestazioni migliorate</span><span class="sxs-lookup"><span data-stu-id="6a47d-395">core: Improved performance</span></span>
* <span data-ttu-id="6a47d-396">core: certificati CA personalizzati: supporta l'impostazione della variabile di ambiente REQUESTS_CA_BUNDLE</span><span class="sxs-lookup"><span data-stu-id="6a47d-396">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="6a47d-397">core: configurazione del cloud: usa l'endpoint "gestione risorse" se l'endpoint "gestione" non è impostato</span><span class="sxs-lookup"><span data-stu-id="6a47d-397">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="6a47d-398">ACS</span><span class="sxs-lookup"><span data-stu-id="6a47d-398">ACS</span></span>

* <span data-ttu-id="6a47d-399">consente di correggere il conteggio di master e agenti affinché sia un numero intero anziché una stringa</span><span class="sxs-lookup"><span data-stu-id="6a47d-399">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="6a47d-400">espone "az acs create --no-wait" e "az acs wait" alla creazione asincrona</span><span class="sxs-lookup"><span data-stu-id="6a47d-400">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="6a47d-401">espone "az acs create --validate" alle convalide del test controllato</span><span class="sxs-lookup"><span data-stu-id="6a47d-401">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="6a47d-402">rimuove il profilo di Windows prima di INSERIRE la chiamata del comando scale ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="6a47d-402">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="6a47d-403">AppService</span><span class="sxs-lookup"><span data-stu-id="6a47d-403">AppService</span></span>

* <span data-ttu-id="6a47d-404">functionapp: aggiunge supporti functionapp completi, tra cui create, show, list, delete, hostname, ssl e così via</span><span class="sxs-lookup"><span data-stu-id="6a47d-404">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="6a47d-405">Aggiunta di servizi di Team (vsts) come opzione di consegna continua a "appservice web source-control config"</span><span class="sxs-lookup"><span data-stu-id="6a47d-405">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="6a47d-406">Consente di creare "az webapp" per sostituire "az appservice web". Per la compatibilità con le versioni precedenti, "az appservice web" viene mantenuta per 2 versioni</span><span class="sxs-lookup"><span data-stu-id="6a47d-406">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="6a47d-407">Espone gli argomenti per configurare la distribuzione e "stack di runtime" su webapp</span><span class="sxs-lookup"><span data-stu-id="6a47d-407">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="6a47d-408">Espone "webapp list-runtimes"</span><span class="sxs-lookup"><span data-stu-id="6a47d-408">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="6a47d-409">supporta le stringhe di connessione per la configurazione ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="6a47d-409">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="6a47d-410">supporta lo scambio di slot con anteprima</span><span class="sxs-lookup"><span data-stu-id="6a47d-410">support slot swap with preview</span></span>
* <span data-ttu-id="6a47d-411">Errori di polacco neii comandi appservice ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="6a47d-411">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="6a47d-412">Usa il gruppo di risorse del piano del servizio app per le operazioni cert ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="6a47d-412">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="6a47d-413">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="6a47d-413">CosmosDB</span></span>

* <span data-ttu-id="6a47d-414">Rinomina il modulo documentdb in cosmosdb.</span><span class="sxs-lookup"><span data-stu-id="6a47d-414">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="6a47d-415">Aggiunto il supporto per le API del piano di dati documentdb: gestione di database e raccolta</span><span class="sxs-lookup"><span data-stu-id="6a47d-415">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="6a47d-416">Aggiunto il supporto per abilitare il failover automatico negli account del database</span><span class="sxs-lookup"><span data-stu-id="6a47d-416">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="6a47d-417">Aggiunto il supporto per nuovi criteri di coerenza ConsistentPrefix</span><span class="sxs-lookup"><span data-stu-id="6a47d-417">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="6a47d-418">Analisi Data Lake</span><span class="sxs-lookup"><span data-stu-id="6a47d-418">Data Lake Analytics</span></span>

* <span data-ttu-id="6a47d-419">Consente di correggere un bug in cui il filtro dei risultati e lo stato degli elenchi del processo genererebbe un errore.</span><span class="sxs-lookup"><span data-stu-id="6a47d-419">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="6a47d-420">Aggiunge il supporto per il tipo di elementi del nuovo catalogo: pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6a47d-420">Add support for new catalog item type: package.</span></span> <span data-ttu-id="6a47d-421">accessibili tramite: `az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="6a47d-421">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="6a47d-422">È possibile elencare gli elementi seguenti del catalogo da un database, senza necessità delle specifiche dello schema:</span><span class="sxs-lookup"><span data-stu-id="6a47d-422">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="6a47d-423">Tabella</span><span class="sxs-lookup"><span data-stu-id="6a47d-423">Table</span></span>
  * <span data-ttu-id="6a47d-424">Funzione con valori di tabella</span><span class="sxs-lookup"><span data-stu-id="6a47d-424">Table valued function</span></span>
  * <span data-ttu-id="6a47d-425">Visualizza</span><span class="sxs-lookup"><span data-stu-id="6a47d-425">View</span></span>
  * <span data-ttu-id="6a47d-426">Statistiche tabelle.</span><span class="sxs-lookup"><span data-stu-id="6a47d-426">Table Statistics.</span></span> <span data-ttu-id="6a47d-427">Questo elemento può essere elencato anche con uno schema, ma senza specificare un nome di tabella.</span><span class="sxs-lookup"><span data-stu-id="6a47d-427">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="6a47d-428">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="6a47d-428">Data Lake Store</span></span>

* <span data-ttu-id="6a47d-429">Aggiorna la versione dell'SDK del file system sottostante, che offre un supporto migliore per la gestione di scenari con limitazione lato server.</span><span class="sxs-lookup"><span data-stu-id="6a47d-429">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="6a47d-430">Migliora le prestazioni di carico del pacchetto e l'esecuzione del comando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="6a47d-430">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="6a47d-431">guida mancate per la presentazione di accesso.</span><span class="sxs-lookup"><span data-stu-id="6a47d-431">missed help for access show.</span></span> <span data-ttu-id="6a47d-432">aggiunta.</span><span class="sxs-lookup"><span data-stu-id="6a47d-432">adding it.</span></span> <span data-ttu-id="6a47d-433">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="6a47d-433">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="6a47d-434">Find</span><span class="sxs-lookup"><span data-stu-id="6a47d-434">Find</span></span>

* <span data-ttu-id="6a47d-435">migliora i risultati di ricerca e consente di controllare le versioni dell'indice di ricerca</span><span class="sxs-lookup"><span data-stu-id="6a47d-435">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="6a47d-436">Insieme di credenziali delle chiavi</span><span class="sxs-lookup"><span data-stu-id="6a47d-436">KeyVault</span></span>

* <span data-ttu-id="6a47d-437">BC: `az keyvault certificate download` modifica -e dalla stringa o dal binario in PEM o DER per rappresentare meglio le opzioni</span><span class="sxs-lookup"><span data-stu-id="6a47d-437">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="6a47d-438">BC: rimuove --expires e --not-before da `keyvault certificate create` poiché questi parametri non sono supportati dal servizio.</span><span class="sxs-lookup"><span data-stu-id="6a47d-438">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="6a47d-439">Aggiunge il parametro --validity a `keyvault certificate create` per eseguire l'override in modo selettivo del valore in --policy</span><span class="sxs-lookup"><span data-stu-id="6a47d-439">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="6a47d-440">Consente di risolvere i problemi in `keyvault certificate get-default-policy` laddove sono stati esposti "expires" e "not_before", ma non "validity_in_months".</span><span class="sxs-lookup"><span data-stu-id="6a47d-440">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="6a47d-441">correzione di keyvault per l'importazione di pem e pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="6a47d-441">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="6a47d-442">Lab</span><span class="sxs-lookup"><span data-stu-id="6a47d-442">Lab</span></span>

* <span data-ttu-id="6a47d-443">Aggiunta dei comandi create, show, delete e list per l'ambiente nel laboratorio.</span><span class="sxs-lookup"><span data-stu-id="6a47d-443">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="6a47d-444">Aggiunta di comandi show e list per visualizzare i modelli ARM nel laboratorio.</span><span class="sxs-lookup"><span data-stu-id="6a47d-444">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="6a47d-445">Aggiunta del flag --environment in `az lab vm list` per filtrare le macchine virtuali in base all'ambiente nel laboratorio.</span><span class="sxs-lookup"><span data-stu-id="6a47d-445">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="6a47d-446">Aggiunge il comando di convenienza `az lab formula export-artifacts` per esportare lo scaffolding dell'elemento all'interno della formula di Lab.</span><span class="sxs-lookup"><span data-stu-id="6a47d-446">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="6a47d-447">Aggiunge i comandi per gestire i segreti in Lab.</span><span class="sxs-lookup"><span data-stu-id="6a47d-447">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="6a47d-448">Monitorare</span><span class="sxs-lookup"><span data-stu-id="6a47d-448">Monitor</span></span>

* <span data-ttu-id="6a47d-449">Correzione di bug: modellazione di `--actions` in `az alert-rules create` per usare una stringa JSON ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="6a47d-449">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="6a47d-450">Correzione di bug: diagnostic settings create non accetta i registri/le metriche dei comandi show ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="6a47d-450">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="6a47d-451">Rete</span><span class="sxs-lookup"><span data-stu-id="6a47d-451">Network</span></span>

* <span data-ttu-id="6a47d-452">Aggiunge il comando `network watcher test-connectivity`.</span><span class="sxs-lookup"><span data-stu-id="6a47d-452">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="6a47d-453">Aggiunge il supporto per il parametro `--filters` per `network watcher packet-capture create`.</span><span class="sxs-lookup"><span data-stu-id="6a47d-453">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="6a47d-454">Aggiunge il supporto per lo svuotamento della connessione del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6a47d-454">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="6a47d-455">Aggiunge il supporto per la configurazione dell'insieme di regole WAF del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6a47d-455">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="6a47d-456">Aggiunge il supporto per le regole e i filtri di route ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6a47d-456">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="6a47d-457">Aggiunge il supporto per il routing geografico di TrafficManager.</span><span class="sxs-lookup"><span data-stu-id="6a47d-457">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="6a47d-458">Aggiunge il supporto per i selettori di traffico basati su criteri di connessione VPN.</span><span class="sxs-lookup"><span data-stu-id="6a47d-458">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="6a47d-459">Aggiunge il supporto per i criteri IPSec della connessione VPN.</span><span class="sxs-lookup"><span data-stu-id="6a47d-459">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="6a47d-460">Correzione di bug con `vpn-connection create` quando si usano i parametri `--no-wait` o `--validate`.</span><span class="sxs-lookup"><span data-stu-id="6a47d-460">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="6a47d-461">Aggiunge il supporto per i gateway di rete virtuale attivo/attivo</span><span class="sxs-lookup"><span data-stu-id="6a47d-461">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="6a47d-462">Rimuove i valori null i valori dall'output dei comandi `network vpn-connection list/show`.</span><span class="sxs-lookup"><span data-stu-id="6a47d-462">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="6a47d-463">BC: correzione di bug nell'output di `vpn-connection create`</span><span class="sxs-lookup"><span data-stu-id="6a47d-463">BC: Fix bug in the output of `vpn-connection create`</span></span> 
* <span data-ttu-id="6a47d-464">Corregge i bug in cui l'argomento "--key-length" di "vpn-connection create"' non è stato analizzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="6a47d-464">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="6a47d-465">Corregge i bug in `dns zone import` in cui i record non sono stati importati correttamente.</span><span class="sxs-lookup"><span data-stu-id="6a47d-465">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="6a47d-466">Corregge i bug laddove `traffic-manager endpoint update` non funzionava.</span><span class="sxs-lookup"><span data-stu-id="6a47d-466">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="6a47d-467">Aggiunge i comandi di anteprima "network watcher".</span><span class="sxs-lookup"><span data-stu-id="6a47d-467">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="6a47d-468">Profilo</span><span class="sxs-lookup"><span data-stu-id="6a47d-468">Profile</span></span>

* <span data-ttu-id="6a47d-469">Supporta l'accesso quando non sono state trovate sottoscrizioni ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="6a47d-469">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="6a47d-470">Supporta l'abbreviazione del nome dei parametri in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="6a47d-470">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="6a47d-471">Redis</span><span class="sxs-lookup"><span data-stu-id="6a47d-471">Redis</span></span>

* <span data-ttu-id="6a47d-472">Aggiunta del comando update che offre anche la possibilità di passare alla cache Redis</span><span class="sxs-lookup"><span data-stu-id="6a47d-472">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="6a47d-473">Il comando "update-settings" viene deprecato.</span><span class="sxs-lookup"><span data-stu-id="6a47d-473">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="6a47d-474">Risorsa</span><span class="sxs-lookup"><span data-stu-id="6a47d-474">Resource</span></span>

* <span data-ttu-id="6a47d-475">Aggiunge i comandi managedapp e managedapp definition ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="6a47d-475">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="6a47d-476">Supporta i comandi "provider operation" ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="6a47d-476">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="6a47d-477">Supporta la creazione della risorsa generica ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="6a47d-477">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="6a47d-478">Corregge l'analisi della risorsa e la ricerca della versione API.</span><span class="sxs-lookup"><span data-stu-id="6a47d-478">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="6a47d-479">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="6a47d-479">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="6a47d-480">Aggiunge docs ad az lock update.</span><span class="sxs-lookup"><span data-stu-id="6a47d-480">Add docs for az lock update.</span></span> <span data-ttu-id="6a47d-481">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="6a47d-481">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="6a47d-482">Genera un errore se si tenta di elencare le risorse per un gruppo che non esiste.</span><span class="sxs-lookup"><span data-stu-id="6a47d-482">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="6a47d-483">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="6a47d-483">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="6a47d-484">[Compute] Risolve i problemi con l'aggiornamento dei set di disponibilità VMSS e della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6a47d-484">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="6a47d-485">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="6a47d-485">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="6a47d-486">Correzione della creazione e dell'eliminazione del blocco se parent-resource-path è Nessuno ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="6a47d-486">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="6a47d-487">Ruolo</span><span class="sxs-lookup"><span data-stu-id="6a47d-487">Role</span></span>

* <span data-ttu-id="6a47d-488">create-for-rbac: assicura che la data di fine di SP non superi la data di scadenza del certificato ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="6a47d-488">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="6a47d-489">RBAC: aggiunge il supporto completo ad "ad group" ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="6a47d-489">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="6a47d-490">role: corregge i problemi in role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="6a47d-490">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="6a47d-491">create-for-rbac: garantisce che venga presa la password indicata</span><span class="sxs-lookup"><span data-stu-id="6a47d-491">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="6a47d-492">SQL</span><span class="sxs-lookup"><span data-stu-id="6a47d-492">SQL</span></span>

* <span data-ttu-id="6a47d-493">Aggiunti i comandi az sql server list-usages e az sql db list-usages.</span><span class="sxs-lookup"><span data-stu-id="6a47d-493">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="6a47d-494">SQL: possibilità di connettersi direttamente al provider di risorse ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="6a47d-494">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="6a47d-495">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="6a47d-495">Storage</span></span>

* <span data-ttu-id="6a47d-496">Percorso predefinito al percorso del gruppo di risorse per `storage account create`.</span><span class="sxs-lookup"><span data-stu-id="6a47d-496">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="6a47d-497">Aggiunge il supporto per la copia di BLOB incrementale</span><span class="sxs-lookup"><span data-stu-id="6a47d-497">Add support for incremental blob copy</span></span>
* <span data-ttu-id="6a47d-498">Aggiunge il supporto per il upload di BLOB in blocchi di grandi dimensioni</span><span class="sxs-lookup"><span data-stu-id="6a47d-498">Add support for large block blob upload</span></span>
* <span data-ttu-id="6a47d-499">Modifica le dimensioni del blocco in 100 MB quando il file da caricare supera i 200 GB</span><span class="sxs-lookup"><span data-stu-id="6a47d-499">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="6a47d-500">VM</span><span class="sxs-lookup"><span data-stu-id="6a47d-500">VM</span></span>

* <span data-ttu-id="6a47d-501">avail-set: rende facoltativo il conteggio del dominio UD&FD</span><span class="sxs-lookup"><span data-stu-id="6a47d-501">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="6a47d-502">note: comandi della VM nei cloud sovrani. Evitare le funzionalità correlate al disco gestito, tra cui:</span><span class="sxs-lookup"><span data-stu-id="6a47d-502">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="6a47d-503">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="6a47d-503">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="6a47d-504">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="6a47d-504">az vm/vmss disk</span></span>
  3. <span data-ttu-id="6a47d-505">All'interno di "az vm/vmss create" usare "—use-unmanaged-disk" per evitare che il disco gestito. Funziona anche con altri comandi</span><span class="sxs-lookup"><span data-stu-id="6a47d-505">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="6a47d-506">vm/vmss: migliora il testo di avviso quando si generano coppie di chiavi SSH</span><span class="sxs-lookup"><span data-stu-id="6a47d-506">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="6a47d-507">vm/vmss: supporta la creazione da un'immagine del marketplace che richiede informazioni sul piano ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="6a47d-507">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="6a47d-508">3 aprile 2017</span><span class="sxs-lookup"><span data-stu-id="6a47d-508">April 3, 2017</span></span>

<span data-ttu-id="6a47d-509">Versione 2.0.2</span><span class="sxs-lookup"><span data-stu-id="6a47d-509">Version 2.0.2</span></span>

<span data-ttu-id="6a47d-510">In questa versione sono stati rilasciati i componenti ACR, Batch, KeyVault e SQL.</span><span class="sxs-lookup"><span data-stu-id="6a47d-510">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="6a47d-511">Core</span><span class="sxs-lookup"><span data-stu-id="6a47d-511">Core</span></span>

* <span data-ttu-id="6a47d-512">Aggiunta dei moduli acr, lab, monitor e find all'elenco predefinito.</span><span class="sxs-lookup"><span data-stu-id="6a47d-512">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="6a47d-513">Login: esclusione del tenant errato ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="6a47d-513">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="6a47d-514">login: impostazione della sottoscrizione predefinita su una con lo stato "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="6a47d-514">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="6a47d-515">Aggiunta di comandi wait e di supporto per --no-wait a più comandi ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="6a47d-515">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="6a47d-516">core: supporto per accesso mediante entità servizio con un certificato ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="6a47d-516">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="6a47d-517">Aggiunta della richiesta dei parametri di modello mancanti.</span><span class="sxs-lookup"><span data-stu-id="6a47d-517">Add prompting for missing template parameters.</span></span> <span data-ttu-id="6a47d-518">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="6a47d-518">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="6a47d-519">Supporto per l'impostazione di valori predefiniti per argomenti comuni ad esempio gruppo di risorse predefinito, Web predefinito, macchina virtuale predefinita</span><span class="sxs-lookup"><span data-stu-id="6a47d-519">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="6a47d-520">Supporto per l'accesso al tenant specifico</span><span class="sxs-lookup"><span data-stu-id="6a47d-520">Support login to specific tenant</span></span>
 
### <a name="acs"></a><span data-ttu-id="6a47d-521">ACS</span><span class="sxs-lookup"><span data-stu-id="6a47d-521">ACS</span></span>

* <span data-ttu-id="6a47d-522">[ACS] Aggiunta di supporto per la configurazione di un cluster ACS predefinito ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="6a47d-522">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="6a47d-523">Aggiunta di supporto per la richiesta di password della chiave SSH.</span><span class="sxs-lookup"><span data-stu-id="6a47d-523">Add support for ssh key password prompting.</span></span> <span data-ttu-id="6a47d-524">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="6a47d-524">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="6a47d-525">Aggiunta di supporto per i cluster Windows.</span><span class="sxs-lookup"><span data-stu-id="6a47d-525">Add support for windows clusters.</span></span> <span data-ttu-id="6a47d-526">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="6a47d-526">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="6a47d-527">Passaggio dal ruolo Proprietario al ruolo Collaboratore.</span><span class="sxs-lookup"><span data-stu-id="6a47d-527">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="6a47d-528">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="6a47d-528">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>
 
### <a name="appservice"></a><span data-ttu-id="6a47d-529">AppService</span><span class="sxs-lookup"><span data-stu-id="6a47d-529">AppService</span></span>

* <span data-ttu-id="6a47d-530">appservice: supporto per ottenere l'indirizzo IP esterno usato per i record DNS A ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="6a47d-530">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="6a47d-531">appservice: supporto dell'associazione di certificati jolly ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="6a47d-531">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="6a47d-532">appservice: supporto dell'elenco di profili di pubblicazione ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="6a47d-532">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="6a47d-533">AppService - attivazione della sincronizzazione del controllo dopo la configurazione ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="6a47d-533">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>
 
### <a name="datalake"></a><span data-ttu-id="6a47d-534">DataLake</span><span class="sxs-lookup"><span data-stu-id="6a47d-534">DataLake</span></span>

* <span data-ttu-id="6a47d-535">Versione iniziale del modulo Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6a47d-535">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="6a47d-536">Versione iniziale del modulo Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6a47d-536">Initial release of Data Lake Store module.</span></span>
 
### <a name="docuemntdb"></a><span data-ttu-id="6a47d-537">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="6a47d-537">DocuemntDB</span></span>

* <span data-ttu-id="6a47d-538">DocumentDB: aggiunta di supporto per l'elenco di stringhe di connessione ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="6a47d-538">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="6a47d-539">VM</span><span class="sxs-lookup"><span data-stu-id="6a47d-539">VM</span></span>

* <span data-ttu-id="6a47d-540">[Compute] Aggiunta di supporto per AppGateway alla creazione di set di scalabilità di macchine virtuali ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="6a47d-540">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="6a47d-541">[VM/VMSS] Miglioramento del supporto per memorizzazione nella cache del disco ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="6a47d-541">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="6a47d-542">VM/VMSS: inclusione di logica di convalida credenziali usata dal portale ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="6a47d-542">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="6a47d-543">Aggiunta di comandi wait e di supporto per --no-wait ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="6a47d-543">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="6a47d-544">Virtual machine scale set: supporto * per elencare le visualizzazioni di istanza tra le macchine virtuali ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="6a47d-544">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="6a47d-545">Aggiunta di --secrets per la macchina virtuale e il set di scalabilità di macchine virtuali ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="6a47d-545">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="6a47d-546">Consentita la creazione di macchine virtuali con disco rigido virtuale specializzato ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="6a47d-546">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="6a47d-547">27 febbraio 2017</span><span class="sxs-lookup"><span data-stu-id="6a47d-547">February 27, 2017</span></span>

<span data-ttu-id="6a47d-548">Versione 2.0.0</span><span class="sxs-lookup"><span data-stu-id="6a47d-548">Version 2.0.0</span></span>

<span data-ttu-id="6a47d-549">Questa versione dell'interfaccia della riga di comando di Azure 2.0 è la prima versione disponibile a livello generale.</span><span class="sxs-lookup"><span data-stu-id="6a47d-549">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="6a47d-550">La disponibilità generale si applica ai moduli comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="6a47d-550">General availability applies to these command modules:</span></span>
- <span data-ttu-id="6a47d-551">Servizio contenitore (acs)</span><span class="sxs-lookup"><span data-stu-id="6a47d-551">Container Service (acs)</span></span>
- <span data-ttu-id="6a47d-552">Compute (inclusi Resource Manager, macchina virtuale, set di scalabilità di macchine virtuali, Managed Disks)</span><span class="sxs-lookup"><span data-stu-id="6a47d-552">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="6a47d-553">Rete</span><span class="sxs-lookup"><span data-stu-id="6a47d-553">Networking</span></span>
- <span data-ttu-id="6a47d-554">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="6a47d-554">Storage</span></span>

<span data-ttu-id="6a47d-555">Questi moduli comandi possono essere usati nella produzione e sono supportati dal contratto di servizio Microsoft standard.</span><span class="sxs-lookup"><span data-stu-id="6a47d-555">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="6a47d-556">È possibile segnalare i problemi direttamente al supporto tecnico Microsoft o tramite l'[elenco di problemi github](https://github.com/azure/azure-cli/issues/).</span><span class="sxs-lookup"><span data-stu-id="6a47d-556">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="6a47d-557">È possibile porre domande su [StackOverflow usando il tag azure-cli](http://stackoverflow.com/questions/tagged/azure-cli) o contattare il team del prodotto all'indirizzo [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). È possibile fornire commenti e suggerimenti dalla riga di comando con il comando `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="6a47d-557">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="6a47d-558">I comandi in questi moduli sono stabili e non si prevede che la sintassi cambi nei prossimi rilasci di questa versione dell'interfaccia della riga di comando di Azure.</span><span class="sxs-lookup"><span data-stu-id="6a47d-558">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="6a47d-559">Per verificare la versione dell'interfaccia della riga di comando, usare `az --version`.</span><span class="sxs-lookup"><span data-stu-id="6a47d-559">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="6a47d-560">L'output elenca la versione dell'interfaccia della riga di comando stessa (2.0.0 in questo rilascio), i singoli moduli comandi e le versioni di Python e GCC in uso.</span><span class="sxs-lookup"><span data-stu-id="6a47d-560">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="6a47d-561">Alcuni dei moduli del comando presentano un suffisso "b*n*" o "rc*n*".</span><span class="sxs-lookup"><span data-stu-id="6a47d-561">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="6a47d-562">Questi moduli comandi sono ancora in fase di anteprima e saranno disponibili a livello generale in futuro.</span><span class="sxs-lookup"><span data-stu-id="6a47d-562">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="6a47d-563">Sono anche disponibili build di anteprima notturne dell'interfaccia della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="6a47d-563">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="6a47d-564">Per informazioni, vedere le istruzioni su come [ottenere le build notturne](https://github.com/Azure/azure-cli#nightly-builds) e le istruzioni sull'[impostazione per gli sviluppatori e sul codice per i collaboratori](https://github.com/Azure/azure-cli#developer-setup).</span><span class="sxs-lookup"><span data-stu-id="6a47d-564">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="6a47d-565">È possibile segnalare problemi relative alle build di anteprima notturne nei seguenti modi:</span><span class="sxs-lookup"><span data-stu-id="6a47d-565">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="6a47d-566">Segnalare i problemi tramite l'[elenco di problemi github](https://github.com/azure/azure-cli/issues/)</span><span class="sxs-lookup"><span data-stu-id="6a47d-566">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="6a47d-567">Contattare il tema del prodotto all'indirizzo [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="6a47d-567">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="6a47d-568">Fornire commenti e suggerimenti dalla riga di comando con il comando `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="6a47d-568">Provide feedback from the command line with the `az feedback` command.</span></span>

