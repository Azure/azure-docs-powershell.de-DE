---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 71650d36c319536db5ad96aa142e2712e229d712
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659891"
---
# Get-AzRecoveryServicesBackupSchedulePolicyObject

## Synopsis
Ruft ein Basis Zeitplan-Richtlinienobjekt ab.

## Syntax

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzRecoveryServicesBackupSchedulePolicyObject** " Ruft eine Basis- **AzureRMRecoveryServicesSchedulePolicyObject** ab.
Dieses Objekt wird im System nicht beibehalten.
Es handelt sich um ein temporäres Objekt, das Sie mit dem New-AzRecoveryServicesBackupProtectionPolicy-Cmdlet bearbeiten und verwenden können, um eine neue Sicherungsschutz Richtlinie zu erstellen.

## Beispiele

### Beispiel 1: Festlegen der Häufigkeit "Zeitplan" auf "wöchentlich"
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Der erste Befehl ruft das Aufbewahrungsrichtlinienobjekt ab und speichert es dann in der $RetPol Variablen.
Der zweite Befehl ruft das Schedule-Richtlinienobjekt ab und speichert es dann in der $SchPol-Variablen.
Der dritte Befehl ändert die Häufigkeit der Zeit Plan Richtlinie in Weekly.
Der letzte Befehl erstellt eine Sicherungsschutz Richtlinie mit dem aktualisierten Zeitplan.

### Beispiel 2: Einrichten der Sicherungszeit
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Der erste Befehl ruft das Schedule-Richtlinienobjekt ab und speichert es dann in der $SchPol-Variablen.
Der zweite Befehl entfernt alle geplanten Ausführungszeiten von $SchPol.
Der dritte Befehl ruft das aktuelle Datum und die aktuelle Uhrzeit ab und speichert es dann in der $dt Variablen.
Der vierte Befehl ersetzt die geplanten Ausführungszeiten durch die aktuelle Uhrzeit.
Sie können AzureVM nur einmal pro Tag sichern, sodass Sie den ursprünglichen Zeitplan ersetzen müssen, um die Sicherungszeit zurückzusetzen.
Mit dem letzten Befehl wird eine Sicherungsschutz Richtlinie mit dem neuen Zeitplan erstellt.

## Parameter

### -BackupManagementType
Gibt den Sicherungs Verwaltungstyp an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- AzureVM 
- AzureSQLDatabase
- AzureStorage

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -Workloadtype
Gibt den Arbeits Auslastungs an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- AzureVM 
- AzureSQLDatabase
- AzureFiles

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. SchedulePolicyBase

## Notizen

## Verwandte Links

[Neu – AzRecoveryServicesBackupProtectionPolicy](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[Satz-AzRecoveryServicesBackupProtectionPolicy](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


