---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: 3c0178ebae2237730d7f0d11eb832a30988ffdb4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843808"
---
# <span data-ttu-id="f7d82-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f7d82-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="f7d82-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7d82-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d82-103">Hinzufügen oder Aktualisieren einer metrischen, nicht klassischen v2-basierten Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="f7d82-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="f7d82-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7d82-104">SYNTAX</span></span>

### <span data-ttu-id="f7d82-105">CreateAlertByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="f7d82-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-DisableRule] [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7d82-106">CreateAlertByResourceIdAndActionGroup</span><span class="sxs-lookup"><span data-stu-id="f7d82-106">CreateAlertByResourceIdAndActionGroup</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7d82-107">CreateAlertByResourceIdAndActionGroupId</span><span class="sxs-lookup"><span data-stu-id="f7d82-107">CreateAlertByResourceIdAndActionGroupId</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroupId <String[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7d82-108">CreateAlertByScopes</span><span class="sxs-lookup"><span data-stu-id="f7d82-108">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-DisableRule] [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7d82-109">CreateAlertByScopesAndActionGroup</span><span class="sxs-lookup"><span data-stu-id="f7d82-109">CreateAlertByScopesAndActionGroup</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7d82-110">CreateAlertByScopesAndActionGroupId</span><span class="sxs-lookup"><span data-stu-id="f7d82-110">CreateAlertByScopesAndActionGroupId</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroupId <String[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7d82-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7d82-111">DESCRIPTION</span></span>
<span data-ttu-id="f7d82-112">Hinzufügen oder Aktualisieren einer **metrischen, nicht klassischen v2-basierten Warnungsregel**</span><span class="sxs-lookup"><span data-stu-id="f7d82-112">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="f7d82-113">Die hinzugefügte Regel ist einer Ressourcengruppe zugeordnet und hat einen Namen.</span><span class="sxs-lookup"><span data-stu-id="f7d82-113">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="f7d82-114">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f7d82-114">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="f7d82-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7d82-115">EXAMPLES</span></span>

### <span data-ttu-id="f7d82-116">Beispiel 1: Hinzufügen einer Metrik-Warnungsregel zu einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="f7d82-116">Example 1: Add a metric alert rule to a virtual machine</span></span>

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

<span data-ttu-id="f7d82-117">Mit diesem Befehl wird eine Metrik-Warnungsregel für einen virtuellen Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="f7d82-117">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="f7d82-118">$Condition ist die Ausgabe von New-AzMetricAlertRuleV2Criteria-Cmdlet, und $Act ist die Ausgabe des New-AzActionGroup-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="f7d82-118">$condition is the output of New-AzMetricAlertRuleV2Criteria cmdlet and $act is the output of New-AzActionGroup cmdlet</span></span>

### <span data-ttu-id="f7d82-119">Beispiel 2: Hinzufügen einer Metrik-Warnungsregel für alle virtuellen Computer in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="f7d82-119">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
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

<span data-ttu-id="f7d82-120">Mit diesem Befehl wird eine metrische Warnungsregel für alle virtuellen Computer im Abonnement erstellt, die in eastus enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="f7d82-120">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="f7d82-121">Beispiel 3: Deaktivieren einer Metrik-Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="f7d82-121">Example 3: Disable a metric alert rule</span></span>
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

<span data-ttu-id="f7d82-122">Mit diesem Befehl wird eine Metrik-Warnungsregel deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f7d82-122">This command disables a metric alert rule.</span></span> <span data-ttu-id="f7d82-123">Hier wird die Ausgabe von Get-AzMetricAlertRuleV2 an Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f7d82-123">Here, we are piping output of Get-AzMetricAlertRuleV2 to Add-AzMetricAlertRuleV2</span></span> 

### <span data-ttu-id="f7d82-124">Beispiel 4: Hinzufügen einer metrischen Warnungsregel mit Bemaßungen</span><span class="sxs-lookup"><span data-stu-id="f7d82-124">Example 4: Add a metric alert rule with dimensions</span></span>

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

<span data-ttu-id="f7d82-125">Wenn Sie eine komplexere Metrik-Warnungsregel erstellen möchten, die die Auswahl von Dimensionswerten oder mehrere Kriterien umfasst, können Sie die Hilfsprogramm-Cmdlets New-AzMetricAlertRuleV2DimensionSelection und New-AzMetricAlertRuleV2Criteria verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7d82-125">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets New-AzMetricAlertRuleV2DimensionSelection and New-AzMetricAlertRuleV2Criteria.</span></span>

<span data-ttu-id="f7d82-126">Über den Satz von Cmdlets wird eine metrische Warnungsregel mit Bemaßungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="f7d82-126">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>

## <span data-ttu-id="f7d82-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7d82-127">PARAMETERS</span></span>

### <span data-ttu-id="f7d82-128">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="f7d82-128">-ActionGroup</span></span>
<span data-ttu-id="f7d82-129">Die Gruppe ' Aktion ' für Regel</span><span class="sxs-lookup"><span data-stu-id="f7d82-129">The Action Group for rule</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]
Parameter Sets: CreateAlertByResourceIdAndActionGroup, CreateAlertByScopesAndActionGroup
Aliases: Actions

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d82-130">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="f7d82-130">-ActionGroupId</span></span>
<span data-ttu-id="f7d82-131">Die Gruppen-ID der Aktion für Regel</span><span class="sxs-lookup"><span data-stu-id="f7d82-131">The Action Group id for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByResourceIdAndActionGroupId, CreateAlertByScopesAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d82-132">-Bedingung</span><span class="sxs-lookup"><span data-stu-id="f7d82-132">-Condition</span></span>
<span data-ttu-id="f7d82-133">Die Bedingung für Regel</span><span class="sxs-lookup"><span data-stu-id="f7d82-133">The condition for rule</span></span>

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

### <span data-ttu-id="f7d82-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d82-134">-DefaultProfile</span></span>
<span data-ttu-id="f7d82-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f7d82-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7d82-136">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7d82-136">-Description</span></span>
<span data-ttu-id="f7d82-137">Die Beschreibung der Metrik-Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="f7d82-137">The description of the metric alert rule</span></span>

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

### <span data-ttu-id="f7d82-138">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="f7d82-138">-DisableRule</span></span>
<span data-ttu-id="f7d82-139">Das Flag zum Deaktivieren der Regel (Status)</span><span class="sxs-lookup"><span data-stu-id="f7d82-139">The disable rule (status) flag</span></span>

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

### <span data-ttu-id="f7d82-140">-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="f7d82-140">-Frequency</span></span>
<span data-ttu-id="f7d82-141">Die Auswertungs Häufigkeit für Regel</span><span class="sxs-lookup"><span data-stu-id="f7d82-141">The evaluation frequency for rule</span></span>

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

### <span data-ttu-id="f7d82-142">-Name</span><span class="sxs-lookup"><span data-stu-id="f7d82-142">-Name</span></span>
<span data-ttu-id="f7d82-143">Der Name der Metrik-Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="f7d82-143">The name of metric alert rule</span></span>

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

### <span data-ttu-id="f7d82-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7d82-144">-ResourceGroupName</span></span>
<span data-ttu-id="f7d82-145">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f7d82-145">The Resource Group Name</span></span>

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

### <span data-ttu-id="f7d82-146">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="f7d82-146">-Severity</span></span>
<span data-ttu-id="f7d82-147">Der Schweregrad für die Metrik-Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="f7d82-147">The severity for the metric alert rule</span></span>

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

### <span data-ttu-id="f7d82-148">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f7d82-148">-TargetResourceId</span></span>
<span data-ttu-id="f7d82-149">Die Ziel Ressourcen-ID für Regel</span><span class="sxs-lookup"><span data-stu-id="f7d82-149">The target resource id for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByResourceId, CreateAlertByResourceIdAndActionGroup, CreateAlertByResourceIdAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d82-150">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="f7d82-150">-TargetResourceRegion</span></span>
<span data-ttu-id="f7d82-151">Der Ziel Ressourcenbereich für Regel</span><span class="sxs-lookup"><span data-stu-id="f7d82-151">The target resource region for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes, CreateAlertByScopesAndActionGroup, CreateAlertByScopesAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d82-152">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="f7d82-152">-TargetResourceScope</span></span>
<span data-ttu-id="f7d82-153">Der Ziel Ressourcenbereich für Regel</span><span class="sxs-lookup"><span data-stu-id="f7d82-153">The target resource scope for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByScopes, CreateAlertByScopesAndActionGroup, CreateAlertByScopesAndActionGroupId
Aliases: Scopes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d82-154">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="f7d82-154">-TargetResourceType</span></span>
<span data-ttu-id="f7d82-155">Der Typ der Zielressource für Regel</span><span class="sxs-lookup"><span data-stu-id="f7d82-155">The target resource type for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes, CreateAlertByScopesAndActionGroup, CreateAlertByScopesAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d82-156">-Windowsisieren</span><span class="sxs-lookup"><span data-stu-id="f7d82-156">-WindowSize</span></span>
<span data-ttu-id="f7d82-157">Fenstergröße für Regel</span><span class="sxs-lookup"><span data-stu-id="f7d82-157">The window size for rule</span></span>

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

### <span data-ttu-id="f7d82-158">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f7d82-158">-Confirm</span></span>
<span data-ttu-id="f7d82-159">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7d82-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7d82-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7d82-160">-WhatIf</span></span>
<span data-ttu-id="f7d82-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7d82-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7d82-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7d82-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7d82-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d82-163">CommonParameters</span></span>
<span data-ttu-id="f7d82-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7d82-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d82-165">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7d82-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d82-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7d82-166">INPUTS</span></span>

### <span data-ttu-id="f7d82-167">System. String</span><span class="sxs-lookup"><span data-stu-id="f7d82-167">System.String</span></span>

### <span data-ttu-id="f7d82-168">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="f7d82-168">System.TimeSpan</span></span>

### <span data-ttu-id="f7d82-169">System. String []</span><span class="sxs-lookup"><span data-stu-id="f7d82-169">System.String[]</span></span>

### <span data-ttu-id="f7d82-170">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Insights. OutputClasses. IPSMultiMetricCriteria, Microsoft. Azure. PowerShell. Cmdlets. Monitor, Version = 1.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f7d82-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f7d82-171">Microsoft. Azure. Management. Monitor. Models. ActivityLogAlertActionGroup []</span><span class="sxs-lookup"><span data-stu-id="f7d82-171">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="f7d82-172">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="f7d82-172">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f7d82-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f7d82-173">System.Int32</span></span>

## <span data-ttu-id="f7d82-174">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7d82-174">OUTPUTS</span></span>

### <span data-ttu-id="f7d82-175">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f7d82-175">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="f7d82-176">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7d82-176">NOTES</span></span>

## <span data-ttu-id="f7d82-177">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7d82-177">RELATED LINKS</span></span>
