---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
ms.openlocfilehash: a5cea42544f2f24ad6c1f1cc1ce64bf122e53440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504153"
---
# <span data-ttu-id="8b832-101">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="8b832-101">New-AzureRmAutoscaleProfile</span></span>

## <span data-ttu-id="8b832-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b832-102">SYNOPSIS</span></span>
<span data-ttu-id="8b832-103">Erstellt ein AutoScale-Profil.</span><span class="sxs-lookup"><span data-stu-id="8b832-103">Creates an Autoscale profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b832-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b832-104">SYNTAX</span></span>

### <span data-ttu-id="8b832-105">Parameter für New-AzureRmAutoscaleProfile-Cmdlet ohne geplante Zeiten</span><span class="sxs-lookup"><span data-stu-id="8b832-105">Parameters for New-AzureRmAutoscaleProfile cmdlet without scheduled times</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b832-106">Parameter für New-AzureRmAutoscaleProfile-Cmdlet mithilfe der Fix-Terminplanung</span><span class="sxs-lookup"><span data-stu-id="8b832-106">Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b832-107">Parameter für New-AzureRmAutoscaleProfile-Cmdlet mithilfe der wiederkehrenden Terminplanung</span><span class="sxs-lookup"><span data-stu-id="8b832-107">Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDays <System.Collections.Generic.List`1[System.String]>
 -ScheduleHours <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinutes <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b832-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b832-108">DESCRIPTION</span></span>
<span data-ttu-id="8b832-109">Das Cmdlet **New-AzureRmAutoscaleProfile** erstellt ein AutoScale-Profil.</span><span class="sxs-lookup"><span data-stu-id="8b832-109">The **New-AzureRmAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="8b832-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b832-110">EXAMPLES</span></span>

### <span data-ttu-id="8b832-111">Beispiel 1: Erstellen eines einzelnen Profils mit einem festen Datum</span><span class="sxs-lookup"><span data-stu-id="8b832-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="8b832-112">Der erste Befehl erstellt eine AutoScale-Regel mit dem Namen "Anforderungen" und speichert Sie dann in der $Rule-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8b832-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="8b832-113">Der zweite Befehl erstellt ein Profil mit dem Namen Profile01 mit einem festen Datum, wobei die Regel in $Rule verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8b832-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="8b832-114">Beispiel 2: Erstellen eines Profils mit einem Terminplan</span><span class="sxs-lookup"><span data-stu-id="8b832-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="8b832-115">Der erste Befehl erstellt eine AutoScale-Regel mit dem Namen "Anforderungen" und speichert Sie dann in der $Rule-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8b832-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="8b832-116">Der zweite Befehl erstellt ein Profil mit dem Namen SecondProfileName mit einem wiederkehrenden Zeitplan, wobei die Regel in $Rule verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8b832-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="8b832-117">Beispiel 3: Erstellen von Profilen mit zwei Regeln</span><span class="sxs-lookup"><span data-stu-id="8b832-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDays "1" -ScheduleHours 5 -ScheduleMinutes 15 -ScheduleTimeZone UTC
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

<span data-ttu-id="8b832-118">Die ersten beiden Befehle erstellen Regeln und speichern Sie in den Variablen $Rule 1 und $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="8b832-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>

<span data-ttu-id="8b832-119">Der dritte Befehl erstellt mit den Regeln in Rule1 und Rule2 ein Profil mit dem Namen Profile Name und speichert es dann in der $Profile 1-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8b832-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>

<span data-ttu-id="8b832-120">Der endgültige Befehl erstellt mithilfe der Regeln in Rule1 und Rule2 ein Profil mit dem Namen SecondProfileName und speichert es dann in der Variablen $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="8b832-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="8b832-121">Beispiel 4: Erstellen eines Profils ohne Terminplan oder festes Datum</span><span class="sxs-lookup"><span data-stu-id="8b832-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "ProfileName"
```

<span data-ttu-id="8b832-122">Der erste Befehl erstellt eine AutoScale-Regel mit dem Namen "Anforderungen" und speichert Sie dann in der $Rule-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8b832-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="8b832-123">Der zweite Befehl erstellt ein Profil ohne Zeitplan oder ein festes Datum und speichert es dann in der $Profile Variablen.</span><span class="sxs-lookup"><span data-stu-id="8b832-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="8b832-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b832-124">PARAMETERS</span></span>

### <span data-ttu-id="8b832-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="8b832-125">-DefaultCapacity</span></span>
<span data-ttu-id="8b832-126">Gibt die Standardkapazität an.</span><span class="sxs-lookup"><span data-stu-id="8b832-126">Specifies the default capacity.</span></span>

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

### <span data-ttu-id="8b832-127">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="8b832-127">-EndTimeWindow</span></span>
<span data-ttu-id="8b832-128">Gibt das Ende des Zeitfensters an.</span><span class="sxs-lookup"><span data-stu-id="8b832-128">Specifies the end of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b832-129">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="8b832-129">-MaximumCapacity</span></span>
<span data-ttu-id="8b832-130">Gibt die maximale Kapazität an.</span><span class="sxs-lookup"><span data-stu-id="8b832-130">Specifies the maximum capacity.</span></span>

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

### <span data-ttu-id="8b832-131">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="8b832-131">-MinimumCapacity</span></span>
<span data-ttu-id="8b832-132">Gibt die minimale Kapazität an.</span><span class="sxs-lookup"><span data-stu-id="8b832-132">Specifies the minimum capacity.</span></span>

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

### <span data-ttu-id="8b832-133">-Name</span><span class="sxs-lookup"><span data-stu-id="8b832-133">-Name</span></span>
<span data-ttu-id="8b832-134">Gibt den Namen des zu erstellendes Profils an.</span><span class="sxs-lookup"><span data-stu-id="8b832-134">Specifies the name of the profile to create.</span></span>

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

### <span data-ttu-id="8b832-135">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="8b832-135">-RecurrenceFrequency</span></span>
<span data-ttu-id="8b832-136">Gibt die Häufigkeit der Wiederholung an.</span><span class="sxs-lookup"><span data-stu-id="8b832-136">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="8b832-137">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8b832-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8b832-138">Keine</span><span class="sxs-lookup"><span data-stu-id="8b832-138">None</span></span>
- <span data-ttu-id="8b832-139">Zweiten</span><span class="sxs-lookup"><span data-stu-id="8b832-139">Second</span></span>
- <span data-ttu-id="8b832-140">Minuten</span><span class="sxs-lookup"><span data-stu-id="8b832-140">Minute</span></span>
- <span data-ttu-id="8b832-141">Stunde</span><span class="sxs-lookup"><span data-stu-id="8b832-141">Hour</span></span>
- <span data-ttu-id="8b832-142">Tag</span><span class="sxs-lookup"><span data-stu-id="8b832-142">Day</span></span>
- <span data-ttu-id="8b832-143">Woche</span><span class="sxs-lookup"><span data-stu-id="8b832-143">Week</span></span>
- <span data-ttu-id="8b832-144">Monat</span><span class="sxs-lookup"><span data-stu-id="8b832-144">Month</span></span>
- <span data-ttu-id="8b832-145">Jahr</span><span class="sxs-lookup"><span data-stu-id="8b832-145">Year</span></span>

<span data-ttu-id="8b832-146">Nicht alle diese Werte werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8b832-146">Not all of these values are supported.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b832-147">-Regeln</span><span class="sxs-lookup"><span data-stu-id="8b832-147">-Rules</span></span>
<span data-ttu-id="8b832-148">Gibt die Liste der Regeln an, die dem Profil hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8b832-148">Specifies the list of rules to add to the profile.</span></span>

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

### <span data-ttu-id="8b832-149">-ScheduleDays</span><span class="sxs-lookup"><span data-stu-id="8b832-149">-ScheduleDays</span></span>
<span data-ttu-id="8b832-150">Gibt die geplanten Tage an.</span><span class="sxs-lookup"><span data-stu-id="8b832-150">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b832-151">-ScheduleHours</span><span class="sxs-lookup"><span data-stu-id="8b832-151">-ScheduleHours</span></span>
<span data-ttu-id="8b832-152">Gibt die geplanten Stunden an.</span><span class="sxs-lookup"><span data-stu-id="8b832-152">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b832-153">-ScheduleMinutes</span><span class="sxs-lookup"><span data-stu-id="8b832-153">-ScheduleMinutes</span></span>
<span data-ttu-id="8b832-154">Gibt die geplanten Minuten an.</span><span class="sxs-lookup"><span data-stu-id="8b832-154">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b832-155">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="8b832-155">-ScheduleTimeZone</span></span>
<span data-ttu-id="8b832-156">Gibt die Zeitzone des Zeitplans an.</span><span class="sxs-lookup"><span data-stu-id="8b832-156">Specifies the time zone of the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b832-157">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="8b832-157">-StartTimeWindow</span></span>
<span data-ttu-id="8b832-158">Gibt den Anfang des Zeitfensters an.</span><span class="sxs-lookup"><span data-stu-id="8b832-158">Specifies the start of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b832-159">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="8b832-159">-TimeWindowTimeZone</span></span>
<span data-ttu-id="8b832-160">Gibt die Zeitzone des Zeitfensters an.</span><span class="sxs-lookup"><span data-stu-id="8b832-160">Specifies the time zone of the time window.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b832-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b832-161">-DefaultProfile</span></span>
<span data-ttu-id="8b832-162">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b832-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b832-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b832-163">CommonParameters</span></span>
<span data-ttu-id="8b832-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b832-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b832-165">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b832-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b832-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b832-166">INPUTS</span></span>

## <span data-ttu-id="8b832-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b832-167">OUTPUTS</span></span>

### <span data-ttu-id="8b832-168">Microsoft. Azure. Management. Monitor. Management. Models. AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="8b832-168">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="8b832-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b832-169">NOTES</span></span>

## <span data-ttu-id="8b832-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b832-170">RELATED LINKS</span></span>

[<span data-ttu-id="8b832-171">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8b832-171">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="8b832-172">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="8b832-172">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="8b832-173">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8b832-173">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="8b832-174">Neu – AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="8b832-174">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="8b832-175">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8b832-175">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


