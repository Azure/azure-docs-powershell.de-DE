---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
ms.openlocfilehash: 9f9cd5b779fcc4e1b9dd6f3df7ed0255adeaa3af
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373483"
---
# <span data-ttu-id="3434c-101">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3434c-101">New-AzAutomationSchedule</span></span>

## <span data-ttu-id="3434c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3434c-102">SYNOPSIS</span></span>
<span data-ttu-id="3434c-103">Erstellt einen Automatisierungszeitplan.</span><span class="sxs-lookup"><span data-stu-id="3434c-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="3434c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3434c-104">SYNTAX</span></span>

### <span data-ttu-id="3434c-105">ByDaily (Standard)</span><span class="sxs-lookup"><span data-stu-id="3434c-105">ByDaily (Default)</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3434c-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="3434c-106">ByWeekly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3434c-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="3434c-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3434c-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="3434c-108">ByMonthlyDayOfWeek</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3434c-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="3434c-109">ByOneTime</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3434c-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="3434c-110">ByHourly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3434c-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3434c-111">DESCRIPTION</span></span>
<span data-ttu-id="3434c-112">Das **Cmdlet "New-AzAutomationSchedule"** erstellt einen Zeitplan in der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="3434c-112">The **New-AzAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="3434c-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3434c-113">EXAMPLES</span></span>

### <span data-ttu-id="3434c-114">Beispiel 1: Erstellen eines einmalplans in Ortszeit</span><span class="sxs-lookup"><span data-stu-id="3434c-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\> $TimeZone = ([System.TimeZoneInfo]::Local).Id
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="3434c-115">Der erste Befehl ruft die Zeitzonen-ID vom System ab und speichert sie in $TimeZone Variable.</span><span class="sxs-lookup"><span data-stu-id="3434c-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="3434c-116">Der zweite Befehl erstellt einen Zeitplan, der an dem aktuellen Datum um 23:00 Uhr in der angegebenen Zeitzone einmal ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3434c-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="3434c-117">Beispiel 2: Erstellen eines wiederkehrenden Zeitplans</span><span class="sxs-lookup"><span data-stu-id="3434c-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DayInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3434c-118">Der erste Befehl erstellt mithilfe des **Cmdlets "Get-Date"** ein Datumsobjekt und speichert das Objekt dann in der $StartDate Variable.</span><span class="sxs-lookup"><span data-stu-id="3434c-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="3434c-119">Geben Sie eine Zeit an, die mindestens fünf Minuten in der Zukunft liegt.</span><span class="sxs-lookup"><span data-stu-id="3434c-119">Specify a time that is at least five minutes in the future.</span></span>
<span data-ttu-id="3434c-120">Der zweite Befehl erstellt mithilfe des **Get-Date-Cmdlets** ein Datumsobjekt und speichert das Objekt dann in der $EndDate Variable.</span><span class="sxs-lookup"><span data-stu-id="3434c-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="3434c-121">Der Befehl gibt eine zukünftige Uhrzeit an.</span><span class="sxs-lookup"><span data-stu-id="3434c-121">The command specifies a future time.</span></span>
<span data-ttu-id="3434c-122">Der endgültige Befehl erstellt einen täglichen Zeitplan mit dem Namen "Schedule02", der zu der in $StartDate gespeicherten Uhrzeit beginnt und zu der in der Datei gespeicherten $EndDate.</span><span class="sxs-lookup"><span data-stu-id="3434c-122">The final command creates a daily schedule named Schedule02 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

### <span data-ttu-id="3434c-123">Beispiel 3: Erstellen eines wöchentlichen wiederkehrenden Zeitplans</span><span class="sxs-lookup"><span data-stu-id="3434c-123">Example 3: Create a weekly recurring schedule</span></span>
```
PS C:\> $StartTime = (Get-Date "13:00:00").AddDays(1)
PS C:\> [System.DayOfWeek[]]$WeekDays = @([System.DayOfWeek]::Monday..[System.DayOfWeek]::Friday)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule03" -StartTime $StartTime - WeekInterval 1 -DaysOfWeek $WeekDays -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3434c-124">Der erste Befehl erstellt mithilfe des **Cmdlets "Get-Date"** ein Datumsobjekt und speichert das Objekt dann in der $StartDate Variable.</span><span class="sxs-lookup"><span data-stu-id="3434c-124">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="3434c-125">Mit dem zweiten Befehl wird ein Array von Wochentagen erstellt, das Montag, Dienstag, Mittwoch, Donnerstag und Freitag enthält.</span><span class="sxs-lookup"><span data-stu-id="3434c-125">The second command creates an array of week days that contains Monday, Tuesday, Wednesday, Thursday and Friday.</span></span>
<span data-ttu-id="3434c-126">Mit dem endgültigen Befehl wird ein Tagesplan namens "Schedule03" erstellt, der jede Woche montags bis freitags um 13:00 Uhr ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3434c-126">The final command creates a daily schedule named Schedule03 that will run Monday to Friday each week at 13:00.</span></span> <span data-ttu-id="3434c-127">Der Zeitplan läuft nie ab.</span><span class="sxs-lookup"><span data-stu-id="3434c-127">The schedule will never expire.</span></span>

## <span data-ttu-id="3434c-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3434c-128">PARAMETERS</span></span>

### <span data-ttu-id="3434c-129">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3434c-129">-AutomationAccountName</span></span>
<span data-ttu-id="3434c-130">Gibt den Namen eines Automatisierungskontos an, für das dieses Cmdlet einen Zeitplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="3434c-130">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="3434c-131">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="3434c-131">-DayInterval</span></span>
<span data-ttu-id="3434c-132">Gibt ein Intervall in Tagen für den Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="3434c-132">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="3434c-133">Wenn Sie diesen Parameter nicht angeben und den Parameter *"OneTime"* nicht angeben, ist der Standardwert 1 (1).</span><span class="sxs-lookup"><span data-stu-id="3434c-133">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

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

### <span data-ttu-id="3434c-134">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="3434c-134">-DayOfWeek</span></span>
<span data-ttu-id="3434c-135">Gibt eine Liste der Wochentage für den Wöchentlichen Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="3434c-135">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="3434c-136">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="3434c-136">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="3434c-137">Gibt das Vorkommen der Woche innerhalb des Monats an, in dem der Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3434c-137">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="3434c-138">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="3434c-138">psdx_paramvalues</span></span>
- <span data-ttu-id="3434c-139">1</span><span class="sxs-lookup"><span data-stu-id="3434c-139">1</span></span>
- <span data-ttu-id="3434c-140">2</span><span class="sxs-lookup"><span data-stu-id="3434c-140">2</span></span>
- <span data-ttu-id="3434c-141">3</span><span class="sxs-lookup"><span data-stu-id="3434c-141">3</span></span>
- <span data-ttu-id="3434c-142">4</span><span class="sxs-lookup"><span data-stu-id="3434c-142">4</span></span>
- <span data-ttu-id="3434c-143">-1</span><span class="sxs-lookup"><span data-stu-id="3434c-143">-1</span></span>
- <span data-ttu-id="3434c-144">First</span><span class="sxs-lookup"><span data-stu-id="3434c-144">First</span></span>
- <span data-ttu-id="3434c-145">Sekunde</span><span class="sxs-lookup"><span data-stu-id="3434c-145">Second</span></span>
- <span data-ttu-id="3434c-146">Dritter</span><span class="sxs-lookup"><span data-stu-id="3434c-146">Third</span></span>
- <span data-ttu-id="3434c-147">Vierter</span><span class="sxs-lookup"><span data-stu-id="3434c-147">Fourth</span></span>
- <span data-ttu-id="3434c-148">LastDay</span><span class="sxs-lookup"><span data-stu-id="3434c-148">LastDay</span></span>

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

### <span data-ttu-id="3434c-149">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="3434c-149">-DaysOfMonth</span></span>
<span data-ttu-id="3434c-150">Gibt eine Liste der Tage des Monats für den Monatsplan an.</span><span class="sxs-lookup"><span data-stu-id="3434c-150">Specifies a list of days of the month for the monthly schedule.</span></span>

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

### <span data-ttu-id="3434c-151">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="3434c-151">-DaysOfWeek</span></span>
<span data-ttu-id="3434c-152">Gibt eine Liste der Wochentage für den Wöchentlichen Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="3434c-152">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="3434c-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3434c-153">-DefaultProfile</span></span>
<span data-ttu-id="3434c-154">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3434c-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3434c-155">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3434c-155">-Description</span></span>
<span data-ttu-id="3434c-156">Gibt eine Beschreibung für den Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="3434c-156">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="3434c-157">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3434c-157">-ExpiryTime</span></span>
<span data-ttu-id="3434c-158">Gibt die Ablaufzeit eines Zeitplans als **"DateTimeOffset"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="3434c-158">Specifies the expiry time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="3434c-159">Sie können eine Zeichenfolge angeben, die in einen gültigen **DateTimeOffset konvertiert werden kann.**</span><span class="sxs-lookup"><span data-stu-id="3434c-159">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="3434c-160">-ForUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="3434c-160">-ForUpdateConfiguration</span></span>
<span data-ttu-id="3434c-161">Gibt an, dass dieses Zeitplanobjekt zum Planen einer Softwareupdatekonfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3434c-161">Indicates that this schedule object will be used for scheduling a software update configuration</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3434c-162">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="3434c-162">-HourInterval</span></span>
<span data-ttu-id="3434c-163">Gibt ein Intervall in Stunden für den Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="3434c-163">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="3434c-164">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="3434c-164">-MonthInterval</span></span>
<span data-ttu-id="3434c-165">Gibt ein Intervall in "Monate" für den Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="3434c-165">Specifies an interval, in Months, for the schedule.</span></span>

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

### <span data-ttu-id="3434c-166">-Name</span><span class="sxs-lookup"><span data-stu-id="3434c-166">-Name</span></span>
<span data-ttu-id="3434c-167">Gibt einen Namen für den Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="3434c-167">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="3434c-168">-OneTime</span><span class="sxs-lookup"><span data-stu-id="3434c-168">-OneTime</span></span>
<span data-ttu-id="3434c-169">Gibt an, dass das Cmdlet einen einmalplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="3434c-169">Specifies that the cmdlet creates a one-time schedule.</span></span>

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

### <span data-ttu-id="3434c-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3434c-170">-ResourceGroupName</span></span>
<span data-ttu-id="3434c-171">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet einen Zeitplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="3434c-171">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="3434c-172">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3434c-172">-StartTime</span></span>
<span data-ttu-id="3434c-173">Gibt die Startzeit eines Zeitplans als **"DateTimeOffset"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="3434c-173">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="3434c-174">Sie können eine Zeichenfolge angeben, die in einen gültigen **DateTimeOffset konvertiert werden kann.**</span><span class="sxs-lookup"><span data-stu-id="3434c-174">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="3434c-175">Wenn der *Parameter "TimeZone"* angegeben wird, wird der Offset ignoriert, und die angegebene Zeitzone wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="3434c-175">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

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

### <span data-ttu-id="3434c-176">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="3434c-176">-TimeZone</span></span>
<span data-ttu-id="3434c-177">Gibt die Zeitzone für den Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="3434c-177">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="3434c-178">Diese Zeichenfolge kann die IANA-ID oder die Windows-Zeitzonen-ID sein.</span><span class="sxs-lookup"><span data-stu-id="3434c-178">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

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

### <span data-ttu-id="3434c-179">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="3434c-179">-WeekInterval</span></span>
<span data-ttu-id="3434c-180">Gibt ein Intervall in Wochen für den Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="3434c-180">Specifies an interval, in weeks, for the schedule.</span></span>

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

### <span data-ttu-id="3434c-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3434c-181">CommonParameters</span></span>
<span data-ttu-id="3434c-182">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3434c-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3434c-183">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3434c-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3434c-184">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3434c-184">INPUTS</span></span>

### <span data-ttu-id="3434c-185">System.String</span><span class="sxs-lookup"><span data-stu-id="3434c-185">System.String</span></span>

### <span data-ttu-id="3434c-186">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3434c-186">System.DateTimeOffset</span></span>

### <span data-ttu-id="3434c-187">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3434c-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3434c-188">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3434c-188">OUTPUTS</span></span>

### <span data-ttu-id="3434c-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="3434c-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="3434c-190">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3434c-190">NOTES</span></span>

## <span data-ttu-id="3434c-191">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3434c-191">RELATED LINKS</span></span>

[<span data-ttu-id="3434c-192">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3434c-192">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="3434c-193">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3434c-193">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="3434c-194">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3434c-194">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


