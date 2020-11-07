---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: b900e9b137c8268969ef1eb715f0b79356abc720
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825247"
---
# Remove-AzRecoveryServicesBackupProtectionPolicy

## Synopsis
Löscht eine Sicherungsschutz Richtlinie aus einem Tresor.

## Syntax

### Richtlinienwert (Standard)
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Richtlinienobject
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzRecoveryServicesBackupProtectionPolicy** löscht Sicherungsrichtlinien für einen Tresor.
Bevor Sie eine Sicherungsschutz Richtlinie löschen können, darf die Richtlinie keine zugeordneten Sicherungselemente enthalten.
Bevor Sie die Richtlinie löschen, stellen Sie sicher, dass jedes zugeordnete Element einer anderen Richtlinie zugeordnet ist.
Verwenden Sie das Enable-AzRecoveryServicesBackupProtection-Cmdlet, um eine andere Richtlinie einem Sicherungselement zuzuordnen.
Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.

## Beispiele

### Beispiel 1: Entfernen einer Richtlinie
```
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

Der erste Befehl ruft die Sicherungsschutz Richtlinie mit dem Namen "Richtlinie" ab und speichert Sie dann in der $Pol-Variablen.
Der zweite Befehl entfernt das Richtlinienobjekt in $Pol.

## Parameter

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

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen der zu entfernenden Sicherungsschutz Richtlinie an.

```yaml
Type: System.String
Parameter Sets: PolicyName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Gibt die zu löschende Richtlinie zurück.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Richtlinien
Gibt die zu entfernende Sicherungsschutz Richtlinie an.
Verwenden Sie das Get-AzRecoveryServicesBackupProtectionPolicy-Cmdlet, um ein **BackupPolicy** -Objekt zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. PolicyBase

### System. String

## Ausgaben

### Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. PolicyBase

## Notizen

## Verwandte Links

[Get-AzRecoveryServicesBackupProtectionPolicy](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[Neu – AzRecoveryServicesBackupProtectionPolicy](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[Satz-AzRecoveryServicesBackupProtectionPolicy](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


