---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 687838573459c09ceaf08c0d1c3335caa4a99769
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840599"
---
# Get-AzsStorageQuota

## Synopsis
Gibt eine Liste der Speicherkontingente an der angegebenen Position zurück.

## Syntax

### Liste (Standard)
```
Get-AzsStorageQuota [-Location <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### Erhalten
```
Get-AzsStorageQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsStorageQuota -ResourceId <String> [<CommonParameters>]
```

## Beschreibung
Gibt eine Liste der Speicherkontingente an der angegebenen Position zurück.

## Beispiele

### Beispiel 1
```
Get-AzsStorageQuota
```

Rufen Sie die Liste der Speicherkontingente ab.

### Beispiel 2
```
Get-AzsStorageQuota -Name "storagequota1"
```

Abrufen von Details des angegebenen Speicherkontingents anhand des Namens

## Parameter

### -Name
Der Name des Speicherkontingents.

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

### -Standort
Ressourcen Standort.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota

## Notizen

## Verwandte Links
