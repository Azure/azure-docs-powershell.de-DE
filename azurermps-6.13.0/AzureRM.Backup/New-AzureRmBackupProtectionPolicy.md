---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3A7B0280-CE6E-4374-87AF-4C1015EB88FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: ce4550d4b0b0206db3a28f11a58ac4384ecbac60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477974"
---
# New-AzureRmBackupProtectionPolicy

## Synopsis
Erstellt eine Sicherungsrichtlinie.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### NoScheduleParamSet (Standard)
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-BackupTime] <DateTime>
 [[-DaysOfWeek] <String[]>] [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DailyScheduleParamSet
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Daily] [-BackupTime] <DateTime>
 [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WeeklyScheduleParamSet
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Weekly] [-BackupTime] <DateTime>
 [-DaysOfWeek] <String[]> [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmBackupProtectionPolicy** erstellt eine Azure-Sicherungsrichtlinie als Azure PowerShell-Objekt.
Eine Sicherungsrichtlinie definiert, wann und wie oft Backups ein Element sichern.
Das Enable-AzureRmBackupProtection-Cmdlet verwendet eine Sicherungsrichtlinie.

## Beispiele

### Beispiel 1: Erstellen einer täglichen Backup-Richtlinie mit täglicher und monatlicher Aufbewahrung
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $ProtectionPolicy = New-AzureRmBackupProtectionPolicy -Name DailyBackup01 -Type AzureVM -Daily -BackupTime ([datetime]"3:30 PM") -RetentionPolicy ($Daily,$Monthly) -Vault $Vault
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
```

Der erste Befehl ruft den Tresor mit dem Namen Vault03 mithilfe des Get-AzureRmBackupVault-Cmdlets ab.
Der Befehl speichert das Objekt in der $Vault Variablen.
Der zweite Befehl erstellt eine Aufbewahrungsrichtlinie für 30 Tage tägliche Aufbewahrung und speichert Sie dann in der $Daily-Variablen.
Der dritte Befehl erstellt eine Aufbewahrungsrichtlinie, die die Sicherung auf dem zehnten und dem zwanzigsten Monat für zwölf Monate aufrecht erhält.
Der Befehl speichert die Aufbewahrungsrichtlinie in der $Monthly Variablen.
Der endgültige Befehl erstellt eine Sicherungsrichtlinie für den Tresor in $Vault, die eine tägliche Sicherungszeit von 3:00 Uhr aufweist.
Der Befehl weist die Aufbewahrungsrichtlinien zu, die in $Daily und $Monthly gespeichert sind.
Der Befehl speichert das Ergebnis in der $ProtectionPolicy-Variablen.

## Parameter

### -Backup-Daten
Gibt die Tageszeit als **DateTime** -Objekt für den Sicherungsvorgang an.
Verwenden Sie zum Abrufen eines **DateTime** -Cmdlets das Get-Date-Cmdlet.
Für Informationen zu **DateTime** -Objekten geben Sie `Get-Help Get-Date` .

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Täglich
Gibt an, dass der Sicherungsvorgang nach einem täglichen Zeitplan ausgeführt wird.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysOfWeek
Gibt ein Array von Wochentagen an.
Diese Richtlinie führt Sicherungen an den Tagen durch, die durch diesen Parameter angegeben werden.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Montag 
- Dienstag 
- Mittwoch 
- Donnerstag 
- Freitag 
- Samstag 
- Sonntag Wenn Sie den Parameter *Weekly* angeben, geben Sie diesen Parameter an.

```yaml
Type: System.String[]
Parameter Sets: NoScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Name
Gibt einen Namen für die Sicherungsrichtlinie an.
Wählen Sie einen Namen aus, der im Tresor eindeutig ist.

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
Gibt ein Array von Aufbewahrungsrichtlinien für die Sicherungsrichtlinie an.
Verwenden Sie zum Abrufen eines **AzureRmBackupRetentionPolicy** das New-AzureRmBackupRetentionPolicyObject-Cmdlet.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Typ
Gibt den Typ des sicherungselements an, auf das die Richtlinie angewendet werden soll.
Derzeit ist der einzige unterstützte Wert AzureVM.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Vault
Gibt den Azure-sicherungstresor an, zu dem die Sicherungsrichtlinie gehört.
Verwenden Sie das Get-AzureRmBackupVault-Cmdlet, um ein **AzureRmBackupVault** -Objekt zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### – Wöchentlich
Gibt an, dass die Sicherungsrichtlinie wöchentlich an einem oder mehreren Wochentagen ausgelöst wird.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### System. DateTime

### System. String []

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupRetentionPolicy []

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault
Parameter: Vault (ByValue)

## Ausgaben

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupProtectionPolicy

## Notizen
* Keine

## Verwandte Links

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[Get-AzureRmBackupProtectionPolicy](./Get-AzureRmBackupProtectionPolicy.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Neu – AzureRmBackupRetentionPolicyObject](./New-AzureRmBackupRetentionPolicyObject.md)

[Remove-AzureRmBackupProtectionPolicy](./Remove-AzureRmBackupProtectionPolicy.md)

[Satz-AzureRmBackupProtectionPolicy](./Set-AzureRmBackupProtectionPolicy.md)


