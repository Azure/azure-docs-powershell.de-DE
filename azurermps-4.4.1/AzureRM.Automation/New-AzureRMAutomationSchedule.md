---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
ms.openlocfilehash: d82e63d21e18b7fb75282da9ac12be7644b0535a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663091"
---
# New-AzureRmAutomationSchedule

## Synopsis
Erstellt einen Automatisierungs Zeitplan.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByDaily (Standard)
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByWeekly
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByMonthlyDaysOfMonth
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByMonthlyDayOfWeek
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByOneTime
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByHourly
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmAutomationSchedule** erstellt einen Zeitplan in der Azure-Automatisierung.

## Beispiele

### Beispiel 1: Erstellen eines einmaligen Zeitplans in Ortszeit
```
PS C:\>$TimeZone = ([System.TimeZoneInfo]::Local)Id
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

Der erste Befehl ruft die Zeit Zonen-ID des Systems ab und speichert Sie in der $TimeZone-Variablen.
Der zweite Befehl erstellt einen Zeitplan, der zum aktuellen Datum um 11:00 Uhr in der angegebenen Zeitzone einmal ausgeführt wird.

### Beispiel 2: Erstellen eines wiederkehrenden Zeitplans
```
PS C:\>$StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1 -ResourceGroupName "ResourceGroup01"
```

Mit dem ersten Befehl wird ein Date-Objekt mithilfe des **Get-Date-** Cmdlets erstellt, und das Objekt wird dann in der $StartDate-Variablen gespeichert.
Geben Sie eine Uhrzeit an, die in der Zukunft mindestens fünf Minuten beträgt.

Mit dem zweiten Befehl wird ein Date-Objekt mithilfe des **Get-Date-** Cmdlets erstellt, und das Objekt wird dann in der $EndDate-Variablen gespeichert.
Der Befehl gibt eine zukünftige Zeit an.

Der endgültige Befehl erstellt einen täglichen Zeitplan mit dem Namen Schedule01, um zu dem in $StartDate gespeicherten Zeitpunkt zu beginnen und zu dem in $EndDate gespeicherten Zeitpunkt zu verfallen.

## Parameter

### -AutomationAccountName
Gibt den Namen eines Automatisierungs Kontos an, für das dieses Cmdlet einen Zeitplan erstellt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DayInterval
Gibt ein Intervall in Tagen für den Terminplan an.
Wenn Sie diesen Parameter nicht angeben und den *einmaligen* Parameter nicht angeben, ist der Standardwert 1.

```yaml
Type: System.Byte
Parameter Sets: ByDaily
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DayOfWeek
Gibt eine Liste der Wochentage für den Wochenplan an.

```yaml
Type: System.Nullable`1[System.DayOfWeek]
Parameter Sets: ByMonthlyDayOfWeek
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DayOfWeekOccurrence
Gibt das Vorkommen der Woche innerhalb des Monats an, in dem der Terminplan ausgeführt wird.
psdx_paramvalues

- 1
- 2
- 3
- 4
- -1
- Ersten
- Zweiten
- Dritt
- Vierten
- LETZTERTAG

```yaml
Type: Microsoft.Azure.Commands.Automation.Cmdlet.DayOfWeekOccurrence
Parameter Sets: ByMonthlyDayOfWeek
Aliases: 
Accepted values: First, Second, Third, Fourth, Last

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysOfMonth
Gibt eine Liste der Tage des Monats für den monatlichen Zeitplan an.

```yaml
Type: Microsoft.Azure.Commands.Automation.Cmdlet.DaysOfMonth[]
Parameter Sets: ByMonthlyDaysOfMonth
Aliases: 
Accepted values: One, Two, Three, Four, Five, Six, Seventh, Eighth, Ninth, Tenth, Eleventh, Twelfth, Thirteenth, Fourteenth, Fifteenth, Sixteenth, Seventeenth, Eighteenth, Nineteenth, Twentieth, TwentyFirst, TwentySecond, TwentyThird, TwentyFourth, TwentyFifth, TwentySixth, TwentySeventh, TwentyEighth, TwentyNinth, Thirtieth, ThirtyFirst, LastDay

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysOfWeek
Gibt eine Liste der Wochentage für den Wochenplan an.

```yaml
Type: System.DayOfWeek[]
Parameter Sets: ByWeekly
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Beschreibung
Gibt eine Beschreibung für den Terminplan an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ExpiryTime
Gibt die Ablaufzeit eines Zeitplans als **DateTimeOffest** -Objekt an.
Sie können eine Zeichenfolge angeben, die in einen gültigen **DateTimeOffset** konvertiert werden kann.

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByDaily, ByWeekly, ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek, ByHourly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HourInterval
Gibt ein Intervall in Stunden für den Terminplan an.

```yaml
Type: System.Byte
Parameter Sets: ByHourly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonthInterval
Gibt ein Intervall in Monaten für den Terminplan an.

```yaml
Type: System.Byte
Parameter Sets: ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt einen Namen für den Terminplan an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Einmalig
Gibt an, dass das Cmdlet einen einmaligen Zeitplan erstellt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByOneTime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet einen Terminplan erstellt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Startzeit
Gibt die Startzeit eines Zeitplans als **DateTimeOffset** -Objekt an.
Sie können eine Zeichenfolge angeben, die in einen gültigen **DateTimeOffset** konvertiert werden kann.
. Wenn der *TimeZone* -Parameter angegeben wird, wird der Offset ignoriert, und die angegebene Zeitzone wird verwendet.

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
Gibt die Zeitzone für den Terminplan an.
Diese Zeichenfolge kann die IANA-ID oder die Windows-Zeitzone-ID sein.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WeekInterval
Gibt ein Intervall für den Terminplan in Wochen an.

```yaml
Type: System.Byte
Parameter Sets: ByWeekly
Aliases: 

Required: True
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

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. Schedule

## Notizen

## Verwandte Links

[Get-AzureRmAutomationSchedule](./Get-AzureRMAutomationSchedule.md)

[Remove-AzureRmAutomationSchedule](./Remove-AzureRMAutomationSchedule.md)

[Satz-AzureRmAutomationSchedule](./Set-AzureRMAutomationSchedule.md)


