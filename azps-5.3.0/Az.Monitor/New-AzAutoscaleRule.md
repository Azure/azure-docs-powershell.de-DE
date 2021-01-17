---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: cd4e374909fa58f036a0f67cd7a89bb968defd71
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459019"
---
# <span data-ttu-id="b7eea-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="b7eea-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="b7eea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7eea-102">SYNOPSIS</span></span>
<span data-ttu-id="b7eea-103">Erstellt eine Autoskalenregel.</span><span class="sxs-lookup"><span data-stu-id="b7eea-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="b7eea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7eea-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7eea-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b7eea-105">DESCRIPTION</span></span>
<span data-ttu-id="b7eea-106">Das **Cmdlet "New-AzAutoscaleRule"** erstellt eine Autoskalenregel.</span><span class="sxs-lookup"><span data-stu-id="b7eea-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="b7eea-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b7eea-107">EXAMPLES</span></span>

### <span data-ttu-id="b7eea-108">Beispiel 1: Erstellen einer Regel</span><span class="sxs-lookup"><span data-stu-id="b7eea-108">Example 1: Create a rule</span></span>
```powershell
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="b7eea-109">Mit diesem Befehl wird eine Regel erstellt.</span><span class="sxs-lookup"><span data-stu-id="b7eea-109">This command creates a rule.</span></span>

### <span data-ttu-id="b7eea-110">Beispiel 2: Erstellen von zwei Regeln</span><span class="sxs-lookup"><span data-stu-id="b7eea-110">Example 2: Create two rules</span></span>
```powershell
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="b7eea-111">Der erste Befehl erstellt eine Regel für die Metrik "Anforderungen" und speichert sie dann in $Rule 1-Variable.</span><span class="sxs-lookup"><span data-stu-id="b7eea-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="b7eea-112">Der zweite Befehl erstellt eine zweite Regel für die Metrik "Anforderungen" und speichert sie dann in der $Rule 2-Variable.</span><span class="sxs-lookup"><span data-stu-id="b7eea-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

### <span data-ttu-id="b7eea-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b7eea-113">Example 3</span></span>

<span data-ttu-id="b7eea-114">Erstellt eine Autoskalenregel.</span><span class="sxs-lookup"><span data-stu-id="b7eea-114">Creates an Autoscale rule.</span></span> <span data-ttu-id="b7eea-115">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="b7eea-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzAutoscaleRule -MetricName 'Requests' -MetricResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite' -MetricStatistic Average -Operator Equals -ScaleActionCooldown 00:05:00 -ScaleActionDirection None -ScaleActionScaleType ChangeCount -ScaleActionValue '1' -Threshold 10 -TimeGrain 00:01:00 -TimeWindow <TimeSpan>
```

## <span data-ttu-id="b7eea-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7eea-116">PARAMETERS</span></span>

### <span data-ttu-id="b7eea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7eea-117">-DefaultProfile</span></span>
<span data-ttu-id="b7eea-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b7eea-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7eea-119">-MetricName</span><span class="sxs-lookup"><span data-stu-id="b7eea-119">-MetricName</span></span>
<span data-ttu-id="b7eea-120">Gibt den Namen der Metrik an.</span><span class="sxs-lookup"><span data-stu-id="b7eea-120">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="b7eea-121">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="b7eea-121">-MetricResourceId</span></span>
<span data-ttu-id="b7eea-122">Gibt die metrische Ressourcen-ID an.</span><span class="sxs-lookup"><span data-stu-id="b7eea-122">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="b7eea-123">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="b7eea-123">-MetricStatistic</span></span>
<span data-ttu-id="b7eea-124">Gibt die metrische Statistik an.</span><span class="sxs-lookup"><span data-stu-id="b7eea-124">Specifies the metric statistic.</span></span>
<span data-ttu-id="b7eea-125">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="b7eea-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7eea-126">Mittelwert</span><span class="sxs-lookup"><span data-stu-id="b7eea-126">Average</span></span>
- <span data-ttu-id="b7eea-127">Min</span><span class="sxs-lookup"><span data-stu-id="b7eea-127">Min</span></span>
- <span data-ttu-id="b7eea-128">Max</span><span class="sxs-lookup"><span data-stu-id="b7eea-128">Max</span></span>
- <span data-ttu-id="b7eea-129">Summe</span><span class="sxs-lookup"><span data-stu-id="b7eea-129">Sum</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType
Parameter Sets: (All)
Aliases:
Accepted values: Average, Min, Max, Sum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7eea-130">-Operator</span><span class="sxs-lookup"><span data-stu-id="b7eea-130">-Operator</span></span>
<span data-ttu-id="b7eea-131">Gibt den Operator an.</span><span class="sxs-lookup"><span data-stu-id="b7eea-131">Specifies the operator.</span></span>
<span data-ttu-id="b7eea-132">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="b7eea-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7eea-133">Gleich</span><span class="sxs-lookup"><span data-stu-id="b7eea-133">Equals</span></span>
- <span data-ttu-id="b7eea-134">NotEquals</span><span class="sxs-lookup"><span data-stu-id="b7eea-134">NotEquals</span></span>
- <span data-ttu-id="b7eea-135">Greater Durchf</span><span class="sxs-lookup"><span data-stu-id="b7eea-135">GreaterThan</span></span>
- <span data-ttu-id="b7eea-136">GreaterHanaOrEqual</span><span class="sxs-lookup"><span data-stu-id="b7eea-136">GreaterThanOrEqual</span></span>
- <span data-ttu-id="b7eea-137">Less Immer</span><span class="sxs-lookup"><span data-stu-id="b7eea-137">LessThan</span></span>
- <span data-ttu-id="b7eea-138">LessHanaOrEqual</span><span class="sxs-lookup"><span data-stu-id="b7eea-138">LessThanOrEqual</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType
Parameter Sets: (All)
Aliases:
Accepted values: Equals, NotEquals, GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7eea-139">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="b7eea-139">-ScaleActionCooldown</span></span>
<span data-ttu-id="b7eea-140">Gibt die Abklingzeit für die Aktion "Autoskala" an.</span><span class="sxs-lookup"><span data-stu-id="b7eea-140">Specifies the Autoscale action cooldown time.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7eea-141">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="b7eea-141">-ScaleActionDirection</span></span>
<span data-ttu-id="b7eea-142">Gibt die Richtung der Skalierungsaktion an.</span><span class="sxs-lookup"><span data-stu-id="b7eea-142">Specifies the scale action direction.</span></span>
<span data-ttu-id="b7eea-143">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="b7eea-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7eea-144">Keine</span><span class="sxs-lookup"><span data-stu-id="b7eea-144">None</span></span>
- <span data-ttu-id="b7eea-145">Erhöhen</span><span class="sxs-lookup"><span data-stu-id="b7eea-145">Increase</span></span>
- <span data-ttu-id="b7eea-146">Verringern</span><span class="sxs-lookup"><span data-stu-id="b7eea-146">Decrease</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection
Parameter Sets: (All)
Aliases:
Accepted values: None, Increase, Decrease

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7eea-147">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="b7eea-147">-ScaleActionScaleType</span></span>
<span data-ttu-id="b7eea-148">Gibt den Skalierungstyp an.</span><span class="sxs-lookup"><span data-stu-id="b7eea-148">Specifies the scale type.</span></span>
<span data-ttu-id="b7eea-149">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="b7eea-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7eea-150">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="b7eea-150">ChangeSize</span></span>
- <span data-ttu-id="b7eea-151">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="b7eea-151">ChangeCount</span></span>
- <span data-ttu-id="b7eea-152">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="b7eea-152">PercentChangeCount</span></span>
- <span data-ttu-id="b7eea-153">ExactCount</span><span class="sxs-lookup"><span data-stu-id="b7eea-153">ExactCount</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ScaleType
Parameter Sets: (All)
Aliases:
Accepted values: ChangeCount, PercentChangeCount, ExactCount

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7eea-154">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="b7eea-154">-ScaleActionValue</span></span>
<span data-ttu-id="b7eea-155">Gibt den Aktionswert an.</span><span class="sxs-lookup"><span data-stu-id="b7eea-155">Specifies the action value.</span></span>

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

### <span data-ttu-id="b7eea-156">-Threshold</span><span class="sxs-lookup"><span data-stu-id="b7eea-156">-Threshold</span></span>
<span data-ttu-id="b7eea-157">Gibt den Schwellenwert für den metrischen Wert an.</span><span class="sxs-lookup"><span data-stu-id="b7eea-157">Specifies the threshold of the metric value.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7eea-158">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="b7eea-158">-TimeAggregationOperator</span></span>
<span data-ttu-id="b7eea-159">Gibt den Zeitaggregationsoperator an.</span><span class="sxs-lookup"><span data-stu-id="b7eea-159">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="b7eea-160">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="b7eea-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7eea-161">Mittelwert</span><span class="sxs-lookup"><span data-stu-id="b7eea-161">Average</span></span>
- <span data-ttu-id="b7eea-162">Minimum</span><span class="sxs-lookup"><span data-stu-id="b7eea-162">Minimum</span></span>
- <span data-ttu-id="b7eea-163">Maximum</span><span class="sxs-lookup"><span data-stu-id="b7eea-163">Maximum</span></span>
- <span data-ttu-id="b7eea-164">Nach</span><span class="sxs-lookup"><span data-stu-id="b7eea-164">Last</span></span>
- <span data-ttu-id="b7eea-165">Summe, Anzahl</span><span class="sxs-lookup"><span data-stu-id="b7eea-165">Total, Count</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType
Parameter Sets: (All)
Aliases:
Accepted values: Average, Minimum, Maximum, Total, Count

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7eea-166">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="b7eea-166">-TimeGrain</span></span>
<span data-ttu-id="b7eea-167">Gibt die Zeitkörner an.</span><span class="sxs-lookup"><span data-stu-id="b7eea-167">Specifies the time grain.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7eea-168">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="b7eea-168">-TimeWindow</span></span>
<span data-ttu-id="b7eea-169">Gibt das Zeitfenster an.</span><span class="sxs-lookup"><span data-stu-id="b7eea-169">Specifies the time window.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7eea-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7eea-170">CommonParameters</span></span>
<span data-ttu-id="b7eea-171">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7eea-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7eea-172">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7eea-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7eea-173">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b7eea-173">INPUTS</span></span>

### <span data-ttu-id="b7eea-174">System.String</span><span class="sxs-lookup"><span data-stu-id="b7eea-174">System.String</span></span>

### <span data-ttu-id="b7eea-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="b7eea-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="b7eea-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="b7eea-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="b7eea-177">System.Double</span><span class="sxs-lookup"><span data-stu-id="b7eea-177">System.Double</span></span>

### <span data-ttu-id="b7eea-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span><span class="sxs-lookup"><span data-stu-id="b7eea-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="b7eea-179">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="b7eea-179">System.TimeSpan</span></span>

### <span data-ttu-id="b7eea-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="b7eea-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="b7eea-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span><span class="sxs-lookup"><span data-stu-id="b7eea-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="b7eea-182">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b7eea-182">OUTPUTS</span></span>

### <span data-ttu-id="b7eea-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span><span class="sxs-lookup"><span data-stu-id="b7eea-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="b7eea-184">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b7eea-184">NOTES</span></span>

## <span data-ttu-id="b7eea-185">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b7eea-185">RELATED LINKS</span></span>

[<span data-ttu-id="b7eea-186">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b7eea-186">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="b7eea-187">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="b7eea-187">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="b7eea-188">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b7eea-188">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="b7eea-189">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="b7eea-189">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="b7eea-190">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b7eea-190">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


