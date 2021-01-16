---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/invoke-azcostmanagementquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
ms.openlocfilehash: 1eec241ab9fba3f9e8daa3218b65140d644d56ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295078"
---
# <span data-ttu-id="f4347-101">Invoke-AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="f4347-101">Invoke-AzCostManagementQuery</span></span>

## <span data-ttu-id="f4347-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4347-102">SYNOPSIS</span></span>
<span data-ttu-id="f4347-103">Abfragen der Verwendungsdaten für den definierten Bereich</span><span class="sxs-lookup"><span data-stu-id="f4347-103">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="f4347-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4347-104">SYNTAX</span></span>

### <span data-ttu-id="f4347-105">UsageExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4347-105">UsageExpanded (Default)</span></span>
```
Invoke-AzCostManagementQuery -Scope <String> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f4347-106">UsageExpanded1</span><span class="sxs-lookup"><span data-stu-id="f4347-106">UsageExpanded1</span></span>
```
Invoke-AzCostManagementQuery -ExternalCloudProviderId <String>
 -ExternalCloudProviderType <ExternalCloudProviderType> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f4347-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4347-107">DESCRIPTION</span></span>
<span data-ttu-id="f4347-108">Abfragen der Verwendungsdaten für den definierten Bereich</span><span class="sxs-lookup"><span data-stu-id="f4347-108">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="f4347-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f4347-109">EXAMPLES</span></span>

### <span data-ttu-id="f4347-110">Beispiel 1: Aufrufen von AzCostManagementQuery nach Bereich</span><span class="sxs-lookup"><span data-stu-id="f4347-110">Example 1: Invoke AzCostManagementQuery by Scope</span></span>
```powershell
PS C:\> Invoke-AzCostManagementQuery -Scope "/subscriptions/***********" -Timeframe MonthToDate -Type Usage -DatasetGranularity 'Daily'

Column                Row
------                ---
{UsageDate, Currency} {20201101 USD, 20201102 USD, 20201103 USD, 20201104 USD…}
```

<span data-ttu-id="f4347-111">Aufrufen von AzCostManagementQuery nach Bereich</span><span class="sxs-lookup"><span data-stu-id="f4347-111">Invoke AzCostManagementQuery by Scope</span></span>

### <span data-ttu-id="f4347-112">Beispiel 2: Aufrufen von AzCostManagementQuery nach Bereich mit Dimensionen</span><span class="sxs-lookup"><span data-stu-id="f4347-112">Example 2: Invoke AzCostManagementQuery by Scope with Dimensions</span></span>
```powershell
PS C:\> $dimensions = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceGroup' -Operator 'In' -Value 'API'
$filter = New-AzCostManagementQueryFilterObject -Dimensions $dimensions
Invoke-AzCostManagementQuery -Type Usage -Scope "subscriptions/***********" -DatasetGranularity 'Monthly' -DatasetFilter $filter -Timeframe MonthToDate -Debug


Column                   Row
------                   ---
{BillingMonth, Currency} {}
```

<span data-ttu-id="f4347-113">Aufrufen von AzCostManagementQuery nach Bereich mit Dimensionen</span><span class="sxs-lookup"><span data-stu-id="f4347-113">Invoke AzCostManagementQuery by Scope with Dimensions</span></span>

## <span data-ttu-id="f4347-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4347-114">PARAMETERS</span></span>

### <span data-ttu-id="f4347-115">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="f4347-115">-ConfigurationColumn</span></span>
<span data-ttu-id="f4347-116">Array von Spaltennamen, die in die Abfrage eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f4347-116">Array of column names to be included in the query.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4347-117">-DatasetAggregation</span><span class="sxs-lookup"><span data-stu-id="f4347-117">-DatasetAggregation</span></span>
<span data-ttu-id="f4347-118">Wörterbuch des Aggregationsausdrucks, der in der Abfrage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f4347-118">Dictionary of aggregation expression to use in the query.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4347-119">-DatasetFilter</span><span class="sxs-lookup"><span data-stu-id="f4347-119">-DatasetFilter</span></span>
<span data-ttu-id="f4347-120">Verfügt über einen Filterausdruck, der in der Abfrage verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4347-120">Has filter expression to use in the query.</span></span>
<span data-ttu-id="f4347-121">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f4347-121">To construct, see NOTES section for DATASETFILTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="f4347-122">-DatasetDataUlarity</span><span class="sxs-lookup"><span data-stu-id="f4347-122">-DatasetGranularity</span></span>
<span data-ttu-id="f4347-123">Die Granularität der Zeilen in der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="f4347-123">The granularity of rows in the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.GranularityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4347-124">-DatasetGrouping</span><span class="sxs-lookup"><span data-stu-id="f4347-124">-DatasetGrouping</span></span>
<span data-ttu-id="f4347-125">Array von "Gruppieren nach Ausdruck", das in der Abfrage verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4347-125">Array of group by expression to use in the query.</span></span>
<span data-ttu-id="f4347-126">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f4347-126">To construct, see NOTES section for DATASETGROUPING properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryGrouping[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4347-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4347-127">-DefaultProfile</span></span>
<span data-ttu-id="f4347-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f4347-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4347-129">-ExternalCloudProviderId</span><span class="sxs-lookup"><span data-stu-id="f4347-129">-ExternalCloudProviderId</span></span>
<span data-ttu-id="f4347-130">Dies kann "{externalSubscriptionId}" für verknüpftes Konto oder "{externalBillingAccountId}" für konsolidiertes Konto sein, das für Dimensions-/Abfragevorgänge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f4347-130">This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>

```yaml
Type: System.String
Parameter Sets: UsageExpanded1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4347-131">-ExternalCloudProviderType</span><span class="sxs-lookup"><span data-stu-id="f4347-131">-ExternalCloudProviderType</span></span>
<span data-ttu-id="f4347-132">Der mit Dimensions-/Abfragevorgängen verknüpfte externe Cloudanbietertyp.</span><span class="sxs-lookup"><span data-stu-id="f4347-132">The external cloud provider type associated with dimension/query operations.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExternalCloudProviderType
Parameter Sets: UsageExpanded1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4347-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="f4347-133">-Scope</span></span>
<span data-ttu-id="f4347-134">Dazu gehören "subscriptions/{subscriptionId}/" für den Abonnementbereich, "subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}" für den Ressourcengruppenbereich, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId} for Management Group scope, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}" für billingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}' für invoiceSection scope und 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}' speziell für Partner.</span><span class="sxs-lookup"><span data-stu-id="f4347-134">This includes 'subscriptions/{subscriptionId}/' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId} for Management Group scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for billingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}' for invoiceSection scope, and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}' specific for partners.</span></span>

```yaml
Type: System.String
Parameter Sets: UsageExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4347-135">-Timeframe</span><span class="sxs-lookup"><span data-stu-id="f4347-135">-Timeframe</span></span>
<span data-ttu-id="f4347-136">Der Zeitrahmen für das Pulling von Daten für die Abfrage.</span><span class="sxs-lookup"><span data-stu-id="f4347-136">The time frame for pulling data for the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.TimeframeType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4347-137">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="f4347-137">-TimePeriodFrom</span></span>
<span data-ttu-id="f4347-138">Das Startdatum, von dem Daten ab pullt werden.</span><span class="sxs-lookup"><span data-stu-id="f4347-138">The start date to pull data from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4347-139">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="f4347-139">-TimePeriodTo</span></span>
<span data-ttu-id="f4347-140">Das Enddatum, an das daten pullt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4347-140">The end date to pull data to.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4347-141">-Type</span><span class="sxs-lookup"><span data-stu-id="f4347-141">-Type</span></span>
<span data-ttu-id="f4347-142">Der Typ der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="f4347-142">The type of the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExportType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4347-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4347-143">-Confirm</span></span>
<span data-ttu-id="f4347-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4347-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4347-145">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f4347-145">-WhatIf</span></span>
<span data-ttu-id="f4347-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4347-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4347-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4347-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4347-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4347-148">CommonParameters</span></span>
<span data-ttu-id="f4347-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4347-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4347-150">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4347-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4347-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f4347-151">INPUTS</span></span>

## <span data-ttu-id="f4347-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f4347-152">OUTPUTS</span></span>

### <span data-ttu-id="f4347-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryResult</span><span class="sxs-lookup"><span data-stu-id="f4347-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryResult</span></span>

## <span data-ttu-id="f4347-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f4347-154">NOTES</span></span>

<span data-ttu-id="f4347-155">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f4347-155">ALIASES</span></span>

<span data-ttu-id="f4347-156">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="f4347-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f4347-157">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f4347-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f4347-158">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f4347-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f4347-159">DATASETFILTER <IQueryFilter> : Verfügt über einen Filterausdruck, der in der Abfrage verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4347-159">DATASETFILTER <IQueryFilter>: Has filter expression to use in the query.</span></span>
  - <span data-ttu-id="f4347-160">`[And <IQueryFilter[]>]`: Der logische Ausdruck "UND".</span><span class="sxs-lookup"><span data-stu-id="f4347-160">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="f4347-161">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="f4347-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="f4347-162">`[Dimensions <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für eine Dimension</span><span class="sxs-lookup"><span data-stu-id="f4347-162">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="f4347-163">`Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4347-163">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="f4347-164">`Operator <OperatorType>`: Der zum Vergleich zu verwendende Operator.</span><span class="sxs-lookup"><span data-stu-id="f4347-164">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="f4347-165">`Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f4347-165">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="f4347-166">`[Not <IQueryFilter>]`: Der logische Ausdruck "NICHT".</span><span class="sxs-lookup"><span data-stu-id="f4347-166">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="f4347-167">`[Or <IQueryFilter[]>]`: Der logische Ausdruck "ODER".</span><span class="sxs-lookup"><span data-stu-id="f4347-167">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="f4347-168">Mindestens zwei Elemente müssen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="f4347-168">Must have at least 2 items.</span></span>
  - <span data-ttu-id="f4347-169">`[Tag <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für ein Tag</span><span class="sxs-lookup"><span data-stu-id="f4347-169">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="f4347-170">DATASETGROUPING <IQueryGrouping[]>: Array der Gruppe nach Ausdruck, die in der Abfrage verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4347-170">DATASETGROUPING <IQueryGrouping[]>: Array of group by expression to use in the query.</span></span>
  - <span data-ttu-id="f4347-171">`Name <String>`: Der Name der zu gruppierende Spalte.</span><span class="sxs-lookup"><span data-stu-id="f4347-171">`Name <String>`: The name of the column to group.</span></span>
  - <span data-ttu-id="f4347-172">`Type <QueryColumnType>`: Hat den Typ der zu gruppierende Spalte.</span><span class="sxs-lookup"><span data-stu-id="f4347-172">`Type <QueryColumnType>`: Has type of the column to group.</span></span>

## <span data-ttu-id="f4347-173">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f4347-173">RELATED LINKS</span></span>

