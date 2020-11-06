---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 7d41abd1d56bab4df0d716c3a9d11ea14140b784
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501486"
---
# Set-AzureRmBackupProtectionPolicy

## Synopsis
Ändert eine vorhandene Schutzrichtlinie.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### NoScheduleParamSet (Standard)
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DailyScheduleParamSet
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WeeklyScheduleParamSet
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **festlegen-AzureRmBackupProtectionPolicy** " wird eine vorhandene Schutzrichtlinie in Azure Backup geändert.
Sie können die folgenden Schutzrichtlinien Komponenten ändern: 

- Namen
- Sicherungszeitplan
- Aufbewahrungsrichtlinien

Jede Änderung kann sich auf die Sicherung und Aufbewahrung der mit der Richtlinie verknüpften Elemente auswirken.

## Beispiele

## Parameter

### -Backup-Daten
Gibt die neue Sicherungszeit des Tages als **DateTime** -Objekt für die Richtlinie an.
Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt zu erhalten.
Für Informationen zu **DateTime** -Objekten geben Sie `Get-Help Get-Date` .

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Täglich
Gibt an, dass der Sicherungsvorgang nach einem täglichen Zeitplan ausgeführt wird.

```yaml
Type: SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 2
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
- Sonntag

```yaml
Type: String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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
Gibt den neuen Namen für die Richtlinie an.
Dieser Name muss in einem Tresor eindeutig sein.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionPolicy
Gibt Schutzrichtlinien an, die von diesem Cmdlet geändert werden.
Verwenden Sie das Get-AzureRmBackupProtectionPolicy-Cmdlet, um ein **AzureRmBackupProtectionPolicy** -Objekt zu erhalten.

```yaml
Type: AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RetentionPolicy
Gibt ein Array von Aufbewahrungsrichtlinien für die Sicherungsrichtlinie an.
Verwenden Sie zum Abrufen von **AzureRmBackupRetentionPolicy** -Objekten das New-AzureRmBackupRetentionPolicyObject-Cmdlet.

```yaml
Type: AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Wöchentlich
Gibt an, dass der Sicherungsvorgang nach einem wöchentlichen Zeitplan ausgeführt wird.

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### AzureRmBackupProtectionPolicy

## Ausgaben

### Keine

## Notizen

## Verwandte Links

[Neu – AzureRmBackupProtectionPolicy](./New-AzureRmBackupProtectionPolicy.md)


