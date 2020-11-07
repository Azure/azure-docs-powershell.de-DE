---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscaleprofile
schema: 2.0.0
ms.openlocfilehash: 2192a03713b82e49f1958a34678353856197b3a6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850820"
---
# <span data-ttu-id="85660-101">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="85660-101">New-AzureRmAutoscaleProfile</span></span>

## <span data-ttu-id="85660-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="85660-102">SYNOPSIS</span></span>
<span data-ttu-id="85660-103">Erstellt ein AutoScale-Profil.</span><span class="sxs-lookup"><span data-stu-id="85660-103">Creates an Autoscale profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85660-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="85660-104">SYNTAX</span></span>

### <span data-ttu-id="85660-105">CreateWithoutScheduledTimes</span><span class="sxs-lookup"><span data-stu-id="85660-105">CreateWithoutScheduledTimes</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85660-106">CreateWithFixedDateScheduling</span><span class="sxs-lookup"><span data-stu-id="85660-106">CreateWithFixedDateScheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85660-107">CreateUsingRecurrentScheduling</span><span class="sxs-lookup"><span data-stu-id="85660-107">CreateUsingRecurrentScheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDay <System.Collections.Generic.List`1[System.String]>
 -ScheduleHour <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinute <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85660-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85660-108">DESCRIPTION</span></span>
<span data-ttu-id="85660-109">Das Cmdlet **New-AzureRmAutoscaleProfile** erstellt ein AutoScale-Profil.</span><span class="sxs-lookup"><span data-stu-id="85660-109">The **New-AzureRmAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="85660-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85660-110">EXAMPLES</span></span>

### <span data-ttu-id="85660-111">Beispiel 1: Erstellen eines einzelnen Profils mit einem festen Datum</span><span class="sxs-lookup"><span data-stu-id="85660-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="85660-112">Der erste Befehl erstellt eine AutoScale-Regel mit dem Namen "Anforderungen" und speichert Sie dann in der $Rule-Variablen.</span><span class="sxs-lookup"><span data-stu-id="85660-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="85660-113">Der zweite Befehl erstellt ein Profil mit dem Namen Profile01 mit einem festen Datum, wobei die Regel in $Rule verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="85660-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="85660-114">Beispiel 2: Erstellen eines Profils mit einem Terminplan</span><span class="sxs-lookup"><span data-stu-id="85660-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="85660-115">Der erste Befehl erstellt eine AutoScale-Regel mit dem Namen "Anforderungen" und speichert Sie dann in der $Rule-Variablen.</span><span class="sxs-lookup"><span data-stu-id="85660-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="85660-116">Der zweite Befehl erstellt ein Profil mit dem Namen SecondProfileName mit einem wiederkehrenden Zeitplan, wobei die Regel in $Rule verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="85660-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="85660-117">Beispiel 3: Erstellen von Profilen mit zwei Regeln</span><span class="sxs-lookup"><span data-stu-id="85660-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDays "1" -ScheduleHours 5 -ScheduleMinutes 15 -ScheduleTimeZone UTC
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

<span data-ttu-id="85660-118">Die ersten beiden Befehle erstellen Regeln und speichern Sie in den Variablen $Rule 1 und $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="85660-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>
<span data-ttu-id="85660-119">Der dritte Befehl erstellt mit den Regeln in Rule1 und Rule2 ein Profil mit dem Namen Profile Name und speichert es dann in der $Profile 1-Variablen.</span><span class="sxs-lookup"><span data-stu-id="85660-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>
<span data-ttu-id="85660-120">Der endgültige Befehl erstellt mithilfe der Regeln in Rule1 und Rule2 ein Profil mit dem Namen SecondProfileName und speichert es dann in der Variablen $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="85660-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="85660-121">Beispiel 4: Erstellen eines Profils ohne Terminplan oder festes Datum</span><span class="sxs-lookup"><span data-stu-id="85660-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "ProfileName"
```

<span data-ttu-id="85660-122">Der erste Befehl erstellt eine AutoScale-Regel mit dem Namen "Anforderungen" und speichert Sie dann in der $Rule-Variablen.</span><span class="sxs-lookup"><span data-stu-id="85660-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="85660-123">Der zweite Befehl erstellt ein Profil ohne Zeitplan oder ein festes Datum und speichert es dann in der $Profile Variablen.</span><span class="sxs-lookup"><span data-stu-id="85660-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="85660-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="85660-124">PARAMETERS</span></span>

### <span data-ttu-id="85660-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="85660-125">-DefaultCapacity</span></span>
<span data-ttu-id="85660-126">Gibt die Standardkapazität an.</span><span class="sxs-lookup"><span data-stu-id="85660-126">Specifies the default capacity.</span></span>

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

### <span data-ttu-id="85660-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85660-127">-DefaultProfile</span></span>
<span data-ttu-id="85660-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="85660-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85660-129">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="85660-129">-EndTimeWindow</span></span>
<span data-ttu-id="85660-130">Gibt das Ende des Zeitfensters an.</span><span class="sxs-lookup"><span data-stu-id="85660-130">Specifies the end of the time window.</span></span>

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

### <span data-ttu-id="85660-131">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="85660-131">-MaximumCapacity</span></span>
<span data-ttu-id="85660-132">Gibt die maximale Kapazität an.</span><span class="sxs-lookup"><span data-stu-id="85660-132">Specifies the maximum capacity.</span></span>

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

### <span data-ttu-id="85660-133">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="85660-133">-MinimumCapacity</span></span>
<span data-ttu-id="85660-134">Gibt die minimale Kapazität an.</span><span class="sxs-lookup"><span data-stu-id="85660-134">Specifies the minimum capacity.</span></span>

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

### <span data-ttu-id="85660-135">-Name</span><span class="sxs-lookup"><span data-stu-id="85660-135">-Name</span></span>
<span data-ttu-id="85660-136">Gibt den Namen des zu erstellendes Profils an.</span><span class="sxs-lookup"><span data-stu-id="85660-136">Specifies the name of the profile to create.</span></span>

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

### <span data-ttu-id="85660-137">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="85660-137">-RecurrenceFrequency</span></span>
<span data-ttu-id="85660-138">Gibt die Häufigkeit der Wiederholung an.</span><span class="sxs-lookup"><span data-stu-id="85660-138">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="85660-139">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="85660-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="85660-140">Keine</span><span class="sxs-lookup"><span data-stu-id="85660-140">None</span></span>
- <span data-ttu-id="85660-141">Zweiten</span><span class="sxs-lookup"><span data-stu-id="85660-141">Second</span></span>
- <span data-ttu-id="85660-142">Minuten</span><span class="sxs-lookup"><span data-stu-id="85660-142">Minute</span></span>
- <span data-ttu-id="85660-143">Stunde</span><span class="sxs-lookup"><span data-stu-id="85660-143">Hour</span></span>
- <span data-ttu-id="85660-144">Tag</span><span class="sxs-lookup"><span data-stu-id="85660-144">Day</span></span>
- <span data-ttu-id="85660-145">Woche</span><span class="sxs-lookup"><span data-stu-id="85660-145">Week</span></span>
- <span data-ttu-id="85660-146">Monat</span><span class="sxs-lookup"><span data-stu-id="85660-146">Month</span></span>
- <span data-ttu-id="85660-147">Jahr nicht alle diese Werte werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="85660-147">Year Not all of these values are supported.</span></span>

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

### <span data-ttu-id="85660-148">-Rule</span><span class="sxs-lookup"><span data-stu-id="85660-148">-Rule</span></span>
<span data-ttu-id="85660-149">Gibt die Liste der Regeln an, die dem Profil hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="85660-149">Specifies the list of rules to add to the profile.</span></span>

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

### <span data-ttu-id="85660-150">-ScheduleDay</span><span class="sxs-lookup"><span data-stu-id="85660-150">-ScheduleDay</span></span>
<span data-ttu-id="85660-151">Gibt die geplanten Tage an.</span><span class="sxs-lookup"><span data-stu-id="85660-151">Specifies the scheduled days.</span></span>

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

### <span data-ttu-id="85660-152">-ScheduleHour</span><span class="sxs-lookup"><span data-stu-id="85660-152">-ScheduleHour</span></span>
<span data-ttu-id="85660-153">Gibt die geplanten Stunden an.</span><span class="sxs-lookup"><span data-stu-id="85660-153">Specifies the scheduled hours.</span></span>

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

### <span data-ttu-id="85660-154">-ScheduleMinute</span><span class="sxs-lookup"><span data-stu-id="85660-154">-ScheduleMinute</span></span>
<span data-ttu-id="85660-155">Gibt die geplanten Minuten an.</span><span class="sxs-lookup"><span data-stu-id="85660-155">Specifies the scheduled minutes.</span></span>

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

### <span data-ttu-id="85660-156">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="85660-156">-ScheduleTimeZone</span></span>
<span data-ttu-id="85660-157">Gibt die Zeitzone des Zeitplans an.</span><span class="sxs-lookup"><span data-stu-id="85660-157">Specifies the time zone of the schedule.</span></span>

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

### <span data-ttu-id="85660-158">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="85660-158">-StartTimeWindow</span></span>
<span data-ttu-id="85660-159">Gibt den Anfang des Zeitfensters an.</span><span class="sxs-lookup"><span data-stu-id="85660-159">Specifies the start of the time window.</span></span>

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

### <span data-ttu-id="85660-160">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="85660-160">-TimeWindowTimeZone</span></span>
<span data-ttu-id="85660-161">Gibt die Zeitzone des Zeitfensters an.</span><span class="sxs-lookup"><span data-stu-id="85660-161">Specifies the time zone of the time window.</span></span>

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

### <span data-ttu-id="85660-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85660-162">CommonParameters</span></span>
<span data-ttu-id="85660-163">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85660-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85660-164">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85660-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85660-165">Eingaben</span><span class="sxs-lookup"><span data-stu-id="85660-165">INPUTS</span></span>

### <span data-ttu-id="85660-166">System. String</span><span class="sxs-lookup"><span data-stu-id="85660-166">System.String</span></span>

### <span data-ttu-id="85660-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="85660-167">System.DateTime</span></span>

### <span data-ttu-id="85660-168">Microsoft. Azure. Management. Monitor. Management. Models. RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="85660-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span></span>

### <span data-ttu-id="85660-169">System. Collections. Generic. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="85660-169">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="85660-170">System. Collections. Generic. List `1[[System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089], mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="85660-170">System.Collections.Generic.List`1[[System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]], mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="85660-171">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Management. Monitor. Management. Models. ScaleRule, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="85660-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="85660-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="85660-172">OUTPUTS</span></span>

### <span data-ttu-id="85660-173">Microsoft. Azure. Management. Monitor. Management. Models. AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="85660-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="85660-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="85660-174">NOTES</span></span>

## <span data-ttu-id="85660-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="85660-175">RELATED LINKS</span></span>

[<span data-ttu-id="85660-176">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="85660-176">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="85660-177">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="85660-177">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="85660-178">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="85660-178">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="85660-179">Neu – AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="85660-179">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="85660-180">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="85660-180">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


