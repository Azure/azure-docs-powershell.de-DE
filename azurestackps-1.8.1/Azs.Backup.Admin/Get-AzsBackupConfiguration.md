---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25091f0cb439e0447d19b534d59a0084a5b05c6e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828251"
---
# Get-AzsBackupConfiguration

## Synopsis
Gibt die Liste der Sicherungs Konfigurationen zurück.

## Syntax

### Liste (Standard)
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### Erhalten
```
Get-AzsBackupConfiguration [[-Location] <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsBackupConfiguration -ResourceId <String> [<CommonParameters>]
```

## Beschreibung
Gibt die Liste der Sicherungs Konfigurationen zurück.

## Beispiele

### --------------------------Beispiel 1--------------------------
```
Get-AzsBackupConfiguration
```

Erhalten Sie die Azure Stack-Sicherungskonfiguration.

## Parameter

### -Standort
Sicherungsspeicherort.

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.

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

### Microsoft. AzureStack. Management. Backup. admin. Models. BackupLocation

## Notizen

## Verwandte Links

