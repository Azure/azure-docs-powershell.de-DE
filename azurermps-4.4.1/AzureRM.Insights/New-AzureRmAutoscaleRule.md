---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
ms.openlocfilehash: e6f157e199dedf6a7587f607cdd275183ec67c78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504145"
---
# <span data-ttu-id="29255-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="29255-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="29255-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29255-102">SYNOPSIS</span></span>
<span data-ttu-id="29255-103">Erstellt eine AutoScale-Regel.</span><span class="sxs-lookup"><span data-stu-id="29255-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29255-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29255-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29255-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29255-105">DESCRIPTION</span></span>
<span data-ttu-id="29255-106">Das Cmdlet **New-AzureRmAutoscaleRule** erstellt eine AutoScale-Regel.</span><span class="sxs-lookup"><span data-stu-id="29255-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="29255-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29255-107">EXAMPLES</span></span>

### <span data-ttu-id="29255-108">Beispiel 1: Erstellen einer Regel</span><span class="sxs-lookup"><span data-stu-id="29255-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="29255-109">Mit diesem Befehl wird eine Regel erstellt.</span><span class="sxs-lookup"><span data-stu-id="29255-109">This command creates a rule.</span></span>

### <span data-ttu-id="29255-110">Beispiel 2: Erstellen von zwei Regeln</span><span class="sxs-lookup"><span data-stu-id="29255-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="29255-111">Der erste Befehl erstellt eine Regel für die Anforderungs Metrik und speichert Sie dann in der $Rule 1-Variablen.</span><span class="sxs-lookup"><span data-stu-id="29255-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>

<span data-ttu-id="29255-112">Der zweite Befehl erstellt eine zweite Regel für die Anforderungs Metrik und speichert Sie dann in der Variablen $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="29255-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="29255-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="29255-113">PARAMETERS</span></span>

### <span data-ttu-id="29255-114">-Metricname</span><span class="sxs-lookup"><span data-stu-id="29255-114">-MetricName</span></span>
<span data-ttu-id="29255-115">Gibt den Namen der Metrik an.</span><span class="sxs-lookup"><span data-stu-id="29255-115">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="29255-116">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="29255-116">-MetricResourceId</span></span>
<span data-ttu-id="29255-117">Gibt die metrische Ressourcen-ID an.</span><span class="sxs-lookup"><span data-stu-id="29255-117">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="29255-118">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="29255-118">-MetricStatistic</span></span>
<span data-ttu-id="29255-119">Gibt die metrische Statistik an.</span><span class="sxs-lookup"><span data-stu-id="29255-119">Specifies the metric statistic.</span></span>
<span data-ttu-id="29255-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="29255-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29255-121">Mittelwert</span><span class="sxs-lookup"><span data-stu-id="29255-121">Average</span></span>
- <span data-ttu-id="29255-122">Min</span><span class="sxs-lookup"><span data-stu-id="29255-122">Min</span></span>
- <span data-ttu-id="29255-123">Max</span><span class="sxs-lookup"><span data-stu-id="29255-123">Max</span></span>
- <span data-ttu-id="29255-124">Summe</span><span class="sxs-lookup"><span data-stu-id="29255-124">Sum</span></span>

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

### <span data-ttu-id="29255-125">-Operator</span><span class="sxs-lookup"><span data-stu-id="29255-125">-Operator</span></span>
<span data-ttu-id="29255-126">Gibt den Operator an.</span><span class="sxs-lookup"><span data-stu-id="29255-126">Specifies the operator.</span></span>
<span data-ttu-id="29255-127">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="29255-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29255-128">Gleich</span><span class="sxs-lookup"><span data-stu-id="29255-128">Equals</span></span>
- <span data-ttu-id="29255-129">NotEquals</span><span class="sxs-lookup"><span data-stu-id="29255-129">NotEquals</span></span>
- <span data-ttu-id="29255-130">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="29255-130">GreaterThan</span></span>
- <span data-ttu-id="29255-131">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="29255-131">GreaterThanOrEqual</span></span>
- <span data-ttu-id="29255-132">LessThan</span><span class="sxs-lookup"><span data-stu-id="29255-132">LessThan</span></span>
- <span data-ttu-id="29255-133">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="29255-133">LessThanOrEqual</span></span>

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

### <span data-ttu-id="29255-134">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="29255-134">-ScaleActionCooldown</span></span>
<span data-ttu-id="29255-135">Gibt die Abklingzeit der autoskala-Aktion an.</span><span class="sxs-lookup"><span data-stu-id="29255-135">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="29255-136">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="29255-136">-ScaleActionDirection</span></span>
<span data-ttu-id="29255-137">Gibt die Richtung der skalierungsaktion an.</span><span class="sxs-lookup"><span data-stu-id="29255-137">Specifies the scale action direction.</span></span>
<span data-ttu-id="29255-138">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="29255-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29255-139">Keine</span><span class="sxs-lookup"><span data-stu-id="29255-139">None</span></span>
- <span data-ttu-id="29255-140">Vergrößern</span><span class="sxs-lookup"><span data-stu-id="29255-140">Increase</span></span>
- <span data-ttu-id="29255-141">Verkleinern</span><span class="sxs-lookup"><span data-stu-id="29255-141">Decrease</span></span>

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

### <span data-ttu-id="29255-142">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="29255-142">-ScaleActionScaleType</span></span>
<span data-ttu-id="29255-143">Gibt den Skalierungs an.</span><span class="sxs-lookup"><span data-stu-id="29255-143">Specifies the scale type.</span></span>
<span data-ttu-id="29255-144">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="29255-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29255-145">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="29255-145">ChangeSize</span></span>
- <span data-ttu-id="29255-146">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="29255-146">ChangeCount</span></span>
- <span data-ttu-id="29255-147">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="29255-147">PercentChangeCount</span></span>
- <span data-ttu-id="29255-148">ExactCount</span><span class="sxs-lookup"><span data-stu-id="29255-148">ExactCount</span></span>

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

### <span data-ttu-id="29255-149">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="29255-149">-ScaleActionValue</span></span>
<span data-ttu-id="29255-150">Gibt den Wert der Aktion an.</span><span class="sxs-lookup"><span data-stu-id="29255-150">Specifies the action value.</span></span>

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

### <span data-ttu-id="29255-151">-Threshold</span><span class="sxs-lookup"><span data-stu-id="29255-151">-Threshold</span></span>
<span data-ttu-id="29255-152">Gibt den Schwellenwert für den Metrikwert an.</span><span class="sxs-lookup"><span data-stu-id="29255-152">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="29255-153">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="29255-153">-TimeAggregationOperator</span></span>
<span data-ttu-id="29255-154">Gibt den Zeit Aggregations Operator an.</span><span class="sxs-lookup"><span data-stu-id="29255-154">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="29255-155">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="29255-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29255-156">Mittelwert</span><span class="sxs-lookup"><span data-stu-id="29255-156">Average</span></span>
- <span data-ttu-id="29255-157">Mindestens</span><span class="sxs-lookup"><span data-stu-id="29255-157">Minimum</span></span>
- <span data-ttu-id="29255-158">Maximale</span><span class="sxs-lookup"><span data-stu-id="29255-158">Maximum</span></span>
- <span data-ttu-id="29255-159">Letzten</span><span class="sxs-lookup"><span data-stu-id="29255-159">Last</span></span>
- <span data-ttu-id="29255-160">Summe, Anzahl</span><span class="sxs-lookup"><span data-stu-id="29255-160">Total, Count</span></span>

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

### <span data-ttu-id="29255-161">-Zeitkorn</span><span class="sxs-lookup"><span data-stu-id="29255-161">-TimeGrain</span></span>
<span data-ttu-id="29255-162">Gibt das Zeit Korn an.</span><span class="sxs-lookup"><span data-stu-id="29255-162">Specifies the time grain.</span></span>

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

### <span data-ttu-id="29255-163">-Fenster</span><span class="sxs-lookup"><span data-stu-id="29255-163">-TimeWindow</span></span>
<span data-ttu-id="29255-164">Gibt das Zeitfenster an.</span><span class="sxs-lookup"><span data-stu-id="29255-164">Specifies the time window.</span></span>

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

### <span data-ttu-id="29255-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29255-165">-DefaultProfile</span></span>
<span data-ttu-id="29255-166">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="29255-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29255-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29255-167">CommonParameters</span></span>
<span data-ttu-id="29255-168">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29255-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29255-169">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29255-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29255-170">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29255-170">INPUTS</span></span>

## <span data-ttu-id="29255-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29255-171">OUTPUTS</span></span>

### <span data-ttu-id="29255-172">Microsoft. Azure. Management. Monitor. Management. Models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="29255-172">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="29255-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="29255-173">NOTES</span></span>

## <span data-ttu-id="29255-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29255-174">RELATED LINKS</span></span>

[<span data-ttu-id="29255-175">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="29255-175">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="29255-176">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="29255-176">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="29255-177">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="29255-177">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="29255-178">Neu – AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="29255-178">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="29255-179">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="29255-179">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


