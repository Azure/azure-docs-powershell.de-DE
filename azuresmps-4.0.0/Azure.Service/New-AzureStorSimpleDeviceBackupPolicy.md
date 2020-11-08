---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EFAE7117-9B8B-4CB9-B4D9-3F08DCE1816E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 405b9d427c7e59dfb3628806a878d57a281a6b4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006414"
---
# New-AzureStorSimpleDeviceBackupPolicy

## Synopsis
Erstellt eine Sicherungsrichtlinie.

## Syntax

```
New-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyName <String>
 -BackupSchedulesToAdd <PSObject[]> -VolumeIdsToAdd <PSObject[]> [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureStorSimpleDeviceBackupPolicy** erstellt eine Sicherungsrichtlinie.
Eine Sicherungsrichtlinie enthält mindestens einen Sicherungszeitplan, der auf einem oder mehreren Volumes ausgeführt werden kann.
Verwenden Sie zum Erstellen eines Sicherungszeitplans das Cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .

## Beispiele

### Beispiel 1: Erstellen einer Sicherungsrichtlinie
```
PS C:\>$Schedule01 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType LocalSnapshot -RecurrenceType Daily -RecurrenceValue 10 -RetentionCount 5 -Enabled $True
PS C:\> $Schedule02 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 5 -Enabled $True
PS C:\> $ScheduleArray = @()
PS C:\> $ScheduleArray += $Schedule01
PS C:\> $ScheduleArray += $Schedule02
PS C:\> $DeviceContainer = Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm"
PS C:\> $Volume = $(Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeContainer $DeviceContainer[0])
PS C:\> $VolumeArray = @()
PS C:\> $VolumeArray += $Volume[0].InstanceId
PS C:\> New-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "GeneralPolicy07" -BackupSchedulesToAdd $ScheduleArray -VolumeIdsToAdd $VolumeArray
VERBOSE: ClientRequestId: e9d6771e-c323-47b9-b424-cb98f8ed0273_PS
VERBOSE: ClientRequestId: db0e7c86-d0d2-4a5a-b1cb-182494cba027_PS
VERBOSE: ClientRequestId: 77708dfd-a386-4999-b7ed-5d53e288ae83_PS


JobId        : d4ce5340-d5d1-4471-9cc8-013193f021b3
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your add operation has completed successfully. 
VERBOSE: ClientRequestId: bbf7e9b9-b493-40b3-8348-f15bcfc4da8a_PS
BackupSchedules          : {36d21096-bbd1-47b7-91b5-40ad1792d992, 505fc91f-deb5-4dca-bfcb-98c20b75ebcc}
Volumes                  : {volume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 01-01-2010 05:30:00
NextBackup               : 16-12-2014 01:13:43
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : 8799c2f0-8850-4e91-aa23-ee18c67da8bd
Name                     : GeneralPolicy07
OperationInProgress      : None
```

Der erste Befehl erstellt mithilfe des Cmdlets **New-AzureStorSimpleDeviceBackupScheduleAddConfig** ein Konfigurationsobjekt für den Sicherungszeitplan und speichert dieses Objekt dann in der Variablen $Schedule 01.

Der zweite Befehl erstellt ein weiteres Backup-Konfigurationsobjekt mithilfe von **New-AzureStorSimpleDeviceBackupScheduleAddConfig** und speichert dieses Objekt dann in der Variablen $Schedule 02.

Der dritte Befehl erstellt eine leere Arrayvariable mit dem Namen $ScheduleArray.
Mit den nächsten beiden Befehlen werden die in den ersten beiden Befehlen erstellten Objekte $ScheduleArray hinzugefügt.

Der sechste Befehl ruft mithilfe des Cmdlets **Get-AzureStorSimpleDeviceVolumeContainer** einen Volumen Container für das Gerät mit dem Namen Contoso63-AppVm ab und speichert dann das Containerobjekt in der $DeviceContainer Variablen.

Der siebte Befehl ruft einen Datenträger für den Volumen Container ab, der im ersten Mitglied von $DeviceContainer mit dem Cmdlet **Get-AzureStorSimpleDeviceVolume** gespeichert ist, und speichert dann das Volume in der $Volume-Variablen.

Der achte Befehl erstellt eine leere Arrayvariable mit dem Namen $VolumeArray.
Mit dem nächsten Befehl wird $VolumeArray eine Volumen-ID hinzugefügt.
Dieser Wert gibt den in $Volume gespeicherten Datenträger an, auf dem die Sicherungsrichtlinie ausgeführt wird.
Sie können $VolumeArray weitere Volumen-IDs hinzufügen.

Der endgültige Befehl erstellt die Sicherungsrichtlinie mit dem Namen "GeneralPolicy07" für das Gerät mit dem Namen Contoso63-AppVm.
Der Befehl gibt die Plan Konfigurationsobjekte an, die in $ScheduleArray gespeichert sind.
Der Befehl gibt die Volumes an, auf die die Richtlinie in $VolumeArray angewendet werden soll.
Sie können die Sicherungsrichtlinie mit dem Cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** überprüfen.

## Parameter

### -BackupPolicyName
Gibt den Namen der Sicherungsrichtlinie an.

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

### -BackupSchedulesToAdd
Gibt ein Array von **BackupScheduleBase** -Objekten an, die der Richtlinie hinzugefügt werden sollen.
Jedes Objekt stellt einen Zeitplan dar.
Eine Sicherungsrichtlinie enthält einen oder mehrere Zeitpläne.
Verwenden Sie zum Abrufen eines **BackupScheduleBase** -Objekts das Cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Gibt den Namen des StorSimple-Geräts an, auf dem die Sicherungsrichtlinie erstellt werden soll.

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

### -VolumeIdsToAdd
Gibt ein Array der IDs von Volumes an, die der Sicherungsrichtlinie hinzugefügt werden sollen.

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForComplete
Gibt an, dass dieses Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.

```yaml
Type: SwitchParameter
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

### BackupPolicy
Dieses Cmdlet gibt ein **BackupPolicy** -Objekt zurück, das die neuen Zeitpläne und Volumes enthält.

## Notizen

## Verwandte Links

[Get-AzureStorSimpleDeviceBackupPolicy](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[Get-AzureStorSimpleDeviceVolume](./Get-AzureStorSimpleDeviceVolume.md)

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[Remove-AzureStorSimpleDeviceBackupPolicy](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[Satz-AzureStorSimpleDeviceBackupPolicy](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[Neu – AzureStorSimpleDeviceBackupScheduleAddConfig](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)


