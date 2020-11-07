---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09391f521a2b75663b25731c6cc20ef78a658d5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827408"
---
# Add-AzsScaleUnitNode

## Synopsis
Skalieren einer Skalierungseinheit

## Syntax

```
Add-AzsScaleUnitNode [-NodeList] <ScaleOutScaleUnitParameters[]> [[-ResourceGroupName] <String>]
 [-ScaleUnit] <String> [[-Location] <String>] [-AwaitStorageConvergence] [-AsJob] [<CommonParameters>]
```

## Beschreibung
Fügen Sie einen neuen Skalierungseinheiten Knoten zu Ihrem Skalierungseinheiten Cluster hinzu.

## Beispiele

### --------------------------Beispiel 1--------------------------
```
Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName
```

Fügt der Skalierungseinheit eine Liste von Knoten hinzu.

## Parameter

### -AsJob
Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.

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

### -AwaitStorageConvergence
Warten Sie, bis die Speicherreplikation abgeschlossen ist, bevor Sie erfolgreich zurückkehren.

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

### -Standort
Der Speicherort der Ressource.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nodeliste
Eine Liste mit Eingabedaten, die das Hinzufügen einer Gruppe von Skalierungseinheiten Knoten ermöglicht.

```yaml
Type: ScaleOutScaleUnitParameters[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScaleUnit
Name der Skalierungseinheiten

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

