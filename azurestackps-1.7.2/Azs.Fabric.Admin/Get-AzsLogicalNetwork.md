---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fdf0c09e087779e9a08161f2af6f9070f193c31b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827047"
---
# Get-AzsLogicalNetwork

## Synopsis
Gibt eine Liste aller logischen Netzwerke an einem Speicherort zurück.

## Syntax

### Liste (Standard)
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### Erhalten
```
Get-AzsLogicalNetwork [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsLogicalNetwork -ResourceId <String> [<CommonParameters>]
```

## Beschreibung
Gibt eine Liste aller logischen Netzwerke an einem Speicherort zurück.

## Beispiele

### --------------------------Beispiel 1--------------------------
```
Get-AzsLogicalNetwork
```

Abrufen aller logischen Netzwerke an einem Speicherort

### --------------------------Beispiel 2--------------------------
```
Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"
```

Abrufen bestimmter logischer Netzwerke an einem Speicherort, der auf einem Namen basiert.

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

### -Standort
Der Speicherort der Ressource.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name des logischen Netzwerks.

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resourcen-Nr
Die Ressourcen-ID.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Skip
Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -Top
Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.
Gilt nach dem-Skip-Parameter.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. AzureStack. Management. Fabric. admin. Models. LogicalNetwork

## Notizen

## Verwandte Links

