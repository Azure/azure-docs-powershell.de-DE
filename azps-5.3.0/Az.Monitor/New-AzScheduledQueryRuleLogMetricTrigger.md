---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c4d44f266a9966f605e009cc4ce5dece0fa5e2ae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467563"
---
# <span data-ttu-id="fd888-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="fd888-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="fd888-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd888-102">SYNOPSIS</span></span>
<span data-ttu-id="fd888-103">Erstellt ein Objekt vom Typ "Protokollmetrischer Trigger".</span><span class="sxs-lookup"><span data-stu-id="fd888-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="fd888-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd888-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd888-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd888-105">DESCRIPTION</span></span>
<span data-ttu-id="fd888-106">Erstellt ein Objekt vom Typ "Protokollmetrischer Trigger" und ist optional.</span><span class="sxs-lookup"><span data-stu-id="fd888-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="fd888-107">Dies ist die Auslösebedingung für die metrische Abfrageregel, die verwendet wird, wenn Sie den Typ der warnungsmetrischen Messung zustandsmetrisch eingeben müssen.</span><span class="sxs-lookup"><span data-stu-id="fd888-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="fd888-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fd888-108">EXAMPLES</span></span>

### <span data-ttu-id="fd888-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fd888-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="fd888-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd888-110">PARAMETERS</span></span>

### <span data-ttu-id="fd888-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd888-111">-DefaultProfile</span></span>
<span data-ttu-id="fd888-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd888-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd888-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="fd888-113">-MetricColumn</span></span>
<span data-ttu-id="fd888-114">Spalte, in der der metrische Wert aggregiert wird.</span><span class="sxs-lookup"><span data-stu-id="fd888-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="fd888-115">Die Eingabe wird nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="fd888-115">The input is not validated.</span></span> <span data-ttu-id="fd888-116">Es wird zuerst überprüft, wenn New-AzScheduledQueryRule schließlich aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fd888-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="fd888-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="fd888-117">-MetricTriggerType</span></span>
<span data-ttu-id="fd888-118">Der metrische Triggertyp.</span><span class="sxs-lookup"><span data-stu-id="fd888-118">The metric trigger type.</span></span>
<span data-ttu-id="fd888-119">Die Eingabe wird nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="fd888-119">The input is not validated.</span></span> <span data-ttu-id="fd888-120">Es wird zuerst überprüft, wenn New-AzScheduledQueryRule schließlich aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fd888-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="fd888-121">-Threshold</span><span class="sxs-lookup"><span data-stu-id="fd888-121">-Threshold</span></span>
<span data-ttu-id="fd888-122">Der Schwellenwert für die Metrik: "Aufeinanderfolgender Schwellenwert", "Summe".</span><span class="sxs-lookup"><span data-stu-id="fd888-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="fd888-123">Die Eingabe wird nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="fd888-123">The input is not validated.</span></span> <span data-ttu-id="fd888-124">Es wird zuerst überprüft, wenn New-AzScheduledQueryRule schließlich aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fd888-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd888-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="fd888-125">-ThresholdOperator</span></span>
<span data-ttu-id="fd888-126">Der metrische Schwellenwertoperator: Greater Durch, Less Aus, Gleich.</span><span class="sxs-lookup"><span data-stu-id="fd888-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="fd888-127">Die Eingabe wird nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="fd888-127">The input is not validated.</span></span> <span data-ttu-id="fd888-128">Es wird zuerst überprüft, wenn New-AzScheduledQueryRule schließlich aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fd888-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="fd888-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd888-129">CommonParameters</span></span>
<span data-ttu-id="fd888-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd888-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd888-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd888-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd888-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fd888-132">INPUTS</span></span>

### <span data-ttu-id="fd888-133">Keine</span><span class="sxs-lookup"><span data-stu-id="fd888-133">None</span></span>

## <span data-ttu-id="fd888-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fd888-134">OUTPUTS</span></span>

### <span data-ttu-id="fd888-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="fd888-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="fd888-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fd888-136">NOTES</span></span>

## <span data-ttu-id="fd888-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fd888-137">RELATED LINKS</span></span>
