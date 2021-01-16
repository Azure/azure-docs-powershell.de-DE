---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: 0fffbc11291fcf3cd7d3989e211bcbb0d202ea9b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290063"
---
# <span data-ttu-id="8aa68-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="8aa68-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="8aa68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8aa68-102">SYNOPSIS</span></span>
<span data-ttu-id="8aa68-103">Erstellt ein Objekt vom Typ "Triggerbedingung".</span><span class="sxs-lookup"><span data-stu-id="8aa68-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="8aa68-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8aa68-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8aa68-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8aa68-105">DESCRIPTION</span></span>
<span data-ttu-id="8aa68-106">Erstellt ein Objekt vom Typ "Triggerbedingung".</span><span class="sxs-lookup"><span data-stu-id="8aa68-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="8aa68-107">Dieses Objekt wird an den Befehl übergeben, der das Warnungsaktionsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="8aa68-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="8aa68-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8aa68-108">EXAMPLES</span></span>

### <span data-ttu-id="8aa68-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8aa68-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="8aa68-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8aa68-110">PARAMETERS</span></span>

### <span data-ttu-id="8aa68-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aa68-111">-DefaultProfile</span></span>
<span data-ttu-id="8aa68-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8aa68-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8aa68-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="8aa68-113">-MetricTrigger</span></span>
<span data-ttu-id="8aa68-114">Triggerbedingung für metrische Abfrageregel</span><span class="sxs-lookup"><span data-stu-id="8aa68-114">Trigger condition for metric query rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aa68-115">-Threshold</span><span class="sxs-lookup"><span data-stu-id="8aa68-115">-Threshold</span></span>
<span data-ttu-id="8aa68-116">Der Schwellenwert, über dem die Warnung ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="8aa68-116">The threshold above which alert gets fired</span></span>

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

### <span data-ttu-id="8aa68-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="8aa68-117">-ThresholdOperator</span></span>
<span data-ttu-id="8aa68-118">Der Schwellenwertoperator: Greater Aus, Less Durch oder Gleich</span><span class="sxs-lookup"><span data-stu-id="8aa68-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

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

### <span data-ttu-id="8aa68-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aa68-119">CommonParameters</span></span>
<span data-ttu-id="8aa68-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aa68-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aa68-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8aa68-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aa68-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8aa68-122">INPUTS</span></span>

### <span data-ttu-id="8aa68-123">Keine</span><span class="sxs-lookup"><span data-stu-id="8aa68-123">None</span></span>

## <span data-ttu-id="8aa68-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8aa68-124">OUTPUTS</span></span>

### <span data-ttu-id="8aa68-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="8aa68-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="8aa68-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8aa68-126">NOTES</span></span>

## <span data-ttu-id="8aa68-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8aa68-127">RELATED LINKS</span></span>
