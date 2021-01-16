---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
ms.openlocfilehash: 0351d6920c4af7f781ef27f4dfbc36a13e0c50cd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296705"
---
# <span data-ttu-id="2a6c7-101">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2a6c7-101">Set-AzScheduledQueryRule</span></span>

## <span data-ttu-id="2a6c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a6c7-102">SYNOPSIS</span></span>
<span data-ttu-id="2a6c7-103">Aktualisiert eine Protokollwarnungsregel</span><span class="sxs-lookup"><span data-stu-id="2a6c7-103">Updates a Log Alert Rule</span></span>

## <span data-ttu-id="2a6c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a6c7-104">SYNTAX</span></span>

### <span data-ttu-id="2a6c7-105">ByRuleName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2a6c7-105">ByRuleName (Default)</span></span>
```
Set-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> [-Schedule <PSScheduledQueryRuleSchedule>]
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -ResourceGroupName <String> [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a6c7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2a6c7-106">ByInputObject</span></span>
```
Set-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-Source <PSScheduledQueryRuleSource>]
 [-Schedule <PSScheduledQueryRuleSchedule>] [-Action <PSScheduledQueryRuleAlertingAction>] [-Location <String>]
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a6c7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2a6c7-107">ByResourceId</span></span>
```
Set-AzScheduledQueryRule -ResourceId <String> -Source <PSScheduledQueryRuleSource>
 [-Schedule <PSScheduledQueryRuleSchedule>] -Action <PSScheduledQueryRuleAlertingAction> -Location <String>
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a6c7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a6c7-108">DESCRIPTION</span></span>
<span data-ttu-id="2a6c7-109">Aktualisiert eine Protokollwarnungsregel durch PUT-Semantik.</span><span class="sxs-lookup"><span data-stu-id="2a6c7-109">Updates a Log Alert Rule by PUT semantics</span></span>

## <span data-ttu-id="2a6c7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2a6c7-110">EXAMPLES</span></span>

### <span data-ttu-id="2a6c7-111">Beispiel 1: Festlegen nach Regelname</span><span class="sxs-lookup"><span data-stu-id="2a6c7-111">Example 1: Set by rule name</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1" -Enabled $true -Location "centralindia" -Action $alertingAction -Description "log alert description" -Schedule $schedule -Source $source

Description       : log alert description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:45:04 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="2a6c7-112">Beispiel 2: Festlegen durch ein Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="2a6c7-112">Example 2: Set by Input Object</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -InputObject $sqr -Description "changed description"

Description       : changed description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:46:38 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="2a6c7-113">Beispiel 3: Festlegen nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2a6c7-113">Example 3: Set by resource Id</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -ResourceId "/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1" -Enabled $true -Location "centralindia" -Action $alertingAction -Description "change description again" -Schedule $schedule -Source $source

Description       : change description again
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:47:59 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

## <span data-ttu-id="2a6c7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a6c7-114">PARAMETERS</span></span>

### <span data-ttu-id="2a6c7-115">-Aktion</span><span class="sxs-lookup"><span data-stu-id="2a6c7-115">-Action</span></span>
<span data-ttu-id="2a6c7-116">Benachrichtigungsaktion für die geplante Abfrageregel</span><span class="sxs-lookup"><span data-stu-id="2a6c7-116">The scheduled query rule Alerting Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a6c7-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a6c7-117">-AsJob</span></span>
<span data-ttu-id="2a6c7-118">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2a6c7-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a6c7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a6c7-119">-DefaultProfile</span></span>
<span data-ttu-id="2a6c7-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a6c7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a6c7-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2a6c7-121">-Description</span></span>
<span data-ttu-id="2a6c7-122">Die Beschreibung für diese Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="2a6c7-122">The description for this alert</span></span>

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

### <span data-ttu-id="2a6c7-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="2a6c7-123">-Enabled</span></span>
<span data-ttu-id="2a6c7-124">Der Azure Alert State – gültige Werte – $true, $false</span><span class="sxs-lookup"><span data-stu-id="2a6c7-124">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a6c7-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a6c7-125">-InputObject</span></span>
<span data-ttu-id="2a6c7-126">Ressource "Geplante Abfrageregel"</span><span class="sxs-lookup"><span data-stu-id="2a6c7-126">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a6c7-127">-Location</span><span class="sxs-lookup"><span data-stu-id="2a6c7-127">-Location</span></span>
<span data-ttu-id="2a6c7-128">Der Speicherort für diese Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="2a6c7-128">The location for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a6c7-129">-Name</span><span class="sxs-lookup"><span data-stu-id="2a6c7-129">-Name</span></span>
<span data-ttu-id="2a6c7-130">Der Benachrichtigungsname</span><span class="sxs-lookup"><span data-stu-id="2a6c7-130">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a6c7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a6c7-131">-ResourceGroupName</span></span>
<span data-ttu-id="2a6c7-132">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2a6c7-132">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a6c7-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a6c7-133">-ResourceId</span></span>
<span data-ttu-id="2a6c7-134">Die Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2a6c7-134">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a6c7-135">-Schedule</span><span class="sxs-lookup"><span data-stu-id="2a6c7-135">-Schedule</span></span>
<span data-ttu-id="2a6c7-136">Der Zeitplan für geplante Abfrageregel</span><span class="sxs-lookup"><span data-stu-id="2a6c7-136">The scheduled query rule schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a6c7-137">-Source</span><span class="sxs-lookup"><span data-stu-id="2a6c7-137">-Source</span></span>
<span data-ttu-id="2a6c7-138">Quelle der geplanten Abfrageregel</span><span class="sxs-lookup"><span data-stu-id="2a6c7-138">The scheduled query rule source</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a6c7-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="2a6c7-139">-Tag</span></span>
<span data-ttu-id="2a6c7-140">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="2a6c7-140">Resource tags</span></span>

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

### <span data-ttu-id="2a6c7-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a6c7-141">-Confirm</span></span>
<span data-ttu-id="2a6c7-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2a6c7-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a6c7-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2a6c7-143">-WhatIf</span></span>
<span data-ttu-id="2a6c7-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2a6c7-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a6c7-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a6c7-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a6c7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a6c7-146">CommonParameters</span></span>
<span data-ttu-id="2a6c7-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a6c7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a6c7-148">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a6c7-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a6c7-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2a6c7-149">INPUTS</span></span>

### <span data-ttu-id="2a6c7-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="2a6c7-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="2a6c7-151">System.String</span><span class="sxs-lookup"><span data-stu-id="2a6c7-151">System.String</span></span>

### <span data-ttu-id="2a6c7-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="2a6c7-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

### <span data-ttu-id="2a6c7-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="2a6c7-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

### <span data-ttu-id="2a6c7-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="2a6c7-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="2a6c7-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2a6c7-155">OUTPUTS</span></span>

### <span data-ttu-id="2a6c7-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="2a6c7-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="2a6c7-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2a6c7-157">NOTES</span></span>

## <span data-ttu-id="2a6c7-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2a6c7-158">RELATED LINKS</span></span>
