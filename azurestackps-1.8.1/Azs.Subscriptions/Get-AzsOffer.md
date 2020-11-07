---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77d6a4861dbdb93dff2d5511faeceac30e3f9cf8
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840636"
---
# Get-AzsOffer

## Synopsis
Holen Sie sich die Liste der öffentlichen Angebote.

## Syntax

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [[-Provider] <String>] [<CommonParameters>]
```

## Beschreibung
Holen Sie sich die Liste der öffentlichen Angebote.

## Beispiele

### Beispiel 1
```
Get-AzsOffer | fl
```

Holen Sie sich die Liste der öffentlichen Angebote.

## Parameter

### -Skip
Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -Top
Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.
Gilt nach dem-Skip-Parameter.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -Anbieter
Optionaler Parameter, um den Namen des Delegierten Anbieters anzugeben. Dieser Parameter wird nicht verwendet und wird in Zukunft veraltet sein.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. AzureStack. Management. Subscription. Models. offer

## Notizen

## Verwandte Links
