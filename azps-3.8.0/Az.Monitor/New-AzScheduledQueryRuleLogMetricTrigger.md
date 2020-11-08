---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c4d44f266a9966f605e009cc4ce5dece0fa5e2ae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995093"
---
# <span data-ttu-id="e5cf3-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="e5cf3-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="e5cf3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5cf3-102">SYNOPSIS</span></span>
<span data-ttu-id="e5cf3-103">Erstellt ein Objekt vom Typ Log Metric Trigger.</span><span class="sxs-lookup"><span data-stu-id="e5cf3-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="e5cf3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5cf3-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5cf3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5cf3-105">DESCRIPTION</span></span>
<span data-ttu-id="e5cf3-106">Erstellt ein Objekt vom Typ Log Metric Trigger und ist optional.</span><span class="sxs-lookup"><span data-stu-id="e5cf3-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="e5cf3-107">Dies ist die Trigger-Bedingung für eine metrische Abfrageregel, die verwendet werden soll, wenn Sie den metrischen Messtyp der Warnung angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="e5cf3-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="e5cf3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5cf3-108">EXAMPLES</span></span>

### <span data-ttu-id="e5cf3-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5cf3-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="e5cf3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5cf3-110">PARAMETERS</span></span>

### <span data-ttu-id="e5cf3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5cf3-111">-DefaultProfile</span></span>
<span data-ttu-id="e5cf3-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5cf3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5cf3-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="e5cf3-113">-MetricColumn</span></span>
<span data-ttu-id="e5cf3-114">Die Spalte, in der der metrische Wert aggregiert wird.</span><span class="sxs-lookup"><span data-stu-id="e5cf3-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="e5cf3-115">Die Eingabe wird nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="e5cf3-115">The input is not validated.</span></span> <span data-ttu-id="e5cf3-116">Sie wird zuerst überprüft, wenn New-AzScheduledQueryRule schließlich aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e5cf3-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="e5cf3-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="e5cf3-117">-MetricTriggerType</span></span>
<span data-ttu-id="e5cf3-118">Der Typ des metrischen Triggers.</span><span class="sxs-lookup"><span data-stu-id="e5cf3-118">The metric trigger type.</span></span>
<span data-ttu-id="e5cf3-119">Die Eingabe wird nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="e5cf3-119">The input is not validated.</span></span> <span data-ttu-id="e5cf3-120">Sie wird zuerst überprüft, wenn New-AzScheduledQueryRule schließlich aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e5cf3-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="e5cf3-121">-Threshold</span><span class="sxs-lookup"><span data-stu-id="e5cf3-121">-Threshold</span></span>
<span data-ttu-id="e5cf3-122">Der metrische Schwellenwert: konsekutiv, Total.</span><span class="sxs-lookup"><span data-stu-id="e5cf3-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="e5cf3-123">Die Eingabe wird nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="e5cf3-123">The input is not validated.</span></span> <span data-ttu-id="e5cf3-124">Sie wird zuerst überprüft, wenn New-AzScheduledQueryRule schließlich aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e5cf3-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="e5cf3-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="e5cf3-125">-ThresholdOperator</span></span>
<span data-ttu-id="e5cf3-126">Der Metrik-Schwellenwert Operator: GreaterThan, LessThan, gleich.</span><span class="sxs-lookup"><span data-stu-id="e5cf3-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="e5cf3-127">Die Eingabe wird nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="e5cf3-127">The input is not validated.</span></span> <span data-ttu-id="e5cf3-128">Sie wird zuerst überprüft, wenn New-AzScheduledQueryRule schließlich aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e5cf3-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="e5cf3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5cf3-129">CommonParameters</span></span>
<span data-ttu-id="e5cf3-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5cf3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5cf3-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5cf3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5cf3-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5cf3-132">INPUTS</span></span>

### <span data-ttu-id="e5cf3-133">Keine</span><span class="sxs-lookup"><span data-stu-id="e5cf3-133">None</span></span>

## <span data-ttu-id="e5cf3-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5cf3-134">OUTPUTS</span></span>

### <span data-ttu-id="e5cf3-135">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="e5cf3-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="e5cf3-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5cf3-136">NOTES</span></span>

## <span data-ttu-id="e5cf3-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5cf3-137">RELATED LINKS</span></span>
