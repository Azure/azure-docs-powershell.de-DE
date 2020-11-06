---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
ms.openlocfilehash: 3528a95e9dab3c92571ec49e9bf5d567012fb5b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503110"
---
# <span data-ttu-id="b97ad-101">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="b97ad-101">New-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="b97ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b97ad-102">SYNOPSIS</span></span>
<span data-ttu-id="b97ad-103">Erstellt einen Automatisierungs Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="b97ad-103">Creates an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b97ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b97ad-104">SYNTAX</span></span>

### <span data-ttu-id="b97ad-105">ByDaily (Standard)</span><span class="sxs-lookup"><span data-stu-id="b97ad-105">ByDaily (Default)</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b97ad-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="b97ad-106">ByWeekly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b97ad-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="b97ad-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b97ad-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="b97ad-108">ByMonthlyDayOfWeek</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b97ad-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="b97ad-109">ByOneTime</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b97ad-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="b97ad-110">ByHourly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b97ad-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b97ad-111">DESCRIPTION</span></span>
<span data-ttu-id="b97ad-112">Das Cmdlet **New-AzureRmAutomationSchedule** erstellt einen Zeitplan in der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="b97ad-112">The **New-AzureRmAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="b97ad-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b97ad-113">EXAMPLES</span></span>

### <span data-ttu-id="b97ad-114">Beispiel 1: Erstellen eines einmaligen Zeitplans in Ortszeit</span><span class="sxs-lookup"><span data-stu-id="b97ad-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\>$TimeZone = ([System.TimeZoneInfo]::Local)Id
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="b97ad-115">Der erste Befehl ruft die Zeit Zonen-ID des Systems ab und speichert Sie in der $TimeZone-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b97ad-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="b97ad-116">Der zweite Befehl erstellt einen Zeitplan, der zum aktuellen Datum um 11:00 Uhr in der angegebenen Zeitzone einmal ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b97ad-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="b97ad-117">Beispiel 2: Erstellen eines wiederkehrenden Zeitplans</span><span class="sxs-lookup"><span data-stu-id="b97ad-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\>$StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b97ad-118">Mit dem ersten Befehl wird ein Date-Objekt mithilfe des **Get-Date-** Cmdlets erstellt, und das Objekt wird dann in der $StartDate-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b97ad-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="b97ad-119">Geben Sie eine Uhrzeit an, die in der Zukunft mindestens fünf Minuten beträgt.</span><span class="sxs-lookup"><span data-stu-id="b97ad-119">Specify a time that is at least five minutes in the future.</span></span>

<span data-ttu-id="b97ad-120">Mit dem zweiten Befehl wird ein Date-Objekt mithilfe des **Get-Date-** Cmdlets erstellt, und das Objekt wird dann in der $EndDate-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b97ad-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="b97ad-121">Der Befehl gibt eine zukünftige Zeit an.</span><span class="sxs-lookup"><span data-stu-id="b97ad-121">The command specifies a future time.</span></span>

<span data-ttu-id="b97ad-122">Der endgültige Befehl erstellt einen täglichen Zeitplan mit dem Namen Schedule01, um zu dem in $StartDate gespeicherten Zeitpunkt zu beginnen und zu dem in $EndDate gespeicherten Zeitpunkt zu verfallen.</span><span class="sxs-lookup"><span data-stu-id="b97ad-122">The final command creates a daily schedule named Schedule01 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

## <span data-ttu-id="b97ad-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="b97ad-123">PARAMETERS</span></span>

### <span data-ttu-id="b97ad-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b97ad-124">-AutomationAccountName</span></span>
<span data-ttu-id="b97ad-125">Gibt den Namen eines Automatisierungs Kontos an, für das dieses Cmdlet einen Zeitplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="b97ad-125">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b97ad-126">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="b97ad-126">-DayInterval</span></span>
<span data-ttu-id="b97ad-127">Gibt ein Intervall in Tagen für den Terminplan an.</span><span class="sxs-lookup"><span data-stu-id="b97ad-127">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="b97ad-128">Wenn Sie diesen Parameter nicht angeben und den *einmaligen* Parameter nicht angeben, ist der Standardwert 1.</span><span class="sxs-lookup"><span data-stu-id="b97ad-128">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

```yaml
Type: Byte
Parameter Sets: ByDaily
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97ad-129">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="b97ad-129">-DayOfWeek</span></span>
<span data-ttu-id="b97ad-130">Gibt eine Liste der Wochentage für den Wochenplan an.</span><span class="sxs-lookup"><span data-stu-id="b97ad-130">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: DayOfWeek
Parameter Sets: ByMonthlyDayOfWeek
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97ad-131">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="b97ad-131">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="b97ad-132">Gibt das Vorkommen der Woche innerhalb des Monats an, in dem der Terminplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b97ad-132">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="b97ad-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="b97ad-133">psdx_paramvalues</span></span>

- <span data-ttu-id="b97ad-134">1</span><span class="sxs-lookup"><span data-stu-id="b97ad-134">1</span></span>
- <span data-ttu-id="b97ad-135">2</span><span class="sxs-lookup"><span data-stu-id="b97ad-135">2</span></span>
- <span data-ttu-id="b97ad-136">3</span><span class="sxs-lookup"><span data-stu-id="b97ad-136">3</span></span>
- <span data-ttu-id="b97ad-137">4</span><span class="sxs-lookup"><span data-stu-id="b97ad-137">4</span></span>
- <span data-ttu-id="b97ad-138">-1</span><span class="sxs-lookup"><span data-stu-id="b97ad-138">-1</span></span>
- <span data-ttu-id="b97ad-139">Ersten</span><span class="sxs-lookup"><span data-stu-id="b97ad-139">First</span></span>
- <span data-ttu-id="b97ad-140">Zweiten</span><span class="sxs-lookup"><span data-stu-id="b97ad-140">Second</span></span>
- <span data-ttu-id="b97ad-141">Dritt</span><span class="sxs-lookup"><span data-stu-id="b97ad-141">Third</span></span>
- <span data-ttu-id="b97ad-142">Vierten</span><span class="sxs-lookup"><span data-stu-id="b97ad-142">Fourth</span></span>
- <span data-ttu-id="b97ad-143">LETZTERTAG</span><span class="sxs-lookup"><span data-stu-id="b97ad-143">LastDay</span></span>

```yaml
Type: DayOfWeekOccurrence
Parameter Sets: ByMonthlyDayOfWeek
Aliases: 
Accepted values: First, Second, Third, Fourth, Last

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97ad-144">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="b97ad-144">-DaysOfMonth</span></span>
<span data-ttu-id="b97ad-145">Gibt eine Liste der Tage des Monats für den monatlichen Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="b97ad-145">Specifies a list of days of the month for the monthly schedule.</span></span>

```yaml
Type: DaysOfMonth[]
Parameter Sets: ByMonthlyDaysOfMonth
Aliases: 
Accepted values: One, Two, Three, Four, Five, Six, Seventh, Eighth, Ninth, Tenth, Eleventh, Twelfth, Thirteenth, Fourteenth, Fifteenth, Sixteenth, Seventeenth, Eighteenth, Nineteenth, Twentieth, TwentyFirst, TwentySecond, TwentyThird, TwentyFourth, TwentyFifth, TwentySixth, TwentySeventh, TwentyEighth, TwentyNinth, Thirtieth, ThirtyFirst, LastDay

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97ad-146">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="b97ad-146">-DaysOfWeek</span></span>
<span data-ttu-id="b97ad-147">Gibt eine Liste der Wochentage für den Wochenplan an.</span><span class="sxs-lookup"><span data-stu-id="b97ad-147">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: DayOfWeek[]
Parameter Sets: ByWeekly
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97ad-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b97ad-148">-DefaultProfile</span></span>
<span data-ttu-id="b97ad-149">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b97ad-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b97ad-150">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b97ad-150">-Description</span></span>
<span data-ttu-id="b97ad-151">Gibt eine Beschreibung für den Terminplan an.</span><span class="sxs-lookup"><span data-stu-id="b97ad-151">Specifies a description for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b97ad-152">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b97ad-152">-ExpiryTime</span></span>
<span data-ttu-id="b97ad-153">Gibt die Ablaufzeit eines Zeitplans als **DateTimeOffest** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b97ad-153">Specifies the expiry time of a schedule as a **DateTimeOffest** object.</span></span>
<span data-ttu-id="b97ad-154">Sie können eine Zeichenfolge angeben, die in einen gültigen **DateTimeOffset** konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b97ad-154">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByDaily, ByWeekly, ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek, ByHourly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97ad-155">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="b97ad-155">-HourInterval</span></span>
<span data-ttu-id="b97ad-156">Gibt ein Intervall in Stunden für den Terminplan an.</span><span class="sxs-lookup"><span data-stu-id="b97ad-156">Specifies an interval, in hours, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByHourly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97ad-157">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="b97ad-157">-MonthInterval</span></span>
<span data-ttu-id="b97ad-158">Gibt ein Intervall in Monaten für den Terminplan an.</span><span class="sxs-lookup"><span data-stu-id="b97ad-158">Specifies an interval, in Months, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97ad-159">-Name</span><span class="sxs-lookup"><span data-stu-id="b97ad-159">-Name</span></span>
<span data-ttu-id="b97ad-160">Gibt einen Namen für den Terminplan an.</span><span class="sxs-lookup"><span data-stu-id="b97ad-160">Specifies a name for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b97ad-161">-Einmalig</span><span class="sxs-lookup"><span data-stu-id="b97ad-161">-OneTime</span></span>
<span data-ttu-id="b97ad-162">Gibt an, dass das Cmdlet einen einmaligen Zeitplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="b97ad-162">Specifies that the cmdlet creates a one-time schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByOneTime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97ad-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b97ad-163">-ResourceGroupName</span></span>
<span data-ttu-id="b97ad-164">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet einen Terminplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="b97ad-164">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b97ad-165">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="b97ad-165">-StartTime</span></span>
<span data-ttu-id="b97ad-166">Gibt die Startzeit eines Zeitplans als **DateTimeOffset** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b97ad-166">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="b97ad-167">Sie können eine Zeichenfolge angeben, die in einen gültigen **DateTimeOffset** konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b97ad-167">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="b97ad-168">.</span><span class="sxs-lookup"><span data-stu-id="b97ad-168">.</span></span> <span data-ttu-id="b97ad-169">Wenn der *TimeZone* -Parameter angegeben wird, wird der Offset ignoriert, und die angegebene Zeitzone wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="b97ad-169">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b97ad-170">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="b97ad-170">-TimeZone</span></span>
<span data-ttu-id="b97ad-171">Gibt die Zeitzone für den Terminplan an.</span><span class="sxs-lookup"><span data-stu-id="b97ad-171">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="b97ad-172">Diese Zeichenfolge kann die IANA-ID oder die Windows-Zeitzone-ID sein.</span><span class="sxs-lookup"><span data-stu-id="b97ad-172">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b97ad-173">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="b97ad-173">-WeekInterval</span></span>
<span data-ttu-id="b97ad-174">Gibt ein Intervall für den Terminplan in Wochen an.</span><span class="sxs-lookup"><span data-stu-id="b97ad-174">Specifies an interval, in weeks, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByWeekly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97ad-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b97ad-175">CommonParameters</span></span>
<span data-ttu-id="b97ad-176">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b97ad-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b97ad-177">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b97ad-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b97ad-178">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b97ad-178">INPUTS</span></span>

### <span data-ttu-id="b97ad-179">Keine</span><span class="sxs-lookup"><span data-stu-id="b97ad-179">None</span></span>
<span data-ttu-id="b97ad-180">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="b97ad-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b97ad-181">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b97ad-181">OUTPUTS</span></span>

### <span data-ttu-id="b97ad-182">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="b97ad-182">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="b97ad-183">Notizen</span><span class="sxs-lookup"><span data-stu-id="b97ad-183">NOTES</span></span>

## <span data-ttu-id="b97ad-184">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b97ad-184">RELATED LINKS</span></span>

[<span data-ttu-id="b97ad-185">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="b97ad-185">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="b97ad-186">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="b97ad-186">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="b97ad-187">Satz-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="b97ad-187">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


