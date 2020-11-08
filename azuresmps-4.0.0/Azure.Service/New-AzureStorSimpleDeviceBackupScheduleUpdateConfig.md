---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 22C6845E-D7BD-4BBC-B373-394A23488A94
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0695dc42d9c540e30ddf9ac55bd6fc136c84bff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005730"
---
# New-AzureStorSimpleDeviceBackupScheduleUpdateConfig

## Synopsis
Erstellt ein Konfigurationsobjekt für das Aktualisierungszeitplan-Update.

## Syntax

```
New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id <String> -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] [-Enabled <Boolean>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** wird ein **BackupScheduleUpdateRequest** -Konfigurationsobjekt erstellt.
Verwenden Sie dieses Konfigurationsobjekt, um eine Sicherungsrichtlinie mithilfe des Cmdlets " **festlegen-AzureStorSimpleDeviceBackupPolicy** " zu aktualisieren.

## Beispiele

### Beispiel 1: Erstellen einer Aktualisierungsanforderung für einen Zeitplan
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "147f734d-a31a-4473-8501-6ba38be2cb30" -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 50 -Enabled $True
VERBOSE: ClientRequestId: ef346641-54b4-4273-8898-7f863e7c5b7e_PS


BackupType     : CloudSnapshot
Id             : 147f734d-a31a-4473-8501-6ba38be2cb30
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 50
StartTime      : 2014-12-16T00:39:32+05:30
Status         : Enabled
```

Mit diesem Befehl wird eine Aktualisierungsanforderung für den Terminplan für den Zeitplan erstellt, die die angegebene ID aufweist.
Die Anforderung besteht darin, den Zeitplan zu einer Cloud-Snapshot-Sicherung zu machen, die stündlich wiederholt wird.
Die Sicherungen werden für 50 Tage aufbewahrt.
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

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Gibt die Instanz-ID des zu aktualisierende Backup-Zeitplans an.

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

### BackupScheduleUpdateRequest
Dieses Cmdlet gibt ein **BackupScheduleUpdateRequest** -Objekt zurück, das Informationen zu aktualisierten Sicherungszeitplänen enthält.

## Notizen

## Verwandte Links

[Neu – AzureStorSimpleDeviceBackupScheduleAddConfig](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)

[Satz-AzureStorSimpleDeviceBackupPolicy](./Set-AzureStorSimpleDeviceBackupPolicy.md)


