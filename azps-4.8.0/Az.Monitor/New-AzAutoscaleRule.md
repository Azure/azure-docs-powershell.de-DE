---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: cd4e374909fa58f036a0f67cd7a89bb968defd71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174637"
---
# <span data-ttu-id="5caa5-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="5caa5-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="5caa5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5caa5-102">SYNOPSIS</span></span>
<span data-ttu-id="5caa5-103">Erstellt eine AutoScale-Regel.</span><span class="sxs-lookup"><span data-stu-id="5caa5-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="5caa5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5caa5-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5caa5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5caa5-105">DESCRIPTION</span></span>
<span data-ttu-id="5caa5-106">Das Cmdlet **New-AzAutoscaleRule** erstellt eine AutoScale-Regel.</span><span class="sxs-lookup"><span data-stu-id="5caa5-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="5caa5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5caa5-107">EXAMPLES</span></span>

### <span data-ttu-id="5caa5-108">Beispiel 1: Erstellen einer Regel</span><span class="sxs-lookup"><span data-stu-id="5caa5-108">Example 1: Create a rule</span></span>
```powershell
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="5caa5-109">Mit diesem Befehl wird eine Regel erstellt.</span><span class="sxs-lookup"><span data-stu-id="5caa5-109">This command creates a rule.</span></span>

### <span data-ttu-id="5caa5-110">Beispiel 2: Erstellen von zwei Regeln</span><span class="sxs-lookup"><span data-stu-id="5caa5-110">Example 2: Create two rules</span></span>
```powershell
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="5caa5-111">Der erste Befehl erstellt eine Regel für die Anforderungs Metrik und speichert Sie dann in der $Rule 1-Variablen.</span><span class="sxs-lookup"><span data-stu-id="5caa5-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="5caa5-112">Der zweite Befehl erstellt eine zweite Regel für die Anforderungs Metrik und speichert Sie dann in der Variablen $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="5caa5-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

### <span data-ttu-id="5caa5-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5caa5-113">Example 3</span></span>

<span data-ttu-id="5caa5-114">Erstellt eine AutoScale-Regel.</span><span class="sxs-lookup"><span data-stu-id="5caa5-114">Creates an Autoscale rule.</span></span> <span data-ttu-id="5caa5-115">automatisch</span><span class="sxs-lookup"><span data-stu-id="5caa5-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzAutoscaleRule -MetricName 'Requests' -MetricResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite' -MetricStatistic Average -Operator Equals -ScaleActionCooldown 00:05:00 -ScaleActionDirection None -ScaleActionScaleType ChangeCount -ScaleActionValue '1' -Threshold 10 -TimeGrain 00:01:00 -TimeWindow <TimeSpan>
```

## <span data-ttu-id="5caa5-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="5caa5-116">PARAMETERS</span></span>

### <span data-ttu-id="5caa5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5caa5-117">-DefaultProfile</span></span>
<span data-ttu-id="5caa5-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5caa5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5caa5-119">-Metricname</span><span class="sxs-lookup"><span data-stu-id="5caa5-119">-MetricName</span></span>
<span data-ttu-id="5caa5-120">Gibt den Namen der Metrik an.</span><span class="sxs-lookup"><span data-stu-id="5caa5-120">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="5caa5-121">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="5caa5-121">-MetricResourceId</span></span>
<span data-ttu-id="5caa5-122">Gibt die metrische Ressourcen-ID an.</span><span class="sxs-lookup"><span data-stu-id="5caa5-122">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="5caa5-123">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="5caa5-123">-MetricStatistic</span></span>
<span data-ttu-id="5caa5-124">Gibt die metrische Statistik an.</span><span class="sxs-lookup"><span data-stu-id="5caa5-124">Specifies the metric statistic.</span></span>
<span data-ttu-id="5caa5-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5caa5-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5caa5-126">Mittelwert</span><span class="sxs-lookup"><span data-stu-id="5caa5-126">Average</span></span>
- <span data-ttu-id="5caa5-127">Min</span><span class="sxs-lookup"><span data-stu-id="5caa5-127">Min</span></span>
- <span data-ttu-id="5caa5-128">Max</span><span class="sxs-lookup"><span data-stu-id="5caa5-128">Max</span></span>
- <span data-ttu-id="5caa5-129">Summe</span><span class="sxs-lookup"><span data-stu-id="5caa5-129">Sum</span></span>

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

### <span data-ttu-id="5caa5-130">-Operator</span><span class="sxs-lookup"><span data-stu-id="5caa5-130">-Operator</span></span>
<span data-ttu-id="5caa5-131">Gibt den Operator an.</span><span class="sxs-lookup"><span data-stu-id="5caa5-131">Specifies the operator.</span></span>
<span data-ttu-id="5caa5-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5caa5-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5caa5-133">Gleich</span><span class="sxs-lookup"><span data-stu-id="5caa5-133">Equals</span></span>
- <span data-ttu-id="5caa5-134">NotEquals</span><span class="sxs-lookup"><span data-stu-id="5caa5-134">NotEquals</span></span>
- <span data-ttu-id="5caa5-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="5caa5-135">GreaterThan</span></span>
- <span data-ttu-id="5caa5-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="5caa5-136">GreaterThanOrEqual</span></span>
- <span data-ttu-id="5caa5-137">LessThan</span><span class="sxs-lookup"><span data-stu-id="5caa5-137">LessThan</span></span>
- <span data-ttu-id="5caa5-138">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="5caa5-138">LessThanOrEqual</span></span>

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

### <span data-ttu-id="5caa5-139">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="5caa5-139">-ScaleActionCooldown</span></span>
<span data-ttu-id="5caa5-140">Gibt die Abklingzeit der autoskala-Aktion an.</span><span class="sxs-lookup"><span data-stu-id="5caa5-140">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="5caa5-141">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="5caa5-141">-ScaleActionDirection</span></span>
<span data-ttu-id="5caa5-142">Gibt die Richtung der skalierungsaktion an.</span><span class="sxs-lookup"><span data-stu-id="5caa5-142">Specifies the scale action direction.</span></span>
<span data-ttu-id="5caa5-143">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5caa5-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5caa5-144">Keine</span><span class="sxs-lookup"><span data-stu-id="5caa5-144">None</span></span>
- <span data-ttu-id="5caa5-145">Vergrößern</span><span class="sxs-lookup"><span data-stu-id="5caa5-145">Increase</span></span>
- <span data-ttu-id="5caa5-146">Verkleinern</span><span class="sxs-lookup"><span data-stu-id="5caa5-146">Decrease</span></span>

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

### <span data-ttu-id="5caa5-147">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="5caa5-147">-ScaleActionScaleType</span></span>
<span data-ttu-id="5caa5-148">Gibt den Skalierungs an.</span><span class="sxs-lookup"><span data-stu-id="5caa5-148">Specifies the scale type.</span></span>
<span data-ttu-id="5caa5-149">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5caa5-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5caa5-150">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="5caa5-150">ChangeSize</span></span>
- <span data-ttu-id="5caa5-151">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="5caa5-151">ChangeCount</span></span>
- <span data-ttu-id="5caa5-152">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="5caa5-152">PercentChangeCount</span></span>
- <span data-ttu-id="5caa5-153">ExactCount</span><span class="sxs-lookup"><span data-stu-id="5caa5-153">ExactCount</span></span>

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

### <span data-ttu-id="5caa5-154">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="5caa5-154">-ScaleActionValue</span></span>
<span data-ttu-id="5caa5-155">Gibt den Wert der Aktion an.</span><span class="sxs-lookup"><span data-stu-id="5caa5-155">Specifies the action value.</span></span>

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

### <span data-ttu-id="5caa5-156">-Threshold</span><span class="sxs-lookup"><span data-stu-id="5caa5-156">-Threshold</span></span>
<span data-ttu-id="5caa5-157">Gibt den Schwellenwert für den Metrikwert an.</span><span class="sxs-lookup"><span data-stu-id="5caa5-157">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="5caa5-158">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="5caa5-158">-TimeAggregationOperator</span></span>
<span data-ttu-id="5caa5-159">Gibt den Zeit Aggregations Operator an.</span><span class="sxs-lookup"><span data-stu-id="5caa5-159">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="5caa5-160">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5caa5-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5caa5-161">Mittelwert</span><span class="sxs-lookup"><span data-stu-id="5caa5-161">Average</span></span>
- <span data-ttu-id="5caa5-162">Mindestens</span><span class="sxs-lookup"><span data-stu-id="5caa5-162">Minimum</span></span>
- <span data-ttu-id="5caa5-163">Maximale</span><span class="sxs-lookup"><span data-stu-id="5caa5-163">Maximum</span></span>
- <span data-ttu-id="5caa5-164">Letzten</span><span class="sxs-lookup"><span data-stu-id="5caa5-164">Last</span></span>
- <span data-ttu-id="5caa5-165">Summe, Anzahl</span><span class="sxs-lookup"><span data-stu-id="5caa5-165">Total, Count</span></span>

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

### <span data-ttu-id="5caa5-166">-Zeitkorn</span><span class="sxs-lookup"><span data-stu-id="5caa5-166">-TimeGrain</span></span>
<span data-ttu-id="5caa5-167">Gibt das Zeit Korn an.</span><span class="sxs-lookup"><span data-stu-id="5caa5-167">Specifies the time grain.</span></span>

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

### <span data-ttu-id="5caa5-168">-Fenster</span><span class="sxs-lookup"><span data-stu-id="5caa5-168">-TimeWindow</span></span>
<span data-ttu-id="5caa5-169">Gibt das Zeitfenster an.</span><span class="sxs-lookup"><span data-stu-id="5caa5-169">Specifies the time window.</span></span>

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

### <span data-ttu-id="5caa5-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5caa5-170">CommonParameters</span></span>
<span data-ttu-id="5caa5-171">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5caa5-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5caa5-172">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5caa5-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5caa5-173">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5caa5-173">INPUTS</span></span>

### <span data-ttu-id="5caa5-174">System. String</span><span class="sxs-lookup"><span data-stu-id="5caa5-174">System.String</span></span>

### <span data-ttu-id="5caa5-175">Microsoft. Azure. Management. Monitor. Management. Models. ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="5caa5-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="5caa5-176">Microsoft. Azure. Management. Monitor. Management. Models. MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="5caa5-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="5caa5-177">System. Double</span><span class="sxs-lookup"><span data-stu-id="5caa5-177">System.Double</span></span>

### <span data-ttu-id="5caa5-178">Microsoft. Azure. Management. Monitor. Management. Models. zeitaggregationtype</span><span class="sxs-lookup"><span data-stu-id="5caa5-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="5caa5-179">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="5caa5-179">System.TimeSpan</span></span>

### <span data-ttu-id="5caa5-180">Microsoft. Azure. Management. Monitor. Management. Models. ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="5caa5-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="5caa5-181">Microsoft. Azure. Management. Monitor. Management. Models. ScaleType</span><span class="sxs-lookup"><span data-stu-id="5caa5-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="5caa5-182">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5caa5-182">OUTPUTS</span></span>

### <span data-ttu-id="5caa5-183">Microsoft. Azure. Management. Monitor. Management. Models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="5caa5-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="5caa5-184">Notizen</span><span class="sxs-lookup"><span data-stu-id="5caa5-184">NOTES</span></span>

## <span data-ttu-id="5caa5-185">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5caa5-185">RELATED LINKS</span></span>

[<span data-ttu-id="5caa5-186">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5caa5-186">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="5caa5-187">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="5caa5-187">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="5caa5-188">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5caa5-188">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="5caa5-189">Neu – AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="5caa5-189">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="5caa5-190">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5caa5-190">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


