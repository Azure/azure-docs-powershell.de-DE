---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 3fb6b89f5708c951731c45e0d32e0f7a379cf754
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504798"
---
# Get-AzureRmRecoveryServicesBackupJob

## Synopsis
Ruft Backup-Aufträge ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmRecoveryServicesBackupJob** " ruft Azure Backup-Aufträge für einen bestimmten Tresor ab.

Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.

## Beispiele

### Beispiel 1: Abrufen aller in Bearbeitung befindlichen Aufträge
```
PS C:\>$Joblist = Get-AzureRMRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

Der erste Befehl ruft den Status eines in Bearbeitung befindlichen Auftrags als Array ab und speichert ihn dann in der $jobList Variablen.

Der zweite Befehl zeigt das erste Element im $jobList-Array an.

### Beispiel 2: Abrufen aller fehlgeschlagenen Aufträge in den letzten 7 Tagen
```
PS C:\>Get-AzureRmRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

Dieser Befehl ruft fehlerhafte Aufträge aus der letzten Woche im Tresor ab.
Der Parameter " *from* " gibt an, welche Uhrzeit sieben Tage in der Vergangenheit in UTC angegeben sind.
Der Befehl gibt keinen Wert für den Parameter " *to" an* .
Daher wird der Standardwert für die aktuelle Uhrzeit verwendet.

### Beispiel 3: Abrufen eines in Bearbeitung befindlichen Auftrags und warten auf den Abschluss
```
PS C:\> 
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

Dieses Skript ruft den ersten Job ab, der gerade ausgeführt wird, bis der Auftrag abgeschlossen ist.

## Parameter

### -BackupManagementType
Gibt den Sicherungs Verwaltungstyp an.
Derzeit wird nur AzureVM unterstützt.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ab
Gibt den Anfang als **DateTime** -Objekt eines Zeitbereichs für die Aufträge an, die dieses Cmdlet erhält.
Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt zu erhalten.
Wenn Sie weitere Informationen zu **DateTime** -Objekten wünschen, geben Sie `Get-Help Get-Date` .
Verwenden des UTC-Formats für Datumsangaben

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Gibt den Namen des abzurufenden Sicherungsauftrags an.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Gibt die ID eines Auftrags an, den dieses Cmdlet erhält.
Die ID ist die InstanceId-Eigenschaft eines **AzureRmRecoveryServicesBackupJob** -Objekts.
Verwenden Sie Get-AzureRmRecoveryServicesBackupJob, um ein **AzureRmRecoveryServicesBackupJob** -Objekt zu erhalten.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vorgang
Gibt einen Vorgang der Aufträge an, die dieses Cmdlet erhält.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Backup
- ConfigureBackup
- DeleteBackupData
- Registrieren
- Wiederherstellungs
- Schutz aufheben
- Registrierung

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobOperation]
Parameter Sets: (All)
Aliases: 
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Gibt den Status der Aufträge an, die dieses Cmdlet erhält.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- InProgress
- Fehlgeschlagen
- Storniert
- Abbrechen
- Abgeschlossen
- CompletedWithWarnings

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobStatus]
Parameter Sets: (All)
Aliases: 
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -To
Gibt das Ende als **DateTime** -Objekt eines Zeitbereichs für die Aufträge an, die dieses Cmdlet erhält.
Der Standardwert ist die aktuelle Systemzeit.
Wenn Sie diesen Parameter angeben, müssen Sie auch den *from* -Parameter angeben.
Verwenden des UTC-Formats für Datumsangaben

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase

### System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase]

## Notizen

## Verwandte Links

[Get-AzureRmRecoveryServicesBackupJobDetails](./Get-AzureRmRecoveryServicesBackupJobDetails.md)

[Stopp-AzureRmRecoveryServicesBackupJob](./Stop-AzureRmRecoveryServicesBackupJob.md)

[Wait-AzureRmRecoveryServicesBackupJob](./Wait-AzureRmRecoveryServicesBackupJob.md)


