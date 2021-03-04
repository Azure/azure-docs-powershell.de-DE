---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 244e71148557ef46ea3305f7dc2826eb06e3b50d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924064"
---
# <span data-ttu-id="b8c09-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="b8c09-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="b8c09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8c09-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c09-103">Erstellt ein lokales Dimensionsauswahlobjekt, das zum Erstellen eines Metrikwarnkriteriums verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b8c09-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="b8c09-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8c09-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8c09-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8c09-105">DESCRIPTION</span></span>
<span data-ttu-id="b8c09-106">Das **Cmdlet New-AzMetricAlertRuleV2DimensionSelection** erstellt ein lokales Dimensionsauswahlobjekt, das beim Erstellen von Metrikwarnkriterien mithilfe des [Cmdlets New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria) helfen soll.</span><span class="sxs-lookup"><span data-stu-id="b8c09-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet.</span></span>

## <span data-ttu-id="b8c09-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b8c09-107">EXAMPLES</span></span>

### <span data-ttu-id="b8c09-108">Beispiel 1: Erstellen eines Bemaßungsauswahlobjekts</span><span class="sxs-lookup"><span data-stu-id="b8c09-108">Example 1: Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="b8c09-109">Mit diesem Befehl wird ein Dimensionsauswahlobjekt erstellt, das angibt, dass Werte für {1,3,4} Dimension "LUN" ausgewählt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b8c09-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="b8c09-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b8c09-110">PARAMETERS</span></span>

### <span data-ttu-id="b8c09-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c09-111">-DefaultProfile</span></span>
<span data-ttu-id="b8c09-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8c09-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8c09-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="b8c09-113">-DimensionName</span></span>
<span data-ttu-id="b8c09-114">Name der Dimension</span><span class="sxs-lookup"><span data-stu-id="b8c09-114">The Dimension name</span></span>

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

### <span data-ttu-id="b8c09-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="b8c09-115">-ValuesToExclude</span></span>
<span data-ttu-id="b8c09-116">Die ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="b8c09-116">The ExcludeValues</span></span>

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

### <span data-ttu-id="b8c09-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="b8c09-117">-ValuesToInclude</span></span>
<span data-ttu-id="b8c09-118">Die IncludeValues</span><span class="sxs-lookup"><span data-stu-id="b8c09-118">The IncludeValues</span></span>

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

### <span data-ttu-id="b8c09-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c09-119">CommonParameters</span></span>
<span data-ttu-id="b8c09-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8c09-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c09-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8c09-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c09-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b8c09-122">INPUTS</span></span>

### <span data-ttu-id="b8c09-123">System.String</span><span class="sxs-lookup"><span data-stu-id="b8c09-123">System.String</span></span>

### <span data-ttu-id="b8c09-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b8c09-124">System.String[]</span></span>

## <span data-ttu-id="b8c09-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b8c09-125">OUTPUTS</span></span>

### <span data-ttu-id="b8c09-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="b8c09-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="b8c09-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b8c09-127">NOTES</span></span>

## <span data-ttu-id="b8c09-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b8c09-128">RELATED LINKS</span></span>
