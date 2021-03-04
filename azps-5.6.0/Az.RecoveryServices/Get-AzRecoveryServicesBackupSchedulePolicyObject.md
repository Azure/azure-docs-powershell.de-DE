---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 5bf91aafffb1c6fd650b5fd88f343897afc6c5d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932331"
---
# Get-AzRecoveryServicesBackupSchedulePolicyObject

## SYNOPSIS
Ruft ein Basiszeitplanrichtlinienobjekt ab.

## SYNTAX

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzRecoveryServicesBackupSchedulePolicyObject-Cmdlet** ruft ein **AzureRMRecoveryServicesSchedulePolicyObject ab.**
Dieses Objekt wird im System nicht beibehalten.
Es ist ein temporäres Objekt, das Sie bearbeiten und mit dem New-AzRecoveryServicesBackupProtectionPolicy verwenden können, um eine neue Sicherungsschutzrichtlinie zu erstellen.

## BEISPIELE

### Beispiel 1: Festlegen der Zeitplanhäufigkeit auf wöchentlich
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Der erste Befehl ruft das Aufbewahrungsrichtlinienobjekt ab und speichert es dann in der $RetPol-Variable.
Der zweite Befehl ruft das Richtlinienobjekt des Zeitplans ab und speichert es dann in der $SchPol Variablen.
Mit dem dritten Befehl wird die Häufigkeit für die Zeitplanrichtlinie in wöchentlich geändert.
Mit dem letzten Befehl wird eine Sicherungsschutzrichtlinie mit dem aktualisierten Zeitplan erstellt.

### Beispiel 2: Festlegen der Sicherungszeit
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Der erste Befehl ruft das Richtlinienobjekt des Zeitplans ab und speichert es dann in der $SchPol Variablen.
Mit dem zweiten Befehl werden alle geplanten Laufzeiten aus $SchPol.
Der dritte Befehl ruft das aktuelle Datum und die aktuelle Uhrzeit ab und speichert ihn dann in der $DT Variablen.
Der vierte Befehl ersetzt die geplanten Laufzeiten durch die aktuelle Uhrzeit.
Sie können AzureVM nur einmal pro Tag sichern. Um also die Sicherungszeit zurückzusetzen, müssen Sie den ursprünglichen Zeitplan ersetzen.
Mit dem letzten Befehl wird mithilfe des neuen Zeitplans eine Sicherungsschutzrichtlinie erstellt.

## PARAMETER

### -BackupManagementType
Die Klasse der zu schützenden Ressourcen. Die zulässigen Werte für diesen Parameter sind:
- AzureVM 
- AzureStorage
- AzureWorkload

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -WorkloadType
Arbeitsauslastungstyp der Ressource. Die zulässigen Werte für diesen Parameter sind:
- AzureVM 
- AzureFiles
- MSSQL


```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase

## NOTIZEN

## VERWANDTE LINKS

[New-AzRecoveryServicesBackupProtectionPolicy](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[Set-AzRecoveryServicesBackupProtectionPolicy](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


