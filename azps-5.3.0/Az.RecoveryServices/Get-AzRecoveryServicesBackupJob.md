---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 623acc7d96fc6c3dc4f1496f42a53bf276f8e778
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470365"
---
# Get-AzRecoveryServicesBackupJob

## SYNOPSIS

Ruft Sicherungsaufträge ab.

## SYNTAX

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG

Das **Cmdlet "Get-AzRecoveryServicesBackupJob"** ruft Azure -Sicherungsaufträge für einen bestimmten Tresor ab.
Legen Sie den Tresorkontext mithilfe des Parameters "-VaultId" ein.

## BEISPIELE

### Beispiel 1: Alle in Bearbeitung ausgeführten Aufträge erhalten

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

Der erste Befehl ruft den Status einer in Bearbeitung ausgeführten Aufträge als Array ab und speichert ihn dann in der $Joblist Variable.
Der zweite Befehl zeigt das erste Element in der $Joblist an.

### Beispiel 2: Alle fehlgeschlagenen Aufträge in den letzten 7 Tagen erhalten

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

Dieser Befehl ruft fehlgeschlagene Aufträge aus der letzten Woche im Tresor ab.
Der *Parameter "Von"* gibt eine in UTC angegebene Zeit von sieben Tagen in der Vergangenheit an.
Der Befehl gibt keinen Wert für den Parameter *"An"* an.
Daher wird der Standardwert der aktuellen Uhrzeit verwendet.

### Beispiel 3: Erhalten eines in Bearbeitung ausgeführten Auftrags und Warten auf den Abschluss

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
$Job = $Jobs[0]
While ( $Job.Status -ne Completed ) {
    Write-Host -Object "Waiting for completion..."
    Start-Sleep -Seconds 10
    $Job = Get-AzRecoveryServicesBackupJob -Job $Job -VaultId $vault.ID
}
Write-Host -Object "Done!"

Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

Dieses Skript abruft den ersten Auftrag, der derzeit ausgeführt wird, bis der Auftrag abgeschlossen ist.

Hinweis: Sie können das **Cmdlet "Wait-AzRecoveryServicesBackupJob"** verwenden, um auf den Abschluss eines Azure -Sicherungsauftrags zu warten, anstatt eine While-Schleife zu verwenden.

### Beispiel 4: Alle AzureVM-Aufträge in den letzten 2 Tagen erhalten, die erfolgreich abgeschlossen wurden

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
Das erste Cmdlet ruft das Tresorobjekt ab. Das zweite Cmdlet speichert alle AzureVM-Aufträge im angegebenen Tresor, der in den letzten 2 Tagen abgeschlossen wurde, um $jobs. Ändern Sie den Wert des Parameters "BackupManagementType" in MAB, um die MAB-Agentaufträge abrufen zu können.

## PARAMETERS

### -BackupManagementType

Die Klasse der geschützten Ressourcen. Derzeit werden für dieses Cmdlet AzureVM, AzureStorage, AzureWorkload und MAB unterstützt.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload, MAB

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile

Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Von

Gibt den Anfang (als **"DateTime"-Objekt)** eines Zeitbereichs für die Aufträge an, die dieses Cmdlet erhält.
Verwenden Sie das Get-Date-Cmdlet, um ein **"DateTime"-Objekt** zu erhalten. 
Weitere Informationen zu **"DateTime"-Objekten** erhalten Sie, wenn Sie `Get-Help Get-Date` ".
Verwenden Sie das UTC-Format für Datumsangaben.

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

Gibt den zu erhaltenden Auftrag an.

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
Die ID ist die "JobId"-Eigenschaft eines **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase-Objekts.**

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

### -Operation

Gibt einen Vorgang der Aufträge an, die dieses Cmdlet erhält.
Die zulässigen Werte für diesen Parameter sind:

- Sicherung
- ConfigureBackup
- DeleteBackupData
- DisableBackup
- Wiederherstellen
- BackupDataMove

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
Die zulässigen Werte für diesen Parameter sind:

- InProgress
- Fehler
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

Gibt das Ende eines  Zeitraumes für die Aufträge an, die dieses Cmdlet erhält.
Der Standardwert ist die aktuelle Systemzeit.
Wenn Sie diesen Parameter angeben, müssen Sie auch den Parameter **"-From"** angeben.
Verwenden Sie das UTC-Format für Datumsangaben.

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

### -VaultId

ARM-ID des Wiederherstellungsdienste-Tresors.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzRecoveryServicesBackupJobDetail](./Get-AzRecoveryServicesBackupJobDetail.md)

[Stop-AzRecoveryServicesBackupJob](./Stop-AzRecoveryServicesBackupJob.md)

[Wait-AzRecoveryServicesBackupJob](./Wait-AzRecoveryServicesBackupJob.md)
