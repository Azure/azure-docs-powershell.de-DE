---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: 0317f21231edd2608492d37609ab4f4849ba9c20
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289439"
---
# <span data-ttu-id="53ace-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="53ace-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="53ace-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53ace-102">SYNOPSIS</span></span>
<span data-ttu-id="53ace-103">Fügt eine auf V2 basierende (nicht klassische) metrische Warnungsregel hinzu oder aktualisiert diese.</span><span class="sxs-lookup"><span data-stu-id="53ace-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="53ace-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53ace-104">SYNTAX</span></span>

### <span data-ttu-id="53ace-105">CreateAlertByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="53ace-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53ace-106">CreateAlertByScopes</span><span class="sxs-lookup"><span data-stu-id="53ace-106">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53ace-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53ace-107">DESCRIPTION</span></span>
<span data-ttu-id="53ace-108">Fügt eine auf **V2 basierende metrische Warnungsregel (nicht klassische)** hinzu oder aktualisiert diese.</span><span class="sxs-lookup"><span data-stu-id="53ace-108">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="53ace-109">Die hinzugefügte Regel ist einer Ressourcengruppe zugeordnet und hat einen Namen.</span><span class="sxs-lookup"><span data-stu-id="53ace-109">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="53ace-110">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung vom Benutzer anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="53ace-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="53ace-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="53ace-111">EXAMPLES</span></span>

### <span data-ttu-id="53ace-112">Beispiel 1: Hinzufügen einer metrischen Warnungsregel zu einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="53ace-112">Example 1: Add a metric alert rule to a virtual machine</span></span>

```powershell
PS C:\> Add-AzMetricAlertRuleV2 -Name PS3182019 -ResourceGroupName xxxxRG -WindowSize 0:5 -Frequency 0:5 -TargetResourceScope "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM1", "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM2" -TargetResourceType "Microsoft.Compute/virtualMachines" -TargetResourceRegion "eastus" -Description "This is description" -Severity 4 -ActionGroup $act -Condition $condition

Description          : This is description
Severity             : 4
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM1,
                       /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM2}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertMultipleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/xxxxRG/providers/Microsoft.Insights/metricAlerts/PS3182019
Name                 : PS3182019
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="53ace-113">Mit diesem Befehl wird eine metrische Warnungsregel für einen virtuellen Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="53ace-113">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="53ace-114">$condition ist die Ausgabe des [Cmdlets "New-AzMetricAlertRuleV2Criteria",](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) und $act ist die Ausgabe des [Cmdlets "New-AzActionGroup".](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup)</span><span class="sxs-lookup"><span data-stu-id="53ace-114">$condition is the output of [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet and $act is the output of [New-AzActionGroup](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup) cmdlet</span></span>

### <span data-ttu-id="53ace-115">Beispiel 2: Hinzufügen einer metrischen Warnungsregel für alle virtuellen Computer in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="53ace-115">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
```powershell
PS C:\> Add-AzMetricAlertRuleV2 -Name AllVM -ResourceGroupName xxxxRG -WindowSize 0:5 -Frequency 0:5 -TargetResourceScope "/subscriptions/00000000-0000-0000-0000-0000000" -TargetResourceType "Microsoft.Compute/virtualMachines" -TargetResourceRegion "eastus" -Description "This is description" -Severity 4 -ActionGroup $act -Condition $condition

Description          : This is description
Severity             : 4
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertMultipleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/xxxxRG/providers/Microsoft.Insights/metricAlerts/AllVM
Name                 : AllVM
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="53ace-116">Mit diesem Befehl wird eine metrische Warnungsregel für alle virtuellen Computer im Abonnement erstellt, die sich in Eastus befinden.</span><span class="sxs-lookup"><span data-stu-id="53ace-116">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="53ace-117">Beispiel 3: Deaktivieren einer metrischen Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="53ace-117">Example 3: Disable a metric alert rule</span></span>
```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest  -Name TestAlertRule | Add-AzMetricAlertRuleV2 -DisableRule
Description          : This new Metric alert rule was created from Powershell version: 1.0.1
Severity             : 4
Enabled              : False
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertSingleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo1}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/Microsoft.Insights/metricAlerts/TestAlertRule
Name                 : TestAlertRule
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="53ace-118">Mit diesem Befehl wird eine metrische Warnungsregel deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="53ace-118">This command disables a metric alert rule.</span></span> <span data-ttu-id="53ace-119">Hier wird die Ausgabe von ["Get-AzMetricAlertRuleV2"](https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricalertrulev2) in ["Add-AzMetricAlertRuleV2" pipiert.](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2)</span><span class="sxs-lookup"><span data-stu-id="53ace-119">Here, we are piping output of [Get-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricalertrulev2) to [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2)</span></span> 

### <span data-ttu-id="53ace-120">Beispiel 4: Hinzufügen einer metrischen Warnungsregel mit Dimensionen</span><span class="sxs-lookup"><span data-stu-id="53ace-120">Example 4: Add a metric alert rule with dimensions</span></span>

```powershell
PS C:\>$act = New-AzActionGroup -ActionGroupId "/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/actionGroupDemo"
PS C:\>$dim1 = New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest"
PS C:\>$dim2 = New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/location" -ValuesToInclude "*"
PS C:\>$criteria = New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -DimensionSelection $dim1,$dim2 -TimeAggregation Average -Operator GreaterThan -Threshold 2
PS C:\>Add-AzMetricAlertRuleV2 -Name AlertWithDim -ResourceGroupName alertstest -WindowSize 00:05:00 -Frequency 00:05:00 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction" -Condition $criteria -ActionGroup $act -DisableRule -Severity 4
Description          : This new Metric alert rule was created from Powershell version: 1.0.0
Severity             : 4
Enabled              : False
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertSingleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/actionGroupDemo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/Microsoft.Insights/metricAlerts/AlertWithDim
Name                 : AlertWithDim
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="53ace-121">Wenn Sie eine komplexere metrische Warnungsregel erstellen möchten, z. B. diejenigen, die das Auswählen von Dimensionswerten oder mehrere Kriterien umfassen, können Sie die Hilfs cmdlets ["New-AzMetricAlertRuleV2DimensionSelection"](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection) und ["New-AzMetricAlertRuleV2Criteria"](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria)verwenden.</span><span class="sxs-lookup"><span data-stu-id="53ace-121">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets [New-AzMetricAlertRuleV2DimensionSelection](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection) and [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria).</span></span>

<span data-ttu-id="53ace-122">Über einer Gruppe von Cmdlets wird eine metrische Warnungsregel mit Dimensionen erstellt.</span><span class="sxs-lookup"><span data-stu-id="53ace-122">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>

## <span data-ttu-id="53ace-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53ace-123">PARAMETERS</span></span>

### <span data-ttu-id="53ace-124">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="53ace-124">-ActionGroup</span></span>
<span data-ttu-id="53ace-125">Aktionsgruppe für Regel</span><span class="sxs-lookup"><span data-stu-id="53ace-125">The Action Group for rule</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]
Parameter Sets: (All)
Aliases: Actions

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53ace-126">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="53ace-126">-ActionGroupId</span></span>
<span data-ttu-id="53ace-127">Die Id der Aktionsgruppe für die Regel</span><span class="sxs-lookup"><span data-stu-id="53ace-127">The Action Group id for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ace-128">-Bedingung</span><span class="sxs-lookup"><span data-stu-id="53ace-128">-Condition</span></span>
<span data-ttu-id="53ace-129">Die Bedingung für die Regel</span><span class="sxs-lookup"><span data-stu-id="53ace-129">The condition for rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]
Parameter Sets: (All)
Aliases: Criteria

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53ace-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53ace-130">-DefaultProfile</span></span>
<span data-ttu-id="53ace-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="53ace-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53ace-132">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53ace-132">-Description</span></span>
<span data-ttu-id="53ace-133">Beschreibung der metrischen Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="53ace-133">The description of the metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ace-134">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="53ace-134">-DisableRule</span></span>
<span data-ttu-id="53ace-135">Das Kennzeichen "Regel deaktivieren" (Status)</span><span class="sxs-lookup"><span data-stu-id="53ace-135">The disable rule (status) flag</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ace-136">-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="53ace-136">-Frequency</span></span>
<span data-ttu-id="53ace-137">Die Auswertungshäufigkeit für die Regel</span><span class="sxs-lookup"><span data-stu-id="53ace-137">The evaluation frequency for rule</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases: EvaluationFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ace-138">-Name</span><span class="sxs-lookup"><span data-stu-id="53ace-138">-Name</span></span>
<span data-ttu-id="53ace-139">Der Name der metrischen Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="53ace-139">The name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ace-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53ace-140">-ResourceGroupName</span></span>
<span data-ttu-id="53ace-141">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="53ace-141">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ace-142">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="53ace-142">-Severity</span></span>
<span data-ttu-id="53ace-143">Der Schweregrad für die metrische Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="53ace-143">The severity for the metric alert rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ace-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="53ace-144">-TargetResourceId</span></span>
<span data-ttu-id="53ace-145">Die Zielressourcen-ID für die Regel</span><span class="sxs-lookup"><span data-stu-id="53ace-145">The target resource id for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ace-146">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="53ace-146">-TargetResourceRegion</span></span>
<span data-ttu-id="53ace-147">Zielressourcenregion für die Regel</span><span class="sxs-lookup"><span data-stu-id="53ace-147">The target resource region for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ace-148">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="53ace-148">-TargetResourceScope</span></span>
<span data-ttu-id="53ace-149">Der Zielressourcenbereich für die Regel</span><span class="sxs-lookup"><span data-stu-id="53ace-149">The target resource scope for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByScopes
Aliases: Scopes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ace-150">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="53ace-150">-TargetResourceType</span></span>
<span data-ttu-id="53ace-151">Der Zielressourcentyp für die Regel</span><span class="sxs-lookup"><span data-stu-id="53ace-151">The target resource type for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ace-152">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="53ace-152">-WindowSize</span></span>
<span data-ttu-id="53ace-153">Die Fenstergröße für die Regel</span><span class="sxs-lookup"><span data-stu-id="53ace-153">The window size for rule</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ace-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53ace-154">-Confirm</span></span>
<span data-ttu-id="53ace-155">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="53ace-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53ace-156">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="53ace-156">-WhatIf</span></span>
<span data-ttu-id="53ace-157">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="53ace-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53ace-158">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="53ace-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53ace-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53ace-159">CommonParameters</span></span>
<span data-ttu-id="53ace-160">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53ace-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53ace-161">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53ace-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53ace-162">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="53ace-162">INPUTS</span></span>

### <span data-ttu-id="53ace-163">System.String</span><span class="sxs-lookup"><span data-stu-id="53ace-163">System.String</span></span>

### <span data-ttu-id="53ace-164">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="53ace-164">System.TimeSpan</span></span>

### <span data-ttu-id="53ace-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="53ace-165">System.String[]</span></span>

### <span data-ttu-id="53ace-166">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="53ace-166">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="53ace-167">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span><span class="sxs-lookup"><span data-stu-id="53ace-167">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="53ace-168">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="53ace-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="53ace-169">System.Int32</span><span class="sxs-lookup"><span data-stu-id="53ace-169">System.Int32</span></span>

## <span data-ttu-id="53ace-170">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="53ace-170">OUTPUTS</span></span>

### <span data-ttu-id="53ace-171">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="53ace-171">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="53ace-172">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="53ace-172">NOTES</span></span>

## <span data-ttu-id="53ace-173">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="53ace-173">RELATED LINKS</span></span>
