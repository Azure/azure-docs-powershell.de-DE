---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: d66b8515c6b2c3782c6f6c2b49d462dbb7bd1660
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160188"
---
# Get-AzRecoveryServicesBackupSchedulePolicyObject

## SYNOPSIS
Ruft ein Basisplanrichtlinienobjekt ab.

## SYNTAX

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzRecoveryServicesBackupSchedulePolicyObject"** ruft eine Basisversion von **AzureRMRecoveryServicesSchedulePolicyObject ab.**
Dieses Objekt wird nicht im System beibehalten.
Es ist ein temporäres Objekt, das Sie bearbeiten und mit dem New-AzRecoveryServicesBackupProtectionPolicy verwenden können, um eine neue Sicherungsschutzrichtlinie zu erstellen.

## BEISPIELE

### Beispiel 1: Festlegen der Terminplanhäufigkeit auf "Wöchentlich"
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Der erste Befehl ruft das Aufbewahrungsrichtlinienobjekt ab und speichert es dann in der $RetPol Variable.
Der zweite Befehl ruft das Zeitplanrichtlinienobjekt ab und speichert es dann in der $SchPol Variable.
Mit dem dritten Befehl wird die Häufigkeit für die Zeitplanrichtlinie in "Wöchentlich" geändert.
Der letzte Befehl erstellt eine Sicherungsschutzrichtlinie mit dem aktualisierten Zeitplan.

### Beispiel 2: Festlegen der Sicherungszeit
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Der erste Befehl ruft das Zeitplanrichtlinienobjekt ab und speichert es dann in der $SchPol Variable.
Der zweite Befehl entfernt alle geplanten Laufzeiten aus $SchPol.
Der dritte Befehl ruft das aktuelle Datum und die aktuelle Uhrzeit ab und speichert ihn dann in der $DT Variable.
Der vierte Befehl ersetzt die geplanten Laufzeiten durch die aktuelle Uhrzeit.
Da Sie AzureVM nur einmal pro Tag sichern können, müssen Sie den ursprünglichen Zeitplan ersetzen, um die Sicherungszeit zurückzusetzen.
Der letzte Befehl erstellt eine Sicherungsschutzrichtlinie mit dem neuen Zeitplan.

## PARAMETERS

### -BackupManagementType
Die Klasse der geschützten Ressourcen. Die zulässigen Werte für diesen Parameter sind:
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzRecoveryServicesBackupProtectionPolicy](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[Set-AzRecoveryServicesBackupProtectionPolicy](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


