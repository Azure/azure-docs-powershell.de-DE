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
# <span data-ttu-id="ef6eb-101">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ef6eb-101">New-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="ef6eb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef6eb-102">SYNOPSIS</span></span>
<span data-ttu-id="ef6eb-103">Erstellt einen Automatisierungs Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-103">Creates an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef6eb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef6eb-104">SYNTAX</span></span>

### <span data-ttu-id="ef6eb-105">ByDaily (Standard)</span><span class="sxs-lookup"><span data-stu-id="ef6eb-105">ByDaily (Default)</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef6eb-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="ef6eb-106">ByWeekly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef6eb-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="ef6eb-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef6eb-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="ef6eb-108">ByMonthlyDayOfWeek</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef6eb-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="ef6eb-109">ByOneTime</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef6eb-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="ef6eb-110">ByHourly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef6eb-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef6eb-111">DESCRIPTION</span></span>
<span data-ttu-id="ef6eb-112">Das Cmdlet **New-AzureRmAutomationSchedule** erstellt einen Zeitplan in der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-112">The **New-AzureRmAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="ef6eb-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef6eb-113">EXAMPLES</span></span>

### <span data-ttu-id="ef6eb-114">Beispiel 1: Erstellen eines einmaligen Zeitplans in Ortszeit</span><span class="sxs-lookup"><span data-stu-id="ef6eb-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\>$TimeZone = ([System.TimeZoneInfo]::Local)Id
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="ef6eb-115">Der erste Befehl ruft die Zeit Zonen-ID des Systems ab und speichert Sie in der $TimeZone-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="ef6eb-116">Der zweite Befehl erstellt einen Zeitplan, der zum aktuellen Datum um 11:00 Uhr in der angegebenen Zeitzone einmal ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="ef6eb-117">Beispiel 2: Erstellen eines wiederkehrenden Zeitplans</span><span class="sxs-lookup"><span data-stu-id="ef6eb-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\>$StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ef6eb-118">Mit dem ersten Befehl wird ein Date-Objekt mithilfe des **Get-Date-** Cmdlets erstellt, und das Objekt wird dann in der $StartDate-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="ef6eb-119">Geben Sie eine Uhrzeit an, die in der Zukunft mindestens fünf Minuten beträgt.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-119">Specify a time that is at least five minutes in the future.</span></span>

<span data-ttu-id="ef6eb-120">Mit dem zweiten Befehl wird ein Date-Objekt mithilfe des **Get-Date-** Cmdlets erstellt, und das Objekt wird dann in der $EndDate-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="ef6eb-121">Der Befehl gibt eine zukünftige Zeit an.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-121">The command specifies a future time.</span></span>

<span data-ttu-id="ef6eb-122">Der endgültige Befehl erstellt einen täglichen Zeitplan mit dem Namen Schedule01, um zu dem in $StartDate gespeicherten Zeitpunkt zu beginnen und zu dem in $EndDate gespeicherten Zeitpunkt zu verfallen.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-122">The final command creates a daily schedule named Schedule01 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

## <span data-ttu-id="ef6eb-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef6eb-123">PARAMETERS</span></span>

### <span data-ttu-id="ef6eb-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ef6eb-124">-AutomationAccountName</span></span>
<span data-ttu-id="ef6eb-125">Gibt den Namen eines Automatisierungs Kontos an, für das dieses Cmdlet einen Zeitplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-125">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="ef6eb-126">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="ef6eb-126">-DayInterval</span></span>
<span data-ttu-id="ef6eb-127">Gibt ein Intervall in Tagen für den Terminplan an.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-127">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="ef6eb-128">Wenn Sie diesen Parameter nicht angeben und den *einmaligen* Parameter nicht angeben, ist der Standardwert 1.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-128">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

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

### <span data-ttu-id="ef6eb-129">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="ef6eb-129">-DayOfWeek</span></span>
<span data-ttu-id="ef6eb-130">Gibt eine Liste der Wochentage für den Wochenplan an.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-130">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="ef6eb-131">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="ef6eb-131">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="ef6eb-132">Gibt das Vorkommen der Woche innerhalb des Monats an, in dem der Terminplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-132">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="ef6eb-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="ef6eb-133">psdx_paramvalues</span></span>

- <span data-ttu-id="ef6eb-134">1</span><span class="sxs-lookup"><span data-stu-id="ef6eb-134">1</span></span>
- <span data-ttu-id="ef6eb-135">2</span><span class="sxs-lookup"><span data-stu-id="ef6eb-135">2</span></span>
- <span data-ttu-id="ef6eb-136">3</span><span class="sxs-lookup"><span data-stu-id="ef6eb-136">3</span></span>
- <span data-ttu-id="ef6eb-137">4</span><span class="sxs-lookup"><span data-stu-id="ef6eb-137">4</span></span>
- <span data-ttu-id="ef6eb-138">-1</span><span class="sxs-lookup"><span data-stu-id="ef6eb-138">-1</span></span>
- <span data-ttu-id="ef6eb-139">Ersten</span><span class="sxs-lookup"><span data-stu-id="ef6eb-139">First</span></span>
- <span data-ttu-id="ef6eb-140">Zweiten</span><span class="sxs-lookup"><span data-stu-id="ef6eb-140">Second</span></span>
- <span data-ttu-id="ef6eb-141">Dritt</span><span class="sxs-lookup"><span data-stu-id="ef6eb-141">Third</span></span>
- <span data-ttu-id="ef6eb-142">Vierten</span><span class="sxs-lookup"><span data-stu-id="ef6eb-142">Fourth</span></span>
- <span data-ttu-id="ef6eb-143">LETZTERTAG</span><span class="sxs-lookup"><span data-stu-id="ef6eb-143">LastDay</span></span>

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

### <span data-ttu-id="ef6eb-144">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="ef6eb-144">-DaysOfMonth</span></span>
<span data-ttu-id="ef6eb-145">Gibt eine Liste der Tage des Monats für den monatlichen Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-145">Specifies a list of days of the month for the monthly schedule.</span></span>

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

### <span data-ttu-id="ef6eb-146">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="ef6eb-146">-DaysOfWeek</span></span>
<span data-ttu-id="ef6eb-147">Gibt eine Liste der Wochentage für den Wochenplan an.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-147">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="ef6eb-148">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef6eb-148">-Description</span></span>
<span data-ttu-id="ef6eb-149">Gibt eine Beschreibung für den Terminplan an.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-149">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="ef6eb-150">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ef6eb-150">-ExpiryTime</span></span>
<span data-ttu-id="ef6eb-151">Gibt die Ablaufzeit eines Zeitplans als **DateTimeOffest** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-151">Specifies the expiry time of a schedule as a **DateTimeOffest** object.</span></span>
<span data-ttu-id="ef6eb-152">Sie können eine Zeichenfolge angeben, die in einen gültigen **DateTimeOffset** konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-152">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="ef6eb-153">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="ef6eb-153">-HourInterval</span></span>
<span data-ttu-id="ef6eb-154">Gibt ein Intervall in Stunden für den Terminplan an.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-154">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="ef6eb-155">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="ef6eb-155">-MonthInterval</span></span>
<span data-ttu-id="ef6eb-156">Gibt ein Intervall in Monaten für den Terminplan an.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-156">Specifies an interval, in Months, for the schedule.</span></span>

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

### <span data-ttu-id="ef6eb-157">-Name</span><span class="sxs-lookup"><span data-stu-id="ef6eb-157">-Name</span></span>
<span data-ttu-id="ef6eb-158">Gibt einen Namen für den Terminplan an.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-158">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="ef6eb-159">-Einmalig</span><span class="sxs-lookup"><span data-stu-id="ef6eb-159">-OneTime</span></span>
<span data-ttu-id="ef6eb-160">Gibt an, dass das Cmdlet einen einmaligen Zeitplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-160">Specifies that the cmdlet creates a one-time schedule.</span></span>

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

### <span data-ttu-id="ef6eb-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef6eb-161">-ResourceGroupName</span></span>
<span data-ttu-id="ef6eb-162">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet einen Terminplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-162">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="ef6eb-163">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="ef6eb-163">-StartTime</span></span>
<span data-ttu-id="ef6eb-164">Gibt die Startzeit eines Zeitplans als **DateTimeOffset** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-164">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="ef6eb-165">Sie können eine Zeichenfolge angeben, die in einen gültigen **DateTimeOffset** konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-165">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="ef6eb-166">.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-166">.</span></span> <span data-ttu-id="ef6eb-167">Wenn der *TimeZone* -Parameter angegeben wird, wird der Offset ignoriert, und die angegebene Zeitzone wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-167">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

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

### <span data-ttu-id="ef6eb-168">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="ef6eb-168">-TimeZone</span></span>
<span data-ttu-id="ef6eb-169">Gibt die Zeitzone für den Terminplan an.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-169">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="ef6eb-170">Diese Zeichenfolge kann die IANA-ID oder die Windows-Zeitzone-ID sein.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-170">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

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

### <span data-ttu-id="ef6eb-171">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="ef6eb-171">-WeekInterval</span></span>
<span data-ttu-id="ef6eb-172">Gibt ein Intervall für den Terminplan in Wochen an.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-172">Specifies an interval, in weeks, for the schedule.</span></span>

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

### <span data-ttu-id="ef6eb-173">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef6eb-173">-DefaultProfile</span></span>
<span data-ttu-id="ef6eb-174">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-174">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef6eb-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef6eb-175">CommonParameters</span></span>
<span data-ttu-id="ef6eb-176">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef6eb-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef6eb-177">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef6eb-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef6eb-178">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef6eb-178">INPUTS</span></span>

## <span data-ttu-id="ef6eb-179">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef6eb-179">OUTPUTS</span></span>

### <span data-ttu-id="ef6eb-180">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="ef6eb-180">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="ef6eb-181">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef6eb-181">NOTES</span></span>

## <span data-ttu-id="ef6eb-182">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef6eb-182">RELATED LINKS</span></span>

[<span data-ttu-id="ef6eb-183">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ef6eb-183">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="ef6eb-184">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ef6eb-184">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="ef6eb-185">Satz-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ef6eb-185">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


