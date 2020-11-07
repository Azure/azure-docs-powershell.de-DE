---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 16687824216fa0014d59b78a96d22a4da8a19fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93818915"
---
# <span data-ttu-id="0516e-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="0516e-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="0516e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0516e-102">SYNOPSIS</span></span>
<span data-ttu-id="0516e-103">Erstellt ein lokales Criteria-Objekt, das zum Erstellen einer neuen metrischen Warnung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0516e-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="0516e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0516e-104">SYNTAX</span></span>

### <span data-ttu-id="0516e-105">StaticThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0516e-105">StaticThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0516e-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0516e-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 -DynamicThreshold <String> [-Sensitivity <String>] [-FailingPeriod <Int32>] [-TotalPeriod <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0516e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0516e-107">DESCRIPTION</span></span>
<span data-ttu-id="0516e-108">Das Cmdlet **New-AzMetricAlertRuleV2Criteria** erstellt ein lokales metrisches kriterienobjekt, das als Eingabe Add-AzMetricAlertRuleV2-Cmdlet verwendet werden soll, das eine neue Metrik-Warnungsregel erstellt.</span><span class="sxs-lookup"><span data-stu-id="0516e-108">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="0516e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0516e-109">EXAMPLES</span></span>

### <span data-ttu-id="0516e-110">Beispiel 1: Erstellen einer einfachen Metrik für Warnungskriterien</span><span class="sxs-lookup"><span data-stu-id="0516e-110">Example 1: Create a simple metric alert criteria</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 5
Dimensions           :
AdditionalProperties :
```

<span data-ttu-id="0516e-111">Dieser Befehl erstellt eine einfache Metrik-Warnungskriterien, die in einer Metrik-Warnungsregel verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="0516e-111">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="0516e-112">Beispiel 2: Erstellen komplexer Metrik-Warnungskriterien</span><span class="sxs-lookup"><span data-stu-id="0516e-112">Example 2: Create a more complex metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 2
Dimensions           : {availabilityResult/name}
AdditionalProperties :
```

<span data-ttu-id="0516e-113">Dieser Satz von Befehlen erstellt komplexere Metrik-Warnungskriterien, die die Dimensionsauswahl umfassen.</span><span class="sxs-lookup"><span data-stu-id="0516e-113">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

## <span data-ttu-id="0516e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0516e-114">PARAMETERS</span></span>

### <span data-ttu-id="0516e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0516e-115">-DefaultProfile</span></span>
<span data-ttu-id="0516e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0516e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0516e-117">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="0516e-117">-DimensionSelection</span></span>
<span data-ttu-id="0516e-118">Liste der Dimensions Bedingungen</span><span class="sxs-lookup"><span data-stu-id="0516e-118">List of dimension conditions</span></span>

```yaml
Type: PSMetricDimension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0516e-119">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="0516e-119">-DynamicThreshold</span></span>
<span data-ttu-id="0516e-120">Der dynamische Schwellenwert für Regelbedingung</span><span class="sxs-lookup"><span data-stu-id="0516e-120">The Dynamic Threshold for rule condition</span></span>

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0516e-121">-FailingPeriod</span><span class="sxs-lookup"><span data-stu-id="0516e-121">-FailingPeriod</span></span>
<span data-ttu-id="0516e-122">Der fehlerhafte Zeitraum für Regelbedingung</span><span class="sxs-lookup"><span data-stu-id="0516e-122">The Failing Period for rule condition</span></span>

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0516e-123">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="0516e-123">-IgnoreDataBefore</span></span>
<span data-ttu-id="0516e-124">Der IgnoreDataBefore-Parameter</span><span class="sxs-lookup"><span data-stu-id="0516e-124">The IgnoreDataBefore parameter</span></span>

```yaml
Type: DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0516e-125">-Metricname</span><span class="sxs-lookup"><span data-stu-id="0516e-125">-MetricName</span></span>
<span data-ttu-id="0516e-126">Der metrische Name für Regel</span><span class="sxs-lookup"><span data-stu-id="0516e-126">The metric name for rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0516e-127">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="0516e-127">-MetricNamespace</span></span>
<span data-ttu-id="0516e-128">Der Namespace der Metrik</span><span class="sxs-lookup"><span data-stu-id="0516e-128">The Namespace of the metric</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0516e-129">-Operator</span><span class="sxs-lookup"><span data-stu-id="0516e-129">-Operator</span></span>
<span data-ttu-id="0516e-130">Der Regel Bedingungsoperator</span><span class="sxs-lookup"><span data-stu-id="0516e-130">The rule condition operator</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0516e-131">-Empfindlichkeit</span><span class="sxs-lookup"><span data-stu-id="0516e-131">-Sensitivity</span></span>
<span data-ttu-id="0516e-132">Die Vertraulichkeit für Regelbedingung</span><span class="sxs-lookup"><span data-stu-id="0516e-132">The sensitivity for rule condition</span></span>

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0516e-133">-Threshold</span><span class="sxs-lookup"><span data-stu-id="0516e-133">-Threshold</span></span>
<span data-ttu-id="0516e-134">Der Schwellenwert für Regelbedingung</span><span class="sxs-lookup"><span data-stu-id="0516e-134">The threshold for rule condition</span></span>

```yaml
Type: Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0516e-135">-Zeitaggregation</span><span class="sxs-lookup"><span data-stu-id="0516e-135">-TimeAggregation</span></span>
<span data-ttu-id="0516e-136">Der Aggregationsvorgang, der zum Rollup mehrerer metrischer Werte über das Fenster Intervall hinweg verwendet wird</span><span class="sxs-lookup"><span data-stu-id="0516e-136">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0516e-137">-TotalPeriod</span><span class="sxs-lookup"><span data-stu-id="0516e-137">-TotalPeriod</span></span>
<span data-ttu-id="0516e-138">Der Gesamtzeitraum für Regelbedingung</span><span class="sxs-lookup"><span data-stu-id="0516e-138">The Total Period for rule condition</span></span>

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0516e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0516e-139">CommonParameters</span></span>
<span data-ttu-id="0516e-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0516e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0516e-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0516e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0516e-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0516e-142">INPUTS</span></span>

### <span data-ttu-id="0516e-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="0516e-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="0516e-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0516e-144">OUTPUTS</span></span>

### <span data-ttu-id="0516e-145">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="0516e-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria</span></span>

## <span data-ttu-id="0516e-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="0516e-146">NOTES</span></span>

## <span data-ttu-id="0516e-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0516e-147">RELATED LINKS</span></span>
