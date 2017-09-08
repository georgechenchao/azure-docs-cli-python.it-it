---
title: "Modalità interattiva dell'interfaccia della riga di comando di Azure 2.0"
description: "Usare la modalità interattiva dell'interfaccia della riga di comando di Azure 2.0."
keywords: "Interfaccia della riga di comando di Azure 2.0, modalità interattiva"
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 04/06/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 
ms.openlocfilehash: de6a366b84efa5475fd6146ff29c32e32dfe4672
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/04/2017
---
# <a name="interactive-azure-cli-20"></a>Interfaccia della riga di comando di Azure 2.0 interattiva

È possibile usare l'interfaccia della riga di comando di Azure 2.0 in modalità interattiva eseguendo il comando `az interactive`.
Questo consente di accedere a una shell interattiva in cui i comandi vengono completati automaticamente e sarà possibile accedere alle descrizioni dei comandi, nonché ai relativi parametri e agli esempi di comando.

![modalità interattiva](./media/interactive-azure-cli/webapp-create.png)

> [!NOTE]
> Qui non viene usato lo stile predefinito, che non risulta leggibile su sfondo nero.

Se l'utente non ha effettuato l'accesso al proprio account, usare il comando `login` per eseguire questa operazione.

## <a name="configure"></a>Configurare

La modalità interattiva mostra, facoltativamente, le descrizioni dei comandi, le descrizioni dei parametri ed esempi di comando.
È possibile attivare o disattivare descrizioni ed esempi tramite `F1`.

![descrizioni ed esempi](./media/interactive-azure-cli/descriptions-and-examples.png)

È possibile attivare o disattivare la visualizzazione dei valori predefiniti dei parametri usando `F2`.

![valori predefiniti](./media/interactive-azure-cli/defaults.png)

`F3` attiva o disattiva la visualizzazione di alcuni movimenti chiave.

![movimenti](./media/interactive-azure-cli/gestures.png)

## <a name="scope"></a>Scope

È possibile definire un ambito della modalità interattiva per un gruppo di comandi specifici come `vm` o `vm image`.
Quando si esegue questa operazione, tutti i comandi vengono interpretati in tale ambito.
È una sintassi abbreviata ideale se si sta effettuando il lavoro in tale gruppo di comandi.

Anziché digitare i comandi seguenti:

```azurecli
az>> vm create -n myVM -g myRG --image UbuntuLTS
az>> vm list -o table
```

È possibile definire l'ambito per il gruppo di comandi della macchina virtuale e digitare i comandi seguenti:

```azurecli
az>> %%vm
az vm>> create -n myVM -g myRG --image UbuntuLTS
az vm>>list -o table
```

È possibile definire l'ambito anche per gruppi di comandi di livello inferiore.
È possibile definire l'ambito `vm image` usando `%%vm image`.
In questo caso, poiché è già stato definito l'ambito per `vm`, useremo `%%image`.

```azurecli
az vm>> %%image
az vm image>>
```

A questo punto, è possibile riportare l'ambito a `vm` usando `%%..` oppure è possibile definire l'ambito alla radice semplicemente con `%%`.

```azurecli
az vm image>> %%
az>>
```

## <a name="query"></a>Query

È possibile eseguire una query JMESPath sui risultati dell'ultimo comando eseguito.
Ad esempio, dopo aver creato una macchina virtuale, è possibile assicurarsi che abbia completato il provisioning.

```azurecli
az>> vm create --name myVM --resource-group myRG --image UbuntuLTS --no-wait
az>> ? [*].provisioningState
```

```
[
  "Creating"
]
```

Per altre informazioni sulle query ai risultati dei comandi, vedere [Effettuare query ai risultati dei comandi con Azure 2.0](query-azure-cli.md).

## <a name="bash-commands"></a>Comandi Bash

È possibile eseguire i comandi della shell senza uscire dalla modalità interattiva tramite `#[cmd]`.

```azurecli
az>> #dir
```

## <a name="examples"></a>esempi

Alcuni comandi hanno numerosi esempi.
È possibile passare alla pagina successiva di esempi usando `CTRL-N` e alla pagina precedente usando `CTRL-Y`.

![esempi](./media/interactive-azure-cli/examples.png)

È anche possibile vedere un esempio specifico usando `::#`.

```azurecli
az>> vm create ::8
```
