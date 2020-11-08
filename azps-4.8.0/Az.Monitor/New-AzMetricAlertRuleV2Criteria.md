---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 101d522c1f8ae3b44545bdb204bad01fbe21df9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174631"
---
# <span data-ttu-id="65c99-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="65c99-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="65c99-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65c99-102">SYNOPSIS</span></span>
<span data-ttu-id="65c99-103">Erstellt ein lokales Criteria-Objekt, das zum Erstellen einer neuen metrischen Warnung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="65c99-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="65c99-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65c99-104">SYNTAX</span></span>

### <span data-ttu-id="65c99-105">StaticThresholdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="65c99-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> -Threshold <Double> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65c99-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65c99-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> [-ThresholdSensitivity <String>] [-ViolationCount <Int32>]
 [-ExaminedAggregatedPointCount <Int32>] [-IgnoreDataBefore <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65c99-107">WebtestParameterSet</span><span class="sxs-lookup"><span data-stu-id="65c99-107">WebtestParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-WebTest] -WebTestId <String> -ApplicationInsightsId <String>
 [-FailedLocationCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65c99-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65c99-108">DESCRIPTION</span></span>
<span data-ttu-id="65c99-109">Das Cmdlet **New-AzMetricAlertRuleV2Criteria** erstellt ein lokales metrisches kriterienobjekt, das als Eingabe Add-AzMetricAlertRuleV2-Cmdlet verwendet werden soll, das eine neue Metrik-Warnungsregel erstellt.</span><span class="sxs-lookup"><span data-stu-id="65c99-109">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="65c99-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65c99-110">EXAMPLES</span></span>

### <span data-ttu-id="65c99-111">Beispiel 1: Erstellen einer einfachen Metrik für Warnungskriterien</span><span class="sxs-lookup"><span data-stu-id="65c99-111">Example 1: Create a simple metric alert criteria</span></span>

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

<span data-ttu-id="65c99-112">Dieser Befehl erstellt eine einfache Metrik-Warnungskriterien, die in einer Metrik-Warnungsregel verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="65c99-112">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="65c99-113">Beispiel 2: Erstellen einer dynamischen Metrik für Warnungskriterien</span><span class="sxs-lookup"><span data-stu-id="65c99-113">Example 2: Create a dynamic metric alert criteria</span></span>

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

<span data-ttu-id="65c99-114">Dieser Befehl erstellt eine Dynamic Metric-Warnungskriterien, die in einer Metrik-Warnungsregel verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="65c99-114">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="65c99-115">Beispiel 3: Erstellen komplexer Metrik-Warnungskriterien</span><span class="sxs-lookup"><span data-stu-id="65c99-115">Example 3: Create a more complex metric alert criteria</span></span>

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

<span data-ttu-id="65c99-116">Dieser Satz von Befehlen erstellt komplexere Metrik-Warnungskriterien, die die Dimensionsauswahl umfassen.</span><span class="sxs-lookup"><span data-stu-id="65c99-116">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

### <span data-ttu-id="65c99-117">Beispiel 4: Erstellen eines Webtest-Verfügbarkeits Kriteriums</span><span class="sxs-lookup"><span data-stu-id="65c99-117">Example 4: Create a webtest availability criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -WebTest -WebTestId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights" -ApplicationInsightsId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights" -FailedLocationCount 3
CriterionType        : WebtestLocationAvailabilityCriterion
WebTestId            : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights
ComponentId          : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights
FailedLocationCount  : 3
AdditionalProperties :
```

<span data-ttu-id="65c99-118">Dieser Befehl erstellt ein Webtest-Verfügbarkeits Kriterium, das in einer Metrik-Warnungsregel verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="65c99-118">This command creates a webtest availability criteria that can be used in a metric alert rule</span></span>

## <span data-ttu-id="65c99-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="65c99-119">PARAMETERS</span></span>

### <span data-ttu-id="65c99-120">-ApplicationInsightsId</span><span class="sxs-lookup"><span data-stu-id="65c99-120">-ApplicationInsightsId</span></span>
<span data-ttu-id="65c99-121">Die Ressourcen-ID für Application Insights.</span><span class="sxs-lookup"><span data-stu-id="65c99-121">The Application Insights resource Id.</span></span>

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

### <span data-ttu-id="65c99-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65c99-122">-DefaultProfile</span></span>
<span data-ttu-id="65c99-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65c99-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65c99-124">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="65c99-124">-DimensionSelection</span></span>
<span data-ttu-id="65c99-125">Liste der Dimensions Bedingungen</span><span class="sxs-lookup"><span data-stu-id="65c99-125">List of dimension conditions</span></span>

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

### <span data-ttu-id="65c99-126">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="65c99-126">-DynamicThreshold</span></span>
<span data-ttu-id="65c99-127">Schalterparameter für die Verwendung des dynamischen Schwellenwert Typs</span><span class="sxs-lookup"><span data-stu-id="65c99-127">Switch parameter for using Dynamic Threshold Type</span></span>

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

### <span data-ttu-id="65c99-128">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="65c99-128">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="65c99-129">Die Gesamtzahl der untersuchten Punkte</span><span class="sxs-lookup"><span data-stu-id="65c99-129">The Total number of examined points</span></span>

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

### <span data-ttu-id="65c99-130">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="65c99-130">-FailedLocationCount</span></span>
<span data-ttu-id="65c99-131">Die Mindestanzahl fehlgeschlagener Speicherorte, um eine Benachrichtigung auszulösen.</span><span class="sxs-lookup"><span data-stu-id="65c99-131">The minimum number of failed locations to raise an alert.</span></span>

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

### <span data-ttu-id="65c99-132">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="65c99-132">-IgnoreDataBefore</span></span>
<span data-ttu-id="65c99-133">Der IgnoreDataBefore-Parameter</span><span class="sxs-lookup"><span data-stu-id="65c99-133">The IgnoreDataBefore parameter</span></span>

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

### <span data-ttu-id="65c99-134">-Metricname</span><span class="sxs-lookup"><span data-stu-id="65c99-134">-MetricName</span></span>
<span data-ttu-id="65c99-135">Der metrische Name für Regel</span><span class="sxs-lookup"><span data-stu-id="65c99-135">The metric name for rule</span></span>

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

### <span data-ttu-id="65c99-136">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="65c99-136">-MetricNamespace</span></span>
<span data-ttu-id="65c99-137">Der Namespace der Metrik</span><span class="sxs-lookup"><span data-stu-id="65c99-137">The Namespace of the metric</span></span>

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

### <span data-ttu-id="65c99-138">-Operator</span><span class="sxs-lookup"><span data-stu-id="65c99-138">-Operator</span></span>
<span data-ttu-id="65c99-139">Der Regel Bedingungsoperator</span><span class="sxs-lookup"><span data-stu-id="65c99-139">The rule condition operator</span></span>

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

### <span data-ttu-id="65c99-140">-SkipMetricValidation</span><span class="sxs-lookup"><span data-stu-id="65c99-140">-SkipMetricValidation</span></span>
<span data-ttu-id="65c99-141">Ermöglicht das Erstellen einer Warnungsregel für eine benutzerdefinierte Metrik, die noch nicht ausgegeben wurde, indem die Metrik-Validierung übersprungen wird</span><span class="sxs-lookup"><span data-stu-id="65c99-141">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped</span></span>

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

### <span data-ttu-id="65c99-142">-Threshold</span><span class="sxs-lookup"><span data-stu-id="65c99-142">-Threshold</span></span>
<span data-ttu-id="65c99-143">Der Schwellenwert für Regelbedingung</span><span class="sxs-lookup"><span data-stu-id="65c99-143">The threshold for rule condition</span></span>

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

### <span data-ttu-id="65c99-144">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="65c99-144">-ThresholdSensitivity</span></span>
<span data-ttu-id="65c99-145">Die Vertraulichkeit für Regelbedingung</span><span class="sxs-lookup"><span data-stu-id="65c99-145">The sensitivity for rule condition</span></span>

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

### <span data-ttu-id="65c99-146">-Zeitaggregation</span><span class="sxs-lookup"><span data-stu-id="65c99-146">-TimeAggregation</span></span>
<span data-ttu-id="65c99-147">Der Aggregationsvorgang, der zum Rollup mehrerer metrischer Werte über das Fenster Intervall hinweg verwendet wird</span><span class="sxs-lookup"><span data-stu-id="65c99-147">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

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

### <span data-ttu-id="65c99-148">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="65c99-148">-ViolationCount</span></span>
<span data-ttu-id="65c99-149">Die minimale Anzahl von Verstößen, die im ausgewählten Lookback-Zeitfenster erforderlich sind, um eine Benachrichtigung auszulösen</span><span class="sxs-lookup"><span data-stu-id="65c99-149">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

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

### <span data-ttu-id="65c99-150">-Webtest</span><span class="sxs-lookup"><span data-stu-id="65c99-150">-WebTest</span></span>
<span data-ttu-id="65c99-151">Parameter für die Verwendung des Verfügbarkeitskriterien-Typs wechseln</span><span class="sxs-lookup"><span data-stu-id="65c99-151">Switch parameter for using availability criteria Type</span></span>

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

### <span data-ttu-id="65c99-152">-Webtest-Nr</span><span class="sxs-lookup"><span data-stu-id="65c99-152">-WebTestId</span></span>
<span data-ttu-id="65c99-153">Die Webtest-ID für Application Insights.</span><span class="sxs-lookup"><span data-stu-id="65c99-153">The Application Insights web test Id.</span></span>

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

### <span data-ttu-id="65c99-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65c99-154">CommonParameters</span></span>
<span data-ttu-id="65c99-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65c99-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65c99-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65c99-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65c99-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65c99-157">INPUTS</span></span>

### <span data-ttu-id="65c99-158">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="65c99-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="65c99-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65c99-159">OUTPUTS</span></span>

### <span data-ttu-id="65c99-160">Microsoft. Azure. Commands. Insights. OutputClasses. IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="65c99-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="65c99-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="65c99-161">NOTES</span></span>

## <span data-ttu-id="65c99-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65c99-162">RELATED LINKS</span></span>
