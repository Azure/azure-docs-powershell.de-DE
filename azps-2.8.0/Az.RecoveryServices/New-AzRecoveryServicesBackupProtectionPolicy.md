---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 6aaf7fcd32ae7d50f273d69835f9131032b68c21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825284"
---
# New-AzRecoveryServicesBackupProtectionPolicy

## Synopsis
Erstellt eine Sicherungsschutz Richtlinie.

## Syntax

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzRecoveryServicesBackupProtectionPolicy** erstellt eine Sicherungsschutz Richtlinie in einem Tresor.
Eine Schutzrichtlinie ist mit mindestens einer Aufbewahrungsrichtlinie verbunden.
Die Aufbewahrungsrichtlinie definiert, wie lange ein Wiederherstellungspunkt mit Azure-Sicherung beibehalten wird.
Sie können das Get-AzRecoveryServicesBackupRetentionPolicyObject-Cmdlet verwenden, um die Standardaufbewahrungsrichtlinie abzurufen.
Und Sie können das Get-AzRecoveryServicesBackupSchedulePolicyObject-Cmdlet verwenden, um die standardmäßige Terminplan Richtlinie abzurufen.
Die Objekte **SchedulePolicy** und **RetentionPolicy** werden als Eingaben für das Cmdlet **New-AzRecoveryServicesBackupProtectionPolicy** verwendet.
Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.

## Beispiele

### Beispiel 1: Erstellen einer Sicherungsschutz Richtlinie
```
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Der erste Befehl ruft einen Basis- **SchedulePolicyObject** ab und speichert ihn dann in der $SchPol-Variablen.
Der zweite Befehl entfernt alle geplanten Ausführungszeiten aus der Terminplan Richtlinie in $SchPol.
Der dritte Befehl verwendet das Get-Date-Cmdlet, um das aktuelle Datum und die aktuelle Uhrzeit abzurufen.
Der vierte Befehl addiert das aktuelle Datum und die aktuelle Uhrzeit in $dt als geplante Laufzeit zur Zeit Plan Richtlinie.
Der fünfte Befehl ruft ein Basis **RetentionPolicy** -Objekt ab und speichert es dann in der $RetPol-Variablen.
Der sechste Befehl legt die Richtlinie für die Aufbewahrungsdauer auf 365 Tage fest.
Der endgültige Befehl erstellt ein **BackupProtectionPolicy** -Objekt basierend auf den von den vorherigen Befehlen erstellten Plan-und Aufbewahrungsrichtlinien.

## Parameter

### -BackupManagementType
Gibt den Sicherungs Verwaltungstyp an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- AzureVM 
- AzureSQLDatabase

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Name
Gibt den Namen der Richtlinie an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetentionPolicy
Gibt das Basis **RetentionPolicy** -Objekt an.
Sie können das Get-AzRecoveryServicesBackupRetentionPolicyObject-Cmdlet verwenden, um ein **RetentionPolicy** -Objekt abzurufen.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SchedulePolicy
Gibt das Basis **SchedulePolicy** -Objekt an.
Sie können das Get-AzRecoveryServicesBackupSchedulePolicyObject-Cmdlet verwenden, um ein **SchedulePolicy** -Objekt abzurufen.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tresor
Arm-ID des Speichers für Wiederherstellungsdienste

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

### -Workloadtype
Gibt den Arbeits Auslastungs an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- AzureVM 
- AzureSQLDatabase

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. workloadtype

### System. Nullable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. BackupManagementType, Microsoft. Azure. PowerShell. Cmdlets. RecoveryServices. Backup. Models, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]

### Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RetentionPolicyBase

### Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. SchedulePolicyBase

### System. String

## Ausgaben

### Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. PolicyBase

## Notizen

## Verwandte Links

[Enable-AzRecoveryServicesBackupProtection](./Enable-AzRecoveryServicesBackupProtection.md)

[Get-AzRecoveryServicesBackupProtectionPolicy](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[Get-AzRecoveryServicesBackupRetentionPolicyObject](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[Get-AzRecoveryServicesBackupSchedulePolicyObject](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[Remove-AzRecoveryServicesBackupProtectionPolicy](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[Satz-AzRecoveryServicesBackupProtectionPolicy](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


