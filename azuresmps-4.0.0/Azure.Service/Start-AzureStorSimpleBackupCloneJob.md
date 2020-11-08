---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 403AD2BF-5D03-4B48-A635-E08216FFFC0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07df96f59b2278d804312d1076965ffed43c2569
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005954"
---
# Start-AzureStorSimpleBackupCloneJob

## Synopsis
Startet einen Auftrag, der eine Sicherung auf einem Gerät klont.

## Syntax

### Leer (Standard)
```
Start-AzureStorSimpleBackupCloneJob -BackupId <String> -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceName <String> -TargetDeviceName <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceId <String> -TargetDeviceId <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Start-AzureStorSimpleBackupCloneJob** wird ein Auftrag gestartet, der eine vorhandene Sicherung auf einem StorSimple-Gerät klont.

## Beispiele

### Beispiel 1: Klonen einer Sicherung auf ein anderes Volume mithilfe von Gerätenamen
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07 -TargetDeviceName "ContosoDev07" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

Der erste Befehl ruft mit dem Cmdlet **Get-AzureStorSimpleDeviceBackup** die erste Sicherung für das Gerät mit dem Namen ContosoDev07 ab.
Der Befehl speichert diese Sicherung in der $Backup-Variablen.

Der zweite Befehl ruft Zugriffssteuerungseinträge mit dem Cmdlet **Get-AzureStorSimpleAccessControlRecord** ab.
Der Befehl speichert das Ergebnis in der $ACRS-Variablen.

Mit dem letzten Befehl wird ein Auftrag gestartet, der eine angegebene Sicherung eines Volumes auf einem Gerät auf ein anderes Volume auf dem gleichen Gerät klont.
In diesem Beispiel wird der Name des Geräts angegeben.
Der Befehl verwendet die Werte, die in $Backup und $ACRS gespeichert sind.
Der Befehl gibt die ID des Auftrags zurück.

### Beispiel 2: Klonen einer Sicherung auf ein anderes Volume mithilfe von Geräte-IDs
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev07 -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -TargetDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

Der erste Befehl ruft mit dem Cmdlet **Get-AzureStorSimpleDeviceBackup** die erste Sicherung für das Gerät mit dem Namen ContosoDev07 ab.
Der Befehl speichert diese Sicherung in der $Backup-Variablen.

Der zweite Befehl ruft Zugriffssteuerungseinträge mit dem Cmdlet **Get-AzureStorSimpleAccessControlRecord** ab.
Der Befehl speichert das Ergebnis in der $ACRS-Variablen.

Mit dem letzten Befehl wird ein Auftrag gestartet, der eine angegebene Sicherung eines Volumes auf einem Gerät auf ein anderes Volume auf dem gleichen Gerät klont.
In diesem Beispiel wird das Gerät nach Geräte-ID angegeben.
Der Befehl verwendet die Werte, die in $Backup und $ACRS gespeichert sind.
Der Befehl gibt die ID des Auftrags zurück.

### Beispiel 3: Klonen einer Sicherung auf ein Volume auf einem anderen Gerät mithilfe von Gerätenamen
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07" -TargetDeviceName "ContosoDev12" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

Der erste Befehl ruft mit dem Cmdlet **Get-AzureStorSimpleDeviceBackup** die erste Sicherung für das Gerät mit dem Namen ContosoDev07 ab.
Der Befehl speichert diese Sicherung in der $Backup-Variablen.

Der zweite Befehl ruft Zugriffssteuerungseinträge mit dem Cmdlet **Get-AzureStorSimpleAccessControlRecord** ab.
Der Befehl speichert das Ergebnis in der $ACRS-Variablen.

Mit dem letzten Befehl wird ein Auftrag gestartet, der eine angegebene Sicherung eines Volumes auf einem Gerät auf ein Volume auf einem anderen Gerät klont.
In diesem Beispiel werden die Geräte nach Namen angegeben.
Der Befehl verwendet die Werte, die in $Backup und $ACRS gespeichert sind.
Der Befehl gibt die ID des Auftrags zurück.

### Beispiel 4: Klonen einer Sicherung auf ein anderes Volume mithilfe von Gerätenamen und dem Pipelineoperator
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev1 -First 1
PS C:\> Get-AzureStorSimpleAccessControlRecord -ACRName acr1 | Start-AzureStorSimpleBackupCloneJob -SourceDeviceName ContosoDev1 -TargetDeviceName ContosoDev1 -BackupId $backup.InstanceId -Snapshot $backup.Snapshots[0] -CloneVolumeName "cloned_vol1" 
VERBOSE: ClientRequestId: 1183a29d-63a9-408a-9065-032c92d317ee_PS
VERBOSE: ClientRequestId: e195717c-5920-4133-bdf0-c1201ebabf6f_PS
VERBOSE: ClientRequestId: ac16644d-bfd8-4edf-b1ad-f5df4ceb4df7_PS
VERBOSE: ClientRequestId: dcdcab7f-2aaa-496d-8a18-2e7449a70227_PS
VERBOSE: ClientRequestId: 6f92e422-eda9-4087-aefb-2257a49f5beb_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 646b280c-b51c-4812-b5c5-b7ca215f1c90_PS
a747d2dc-2876-474e-aea6-6546b255427e
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId a747d2dc-2876-474e-aea6-6546b255427e for tracking the job's status
VERBOSE: Access Control Record with given name acr11 is found!
```

Der erste Befehl ruft mit dem Cmdlet **Get-AzureStorSimpleDeviceBackup** die erste Sicherung für das Gerät mit dem Namen ContosoDev07 ab.
Der Befehl speichert diese Sicherung in der $Backup-Variablen.

Der zweite Befehl ruft Zugriffssteuerungseinträge mit dem Cmdlet **Get-AzureStorSimpleAccessControlRecord** ab.
Der Befehl übergibt seine Ergebnisse mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet beginnt einen Auftrag, der eine angegebene Sicherung eines Volumes auf einem Gerät auf ein anderes Volume auf demselben Gerät klont.
In diesem Beispiel wird der Name des Geräts angegeben.
Der Befehl verwendet den in $Backup gespeicherten Wert.
Der Befehl übernimmt den Wert des *TargetAccessControlRecords* -Parameters aus der Pipeline.
Der Befehl gibt die ID des Auftrags zurück.

## Parameter

### -Backup-Nr.
Gibt die Instanz-ID des zu klonenden Backups an.

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

### -CloneVolumeName
Gibt den Namen des neuen geklonten Volumes auf dem Zielgerät an.

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

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

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

### -Schnappschuss
Gibt das Snapshot-Objekt an, das dieses Cmdlet klont.

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDeviceId
Gibt die Instanz-ID des Quellgeräts an.
Dieses Cmdlet klont die Rückseite des Quellgeräts.

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

### -SourceDeviceName
Gibt den Namen des Quellgeräts an.
Dieses Cmdlet klont die Rückseite des Quellgeräts.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetAccessControlRecords
Gibt die Zugriffssteuerungsdaten Sätze an.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TargetDeviceId
Gibt die Instanz-ID des Zielgeräts an.

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

### -TargetDeviceName
Gibt den Namen des Geräts an, auf das dieses Cmdlet die Sicherung klont.

```yaml
Type: String
Parameter Sets: IdentifyByName
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

### Schnappschuss, Liste der AccessControlRecord
Sie können **Snapshot** -Objekte oder eine Liste von **AccessControlRecord** -Objekten an dieses Cmdlet übergeben.

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureStorSimpleDeviceBackup](./Get-AzureStorSimpleDeviceBackup.md)

[Get-AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)


