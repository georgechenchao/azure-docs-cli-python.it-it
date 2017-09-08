---
title: Risultati del comando query con l'interfaccia della riga di comando di Azure 2.0
description: Usare --query per eseguire query JMESPath sull'output dei comandi dell'interfaccia della riga di comando di Azure 2.0.
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
ms.openlocfilehash: e0eee9eb9e0a9f136ff076d064ce802f76bc8e3d
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/04/2017
---
# <a name="using-jmespath-queries-with-azure-cli-20"></a>Uso di query JMESPath con l'interfaccia della riga di comando di Azure 2.0

L'interfaccia della riga di comando di Azure 2.0 usa il parametro `--query` per eseguire una [query JMESPath](http://jmespath.org) sui risultati del comando `az`. JMESPath è un linguaggio di query avanzato per output JSON.  Se non si ha familiarità con le query JMESPath è disponibile un'esercitazione in [JMESPath.org/tutorial](http://JMESPath.org/tutorial.html).

Il parametro `Query` è supportato da ogni tipo di risorsa (servizi contenitore, app Web, macchine virtuali e così via) nell'interfaccia della riga di comando di Azure 2.0 e può essere usato per vari scopi diversi.  Di seguito sono riportati alcuni esempi.

## <a name="selecting-simple-properties"></a>Selezione di proprietà semplici

Il comando `list` semplice con il formato di output `table` restituisce un set curato delle proprietà semplici più comuni per ogni tipo di risorsa in un formato tabulare di facile lettura.

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

È possibile usare il parametro `--query` per mostrare solo il nome del gruppo di risorse e il nome della macchina virtuale per tutte le macchine virtuali della sottoscrizione.

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

Nell'esempio precedente, notare che le intestazioni delle colonne sono "Column1" e "Column2".  È anche possibile aggiungere etichette o nomi descrittivi alle proprietà che si selezionano.  Nell'esempio seguente, si sono aggiunte le etichette "VMName" e "RGName" alle proprietà selezionate "name" e "resourceGroup".


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

## <a name="selecting-complex-nested-properties"></a>Selezione di proprietà annidate complesse

Se la proprietà che si desidera selezionare è annidata nell'output JSON sarà necessario fornire il percorso completo di tale proprietà annidata. L'esempio seguente mostra come selezionare il nome della macchina virtuale e il tipo di sistema operativo dal comando list della macchina virtuale.

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

## <a name="filter-with-the-contains-function"></a>Filtro con la funzione contains

È possibile usare la funzione JMESPath `contains` per affinare i risultati restituiti dalla query.
Nell'esempio seguente il comando seleziona solo le macchine virtuali che contengono "RGD" nel loro nome.  

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

Nell'esempio successivo i risultati riporteranno le macchine virtuali con vmSize 'Standard_DS1'.

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

## <a name="filter-with-grep"></a>Filtro con grep

Il formato di output `tsv` è un testo separato da tabulazioni senza intestazioni. Può essere inviato tramite pipe a comandi quali `grep` e `cut` per analizzare ulteriormente valori specifici dell'output `list`. Nell'esempio seguente il comando `grep` seleziona solo le macchine virtuali che contengono "RGD" nel loro nome.  Il comando `cut` seleziona solo il valore dell'ottavo campo (separato da tabulazioni) da mostrare nell'output.

```azurecli-interactive
az vm list --out tsv | grep RGD | cut -f8
```

```
KBDemo001VM
KBDemo020
```

## <a name="explore-with-jpterm"></a>Esplorare con jpterm

È anche possibile inviare tramite pipe l'output del comando a [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) e provare la query JMESPath in tale posizione.

```bash
pip install jmespath-terminal
az vm list | jpterm
```

