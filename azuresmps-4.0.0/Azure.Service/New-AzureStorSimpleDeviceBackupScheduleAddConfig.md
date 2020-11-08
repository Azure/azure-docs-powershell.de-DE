---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EE7EC812-640B-4672-B23C-673F912F0EDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 945d06ddc1be6d2b0864b0421a5a087e14d98218
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005734"
---
# New-AzureStorSimpleDeviceBackupScheduleAddConfig

## Synopsis
Erstellt ein Konfigurationsobjekt für den Sicherungszeitplan.

## Syntax

```
New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] -Enabled <Boolean>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** wird ein **BackupScheduleBase** -Konfigurationsobjekt erstellt.
Verwenden Sie dieses Konfigurationsobjekt, um neue Sicherungsrichtlinien mithilfe des Cmdlets **New-AzureStorSimpleDeviceBackupPolicy** zu erstellen.

## Beispiele

### Beispiel 1: Erstellen eines Backup-Konfigurationsobjekts
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 1 -RetentionCount 100 -Enabled $True
VERBOSE: ClientRequestId: 426a79ee-fed3-4d3d-9123-e371f83222b3_PS


BackupType     : CloudSnapshot
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 100
StartTime      : 2014-12-16T00:37:19+05:30
Status         : Enabled
```

Mit diesem Befehl wird ein Sicherungszeitplan-Basisobjekt für Cloud-Snapshot-Backups erstellt.
Die Sicherung erfolgt täglich, und die Sicherungen werden für 100 Tage aufbewahrt.
Dieser Zeitplan ist ab der Standardzeit, also der aktuellen Uhrzeit, aktiviert.

## Parameter

### -Backuptype
Gibt den Sicherungstyp an.
Gültige Werte sind: LocalSnapshot und CloudSnapshot.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Aktiviert
Gibt an, ob der Sicherungszeitplan aktiviert werden soll.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Gibt ein Azure-Profil an.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Serietype
Gibt den Typ der Serie für diesen Sicherungszeitplan an.
Gültige Werte sind: 

- Minuten
- Grenzen
- Täglich
- Wochen

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Seriewert
Gibt an, wie oft eine Sicherung erstellt werden soll.
Dieser Parameter verwendet die vom *Serientyp* -Parameter angegebene Einheit.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetentionCount
Gibt die Anzahl der Tage an, für die eine Sicherung aufbewahrt werden soll.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartFromDateTime
Gibt das Datum an, ab dem Sicherungskopien erstellt werden sollen.
Der Standardwert ist die aktuelle Uhrzeit.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### BackupScheduleBase
Dieses Cmdlet gibt ein **BackupScheduleBase** -Objekt zurück.
Verwenden Sie eine **BackupScheduleBase** , um neue Sicherungsrichtlinien zu erstellen.

## Notizen

## Verwandte Links

[Neu – AzureStorSimpleDeviceBackupScheduleUpdateConfig](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)

[Neu – AzureStorSimpleDeviceBackupPolicy](./New-AzureStorSimpleDeviceBackupPolicy.md)


