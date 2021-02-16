---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: d2adba5ac5c75745c43e0d1ef62fb39d9b867c5e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163908"
---
# <span data-ttu-id="89c05-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="89c05-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="89c05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89c05-102">SYNOPSIS</span></span>
<span data-ttu-id="89c05-103">Erstellen eines Speicherobjekts für "QueryFilter"</span><span class="sxs-lookup"><span data-stu-id="89c05-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="89c05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89c05-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="89c05-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89c05-105">DESCRIPTION</span></span>
<span data-ttu-id="89c05-106">Erstellen eines Speicherobjekts für "QueryFilter"</span><span class="sxs-lookup"><span data-stu-id="89c05-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="89c05-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="89c05-107">EXAMPLES</span></span>

### <span data-ttu-id="89c05-108">Beispiel 1: Erstellen eines Abfragefilterobjekts für den Kostenmanagementexport</span><span class="sxs-lookup"><span data-stu-id="89c05-108">Example 1: Create a filter object of query for cost management export</span></span>
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

<span data-ttu-id="89c05-109">Mit diesem Befehl wird ein Filterobjekt der Abfrage für den Kostenmanagementexport erstellt.</span><span class="sxs-lookup"><span data-stu-id="89c05-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="89c05-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89c05-110">PARAMETERS</span></span>

### <span data-ttu-id="89c05-111">-Und</span><span class="sxs-lookup"><span data-stu-id="89c05-111">-And</span></span>
<span data-ttu-id="89c05-112">Der logische Ausdruck "UND".</span><span class="sxs-lookup"><span data-stu-id="89c05-112">The logical "AND" expression.</span></span>
<span data-ttu-id="89c05-113">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="89c05-113">Must have at least 2 items.</span></span>
<span data-ttu-id="89c05-114">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="89c05-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89c05-115">-Dimensionen</span><span class="sxs-lookup"><span data-stu-id="89c05-115">-Dimensions</span></span>
<span data-ttu-id="89c05-116">Verfügt über einen Vergleichsausdruck für eine Dimension.</span><span class="sxs-lookup"><span data-stu-id="89c05-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="89c05-117">Informationen zum Erstellen finden Sie im Abschnitt "NOTIZEN" für #A0 und erstellen eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="89c05-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89c05-118">-Not</span><span class="sxs-lookup"><span data-stu-id="89c05-118">-Not</span></span>
<span data-ttu-id="89c05-119">Der logische Ausdruck "NOT".</span><span class="sxs-lookup"><span data-stu-id="89c05-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="89c05-120">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" für #A0 und erstellen eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="89c05-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89c05-121">-Oder</span><span class="sxs-lookup"><span data-stu-id="89c05-121">-Or</span></span>
<span data-ttu-id="89c05-122">Der logische Ausdruck "ODER".</span><span class="sxs-lookup"><span data-stu-id="89c05-122">The logical "OR" expression.</span></span>
<span data-ttu-id="89c05-123">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="89c05-123">Must have at least 2 items.</span></span>
<span data-ttu-id="89c05-124">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" für #A0 und erstellen eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="89c05-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89c05-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="89c05-125">-Tag</span></span>
<span data-ttu-id="89c05-126">Verfügt über einen Vergleichsausdruck für ein Tag.</span><span class="sxs-lookup"><span data-stu-id="89c05-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="89c05-127">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="89c05-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89c05-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89c05-128">CommonParameters</span></span>
<span data-ttu-id="89c05-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89c05-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89c05-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89c05-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89c05-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="89c05-131">INPUTS</span></span>

## <span data-ttu-id="89c05-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="89c05-132">OUTPUTS</span></span>

### <span data-ttu-id="89c05-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span><span class="sxs-lookup"><span data-stu-id="89c05-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="89c05-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="89c05-134">NOTES</span></span>

<span data-ttu-id="89c05-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="89c05-135">ALIASES</span></span>

<span data-ttu-id="89c05-136">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="89c05-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="89c05-137">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="89c05-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="89c05-138">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="89c05-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="89c05-139">AND <IQueryFilter[]>: Der logische Ausdruck "UND".</span><span class="sxs-lookup"><span data-stu-id="89c05-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="89c05-140">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="89c05-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="89c05-141">`[And <IQueryFilter[]>]`: Der logische Ausdruck "UND".</span><span class="sxs-lookup"><span data-stu-id="89c05-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="89c05-142">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="89c05-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="89c05-143">`[Dimensions <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für eine Dimension</span><span class="sxs-lookup"><span data-stu-id="89c05-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="89c05-144">`Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="89c05-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="89c05-145">`Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden</span><span class="sxs-lookup"><span data-stu-id="89c05-145">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="89c05-146">`[Not <IQueryFilter>]`: Der logische Ausdruck "NICHT".</span><span class="sxs-lookup"><span data-stu-id="89c05-146">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="89c05-147">`[Or <IQueryFilter[]>]`: Der logische Ausdruck "ODER".</span><span class="sxs-lookup"><span data-stu-id="89c05-147">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="89c05-148">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="89c05-148">Must have at least 2 items.</span></span>
  - <span data-ttu-id="89c05-149">`[Tag <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für ein Tag</span><span class="sxs-lookup"><span data-stu-id="89c05-149">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="89c05-150">DIMENSIONEN: <IQueryComparisonExpression> Verfügt über einen Vergleichsausdruck für eine Bemaßung.</span><span class="sxs-lookup"><span data-stu-id="89c05-150">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="89c05-151">`Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="89c05-151">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="89c05-152">`Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden</span><span class="sxs-lookup"><span data-stu-id="89c05-152">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="89c05-153">NOT: <IQueryFilter> Der logische Ausdruck "NOT".</span><span class="sxs-lookup"><span data-stu-id="89c05-153">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="89c05-154">`[And <IQueryFilter[]>]`: Der logische Ausdruck "UND".</span><span class="sxs-lookup"><span data-stu-id="89c05-154">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="89c05-155">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="89c05-155">Must have at least 2 items.</span></span>
  - <span data-ttu-id="89c05-156">`[Dimensions <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für eine Dimension</span><span class="sxs-lookup"><span data-stu-id="89c05-156">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="89c05-157">`Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="89c05-157">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="89c05-158">`Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden</span><span class="sxs-lookup"><span data-stu-id="89c05-158">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="89c05-159">`[Not <IQueryFilter>]`: Der logische Ausdruck "NICHT".</span><span class="sxs-lookup"><span data-stu-id="89c05-159">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="89c05-160">`[Or <IQueryFilter[]>]`: Der logische Ausdruck "ODER".</span><span class="sxs-lookup"><span data-stu-id="89c05-160">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="89c05-161">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="89c05-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="89c05-162">`[Tag <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für ein Tag</span><span class="sxs-lookup"><span data-stu-id="89c05-162">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="89c05-163">ODER <IQueryFilter[]>: Der logische Ausdruck "ODER".</span><span class="sxs-lookup"><span data-stu-id="89c05-163">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="89c05-164">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="89c05-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="89c05-165">`[And <IQueryFilter[]>]`: Der logische Ausdruck "UND".</span><span class="sxs-lookup"><span data-stu-id="89c05-165">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="89c05-166">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="89c05-166">Must have at least 2 items.</span></span>
  - <span data-ttu-id="89c05-167">`[Dimensions <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für eine Dimension</span><span class="sxs-lookup"><span data-stu-id="89c05-167">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="89c05-168">`Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="89c05-168">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="89c05-169">`Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden</span><span class="sxs-lookup"><span data-stu-id="89c05-169">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="89c05-170">`[Not <IQueryFilter>]`: Der logische Ausdruck "NICHT".</span><span class="sxs-lookup"><span data-stu-id="89c05-170">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="89c05-171">`[Or <IQueryFilter[]>]`: Der logische Ausdruck "ODER".</span><span class="sxs-lookup"><span data-stu-id="89c05-171">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="89c05-172">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="89c05-172">Must have at least 2 items.</span></span>
  - <span data-ttu-id="89c05-173">`[Tag <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für ein Tag</span><span class="sxs-lookup"><span data-stu-id="89c05-173">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="89c05-174">TAG: <IQueryComparisonExpression> Verfügt über einen Vergleichsausdruck für ein Tag.</span><span class="sxs-lookup"><span data-stu-id="89c05-174">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="89c05-175">`Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="89c05-175">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="89c05-176">`Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden</span><span class="sxs-lookup"><span data-stu-id="89c05-176">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="89c05-177">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="89c05-177">RELATED LINKS</span></span>

