---
title: Formati di output per l&quot;Interfaccia della riga di comando di Azure 2.0
description: Usare --output per formattare l&quot;output dei comandi dell&quot;interfaccia della riga di comando di Azure 2.0 in tabelle, elenchi o json.
keywords: Interfaccia della riga di comando di Azure 2.0, output, formato, tabella, elenco, json, Linux, Mac, Windows, OS X
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 74bdb727-481d-45f7-a44e-15d18dc55483
ms.openlocfilehash: de37b1ad6aa55c9ac73b5b6b89d9507c86cc1245
ms.sourcegitcommit: bcf93ad8ed8802072249cd8187cd4420da89b4c6
ms.translationtype: HT
ms.contentlocale: it-IT
---
# <a name="output-formats-for-azure-cli-20-commands"></a><span data-ttu-id="df413-104">Formati di output per i comandi dell'interfaccia della riga di comando di Azure 2.0</span><span class="sxs-lookup"><span data-stu-id="df413-104">Output formats for Azure CLI 2.0 commands</span></span>

<span data-ttu-id="df413-105">L'interfaccia della riga di comando di Azure 2.0 usa json come opzione di output predefinita ma offre vari modi per formattare l'output di qualsiasi comando.</span><span class="sxs-lookup"><span data-stu-id="df413-105">Azure CLI 2.0 uses json as its default output option, but offers various ways for you to format the output of any command.</span></span>  <span data-ttu-id="df413-106">Usare il parametro `--output` (oppure `--out` o `-o`) per formattare l'output del comando in uno dei tipi di output riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="df413-106">Use the `--output` (or `--out` or `-o`) parameter to format the output of the command into one of the output types noted in the following table.</span></span> 

<span data-ttu-id="df413-107">--output</span><span class="sxs-lookup"><span data-stu-id="df413-107">--output</span></span> | <span data-ttu-id="df413-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df413-108">Description</span></span>
---------|-------------------------------
`json`   | <span data-ttu-id="df413-109">Stringa json.</span><span class="sxs-lookup"><span data-stu-id="df413-109">json string.</span></span> <span data-ttu-id="df413-110">`json` è l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="df413-110">`json` is the default.</span></span>
`jsonc`  | <span data-ttu-id="df413-111">Stringa json colorata.</span><span class="sxs-lookup"><span data-stu-id="df413-111">colorized json string.</span></span>
`table`  | <span data-ttu-id="df413-112">Tabella con intestazioni di colonna.</span><span class="sxs-lookup"><span data-stu-id="df413-112">table with column headings.</span></span>
`tsv`    | <span data-ttu-id="df413-113">Valori delimitati da tabulazioni.</span><span class="sxs-lookup"><span data-stu-id="df413-113">tab-separated values.</span></span>

## <a name="using-the-json-option"></a><span data-ttu-id="df413-114">Uso dell'opzione json</span><span class="sxs-lookup"><span data-stu-id="df413-114">Using the json option</span></span>

<span data-ttu-id="df413-115">L'esempio seguente mostra l'elenco di macchine virtuali nelle proprie sottoscrizioni in formato json predefinito.</span><span class="sxs-lookup"><span data-stu-id="df413-115">The following example displays the list of virtual machines in your subscriptions in the default json format.</span></span>

```azurecli
az vm list --output json
```

<span data-ttu-id="df413-116">I risultati sono in questo formato (viene riportato solo un output parziale per brevità).</span><span class="sxs-lookup"><span data-stu-id="df413-116">The results are in this form (only showing partial output for sake of brevity).</span></span>

```json
[
  {
    "availabilitySet": null,
    "diagnosticsProfile": null,
    "hardwareProfile": {
      "vmSize": "Standard_DS1"
    },
    "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010",
    "instanceView": null,
    "licenseType": null,
    "location": "westus",
    "name": "DemoVM010",
    "networkProfile": {
      "networkInterfaces": [
        {
          "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/demorg1/providers/Microsoft.Network/networkInterfaces/DemoVM010VMNic",
          "primary": null,
          "resourceGroup": "demorg1"
        }
      ]
    },
          ...
          ...
          ...   
]
```
 
## <a name="using-the-table-option"></a><span data-ttu-id="df413-117">Uso dell'opzione table</span><span class="sxs-lookup"><span data-stu-id="df413-117">Using the table option</span></span>

<span data-ttu-id="df413-118">L'opzione table offre un set di output di agevole lettura, ma notare che gli oggetti annidati non vengono inclusi nell'output con il comando `--output table` semplice, a differenza dell'esempio precedente relativo a .json.</span><span class="sxs-lookup"><span data-stu-id="df413-118">The table option provides an easy to read set of output, but note that nested objects are not included in the output with the simple `--output table`, unlike the preceding .json example.</span></span>  <span data-ttu-id="df413-119">Se si usa lo stesso esempio con il formato di output 'table' si ottiene un elenco curato dei valori di proprietà più comuni.</span><span class="sxs-lookup"><span data-stu-id="df413-119">Using the same example with 'table' output format provides a curated list of most common property values.</span></span>

```azurecli
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

<span data-ttu-id="df413-120">È possibile usare il parametro `--query` per personalizzare le proprietà e le colonne che si desidera mostrare nell'output.</span><span class="sxs-lookup"><span data-stu-id="df413-120">You can use the `--query` parameter to customize the properties and columns you want to show in the list output.</span></span> <span data-ttu-id="df413-121">L'esempio seguente mostra come selezionare solo il nome della macchina virtuale e il nome del gruppo di risorse nel comando `list`.</span><span class="sxs-lookup"><span data-stu-id="df413-121">The following example shows how to select just the VM Name and the Resource Group Name in the `list` command.</span></span>

```azurecli
az vm list --query "[].{ resource: resourceGroup, name: name }" -o table
```

```
Resource    Name
----------  -----------
DEMORG1     DemoVM010
DEMORG1     demovm212
DEMORG1     demovm213
RGDEMO001   KBDemo001VM
RGDEMO001   KBDemo020
```

## <a name="using-the-tsv-option"></a><span data-ttu-id="df413-122">Uso dell'opzione tsv</span><span class="sxs-lookup"><span data-stu-id="df413-122">Using the tsv option</span></span>

<span data-ttu-id="df413-123">Il formato di output 'tsv' restituisce un output di testo semplice separato da tabulazioni senza intestazioni né trattini.</span><span class="sxs-lookup"><span data-stu-id="df413-123">'tsv' output format returns a simple text-based and tab-separated output with no headings and dashes.</span></span> <span data-ttu-id="df413-124">Questo formato consente di usare agevolmente l'output in altri comandi e strumenti che devono elaborare il testo in una determinata forma.</span><span class="sxs-lookup"><span data-stu-id="df413-124">This format makes it easy to consume the output into other commands and tools that need to process the text in some form.</span></span> <span data-ttu-id="df413-125">Se si usa l'esempio precedente con l'opzione `tsv` si genera il risultato separato da tabulazioni.</span><span class="sxs-lookup"><span data-stu-id="df413-125">Using the preceding example with the `tsv` option outputs the tab-separated result.</span></span>

```azurecli
az vm list --out tsv
```

```
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010    None    None    westus    DemoVM010            None    Succeeded    DEMORG1    None            Microsoft.Compute/virtualMachines    cbd56d9b-9340-44bc-a722-25f15b578444
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm212    None    None    westus    demovm212            None    Succeeded    DEMORG1    None            Microsoft.Compute/virtualMachines    4bdac85d-c2f7-410f-9907-ca7921d930b4
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm213    None    None    westus    demovm213            None    Succeeded    DEMORG1    None            Microsoft.Compute/virtualMachines    2131c664-221a-4b7f-9653-f6d542fbfa34
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo001VM    None    None    westus    KBDemo001VM            None    Succeeded    RGDEMO001    None            Microsoft.Compute/virtualMachines    14e74761-c17e-4530-a7be-9e4ff06ea74b
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo02None    None    westus    KBDemo020            None    Succeeded    RGDEMO001    None            Microsoft.Compute/virtualMachinesed36baa9-9b80-48a8-b4a9-854c7a858ece
```

<span data-ttu-id="df413-126">L'esempio seguente mostra come l'output `tsv` può essere inviato tramite pipe a comandi quali `grep` e `cut` per analizzare ulteriormente valori specifici dell'output `list`.</span><span class="sxs-lookup"><span data-stu-id="df413-126">The next example shows how the `tsv` output can be piped to commands like `grep` and `cut` to further parse specific values out of the `list` output.</span></span> <span data-ttu-id="df413-127">Il comando `grep` seleziona solo gli elementi che contengono il testo "RGD" e quindi il comando `cut` seleziona solo il valore dell'ottavo campo (separato da tabulazioni ) da mostrare nell'output.</span><span class="sxs-lookup"><span data-stu-id="df413-127">The `grep` command selects only items that have text "RGD" in them and then the `cut` command selects only the eighth field (separated by tabs) value to show in the output.</span></span>

```azurecli
az vm list --out tsv | grep RGD | cut -f8
```

```
KBDemo001VM
KBDemo020
```

## <a name="setting-the-default-output-format"></a><span data-ttu-id="df413-128">Impostazione del formato di output predefinito</span><span class="sxs-lookup"><span data-stu-id="df413-128">Setting the default output format</span></span>

<span data-ttu-id="df413-129">È possibile usare il comando `az configure` per configurare l'ambiente o stabilire preferenze quali le impostazioni predefinite per i formati di output.</span><span class="sxs-lookup"><span data-stu-id="df413-129">You can use the `az configure` command to set up your environment or establish preferences such as default settings for output formats.</span></span> <span data-ttu-id="df413-130">Per l'uso comune, il formato di output predefinito più semplice è il formato "table" - selezionare **3** quando vengono richieste le opzioni di formato di output.</span><span class="sxs-lookup"><span data-stu-id="df413-130">For common use, the easiest output format default is the "table" format - select **3** when prompted for output format choices.</span></span> 

```
What default output format would you like?
 [1] json - JSON formatted output that most closely matches API responses
 [2] jsonc - Colored JSON formatted output that most closely matches API responses
 [3] table - Human-readable output format
 [4] tsv - Tab and Newline delimited, great for GREP, AWK, etc.
Please enter a choice [3]: 
```