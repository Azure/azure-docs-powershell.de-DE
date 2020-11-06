---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
ms.openlocfilehash: 5addf4bae7024d86b6a517a40a4033992047fe08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497450"
---
# <span data-ttu-id="71a88-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="71a88-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="71a88-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71a88-102">SYNOPSIS</span></span>
<span data-ttu-id="71a88-103">Erstellt eine AutoScale-Regel.</span><span class="sxs-lookup"><span data-stu-id="71a88-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71a88-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71a88-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71a88-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71a88-105">DESCRIPTION</span></span>
<span data-ttu-id="71a88-106">Das Cmdlet **New-AzureRmAutoscaleRule** erstellt eine AutoScale-Regel.</span><span class="sxs-lookup"><span data-stu-id="71a88-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="71a88-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71a88-107">EXAMPLES</span></span>

### <span data-ttu-id="71a88-108">Beispiel 1: Erstellen einer Regel</span><span class="sxs-lookup"><span data-stu-id="71a88-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="71a88-109">Mit diesem Befehl wird eine Regel erstellt.</span><span class="sxs-lookup"><span data-stu-id="71a88-109">This command creates a rule.</span></span>

### <span data-ttu-id="71a88-110">Beispiel 2: Erstellen von zwei Regeln</span><span class="sxs-lookup"><span data-stu-id="71a88-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="71a88-111">Der erste Befehl erstellt eine Regel für die Anforderungs Metrik und speichert Sie dann in der $Rule 1-Variablen.</span><span class="sxs-lookup"><span data-stu-id="71a88-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="71a88-112">Der zweite Befehl erstellt eine zweite Regel für die Anforderungs Metrik und speichert Sie dann in der Variablen $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="71a88-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="71a88-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="71a88-113">PARAMETERS</span></span>

### <span data-ttu-id="71a88-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71a88-114">-DefaultProfile</span></span>
<span data-ttu-id="71a88-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="71a88-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71a88-116">-Metricname</span><span class="sxs-lookup"><span data-stu-id="71a88-116">-MetricName</span></span>
<span data-ttu-id="71a88-117">Gibt den Namen der Metrik an.</span><span class="sxs-lookup"><span data-stu-id="71a88-117">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="71a88-118">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="71a88-118">-MetricResourceId</span></span>
<span data-ttu-id="71a88-119">Gibt die metrische Ressourcen-ID an.</span><span class="sxs-lookup"><span data-stu-id="71a88-119">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="71a88-120">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="71a88-120">-MetricStatistic</span></span>
<span data-ttu-id="71a88-121">Gibt die metrische Statistik an.</span><span class="sxs-lookup"><span data-stu-id="71a88-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="71a88-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="71a88-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="71a88-123">Mittelwert</span><span class="sxs-lookup"><span data-stu-id="71a88-123">Average</span></span>
- <span data-ttu-id="71a88-124">Min</span><span class="sxs-lookup"><span data-stu-id="71a88-124">Min</span></span>
- <span data-ttu-id="71a88-125">Max</span><span class="sxs-lookup"><span data-stu-id="71a88-125">Max</span></span>
- <span data-ttu-id="71a88-126">Summe</span><span class="sxs-lookup"><span data-stu-id="71a88-126">Sum</span></span>

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

### <span data-ttu-id="71a88-127">-Operator</span><span class="sxs-lookup"><span data-stu-id="71a88-127">-Operator</span></span>
<span data-ttu-id="71a88-128">Gibt den Operator an.</span><span class="sxs-lookup"><span data-stu-id="71a88-128">Specifies the operator.</span></span>
<span data-ttu-id="71a88-129">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="71a88-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="71a88-130">Gleich</span><span class="sxs-lookup"><span data-stu-id="71a88-130">Equals</span></span>
- <span data-ttu-id="71a88-131">NotEquals</span><span class="sxs-lookup"><span data-stu-id="71a88-131">NotEquals</span></span>
- <span data-ttu-id="71a88-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="71a88-132">GreaterThan</span></span>
- <span data-ttu-id="71a88-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="71a88-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="71a88-134">LessThan</span><span class="sxs-lookup"><span data-stu-id="71a88-134">LessThan</span></span>
- <span data-ttu-id="71a88-135">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="71a88-135">LessThanOrEqual</span></span>

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

### <span data-ttu-id="71a88-136">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="71a88-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="71a88-137">Gibt die Abklingzeit der autoskala-Aktion an.</span><span class="sxs-lookup"><span data-stu-id="71a88-137">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="71a88-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="71a88-138">-ScaleActionDirection</span></span>
<span data-ttu-id="71a88-139">Gibt die Richtung der skalierungsaktion an.</span><span class="sxs-lookup"><span data-stu-id="71a88-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="71a88-140">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="71a88-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="71a88-141">Keine</span><span class="sxs-lookup"><span data-stu-id="71a88-141">None</span></span>
- <span data-ttu-id="71a88-142">Vergrößern</span><span class="sxs-lookup"><span data-stu-id="71a88-142">Increase</span></span>
- <span data-ttu-id="71a88-143">Verkleinern</span><span class="sxs-lookup"><span data-stu-id="71a88-143">Decrease</span></span>

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

### <span data-ttu-id="71a88-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="71a88-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="71a88-145">Gibt den Skalierungs an.</span><span class="sxs-lookup"><span data-stu-id="71a88-145">Specifies the scale type.</span></span>
<span data-ttu-id="71a88-146">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="71a88-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="71a88-147">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="71a88-147">ChangeSize</span></span>
- <span data-ttu-id="71a88-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="71a88-148">ChangeCount</span></span>
- <span data-ttu-id="71a88-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="71a88-149">PercentChangeCount</span></span>
- <span data-ttu-id="71a88-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="71a88-150">ExactCount</span></span>

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

### <span data-ttu-id="71a88-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="71a88-151">-ScaleActionValue</span></span>
<span data-ttu-id="71a88-152">Gibt den Wert der Aktion an.</span><span class="sxs-lookup"><span data-stu-id="71a88-152">Specifies the action value.</span></span>

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

### <span data-ttu-id="71a88-153">-Threshold</span><span class="sxs-lookup"><span data-stu-id="71a88-153">-Threshold</span></span>
<span data-ttu-id="71a88-154">Gibt den Schwellenwert für den Metrikwert an.</span><span class="sxs-lookup"><span data-stu-id="71a88-154">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="71a88-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="71a88-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="71a88-156">Gibt den Zeit Aggregations Operator an.</span><span class="sxs-lookup"><span data-stu-id="71a88-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="71a88-157">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="71a88-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="71a88-158">Mittelwert</span><span class="sxs-lookup"><span data-stu-id="71a88-158">Average</span></span>
- <span data-ttu-id="71a88-159">Mindestens</span><span class="sxs-lookup"><span data-stu-id="71a88-159">Minimum</span></span>
- <span data-ttu-id="71a88-160">Maximale</span><span class="sxs-lookup"><span data-stu-id="71a88-160">Maximum</span></span>
- <span data-ttu-id="71a88-161">Letzten</span><span class="sxs-lookup"><span data-stu-id="71a88-161">Last</span></span>
- <span data-ttu-id="71a88-162">Summe, Anzahl</span><span class="sxs-lookup"><span data-stu-id="71a88-162">Total, Count</span></span>

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

### <span data-ttu-id="71a88-163">-Zeitkorn</span><span class="sxs-lookup"><span data-stu-id="71a88-163">-TimeGrain</span></span>
<span data-ttu-id="71a88-164">Gibt das Zeit Korn an.</span><span class="sxs-lookup"><span data-stu-id="71a88-164">Specifies the time grain.</span></span>

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

### <span data-ttu-id="71a88-165">-Fenster</span><span class="sxs-lookup"><span data-stu-id="71a88-165">-TimeWindow</span></span>
<span data-ttu-id="71a88-166">Gibt das Zeitfenster an.</span><span class="sxs-lookup"><span data-stu-id="71a88-166">Specifies the time window.</span></span>

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

### <span data-ttu-id="71a88-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71a88-167">CommonParameters</span></span>
<span data-ttu-id="71a88-168">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71a88-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71a88-169">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71a88-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71a88-170">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71a88-170">INPUTS</span></span>

### <span data-ttu-id="71a88-171">System. String</span><span class="sxs-lookup"><span data-stu-id="71a88-171">System.String</span></span>

### <span data-ttu-id="71a88-172">Microsoft. Azure. Management. Monitor. Management. Models. ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="71a88-172">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="71a88-173">Microsoft. Azure. Management. Monitor. Management. Models. MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="71a88-173">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="71a88-174">System. Double</span><span class="sxs-lookup"><span data-stu-id="71a88-174">System.Double</span></span>

### <span data-ttu-id="71a88-175">Microsoft. Azure. Management. Monitor. Management. Models. zeitaggregationtype</span><span class="sxs-lookup"><span data-stu-id="71a88-175">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="71a88-176">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="71a88-176">System.TimeSpan</span></span>

### <span data-ttu-id="71a88-177">Microsoft. Azure. Management. Monitor. Management. Models. ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="71a88-177">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="71a88-178">Microsoft. Azure. Management. Monitor. Management. Models. ScaleType</span><span class="sxs-lookup"><span data-stu-id="71a88-178">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="71a88-179">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71a88-179">OUTPUTS</span></span>

### <span data-ttu-id="71a88-180">Microsoft. Azure. Management. Monitor. Management. Models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="71a88-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="71a88-181">Notizen</span><span class="sxs-lookup"><span data-stu-id="71a88-181">NOTES</span></span>

## <span data-ttu-id="71a88-182">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71a88-182">RELATED LINKS</span></span>

[<span data-ttu-id="71a88-183">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="71a88-183">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="71a88-184">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="71a88-184">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="71a88-185">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="71a88-185">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="71a88-186">Neu – AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="71a88-186">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="71a88-187">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="71a88-187">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


