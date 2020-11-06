---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 914b75e3952f7841aaf3ff505f51f7b4ebdc6044
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475054"
---
# Get-AzureRmContext

## Synopsis
Ruft die Metadaten ab, mit denen Azure Resource Manager-Anforderungen authentifiziert werden.

## Syntax

```
Get-AzureRmContext [<CommonParameters>]
```

## Beschreibung
Das Get-AzureRmContext-Cmdlet ruft die aktuellen Metadaten ab, mit denen Azure-Ressourcen-Manager-Anforderungen authentifiziert werden.

Dieses Cmdlet ruft das Active Directory-Konto, den Active Directory-Mandanten, das Azure-Abonnement und die Ziel Azure-Umgebung ab.
Azure Resource Manager-Cmdlets verwenden diese Einstellungen standardmäßig beim Erstellen von Azure-Ressourcen-Manager-Anforderungen.

## Beispiele

### Beispiel 1: Abrufen des aktuellen Kontexts
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

In diesem Beispiel melden wir uns mit einem Azure-Abonnement mit Add-AzureRmAccount bei unserem Konto an, und dann erhalten wir den Kontext der aktuellen Sitzung durch Aufrufen von Get-AzureRmContext.

## Parameter

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### PSAzureContext
Dieses Cmdlet gibt das Konto, den Mandanten und das Abonnement zurück, das von Azure Resource Manager-Cmdlets verwendet wird.

## Notizen

## Verwandte Links

[Satz-AzureRMContext]()

