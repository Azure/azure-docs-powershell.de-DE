---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4403232b45b2a1e69d6148a118e69ccaf80e4a1e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007191"
---
# Get-AzsUserSubscription

## Synopsis
Rufen Sie die Liste der Benutzer Abonnements als Administrator ab.

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
Rufen Sie die Liste der Benutzer Abonnements als Administrator ab.

## Beispiele

### --------------------------Beispiel 1--------------------------
```
Get-AzsUserSubscription
```

Rufen Sie die Liste der Benutzer Abonnements als Administrator ab.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription

## Notizen

## Verwandte Links

