---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/new-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
ms.openlocfilehash: edc0475a9d4299e1bd7346ab441a78b09905d59c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163913"
---
# <span data-ttu-id="d27a3-101">New-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="d27a3-101">New-AzCostManagementExport</span></span>

## <span data-ttu-id="d27a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d27a3-102">SYNOPSIS</span></span>
<span data-ttu-id="d27a3-103">Der Vorgang zum Erstellen oder Aktualisieren eines Exports.</span><span class="sxs-lookup"><span data-stu-id="d27a3-103">The operation to create or update a export.</span></span>
<span data-ttu-id="d27a3-104">Für den Aktualisierungsvorgang muss das neueste eTag in der Anforderung festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="d27a3-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="d27a3-105">Sie können das neueste eTag abrufen, indem Sie einen Get-Vorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="d27a3-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="d27a3-106">Für den Erstellungsvorgang ist kein eTag erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d27a3-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="d27a3-107">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d27a3-107">SYNTAX</span></span>

```
New-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d27a3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d27a3-108">DESCRIPTION</span></span>
<span data-ttu-id="d27a3-109">Der Vorgang zum Erstellen oder Aktualisieren eines Exports.</span><span class="sxs-lookup"><span data-stu-id="d27a3-109">The operation to create or update a export.</span></span>
<span data-ttu-id="d27a3-110">Für den Aktualisierungsvorgang muss das neueste eTag in der Anforderung festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="d27a3-110">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="d27a3-111">Sie können das neueste eTag abrufen, indem Sie einen Get-Vorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="d27a3-111">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="d27a3-112">Für den Erstellungsvorgang ist kein eTag erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d27a3-112">Create operation does not require eTag.</span></span>

## <span data-ttu-id="d27a3-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d27a3-113">EXAMPLES</span></span>

### <span data-ttu-id="d27a3-114">Beispiel 1: Erstellen eines AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="d27a3-114">Example 1: Create an AzCostManagementExport</span></span>
```powershell
PS C:\> New-AzCostManagementExport -Scope "subscriptions/***********" -Name "CostManagementExportTest" -ScheduleStatus "Active" -ScheduleRecurrence "Daily" -RecurrencePeriodFrom "2020-10-31T20:00:00Z" -RecurrencePeriodTo "2020-11-30T00:00:00Z" -Format "Csv" -DestinationResourceId "/subscriptions/*************/resourceGroups/ResourceGroupTest/providers/Microsoft.Storage/storageAccounts/storageAccountTest" `  -DestinationContainer "exports" -DestinationRootFolderPath "ad-hoc" -DefinitionType "Usage" -DefinitionTimeframe "MonthToDate" -DatasetGranularity "Daily"

ETag              Name                                      Type
----              ----                                      ----
"********" TestExportDatasetAggregationInfosagdhaghj Microsoft.CostManagement/exports
```

<span data-ttu-id="d27a3-115">Erstellen eines AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="d27a3-115">Create an AzCostManagementExport</span></span>

## <span data-ttu-id="d27a3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d27a3-116">PARAMETERS</span></span>

### <span data-ttu-id="d27a3-117">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="d27a3-117">-ConfigurationColumn</span></span>
<span data-ttu-id="d27a3-118">Array von Spaltennamen, die in den Export einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d27a3-118">Array of column names to be included in the export.</span></span>
<span data-ttu-id="d27a3-119">Wenn nicht angegeben, enthält der Export alle verfügbaren Spalten.</span><span class="sxs-lookup"><span data-stu-id="d27a3-119">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="d27a3-120">Die verfügbaren Spalten können je nach Kundenkanal variieren (siehe Beispiele).</span><span class="sxs-lookup"><span data-stu-id="d27a3-120">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="d27a3-121">-DataSetUlarity</span><span class="sxs-lookup"><span data-stu-id="d27a3-121">-DataSetGranularity</span></span>
<span data-ttu-id="d27a3-122">Die Granularität der Zeilen im Export.</span><span class="sxs-lookup"><span data-stu-id="d27a3-122">The granularity of rows in the export.</span></span>
<span data-ttu-id="d27a3-123">Derzeit wird nur "Täglich" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d27a3-123">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="d27a3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d27a3-124">-DefaultProfile</span></span>
<span data-ttu-id="d27a3-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d27a3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d27a3-126">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="d27a3-126">-DefinitionTimeframe</span></span>
<span data-ttu-id="d27a3-127">Der Zeitrahmen für das Pulling von Daten für den Export.</span><span class="sxs-lookup"><span data-stu-id="d27a3-127">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="d27a3-128">Wenn benutzerdefiniert, muss ein bestimmter Zeitraum angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d27a3-128">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="d27a3-129">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="d27a3-129">-DefinitionType</span></span>
<span data-ttu-id="d27a3-130">Der Typ des Exports.</span><span class="sxs-lookup"><span data-stu-id="d27a3-130">The type of the export.</span></span>
<span data-ttu-id="d27a3-131">Beachten Sie, dass die Nutzung dem Wert "ActualCost" entspricht und für Exporte gilt, die noch keine Daten zu Gebühren oder Abschreibungen für Dienstreservierungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d27a3-131">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="d27a3-132">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="d27a3-132">-DestinationContainer</span></span>
<span data-ttu-id="d27a3-133">Der Name des Containers, in den die Exporte hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="d27a3-133">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="d27a3-134">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="d27a3-134">-DestinationResourceId</span></span>
<span data-ttu-id="d27a3-135">Die Ressourcen-ID des Speicherkontos, für das Exporte geliefert werden.</span><span class="sxs-lookup"><span data-stu-id="d27a3-135">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="d27a3-136">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="d27a3-136">-DestinationRootFolderPath</span></span>
<span data-ttu-id="d27a3-137">Der Name des Verzeichnisses, in das Exporte hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="d27a3-137">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="d27a3-138">-Format</span><span class="sxs-lookup"><span data-stu-id="d27a3-138">-Format</span></span>
<span data-ttu-id="d27a3-139">Das Format des zu liefernde Exports.</span><span class="sxs-lookup"><span data-stu-id="d27a3-139">The format of the export being delivered.</span></span>
<span data-ttu-id="d27a3-140">Derzeit wird nur "CSV" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d27a3-140">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="d27a3-141">-Name</span><span class="sxs-lookup"><span data-stu-id="d27a3-141">-Name</span></span>
<span data-ttu-id="d27a3-142">Exportname.</span><span class="sxs-lookup"><span data-stu-id="d27a3-142">Export Name.</span></span>

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

### <span data-ttu-id="d27a3-143">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="d27a3-143">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="d27a3-144">Das Startdatum der Serie.</span><span class="sxs-lookup"><span data-stu-id="d27a3-144">The start date of recurrence.</span></span>

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

### <span data-ttu-id="d27a3-145">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="d27a3-145">-RecurrencePeriodTo</span></span>
<span data-ttu-id="d27a3-146">Das Enddatum der Serie.</span><span class="sxs-lookup"><span data-stu-id="d27a3-146">The end date of recurrence.</span></span>

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

### <span data-ttu-id="d27a3-147">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="d27a3-147">-ScheduleRecurrence</span></span>
<span data-ttu-id="d27a3-148">Die Terminplanserie.</span><span class="sxs-lookup"><span data-stu-id="d27a3-148">The schedule recurrence.</span></span>

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

### <span data-ttu-id="d27a3-149">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="d27a3-149">-ScheduleStatus</span></span>
<span data-ttu-id="d27a3-150">Der Status des Zeitplans für den Export.</span><span class="sxs-lookup"><span data-stu-id="d27a3-150">The status of the export's schedule.</span></span>
<span data-ttu-id="d27a3-151">Wenn "Inaktiv" angezeigt wird, wird der Zeitplan des Exports angehalten.</span><span class="sxs-lookup"><span data-stu-id="d27a3-151">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="d27a3-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="d27a3-152">-Scope</span></span>
<span data-ttu-id="d27a3-153">Dieser Parameter definiert den Umfang der Kostenmanagement aus unterschiedlichen Perspektiven wie "Abonnement", "Ressourcengruppe" und "Dienst bereitstellen".</span><span class="sxs-lookup"><span data-stu-id="d27a3-153">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="d27a3-154">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="d27a3-154">-TimePeriodFrom</span></span>
<span data-ttu-id="d27a3-155">Das Startdatum für den Export von Daten.</span><span class="sxs-lookup"><span data-stu-id="d27a3-155">The start date for export data.</span></span>

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

### <span data-ttu-id="d27a3-156">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="d27a3-156">-TimePeriodTo</span></span>
<span data-ttu-id="d27a3-157">Das Enddatum für den Export von Daten.</span><span class="sxs-lookup"><span data-stu-id="d27a3-157">The end date for export data.</span></span>

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

### <span data-ttu-id="d27a3-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d27a3-158">-Confirm</span></span>
<span data-ttu-id="d27a3-159">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d27a3-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d27a3-160">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d27a3-160">-WhatIf</span></span>
<span data-ttu-id="d27a3-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d27a3-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d27a3-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d27a3-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d27a3-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d27a3-163">CommonParameters</span></span>
<span data-ttu-id="d27a3-164">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d27a3-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d27a3-165">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d27a3-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d27a3-166">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d27a3-166">INPUTS</span></span>

## <span data-ttu-id="d27a3-167">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d27a3-167">OUTPUTS</span></span>

### <span data-ttu-id="d27a3-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="d27a3-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="d27a3-169">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d27a3-169">NOTES</span></span>

<span data-ttu-id="d27a3-170">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d27a3-170">ALIASES</span></span>

## <span data-ttu-id="d27a3-171">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d27a3-171">RELATED LINKS</span></span>

