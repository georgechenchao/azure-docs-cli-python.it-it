---
title: Risultati del comando query con l&quot;interfaccia della riga di comando di Azure 2.0
description: Usare --query per eseguire query JMESPath sull&quot;output dei comandi dell&quot;interfaccia della riga di comando di Azure 2.0.
keywords: Interfaccia della riga di comando di Azure 2.0, JMESPath, query, Linux, Mac, Windows, OS X
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 5979acc5-21a5-41e2-a4b6-3183bfe6aa22
ms.openlocfilehash: 23c743210ccc506935f6e78489ca0df2b99d46a1
ms.sourcegitcommit: 4fd631a58cf19c494162510d073fbbbdf0524d16
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2017
---
# <a name="using-jmespath-queries-with-azure-cli-20"></a><span data-ttu-id="5fd8f-104">Uso di query JMESPath con l'interfaccia della riga di comando di Azure 2.0</span><span class="sxs-lookup"><span data-stu-id="5fd8f-104">Using JMESPath queries with Azure CLI 2.0</span></span>

<span data-ttu-id="5fd8f-105">L'interfaccia della riga di comando di Azure 2.0 usa il parametro `--query` per eseguire una [query JMESPath](http://jmespath.org) sui risultati del comando `az`.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-105">The Azure CLI 2.0 uses the `--query` parameter to execute a [JMESPath query](http://jmespath.org) on the results of your `az` command.</span></span> <span data-ttu-id="5fd8f-106">JMESPath è un linguaggio di query avanzato per output JSON.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-106">JMESPath is a powerful query language for JSON outputs.</span></span>  <span data-ttu-id="5fd8f-107">Se non si ha familiarità con le query JMESPath è disponibile un'esercitazione in [JMESPath.org/tutorial](http:/JMESPath.org/tutorial.html).</span><span class="sxs-lookup"><span data-stu-id="5fd8f-107">If you are unfamiliar with JMESPath queries you can find a tutorial at [JMESPath.org/tutorial](http:/JMESPath.org/tutorial.html).</span></span>

<span data-ttu-id="5fd8f-108">Il parametro `Query` è supportato da ogni tipo di risorsa (servizi contenitore, app Web, macchine virtuali e così via) nell'interfaccia della riga di comando di Azure 2.0 e può essere usato per vari scopi diversi.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-108">`Query` parameter is supported by every resource type (Container Services, Web Apps, VM, etc.) within Azure CLI 2.0 and can be used for various different purposes.</span></span>  <span data-ttu-id="5fd8f-109">Di seguito sono riportati alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-109">We have listed several examples below.</span></span>

## <a name="selecting-simple-properties"></a><span data-ttu-id="5fd8f-110">Selezione di proprietà semplici</span><span class="sxs-lookup"><span data-stu-id="5fd8f-110">Selecting simple properties</span></span>

<span data-ttu-id="5fd8f-111">Il comando `list` semplice con il formato di output `table` restituisce un set curato delle proprietà semplici più comuni per ogni tipo di risorsa in un formato tabulare di facile lettura.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-111">The simple `list` command with `table` output format returns a curated set of most common, simple properties for each resource type in an easy-to-read tabular format.</span></span>

```azurecli-interactive
az vm list --out table
```

```
Name         ResourceGroup    Location
-----------  ---------------  ----------
DemoVM010    DEMORG1          westus
demovm212    DEMORG1          westus
demovm213    DEMORG1          westus
KBDemo001VM  RGDEMO001        westus
KBDemo020    RGDEMO001        westus
```

<span data-ttu-id="5fd8f-112">È possibile usare il parametro `--query` per mostrare solo il nome del gruppo di risorse e il nome della macchina virtuale per tutte le macchine virtuali della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-112">You can use the `--query` parameter to show just the Resource Group name and VM name for all virtual machines in your subscription.</span></span>

```azurecli-interactive
az vm list \
  --query [*].[name,resourceGroup] --out table
```

```
Column1     Column2
---------   -----------
DemoVM010   DEMORG1
demovm111   DEMORG1
demovm211   DEMORG1
demovm212   DEMORG1
demovm213   DEMORG1
demovm214   DEMORG1
demovm222   DEMORG1
KBDemo001VM RGDEMO001
KBDemo020   RGDEMO001
```

<span data-ttu-id="5fd8f-113">Nell'esempio precedente, notare che le intestazioni delle colonne sono "Column1" e "Column2".</span><span class="sxs-lookup"><span data-stu-id="5fd8f-113">In the previous example, you notice that the column headings are "Column1" and "Column2".</span></span>  <span data-ttu-id="5fd8f-114">È anche possibile aggiungere etichette o nomi descrittivi alle proprietà che si selezionano.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-114">You can add friendly labels or names to the properties you select, as well.</span></span>  <span data-ttu-id="5fd8f-115">Nell'esempio seguente, si sono aggiunte le etichette "VMName" e "RGName" alle proprietà selezionate "name" e "resourceGroup".</span><span class="sxs-lookup"><span data-stu-id="5fd8f-115">In the following example, we added the labels "VMName" and "RGName" to the selected properties "name" and "resourceGroup".</span></span>


```azurecli-interactive
az vm list \
  --query "[].{RGName:resourceGroup, VMName:name}" --out table
```

```
RGName     VMName
---------  -----------
DEMORG1    DemoVM010
DEMORG1    demovm111
DEMORG1    demovm211
DEMORG1    demovm212
DEMORG1    demovm213
DEMORG1    demovm214
DEMORG1    demovm222
RGDEMO001  KBDemo001VM
RGDEMO001  KBDemo020
```

## <a name="selecting-complex-nested-properties"></a><span data-ttu-id="5fd8f-116">Selezione di proprietà annidate complesse</span><span class="sxs-lookup"><span data-stu-id="5fd8f-116">Selecting complex nested properties</span></span>

<span data-ttu-id="5fd8f-117">Se la proprietà che si desidera selezionare è annidata nell'output JSON sarà necessario fornire il percorso completo di tale proprietà annidata.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-117">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="5fd8f-118">L'esempio seguente mostra come selezionare il nome della macchina virtuale e il tipo di sistema operativo dal comando list della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-118">The following example shows how to select the VMName and the OS type from the vm list command.</span></span>

```azurecli-interactive
az vm list \
  --query "[].{VMName:name,OSType:storageProfile.osDisk.osType}" --out table
```

```
VMName       OSType
-----------  --------
DemoVM010    Linux
demovm111    Linux
demovm211    Linux
demovm212    Linux
demovm213    Linux
demovm214    Linux
demovm222    Linux
KBDemo001VM  Linux
KBDemo020    Linux
```

## <a name="filter-with-the-contains-function"></a><span data-ttu-id="5fd8f-119">Filtro con la funzione contains</span><span class="sxs-lookup"><span data-stu-id="5fd8f-119">Filter with the contains function</span></span>

<span data-ttu-id="5fd8f-120">È possibile usare la funzione JMESPath `contains` per affinare i risultati restituiti dalla query.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-120">You can use the JMESPath `contains` function to refine your results returned in the query.</span></span>
<span data-ttu-id="5fd8f-121">Nell'esempio seguente il comando seleziona solo le macchine virtuali che contengono "RGD" nel loro nome.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-121">In the following example, the command selects only VMs that have the text "RGD" in their name.</span></span>  

```azurecli-interactive
az vm list \
  --query "[?contains(resourceGroup,'RGD')].{ resource: resourceGroup, name: name }" --out table
```

```
Resource    VMName
----------  -----------
RGDEMO001   KBDemo001VM
RGDEMO001   KBDemo020
```

<span data-ttu-id="5fd8f-122">Nell'esempio successivo i risultati riporteranno le macchine virtuali con vmSize 'Standard_DS1'.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-122">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1'.</span></span>

```azurecli-interactive
az vm list \
  --query "[?contains(hardwareProfile.vmSize, 'Standard_DS1')]" --out table
```

```
ResourceGroup    VMName     VmId                                  Location    ProvisioningState
---------------  ---------  ------------------------------------  ----------  -------------------
DEMORG1          DemoVM010  cbd56d9b-9340-44bc-a722-25f15b578444  westus      Succeeded
DEMORG1          demovm111  c1c024eb-3837-4075-9117-bfbc212fa7da  westus      Succeeded
DEMORG1          demovm211  95eda642-417f-4036-9475-67246ac0f0d0  westus      Succeeded
DEMORG1          demovm212  4bdac85d-c2f7-410f-9907-ca7921d930b4  westus      Succeeded
DEMORG1          demovm213  2131c664-221a-4b7f-9653-f6d542fbfa34  westus      Succeeded
DEMORG1          demovm214  48f419af-d27a-4df0-87f3-9481007c2e5a  westus      Succeeded
DEMORG1          demovm222  e0f59516-1d69-4d54-b8a2-f6c4a5d031de  westus      Succeeded
```

## <a name="filter-with-grep"></a><span data-ttu-id="5fd8f-123">Filtro con grep</span><span class="sxs-lookup"><span data-stu-id="5fd8f-123">Filter with grep</span></span>

<span data-ttu-id="5fd8f-124">Il formato di output `tsv` è un testo separato da tabulazioni senza intestazioni.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-124">The `tsv` output format is a tab-separated text with no headers.</span></span> <span data-ttu-id="5fd8f-125">Può essere inviato tramite pipe a comandi quali `grep` e `cut` per analizzare ulteriormente valori specifici dell'output `list`.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-125">It can be piped to commands like `grep` and `cut` to further parse specific values out of the `list` output.</span></span> <span data-ttu-id="5fd8f-126">Nell'esempio seguente il comando `grep` seleziona solo le macchine virtuali che contengono "RGD" nel loro nome.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-126">In the following example, the `grep` command selects only VMs that have text "RGD" in their name.</span></span>  <span data-ttu-id="5fd8f-127">Il comando `cut` seleziona solo il valore dell'ottavo campo (separato da tabulazioni) da mostrare nell'output.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-127">The `cut` command selects only the 8th field (separated by tabs) value to show in the output.</span></span>

```azurecli-interactive
az vm list --out tsv | grep RGD | cut -f8
```

```
KBDemo001VM
KBDemo020
```

## <a name="explore-with-jpterm"></a><span data-ttu-id="5fd8f-128">Esplorare con jpterm</span><span class="sxs-lookup"><span data-stu-id="5fd8f-128">Explore with jpterm</span></span>

<span data-ttu-id="5fd8f-129">È anche possibile inviare tramite pipe l'output del comando a [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) e provare la query JMESPath in tale posizione.</span><span class="sxs-lookup"><span data-stu-id="5fd8f-129">You can also pipe the command output to [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) and experiment with your JMESPath query there.</span></span>

```bash
pip install jmespath-terminal
az vm list | jpterm
```

