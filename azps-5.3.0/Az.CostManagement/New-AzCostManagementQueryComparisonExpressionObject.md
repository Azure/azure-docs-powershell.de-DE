---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: 5163f4747b926118bcd166304815b27bb1c1f629
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470662"
---
# <span data-ttu-id="01f62-101">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="01f62-101">New-AzCostManagementQueryComparisonExpressionObject</span></span>

## <span data-ttu-id="01f62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01f62-102">SYNOPSIS</span></span>
<span data-ttu-id="01f62-103">Erstellen eines Speicherobjekts für den QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="01f62-103">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="01f62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01f62-104">SYNTAX</span></span>

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## <span data-ttu-id="01f62-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01f62-105">DESCRIPTION</span></span>
<span data-ttu-id="01f62-106">Erstellen eines Speicherobjekts für den QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="01f62-106">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="01f62-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="01f62-107">EXAMPLES</span></span>

### <span data-ttu-id="01f62-108">Beispiel 1: Erstellen eines Vergleichsausdrucksobjekts der Abfrage für den Kostenmanagementexport</span><span class="sxs-lookup"><span data-stu-id="01f62-108">Example 1: Create a comparison expression object of query for cost management export</span></span>
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

<span data-ttu-id="01f62-109">Mit diesem Befehl wird ein Vergleichsausdrucksobjekt der Abfrage für den Kostenmanagementexport erstellt.</span><span class="sxs-lookup"><span data-stu-id="01f62-109">This command creates a comparison expression object of query for cost management export.</span></span>

## <span data-ttu-id="01f62-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01f62-110">PARAMETERS</span></span>

### <span data-ttu-id="01f62-111">-Name</span><span class="sxs-lookup"><span data-stu-id="01f62-111">-Name</span></span>
<span data-ttu-id="01f62-112">Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="01f62-112">The name of the column to use in comparison.</span></span>

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

### <span data-ttu-id="01f62-113">-Operator</span><span class="sxs-lookup"><span data-stu-id="01f62-113">-Operator</span></span>
<span data-ttu-id="01f62-114">Der zum Vergleich zu verwendende Operator.</span><span class="sxs-lookup"><span data-stu-id="01f62-114">The operator to use for comparison.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.OperatorType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01f62-115">-Value</span><span class="sxs-lookup"><span data-stu-id="01f62-115">-Value</span></span>
<span data-ttu-id="01f62-116">Array von Werten, die zum Vergleich verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01f62-116">Array of values to use for comparison.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01f62-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01f62-117">CommonParameters</span></span>
<span data-ttu-id="01f62-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01f62-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01f62-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01f62-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01f62-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="01f62-120">INPUTS</span></span>

## <span data-ttu-id="01f62-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="01f62-121">OUTPUTS</span></span>

### <span data-ttu-id="01f62-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="01f62-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span></span>

## <span data-ttu-id="01f62-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="01f62-123">NOTES</span></span>

<span data-ttu-id="01f62-124">ALIASE</span><span class="sxs-lookup"><span data-stu-id="01f62-124">ALIASES</span></span>

## <span data-ttu-id="01f62-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="01f62-125">RELATED LINKS</span></span>

