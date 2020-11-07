---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cadf5ad37119ab6b50191e50e8ec281fe4bce2d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826924"
---
# Get-AzsPlanMetric

## Synopsis
Ermitteln Sie die Plan Metriken.

## Syntax

```
Get-AzsPlanMetric [-ResourceGroupName] <String> [-PlanName] <String> [<CommonParameters>]
```

## Beschreibung
Ermitteln Sie die Plan Metriken.

## Beispiele

### --------------------------Beispiel 1--------------------------
```
Get-AzsPlanMetric -ResourceGroupName rg1 -PlanName plan1
```

Besorgen Sie sich die Metriken eines Plans.

## Parameter

### -Planname
Der Name des Plans.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Die Ressourcengruppe, unter der sich die Ressource befindet.

```yaml
Type: String
Parameter Sets: (All)
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

### Microsoft. AzureStack. Management. Subscriptions. admin. Models. Metric

## Notizen

## Verwandte Links

