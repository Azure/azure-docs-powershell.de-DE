---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5ff90957a655837dbdf75ce3f4242222615f2a73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474889"
---
# Get-AzsUserSubscription

## Synopsis
Rufen Sie die Liste der Benutzer Abonnements als Operator ab.

## Syntax

### Liste (Standard)
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### Erhalten
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## Beschreibung
Rufen Sie die Liste der Benutzer Abonnements als Operator ab.

## Beispiele

### --------------------------Beispiel 1--------------------------
```
Get-AzsUserSubscription
```

Rufen Sie die Liste der Benutzer Abonnements als Operator ab.

## Parameter

### -Filter
OData-Filterparameter

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Abonnement-Nr
Parameter für die Abonnement-ID.

```yaml
Type: Guid
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription

## Notizen

## Verwandte Links

