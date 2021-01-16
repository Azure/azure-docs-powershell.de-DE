---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 500a0bed47fad0174e3e7efb3ee27e2bb98a9894
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293542"
---
# <span data-ttu-id="d3af2-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="d3af2-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="d3af2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3af2-102">SYNOPSIS</span></span>
<span data-ttu-id="d3af2-103">Erstellt ein lokales Dimensionsauswahlobjekt, das zum Erstellen eines metrischen Warnungskriterien verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d3af2-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="d3af2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3af2-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3af2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3af2-105">DESCRIPTION</span></span>
<span data-ttu-id="d3af2-106">Das Cmdlet **"New-AzMetricAlertRuleV2DimensionSelection"** erstellt ein lokales Dimensionsauswahlobjekt, um die Konstruktion metrischer Warnungskriterien mithilfe des Cmdlets ["New-AzMetricAlertRuleV2Criteria"](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d3af2-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet.</span></span>

## <span data-ttu-id="d3af2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d3af2-107">EXAMPLES</span></span>

### <span data-ttu-id="d3af2-108">Beispiel 1: Erstellen eines Dimensionsauswahlobjekts</span><span class="sxs-lookup"><span data-stu-id="d3af2-108">Example 1: Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="d3af2-109">Mit diesem Befehl wird ein Dimensionsauswahlobjekt erstellt, das angibt, dass Werte für die Dimension {1,3,4} "LUN" ausgewählt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d3af2-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="d3af2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3af2-110">PARAMETERS</span></span>

### <span data-ttu-id="d3af2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3af2-111">-DefaultProfile</span></span>
<span data-ttu-id="d3af2-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3af2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3af2-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="d3af2-113">-DimensionName</span></span>
<span data-ttu-id="d3af2-114">Der Name der Dimension</span><span class="sxs-lookup"><span data-stu-id="d3af2-114">The Dimension name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3af2-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="d3af2-115">-ValuesToExclude</span></span>
<span data-ttu-id="d3af2-116">Die ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="d3af2-116">The ExcludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3af2-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="d3af2-117">-ValuesToInclude</span></span>
<span data-ttu-id="d3af2-118">Die IncludeValues</span><span class="sxs-lookup"><span data-stu-id="d3af2-118">The IncludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3af2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3af2-119">CommonParameters</span></span>
<span data-ttu-id="d3af2-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3af2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3af2-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3af2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3af2-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d3af2-122">INPUTS</span></span>

### <span data-ttu-id="d3af2-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d3af2-123">System.String</span></span>

### <span data-ttu-id="d3af2-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d3af2-124">System.String[]</span></span>

## <span data-ttu-id="d3af2-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d3af2-125">OUTPUTS</span></span>

### <span data-ttu-id="d3af2-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="d3af2-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="d3af2-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d3af2-127">NOTES</span></span>

## <span data-ttu-id="d3af2-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d3af2-128">RELATED LINKS</span></span>
