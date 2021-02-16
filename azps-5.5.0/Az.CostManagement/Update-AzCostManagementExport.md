---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/update-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
ms.openlocfilehash: 310600555f36fa0f6b129f2cf2a84581ffad044b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148388"
---
# <span data-ttu-id="36c31-101">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="36c31-101">Update-AzCostManagementExport</span></span>

## <span data-ttu-id="36c31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36c31-102">SYNOPSIS</span></span>
<span data-ttu-id="36c31-103">Der Vorgang zum Erstellen oder Aktualisieren eines Exports.</span><span class="sxs-lookup"><span data-stu-id="36c31-103">The operation to create or update a export.</span></span>
<span data-ttu-id="36c31-104">Für den Aktualisierungsvorgang muss das neueste eTag in der Anforderung festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="36c31-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="36c31-105">Sie können das neueste eTag abrufen, indem Sie einen Get-Vorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="36c31-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="36c31-106">Für den Erstellungsvorgang ist kein eTag erforderlich.</span><span class="sxs-lookup"><span data-stu-id="36c31-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="36c31-107">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36c31-107">SYNTAX</span></span>

### <span data-ttu-id="36c31-108">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="36c31-108">UpdateExpanded (Default)</span></span>
```
Update-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="36c31-109">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="36c31-109">UpdateViaIdentityExpanded</span></span>
```
Update-AzCostManagementExport -InputObject <ICostManagementIdentity> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="36c31-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36c31-110">DESCRIPTION</span></span>
<span data-ttu-id="36c31-111">Der Vorgang zum Erstellen oder Aktualisieren eines Exports.</span><span class="sxs-lookup"><span data-stu-id="36c31-111">The operation to create or update a export.</span></span>
<span data-ttu-id="36c31-112">Für den Aktualisierungsvorgang muss das neueste eTag in der Anforderung festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="36c31-112">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="36c31-113">Sie können das neueste eTag abrufen, indem Sie einen Get-Vorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="36c31-113">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="36c31-114">Für den Erstellungsvorgang ist kein eTag erforderlich.</span><span class="sxs-lookup"><span data-stu-id="36c31-114">Create operation does not require eTag.</span></span>

## <span data-ttu-id="36c31-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="36c31-115">EXAMPLES</span></span>

### <span data-ttu-id="36c31-116">Beispiel 1: Aktualisieren von AzCostManagementExport nach Bereich und Name</span><span class="sxs-lookup"><span data-stu-id="36c31-116">Example 1: Update AzCostManagementExport by scope and name</span></span>
```powershell
PS C:\> Update-AzCostManagementExport -Scope "subscriptions//*********" -Name "TestExport" -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="36c31-117">Aktualisieren von AzCostManagementExport nach Bereich und Name</span><span class="sxs-lookup"><span data-stu-id="36c31-117">Update AzCostManagementExport by Scope and name</span></span>

### <span data-ttu-id="36c31-118">Beispiel 2: Aktualisieren von AzCostManagementExport von InputObject</span><span class="sxs-lookup"><span data-stu-id="36c31-118">Example 2: Update AzCostManagementExport by InputObject</span></span>
```powershell
PS C:\> $oldExport = Get-AzCostManagementExport -Scope "subscriptions/*********" -Name "TestExport"
Update-AzCostManagementExport -InputObject $oldExport -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="36c31-119">Aktualisieren von AzCostManagementExport von InputObject</span><span class="sxs-lookup"><span data-stu-id="36c31-119">Update AzCostManagementExport by InputObject</span></span>

## <span data-ttu-id="36c31-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36c31-120">PARAMETERS</span></span>

### <span data-ttu-id="36c31-121">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="36c31-121">-ConfigurationColumn</span></span>
<span data-ttu-id="36c31-122">Array von Spaltennamen, die in den Export einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="36c31-122">Array of column names to be included in the export.</span></span>
<span data-ttu-id="36c31-123">Wenn nicht angegeben, enthält der Export alle verfügbaren Spalten.</span><span class="sxs-lookup"><span data-stu-id="36c31-123">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="36c31-124">Die verfügbaren Spalten können je nach Kundenkanal variieren (siehe Beispiele).</span><span class="sxs-lookup"><span data-stu-id="36c31-124">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="36c31-125">-DataSetUlarity</span><span class="sxs-lookup"><span data-stu-id="36c31-125">-DataSetGranularity</span></span>
<span data-ttu-id="36c31-126">Die Granularität der Zeilen im Export.</span><span class="sxs-lookup"><span data-stu-id="36c31-126">The granularity of rows in the export.</span></span>
<span data-ttu-id="36c31-127">Derzeit wird nur "Täglich" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="36c31-127">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="36c31-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36c31-128">-DefaultProfile</span></span>
<span data-ttu-id="36c31-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36c31-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36c31-130">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="36c31-130">-DefinitionTimeframe</span></span>
<span data-ttu-id="36c31-131">Der Zeitrahmen für das Pulling von Daten für den Export.</span><span class="sxs-lookup"><span data-stu-id="36c31-131">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="36c31-132">Wenn benutzerdefiniert, muss ein bestimmter Zeitraum angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="36c31-132">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="36c31-133">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="36c31-133">-DefinitionType</span></span>
<span data-ttu-id="36c31-134">Der Typ des Exports.</span><span class="sxs-lookup"><span data-stu-id="36c31-134">The type of the export.</span></span>
<span data-ttu-id="36c31-135">Beachten Sie, dass die Nutzung dem Wert "ActualCost" entspricht und für Exporte gilt, die noch keine Daten zu Gebühren oder Abschreibungen für Dienstreservierungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="36c31-135">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="36c31-136">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="36c31-136">-DestinationContainer</span></span>
<span data-ttu-id="36c31-137">Der Name des Containers, in den die Exporte hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="36c31-137">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="36c31-138">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="36c31-138">-DestinationResourceId</span></span>
<span data-ttu-id="36c31-139">Die Ressourcen-ID des Speicherkontos, für das Exporte geliefert werden.</span><span class="sxs-lookup"><span data-stu-id="36c31-139">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="36c31-140">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="36c31-140">-DestinationRootFolderPath</span></span>
<span data-ttu-id="36c31-141">Der Name des Verzeichnisses, in das Exporte hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="36c31-141">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="36c31-142">-ETag</span><span class="sxs-lookup"><span data-stu-id="36c31-142">-ETag</span></span>
<span data-ttu-id="36c31-143">eTag der Ressource.</span><span class="sxs-lookup"><span data-stu-id="36c31-143">eTag of the resource.</span></span>
<span data-ttu-id="36c31-144">Um Szenarien für gleichzeitige Updates zu behandeln, wird dieses Feld verwendet, um festzustellen, ob der Benutzer die neueste Version aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="36c31-144">To handle concurrent update scenario, this field will be used to determine whether the user is updating the latest version or not.</span></span>

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

### <span data-ttu-id="36c31-145">-Format</span><span class="sxs-lookup"><span data-stu-id="36c31-145">-Format</span></span>
<span data-ttu-id="36c31-146">Das Format des zu liefernde Exports.</span><span class="sxs-lookup"><span data-stu-id="36c31-146">The format of the export being delivered.</span></span>
<span data-ttu-id="36c31-147">Derzeit wird nur "CSV" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="36c31-147">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="36c31-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36c31-148">-InputObject</span></span>
<span data-ttu-id="36c31-149">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="36c31-149">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36c31-150">-Name</span><span class="sxs-lookup"><span data-stu-id="36c31-150">-Name</span></span>
<span data-ttu-id="36c31-151">Exportname.</span><span class="sxs-lookup"><span data-stu-id="36c31-151">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c31-152">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="36c31-152">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="36c31-153">Das Startdatum der Serie.</span><span class="sxs-lookup"><span data-stu-id="36c31-153">The start date of recurrence.</span></span>

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

### <span data-ttu-id="36c31-154">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="36c31-154">-RecurrencePeriodTo</span></span>
<span data-ttu-id="36c31-155">Das Enddatum der Serie.</span><span class="sxs-lookup"><span data-stu-id="36c31-155">The end date of recurrence.</span></span>

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

### <span data-ttu-id="36c31-156">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="36c31-156">-ScheduleRecurrence</span></span>
<span data-ttu-id="36c31-157">Die Terminplanserie.</span><span class="sxs-lookup"><span data-stu-id="36c31-157">The schedule recurrence.</span></span>

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

### <span data-ttu-id="36c31-158">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="36c31-158">-ScheduleStatus</span></span>
<span data-ttu-id="36c31-159">Der Status des Zeitplans für den Export.</span><span class="sxs-lookup"><span data-stu-id="36c31-159">The status of the export's schedule.</span></span>
<span data-ttu-id="36c31-160">Wenn "Inaktiv" angezeigt wird, wird der Zeitplan des Exports angehalten.</span><span class="sxs-lookup"><span data-stu-id="36c31-160">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="36c31-161">-Scope</span><span class="sxs-lookup"><span data-stu-id="36c31-161">-Scope</span></span>
<span data-ttu-id="36c31-162">Dieser Parameter definiert den Umfang der Kostenmanagement aus unterschiedlichen Perspektiven wie "Abonnement", "Ressourcengruppe" und "Dienst bereitstellen".</span><span class="sxs-lookup"><span data-stu-id="36c31-162">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c31-163">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="36c31-163">-TimePeriodFrom</span></span>
<span data-ttu-id="36c31-164">Das Startdatum für den Export von Daten.</span><span class="sxs-lookup"><span data-stu-id="36c31-164">The start date for export data.</span></span>

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

### <span data-ttu-id="36c31-165">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="36c31-165">-TimePeriodTo</span></span>
<span data-ttu-id="36c31-166">Das Enddatum für den Export von Daten.</span><span class="sxs-lookup"><span data-stu-id="36c31-166">The end date for export data.</span></span>

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

### <span data-ttu-id="36c31-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36c31-167">-Confirm</span></span>
<span data-ttu-id="36c31-168">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="36c31-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36c31-169">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="36c31-169">-WhatIf</span></span>
<span data-ttu-id="36c31-170">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="36c31-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36c31-171">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="36c31-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36c31-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36c31-172">CommonParameters</span></span>
<span data-ttu-id="36c31-173">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36c31-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36c31-174">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36c31-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36c31-175">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="36c31-175">INPUTS</span></span>

### <span data-ttu-id="36c31-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="36c31-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="36c31-177">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="36c31-177">OUTPUTS</span></span>

### <span data-ttu-id="36c31-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="36c31-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="36c31-179">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="36c31-179">NOTES</span></span>

<span data-ttu-id="36c31-180">ALIASE</span><span class="sxs-lookup"><span data-stu-id="36c31-180">ALIASES</span></span>

<span data-ttu-id="36c31-181">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="36c31-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="36c31-182">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="36c31-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="36c31-183">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="36c31-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="36c31-184">INPUTOBJECT <ICostManagementIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="36c31-184">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="36c31-185">`[AlertId <String>]`: Benachrichtigungs-ID</span><span class="sxs-lookup"><span data-stu-id="36c31-185">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="36c31-186">`[ExportName <String>]`: Name exportieren.</span><span class="sxs-lookup"><span data-stu-id="36c31-186">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="36c31-187">`[ExternalCloudProviderId <String>]`: Dies kann "{externalSubscriptionId}" für verknüpftes Konto oder "{externalBillingAccountId}" für konsolidiertes Konto sein, das für Dimensions-/Abfragevorgänge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="36c31-187">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="36c31-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Der externe Cloudanbietertyp, der Dimensions-/Abfragevorgängen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="36c31-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="36c31-189">Dies schließt "externalSubscriptions" für verknüpfte Konten und "externalBillingAccounts" für konsolidierte Konten ein.</span><span class="sxs-lookup"><span data-stu-id="36c31-189">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="36c31-190">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="36c31-190">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="36c31-191">`[Scope <String>]`: Der Bereich, der Ansichtsvorgängen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="36c31-191">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="36c31-192">Dies schließt "subscriptions/{subscriptionId}" für den Abonnementbereich ein, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management /managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span><span class="sxs-lookup"><span data-stu-id="36c31-192">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="36c31-193">`[ViewName <String>]`: Anzeigename</span><span class="sxs-lookup"><span data-stu-id="36c31-193">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="36c31-194">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="36c31-194">RELATED LINKS</span></span>

