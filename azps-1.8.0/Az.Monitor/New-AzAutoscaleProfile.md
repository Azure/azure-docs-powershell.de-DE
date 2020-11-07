---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
ms.openlocfilehash: 5fef7a4431c9527fa043ab81490c8251c75ebd9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93818919"
---
# <span data-ttu-id="97f55-101">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="97f55-101">New-AzAutoscaleProfile</span></span>

## <span data-ttu-id="97f55-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="97f55-102">SYNOPSIS</span></span>
<span data-ttu-id="97f55-103">Erstellt ein AutoScale-Profil.</span><span class="sxs-lookup"><span data-stu-id="97f55-103">Creates an Autoscale profile.</span></span>

## <span data-ttu-id="97f55-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="97f55-104">SYNTAX</span></span>

### <span data-ttu-id="97f55-105">CreateWithoutScheduledTimes</span><span class="sxs-lookup"><span data-stu-id="97f55-105">CreateWithoutScheduledTimes</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97f55-106">CreateWithFixedDateScheduling</span><span class="sxs-lookup"><span data-stu-id="97f55-106">CreateWithFixedDateScheduling</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97f55-107">CreateUsingRecurrentScheduling</span><span class="sxs-lookup"><span data-stu-id="97f55-107">CreateUsingRecurrentScheduling</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDay <System.Collections.Generic.List`1[System.String]>
 -ScheduleHour <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinute <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97f55-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97f55-108">DESCRIPTION</span></span>
<span data-ttu-id="97f55-109">Das Cmdlet **New-AzAutoscaleProfile** erstellt ein AutoScale-Profil.</span><span class="sxs-lookup"><span data-stu-id="97f55-109">The **New-AzAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="97f55-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="97f55-110">EXAMPLES</span></span>

### <span data-ttu-id="97f55-111">Beispiel 1: Erstellen eines einzelnen Profils mit einem festen Datum</span><span class="sxs-lookup"><span data-stu-id="97f55-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="97f55-112">Der erste Befehl erstellt eine AutoScale-Regel mit dem Namen "Anforderungen" und speichert Sie dann in der $Rule-Variablen.</span><span class="sxs-lookup"><span data-stu-id="97f55-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="97f55-113">Der zweite Befehl erstellt ein Profil mit dem Namen Profile01 mit einem festen Datum, wobei die Regel in $Rule verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="97f55-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="97f55-114">Beispiel 2: Erstellen eines Profils mit einem Terminplan</span><span class="sxs-lookup"><span data-stu-id="97f55-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="97f55-115">Der erste Befehl erstellt eine AutoScale-Regel mit dem Namen "Anforderungen" und speichert Sie dann in der $Rule-Variablen.</span><span class="sxs-lookup"><span data-stu-id="97f55-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="97f55-116">Der zweite Befehl erstellt ein Profil mit dem Namen SecondProfileName mit einem wiederkehrenden Zeitplan, wobei die Regel in $Rule verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="97f55-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="97f55-117">Beispiel 3: Erstellen von Profilen mit zwei Regeln</span><span class="sxs-lookup"><span data-stu-id="97f55-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDays "1" -ScheduleHours 5 -ScheduleMinutes 15 -ScheduleTimeZone UTC
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : profileName
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="97f55-118">Die ersten beiden Befehle erstellen Regeln und speichern Sie in den Variablen $Rule 1 und $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="97f55-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>
<span data-ttu-id="97f55-119">Der dritte Befehl erstellt mit den Regeln in Rule1 und Rule2 ein Profil mit dem Namen Profile Name und speichert es dann in der $Profile 1-Variablen.</span><span class="sxs-lookup"><span data-stu-id="97f55-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>
<span data-ttu-id="97f55-120">Der endgültige Befehl erstellt mithilfe der Regeln in Rule1 und Rule2 ein Profil mit dem Namen SecondProfileName und speichert es dann in der Variablen $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="97f55-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="97f55-121">Beispiel 4: Erstellen eines Profils ohne Terminplan oder festes Datum</span><span class="sxs-lookup"><span data-stu-id="97f55-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "ProfileName"
```

<span data-ttu-id="97f55-122">Der erste Befehl erstellt eine AutoScale-Regel mit dem Namen "Anforderungen" und speichert Sie dann in der $Rule-Variablen.</span><span class="sxs-lookup"><span data-stu-id="97f55-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="97f55-123">Der zweite Befehl erstellt ein Profil ohne Zeitplan oder ein festes Datum und speichert es dann in der $Profile Variablen.</span><span class="sxs-lookup"><span data-stu-id="97f55-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="97f55-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="97f55-124">PARAMETERS</span></span>

### <span data-ttu-id="97f55-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="97f55-125">-DefaultCapacity</span></span>
<span data-ttu-id="97f55-126">Gibt die Standardkapazität an.</span><span class="sxs-lookup"><span data-stu-id="97f55-126">Specifies the default capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f55-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97f55-127">-DefaultProfile</span></span>
<span data-ttu-id="97f55-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="97f55-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97f55-129">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="97f55-129">-EndTimeWindow</span></span>
<span data-ttu-id="97f55-130">Gibt das Ende des Zeitfensters an.</span><span class="sxs-lookup"><span data-stu-id="97f55-130">Specifies the end of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f55-131">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="97f55-131">-MaximumCapacity</span></span>
<span data-ttu-id="97f55-132">Gibt die maximale Kapazität an.</span><span class="sxs-lookup"><span data-stu-id="97f55-132">Specifies the maximum capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f55-133">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="97f55-133">-MinimumCapacity</span></span>
<span data-ttu-id="97f55-134">Gibt die minimale Kapazität an.</span><span class="sxs-lookup"><span data-stu-id="97f55-134">Specifies the minimum capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f55-135">-Name</span><span class="sxs-lookup"><span data-stu-id="97f55-135">-Name</span></span>
<span data-ttu-id="97f55-136">Gibt den Namen des zu erstellendes Profils an.</span><span class="sxs-lookup"><span data-stu-id="97f55-136">Specifies the name of the profile to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f55-137">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="97f55-137">-RecurrenceFrequency</span></span>
<span data-ttu-id="97f55-138">Gibt die Häufigkeit der Wiederholung an.</span><span class="sxs-lookup"><span data-stu-id="97f55-138">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="97f55-139">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="97f55-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="97f55-140">Keine</span><span class="sxs-lookup"><span data-stu-id="97f55-140">None</span></span>
- <span data-ttu-id="97f55-141">Zweiten</span><span class="sxs-lookup"><span data-stu-id="97f55-141">Second</span></span>
- <span data-ttu-id="97f55-142">Minuten</span><span class="sxs-lookup"><span data-stu-id="97f55-142">Minute</span></span>
- <span data-ttu-id="97f55-143">Stunde</span><span class="sxs-lookup"><span data-stu-id="97f55-143">Hour</span></span>
- <span data-ttu-id="97f55-144">Tag</span><span class="sxs-lookup"><span data-stu-id="97f55-144">Day</span></span>
- <span data-ttu-id="97f55-145">Woche</span><span class="sxs-lookup"><span data-stu-id="97f55-145">Week</span></span>
- <span data-ttu-id="97f55-146">Monat</span><span class="sxs-lookup"><span data-stu-id="97f55-146">Month</span></span>
- <span data-ttu-id="97f55-147">Jahr nicht alle diese Werte werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="97f55-147">Year Not all of these values are supported.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f55-148">-Rule</span><span class="sxs-lookup"><span data-stu-id="97f55-148">-Rule</span></span>
<span data-ttu-id="97f55-149">Gibt die Liste der Regeln an, die dem Profil hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="97f55-149">Specifies the list of rules to add to the profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f55-150">-ScheduleDay</span><span class="sxs-lookup"><span data-stu-id="97f55-150">-ScheduleDay</span></span>
<span data-ttu-id="97f55-151">Gibt die geplanten Tage an.</span><span class="sxs-lookup"><span data-stu-id="97f55-151">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f55-152">-ScheduleHour</span><span class="sxs-lookup"><span data-stu-id="97f55-152">-ScheduleHour</span></span>
<span data-ttu-id="97f55-153">Gibt die geplanten Stunden an.</span><span class="sxs-lookup"><span data-stu-id="97f55-153">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f55-154">-ScheduleMinute</span><span class="sxs-lookup"><span data-stu-id="97f55-154">-ScheduleMinute</span></span>
<span data-ttu-id="97f55-155">Gibt die geplanten Minuten an.</span><span class="sxs-lookup"><span data-stu-id="97f55-155">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f55-156">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="97f55-156">-ScheduleTimeZone</span></span>
<span data-ttu-id="97f55-157">Gibt die Zeitzone des Zeitplans an.</span><span class="sxs-lookup"><span data-stu-id="97f55-157">Specifies the time zone of the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f55-158">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="97f55-158">-StartTimeWindow</span></span>
<span data-ttu-id="97f55-159">Gibt den Anfang des Zeitfensters an.</span><span class="sxs-lookup"><span data-stu-id="97f55-159">Specifies the start of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f55-160">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="97f55-160">-TimeWindowTimeZone</span></span>
<span data-ttu-id="97f55-161">Gibt die Zeitzone des Zeitfensters an.</span><span class="sxs-lookup"><span data-stu-id="97f55-161">Specifies the time zone of the time window.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f55-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97f55-162">CommonParameters</span></span>
<span data-ttu-id="97f55-163">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97f55-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97f55-164">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97f55-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97f55-165">Eingaben</span><span class="sxs-lookup"><span data-stu-id="97f55-165">INPUTS</span></span>

### <span data-ttu-id="97f55-166">System. String</span><span class="sxs-lookup"><span data-stu-id="97f55-166">System.String</span></span>

### <span data-ttu-id="97f55-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="97f55-167">System.DateTime</span></span>

### <span data-ttu-id="97f55-168">Microsoft. Azure. Management. Monitor. Management. Models. RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="97f55-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span></span>

### <span data-ttu-id="97f55-169">System. Collections. Generic. List ' 1 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="97f55-169">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="97f55-170">System. Collections. Generic. List `1[[System.Nullable` 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]], System. private. CoreLib, Version = 4.0.0.0; Kultur = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="97f55-170">System.Collections.Generic.List`1[[System.Nullable`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]], System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="97f55-171">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Management. Monitor. Management. Models. ScaleRule, Microsoft. Azure. PowerShell. Cmdlets. Monitor, Version = 1.0.0.0, Kultur = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="97f55-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="97f55-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="97f55-172">OUTPUTS</span></span>

### <span data-ttu-id="97f55-173">Microsoft. Azure. Management. Monitor. Management. Models. AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="97f55-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="97f55-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="97f55-174">NOTES</span></span>

## <span data-ttu-id="97f55-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="97f55-175">RELATED LINKS</span></span>

[<span data-ttu-id="97f55-176">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="97f55-176">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="97f55-177">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="97f55-177">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="97f55-178">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="97f55-178">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="97f55-179">Neu – AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="97f55-179">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="97f55-180">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="97f55-180">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


