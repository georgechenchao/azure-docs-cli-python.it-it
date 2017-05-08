---
title: Accedere con l&quot;interfaccia della riga di comando di Azure 2.0
description: Accedere con l&quot;interfaccia della riga di comando di Azure 2.0 su Linux, Mac o Windows.
keywords: Interfaccia della riga di comando di Azure 2.0, Linux, Mac, Windows, OS X, Ubuntu, Debian, CentOS, RHEL, SUSE, CoreOS, Docker, Windows, Python, PIP
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 65becd3a-9d69-4415-8a30-777d13a0e7aa
ms.openlocfilehash: fea893ebd55811527e0e92375ffc081a52cdbb57
ms.sourcegitcommit: bcf93ad8ed8802072249cd8187cd4420da89b4c6
ms.translationtype: HT
ms.contentlocale: it-IT
---
# <a name="log-in-with-azure-cli-20"></a>Accedere con l'interfaccia della riga di comando di Azure 2.0

Esistono diversi modi per accedere ed eseguire l'autenticazione con l'interfaccia della riga di comando di Azure. Il modo più semplice per iniziare consiste nell'accedere in modo interattivo tramite il browser o dalla riga di comando. L'approccio consigliato consiste nell'usare delle entità di servizio, che consentono di creare account non interattivi da usare per la modifica delle risorse. Concedendo a un'entità servizio solo le autorizzazioni appropriate, è possibile garantire che gli script di automazione siano ancora più sicuri.

I comandi che si eseguono con l'interfaccia della riga di comando vengono eseguiti sulla sottoscrizione predefinita.  Se si hanno più sottoscrizioni, può essere opportuno [verificare la sottoscrizione predefinita](manage-azure-subscriptions-azure-cli.md) e modificarla in modo appropriato.

## <a name="interactive-log-in"></a>Accesso interattivo

Accedere in modo interattivo dal Web browser.

[!INCLUDE [interactive_login](includes/interactive-login.md)]

## <a name="command-line"></a>Riga di comando

Fornire le credenziali dalla riga di comando.

> [!Note]
> Questo approccio non funziona con gli account Microsoft o gli account in cui è abilitata l'autenticazione a due fattori.

```azurecli
az login -u <username> -p <password>
```

## <a name="logging-in-with-a-service-principal"></a>Accesso con un'entità servizio

Le entità servizio sono analoghe agli account utente a cui è possibile applicare delle regole mediante Azure Active Directory.
L'autenticazione con un'entità servizio rappresenta il modo migliore per proteggere l'utilizzo delle risorse Azure dagli script o dalle applicazioni che modificano le risorse.
Definire i ruoli che si desidera assegnare agli utenti tramite il set di comandi `az role`.
Per altre informazioni ed esempi di ruoli di entità servizio, vedere gli [articoli di riferimento sul ruolo az](https://docs.microsoft.com/cli/azure/role.md).

1. Se non si dispone di un'entità servizio, [crearne una](create-an-azure-service-principal-azure-cli.md).

1. Accedere con l'entità servizio.

   ```azurecli
   az login --service-principal -u "http://my-app" -p <password> --tenant <tenant>
   ```

   Per ottenere il proprio tenant, accedere in modo interattivo e ottenere il tenantId dalla sottoscrizione.

   ```azurecli
   az login
   az account show
   ```

   ```json
   {
       "environmentName": "AzureCloud",
       "id": "********-****-****-****-************",
       "isDefault": true,
       "name": "Pay-As-You-Go",
       "state": "Enabled",
       "tenantId": "********-****-****-****-************",
       "user": {
       "name": "********",
       "type": "user"
       }
   }
   ```