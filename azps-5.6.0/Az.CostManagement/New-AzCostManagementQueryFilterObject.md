---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: 84b54353b1f36dbfbb3cef068987c50a4b60923e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947939"
---
# <span data-ttu-id="539b5-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="539b5-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="539b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="539b5-102">SYNOPSIS</span></span>
<span data-ttu-id="539b5-103">Erstellen eines Speicherobjekts für QueryFilter</span><span class="sxs-lookup"><span data-stu-id="539b5-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="539b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="539b5-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="539b5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="539b5-105">DESCRIPTION</span></span>
<span data-ttu-id="539b5-106">Erstellen eines Speicherobjekts für QueryFilter</span><span class="sxs-lookup"><span data-stu-id="539b5-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="539b5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="539b5-107">EXAMPLES</span></span>

### <span data-ttu-id="539b5-108">Beispiel 1: Erstellen eines Filterobjekts der Abfrage für den Kostenverwaltungsexport</span><span class="sxs-lookup"><span data-stu-id="539b5-108">Example 1: Create a filter object of query for cost management export</span></span>
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

<span data-ttu-id="539b5-109">Mit diesem Befehl wird ein Filterobjekt der Abfrage für den Kostenverwaltungsexport erstellt.</span><span class="sxs-lookup"><span data-stu-id="539b5-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="539b5-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="539b5-110">PARAMETERS</span></span>

### <span data-ttu-id="539b5-111">-Und</span><span class="sxs-lookup"><span data-stu-id="539b5-111">-And</span></span>
<span data-ttu-id="539b5-112">Der logische Ausdruck "UND".</span><span class="sxs-lookup"><span data-stu-id="539b5-112">The logical "AND" expression.</span></span>
<span data-ttu-id="539b5-113">Muss mindestens zwei Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="539b5-113">Must have at least 2 items.</span></span>
<span data-ttu-id="539b5-114">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN für UND-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="539b5-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

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

### <span data-ttu-id="539b5-115">-Dimensionen</span><span class="sxs-lookup"><span data-stu-id="539b5-115">-Dimensions</span></span>
<span data-ttu-id="539b5-116">Verfügt über einen Vergleichsausdruck für eine Dimension.</span><span class="sxs-lookup"><span data-stu-id="539b5-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="539b5-117">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu DIMENSIONS-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="539b5-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

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

### <span data-ttu-id="539b5-118">-Not</span><span class="sxs-lookup"><span data-stu-id="539b5-118">-Not</span></span>
<span data-ttu-id="539b5-119">Der logische Ausdruck "NOT".</span><span class="sxs-lookup"><span data-stu-id="539b5-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="539b5-120">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN für #A0 und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="539b5-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

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

### <span data-ttu-id="539b5-121">-Oder</span><span class="sxs-lookup"><span data-stu-id="539b5-121">-Or</span></span>
<span data-ttu-id="539b5-122">Der logische Ausdruck "ODER".</span><span class="sxs-lookup"><span data-stu-id="539b5-122">The logical "OR" expression.</span></span>
<span data-ttu-id="539b5-123">Muss mindestens zwei Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="539b5-123">Must have at least 2 items.</span></span>
<span data-ttu-id="539b5-124">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN für #A0 und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="539b5-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

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

### <span data-ttu-id="539b5-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="539b5-125">-Tag</span></span>
<span data-ttu-id="539b5-126">Verfügt über einen Vergleichsausdruck für ein Tag.</span><span class="sxs-lookup"><span data-stu-id="539b5-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="539b5-127">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu #A0 und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="539b5-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

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

### <span data-ttu-id="539b5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="539b5-128">CommonParameters</span></span>
<span data-ttu-id="539b5-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="539b5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="539b5-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="539b5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="539b5-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="539b5-131">INPUTS</span></span>

## <span data-ttu-id="539b5-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="539b5-132">OUTPUTS</span></span>

### <span data-ttu-id="539b5-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span><span class="sxs-lookup"><span data-stu-id="539b5-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="539b5-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="539b5-134">NOTES</span></span>

<span data-ttu-id="539b5-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="539b5-135">ALIASES</span></span>

<span data-ttu-id="539b5-136">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="539b5-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="539b5-137">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="539b5-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="539b5-138">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="539b5-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="539b5-139">UND <IQueryFilter[]>: Der logische Ausdruck "UND".</span><span class="sxs-lookup"><span data-stu-id="539b5-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="539b5-140">Muss mindestens zwei Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="539b5-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="539b5-141">`[And <IQueryFilter[]>]`: Der logische Ausdruck "UND".</span><span class="sxs-lookup"><span data-stu-id="539b5-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="539b5-142">Muss mindestens zwei Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="539b5-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="539b5-143">`[Dimensions <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für eine Dimension</span><span class="sxs-lookup"><span data-stu-id="539b5-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="539b5-144">`Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="539b5-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="539b5-145">`Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden</span><span class="sxs-lookup"><span data-stu-id="539b5-145">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="539b5-146">`[Not <IQueryFilter>]`: Der logische Ausdruck "NOT".</span><span class="sxs-lookup"><span data-stu-id="539b5-146">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="539b5-147">`[Or <IQueryFilter[]>]`: Der logische Ausdruck "ODER".</span><span class="sxs-lookup"><span data-stu-id="539b5-147">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="539b5-148">Muss mindestens zwei Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="539b5-148">Must have at least 2 items.</span></span>
  - <span data-ttu-id="539b5-149">`[Tag <IQueryComparisonExpression>]`: Verfügt über Vergleichsausdruck für ein Tag</span><span class="sxs-lookup"><span data-stu-id="539b5-149">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="539b5-150">DIMENSIONEN <IQueryComparisonExpression> : Verfügt über einen Vergleichsausdruck für eine Dimension.</span><span class="sxs-lookup"><span data-stu-id="539b5-150">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="539b5-151">`Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="539b5-151">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="539b5-152">`Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden</span><span class="sxs-lookup"><span data-stu-id="539b5-152">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="539b5-153">NICHT: <IQueryFilter> Der logische Ausdruck "NOT".</span><span class="sxs-lookup"><span data-stu-id="539b5-153">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="539b5-154">`[And <IQueryFilter[]>]`: Der logische Ausdruck "UND".</span><span class="sxs-lookup"><span data-stu-id="539b5-154">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="539b5-155">Muss mindestens zwei Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="539b5-155">Must have at least 2 items.</span></span>
  - <span data-ttu-id="539b5-156">`[Dimensions <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für eine Dimension</span><span class="sxs-lookup"><span data-stu-id="539b5-156">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="539b5-157">`Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="539b5-157">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="539b5-158">`Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden</span><span class="sxs-lookup"><span data-stu-id="539b5-158">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="539b5-159">`[Not <IQueryFilter>]`: Der logische Ausdruck "NOT".</span><span class="sxs-lookup"><span data-stu-id="539b5-159">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="539b5-160">`[Or <IQueryFilter[]>]`: Der logische Ausdruck "ODER".</span><span class="sxs-lookup"><span data-stu-id="539b5-160">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="539b5-161">Muss mindestens zwei Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="539b5-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="539b5-162">`[Tag <IQueryComparisonExpression>]`: Verfügt über Vergleichsausdruck für ein Tag</span><span class="sxs-lookup"><span data-stu-id="539b5-162">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="539b5-163">ODER <IQueryFilter[]>: Der logische Ausdruck "ODER".</span><span class="sxs-lookup"><span data-stu-id="539b5-163">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="539b5-164">Muss mindestens zwei Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="539b5-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="539b5-165">`[And <IQueryFilter[]>]`: Der logische Ausdruck "UND".</span><span class="sxs-lookup"><span data-stu-id="539b5-165">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="539b5-166">Muss mindestens zwei Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="539b5-166">Must have at least 2 items.</span></span>
  - <span data-ttu-id="539b5-167">`[Dimensions <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für eine Dimension</span><span class="sxs-lookup"><span data-stu-id="539b5-167">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="539b5-168">`Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="539b5-168">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="539b5-169">`Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden</span><span class="sxs-lookup"><span data-stu-id="539b5-169">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="539b5-170">`[Not <IQueryFilter>]`: Der logische Ausdruck "NOT".</span><span class="sxs-lookup"><span data-stu-id="539b5-170">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="539b5-171">`[Or <IQueryFilter[]>]`: Der logische Ausdruck "ODER".</span><span class="sxs-lookup"><span data-stu-id="539b5-171">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="539b5-172">Muss mindestens zwei Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="539b5-172">Must have at least 2 items.</span></span>
  - <span data-ttu-id="539b5-173">`[Tag <IQueryComparisonExpression>]`: Verfügt über Vergleichsausdruck für ein Tag</span><span class="sxs-lookup"><span data-stu-id="539b5-173">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="539b5-174">TAG <IQueryComparisonExpression> : Verfügt über einen Vergleichsausdruck für ein Tag.</span><span class="sxs-lookup"><span data-stu-id="539b5-174">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="539b5-175">`Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="539b5-175">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="539b5-176">`Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden</span><span class="sxs-lookup"><span data-stu-id="539b5-176">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="539b5-177">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="539b5-177">RELATED LINKS</span></span>

