---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: 0270c9bf6d543455772095a6d0fe3f0f1a55a416
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931827"
---
# <span data-ttu-id="0e877-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="0e877-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="0e877-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e877-102">SYNOPSIS</span></span>
<span data-ttu-id="0e877-103">Erstellt ein Objekt vom Typ Protokollmetrischer Trigger.</span><span class="sxs-lookup"><span data-stu-id="0e877-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="0e877-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e877-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0e877-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e877-105">DESCRIPTION</span></span>
<span data-ttu-id="0e877-106">Erstellt ein Objekt vom Typ Protokollmetrischer Trigger und ist optional.</span><span class="sxs-lookup"><span data-stu-id="0e877-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="0e877-107">Dies ist die Triggerbedingung für metrikierte Abfrageregel, die verwendet werden muss, wenn Sie den Metrikmesstyp der Benachrichtigung zustandsmetrisch eingeben müssen.</span><span class="sxs-lookup"><span data-stu-id="0e877-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="0e877-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0e877-108">EXAMPLES</span></span>

### <span data-ttu-id="0e877-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0e877-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="0e877-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0e877-110">PARAMETERS</span></span>

### <span data-ttu-id="0e877-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e877-111">-DefaultProfile</span></span>
<span data-ttu-id="0e877-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0e877-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e877-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="0e877-113">-MetricColumn</span></span>
<span data-ttu-id="0e877-114">Spalte, für die der Metrikwert aggregiert wird.</span><span class="sxs-lookup"><span data-stu-id="0e877-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="0e877-115">Die Eingabe wird nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="0e877-115">The input is not validated.</span></span> <span data-ttu-id="0e877-116">Sie wird zuerst überprüft, wenn New-AzScheduledQueryRule schließlich aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0e877-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="0e877-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="0e877-117">-MetricTriggerType</span></span>
<span data-ttu-id="0e877-118">Der metrische Triggertyp.</span><span class="sxs-lookup"><span data-stu-id="0e877-118">The metric trigger type.</span></span>
<span data-ttu-id="0e877-119">Die Eingabe wird nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="0e877-119">The input is not validated.</span></span> <span data-ttu-id="0e877-120">Sie wird zuerst überprüft, wenn New-AzScheduledQueryRule schließlich aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0e877-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="0e877-121">-Threshold</span><span class="sxs-lookup"><span data-stu-id="0e877-121">-Threshold</span></span>
<span data-ttu-id="0e877-122">Der Metrikschwellenwert: Fortlaufend, Summe.</span><span class="sxs-lookup"><span data-stu-id="0e877-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="0e877-123">Die Eingabe wird nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="0e877-123">The input is not validated.</span></span> <span data-ttu-id="0e877-124">Sie wird zuerst überprüft, wenn New-AzScheduledQueryRule schließlich aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0e877-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="0e877-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="0e877-125">-ThresholdOperator</span></span>
<span data-ttu-id="0e877-126">Der metrische Schwellenwertoperator: GreaterThan, LessThan, Equal.</span><span class="sxs-lookup"><span data-stu-id="0e877-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="0e877-127">Die Eingabe wird nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="0e877-127">The input is not validated.</span></span> <span data-ttu-id="0e877-128">Sie wird zuerst überprüft, wenn New-AzScheduledQueryRule schließlich aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0e877-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="0e877-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e877-129">CommonParameters</span></span>
<span data-ttu-id="0e877-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e877-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e877-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e877-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e877-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0e877-132">INPUTS</span></span>

### <span data-ttu-id="0e877-133">Keine</span><span class="sxs-lookup"><span data-stu-id="0e877-133">None</span></span>

## <span data-ttu-id="0e877-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0e877-134">OUTPUTS</span></span>

### <span data-ttu-id="0e877-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="0e877-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="0e877-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0e877-136">NOTES</span></span>

## <span data-ttu-id="0e877-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0e877-137">RELATED LINKS</span></span>
