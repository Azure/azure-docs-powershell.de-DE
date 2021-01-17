---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: e7b5c605af531bd1c1251a1c615da9498059d43d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472756"
---
# <span data-ttu-id="057cd-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="057cd-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="057cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="057cd-102">SYNOPSIS</span></span>
<span data-ttu-id="057cd-103">Erstellen eines Speicherobjekts für "QueryFilter"</span><span class="sxs-lookup"><span data-stu-id="057cd-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="057cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="057cd-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="057cd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="057cd-105">DESCRIPTION</span></span>
<span data-ttu-id="057cd-106">Erstellen eines Speicherobjekts für "QueryFilter"</span><span class="sxs-lookup"><span data-stu-id="057cd-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="057cd-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="057cd-107">EXAMPLES</span></span>

### <span data-ttu-id="057cd-108">Beispiel 1: Erstellen eines Abfragefilterobjekts für den Kostenmanagementexport</span><span class="sxs-lookup"><span data-stu-id="057cd-108">Example 1: Create a filter object of query for cost management export</span></span>
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

<span data-ttu-id="057cd-109">Mit diesem Befehl wird ein Filterobjekt der Abfrage für den Kostenmanagementexport erstellt.</span><span class="sxs-lookup"><span data-stu-id="057cd-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="057cd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="057cd-110">PARAMETERS</span></span>

### <span data-ttu-id="057cd-111">-Und</span><span class="sxs-lookup"><span data-stu-id="057cd-111">-And</span></span>
<span data-ttu-id="057cd-112">Der logische Ausdruck "UND".</span><span class="sxs-lookup"><span data-stu-id="057cd-112">The logical "AND" expression.</span></span>
<span data-ttu-id="057cd-113">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="057cd-113">Must have at least 2 items.</span></span>
<span data-ttu-id="057cd-114">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="057cd-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

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

### <span data-ttu-id="057cd-115">-Dimensionen</span><span class="sxs-lookup"><span data-stu-id="057cd-115">-Dimensions</span></span>
<span data-ttu-id="057cd-116">Verfügt über einen Vergleichsausdruck für eine Dimension.</span><span class="sxs-lookup"><span data-stu-id="057cd-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="057cd-117">Informationen zum Erstellen finden Sie im Abschnitt "NOTIZEN" für #A0 und erstellen eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="057cd-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

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

### <span data-ttu-id="057cd-118">-Not</span><span class="sxs-lookup"><span data-stu-id="057cd-118">-Not</span></span>
<span data-ttu-id="057cd-119">Der logische Ausdruck "NOT".</span><span class="sxs-lookup"><span data-stu-id="057cd-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="057cd-120">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" für #A0 und erstellen eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="057cd-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

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

### <span data-ttu-id="057cd-121">-Oder</span><span class="sxs-lookup"><span data-stu-id="057cd-121">-Or</span></span>
<span data-ttu-id="057cd-122">Der logische Ausdruck "ODER".</span><span class="sxs-lookup"><span data-stu-id="057cd-122">The logical "OR" expression.</span></span>
<span data-ttu-id="057cd-123">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="057cd-123">Must have at least 2 items.</span></span>
<span data-ttu-id="057cd-124">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" für #A0 und erstellen eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="057cd-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

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

### <span data-ttu-id="057cd-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="057cd-125">-Tag</span></span>
<span data-ttu-id="057cd-126">Verfügt über einen Vergleichsausdruck für ein Tag.</span><span class="sxs-lookup"><span data-stu-id="057cd-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="057cd-127">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="057cd-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

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

### <span data-ttu-id="057cd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="057cd-128">CommonParameters</span></span>
<span data-ttu-id="057cd-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="057cd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="057cd-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="057cd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="057cd-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="057cd-131">INPUTS</span></span>

## <span data-ttu-id="057cd-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="057cd-132">OUTPUTS</span></span>

### <span data-ttu-id="057cd-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span><span class="sxs-lookup"><span data-stu-id="057cd-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="057cd-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="057cd-134">NOTES</span></span>

<span data-ttu-id="057cd-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="057cd-135">ALIASES</span></span>

<span data-ttu-id="057cd-136">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="057cd-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="057cd-137">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="057cd-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="057cd-138">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="057cd-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="057cd-139">AND <IQueryFilter[]>: Der logische Ausdruck "UND".</span><span class="sxs-lookup"><span data-stu-id="057cd-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="057cd-140">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="057cd-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="057cd-141">`[And <IQueryFilter[]>]`: Der logische Ausdruck "UND".</span><span class="sxs-lookup"><span data-stu-id="057cd-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="057cd-142">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="057cd-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="057cd-143">`[Dimensions <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für eine Dimension</span><span class="sxs-lookup"><span data-stu-id="057cd-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="057cd-144">`Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="057cd-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="057cd-145">`Operator <OperatorType>`: Der operator, der zum Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="057cd-145">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="057cd-146">`Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden</span><span class="sxs-lookup"><span data-stu-id="057cd-146">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="057cd-147">`[Not <IQueryFilter>]`: Der logische Ausdruck "NICHT".</span><span class="sxs-lookup"><span data-stu-id="057cd-147">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="057cd-148">`[Or <IQueryFilter[]>]`: Der logische Ausdruck "ODER".</span><span class="sxs-lookup"><span data-stu-id="057cd-148">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="057cd-149">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="057cd-149">Must have at least 2 items.</span></span>
  - <span data-ttu-id="057cd-150">`[Tag <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für ein Tag</span><span class="sxs-lookup"><span data-stu-id="057cd-150">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="057cd-151">DIMENSIONEN: <IQueryComparisonExpression> Verfügt über einen Vergleichsausdruck für eine Bemaßung.</span><span class="sxs-lookup"><span data-stu-id="057cd-151">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="057cd-152">`Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="057cd-152">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="057cd-153">`Operator <OperatorType>`: Der operator, der zum Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="057cd-153">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="057cd-154">`Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden</span><span class="sxs-lookup"><span data-stu-id="057cd-154">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="057cd-155">NOT: <IQueryFilter> Der logische Ausdruck "NOT".</span><span class="sxs-lookup"><span data-stu-id="057cd-155">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="057cd-156">`[And <IQueryFilter[]>]`: Der logische Ausdruck "UND".</span><span class="sxs-lookup"><span data-stu-id="057cd-156">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="057cd-157">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="057cd-157">Must have at least 2 items.</span></span>
  - <span data-ttu-id="057cd-158">`[Dimensions <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für eine Dimension</span><span class="sxs-lookup"><span data-stu-id="057cd-158">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="057cd-159">`Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="057cd-159">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="057cd-160">`Operator <OperatorType>`: Der operator, der zum Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="057cd-160">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="057cd-161">`Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden</span><span class="sxs-lookup"><span data-stu-id="057cd-161">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="057cd-162">`[Not <IQueryFilter>]`: Der logische Ausdruck "NICHT".</span><span class="sxs-lookup"><span data-stu-id="057cd-162">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="057cd-163">`[Or <IQueryFilter[]>]`: Der logische Ausdruck "ODER".</span><span class="sxs-lookup"><span data-stu-id="057cd-163">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="057cd-164">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="057cd-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="057cd-165">`[Tag <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für ein Tag</span><span class="sxs-lookup"><span data-stu-id="057cd-165">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="057cd-166">ODER <IQueryFilter[]>: Der logische Ausdruck "ODER".</span><span class="sxs-lookup"><span data-stu-id="057cd-166">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="057cd-167">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="057cd-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="057cd-168">`[And <IQueryFilter[]>]`: Der logische Ausdruck "UND".</span><span class="sxs-lookup"><span data-stu-id="057cd-168">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="057cd-169">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="057cd-169">Must have at least 2 items.</span></span>
  - <span data-ttu-id="057cd-170">`[Dimensions <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für eine Dimension</span><span class="sxs-lookup"><span data-stu-id="057cd-170">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="057cd-171">`Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="057cd-171">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="057cd-172">`Operator <OperatorType>`: Der operator, der zum Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="057cd-172">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="057cd-173">`Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden</span><span class="sxs-lookup"><span data-stu-id="057cd-173">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="057cd-174">`[Not <IQueryFilter>]`: Der logische Ausdruck "NICHT".</span><span class="sxs-lookup"><span data-stu-id="057cd-174">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="057cd-175">`[Or <IQueryFilter[]>]`: Der logische Ausdruck "ODER".</span><span class="sxs-lookup"><span data-stu-id="057cd-175">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="057cd-176">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="057cd-176">Must have at least 2 items.</span></span>
  - <span data-ttu-id="057cd-177">`[Tag <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für ein Tag</span><span class="sxs-lookup"><span data-stu-id="057cd-177">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="057cd-178">TAG: <IQueryComparisonExpression> Verfügt über einen Vergleichsausdruck für ein Tag.</span><span class="sxs-lookup"><span data-stu-id="057cd-178">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="057cd-179">`Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="057cd-179">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="057cd-180">`Operator <OperatorType>`: Der operator, der zum Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="057cd-180">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="057cd-181">`Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden</span><span class="sxs-lookup"><span data-stu-id="057cd-181">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="057cd-182">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="057cd-182">RELATED LINKS</span></span>

