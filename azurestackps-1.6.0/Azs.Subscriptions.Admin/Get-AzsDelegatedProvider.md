---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88c19285ee7188dab272eeab7a668f5f5dfe22a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475453"
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
DelegatedProvider-Bezeichner.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription

## Notizen

## Verwandte Links

