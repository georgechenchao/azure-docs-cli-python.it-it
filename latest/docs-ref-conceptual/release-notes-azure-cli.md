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
ms.openlocfilehash: ad30efeb7efafcc5816160ee130665d37adb62c6
ms.sourcegitcommit: e866977985ba0286fa05f41729dd7e7d9ce86f8e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/13/2017
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="25887-104">Note sulla versione dell'interfaccia della riga di comando di Azure 2.0</span><span class="sxs-lookup"><span data-stu-id="25887-104">Azure CLI 2.0 release notes</span></span>

## <a name="september-11-2017"></a><span data-ttu-id="25887-105">11 settembre 2017</span><span class="sxs-lookup"><span data-stu-id="25887-105">September 11, 2017</span></span>

<span data-ttu-id="25887-106">Versione 2.0.17</span><span class="sxs-lookup"><span data-stu-id="25887-106">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="25887-107">Core</span><span class="sxs-lookup"><span data-stu-id="25887-107">Core</span></span>

* <span data-ttu-id="25887-108">Abilitazione del modulo di comandi per impostare l'ID correlazione nei dati di telemetria</span><span class="sxs-lookup"><span data-stu-id="25887-108">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="25887-109">Risoluzione del problema di dump JSON quando la telemetria viene impostata sulla modalità diagnostica</span><span class="sxs-lookup"><span data-stu-id="25887-109">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="25887-110">ACS</span><span class="sxs-lookup"><span data-stu-id="25887-110">Acs</span></span>

* <span data-ttu-id="25887-111">Aggiunta del comando `acs list-locations`</span><span class="sxs-lookup"><span data-stu-id="25887-111">Added `acs list-locations` command</span></span>
* <span data-ttu-id="25887-112">Impostazione di `ssh-key-file` con il valore predefinito previsto</span><span class="sxs-lookup"><span data-stu-id="25887-112">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="25887-113">Servizio app</span><span class="sxs-lookup"><span data-stu-id="25887-113">Appservice</span></span>

* <span data-ttu-id="25887-114">Possibilità di creare un'app Web in un gruppo di risorse diverso da quello del piano di servizio attivo</span><span class="sxs-lookup"><span data-stu-id="25887-114">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="25887-115">RETE CDN</span><span class="sxs-lookup"><span data-stu-id="25887-115">CDN</span></span>

* <span data-ttu-id="25887-116">Correzione del bug "CustomDomain is not interable" per `cdn custom-domain create`.</span><span class="sxs-lookup"><span data-stu-id="25887-116">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`.</span></span>

### <a name="extension"></a><span data-ttu-id="25887-117">Estensione</span><span class="sxs-lookup"><span data-stu-id="25887-117">Extension</span></span>

* <span data-ttu-id="25887-118">Versione iniziale.</span><span class="sxs-lookup"><span data-stu-id="25887-118">Initial Release.</span></span>

### <a name="keyvault"></a><span data-ttu-id="25887-119">Key Vault</span><span class="sxs-lookup"><span data-stu-id="25887-119">Keyvault</span></span>

* <span data-ttu-id="25887-120">Risoluzione del problema relativo alla distinzione tra maiuscole e minuscole nelle autorizzazioni per `keyvault set-policy`.</span><span class="sxs-lookup"><span data-stu-id="25887-120">Fixed issue where permissions were case sensitive for `keyvault set-policy`.</span></span>

### <a name="network"></a><span data-ttu-id="25887-121">Rete</span><span class="sxs-lookup"><span data-stu-id="25887-121">Network</span></span>

* <span data-ttu-id="25887-122">Ridenominazione di `vnet list-private-access-services` in `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="25887-122">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="25887-123">Ridenominazione dell'argomento `--private-access-services` in `--service-endpoints` per `vnet subnet create/update`</span><span class="sxs-lookup"><span data-stu-id="25887-123">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="25887-124">Aggiunta del supporto per più intervalli IP e intervalli di porte in `nsg rule create/update`</span><span class="sxs-lookup"><span data-stu-id="25887-124">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="25887-125">Aggiunta del supporto per SKU a `lb create`</span><span class="sxs-lookup"><span data-stu-id="25887-125">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="25887-126">Aggiunta del supporto per SKU a `public-ip create`</span><span class="sxs-lookup"><span data-stu-id="25887-126">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="25887-127">Risorsa</span><span class="sxs-lookup"><span data-stu-id="25887-127">Resource</span></span>

* <span data-ttu-id="25887-128">È stato consentito il passaggio delle definizioni dei parametri dei criteri delle risorse in `policy definition create` e `policy definition update`</span><span class="sxs-lookup"><span data-stu-id="25887-128">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="25887-129">È stato consentito il passaggio dei valori dei parametri per `policy assignment create`</span><span class="sxs-lookup"><span data-stu-id="25887-129">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="25887-130">È stato consentito il passaggio di JSON o del file per tutti i parametri</span><span class="sxs-lookup"><span data-stu-id="25887-130">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="25887-131">Incremento della versione API</span><span class="sxs-lookup"><span data-stu-id="25887-131">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="25887-132">SQL</span><span class="sxs-lookup"><span data-stu-id="25887-132">SQL</span></span>

* <span data-ttu-id="25887-133">Aggiunta dei comandi `sql server vnet-rule`</span><span class="sxs-lookup"><span data-stu-id="25887-133">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="25887-134">VM</span><span class="sxs-lookup"><span data-stu-id="25887-134">VM</span></span>

* <span data-ttu-id="25887-135">Correzione: l'accesso non viene assegnato se `--scope` non è specificato</span><span class="sxs-lookup"><span data-stu-id="25887-135">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="25887-136">Correzione: uso della stessa denominazione di estensione usata dal portale</span><span class="sxs-lookup"><span data-stu-id="25887-136">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="25887-137">Rimozione di `subscription` dall'output `[vm|vmss] create`</span><span class="sxs-lookup"><span data-stu-id="25887-137">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="25887-138">Correzione: lo SKU di archiviazione `[vm|vmss] create` non viene applicato nei dischi dati con un'immagine</span><span class="sxs-lookup"><span data-stu-id="25887-138">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="25887-139">Correzione: `vm format-secret --secrets` non accetta ID separati di nuova riga</span><span class="sxs-lookup"><span data-stu-id="25887-139">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="25887-140">31 agosto 2017</span><span class="sxs-lookup"><span data-stu-id="25887-140">August 31, 2017</span></span>

<span data-ttu-id="25887-141">Versione 2.0.16</span><span class="sxs-lookup"><span data-stu-id="25887-141">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="25887-142">Key Vault</span><span class="sxs-lookup"><span data-stu-id="25887-142">Keyvault</span></span>

* <span data-ttu-id="25887-143">Risoluzione del bug relativo al tentativo di risolvere automaticamente la codifica di un segreto con `secret download`</span><span class="sxs-lookup"><span data-stu-id="25887-143">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="25887-144">SF</span><span class="sxs-lookup"><span data-stu-id="25887-144">Sf</span></span>

* <span data-ttu-id="25887-145">Tutti i comandi deprecati a favore dell'interfaccia della riga di comando di Service Fabric (sfctl)</span><span class="sxs-lookup"><span data-stu-id="25887-145">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="25887-146">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="25887-146">Storage</span></span>

* <span data-ttu-id="25887-147">Risoluzione del problema relativo all'impossibilità di creare account di archiviazione in aree che non supportano la funzionalità NetworkACLs</span><span class="sxs-lookup"><span data-stu-id="25887-147">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="25887-148">Determinazione del tipo di contenuto e della codifica del contenuto durante il caricamento di BLOB e file se non vengono specificati né il tipo di contenuto né la codifica del contenuto</span><span class="sxs-lookup"><span data-stu-id="25887-148">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="25887-149">28 agosto 2017</span><span class="sxs-lookup"><span data-stu-id="25887-149">August 28, 2017</span></span>

<span data-ttu-id="25887-150">Versione 2.0.15</span><span class="sxs-lookup"><span data-stu-id="25887-150">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="25887-151">CLI</span><span class="sxs-lookup"><span data-stu-id="25887-151">CLI</span></span>

* <span data-ttu-id="25887-152">Aggiunta di una nota legale a `--version`.</span><span class="sxs-lookup"><span data-stu-id="25887-152">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="25887-153">ACS</span><span class="sxs-lookup"><span data-stu-id="25887-153">ACS</span></span>

* <span data-ttu-id="25887-154">Correzione delle aree di anteprima.</span><span class="sxs-lookup"><span data-stu-id="25887-154">Corrected preview regions.</span></span>
* <span data-ttu-id="25887-155">Formattazione corretta del valore `dns_name_prefix` predefinito.</span><span class="sxs-lookup"><span data-stu-id="25887-155">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="25887-156">Ottimizzazione dell'output del comando di ACS.</span><span class="sxs-lookup"><span data-stu-id="25887-156">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="25887-157">Servizio app</span><span class="sxs-lookup"><span data-stu-id="25887-157">Appservice</span></span>

* <span data-ttu-id="25887-158">[MODIFICA DI RILIEVO] Correzione di incoerenze nell'output di `az webapp config appsettings [delete|set]`</span><span class="sxs-lookup"><span data-stu-id="25887-158">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="25887-159">Aggiunta di un nuovo alias di `-i` per `az webapp config container set --docker-custom-image-name`</span><span class="sxs-lookup"><span data-stu-id="25887-159">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="25887-160">Esposizione di `az webapp log show`</span><span class="sxs-lookup"><span data-stu-id="25887-160">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="25887-161">Esposizione di nuovi argomenti da `az webapp delete` per mantenere il piano di servizio app, le metriche o la registrazione DNS</span><span class="sxs-lookup"><span data-stu-id="25887-161">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="25887-162">Correzione: Rilevamento corretto delle impostazioni dello slot</span><span class="sxs-lookup"><span data-stu-id="25887-162">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="25887-163">IoT</span><span class="sxs-lookup"><span data-stu-id="25887-163">IoT</span></span>

* <span data-ttu-id="25887-164">Correzione #3934: La creazione di criteri non cancella più i criteri esistenti</span><span class="sxs-lookup"><span data-stu-id="25887-164">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="25887-165">Rete</span><span class="sxs-lookup"><span data-stu-id="25887-165">Network</span></span>

* <span data-ttu-id="25887-166">[MODIFICA DI RILIEVO] Ridenominazione di `vnet list-private-access-services` in `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="25887-166">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="25887-167">[MODIFICA DI RILIEVO] Ridenominazione dell'opzione `--private-access-services` in `--service-endpoints` per `vnet subnet [create|update]`</span><span class="sxs-lookup"><span data-stu-id="25887-167">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="25887-168">Aggiunta del supporto per più indirizzi IP e intervalli di porte in `nsg rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="25887-168">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="25887-169">Aggiunta del supporto per SKU a `lb create`</span><span class="sxs-lookup"><span data-stu-id="25887-169">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="25887-170">Aggiunta del supporto per SKU a `public-ip create`</span><span class="sxs-lookup"><span data-stu-id="25887-170">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="25887-171">Profilo</span><span class="sxs-lookup"><span data-stu-id="25887-171">Profile</span></span>

* <span data-ttu-id="25887-172">Esposizione di `--msi` e `--msi-port` per l'accesso tramite l'identità della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="25887-172">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="25887-173">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="25887-173">Service Fabric</span></span>

* <span data-ttu-id="25887-174">Versione di anteprima</span><span class="sxs-lookup"><span data-stu-id="25887-174">Preview release</span></span>
* <span data-ttu-id="25887-175">Semplificazione delle regole relative a utente/password del Registro di sistema per il comando</span><span class="sxs-lookup"><span data-stu-id="25887-175">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="25887-176">Correzione del problema relativo alla richiesta della password per l'utente anche dopo il passaggio del parametro</span><span class="sxs-lookup"><span data-stu-id="25887-176">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="25887-177">Aggiunta del supporto per il valore `registry_cred` vuoto</span><span class="sxs-lookup"><span data-stu-id="25887-177">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="25887-178">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="25887-178">Storage</span></span>

* <span data-ttu-id="25887-179">Abilitazione della configurazione del livello BLOB</span><span class="sxs-lookup"><span data-stu-id="25887-179">Enabled setting blob tier</span></span>
* <span data-ttu-id="25887-180">Aggiunta degli argomenti `--bypass` e `--default-action` a `storage account [create|update]` per supportare il tunneling del servizio</span><span class="sxs-lookup"><span data-stu-id="25887-180">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="25887-181">Aggiunta di comandi per aggiungere regole della rete virtuale e regole basate su indirizzi IP a `storage account network-rule`</span><span class="sxs-lookup"><span data-stu-id="25887-181">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>  
* <span data-ttu-id="25887-182">Abilitazione della crittografia del servizio tramite chiave gestita dal cliente</span><span class="sxs-lookup"><span data-stu-id="25887-182">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="25887-183">[MODIFICA DI RILIEVO] Ridenominazione dell'opzione `--encryption` in `--encryption-services` per il comando `az storage account create and az storage account update`</span><span class="sxs-lookup"><span data-stu-id="25887-183">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="25887-184">Correzione #4220: `az storage account update encryption`: Mancata corrispondenza della sintassi</span><span class="sxs-lookup"><span data-stu-id="25887-184">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="25887-185">VM</span><span class="sxs-lookup"><span data-stu-id="25887-185">VM</span></span>

* <span data-ttu-id="25887-186">Risoluzione del problema relativo alla visualizzazione di informazioni aggiuntive errate per `vmss get-instance-view` quando si usa `--instance-id *`</span><span class="sxs-lookup"><span data-stu-id="25887-186">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="25887-187">Aggiunta del supporto per `--lb-sku` a `vmss create`:</span><span class="sxs-lookup"><span data-stu-id="25887-187">Added support for `--lb-sku` to `vmss create`:</span></span> 
* <span data-ttu-id="25887-188">Rimozione dei nomi di persone dall'elenco di nomi non consentiti dell'amministratore per `[vm|vmss] create`</span><span class="sxs-lookup"><span data-stu-id="25887-188">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span> 
* <span data-ttu-id="25887-189">Risoluzione del problema relativo alla generazione di un errore da parte di `[vm|vmss] create` in caso di impossibilità di estrazione delle informazioni del piano da un'immagine</span><span class="sxs-lookup"><span data-stu-id="25887-189">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="25887-190">Risoluzione del problema relativo all'arresto anomalo in caso di creazione di un set di scalabilità vmms con un servizio di bilanciamento del carico interno</span><span class="sxs-lookup"><span data-stu-id="25887-190">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="25887-191">Risoluzione del problema relativo al mancato funzionamento dell'argomento `--no-wait` con `vm availability-set create`</span><span class="sxs-lookup"><span data-stu-id="25887-191">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="25887-192">15 agosto 2017</span><span class="sxs-lookup"><span data-stu-id="25887-192">August 15, 2017</span></span>

<span data-ttu-id="25887-193">Versione 2.0.14</span><span class="sxs-lookup"><span data-stu-id="25887-193">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="25887-194">ACS</span><span class="sxs-lookup"><span data-stu-id="25887-194">ACS</span></span>

* <span data-ttu-id="25887-195">Correzione del numero di porta sshMaster0 per kubernetes</span><span class="sxs-lookup"><span data-stu-id="25887-195">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="25887-196">Servizio app</span><span class="sxs-lookup"><span data-stu-id="25887-196">Appservice</span></span>

* <span data-ttu-id="25887-197">Correzione dell'eccezione generata durante la creazione di una nuova app Web Linux basata su Git</span><span class="sxs-lookup"><span data-stu-id="25887-197">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="25887-198">Griglia di eventi</span><span class="sxs-lookup"><span data-stu-id="25887-198">Event Grid</span></span>

* <span data-ttu-id="25887-199">Aggiunta di dipendenze di SDK</span><span class="sxs-lookup"><span data-stu-id="25887-199">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="25887-200">11 agosto 2017</span><span class="sxs-lookup"><span data-stu-id="25887-200">August 11, 2017</span></span>

<span data-ttu-id="25887-201">Versione 2.0.13</span><span class="sxs-lookup"><span data-stu-id="25887-201">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="25887-202">ACS</span><span class="sxs-lookup"><span data-stu-id="25887-202">ACS</span></span>

* <span data-ttu-id="25887-203">Aggiunta di altre aree di anteprima</span><span class="sxs-lookup"><span data-stu-id="25887-203">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="25887-204">Batch</span><span class="sxs-lookup"><span data-stu-id="25887-204">Batch</span></span>

* <span data-ttu-id="25887-205">Aggiornamento a Batch SDK 3.1.0 e Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="25887-205">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="25887-206">Aggiunta di un nuovo comando per visualizzare il numero di attività di un processo</span><span class="sxs-lookup"><span data-stu-id="25887-206">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="25887-207">Correzione di un bug nell'elaborazione dell'URL della firma di accesso condiviso del file di risorse</span><span class="sxs-lookup"><span data-stu-id="25887-207">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="25887-208">L'endpoint dell'account Batch supporta ora il prefisso facoltativo 'https://'</span><span class="sxs-lookup"><span data-stu-id="25887-208">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="25887-209">Supporto per l'aggiunta di elenchi di più di 100 attività a un processo</span><span class="sxs-lookup"><span data-stu-id="25887-209">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="25887-210">Aggiunta della registrazione di debug per il caricamento del modulo di comandi delle estensioni</span><span class="sxs-lookup"><span data-stu-id="25887-210">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="25887-211">Componente</span><span class="sxs-lookup"><span data-stu-id="25887-211">Component</span></span>

* <span data-ttu-id="25887-212">Aggiunta dell'avviso relativo a elementi deprecati ai comandi 'az component'</span><span class="sxs-lookup"><span data-stu-id="25887-212">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="25887-213">Contenitore</span><span class="sxs-lookup"><span data-stu-id="25887-213">Container</span></span>

* <span data-ttu-id="25887-214">`create`: risoluzione del problema relativo all'impossibilità di usare il segno di uguale all'interno di una variabile di ambiente</span><span class="sxs-lookup"><span data-stu-id="25887-214">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="25887-215">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="25887-215">Data Lake Store</span></span>

* <span data-ttu-id="25887-216">Abilitazione del controllo dell'avanzamento</span><span class="sxs-lookup"><span data-stu-id="25887-216">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="25887-217">Griglia di eventi</span><span class="sxs-lookup"><span data-stu-id="25887-217">Event Grid</span></span>

* <span data-ttu-id="25887-218">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="25887-218">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="25887-219">Rete</span><span class="sxs-lookup"><span data-stu-id="25887-219">Network</span></span>

* <span data-ttu-id="25887-220">`lb`: correzione del problema relativo alla risoluzione non corretta di determinati nomi di risorse figlio in caso di omissione</span><span class="sxs-lookup"><span data-stu-id="25887-220">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="25887-221">`application-gateway {subresource} delete`: correzione del problema relativo al mancato rispetto di `--no-wait`</span><span class="sxs-lookup"><span data-stu-id="25887-221">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="25887-222">`application-gateway http-settings update`: risoluzione del problema relativo all'impossibilità di disattivare `--connection-draining-timeout`</span><span class="sxs-lookup"><span data-stu-id="25887-222">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="25887-223">Risoluzione del problema relativo all'argomento imprevisto `sa_data_size_kilobyes` della parola chiave con `az network vpn-connection ipsec-policy add`</span><span class="sxs-lookup"><span data-stu-id="25887-223">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="25887-224">Profilo</span><span class="sxs-lookup"><span data-stu-id="25887-224">Profile</span></span>

* <span data-ttu-id="25887-225">`account list`: aggiunta di `--refresh` per la sincronizzazione delle sottoscrizioni più recenti dal server</span><span class="sxs-lookup"><span data-stu-id="25887-225">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="25887-226">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="25887-226">Storage</span></span>

* <span data-ttu-id="25887-227">Abilitazione dell'aggiornamento dell'account di archiviazione con l'identità assegnata dal sistema</span><span class="sxs-lookup"><span data-stu-id="25887-227">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="25887-228">VM</span><span class="sxs-lookup"><span data-stu-id="25887-228">VM</span></span>

* <span data-ttu-id="25887-229">`availability-set`: esposizione del numero di domini di errore in fase di conversione</span><span class="sxs-lookup"><span data-stu-id="25887-229">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="25887-230">Esposizione del comando `list-skus`</span><span class="sxs-lookup"><span data-stu-id="25887-230">Exposed `list-skus` command</span></span>
* <span data-ttu-id="25887-231">Supporto per l'assegnazione di identità senza la creazione di assegnazioni di ruolo</span><span class="sxs-lookup"><span data-stu-id="25887-231">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="25887-232">Applicazione di SKU di archiviazione in fase di collegamento del dischi dati</span><span class="sxs-lookup"><span data-stu-id="25887-232">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="25887-233">Rimozione del nome del disco del sistema operativo predefinito e dello SKU di archiviazione in caso di uso di Managed Disks</span><span class="sxs-lookup"><span data-stu-id="25887-233">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="25887-234">28 luglio 2017</span><span class="sxs-lookup"><span data-stu-id="25887-234">July 28, 2017</span></span>

<span data-ttu-id="25887-235">Versione 2.0.12</span><span class="sxs-lookup"><span data-stu-id="25887-235">Version 2.0.12</span></span>

* <span data-ttu-id="25887-236">Aggiunta di comandi del contenitore</span><span class="sxs-lookup"><span data-stu-id="25887-236">Added container commands</span></span>
* <span data-ttu-id="25887-237">Aggiunta di moduli relativi a fatturazione e consumo</span><span class="sxs-lookup"><span data-stu-id="25887-237">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="25887-238">Core</span><span class="sxs-lookup"><span data-stu-id="25887-238">Core</span></span>

* <span data-ttu-id="25887-239">Restituzione di informazioni di autorizzazioni dell'SDK per entità servizio con certificati</span><span class="sxs-lookup"><span data-stu-id="25887-239">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="25887-240">Risoluzione del problema relativo alle eccezioni nell'avanzamento delle distribuzioni</span><span class="sxs-lookup"><span data-stu-id="25887-240">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="25887-241">Uso dell'endpoint ARM dal cloud corrente per la creazione del client di sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="25887-241">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="25887-242">Miglioramento della gestione simultanea del file clouds.config (#3636)</span><span class="sxs-lookup"><span data-stu-id="25887-242">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="25887-243">Aggiornamento dell'ID della richiesta client per ogni esecuzione del comando</span><span class="sxs-lookup"><span data-stu-id="25887-243">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="25887-244">Creazione dei client di sottoscrizione con il profilo SDK corretto (#3635)</span><span class="sxs-lookup"><span data-stu-id="25887-244">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="25887-245">Creazione di report relativi all'avanzamento per le distribuzioni dei modelli (#3510)</span><span class="sxs-lookup"><span data-stu-id="25887-245">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="25887-246">Aggiunta del supporto per la selezione di campi di output della tabella tramite una query jmespath (#3581)</span><span class="sxs-lookup"><span data-stu-id="25887-246">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="25887-247">Miglioramento della disattivazione dell'audio degli argomenti di analisi e dell'aggiunta di cronologia con gesti (#3434)</span><span class="sxs-lookup"><span data-stu-id="25887-247">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="25887-248">Creazione di client di sottoscrizione con il profilo SDK corretto</span><span class="sxs-lookup"><span data-stu-id="25887-248">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="25887-249">Spostamento di tutti i file di registrazione esistenti nella cartella più recente</span><span class="sxs-lookup"><span data-stu-id="25887-249">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="25887-250">Risoluzione del problema relativo all'idempotenza per la creazione di VM/VMSS (#3586)</span><span class="sxs-lookup"><span data-stu-id="25887-250">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="25887-251">I percorsi dei comandi non rispettano più la distinzione tra maiuscole/minuscole</span><span class="sxs-lookup"><span data-stu-id="25887-251">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="25887-252">Alcuni parametri di tipo booleano non rispettano più la distinzione tra maiuscole/minuscole</span><span class="sxs-lookup"><span data-stu-id="25887-252">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="25887-253">Supporto dell'accesso ad AD FS nel server locale come Azure Stack</span><span class="sxs-lookup"><span data-stu-id="25887-253">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="25887-254">Risoluzione del problema relativo alle operazioni di scrittura simultanee nel file clouds.config (#3255)</span><span class="sxs-lookup"><span data-stu-id="25887-254">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="25887-255">ACR</span><span class="sxs-lookup"><span data-stu-id="25887-255">ACR</span></span>

* <span data-ttu-id="25887-256">Aggiunta del comando `show-usage` per i registri gestiti</span><span class="sxs-lookup"><span data-stu-id="25887-256">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="25887-257">Supporto dell'aggiornamento dello SKU per i registri gestiti</span><span class="sxs-lookup"><span data-stu-id="25887-257">Support SKU update for managed registries</span></span>
* <span data-ttu-id="25887-258">Aggiunta dei registri gestiti con SKU gestito</span><span class="sxs-lookup"><span data-stu-id="25887-258">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="25887-259">Aggiunta di webhook per registri gestiti con modulo di comandi webhook ACR</span><span class="sxs-lookup"><span data-stu-id="25887-259">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="25887-260">Aggiunta dell'autenticazione AAD con il comando di accesso di ACR</span><span class="sxs-lookup"><span data-stu-id="25887-260">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="25887-261">Aggiunta del comando di eliminazione per repository Docker, manifesti e tag</span><span class="sxs-lookup"><span data-stu-id="25887-261">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="25887-262">ACS</span><span class="sxs-lookup"><span data-stu-id="25887-262">ACS</span></span>

* <span data-ttu-id="25887-263">Supporto per l'API versione 2017-07-01</span><span class="sxs-lookup"><span data-stu-id="25887-263">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="25887-264">Servizio app</span><span class="sxs-lookup"><span data-stu-id="25887-264">Appservice</span></span>

* <span data-ttu-id="25887-265">Risoluzione del bug relativo alla mancata restituzione di valori per l'elenco di app Web Linux</span><span class="sxs-lookup"><span data-stu-id="25887-265">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="25887-266">Supporto per il recupero di credenziali da ACR</span><span class="sxs-lookup"><span data-stu-id="25887-266">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="25887-267">Rimozione di tutti i comandi in `appservice web`</span><span class="sxs-lookup"><span data-stu-id="25887-267">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="25887-268">Mascheramento delle password del registro Docker dall'output del comando (#3656)</span><span class="sxs-lookup"><span data-stu-id="25887-268">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="25887-269">Conferma dell'uso del browser predefinito in macOS senza errori (#3623)</span><span class="sxs-lookup"><span data-stu-id="25887-269">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="25887-270">Miglioramento della Guida di `webapp log tail` e `webapp log download` (#3624)</span><span class="sxs-lookup"><span data-stu-id="25887-270">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="25887-271">Esposizione del comando `traffic-routing` per la configurazione del routing statico (#3566)</span><span class="sxs-lookup"><span data-stu-id="25887-271">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="25887-272">Aggiunta di correzioni relative all'affidabilità nella configurazione del controllo del codice sorgente (#3245)</span><span class="sxs-lookup"><span data-stu-id="25887-272">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="25887-273">Rimozione dell'argomento `--node-version` non supportato da `webapp config update` per le app Web Windows.</span><span class="sxs-lookup"><span data-stu-id="25887-273">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="25887-274">Viene usato `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span><span class="sxs-lookup"><span data-stu-id="25887-274">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="25887-275">Batch</span><span class="sxs-lookup"><span data-stu-id="25887-275">Batch</span></span>

* <span data-ttu-id="25887-276">Aggiornamento a Batch SDK 3.0.0 con supporto per le macchine virtuali a priorità bassa nei pool</span><span class="sxs-lookup"><span data-stu-id="25887-276">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="25887-277">Ridenominazione per `pool create` dell'opzione `--target-dedicated` in `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="25887-277">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="25887-278">Aggiunta in `pool create` delle opzioni `--target-low-priority-nodes` e `--application-licenses`</span><span class="sxs-lookup"><span data-stu-id="25887-278">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="25887-279">RETE CDN</span><span class="sxs-lookup"><span data-stu-id="25887-279">CDN</span></span>

* <span data-ttu-id="25887-280">Miglioramento del messaggio di errore per `cdn endpoint list` nel caso in cui il profilo specificato da `--profile-name` non esista.</span><span class="sxs-lookup"><span data-stu-id="25887-280">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="25887-281">Cloud</span><span class="sxs-lookup"><span data-stu-id="25887-281">Cloud</span></span>

* <span data-ttu-id="25887-282">Modifica della versione dell'API dell'endpoint dei metadati del cloud nel formato AAAA-MM-GG</span><span class="sxs-lookup"><span data-stu-id="25887-282">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="25887-283">L'endpoint della raccolta non è obbligatorio</span><span class="sxs-lookup"><span data-stu-id="25887-283">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="25887-284">Supporto per la registrazione del cloud solo con l'endpoint di gestione delle risorse ARM</span><span class="sxs-lookup"><span data-stu-id="25887-284">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="25887-285">Aggiunta di un'opzione per `cloud set` per la scelta del profilo durante la selezione del cloud corrente</span><span class="sxs-lookup"><span data-stu-id="25887-285">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="25887-286">Esposizione di `endpoint_vm_image_alias_doc`</span><span class="sxs-lookup"><span data-stu-id="25887-286">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="25887-287">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="25887-287">CosmosDB</span></span>

* <span data-ttu-id="25887-288">Correzione dell'errore che consente la creazione di una raccolta con una chiave di partizione personalizzata</span><span class="sxs-lookup"><span data-stu-id="25887-288">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="25887-289">Aggiunta di supporto per la durata TTL predefinita della raccolta.</span><span class="sxs-lookup"><span data-stu-id="25887-289">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="25887-290">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="25887-290">Data Lake Analytics</span></span>

* <span data-ttu-id="25887-291">Aggiunta di comandi per la gestione dei criteri di calcolo sotto l'intestazione `dla account compute-policy`</span><span class="sxs-lookup"><span data-stu-id="25887-291">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="25887-292">Aggiunta di `dla job pipeline show`</span><span class="sxs-lookup"><span data-stu-id="25887-292">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="25887-293">Aggiunta di `dla job recurrence list`</span><span class="sxs-lookup"><span data-stu-id="25887-293">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="25887-294">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="25887-294">Data Lake Store</span></span>

* <span data-ttu-id="25887-295">Aggiunta di supporto per la rotazione delle chiavi dell'insieme di credenziali delle chiavi gestito dall'utente in `dls account update`</span><span class="sxs-lookup"><span data-stu-id="25887-295">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="25887-296">Aggiornamento della versione dell'SDK del file system del Data Lake Store sottostante per risolvere un problema di prestazioni</span><span class="sxs-lookup"><span data-stu-id="25887-296">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="25887-297">Aggiunta del comando `dls enable-key-vault`.</span><span class="sxs-lookup"><span data-stu-id="25887-297">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="25887-298">Questo comando prova ad abilitare un'istanza di Key Vault fornita dall'utente per l'uso per la crittografia dei dati in un account Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="25887-298">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="25887-299">Interattività</span><span class="sxs-lookup"><span data-stu-id="25887-299">Interactive</span></span>

* <span data-ttu-id="25887-300">Miglioramento del tempo di avvio tramite i comandi memorizzati nella cache</span><span class="sxs-lookup"><span data-stu-id="25887-300">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="25887-301">Miglioramento della copertura dei test</span><span class="sxs-lookup"><span data-stu-id="25887-301">Increased test coverage</span></span>
* <span data-ttu-id="25887-302">Miglioramento del gesto '?' per consentire anche l'inserimento nel comando successivo</span><span class="sxs-lookup"><span data-stu-id="25887-302">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="25887-303">Risoluzione degli errori relativi all'interattività con il profilo 2017-03-09-profile-preview (#3587)</span><span class="sxs-lookup"><span data-stu-id="25887-303">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="25887-304">Autorizzazione di `--version` come parametro per la modalità interattiva (#3645)</span><span class="sxs-lookup"><span data-stu-id="25887-304">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="25887-305">Interruzione della generazione di errori da parte della modalità interattiva relativi al completamento delle convalide (#3570)</span><span class="sxs-lookup"><span data-stu-id="25887-305">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="25887-306">Creazione di report relativi all'avanzamento per le distribuzioni dei modelli (#3510)</span><span class="sxs-lookup"><span data-stu-id="25887-306">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="25887-307">Aggiunta del flag `--progress`</span><span class="sxs-lookup"><span data-stu-id="25887-307">Added `--progress` flag</span></span>
* <span data-ttu-id="25887-308">Rimozione di `--debug` e `--verbose` dai completamenti</span><span class="sxs-lookup"><span data-stu-id="25887-308">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="25887-309">Rimozione di `interactive` dai completamenti (#3324)</span><span class="sxs-lookup"><span data-stu-id="25887-309">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="25887-310">IoT</span><span class="sxs-lookup"><span data-stu-id="25887-310">IoT</span></span>

* <span data-ttu-id="25887-311">Correzione del problema relativo alla creazione di criteri, che non cancella più i criteri esistenti.</span><span class="sxs-lookup"><span data-stu-id="25887-311">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="25887-312">(#3934)</span><span class="sxs-lookup"><span data-stu-id="25887-312">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="25887-313">Insieme di credenziali delle chiavi</span><span class="sxs-lookup"><span data-stu-id="25887-313">Key vault</span></span>

* <span data-ttu-id="25887-314">Aggiunta di comandi per le funzionalità di ripristino di Key Vault:</span><span class="sxs-lookup"><span data-stu-id="25887-314">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="25887-315">Sottocomandi di `keyvault`: `purge`, `recover`, `keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="25887-315">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="25887-316">Sottocomandi di `keyvault secret`: `backup`, `restore`, `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="25887-316">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="25887-317">Sottocomandi di `keyvault certificate`: `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="25887-317">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="25887-318">Sottocomandi di `keyvault key`: `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="25887-318">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="25887-319">Aggiunta dell'integrazione dell'insieme di credenziali delle chiavi dell'entità servizio (#3133)</span><span class="sxs-lookup"><span data-stu-id="25887-319">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="25887-320">Aggiornamento del piano dati dell'insieme di credenziali delle chiavi a 0.3.2.</span><span class="sxs-lookup"><span data-stu-id="25887-320">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="25887-321">(#3307)</span><span class="sxs-lookup"><span data-stu-id="25887-321">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="25887-322">Lab</span><span class="sxs-lookup"><span data-stu-id="25887-322">Lab</span></span>

* <span data-ttu-id="25887-323">Aggiunta del supporto per la rivendicazione di eventuali macchine virtuali nel laboratorio tramite `az lab vm claim`</span><span class="sxs-lookup"><span data-stu-id="25887-323">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="25887-324">Aggiunta del formattatore dell'output della tabella per `az lab vm list` e `az lab vm show`</span><span class="sxs-lookup"><span data-stu-id="25887-324">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="25887-325">Monitorare</span><span class="sxs-lookup"><span data-stu-id="25887-325">Monitor</span></span>

* <span data-ttu-id="25887-326">Correzione relativa al file del modello con il comando `monitor autoscale-settings get-parameters-template` (#3349)</span><span class="sxs-lookup"><span data-stu-id="25887-326">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="25887-327">Ridenominazione di `monitor alert-rule-incidents list` in `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="25887-327">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="25887-328">Ridenominazione di `monitor alert-rule-incidents show` in `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="25887-328">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="25887-329">Ridenominazione di `monitor metric-defintions list` in `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="25887-329">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="25887-330">Ridenominazione di `monitor alert-rules` in `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="25887-330">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="25887-331">Modifica di `monitor alert create`:</span><span class="sxs-lookup"><span data-stu-id="25887-331">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="25887-332">I sottocomandi `condition` e `action` non accettano più JSON</span><span class="sxs-lookup"><span data-stu-id="25887-332">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="25887-333">Aggiunta di numerosi parametri per la semplificazione del processo di creazione delle regole</span><span class="sxs-lookup"><span data-stu-id="25887-333">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="25887-334">`location` non è più obbligatorio</span><span class="sxs-lookup"><span data-stu-id="25887-334">`location` no longer required</span></span>
  * <span data-ttu-id="25887-335">Aggiunta del supporto di nome ID per la destinazione</span><span class="sxs-lookup"><span data-stu-id="25887-335">Add name and ID support for target</span></span>
  * <span data-ttu-id="25887-336">Rimozione di `--alert-rule-resource-name`</span><span class="sxs-lookup"><span data-stu-id="25887-336">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="25887-337">Ridenominazione di `is-enabled` in `enabled`, non più obbligatorio</span><span class="sxs-lookup"><span data-stu-id="25887-337">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="25887-338">I valori predefiniti di `description` sono ora basati sulla condizione specificata</span><span class="sxs-lookup"><span data-stu-id="25887-338">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="25887-339">Aggiunta di esempi per illustrare in modo più chiaro il nuovo formato</span><span class="sxs-lookup"><span data-stu-id="25887-339">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="25887-340">Supporto di nomi o ID per i comandi `monitor metric`</span><span class="sxs-lookup"><span data-stu-id="25887-340">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="25887-341">Aggiunta di argomenti ed esempi utili a `monitor alert rule update`</span><span class="sxs-lookup"><span data-stu-id="25887-341">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="25887-342">Rete</span><span class="sxs-lookup"><span data-stu-id="25887-342">Network</span></span>

* <span data-ttu-id="25887-343">Aggiunta del comando `list-private-access-services`</span><span class="sxs-lookup"><span data-stu-id="25887-343">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="25887-344">Aggiunta dell'argomento `--private-access-services` a `vnet subnet create` e `vnet subnet update`</span><span class="sxs-lookup"><span data-stu-id="25887-344">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="25887-345">Risoluzione del problema relativo all'esito negativo di `application-gateway redirect-config create`</span><span class="sxs-lookup"><span data-stu-id="25887-345">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="25887-346">Risoluzione del problema relativo al mancato funzionamento di `application-gateway redirect-config update` con `--no-wait`</span><span class="sxs-lookup"><span data-stu-id="25887-346">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="25887-347">Risoluzione del bug relativo all'uso dell'argomento `--servers` con `application-gateway address-pool create` e `application-gateway address-pool update`</span><span class="sxs-lookup"><span data-stu-id="25887-347">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="25887-348">Aggiunta dei comandi `application-gateway redirect-config`</span><span class="sxs-lookup"><span data-stu-id="25887-348">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="25887-349">Aggiunta di comandi ad `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span><span class="sxs-lookup"><span data-stu-id="25887-349">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="25887-350">Aggiunta di comandi ad `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="25887-350">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="25887-351">Aggiunta di argomenti ad `application-gateway http-settings create` e `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span><span class="sxs-lookup"><span data-stu-id="25887-351">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="25887-352">Aggiunta di argomenti ad `application-gateway url-path-map create` e `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="25887-352">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="25887-353">Aggiunta dell'argomento `--redirect-config` a `application-gateway url-path-map rule create`</span><span class="sxs-lookup"><span data-stu-id="25887-353">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="25887-354">Aggiunta del supporto per `--no-wait` a `application-gateway url-path-map rule delete`</span><span class="sxs-lookup"><span data-stu-id="25887-354">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="25887-355">Aggiunta di argomenti ad `application-gateway probe create` e `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="25887-355">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="25887-356">Aggiunta dell'argomento `--redirect-config` a `application-gateway rule create` e `application-gateway rule update`</span><span class="sxs-lookup"><span data-stu-id="25887-356">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="25887-357">Aggiunta del supporto per `--accelerated-networking` a `nic create` e `nic update`</span><span class="sxs-lookup"><span data-stu-id="25887-357">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="25887-358">Rimozione dell'argomento `--internal-dns-name-suffix` da `nic create`</span><span class="sxs-lookup"><span data-stu-id="25887-358">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="25887-359">Aggiunta del supporto per `--dns-servers` a `nic update` e `nic create`: aggiunta del supporto per --dns-servers</span><span class="sxs-lookup"><span data-stu-id="25887-359">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="25887-360">Risoluzione del bug relativo al fatto che `local-gateway create` ignora `--local-address-prefixes`</span><span class="sxs-lookup"><span data-stu-id="25887-360">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="25887-361">Aggiunta del supporto per `--dns-servers` a `vnet update`</span><span class="sxs-lookup"><span data-stu-id="25887-361">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="25887-362">Risoluzione del bug relativo alla creazione di un peering senza filtro delle route con `express-route peering create`</span><span class="sxs-lookup"><span data-stu-id="25887-362">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="25887-363">Risoluzione del bug relativo al mancato funzionamento di `--provider` e `--bandwidth` con `express-route update`</span><span class="sxs-lookup"><span data-stu-id="25887-363">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="25887-364">Risoluzione del bug relativo alla logica delle impostazioni predefinite di `network watcher show-topology`</span><span class="sxs-lookup"><span data-stu-id="25887-364">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="25887-365">Miglioramento della formattazione dell'output per `network list-usages`</span><span class="sxs-lookup"><span data-stu-id="25887-365">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="25887-366">Uso dell'indirizzo IP del front-end predefinito per `application-gateway http-listener create` se ne esiste solo uno</span><span class="sxs-lookup"><span data-stu-id="25887-366">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="25887-367">Uso del pool di indirizzi, delle impostazioni HTTP e del listener HTTP predefiniti per `application-gateway rule create` se ne esiste solo uno</span><span class="sxs-lookup"><span data-stu-id="25887-367">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="25887-368">Uso dell'indirizzo IP del front-end e del pool back-end predefiniti per `lb rule create` se ne esiste solo uno</span><span class="sxs-lookup"><span data-stu-id="25887-368">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="25887-369">Uso dell'indirizzo IP del front-end predefinito per `lb inbound-nat-rule create` se ne esiste solo uno</span><span class="sxs-lookup"><span data-stu-id="25887-369">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="25887-370">Profilo</span><span class="sxs-lookup"><span data-stu-id="25887-370">Profile</span></span>

* <span data-ttu-id="25887-371">Supporto dell'accesso all'interno di una VM con un'identità gestita</span><span class="sxs-lookup"><span data-stu-id="25887-371">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="25887-372">Supporto dell'output per `account show` nel formato di file di autorizzazione di SDK</span><span class="sxs-lookup"><span data-stu-id="25887-372">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="25887-373">Visualizzazione degli avvisi relativi a elementi deprecati quando si usa '--expanded-view'</span><span class="sxs-lookup"><span data-stu-id="25887-373">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="25887-374">Aggiunta del comando `get-access-token` per fornire il token AAD non elaborato</span><span class="sxs-lookup"><span data-stu-id="25887-374">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="25887-375">Supporto dell'accesso con un account utente senza sottoscrizioni associate</span><span class="sxs-lookup"><span data-stu-id="25887-375">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="25887-376">RDBMS</span><span class="sxs-lookup"><span data-stu-id="25887-376">RDBMS</span></span>

* <span data-ttu-id="25887-377">Supporto della creazione di elenchi di server in una sottoscrizione (#3417)</span><span class="sxs-lookup"><span data-stu-id="25887-377">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="25887-378">Risoluzione del problema relativo alla mancata elaborazione di `%s` a causa dell'assenza del valore `% server_type` (#3393)</span><span class="sxs-lookup"><span data-stu-id="25887-378">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="25887-379">Risoluzione del problema relativo alla mappa di origine del documento e aggiunta di un'attività di integrazione continua per la verifica (#3361)</span><span class="sxs-lookup"><span data-stu-id="25887-379">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="25887-380">Risoluzione dei problemi della Guida di MySQL e PostgreSQL (#3369)</span><span class="sxs-lookup"><span data-stu-id="25887-380">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="25887-381">Risorsa</span><span class="sxs-lookup"><span data-stu-id="25887-381">Resource</span></span>

* <span data-ttu-id="25887-382">Miglioramento dei prompt relativi a parametri mancanti per `group deployment create`</span><span class="sxs-lookup"><span data-stu-id="25887-382">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="25887-383">Miglioramento dell'analisi della sintassi di `--parameters KEY=VALUE`</span><span class="sxs-lookup"><span data-stu-id="25887-383">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="25887-384">Risoluzione dei problemi relativi al mancato riconoscimento dei file di parametri di `group deployment create` con la sintassi `@<file>`</span><span class="sxs-lookup"><span data-stu-id="25887-384">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="25887-385">Supporto dell'argomento `--ids` per i comandi `resource` e `managedapp`</span><span class="sxs-lookup"><span data-stu-id="25887-385">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="25887-386">Risoluzione di alcuni messaggi relativi ad analisi ed errori (#3584)</span><span class="sxs-lookup"><span data-stu-id="25887-386">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="25887-387">Risoluzione dei problemi relativi all'analisi di `--resource-type` per consentire al comando `lock` di accettare `<resource-namespace>` e `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="25887-387">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="25887-388">Aggiunta della verifica del parametro per i modelli di collegamenti ai modelli (#3629)</span><span class="sxs-lookup"><span data-stu-id="25887-388">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="25887-389">Aggiunta del supporto per specificare i parametri di distribuzione tramite la sintassi `KEY=VALUE`</span><span class="sxs-lookup"><span data-stu-id="25887-389">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="25887-390">Ruolo</span><span class="sxs-lookup"><span data-stu-id="25887-390">Role</span></span>

* <span data-ttu-id="25887-391">Supporto dell'output nel formato del file di autenticazione di SDK per `create-for-rbac`</span><span class="sxs-lookup"><span data-stu-id="25887-391">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="25887-392">Pulizia delle assegnazioni di ruolo e dell'applicazione AAD correlata in caso di eliminazione di un'entità servizio (#3610)</span><span class="sxs-lookup"><span data-stu-id="25887-392">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="25887-393">Inclusione del formato dell'ora negli argomenti `app create` per le descrizioni `--start-date` ed `--end-date`</span><span class="sxs-lookup"><span data-stu-id="25887-393">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="25887-394">Visualizzazione degli avvisi relativi a elementi deprecati quando si usa `--expanded-view`</span><span class="sxs-lookup"><span data-stu-id="25887-394">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="25887-395">Aggiunta dell'integrazione dell'insieme di credenziali delle chiavi ai comandi `create-for-rbac` e `reset-credentials`</span><span class="sxs-lookup"><span data-stu-id="25887-395">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="25887-396">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="25887-396">Service Fabric</span></span>
* <span data-ttu-id="25887-397">Risoluzione di un problema relativo al troncamento dei file di grandi dimensioni nelle applicazioni in fase di caricamento (#3666)</span><span class="sxs-lookup"><span data-stu-id="25887-397">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="25887-398">Aggiunta dei test per i comandi di Service Fabric (#3424)</span><span class="sxs-lookup"><span data-stu-id="25887-398">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="25887-399">Risoluzione dei problemi di numerosi comandi di Service Fabric (#3234)</span><span class="sxs-lookup"><span data-stu-id="25887-399">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="25887-400">SQL</span><span class="sxs-lookup"><span data-stu-id="25887-400">SQL</span></span>

* <span data-ttu-id="25887-401">Rimozione del parametro `sql server create` `--identity` non funzionante</span><span class="sxs-lookup"><span data-stu-id="25887-401">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="25887-402">Rimozione dei valori della password dall'output dei comandi `sql server create` e `sql server update`</span><span class="sxs-lookup"><span data-stu-id="25887-402">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="25887-403">Aggiunta dei comandi `sql db list-editions` e `sql elastic-pool list-editions`</span><span class="sxs-lookup"><span data-stu-id="25887-403">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="25887-404">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="25887-404">Storage</span></span>

* <span data-ttu-id="25887-405">Rimozione dell'opzione `--marker` dai comandi `storage blob list`, `storage container list` e `storage share list` (#3745)</span><span class="sxs-lookup"><span data-stu-id="25887-405">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="25887-406">Abilitazione della creazione di un account di archiviazione solo HTTPS</span><span class="sxs-lookup"><span data-stu-id="25887-406">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="25887-407">Aggiornamento delle metriche di archiviazione, della registrazione e dei comandi CORS (#3495)</span><span class="sxs-lookup"><span data-stu-id="25887-407">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="25887-408">Nuova formulazione del messaggio di eccezione dall'aggiunta di CORS (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="25887-408">Rephrased exception message from CORS add (#3638) (#3362)</span></span>  
* <span data-ttu-id="25887-409">Conversione del generatore in elenco in modalità di test controllato del comando Batch di download (#3592)</span><span class="sxs-lookup"><span data-stu-id="25887-409">Converted generator to a list in download batch command dry run mode (#3592)</span></span> 
* <span data-ttu-id="25887-410">Risoluzione del problema relativo al test controllato di Batch del download di BLOB (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="25887-410">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="25887-411">VM</span><span class="sxs-lookup"><span data-stu-id="25887-411">VM</span></span>

* <span data-ttu-id="25887-412">Supporto per la configurazione di nsg</span><span class="sxs-lookup"><span data-stu-id="25887-412">Support configuring nsg</span></span>
* <span data-ttu-id="25887-413">Risoluzione di un bug relativo alla configurazione non corretta del server DNS</span><span class="sxs-lookup"><span data-stu-id="25887-413">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="25887-414">Supporto per le identità del servizio gestito</span><span class="sxs-lookup"><span data-stu-id="25887-414">Support managed service identities</span></span>
* <span data-ttu-id="25887-415">Risoluzione del problema relativo al fatto che `cmss create` con un servizio di bilanciamento del carico esistente richiede `--backend-pool-name`.</span><span class="sxs-lookup"><span data-stu-id="25887-415">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="25887-416">I dischi dati creati con LUN `vm image create` iniziano con 0</span><span class="sxs-lookup"><span data-stu-id="25887-416">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="25887-417">10 maggio 2017</span><span class="sxs-lookup"><span data-stu-id="25887-417">May 10, 2017</span></span>

<span data-ttu-id="25887-418">Versione 2.0.6</span><span class="sxs-lookup"><span data-stu-id="25887-418">Version 2.0.6</span></span>

* <span data-ttu-id="25887-419">documentdb rinominato come cosmosdb</span><span class="sxs-lookup"><span data-stu-id="25887-419">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="25887-420">Aggiunge rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="25887-420">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="25887-421">Include i moduli di Data Lake Store e Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="25887-421">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="25887-422">Include i moduli di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="25887-422">Include Cognitive Services module.</span></span>
* <span data-ttu-id="25887-423">Include i moduli di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="25887-423">Include Service Fabric module.</span></span>
* <span data-ttu-id="25887-424">Include i moduli interattivi e rinomina az-shell.</span><span class="sxs-lookup"><span data-stu-id="25887-424">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="25887-425">Aggiunge il supporto per i comandi CDN.</span><span class="sxs-lookup"><span data-stu-id="25887-425">Add support for CDN commands.</span></span>
* <span data-ttu-id="25887-426">Rimuove il modulo del contenitore.</span><span class="sxs-lookup"><span data-stu-id="25887-426">Remove Container module.</span></span>
* <span data-ttu-id="25887-427">Aggiunge "az -v" come collegamento per "az -- version" ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="25887-427">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="25887-428">Migliora le prestazioni di carico del pacchetto e l'esecuzione del comando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="25887-428">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="25887-429">Core</span><span class="sxs-lookup"><span data-stu-id="25887-429">Core</span></span>

* <span data-ttu-id="25887-430">core: consente di acquisire le eccezioni causate dall'annullamento della registrazione e dalla registrazione automatica del provider</span><span class="sxs-lookup"><span data-stu-id="25887-430">core: capture exceptions caused by unregistered provider and auto-register it</span></span>   
* <span data-ttu-id="25887-431">perf: consente di mantenere la cache del token ADAL in memoria fino alla chiusura di processo ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="25887-431">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="25887-432">Consente di correggere i byte restituiti da impronta digitale hex -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="25887-432">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="25887-433">Download dei certificati del Key Vault e dell'integrazione AAD SP migliorati ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="25887-433">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="25887-434">Aggiunge il percorso di Python per "az —version" ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="25887-434">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="25887-435">login: supporta l'accesso quando non sono presenti sottoscrizioni ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="25887-435">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="25887-436">core: consente di correggere un errore quando si effettua l'accesso usando un'entità servizio due volte ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="25887-436">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="25887-437">core: consente al percorso del file accessTokens.json di poter essere configurato tramite un env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="25887-437">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="25887-438">core: consente ai valori predefiniti configurati di essere applicati solo ad argomenti facoltativi ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="25887-438">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="25887-439">core: prestazioni migliorate</span><span class="sxs-lookup"><span data-stu-id="25887-439">core: Improved performance</span></span>
* <span data-ttu-id="25887-440">core: certificati CA personalizzati: supporta l'impostazione della variabile di ambiente REQUESTS_CA_BUNDLE</span><span class="sxs-lookup"><span data-stu-id="25887-440">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="25887-441">core: configurazione del cloud: usa l'endpoint "gestione risorse" se l'endpoint "gestione" non è impostato</span><span class="sxs-lookup"><span data-stu-id="25887-441">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="25887-442">ACS</span><span class="sxs-lookup"><span data-stu-id="25887-442">ACS</span></span>

* <span data-ttu-id="25887-443">consente di correggere il conteggio di master e agenti affinché sia un numero intero anziché una stringa</span><span class="sxs-lookup"><span data-stu-id="25887-443">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="25887-444">espone "az acs create --no-wait" e "az acs wait" alla creazione asincrona</span><span class="sxs-lookup"><span data-stu-id="25887-444">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="25887-445">espone "az acs create --validate" alle convalide del test controllato</span><span class="sxs-lookup"><span data-stu-id="25887-445">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="25887-446">rimuove il profilo di Windows prima di INSERIRE la chiamata del comando scale ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="25887-446">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="25887-447">AppService</span><span class="sxs-lookup"><span data-stu-id="25887-447">AppService</span></span>

* <span data-ttu-id="25887-448">functionapp: aggiunge supporti functionapp completi, tra cui create, show, list, delete, hostname, ssl e così via</span><span class="sxs-lookup"><span data-stu-id="25887-448">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="25887-449">Aggiunta di servizi di Team (vsts) come opzione di consegna continua a "appservice web source-control config"</span><span class="sxs-lookup"><span data-stu-id="25887-449">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="25887-450">Consente di creare "az webapp" per sostituire "az appservice web". Per la compatibilità con le versioni precedenti, "az appservice web" viene mantenuta per 2 versioni</span><span class="sxs-lookup"><span data-stu-id="25887-450">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="25887-451">Espone gli argomenti per configurare la distribuzione e "stack di runtime" su webapp</span><span class="sxs-lookup"><span data-stu-id="25887-451">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="25887-452">Espone "webapp list-runtimes"</span><span class="sxs-lookup"><span data-stu-id="25887-452">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="25887-453">supporta le stringhe di connessione per la configurazione ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="25887-453">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="25887-454">supporta lo scambio di slot con anteprima</span><span class="sxs-lookup"><span data-stu-id="25887-454">support slot swap with preview</span></span>
* <span data-ttu-id="25887-455">Errori di polacco neii comandi appservice ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="25887-455">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="25887-456">Usa il gruppo di risorse del piano del servizio app per le operazioni cert ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="25887-456">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="25887-457">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="25887-457">CosmosDB</span></span>

* <span data-ttu-id="25887-458">Rinomina il modulo documentdb in cosmosdb.</span><span class="sxs-lookup"><span data-stu-id="25887-458">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="25887-459">Aggiunto il supporto per le API del piano di dati documentdb: gestione di database e raccolta</span><span class="sxs-lookup"><span data-stu-id="25887-459">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="25887-460">Aggiunto il supporto per abilitare il failover automatico negli account del database</span><span class="sxs-lookup"><span data-stu-id="25887-460">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="25887-461">Aggiunto il supporto per nuovi criteri di coerenza ConsistentPrefix</span><span class="sxs-lookup"><span data-stu-id="25887-461">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="25887-462">Analisi Data Lake</span><span class="sxs-lookup"><span data-stu-id="25887-462">Data Lake Analytics</span></span>

* <span data-ttu-id="25887-463">Consente di correggere un bug in cui il filtro dei risultati e lo stato degli elenchi del processo genererebbe un errore.</span><span class="sxs-lookup"><span data-stu-id="25887-463">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="25887-464">Aggiunge il supporto per il tipo di elementi del nuovo catalogo: pacchetto.</span><span class="sxs-lookup"><span data-stu-id="25887-464">Add support for new catalog item type: package.</span></span> <span data-ttu-id="25887-465">accessibili tramite: `az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="25887-465">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="25887-466">È possibile elencare gli elementi seguenti del catalogo da un database, senza necessità delle specifiche dello schema:</span><span class="sxs-lookup"><span data-stu-id="25887-466">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="25887-467">Tabella</span><span class="sxs-lookup"><span data-stu-id="25887-467">Table</span></span>
  * <span data-ttu-id="25887-468">Funzione con valori di tabella</span><span class="sxs-lookup"><span data-stu-id="25887-468">Table valued function</span></span>
  * <span data-ttu-id="25887-469">Visualizza</span><span class="sxs-lookup"><span data-stu-id="25887-469">View</span></span>
  * <span data-ttu-id="25887-470">Statistiche tabelle.</span><span class="sxs-lookup"><span data-stu-id="25887-470">Table Statistics.</span></span> <span data-ttu-id="25887-471">Questo elemento può essere elencato anche con uno schema, ma senza specificare un nome di tabella.</span><span class="sxs-lookup"><span data-stu-id="25887-471">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="25887-472">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="25887-472">Data Lake Store</span></span>

* <span data-ttu-id="25887-473">Aggiorna la versione dell'SDK del file system sottostante, che offre un supporto migliore per la gestione di scenari con limitazione lato server.</span><span class="sxs-lookup"><span data-stu-id="25887-473">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="25887-474">Migliora le prestazioni di carico del pacchetto e l'esecuzione del comando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="25887-474">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="25887-475">guida mancate per la presentazione di accesso.</span><span class="sxs-lookup"><span data-stu-id="25887-475">missed help for access show.</span></span> <span data-ttu-id="25887-476">aggiunta.</span><span class="sxs-lookup"><span data-stu-id="25887-476">adding it.</span></span> <span data-ttu-id="25887-477">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="25887-477">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="25887-478">Find</span><span class="sxs-lookup"><span data-stu-id="25887-478">Find</span></span>

* <span data-ttu-id="25887-479">migliora i risultati di ricerca e consente di controllare le versioni dell'indice di ricerca</span><span class="sxs-lookup"><span data-stu-id="25887-479">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="25887-480">Insieme di credenziali delle chiavi</span><span class="sxs-lookup"><span data-stu-id="25887-480">KeyVault</span></span>

* <span data-ttu-id="25887-481">BC: `az keyvault certificate download` modifica -e dalla stringa o dal binario in PEM o DER per rappresentare meglio le opzioni</span><span class="sxs-lookup"><span data-stu-id="25887-481">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="25887-482">BC: rimuove --expires e --not-before da `keyvault certificate create` poiché questi parametri non sono supportati dal servizio.</span><span class="sxs-lookup"><span data-stu-id="25887-482">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="25887-483">Aggiunge il parametro --validity a `keyvault certificate create` per eseguire l'override in modo selettivo del valore in --policy</span><span class="sxs-lookup"><span data-stu-id="25887-483">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="25887-484">Consente di risolvere i problemi in `keyvault certificate get-default-policy` laddove sono stati esposti "expires" e "not_before", ma non "validity_in_months".</span><span class="sxs-lookup"><span data-stu-id="25887-484">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="25887-485">correzione di keyvault per l'importazione di pem e pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="25887-485">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="25887-486">Lab</span><span class="sxs-lookup"><span data-stu-id="25887-486">Lab</span></span>

* <span data-ttu-id="25887-487">Aggiunta dei comandi create, show, delete e list per l'ambiente nel laboratorio.</span><span class="sxs-lookup"><span data-stu-id="25887-487">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="25887-488">Aggiunta di comandi show e list per visualizzare i modelli ARM nel laboratorio.</span><span class="sxs-lookup"><span data-stu-id="25887-488">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="25887-489">Aggiunta del flag --environment in `az lab vm list` per filtrare le macchine virtuali in base all'ambiente nel laboratorio.</span><span class="sxs-lookup"><span data-stu-id="25887-489">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="25887-490">Aggiunge il comando di convenienza `az lab formula export-artifacts` per esportare lo scaffolding dell'elemento all'interno della formula di Lab.</span><span class="sxs-lookup"><span data-stu-id="25887-490">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="25887-491">Aggiunge i comandi per gestire i segreti in Lab.</span><span class="sxs-lookup"><span data-stu-id="25887-491">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="25887-492">Monitorare</span><span class="sxs-lookup"><span data-stu-id="25887-492">Monitor</span></span>

* <span data-ttu-id="25887-493">Correzione di bug: modellazione di `--actions` in `az alert-rules create` per usare una stringa JSON ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="25887-493">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="25887-494">Correzione di bug: diagnostic settings create non accetta i registri/le metriche dei comandi show ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="25887-494">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="25887-495">Rete</span><span class="sxs-lookup"><span data-stu-id="25887-495">Network</span></span>

* <span data-ttu-id="25887-496">Aggiunge il comando `network watcher test-connectivity`.</span><span class="sxs-lookup"><span data-stu-id="25887-496">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="25887-497">Aggiunge il supporto per il parametro `--filters` per `network watcher packet-capture create`.</span><span class="sxs-lookup"><span data-stu-id="25887-497">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="25887-498">Aggiunge il supporto per lo svuotamento della connessione del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="25887-498">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="25887-499">Aggiunge il supporto per la configurazione dell'insieme di regole WAF del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="25887-499">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="25887-500">Aggiunge il supporto per le regole e i filtri di route ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="25887-500">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="25887-501">Aggiunge il supporto per il routing geografico di TrafficManager.</span><span class="sxs-lookup"><span data-stu-id="25887-501">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="25887-502">Aggiunge il supporto per i selettori di traffico basati su criteri di connessione VPN.</span><span class="sxs-lookup"><span data-stu-id="25887-502">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="25887-503">Aggiunge il supporto per i criteri IPSec della connessione VPN.</span><span class="sxs-lookup"><span data-stu-id="25887-503">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="25887-504">Correzione di bug con `vpn-connection create` quando si usano i parametri `--no-wait` o `--validate`.</span><span class="sxs-lookup"><span data-stu-id="25887-504">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="25887-505">Aggiunge il supporto per i gateway di rete virtuale attivo/attivo</span><span class="sxs-lookup"><span data-stu-id="25887-505">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="25887-506">Rimuove i valori null i valori dall'output dei comandi `network vpn-connection list/show`.</span><span class="sxs-lookup"><span data-stu-id="25887-506">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="25887-507">BC: correzione di bug nell'output di `vpn-connection create`</span><span class="sxs-lookup"><span data-stu-id="25887-507">BC: Fix bug in the output of `vpn-connection create`</span></span> 
* <span data-ttu-id="25887-508">Corregge i bug in cui l'argomento "--key-length" di "vpn-connection create"' non è stato analizzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="25887-508">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="25887-509">Corregge i bug in `dns zone import` in cui i record non sono stati importati correttamente.</span><span class="sxs-lookup"><span data-stu-id="25887-509">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="25887-510">Corregge i bug laddove `traffic-manager endpoint update` non funzionava.</span><span class="sxs-lookup"><span data-stu-id="25887-510">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="25887-511">Aggiunge i comandi di anteprima "network watcher".</span><span class="sxs-lookup"><span data-stu-id="25887-511">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="25887-512">Profilo</span><span class="sxs-lookup"><span data-stu-id="25887-512">Profile</span></span>

* <span data-ttu-id="25887-513">Supporta l'accesso quando non sono state trovate sottoscrizioni ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="25887-513">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="25887-514">Supporta l'abbreviazione del nome dei parametri in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="25887-514">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="25887-515">Redis</span><span class="sxs-lookup"><span data-stu-id="25887-515">Redis</span></span>

* <span data-ttu-id="25887-516">Aggiunta del comando update che offre anche la possibilità di passare alla cache Redis</span><span class="sxs-lookup"><span data-stu-id="25887-516">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="25887-517">Il comando "update-settings" viene deprecato.</span><span class="sxs-lookup"><span data-stu-id="25887-517">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="25887-518">Risorsa</span><span class="sxs-lookup"><span data-stu-id="25887-518">Resource</span></span>

* <span data-ttu-id="25887-519">Aggiunge i comandi managedapp e managedapp definition ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="25887-519">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="25887-520">Supporta i comandi "provider operation" ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="25887-520">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="25887-521">Supporta la creazione della risorsa generica ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="25887-521">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="25887-522">Corregge l'analisi della risorsa e la ricerca della versione API.</span><span class="sxs-lookup"><span data-stu-id="25887-522">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="25887-523">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="25887-523">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="25887-524">Aggiunge docs ad az lock update.</span><span class="sxs-lookup"><span data-stu-id="25887-524">Add docs for az lock update.</span></span> <span data-ttu-id="25887-525">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="25887-525">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="25887-526">Genera un errore se si tenta di elencare le risorse per un gruppo che non esiste.</span><span class="sxs-lookup"><span data-stu-id="25887-526">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="25887-527">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="25887-527">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="25887-528">[Compute] Risolve i problemi con l'aggiornamento dei set di disponibilità VMSS e della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="25887-528">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="25887-529">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="25887-529">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="25887-530">Correzione della creazione e dell'eliminazione del blocco se parent-resource-path è Nessuno ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="25887-530">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="25887-531">Ruolo</span><span class="sxs-lookup"><span data-stu-id="25887-531">Role</span></span>

* <span data-ttu-id="25887-532">create-for-rbac: assicura che la data di fine di SP non superi la data di scadenza del certificato ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="25887-532">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="25887-533">RBAC: aggiunge il supporto completo ad "ad group" ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="25887-533">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="25887-534">role: corregge i problemi in role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="25887-534">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="25887-535">create-for-rbac: garantisce che venga presa la password indicata</span><span class="sxs-lookup"><span data-stu-id="25887-535">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="25887-536">SQL</span><span class="sxs-lookup"><span data-stu-id="25887-536">SQL</span></span>

* <span data-ttu-id="25887-537">Aggiunti i comandi az sql server list-usages e az sql db list-usages.</span><span class="sxs-lookup"><span data-stu-id="25887-537">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="25887-538">SQL: possibilità di connettersi direttamente al provider di risorse ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="25887-538">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="25887-539">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="25887-539">Storage</span></span>

* <span data-ttu-id="25887-540">Percorso predefinito al percorso del gruppo di risorse per `storage account create`.</span><span class="sxs-lookup"><span data-stu-id="25887-540">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="25887-541">Aggiunge il supporto per la copia di BLOB incrementale</span><span class="sxs-lookup"><span data-stu-id="25887-541">Add support for incremental blob copy</span></span>
* <span data-ttu-id="25887-542">Aggiunge il supporto per il upload di BLOB in blocchi di grandi dimensioni</span><span class="sxs-lookup"><span data-stu-id="25887-542">Add support for large block blob upload</span></span>
* <span data-ttu-id="25887-543">Modifica le dimensioni del blocco in 100 MB quando il file da caricare supera i 200 GB</span><span class="sxs-lookup"><span data-stu-id="25887-543">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="25887-544">VM</span><span class="sxs-lookup"><span data-stu-id="25887-544">VM</span></span>

* <span data-ttu-id="25887-545">avail-set: rende facoltativo il conteggio del dominio UD&FD</span><span class="sxs-lookup"><span data-stu-id="25887-545">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="25887-546">note: comandi della VM nei cloud sovrani. Evitare le funzionalità correlate al disco gestito, tra cui:</span><span class="sxs-lookup"><span data-stu-id="25887-546">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="25887-547">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="25887-547">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="25887-548">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="25887-548">az vm/vmss disk</span></span>
  3. <span data-ttu-id="25887-549">All'interno di "az vm/vmss create" usare "—use-unmanaged-disk" per evitare che il disco gestito. Funziona anche con altri comandi</span><span class="sxs-lookup"><span data-stu-id="25887-549">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="25887-550">vm/vmss: migliora il testo di avviso quando si generano coppie di chiavi SSH</span><span class="sxs-lookup"><span data-stu-id="25887-550">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="25887-551">vm/vmss: supporta la creazione da un'immagine del marketplace che richiede informazioni sul piano ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="25887-551">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="25887-552">3 aprile 2017</span><span class="sxs-lookup"><span data-stu-id="25887-552">April 3, 2017</span></span>

<span data-ttu-id="25887-553">Versione 2.0.2</span><span class="sxs-lookup"><span data-stu-id="25887-553">Version 2.0.2</span></span>

<span data-ttu-id="25887-554">In questa versione sono stati rilasciati i componenti ACR, Batch, KeyVault e SQL.</span><span class="sxs-lookup"><span data-stu-id="25887-554">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="25887-555">Core</span><span class="sxs-lookup"><span data-stu-id="25887-555">Core</span></span>

* <span data-ttu-id="25887-556">Aggiunta dei moduli acr, lab, monitor e find all'elenco predefinito.</span><span class="sxs-lookup"><span data-stu-id="25887-556">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="25887-557">Login: esclusione del tenant errato ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="25887-557">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="25887-558">login: impostazione della sottoscrizione predefinita su una con lo stato "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="25887-558">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="25887-559">Aggiunta di comandi wait e di supporto per --no-wait a più comandi ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="25887-559">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="25887-560">core: supporto per accesso mediante entità servizio con un certificato ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="25887-560">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="25887-561">Aggiunta della richiesta dei parametri di modello mancanti.</span><span class="sxs-lookup"><span data-stu-id="25887-561">Add prompting for missing template parameters.</span></span> <span data-ttu-id="25887-562">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="25887-562">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="25887-563">Supporto per l'impostazione di valori predefiniti per argomenti comuni ad esempio gruppo di risorse predefinito, Web predefinito, macchina virtuale predefinita</span><span class="sxs-lookup"><span data-stu-id="25887-563">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="25887-564">Supporto per l'accesso al tenant specifico</span><span class="sxs-lookup"><span data-stu-id="25887-564">Support login to specific tenant</span></span>
 
### <a name="acs"></a><span data-ttu-id="25887-565">ACS</span><span class="sxs-lookup"><span data-stu-id="25887-565">ACS</span></span>

* <span data-ttu-id="25887-566">[ACS] Aggiunta di supporto per la configurazione di un cluster ACS predefinito ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="25887-566">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="25887-567">Aggiunta di supporto per la richiesta di password della chiave SSH.</span><span class="sxs-lookup"><span data-stu-id="25887-567">Add support for ssh key password prompting.</span></span> <span data-ttu-id="25887-568">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="25887-568">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="25887-569">Aggiunta di supporto per i cluster Windows.</span><span class="sxs-lookup"><span data-stu-id="25887-569">Add support for windows clusters.</span></span> <span data-ttu-id="25887-570">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="25887-570">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="25887-571">Passaggio dal ruolo Proprietario al ruolo Collaboratore.</span><span class="sxs-lookup"><span data-stu-id="25887-571">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="25887-572">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="25887-572">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>
 
### <a name="appservice"></a><span data-ttu-id="25887-573">AppService</span><span class="sxs-lookup"><span data-stu-id="25887-573">AppService</span></span>

* <span data-ttu-id="25887-574">appservice: supporto per ottenere l'indirizzo IP esterno usato per i record DNS A ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="25887-574">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="25887-575">appservice: supporto dell'associazione di certificati jolly ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="25887-575">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="25887-576">appservice: supporto dell'elenco di profili di pubblicazione ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="25887-576">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="25887-577">AppService - attivazione della sincronizzazione del controllo dopo la configurazione ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="25887-577">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>
 
### <a name="datalake"></a><span data-ttu-id="25887-578">DataLake</span><span class="sxs-lookup"><span data-stu-id="25887-578">DataLake</span></span>

* <span data-ttu-id="25887-579">Versione iniziale del modulo Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="25887-579">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="25887-580">Versione iniziale del modulo Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="25887-580">Initial release of Data Lake Store module.</span></span>
 
### <a name="docuemntdb"></a><span data-ttu-id="25887-581">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="25887-581">DocuemntDB</span></span>

* <span data-ttu-id="25887-582">DocumentDB: aggiunta di supporto per l'elenco di stringhe di connessione ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="25887-582">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="25887-583">VM</span><span class="sxs-lookup"><span data-stu-id="25887-583">VM</span></span>

* <span data-ttu-id="25887-584">[Compute] Aggiunta di supporto per AppGateway alla creazione di set di scalabilità di macchine virtuali ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="25887-584">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="25887-585">[VM/VMSS] Miglioramento del supporto per memorizzazione nella cache del disco ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="25887-585">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="25887-586">VM/VMSS: inclusione di logica di convalida credenziali usata dal portale ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="25887-586">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="25887-587">Aggiunta di comandi wait e di supporto per --no-wait ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="25887-587">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="25887-588">Virtual machine scale set: supporto * per elencare le visualizzazioni di istanza tra le macchine virtuali ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="25887-588">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="25887-589">Aggiunta di --secrets per la macchina virtuale e il set di scalabilità di macchine virtuali ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="25887-589">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="25887-590">Consentita la creazione di macchine virtuali con disco rigido virtuale specializzato ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="25887-590">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="25887-591">27 febbraio 2017</span><span class="sxs-lookup"><span data-stu-id="25887-591">February 27, 2017</span></span>

<span data-ttu-id="25887-592">Versione 2.0.0</span><span class="sxs-lookup"><span data-stu-id="25887-592">Version 2.0.0</span></span>

<span data-ttu-id="25887-593">Questa versione dell'interfaccia della riga di comando di Azure 2.0 è la prima versione disponibile a livello generale.</span><span class="sxs-lookup"><span data-stu-id="25887-593">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="25887-594">La disponibilità generale si applica ai moduli comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="25887-594">General availability applies to these command modules:</span></span>
- <span data-ttu-id="25887-595">Servizio contenitore (acs)</span><span class="sxs-lookup"><span data-stu-id="25887-595">Container Service (acs)</span></span>
- <span data-ttu-id="25887-596">Compute (inclusi Resource Manager, macchina virtuale, set di scalabilità di macchine virtuali, Managed Disks)</span><span class="sxs-lookup"><span data-stu-id="25887-596">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="25887-597">Rete</span><span class="sxs-lookup"><span data-stu-id="25887-597">Networking</span></span>
- <span data-ttu-id="25887-598">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="25887-598">Storage</span></span>

<span data-ttu-id="25887-599">Questi moduli comandi possono essere usati nella produzione e sono supportati dal contratto di servizio Microsoft standard.</span><span class="sxs-lookup"><span data-stu-id="25887-599">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="25887-600">È possibile segnalare i problemi direttamente al supporto tecnico Microsoft o tramite l'[elenco di problemi github](https://github.com/azure/azure-cli/issues/).</span><span class="sxs-lookup"><span data-stu-id="25887-600">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="25887-601">È possibile porre domande su [StackOverflow usando il tag azure-cli](http://stackoverflow.com/questions/tagged/azure-cli) o contattare il team del prodotto all'indirizzo [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). È possibile fornire commenti e suggerimenti dalla riga di comando con il comando `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="25887-601">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="25887-602">I comandi in questi moduli sono stabili e non si prevede che la sintassi cambi nei prossimi rilasci di questa versione dell'interfaccia della riga di comando di Azure.</span><span class="sxs-lookup"><span data-stu-id="25887-602">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="25887-603">Per verificare la versione dell'interfaccia della riga di comando, usare `az --version`.</span><span class="sxs-lookup"><span data-stu-id="25887-603">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="25887-604">L'output elenca la versione dell'interfaccia della riga di comando stessa (2.0.0 in questo rilascio), i singoli moduli comandi e le versioni di Python e GCC in uso.</span><span class="sxs-lookup"><span data-stu-id="25887-604">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="25887-605">Alcuni dei moduli del comando presentano un suffisso "b*n*" o "rc*n*".</span><span class="sxs-lookup"><span data-stu-id="25887-605">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="25887-606">Questi moduli comandi sono ancora in fase di anteprima e saranno disponibili a livello generale in futuro.</span><span class="sxs-lookup"><span data-stu-id="25887-606">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="25887-607">Sono anche disponibili build di anteprima notturne dell'interfaccia della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="25887-607">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="25887-608">Per informazioni, vedere le istruzioni su come [ottenere le build notturne](https://github.com/Azure/azure-cli#nightly-builds) e le istruzioni sull'[impostazione per gli sviluppatori e sul codice per i collaboratori](https://github.com/Azure/azure-cli#developer-setup).</span><span class="sxs-lookup"><span data-stu-id="25887-608">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="25887-609">È possibile segnalare problemi relative alle build di anteprima notturne nei seguenti modi:</span><span class="sxs-lookup"><span data-stu-id="25887-609">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="25887-610">Segnalare i problemi tramite l'[elenco di problemi github](https://github.com/azure/azure-cli/issues/)</span><span class="sxs-lookup"><span data-stu-id="25887-610">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="25887-611">Contattare il tema del prodotto all'indirizzo [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="25887-611">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="25887-612">Fornire commenti e suggerimenti dalla riga di comando con il comando `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="25887-612">Provide feedback from the command line with the `az feedback` command.</span></span>

