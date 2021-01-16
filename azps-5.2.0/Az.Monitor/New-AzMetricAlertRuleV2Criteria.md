---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 0158f274ea485262b05fa1a336a2ce071fc64930
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293549"
---
# <span data-ttu-id="85cf5-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="85cf5-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="85cf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85cf5-102">SYNOPSIS</span></span>
<span data-ttu-id="85cf5-103">Erstellt ein Lokales Kriterienobjekt, das zum Erstellen einer neuen metrischen Warnung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="85cf5-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="85cf5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85cf5-104">SYNTAX</span></span>

### <span data-ttu-id="85cf5-105">StaticThresholdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="85cf5-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> -Threshold <Double> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85cf5-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85cf5-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> [-ThresholdSensitivity <String>] [-ViolationCount <Int32>]
 [-ExaminedAggregatedPointCount <Int32>] [-IgnoreDataBefore <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85cf5-107">WebtestParameterSet</span><span class="sxs-lookup"><span data-stu-id="85cf5-107">WebtestParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-WebTest] -WebTestId <String> -ApplicationInsightsId <String>
 [-FailedLocationCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85cf5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85cf5-108">DESCRIPTION</span></span>
<span data-ttu-id="85cf5-109">Das Cmdlet **"New-AzMetricAlertRuleV2Criteria"** erstellt ein Objekt für lokale metrische Kriterien, das als Eingabe-Add-AzMetricAlertRuleV2-Cmdlet verwendet wird, das eine neue metrische Warnungsregel erstellt. [](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2)</span><span class="sxs-lookup"><span data-stu-id="85cf5-109">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2) cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="85cf5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="85cf5-110">EXAMPLES</span></span>

### <span data-ttu-id="85cf5-111">Beispiel 1: Erstellen eines einfachen metrischen Warnungskriterien</span><span class="sxs-lookup"><span data-stu-id="85cf5-111">Example 1: Create a simple metric alert criteria</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 5
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="85cf5-112">Mit diesem Befehl wird ein einfaches metrisches Warnungskriterium erstellt, das in einer metrischen Warnungsregel verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="85cf5-112">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="85cf5-113">Beispiel 2: Erstellen eines dynamischen metrischen Warnungskriterien</span><span class="sxs-lookup"><span data-stu-id="85cf5-113">Example 2: Create a dynamic metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -Dynamic -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -ThresholdSensitivity Medium -ViolationCount 2 -ExaminedAggregatedPointCount 4
CriterionType        : DynamicThresholdCriterion
OperatorProperty     : GreaterThan
AlertSensitivity     : Medium
FailingPeriods       : Microsoft.Azure.Management.Monitor.Models.DynamicThresholdFailingPeriods
IgnoreDataBefore     :
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="85cf5-114">Dieser Befehl erstellt ein Kriterium für dynamische metrische Warnungen, das in einer metrischen Warnungsregel verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="85cf5-114">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="85cf5-115">Beispiel 3: Erstellen komplexerer metrischer Warnungskriterien</span><span class="sxs-lookup"><span data-stu-id="85cf5-115">Example 3: Create a more complex metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 2
AdditionalProperties :
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
TimeAggregation      : Average
Dimensions           : {availabilityResult/name}
```

<span data-ttu-id="85cf5-116">Diese Gruppe von Befehlen erstellt ein komplexeres metrisches Warnungskriterium, das die Dimensionsauswahl umfasst.</span><span class="sxs-lookup"><span data-stu-id="85cf5-116">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

### <span data-ttu-id="85cf5-117">Beispiel 4: Erstellen eines Webtestverfügbarkeitskriteriens</span><span class="sxs-lookup"><span data-stu-id="85cf5-117">Example 4: Create a webtest availability criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -WebTest -WebTestId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights" -ApplicationInsightsId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights" -FailedLocationCount 3
CriterionType        : WebtestLocationAvailabilityCriterion
WebTestId            : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights
ComponentId          : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights
FailedLocationCount  : 3
AdditionalProperties :
```

<span data-ttu-id="85cf5-118">Dieser Befehl erstellt ein Webtestverfügbarkeitskriterien, das in einer metrischen Warnungsregel verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="85cf5-118">This command creates a webtest availability criteria that can be used in a metric alert rule</span></span>

## <span data-ttu-id="85cf5-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85cf5-119">PARAMETERS</span></span>

### <span data-ttu-id="85cf5-120">-ApplicationInsightsId</span><span class="sxs-lookup"><span data-stu-id="85cf5-120">-ApplicationInsightsId</span></span>
<span data-ttu-id="85cf5-121">Die Ressourcen-ID von Application Insights.</span><span class="sxs-lookup"><span data-stu-id="85cf5-121">The Application Insights resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases: componentId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85cf5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85cf5-122">-DefaultProfile</span></span>
<span data-ttu-id="85cf5-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85cf5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85cf5-124">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="85cf5-124">-DimensionSelection</span></span>
<span data-ttu-id="85cf5-125">Liste der Dimensionsbedingungen</span><span class="sxs-lookup"><span data-stu-id="85cf5-125">List of dimension conditions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85cf5-126">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="85cf5-126">-DynamicThreshold</span></span>
<span data-ttu-id="85cf5-127">Parameter für die Verwendung des dynamischen Schwellenwerttyps wechseln</span><span class="sxs-lookup"><span data-stu-id="85cf5-127">Switch parameter for using Dynamic Threshold Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85cf5-128">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="85cf5-128">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="85cf5-129">Die Gesamtzahl der überprüften Punkte</span><span class="sxs-lookup"><span data-stu-id="85cf5-129">The Total number of examined points</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: TotalPeriod, NumberOfExaminedAggregatedPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85cf5-130">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="85cf5-130">-FailedLocationCount</span></span>
<span data-ttu-id="85cf5-131">Die minimale Anzahl fehlgeschlagener Speicherorte zum Ausstellen einer Warnung.</span><span class="sxs-lookup"><span data-stu-id="85cf5-131">The minimum number of failed locations to raise an alert.</span></span>

```yaml
Type: System.Int32
Parameter Sets: WebtestParameterSet
Aliases: AlertLocationThreshold

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85cf5-132">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="85cf5-132">-IgnoreDataBefore</span></span>
<span data-ttu-id="85cf5-133">Der Parameter IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="85cf5-133">The IgnoreDataBefore parameter</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85cf5-134">-MetricName</span><span class="sxs-lookup"><span data-stu-id="85cf5-134">-MetricName</span></span>
<span data-ttu-id="85cf5-135">Der metrische Name für die Regel</span><span class="sxs-lookup"><span data-stu-id="85cf5-135">The metric name for rule</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85cf5-136">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="85cf5-136">-MetricNamespace</span></span>
<span data-ttu-id="85cf5-137">Der Namespace der Metrik</span><span class="sxs-lookup"><span data-stu-id="85cf5-137">The Namespace of the metric</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85cf5-138">-Operator</span><span class="sxs-lookup"><span data-stu-id="85cf5-138">-Operator</span></span>
<span data-ttu-id="85cf5-139">Regelbedingungsoperator</span><span class="sxs-lookup"><span data-stu-id="85cf5-139">The rule condition operator</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85cf5-140">-SkipMetricValidation</span><span class="sxs-lookup"><span data-stu-id="85cf5-140">-SkipMetricValidation</span></span>
<span data-ttu-id="85cf5-141">Ermöglicht das Erstellen einer Warnungsregel für eine benutzerdefinierte Metrik, die noch nicht angegeben ist, indem die Metriküberprüfung übersprungen wird.</span><span class="sxs-lookup"><span data-stu-id="85cf5-141">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85cf5-142">-Threshold</span><span class="sxs-lookup"><span data-stu-id="85cf5-142">-Threshold</span></span>
<span data-ttu-id="85cf5-143">Der Schwellenwert für die Regelbedingung</span><span class="sxs-lookup"><span data-stu-id="85cf5-143">The threshold for rule condition</span></span>

```yaml
Type: System.Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85cf5-144">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="85cf5-144">-ThresholdSensitivity</span></span>
<span data-ttu-id="85cf5-145">Die Empfindlichkeit für Regelbedingung</span><span class="sxs-lookup"><span data-stu-id="85cf5-145">The sensitivity for rule condition</span></span>

```yaml
Type: System.String
Parameter Sets: DynamicThresholdParameterSet
Aliases: Sensitivity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85cf5-146">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="85cf5-146">-TimeAggregation</span></span>
<span data-ttu-id="85cf5-147">Der Aggregationsvorgang, der zum Rollup mehrerer metrischer Werte im Fensterintervall verwendet wird</span><span class="sxs-lookup"><span data-stu-id="85cf5-147">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85cf5-148">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="85cf5-148">-ViolationCount</span></span>
<span data-ttu-id="85cf5-149">Die minimale Anzahl von Verletzungen, die innerhalb des ausgewählten Zeitfensters für die Nachschlagezeit erforderlich sind, um eine Warnung aus-</span><span class="sxs-lookup"><span data-stu-id="85cf5-149">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: FailingPeriod, NumberOfViolations

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85cf5-150">-WebTest</span><span class="sxs-lookup"><span data-stu-id="85cf5-150">-WebTest</span></span>
<span data-ttu-id="85cf5-151">Parameter für die Verwendung des Verfügbarkeitskriterientyps wechseln</span><span class="sxs-lookup"><span data-stu-id="85cf5-151">Switch parameter for using availability criteria Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebtestParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85cf5-152">-WebTestId</span><span class="sxs-lookup"><span data-stu-id="85cf5-152">-WebTestId</span></span>
<span data-ttu-id="85cf5-153">Die Webtest-ID von Application Insights.</span><span class="sxs-lookup"><span data-stu-id="85cf5-153">The Application Insights web test Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85cf5-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85cf5-154">CommonParameters</span></span>
<span data-ttu-id="85cf5-155">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85cf5-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85cf5-156">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85cf5-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85cf5-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="85cf5-157">INPUTS</span></span>

### <span data-ttu-id="85cf5-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span><span class="sxs-lookup"><span data-stu-id="85cf5-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="85cf5-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="85cf5-159">OUTPUTS</span></span>

### <span data-ttu-id="85cf5-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="85cf5-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="85cf5-161">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="85cf5-161">NOTES</span></span>

## <span data-ttu-id="85cf5-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="85cf5-162">RELATED LINKS</span></span>
