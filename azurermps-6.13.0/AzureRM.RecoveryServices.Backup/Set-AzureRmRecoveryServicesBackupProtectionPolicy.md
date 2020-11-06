---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/set-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: fb0373e97d719535c87c01c0a4b53b029cc2a878
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500146"
---
# Set-AzureRmRecoveryServicesBackupProtectionPolicy

## Synopsis
Ändert eine Sicherungsschutz Richtlinie.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase>
 [[-RetentionPolicy] <RetentionPolicyBase>] [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **festlegen-AzureRmBackupProtectionPolicy** " ändert eine vorhandene Azure Backup-Schutzrichtlinie.
Sie können die Komponenten für den Sicherungszeitplan und die Aufbewahrungsrichtlinie ändern.
Alle Änderungen, die Sie vornehmen, wirken sich auf die Sicherung und Aufbewahrung der Elemente aus, die der Richtlinie zugeordnet sind.
Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.

## Beispiele

### Beispiel 1: Ändern einer Sicherungsschutz Richtlinie
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

Der erste Befehl ruft ein Basis SchedulePolicy-Objekt ab und speichert es dann in der $SchPol-Variablen.
Der zweite Befehl entfernt alle geplanten Ausführungszeiten aus der Terminplan Richtlinie in $SchPol.
Der dritte Befehl verwendet das Get-Date-Cmdlet, um das aktuelle Datum und die aktuelle Uhrzeit abzurufen, und speichert es dann in der $dt-Variablen.
Der vierte Befehl addiert das Datum und die Uhrzeit in $dt zur Zeit Plan Laufzeit für die Terminplan Richtlinie.
Der fünfte Befehl ruft ein Basis Aufbewahrungsrichtlinienobjekt ab und speichert es dann in der $RetPol Variablen.
Der sechste Befehl legt die Aufbewahrungsdauer auf 365 Tage fest.
Der siebte Befehl ruft die Sicherungsschutz Richtlinie mit dem Namen "Richtlinie" ab und speichert Sie dann in der $Pol-Variablen.
Der endgültige Befehl ändert die Richtlinie für den Sicherungsschutz in $Pol mithilfe der Zeit Plan Richtlinie in $SchPol und der Aufbewahrungsrichtlinie in $RetPol.

## Parameter

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

### – Richtlinien
Gibt die Richtlinie für den Sicherungsschutz an, die von diesem Cmdlet geändert wird.
Verwenden Sie das Get-AzureRmRecoveryServicesBackupProtectionPolicy-Cmdlet, um ein **BackupProtectionPolicy** -Objekt zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RetentionPolicy
Gibt die Basis Aufbewahrungsrichtlinie an.
Verwenden Sie das Get-AzureRmRecoveryServicesBackupRetentionPolicyObject-Cmdlet, um ein **RetentionPolicy** -Objekt zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SchedulePolicy
Gibt das Basis Zeitplan-Richtlinienobjekt an.
Verwenden Sie zum Abrufen eines **SchedulePolicy** -Objekts das Get-AzureRmRecoveryServicesBackupSchedulePolicyObject-Objekt.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
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

### Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. PolicyBase
Parameter: Richtlinie (ByValue)

### System. String
Parameter: Vault-ByValue

## Ausgaben

### Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase

## Notizen

## Verwandte Links

[Get-AzureRmRecoveryServicesBackupProtectionPolicy](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Get-AzureRmRecoveryServicesBackupRetentionPolicyObject](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[Neu – AzureRmRecoveryServicesBackupProtectionPolicy](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Remove-AzureRmRecoveryServicesBackupProtectionPolicy](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)


