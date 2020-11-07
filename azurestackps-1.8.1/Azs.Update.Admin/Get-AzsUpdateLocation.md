---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d94fdb44a5e37988853c95de794d67fcb26a515
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840604"
---
# Get-AzsUpdateLocation

## Synopsis
Rufen Sie die Liste der Update Speicherorte ab.

## Syntax

### Liste (Standard)
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### Erhalten
```
Get-AzsUpdateLocation [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## Beschreibung
Rufen Sie die Liste der Update Speicherorte ab. Die zurückgegebenen Speicherorte können verwendet werden, um verfügbare Updates an einem bestimmten Speicherort mithilfe von Get-AzsUpdate abzurufen.

## Beispiele

### Beispiel 1
```
Get-AzsUpdateLocation
```

Rufen Sie die Liste der Update Speicherorte ab.

## Parameter

### -Standort
Name des Standorts.

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Die Ressourcengruppe, unter der sich die Ressource befindet.

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
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. AzureStack. Management. Update. admin. Models. UpdateLocation angegeben ist

## Notizen

## Verwandte Links
