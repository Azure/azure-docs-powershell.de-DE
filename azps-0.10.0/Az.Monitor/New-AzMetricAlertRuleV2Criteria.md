---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: bb72a50c2db43a8db053d273c601ca51e96402f0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841975"
---
# <span data-ttu-id="85fcd-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="85fcd-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="85fcd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="85fcd-102">SYNOPSIS</span></span>
<span data-ttu-id="85fcd-103">Erstellt ein lokales Criteria-Objekt, das zum Erstellen einer neuen metrischen Warnung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="85fcd-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="85fcd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="85fcd-104">SYNTAX</span></span>

### <span data-ttu-id="85fcd-105">StaticThresholdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="85fcd-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85fcd-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85fcd-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 [-ThresholdSensitivity <String>] [-ViolationCount <Int32>] [-ExaminedAggregatedPointCount <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85fcd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85fcd-107">DESCRIPTION</span></span>
<span data-ttu-id="85fcd-108">Das Cmdlet **New-AzMetricAlertRuleV2Criteria** erstellt ein lokales metrisches kriterienobjekt, das als Eingabe Add-AzMetricAlertRuleV2-Cmdlet verwendet werden soll, das eine neue Metrik-Warnungsregel erstellt.</span><span class="sxs-lookup"><span data-stu-id="85fcd-108">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="85fcd-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85fcd-109">EXAMPLES</span></span>

### <span data-ttu-id="85fcd-110">Beispiel 1: Erstellen einer einfachen Metrik für Warnungskriterien</span><span class="sxs-lookup"><span data-stu-id="85fcd-110">Example 1: Create a simple metric alert criteria</span></span>

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

<span data-ttu-id="85fcd-111">Dieser Befehl erstellt eine einfache Metrik-Warnungskriterien, die in einer Metrik-Warnungsregel verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="85fcd-111">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="85fcd-112">Beispiel 2: Erstellen einer dynamischen Metrik für Warnungskriterien</span><span class="sxs-lookup"><span data-stu-id="85fcd-112">Example 2: Create a dynamic metric alert criteria</span></span>

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

<span data-ttu-id="85fcd-113">Dieser Befehl erstellt eine Dynamic Metric-Warnungskriterien, die in einer Metrik-Warnungsregel verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="85fcd-113">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="85fcd-114">Beispiel 3: Erstellen komplexer Metrik-Warnungskriterien</span><span class="sxs-lookup"><span data-stu-id="85fcd-114">Example 3: Create a more complex metric alert criteria</span></span>

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

<span data-ttu-id="85fcd-115">Dieser Satz von Befehlen erstellt komplexere Metrik-Warnungskriterien, die die Dimensionsauswahl umfassen.</span><span class="sxs-lookup"><span data-stu-id="85fcd-115">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

## <span data-ttu-id="85fcd-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="85fcd-116">PARAMETERS</span></span>

### <span data-ttu-id="85fcd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85fcd-117">-DefaultProfile</span></span>
<span data-ttu-id="85fcd-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="85fcd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85fcd-119">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="85fcd-119">-DimensionSelection</span></span>
<span data-ttu-id="85fcd-120">Liste der Dimensions Bedingungen</span><span class="sxs-lookup"><span data-stu-id="85fcd-120">List of dimension conditions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85fcd-121">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="85fcd-121">-DynamicThreshold</span></span>
<span data-ttu-id="85fcd-122">Schalterparameter für die Verwendung des dynamischen Schwellenwert Typs</span><span class="sxs-lookup"><span data-stu-id="85fcd-122">Switch parameter for using Dynamic Threshold Type</span></span>

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

### <span data-ttu-id="85fcd-123">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="85fcd-123">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="85fcd-124">Die Gesamtzahl der untersuchten Punkte</span><span class="sxs-lookup"><span data-stu-id="85fcd-124">The Total number of examined points</span></span>

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

### <span data-ttu-id="85fcd-125">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="85fcd-125">-IgnoreDataBefore</span></span>
<span data-ttu-id="85fcd-126">Der IgnoreDataBefore-Parameter</span><span class="sxs-lookup"><span data-stu-id="85fcd-126">The IgnoreDataBefore parameter</span></span>

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

### <span data-ttu-id="85fcd-127">-Metricname</span><span class="sxs-lookup"><span data-stu-id="85fcd-127">-MetricName</span></span>
<span data-ttu-id="85fcd-128">Der metrische Name für Regel</span><span class="sxs-lookup"><span data-stu-id="85fcd-128">The metric name for rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85fcd-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="85fcd-129">-MetricNamespace</span></span>
<span data-ttu-id="85fcd-130">Der Namespace der Metrik</span><span class="sxs-lookup"><span data-stu-id="85fcd-130">The Namespace of the metric</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85fcd-131">-Operator</span><span class="sxs-lookup"><span data-stu-id="85fcd-131">-Operator</span></span>
<span data-ttu-id="85fcd-132">Der Regel Bedingungsoperator</span><span class="sxs-lookup"><span data-stu-id="85fcd-132">The rule condition operator</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85fcd-133">-Threshold</span><span class="sxs-lookup"><span data-stu-id="85fcd-133">-Threshold</span></span>
<span data-ttu-id="85fcd-134">Der Schwellenwert für Regelbedingung</span><span class="sxs-lookup"><span data-stu-id="85fcd-134">The threshold for rule condition</span></span>

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

### <span data-ttu-id="85fcd-135">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="85fcd-135">-ThresholdSensitivity</span></span>
<span data-ttu-id="85fcd-136">Die Vertraulichkeit für Regelbedingung</span><span class="sxs-lookup"><span data-stu-id="85fcd-136">The sensitivity for rule condition</span></span>

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

### <span data-ttu-id="85fcd-137">-Zeitaggregation</span><span class="sxs-lookup"><span data-stu-id="85fcd-137">-TimeAggregation</span></span>
<span data-ttu-id="85fcd-138">Der Aggregationsvorgang, der zum Rollup mehrerer metrischer Werte über das Fenster Intervall hinweg verwendet wird</span><span class="sxs-lookup"><span data-stu-id="85fcd-138">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85fcd-139">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="85fcd-139">-ViolationCount</span></span>
<span data-ttu-id="85fcd-140">Die minimale Anzahl von Verstößen, die im ausgewählten Lookback-Zeitfenster erforderlich sind, um eine Benachrichtigung auszulösen</span><span class="sxs-lookup"><span data-stu-id="85fcd-140">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

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

### <span data-ttu-id="85fcd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85fcd-141">CommonParameters</span></span>
<span data-ttu-id="85fcd-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85fcd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85fcd-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85fcd-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85fcd-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="85fcd-144">INPUTS</span></span>

### <span data-ttu-id="85fcd-145">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="85fcd-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="85fcd-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="85fcd-146">OUTPUTS</span></span>

### <span data-ttu-id="85fcd-147">Microsoft. Azure. Commands. Insights. OutputClasses. IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="85fcd-147">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="85fcd-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="85fcd-148">NOTES</span></span>

## <span data-ttu-id="85fcd-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="85fcd-149">RELATED LINKS</span></span>
