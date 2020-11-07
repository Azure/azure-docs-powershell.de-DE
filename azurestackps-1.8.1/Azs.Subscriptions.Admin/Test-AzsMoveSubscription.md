---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a04836e2d361f4c9686fa5dfe62babfa57ade189
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828100"
---
# Test-AzsMoveSubscription

## Synopsis
Überprüfen Sie, ob Benutzer Abonnements zwischen angeboten des Delegierten Anbieters verschoben werden können.

## Syntax

```
Test-AzsMoveSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## Beschreibung
Überprüfen Sie, ob Benutzer Abonnements zwischen angeboten des Delegierten Anbieters verschoben werden können.

## Beispiele

### --------------------------Beispiel 1--------------------------
```
Test that user subscriptions can be moved to a delegated provider offer.
```

Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/Subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/RO1"-Resourcen-"/Subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/Subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6"; "/Subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/Subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"

### --------------------------Beispiel 2--------------------------
```
Test that user subscriptions can be moved from a delegated provider to the Default Provider.
```

$resourceIds = Get-AzsUserSubscription-Filter "Offername EQ ' O1 '" | SELECT-expando-ID Test-MoveSubscription-ResoruceId $resourceIds

## Parameter

### -AsJob
Gibt an, ob der Verschiebevorgang als Job ausgeführt werden soll.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationDelegatedProviderOffer
Gibt das vollqualifizierte Anbieter Angebot für Delegierte an, in das dieses Cmdlet Abonnements verschiebt.
NULL, wenn die Abonnements zurück zum Standardanbieter verschoben werden sollen.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resourcen-Nr
Gibt ein Array vollständig qualifizierter Abonnement Ressourcen-IDs an, die dieses Cmdlet verschiebt.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

