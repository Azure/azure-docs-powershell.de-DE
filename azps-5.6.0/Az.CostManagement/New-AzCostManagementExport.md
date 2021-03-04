---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/new-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
ms.openlocfilehash: bc3ff9c6d27cba92cf29090dda988a27f9e8a50b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947952"
---
# <span data-ttu-id="bf0e7-101">New-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="bf0e7-101">New-AzCostManagementExport</span></span>

## <span data-ttu-id="bf0e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf0e7-102">SYNOPSIS</span></span>
<span data-ttu-id="bf0e7-103">Der Vorgang zum Erstellen oder Aktualisieren eines Exports.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-103">The operation to create or update a export.</span></span>
<span data-ttu-id="bf0e7-104">Für den Aktualisierungsvorgang muss das neueste eTag in der Anforderung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="bf0e7-105">Sie können das neueste eTag abrufen, indem Sie einen Get-Vorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="bf0e7-106">Beim Erstellen eines Vorgangs ist kein eTag erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="bf0e7-107">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf0e7-107">SYNTAX</span></span>

```
New-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bf0e7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf0e7-108">DESCRIPTION</span></span>
<span data-ttu-id="bf0e7-109">Der Vorgang zum Erstellen oder Aktualisieren eines Exports.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-109">The operation to create or update a export.</span></span>
<span data-ttu-id="bf0e7-110">Für den Aktualisierungsvorgang muss das neueste eTag in der Anforderung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-110">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="bf0e7-111">Sie können das neueste eTag abrufen, indem Sie einen Get-Vorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-111">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="bf0e7-112">Beim Erstellen eines Vorgangs ist kein eTag erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-112">Create operation does not require eTag.</span></span>

## <span data-ttu-id="bf0e7-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bf0e7-113">EXAMPLES</span></span>

### <span data-ttu-id="bf0e7-114">Beispiel 1: Erstellen eines AzCostManagementExports</span><span class="sxs-lookup"><span data-stu-id="bf0e7-114">Example 1: Create an AzCostManagementExport</span></span>
```powershell
PS C:\> New-AzCostManagementExport -Scope "subscriptions/***********" -Name "CostManagementExportTest" -ScheduleStatus "Active" -ScheduleRecurrence "Daily" -RecurrencePeriodFrom "2020-10-31T20:00:00Z" -RecurrencePeriodTo "2020-11-30T00:00:00Z" -Format "Csv" -DestinationResourceId "/subscriptions/*************/resourceGroups/ResourceGroupTest/providers/Microsoft.Storage/storageAccounts/storageAccountTest" `  -DestinationContainer "exports" -DestinationRootFolderPath "ad-hoc" -DefinitionType "Usage" -DefinitionTimeframe "MonthToDate" -DatasetGranularity "Daily"

ETag              Name                                      Type
----              ----                                      ----
"********" TestExportDatasetAggregationInfosagdhaghj Microsoft.CostManagement/exports
```

<span data-ttu-id="bf0e7-115">Erstellen eines AzCostManagementExports</span><span class="sxs-lookup"><span data-stu-id="bf0e7-115">Create an AzCostManagementExport</span></span>

## <span data-ttu-id="bf0e7-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bf0e7-116">PARAMETERS</span></span>

### <span data-ttu-id="bf0e7-117">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="bf0e7-117">-ConfigurationColumn</span></span>
<span data-ttu-id="bf0e7-118">Array von Spaltennamen, die in den Export einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-118">Array of column names to be included in the export.</span></span>
<span data-ttu-id="bf0e7-119">Wenn nicht angegeben, enthält der Export alle verfügbaren Spalten.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-119">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="bf0e7-120">Die verfügbaren Spalten können je nach Kundenkanal variieren (siehe Beispiele).</span><span class="sxs-lookup"><span data-stu-id="bf0e7-120">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="bf0e7-121">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="bf0e7-121">-DataSetGranularity</span></span>
<span data-ttu-id="bf0e7-122">Die Granularität der Zeilen im Export.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-122">The granularity of rows in the export.</span></span>
<span data-ttu-id="bf0e7-123">Derzeit wird nur "Täglich" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-123">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="bf0e7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf0e7-124">-DefaultProfile</span></span>
<span data-ttu-id="bf0e7-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf0e7-126">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="bf0e7-126">-DefinitionTimeframe</span></span>
<span data-ttu-id="bf0e7-127">Der Zeitrahmen für das Ziehen von Daten für den Export.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-127">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="bf0e7-128">Wenn benutzerdefiniert, muss ein bestimmter Zeitraum angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-128">If custom, then a specific time period must be provided.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.TimeframeType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0e7-129">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="bf0e7-129">-DefinitionType</span></span>
<span data-ttu-id="bf0e7-130">Der Typ des Exports.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-130">The type of the export.</span></span>
<span data-ttu-id="bf0e7-131">Beachten Sie, dass "Nutzung" dem Wert "ActualCost" entspricht und für Exporte gilt, die noch keine Daten für Gebühren oder Abschreibungen für Dienstreservierungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-131">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExportType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0e7-132">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="bf0e7-132">-DestinationContainer</span></span>
<span data-ttu-id="bf0e7-133">Der Name des Containers, in den exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-133">The name of the container where exports will be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0e7-134">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="bf0e7-134">-DestinationResourceId</span></span>
<span data-ttu-id="bf0e7-135">Die Ressourcen-ID des Speicherkontos, in dem Exporte geliefert werden.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-135">The resource id of the storage account where exports will be delivered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0e7-136">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="bf0e7-136">-DestinationRootFolderPath</span></span>
<span data-ttu-id="bf0e7-137">Der Name des Verzeichnisses, in das exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-137">The name of the directory where exports will be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0e7-138">-Format</span><span class="sxs-lookup"><span data-stu-id="bf0e7-138">-Format</span></span>
<span data-ttu-id="bf0e7-139">Das Format des zugestellten Exports.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-139">The format of the export being delivered.</span></span>
<span data-ttu-id="bf0e7-140">Derzeit wird nur "Csv" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-140">Currently only 'Csv' is supported.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.FormatType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0e7-141">-Name</span><span class="sxs-lookup"><span data-stu-id="bf0e7-141">-Name</span></span>
<span data-ttu-id="bf0e7-142">Exportname.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-142">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0e7-143">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="bf0e7-143">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="bf0e7-144">Das Startdatum der Serie.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-144">The start date of recurrence.</span></span>

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

### <span data-ttu-id="bf0e7-145">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="bf0e7-145">-RecurrencePeriodTo</span></span>
<span data-ttu-id="bf0e7-146">Das Enddatum der Serie.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-146">The end date of recurrence.</span></span>

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

### <span data-ttu-id="bf0e7-147">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="bf0e7-147">-ScheduleRecurrence</span></span>
<span data-ttu-id="bf0e7-148">Die Terminserie.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-148">The schedule recurrence.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.RecurrenceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0e7-149">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="bf0e7-149">-ScheduleStatus</span></span>
<span data-ttu-id="bf0e7-150">Der Status des Exportzeitplans.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-150">The status of the export's schedule.</span></span>
<span data-ttu-id="bf0e7-151">Wenn "Inaktiv" angezeigt wird, wird der Exportzeitplan angehalten.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-151">If 'Inactive', the export's schedule is paused.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.StatusType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0e7-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="bf0e7-152">-Scope</span></span>
<span data-ttu-id="bf0e7-153">Dieser Parameter definiert den Umfang des Kostenmanagements aus verschiedenen Perspektiven : "Abonnement", "Ressourcengruppe" und "Dienst bereitstellen".</span><span class="sxs-lookup"><span data-stu-id="bf0e7-153">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="bf0e7-154">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="bf0e7-154">-TimePeriodFrom</span></span>
<span data-ttu-id="bf0e7-155">Das Startdatum für den Export von Daten.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-155">The start date for export data.</span></span>

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

### <span data-ttu-id="bf0e7-156">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="bf0e7-156">-TimePeriodTo</span></span>
<span data-ttu-id="bf0e7-157">Das Enddatum für den Export von Daten.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-157">The end date for export data.</span></span>

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

### <span data-ttu-id="bf0e7-158">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bf0e7-158">-Confirm</span></span>
<span data-ttu-id="bf0e7-159">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf0e7-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf0e7-160">-WhatIf</span></span>
<span data-ttu-id="bf0e7-161">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf0e7-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf0e7-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf0e7-163">CommonParameters</span></span>
<span data-ttu-id="bf0e7-164">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf0e7-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf0e7-165">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf0e7-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf0e7-166">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bf0e7-166">INPUTS</span></span>

## <span data-ttu-id="bf0e7-167">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bf0e7-167">OUTPUTS</span></span>

### <span data-ttu-id="bf0e7-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="bf0e7-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="bf0e7-169">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bf0e7-169">NOTES</span></span>

<span data-ttu-id="bf0e7-170">ALIASE</span><span class="sxs-lookup"><span data-stu-id="bf0e7-170">ALIASES</span></span>

## <span data-ttu-id="bf0e7-171">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bf0e7-171">RELATED LINKS</span></span>

