---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A40879D2-371B-4CF1-BF1F-9E5C896EB89C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5ffe0a6e5a2d6ae181f4396eae2b5732f527843
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006496"
---
# Get-AzureStorSimpleDeviceBackup

## Synopsis
Ruft Sicherungen von einem Gerät ab.

## Syntax

### Leer (Standard)
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> [-From <String>] [-To <String>] [-First <Int32>]
 [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicyId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById2
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -VolumeId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-From <String>]
 [-To <String>] [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject2
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -Volume <VirtualDisk> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureStorSimpleDeviceBackup** " ruft Sicherungen von einem Gerät ab.
Sie können die Sicherungsrichtlinie, das Volume und die Erstellungszeit für Sicherungen angeben.

Dieses Cmdlet kann auf der ersten Seite maximal 100-Sicherungen zurückgeben.
Wenn mehr als 100-Sicherungen vorhanden sind, rufen Sie nachfolgende Seiten mithilfe des *First* -und *Skip* -Parameters ab.
Wenn Sie einen Wert von 100 für *Skip* und 50 für *First* angeben, gibt dieses Cmdlet nicht die ersten 100 Ergebnisse zurück.
Nach dem 100 werden die nächsten 50-Ergebnisse zurückgegeben, die übersprungen werden.

## Beispiele

### Beispiel 1: Abrufen aller Sicherungen auf einem Gerät
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
InstanceId                           Name                               Type          BackupJobCreationType              CreatedOn                          SizeInBytes                       Snapshots                         SSMHostName                      
----------                           ----                               ----          ---------------------              ---------                          -----------                       ---------                         -----------                      
85074062-ef6a-408a-b6c9-2a0904bb99ca Snapshot_vg-all                    LocalSnapshot BySchedule                         4/15/2015 1:30:02 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
ebd87fa3-a9e2-49c9-a7e6-dada47071544 Cloud_Snapshot_vg-all              CloudSnapshot BySchedule                         4/15/2015 11:30:02 AM              9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
9f7a03be-8c39-474c-bf88-b2c7b54e833c Cloud_Snapshot_Vol3_clone VG       CloudSnapshot BySchedule                         4/15/2015 9:00:03 AM               1717986918400                     {Volume 3 Clone}                                                   
177b2dad-c0b2-42d6-b7bb-16926e54e9c6 VG Clones                          CloudSnapshot BySchedule                         4/15/2015 8:30:02 AM               5016521801728                     {Volume 1 Clone, Volume 3 Clone}                                   
49c470c0-eadb-40ac-9928-94018a8edcd4 Cloud_Snapshot_Vol1_clone VG       CloudSnapshot BySchedule                         4/15/2015 7:30:02 AM               3298534883328                     {Volume 1 Clone}                                                   
45dfd283-f924-4b45-93eb-b20650cadf43 vg-all                             LocalSnapshot Adhoc                              3/27/2015 9:12:15 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
2c3dd48d-824c-4298-82b5-fb44abb67a1e Test Group                         LocalSnapshot Adhoc                              3/27/2015 1:47:00 AM               5016521801728                     {Volume 1, Volume 3}
```

Dieser Befehl ruft alle Sicherungen ab, die auf dem Gerät mit dem Namen Contoso63-AppVm vorhanden sind.
Wenn für die erste Seite mehr als maximal 100-Sicherungen zulässig sind, verwenden Sie die Parameter *First* und *Skip* , um weitere Ergebnisse anzuzeigen.

### Beispiel 2: Abrufen von Sicherungen, die zwischen zwei Datumsangaben erstellt wurden
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -From "9/7/2014" -To "10/7/2014" -First 2 -Skip 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/5/2014 11:00:04 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : ec2fdf5c-c807-4f7b-a942-d4c4a9b68c44
Name                  : ContosoTSQA_Default
BackupJobCreationType : BySchedule
CreatedOn             : 10/4/2014 11:00:06 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 5ac4f947-f4c6-4770-9000-2242e72fc6d3
Name                  : ContosoTSQA_DefaultVERBOSE: # of backups returned : 2
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 2 -Skip 3\" in
your commandlet
```

Dieser Befehl ruft Sicherungen auf dem Gerät mit dem Namen Contoso63-AppVm ab, die am oder nach 10/7/2014 und vor 10/8/2014 erstellt wurden.
Dieses Cmdlet überspringt das erste Ergebnis und gibt die ersten beiden Ergebnisse nach dem ersten Ergebnis zurück.
Ändern Sie die Werte für *First* , und *überspringen* Sie, um andere Ergebnisse anzuzeigen.

### Beispiel 3: Abrufen von Sicherungen für eine Sicherungsrichtlinien-ID
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

Dieser Befehl ruft Sicherungen auf dem Gerät mit dem Namen Contoso63-AppVm ab, die am oder vor dem angegebenen Datum erstellt wurden.
Der Befehl ruft Sicherungen ab, die mit der Sicherungsrichtlinie erstellt wurden, die die angegebene ID aufweist.
Dieser Befehl gibt den *ersten* Parameter an, sodass nur die ersten 10 Ergebnisse zurückgegeben werden.

### Beispiel 4: Abrufen von Sicherungen für ein sicherungsrichtlinienobjekt
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQATest_Default" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

Dieser Befehl ruft mit dem Cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** ein **BackupPolicyDetails** -Objekt ab und übergibt dieses Objekt dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Dieses Cmdlet ruft Sicherungen für das Gerät mit dem Namen Contoso63-AppVm ab, das mithilfe der Sicherungsrichtlinie aus dem ersten Teil des Befehls erstellt wurde.
Der Befehl ruft Sicherungen ab, die am oder vor dem angegebenen Datum erstellt wurden, genau wie im vorherigen Beispiel.
Dieser Befehl gibt nur die ersten 10 Ergebnisse zurück.

### Beispiel 5: Abrufen einer Sicherung für eine Volumen-ID
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -VolumeId "SS-VOL-246b9df1-11bb-4071-8043-f955cc406446" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

Dieser Befehl ruft eine Sicherung auf dem Gerät ab, die auf dem Datenträger mit der angegebenen Instanz-ID erstellt wird.
Dieser Befehl gibt den *ersten* Parameter an, sodass nur das erste Ergebnis zurückgegeben wird.

### Beispiel 6: Abrufen einer Sicherung für einen Datenträgernamen
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "TSQATest03" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

Dieser Befehl ruft mit dem Cmdlet **Get-AzureStorSimpleDeviceVolume** ein **VirtualDisk** -Objekt ab und übergibt dieses Objekt dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Dieses Cmdlet ruft Sicherungen für das Gerät mit dem Namen Contoso63-AppVm ab, das auf dem Volume aus dem ersten Teil des Befehls erstellt wurde.
Dieser Befehl gibt nur das erste Ergebnis zurück.

## Parameter

### -BackupPolicy
Gibt ein **BackupPolicyDetails** -Objekt an.
Dieses Cmdlet verwendet die **InstanceId** dieses Objekts, um zu ermitteln, welche Sicherungen abgerufen werden sollen.
Verwenden Sie das Cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** , um ein **BackupPolicyDetails** -Objekt abzurufen.

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: BackupPolicyDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BackupPolicyId
Gibt eine Instanz-ID einer Sicherungsrichtlinie an.
Dieses Cmdlet ruft Gerätesicherungen für Richtlinien ab, die dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Gibt den Namen des StorSimple-Geräts an, für das Sicherungen abgerufen werden sollen.

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

### -First
Ruft nur die angegebene Anzahl von Objekten ab.
Geben Sie die Anzahl der abzurufenden Objekte ein.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ab
Gibt das Startdatum und die Startzeit für die Sicherungen an, die dieses Cmdlet erhält.

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

### -Skip
Ignoriert die angegebene Anzahl von Objekten und ruft dann die restlichen Objekte ab.
Geben Sie die Anzahl der zu überspringenden Objekte ein.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -To
Gibt das Enddatum und die Endzeit für die Sicherungen an, die dieses Cmdlet erhält.

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

### -Lautstärke
Gibt ein **VirtualDisk** -Objekt an.
Dieses Cmdlet verwendet die **InstanceId** dieses Objekts, um das Volume zu ermitteln, in dem Sicherungen vorhanden sind.
Verwenden Sie zum Abrufen eines **VirtualDisk** -Objekts den **Get-AzureStorSimpleDeviceVolume-** Parameter.

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject2
Aliases: VirtualDiskInfo

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Volumen-Nr.
Gibt die Instanz-ID des Volumes an, in dem Sicherungen vorhanden sind.

```yaml
Type: String
Parameter Sets: IdentifyById2
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### BackupPolicyDetails, VirtualDisk
Dieses Cmdlet akzeptiert **BackupPolicyDetails** -und **VirtualDisk** -Objekte.

## Ausgaben

### IList\<Backup\>
Dieses Cmdlet gibt eine Liste von **Sicherungs** Objekten zurück.

## Notizen

## Verwandte Links

[Remove-AzureStorSimpleDeviceBackup](./Remove-AzureStorSimpleDeviceBackup.md)

[Get-AzureStorSimpleDeviceBackupPolicy](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[Get-AzureStorSimpleDeviceVolume](./Get-AzureStorSimpleDeviceVolume.md)


