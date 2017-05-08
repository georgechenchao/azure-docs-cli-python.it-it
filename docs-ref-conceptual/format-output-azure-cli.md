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
# <a name="output-formats-for-azure-cli-20-commands"></a>Formati di output per i comandi dell'interfaccia della riga di comando di Azure 2.0

L'interfaccia della riga di comando di Azure 2.0 usa json come opzione di output predefinita ma offre vari modi per formattare l'output di qualsiasi comando.  Usare il parametro `--output` (oppure `--out` o `-o`) per formattare l'output del comando in uno dei tipi di output riportati nella tabella seguente. 

--output | Descrizione
---------|-------------------------------
`json`   | Stringa json. `json` è l'impostazione predefinita.
`jsonc`  | Stringa json colorata.
`table`  | Tabella con intestazioni di colonna.
`tsv`    | Valori delimitati da tabulazioni.

## <a name="using-the-json-option"></a>Uso dell'opzione json

L'esempio seguente mostra l'elenco di macchine virtuali nelle proprie sottoscrizioni in formato json predefinito.

```azurecli
az vm list --output json
```

I risultati sono in questo formato (viene riportato solo un output parziale per brevità).

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
 
## <a name="using-the-table-option"></a>Uso dell'opzione table

L'opzione table offre un set di output di agevole lettura, ma notare che gli oggetti annidati non vengono inclusi nell'output con il comando `--output table` semplice, a differenza dell'esempio precedente relativo a .json.  Se si usa lo stesso esempio con il formato di output 'table' si ottiene un elenco curato dei valori di proprietà più comuni.

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

È possibile usare il parametro `--query` per personalizzare le proprietà e le colonne che si desidera mostrare nell'output. L'esempio seguente mostra come selezionare solo il nome della macchina virtuale e il nome del gruppo di risorse nel comando `list`.

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

## <a name="using-the-tsv-option"></a>Uso dell'opzione tsv

Il formato di output 'tsv' restituisce un output di testo semplice separato da tabulazioni senza intestazioni né trattini. Questo formato consente di usare agevolmente l'output in altri comandi e strumenti che devono elaborare il testo in una determinata forma. Se si usa l'esempio precedente con l'opzione `tsv` si genera il risultato separato da tabulazioni.

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

L'esempio seguente mostra come l'output `tsv` può essere inviato tramite pipe a comandi quali `grep` e `cut` per analizzare ulteriormente valori specifici dell'output `list`. Il comando `grep` seleziona solo gli elementi che contengono il testo "RGD" e quindi il comando `cut` seleziona solo il valore dell'ottavo campo (separato da tabulazioni ) da mostrare nell'output.

```azurecli
az vm list --out tsv | grep RGD | cut -f8
```

```
KBDemo001VM
KBDemo020
```

## <a name="setting-the-default-output-format"></a>Impostazione del formato di output predefinito

È possibile usare il comando `az configure` per configurare l'ambiente o stabilire preferenze quali le impostazioni predefinite per i formati di output. Per l'uso comune, il formato di output predefinito più semplice è il formato "table" - selezionare **3** quando vengono richieste le opzioni di formato di output. 

```
What default output format would you like?
 [1] json - JSON formatted output that most closely matches API responses
 [2] jsonc - Colored JSON formatted output that most closely matches API responses
 [3] table - Human-readable output format
 [4] tsv - Tab and Newline delimited, great for GREP, AWK, etc.
Please enter a choice [3]: 
```