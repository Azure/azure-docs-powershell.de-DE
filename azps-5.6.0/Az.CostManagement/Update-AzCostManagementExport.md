---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/update-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
ms.openlocfilehash: d4be10cf33952b026ceabe6cd407929acbe5c058
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918987"
---
# <span data-ttu-id="32264-101">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="32264-101">Update-AzCostManagementExport</span></span>

## <span data-ttu-id="32264-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32264-102">SYNOPSIS</span></span>
<span data-ttu-id="32264-103">Der Vorgang zum Erstellen oder Aktualisieren eines Exports.</span><span class="sxs-lookup"><span data-stu-id="32264-103">The operation to create or update a export.</span></span>
<span data-ttu-id="32264-104">Für den Aktualisierungsvorgang muss das neueste eTag in der Anforderung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="32264-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="32264-105">Sie können das neueste eTag abrufen, indem Sie einen Get-Vorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="32264-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="32264-106">Beim Erstellen eines Vorgangs ist kein eTag erforderlich.</span><span class="sxs-lookup"><span data-stu-id="32264-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="32264-107">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32264-107">SYNTAX</span></span>

### <span data-ttu-id="32264-108">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="32264-108">UpdateExpanded (Default)</span></span>
```
Update-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="32264-109">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="32264-109">UpdateViaIdentityExpanded</span></span>
```
Update-AzCostManagementExport -InputObject <ICostManagementIdentity> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="32264-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="32264-110">DESCRIPTION</span></span>
<span data-ttu-id="32264-111">Der Vorgang zum Erstellen oder Aktualisieren eines Exports.</span><span class="sxs-lookup"><span data-stu-id="32264-111">The operation to create or update a export.</span></span>
<span data-ttu-id="32264-112">Für den Aktualisierungsvorgang muss das neueste eTag in der Anforderung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="32264-112">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="32264-113">Sie können das neueste eTag abrufen, indem Sie einen Get-Vorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="32264-113">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="32264-114">Beim Erstellen eines Vorgangs ist kein eTag erforderlich.</span><span class="sxs-lookup"><span data-stu-id="32264-114">Create operation does not require eTag.</span></span>

## <span data-ttu-id="32264-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="32264-115">EXAMPLES</span></span>

### <span data-ttu-id="32264-116">Beispiel 1: Aktualisieren von AzCostManagementExport nach Bereich und Name</span><span class="sxs-lookup"><span data-stu-id="32264-116">Example 1: Update AzCostManagementExport by scope and name</span></span>
```powershell
PS C:\> Update-AzCostManagementExport -Scope "subscriptions//*********" -Name "TestExport" -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="32264-117">Aktualisieren von AzCostManagementExport nach Umfang und Name</span><span class="sxs-lookup"><span data-stu-id="32264-117">Update AzCostManagementExport by Scope and name</span></span>

### <span data-ttu-id="32264-118">Beispiel 2: Aktualisieren von AzCostManagementExport by InputObject</span><span class="sxs-lookup"><span data-stu-id="32264-118">Example 2: Update AzCostManagementExport by InputObject</span></span>
```powershell
PS C:\> $oldExport = Get-AzCostManagementExport -Scope "subscriptions/*********" -Name "TestExport"
Update-AzCostManagementExport -InputObject $oldExport -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="32264-119">Aktualisieren von AzCostManagementExport by InputObject</span><span class="sxs-lookup"><span data-stu-id="32264-119">Update AzCostManagementExport by InputObject</span></span>

## <span data-ttu-id="32264-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="32264-120">PARAMETERS</span></span>

### <span data-ttu-id="32264-121">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="32264-121">-ConfigurationColumn</span></span>
<span data-ttu-id="32264-122">Array von Spaltennamen, die in den Export einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="32264-122">Array of column names to be included in the export.</span></span>
<span data-ttu-id="32264-123">Wenn nicht angegeben, enthält der Export alle verfügbaren Spalten.</span><span class="sxs-lookup"><span data-stu-id="32264-123">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="32264-124">Die verfügbaren Spalten können je nach Kundenkanal variieren (siehe Beispiele).</span><span class="sxs-lookup"><span data-stu-id="32264-124">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="32264-125">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="32264-125">-DataSetGranularity</span></span>
<span data-ttu-id="32264-126">Die Granularität der Zeilen im Export.</span><span class="sxs-lookup"><span data-stu-id="32264-126">The granularity of rows in the export.</span></span>
<span data-ttu-id="32264-127">Derzeit wird nur "Täglich" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="32264-127">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="32264-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32264-128">-DefaultProfile</span></span>
<span data-ttu-id="32264-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="32264-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32264-130">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="32264-130">-DefinitionTimeframe</span></span>
<span data-ttu-id="32264-131">Der Zeitrahmen für das Ziehen von Daten für den Export.</span><span class="sxs-lookup"><span data-stu-id="32264-131">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="32264-132">Wenn benutzerdefiniert, muss ein bestimmter Zeitraum angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="32264-132">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="32264-133">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="32264-133">-DefinitionType</span></span>
<span data-ttu-id="32264-134">Der Typ des Exports.</span><span class="sxs-lookup"><span data-stu-id="32264-134">The type of the export.</span></span>
<span data-ttu-id="32264-135">Beachten Sie, dass "Nutzung" dem Wert "ActualCost" entspricht und für Exporte gilt, die noch keine Daten für Gebühren oder Abschreibungen für Dienstreservierungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="32264-135">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="32264-136">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="32264-136">-DestinationContainer</span></span>
<span data-ttu-id="32264-137">Der Name des Containers, in den exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="32264-137">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="32264-138">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="32264-138">-DestinationResourceId</span></span>
<span data-ttu-id="32264-139">Die Ressourcen-ID des Speicherkontos, in dem Exporte geliefert werden.</span><span class="sxs-lookup"><span data-stu-id="32264-139">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="32264-140">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="32264-140">-DestinationRootFolderPath</span></span>
<span data-ttu-id="32264-141">Der Name des Verzeichnisses, in das exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="32264-141">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="32264-142">-ETag</span><span class="sxs-lookup"><span data-stu-id="32264-142">-ETag</span></span>
<span data-ttu-id="32264-143">eTag der Ressource.</span><span class="sxs-lookup"><span data-stu-id="32264-143">eTag of the resource.</span></span>
<span data-ttu-id="32264-144">Zum Behandeln eines Szenarios für gleichzeitiges Update wird dieses Feld verwendet, um festzustellen, ob der Benutzer die neueste Version aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="32264-144">To handle concurrent update scenario, this field will be used to determine whether the user is updating the latest version or not.</span></span>

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

### <span data-ttu-id="32264-145">-Format</span><span class="sxs-lookup"><span data-stu-id="32264-145">-Format</span></span>
<span data-ttu-id="32264-146">Das Format des zugestellten Exports.</span><span class="sxs-lookup"><span data-stu-id="32264-146">The format of the export being delivered.</span></span>
<span data-ttu-id="32264-147">Derzeit wird nur "Csv" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="32264-147">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="32264-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32264-148">-InputObject</span></span>
<span data-ttu-id="32264-149">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="32264-149">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="32264-150">-Name</span><span class="sxs-lookup"><span data-stu-id="32264-150">-Name</span></span>
<span data-ttu-id="32264-151">Exportname.</span><span class="sxs-lookup"><span data-stu-id="32264-151">Export Name.</span></span>

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

### <span data-ttu-id="32264-152">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="32264-152">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="32264-153">Das Startdatum der Serie.</span><span class="sxs-lookup"><span data-stu-id="32264-153">The start date of recurrence.</span></span>

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

### <span data-ttu-id="32264-154">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="32264-154">-RecurrencePeriodTo</span></span>
<span data-ttu-id="32264-155">Das Enddatum der Serie.</span><span class="sxs-lookup"><span data-stu-id="32264-155">The end date of recurrence.</span></span>

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

### <span data-ttu-id="32264-156">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="32264-156">-ScheduleRecurrence</span></span>
<span data-ttu-id="32264-157">Die Terminserie.</span><span class="sxs-lookup"><span data-stu-id="32264-157">The schedule recurrence.</span></span>

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

### <span data-ttu-id="32264-158">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="32264-158">-ScheduleStatus</span></span>
<span data-ttu-id="32264-159">Der Status des Exportzeitplans.</span><span class="sxs-lookup"><span data-stu-id="32264-159">The status of the export's schedule.</span></span>
<span data-ttu-id="32264-160">Wenn "Inaktiv" angezeigt wird, wird der Exportzeitplan angehalten.</span><span class="sxs-lookup"><span data-stu-id="32264-160">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="32264-161">-Scope</span><span class="sxs-lookup"><span data-stu-id="32264-161">-Scope</span></span>
<span data-ttu-id="32264-162">Dieser Parameter definiert den Umfang des Kostenmanagements aus verschiedenen Perspektiven : "Abonnement", "Ressourcengruppe" und "Dienst bereitstellen".</span><span class="sxs-lookup"><span data-stu-id="32264-162">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="32264-163">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="32264-163">-TimePeriodFrom</span></span>
<span data-ttu-id="32264-164">Das Startdatum für den Export von Daten.</span><span class="sxs-lookup"><span data-stu-id="32264-164">The start date for export data.</span></span>

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

### <span data-ttu-id="32264-165">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="32264-165">-TimePeriodTo</span></span>
<span data-ttu-id="32264-166">Das Enddatum für den Export von Daten.</span><span class="sxs-lookup"><span data-stu-id="32264-166">The end date for export data.</span></span>

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

### <span data-ttu-id="32264-167">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="32264-167">-Confirm</span></span>
<span data-ttu-id="32264-168">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="32264-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32264-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32264-169">-WhatIf</span></span>
<span data-ttu-id="32264-170">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32264-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32264-171">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="32264-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32264-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32264-172">CommonParameters</span></span>
<span data-ttu-id="32264-173">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32264-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32264-174">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32264-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32264-175">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="32264-175">INPUTS</span></span>

### <span data-ttu-id="32264-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="32264-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="32264-177">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="32264-177">OUTPUTS</span></span>

### <span data-ttu-id="32264-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="32264-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="32264-179">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="32264-179">NOTES</span></span>

<span data-ttu-id="32264-180">ALIASE</span><span class="sxs-lookup"><span data-stu-id="32264-180">ALIASES</span></span>

<span data-ttu-id="32264-181">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="32264-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="32264-182">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="32264-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="32264-183">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="32264-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="32264-184">INPUTOBJECT <ICostManagementIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="32264-184">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="32264-185">`[AlertId <String>]`: Warnungs-ID</span><span class="sxs-lookup"><span data-stu-id="32264-185">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="32264-186">`[ExportName <String>]`: Name exportieren.</span><span class="sxs-lookup"><span data-stu-id="32264-186">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="32264-187">`[ExternalCloudProviderId <String>]`: Dies kann "{externalSubscriptionId}" für verknüpftes Konto oder "{externalBillingAccountId}" für konsolidiertes Konto sein, das mit Dimensions-/Abfragevorgängen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="32264-187">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="32264-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Der externe Cloudanbietertyp, der mit Dimensions-/Abfragevorgängen verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="32264-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="32264-189">Dies umfasst "externalSubscriptions" für verknüpfte Konten und "externalBillingAccounts" für konsolidierte Konten.</span><span class="sxs-lookup"><span data-stu-id="32264-189">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="32264-190">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="32264-190">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="32264-191">`[Scope <String>]`: Der Bereich, der Ansichtsvorgängen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="32264-191">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="32264-192">Dies umfasst "Abonnements/{subscriptionId}" für den Abonnementbereich, "subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}" für resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}" for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management /managementGroups/{managementGroupId}" für den Bereich "Management Group", "providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}" für den Bereich "Externe Abrechnungskonten", "providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}" für den Bereich "Externes Abonnement".</span><span class="sxs-lookup"><span data-stu-id="32264-192">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="32264-193">`[ViewName <String>]`: Anzeigename</span><span class="sxs-lookup"><span data-stu-id="32264-193">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="32264-194">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="32264-194">RELATED LINKS</span></span>

