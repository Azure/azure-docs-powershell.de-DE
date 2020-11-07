---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 819cdc45e75c15c38c9ae28c583ac3c73e54f4ac
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840791"
---
# Get-AzsComputeQuota

## Synopsis
Gibt Kontingente zurück, die die Kontingentgrenzen für Compute-Objekte angeben.

## Syntax

### Liste (Standard)
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### Erhalten
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## Beschreibung
Abrufen einer Liste vorhandener Kontingente

## Beispiele

### --------------------------Beispiel 1--------------------------
```
Get-AzsComputeQuota -Location 'local'
```

Rufen Sie alle Compute-Kontingente an der angegebenen Position ab.

### --------------------------Beispiel 2--------------------------
```
Get-AzsComputeQuota 'Default Quota'
```

Abrufen eines bestimmten Compute-Kontingents

## Parameter

### -Standort
{{Fill Location Description}}

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
Der Name des Kontingents.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### ComputeQuotaObject

## Notizen

## Verwandte Links

