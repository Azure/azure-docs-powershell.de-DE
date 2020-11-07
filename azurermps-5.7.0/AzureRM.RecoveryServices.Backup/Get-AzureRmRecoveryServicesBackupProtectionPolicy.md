---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 3220ef801ff86a3fb95a4595efd8c94330bfcba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662354"
---
# Get-AzureRmRecoveryServicesBackupProtectionPolicy

## Synopsis
Ruft Sicherungsschutz Richtlinien für einen Tresor ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Noparamet (Standard)
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicyNameParamSet
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### WorkloadParamSet
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WorkloadBackupManagementTypeParamSet
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmRecoveryServicesBackupProtectionPolicy** " ruft Azure-Sicherungsschutz Richtlinien für einen Tresor ab.

Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.

## Beispiele

### Beispiel 1: Abrufen aller Richtlinien im Tresor
```
PS C:\> Get-AzureRmRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

Dieser Befehl ruft alle im Tresor erstellten Schutzrichtlinien ab.

### Beispiel 2: Abrufen einer bestimmten Richtlinie
```
PS C:\> $Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

Dieser Befehl ruft die Schutzrichtlinie mit dem Namen DefaultPolicy ab und speichert Sie dann in der $Pol-Variablen.

## Parameter

### -BackupManagementType
Gibt den Sicherungs Verwaltungstyp an.
Derzeit wird nur AzureVM unterstützt.

```yaml
Type: BackupManagementType
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Richtlinie an.

```yaml
Type: String
Parameter Sets: PolicyNameParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Workloadtype
Gibt den Arbeits Auslastungs an.
Derzeit wird nur AzureVM unterstützt.

```yaml
Type: WorkloadType
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. PolicyBase

### System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. PolicyBase]

## Notizen

## Verwandte Links

[Neu – AzureRmRecoveryServicesBackupProtectionPolicy](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Remove-AzureRmRecoveryServicesBackupProtectionPolicy](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Satz-AzureRmRecoveryServicesBackupProtectionPolicy](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


