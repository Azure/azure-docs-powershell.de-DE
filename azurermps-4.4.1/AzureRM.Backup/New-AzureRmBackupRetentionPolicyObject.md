---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9574CEB5-B699-4606-8C5E-CE2C0D01092D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
ms.openlocfilehash: 3637709ca347a8e00433f247c80ec1c916e42017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479934"
---
# New-AzureRmBackupRetentionPolicyObject

## Synopsis
Erstellt eine Aufbewahrungsrichtlinie für Backups.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### DailyRetentionParamSet
```
New-AzureRmBackupRetentionPolicyObject [-DailyRetention] -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WeeklyRetentionParamSet
```
New-AzureRmBackupRetentionPolicyObject [-WeeklyRetention] -DaysOfWeek <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MonthlyRetentionInDailyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MonthlyRetentionInWeeklyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### YearlyRetentionInDailyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -MonthsOfYear <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### YearlyRetentionInWeeklyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -MonthsOfYear <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmBackupRetentionPolicyObject** erstellt eine Azure Backup-Aufbewahrungsrichtlinie.
Eine Aufbewahrungsrichtlinie definiert, wie lange die Sicherung einen Wiederherstellungspunkt aufrecht erhält.
Die Aufbewahrungsarten sind wie folgt: 

- Täglich 
- Wochen 
- Monatliche 
- Jahres 

Erstellen Sie eine Aufbewahrungsrichtlinie für jede Art von Aufbewahrung, die Sie verwenden möchten.

Eine Sicherungsrichtlinie ist mit mindestens einer Aufbewahrungsrichtlinie verbunden.
Verwenden Sie zum Erstellen einer Sicherungsrichtlinie das New-AzureRmBackupProtectionPolicy-Cmdlet.
Sie können stattdessen eine Aufbewahrungsrichtlinie für das Enable-AzureRmBackupProtection-Cmdlet bereitstellen.

## Beispiele

### Beispiel 1: Erstellen einer Aufbewahrungsrichtlinie für die tägliche Aufbewahrung
```
PS C:\>$Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Daily
RetentionType      Retention          RetentionTimes
-------------      ---------          --------------
Daily              30
```

Der erste Befehl erstellt eine Aufbewahrungsrichtlinie für 30 Tage tägliche Aufbewahrung und speichert Sie dann in der $Daily-Variablen.

Der zweite Befehl zeigt den Inhalt von $Daily an.

### Beispiel 2: Erstellen einer monatlichen Aufbewahrungsrichtlinie
```
PS C:\>$Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $Monthly | select *
RetentionFormat : Daily
DaysOfMonth     : {10, 20}
WeekNumber      : 
DaysOfWeek      : 
RetentionType   : Monthly
Retention       : 12
RetentionTimes  :
```

Mit dem ersten Befehl wird eine Aufbewahrungsrichtlinie erstellt, die die Sicherung auf dem zehnten und dem zwanzigsten Monat für zwölf Monate aufrecht erhält.
Der Befehl speichert die Aufbewahrungsrichtlinie in der $Monthly Variablen.

Der zweite Befehl zeigt den Inhalt von $Monthly an.

## Parameter

### -DailyRetention
Gibt an, dass mit diesem Cmdlet eine tägliche Aufbewahrungsrichtlinie erstellt wird.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysOfMonth
Gibt die Tage des Monats an, die ermitteln, welche Wiederherstellungspunkte gesichert werden und wie lange.
Die zulässigen Werte für diesen Parameter sind: ganze Zahlen von 1 bis 28 und zuletzt.
Geben Sie diesen Parameter an, wenn Sie die *DailyRetention* -, *MonthlyRetentionInDailyFormat* -und *YearlyRetentionInDailyFormat* -Parameter angeben.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: MonthlyRetentionInDailyFormatParamSet, YearlyRetentionInDailyFormatParamSet
Aliases: 
Accepted values: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysOfWeek
Gibt ein Array von Wochentagen an.
Die Tage, die dieses Cmdlet angibt, geben an, welche Wiederherstellungspunkte von der Sicherung beibehalten werden und wie lange.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Montag 
- Dienstag 
- Mittwoch 
- Donnerstag 
- Freitag 
- Samstag 
- Sonntag

Geben Sie diesen Parameter an, wenn Sie die *WeeklyRetention* -, *MonthlyRetentionInWeeklyFormat* -und *YearlyRetentionInWeeklyFormat* -Parameter angeben.

Achten Sie darauf, dass die Wochentage, die Sie für die Sicherung und für die Aufbewahrung auswählen, ausgerichtet sind.
Wenn Ihre Sicherung beispielsweise für samstags eingestellt ist, müssen die Aufbewahrungsrichtlinien auch Saturday verwenden.

```yaml
Type: System.String[]
Parameter Sets: WeeklyRetentionParamSet, MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonthlyRetentionInDailyFormat
Gibt an, dass dieses Cmdlet eine monatliche Richtlinie im Tagesformat erstellt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonthlyRetentionInWeeklyFormat
Gibt an, dass dieses Cmdlet eine monatliche Richtlinie im Wochenformat erstellt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonthsOfYear
Gibt an, welche Monate des Jahres die Wiederherstellungspunkte aufweisen, die von der Sicherung jährlich aufbewahrt werden.
Die zulässigen Werte für diesen Parameter sind: Namen von Monaten wie Januar oder Februar.

```yaml
Type: System.String[]
Parameter Sets: YearlyRetentionInDailyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: January, February, March, April, May, June, July, August, September, October, November, December

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Aufbewahrung
Gibt den Aufbewahrungszeitraum in Tagen, Monaten oder Jahren an, für den Backup einen Sicherungspunkt speichert.
Die Einheit hängt davon ab, ob dieses Cmdlet eine Tages-, Monats-oder Jahres Aufbewahrungs Option auswählt.
Wenn Sie beispielsweise den *DailyRetention* -Parameter angeben, interpretiert das Cmdlet den aktuellen Parameter als Anzahl von Tagen.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WeeklyRetention
Gibt an, dass mit diesem Cmdlet eine wöchentliche Aufbewahrungsrichtlinie erstellt wird.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WeekNumber
Gibt die Wochen des Monats an, die ermitteln, welche Wiederherstellungspunkte gesichert werden und wie lange.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Ersten 
- Zweiten 
- Dritt 
- Vierten 
- Letzten

```yaml
Type: System.String[]
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: First, Second, Third, Fourth, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -YearlyRetentionInDailyFormat
Gibt an, dass dieses Cmdlet eine jährliche Aufbewahrungsrichtlinie im Tagesformat erstellt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -YearlyRetentionInWeeklyFormat
Gibt an, dass dieses Cmdlet eine jährliche Aufbewahrungsrichtlinie im wöchentlichen Format erstellt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### AzureRmBackupRetentionPolicy

## Notizen
* Keine

## Verwandte Links

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[Neu – AzureRmBackupProtectionPolicy](./New-AzureRmBackupProtectionPolicy.md)


