---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b51280387ad3eb29f05bee8876765a621e0d07c4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828252"
---
# Get-AzsBackup

## Synopsis
Gibt eine Sicherung von einem Speicherort basierend auf dem Namen zurück.

## Syntax

### Liste (Standard)
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### Erhalten
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### ParentResource
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## Beschreibung
Gibt eine Sicherung von einem Speicherort basierend auf dem Namen zurück.

## Beispiele

### --------------------------Beispiel 1--------------------------
```
Get-AzsBackup
```

Abrufen von Informationen über alle Azure Stack-Sicherungen.

### --------------------------Beispiel 2--------------------------
```
Get-AzsBackup -Name 'backupName'
```

Rufen Sie Informationen für die angegebene Azure Stack-Sicherung ab.

## Parameter

### -Standort
Speicherort gesichert.

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
Der Name der Sicherung.

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentResource
Durch das Übergeben eines Sicherungsspeicherorts wird die Liste aller Sicherungen an diesem Sicherungsspeicherort zurückgegeben.

```yaml
Type: BackupLocation
Parameter Sets: ParentResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
{{Fill Skip Description}}

```yaml
Type: Int32
Parameter Sets: List, ParentResource
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -Top
{{Fill Top Description}}

```yaml
Type: Int32
Parameter Sets: List, ParentResource
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

### Microsoft. AzureStack. Management. Backup. admin. Models. Backup

## Notizen

## Verwandte Links

