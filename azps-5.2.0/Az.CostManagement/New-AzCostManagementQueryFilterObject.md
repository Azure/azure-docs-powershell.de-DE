---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: e7b5c605af531bd1c1251a1c615da9498059d43d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296057"
---
# <span data-ttu-id="16a8b-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="16a8b-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="16a8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="16a8b-103">Erstellen eines Speicherobjekts für "QueryFilter"</span><span class="sxs-lookup"><span data-stu-id="16a8b-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="16a8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16a8b-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="16a8b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16a8b-105">DESCRIPTION</span></span>
<span data-ttu-id="16a8b-106">Erstellen eines Speicherobjekts für "QueryFilter"</span><span class="sxs-lookup"><span data-stu-id="16a8b-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="16a8b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="16a8b-107">EXAMPLES</span></span>

### <span data-ttu-id="16a8b-108">Beispiel 1: Erstellen eines Abfragefilterobjekts für den Kostenmanagementexport</span><span class="sxs-lookup"><span data-stu-id="16a8b-108">Example 1: Create a filter object of query for cost management export</span></span>
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Operator In -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

<span data-ttu-id="16a8b-109">Mit diesem Befehl wird ein Filterobjekt der Abfrage für den Kostenmanagementexport erstellt.</span><span class="sxs-lookup"><span data-stu-id="16a8b-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="16a8b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16a8b-110">PARAMETERS</span></span>

### <span data-ttu-id="16a8b-111">-Und</span><span class="sxs-lookup"><span data-stu-id="16a8b-111">-And</span></span>
<span data-ttu-id="16a8b-112">Der logische Ausdruck "UND".</span><span class="sxs-lookup"><span data-stu-id="16a8b-112">The logical "AND" expression.</span></span>
<span data-ttu-id="16a8b-113">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="16a8b-113">Must have at least 2 items.</span></span>
<span data-ttu-id="16a8b-114">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="16a8b-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

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

### <span data-ttu-id="16a8b-115">-Dimensionen</span><span class="sxs-lookup"><span data-stu-id="16a8b-115">-Dimensions</span></span>
<span data-ttu-id="16a8b-116">Verfügt über einen Vergleichsausdruck für eine Dimension.</span><span class="sxs-lookup"><span data-stu-id="16a8b-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="16a8b-117">Informationen zum Erstellen finden Sie im Abschnitt "NOTIZEN" für #A0 und erstellen eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="16a8b-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

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

### <span data-ttu-id="16a8b-118">-Not</span><span class="sxs-lookup"><span data-stu-id="16a8b-118">-Not</span></span>
<span data-ttu-id="16a8b-119">Der logische Ausdruck "NOT".</span><span class="sxs-lookup"><span data-stu-id="16a8b-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="16a8b-120">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" für #A0 und erstellen eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="16a8b-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

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

### <span data-ttu-id="16a8b-121">-Oder</span><span class="sxs-lookup"><span data-stu-id="16a8b-121">-Or</span></span>
<span data-ttu-id="16a8b-122">Der logische Ausdruck "ODER".</span><span class="sxs-lookup"><span data-stu-id="16a8b-122">The logical "OR" expression.</span></span>
<span data-ttu-id="16a8b-123">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="16a8b-123">Must have at least 2 items.</span></span>
<span data-ttu-id="16a8b-124">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" für #A0 und erstellen eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="16a8b-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

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

### <span data-ttu-id="16a8b-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="16a8b-125">-Tag</span></span>
<span data-ttu-id="16a8b-126">Verfügt über einen Vergleichsausdruck für ein Tag.</span><span class="sxs-lookup"><span data-stu-id="16a8b-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="16a8b-127">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="16a8b-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

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

### <span data-ttu-id="16a8b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16a8b-128">CommonParameters</span></span>
<span data-ttu-id="16a8b-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16a8b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16a8b-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16a8b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16a8b-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="16a8b-131">INPUTS</span></span>

## <span data-ttu-id="16a8b-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="16a8b-132">OUTPUTS</span></span>

### <span data-ttu-id="16a8b-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span><span class="sxs-lookup"><span data-stu-id="16a8b-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="16a8b-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="16a8b-134">NOTES</span></span>

<span data-ttu-id="16a8b-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="16a8b-135">ALIASES</span></span>

<span data-ttu-id="16a8b-136">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="16a8b-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="16a8b-137">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="16a8b-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="16a8b-138">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="16a8b-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="16a8b-139">AND <IQueryFilter[]>: Der logische Ausdruck "UND".</span><span class="sxs-lookup"><span data-stu-id="16a8b-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="16a8b-140">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="16a8b-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="16a8b-141">`[And <IQueryFilter[]>]`: Der logische Ausdruck "UND".</span><span class="sxs-lookup"><span data-stu-id="16a8b-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="16a8b-142">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="16a8b-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="16a8b-143">`[Dimensions <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für eine Dimension</span><span class="sxs-lookup"><span data-stu-id="16a8b-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="16a8b-144">`Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="16a8b-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="16a8b-145">`Operator <OperatorType>`: Der operator, der zum Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="16a8b-145">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="16a8b-146">`Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden</span><span class="sxs-lookup"><span data-stu-id="16a8b-146">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="16a8b-147">`[Not <IQueryFilter>]`: Der logische Ausdruck "NICHT".</span><span class="sxs-lookup"><span data-stu-id="16a8b-147">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="16a8b-148">`[Or <IQueryFilter[]>]`: Der logische Ausdruck "ODER".</span><span class="sxs-lookup"><span data-stu-id="16a8b-148">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="16a8b-149">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="16a8b-149">Must have at least 2 items.</span></span>
  - <span data-ttu-id="16a8b-150">`[Tag <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für ein Tag</span><span class="sxs-lookup"><span data-stu-id="16a8b-150">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="16a8b-151">DIMENSIONEN: <IQueryComparisonExpression> Verfügt über einen Vergleichsausdruck für eine Bemaßung.</span><span class="sxs-lookup"><span data-stu-id="16a8b-151">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="16a8b-152">`Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="16a8b-152">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="16a8b-153">`Operator <OperatorType>`: Der operator, der zum Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="16a8b-153">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="16a8b-154">`Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden</span><span class="sxs-lookup"><span data-stu-id="16a8b-154">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="16a8b-155">NOT: <IQueryFilter> Der logische Ausdruck "NOT".</span><span class="sxs-lookup"><span data-stu-id="16a8b-155">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="16a8b-156">`[And <IQueryFilter[]>]`: Der logische Ausdruck "UND".</span><span class="sxs-lookup"><span data-stu-id="16a8b-156">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="16a8b-157">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="16a8b-157">Must have at least 2 items.</span></span>
  - <span data-ttu-id="16a8b-158">`[Dimensions <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für eine Dimension</span><span class="sxs-lookup"><span data-stu-id="16a8b-158">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="16a8b-159">`Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="16a8b-159">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="16a8b-160">`Operator <OperatorType>`: Der operator, der zum Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="16a8b-160">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="16a8b-161">`Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden</span><span class="sxs-lookup"><span data-stu-id="16a8b-161">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="16a8b-162">`[Not <IQueryFilter>]`: Der logische Ausdruck "NICHT".</span><span class="sxs-lookup"><span data-stu-id="16a8b-162">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="16a8b-163">`[Or <IQueryFilter[]>]`: Der logische Ausdruck "ODER".</span><span class="sxs-lookup"><span data-stu-id="16a8b-163">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="16a8b-164">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="16a8b-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="16a8b-165">`[Tag <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für ein Tag</span><span class="sxs-lookup"><span data-stu-id="16a8b-165">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="16a8b-166">ODER <IQueryFilter[]>: Der logische Ausdruck "ODER".</span><span class="sxs-lookup"><span data-stu-id="16a8b-166">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="16a8b-167">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="16a8b-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="16a8b-168">`[And <IQueryFilter[]>]`: Der logische Ausdruck "UND".</span><span class="sxs-lookup"><span data-stu-id="16a8b-168">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="16a8b-169">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="16a8b-169">Must have at least 2 items.</span></span>
  - <span data-ttu-id="16a8b-170">`[Dimensions <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für eine Dimension</span><span class="sxs-lookup"><span data-stu-id="16a8b-170">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="16a8b-171">`Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="16a8b-171">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="16a8b-172">`Operator <OperatorType>`: Der operator, der zum Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="16a8b-172">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="16a8b-173">`Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden</span><span class="sxs-lookup"><span data-stu-id="16a8b-173">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="16a8b-174">`[Not <IQueryFilter>]`: Der logische Ausdruck "NICHT".</span><span class="sxs-lookup"><span data-stu-id="16a8b-174">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="16a8b-175">`[Or <IQueryFilter[]>]`: Der logische Ausdruck "ODER".</span><span class="sxs-lookup"><span data-stu-id="16a8b-175">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="16a8b-176">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="16a8b-176">Must have at least 2 items.</span></span>
  - <span data-ttu-id="16a8b-177">`[Tag <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für ein Tag</span><span class="sxs-lookup"><span data-stu-id="16a8b-177">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="16a8b-178">TAG: <IQueryComparisonExpression> Verfügt über einen Vergleichsausdruck für ein Tag.</span><span class="sxs-lookup"><span data-stu-id="16a8b-178">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="16a8b-179">`Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="16a8b-179">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="16a8b-180">`Operator <OperatorType>`: Der operator, der zum Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="16a8b-180">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="16a8b-181">`Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden</span><span class="sxs-lookup"><span data-stu-id="16a8b-181">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="16a8b-182">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="16a8b-182">RELATED LINKS</span></span>

