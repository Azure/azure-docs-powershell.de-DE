---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: 4873d093411c07af9b1a5389299e39ecca0a5f71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822680"
---
# <span data-ttu-id="532ae-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="532ae-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="532ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="532ae-102">SYNOPSIS</span></span>
<span data-ttu-id="532ae-103">Erstellt ein Objekt vom Typ Log Metric Trigger</span><span class="sxs-lookup"><span data-stu-id="532ae-103">Creates an object of type Log Metric Trigger</span></span>

## <span data-ttu-id="532ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="532ae-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="532ae-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="532ae-105">DESCRIPTION</span></span>
<span data-ttu-id="532ae-106">Erstellt ein Objekt vom Typ Log Metric Trigger und ist optional.</span><span class="sxs-lookup"><span data-stu-id="532ae-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="532ae-107">Dies ist die Trigger-Bedingung für eine metrische Abfrageregel, die verwendet werden soll, wenn Sie den metrischen Messtyp der Warnung angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="532ae-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="532ae-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="532ae-108">EXAMPLES</span></span>

### <span data-ttu-id="532ae-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="532ae-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="532ae-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="532ae-110">PARAMETERS</span></span>

### <span data-ttu-id="532ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="532ae-111">-DefaultProfile</span></span>
<span data-ttu-id="532ae-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="532ae-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="532ae-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="532ae-113">-MetricColumn</span></span>
<span data-ttu-id="532ae-114">Spalte, in der der metrische Wert aggregiert wird</span><span class="sxs-lookup"><span data-stu-id="532ae-114">Column on which metric value is being aggregated</span></span>

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

### <span data-ttu-id="532ae-115">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="532ae-115">-MetricTriggerType</span></span>
<span data-ttu-id="532ae-116">Der Typ des metrischen Triggers</span><span class="sxs-lookup"><span data-stu-id="532ae-116">The metric trigger type</span></span>

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

### <span data-ttu-id="532ae-117">-Threshold</span><span class="sxs-lookup"><span data-stu-id="532ae-117">-Threshold</span></span>
<span data-ttu-id="532ae-118">Der metrische Schwellenwert</span><span class="sxs-lookup"><span data-stu-id="532ae-118">The metric threshold value</span></span>

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

### <span data-ttu-id="532ae-119">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="532ae-119">-ThresholdOperator</span></span>
<span data-ttu-id="532ae-120">Der Metrik-Schwellenwert Operator: GreaterThan, LessThan, gleich</span><span class="sxs-lookup"><span data-stu-id="532ae-120">The metric threshold operator : GreaterThan, LessThan, Equal</span></span>

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

### <span data-ttu-id="532ae-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="532ae-121">CommonParameters</span></span>
<span data-ttu-id="532ae-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="532ae-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="532ae-123">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="532ae-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="532ae-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="532ae-124">INPUTS</span></span>

### <span data-ttu-id="532ae-125">Keine</span><span class="sxs-lookup"><span data-stu-id="532ae-125">None</span></span>

## <span data-ttu-id="532ae-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="532ae-126">OUTPUTS</span></span>

### <span data-ttu-id="532ae-127">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="532ae-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="532ae-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="532ae-128">NOTES</span></span>

## <span data-ttu-id="532ae-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="532ae-129">RELATED LINKS</span></span>
