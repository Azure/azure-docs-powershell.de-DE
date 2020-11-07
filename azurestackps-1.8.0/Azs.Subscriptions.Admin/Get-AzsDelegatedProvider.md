---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc99afebed095da96d826918cc6912f197d1899
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827900"
---
# Get-AzsDelegatedProvider

## Synopsis
Rufen Sie die Liste der delegatedProviders.

## Syntax

### Liste (Standard)
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### Erhalten
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## Beschreibung
Rufen Sie die Liste der delegatedProviders.

## Beispiele

### --------------------------Beispiel 1--------------------------
```
Get-AzsDelegatedProvider
```

Rufen Sie eine Liste der Delegierten Anbieter ab.

### --------------------------Beispiel 2--------------------------
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

Rufen Sie den jeweiligen Delegierten Anbieter ab.

## Parameter

### -DelegatedProviderId
{{Fill DelegatedProviderId Description}}

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
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

