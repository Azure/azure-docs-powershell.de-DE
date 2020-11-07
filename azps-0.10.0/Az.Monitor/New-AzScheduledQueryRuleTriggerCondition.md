---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: 53331c82a2ea1ac16b67c32f67545fec7d08e3dd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841939"
---
# <span data-ttu-id="33666-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="33666-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="33666-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="33666-102">SYNOPSIS</span></span>
<span data-ttu-id="33666-103">Erstellt ein Objekt vom Typ Trigger Condition</span><span class="sxs-lookup"><span data-stu-id="33666-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="33666-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="33666-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33666-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="33666-105">DESCRIPTION</span></span>
<span data-ttu-id="33666-106">Erstellt ein Objekt vom Typ Trigger Condition.</span><span class="sxs-lookup"><span data-stu-id="33666-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="33666-107">Dieses Objekt soll an den Befehl übergeben werden, der ein Warnungs Aktionsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="33666-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="33666-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33666-108">EXAMPLES</span></span>

### <span data-ttu-id="33666-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="33666-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="33666-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="33666-110">PARAMETERS</span></span>

### <span data-ttu-id="33666-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33666-111">-DefaultProfile</span></span>
<span data-ttu-id="33666-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="33666-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33666-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="33666-113">-MetricTrigger</span></span>
<span data-ttu-id="33666-114">Trigger-Bedingung für metrische Abfrageregel</span><span class="sxs-lookup"><span data-stu-id="33666-114">Trigger condition for metric query rule</span></span>

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

### <span data-ttu-id="33666-115">-Threshold</span><span class="sxs-lookup"><span data-stu-id="33666-115">-Threshold</span></span>
<span data-ttu-id="33666-116">Der Schwellenwert, über dem die Benachrichtigung ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="33666-116">The threshold above which alert gets fired</span></span>

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

### <span data-ttu-id="33666-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="33666-117">-ThresholdOperator</span></span>
<span data-ttu-id="33666-118">Der Schwellenwert Operator: GreaterThan, LessThan oder gleich</span><span class="sxs-lookup"><span data-stu-id="33666-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

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

### <span data-ttu-id="33666-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33666-119">CommonParameters</span></span>
<span data-ttu-id="33666-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33666-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33666-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33666-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33666-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="33666-122">INPUTS</span></span>

### <span data-ttu-id="33666-123">Keine</span><span class="sxs-lookup"><span data-stu-id="33666-123">None</span></span>

## <span data-ttu-id="33666-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="33666-124">OUTPUTS</span></span>

### <span data-ttu-id="33666-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="33666-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="33666-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="33666-126">NOTES</span></span>

## <span data-ttu-id="33666-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="33666-127">RELATED LINKS</span></span>
