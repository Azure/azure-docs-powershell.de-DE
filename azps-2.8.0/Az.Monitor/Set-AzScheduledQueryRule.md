---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
ms.openlocfilehash: 142dfbf1e2a0868581d30aba344395cf264bb352
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822620"
---
# <span data-ttu-id="5844d-101">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5844d-101">Set-AzScheduledQueryRule</span></span>

## <span data-ttu-id="5844d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5844d-102">SYNOPSIS</span></span>
<span data-ttu-id="5844d-103">Aktualisiert eine Protokoll Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="5844d-103">Updates a Log Alert Rule</span></span>

## <span data-ttu-id="5844d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5844d-104">SYNTAX</span></span>

### <span data-ttu-id="5844d-105">ByRuleName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5844d-105">ByRuleName (Default)</span></span>
```
Set-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> [-Schedule <PSScheduledQueryRuleSchedule>]
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -ResourceGroupName <String> [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5844d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5844d-106">ByInputObject</span></span>
```
Set-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-Source <PSScheduledQueryRuleSource>]
 [-Schedule <PSScheduledQueryRuleSchedule>] [-Action <PSScheduledQueryRuleAlertingAction>] [-Location <String>]
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5844d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5844d-107">ByResourceId</span></span>
```
Set-AzScheduledQueryRule -ResourceId <String> -Source <PSScheduledQueryRuleSource>
 [-Schedule <PSScheduledQueryRuleSchedule>] -Action <PSScheduledQueryRuleAlertingAction> -Location <String>
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5844d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5844d-108">DESCRIPTION</span></span>
<span data-ttu-id="5844d-109">Aktualisieren einer Warnungsregel für Protokolle durch Put-Semantik</span><span class="sxs-lookup"><span data-stu-id="5844d-109">Updates a Log Alert Rule by PUT semantics</span></span>

## <span data-ttu-id="5844d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5844d-110">EXAMPLES</span></span>

### <span data-ttu-id="5844d-111">Beispiel 1 – Satz von Regelnamen</span><span class="sxs-lookup"><span data-stu-id="5844d-111">Example 1 - Set by rule name</span></span>
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

### <span data-ttu-id="5844d-112">Beispiel 2 – Satz von Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="5844d-112">Example 2 - Set by Input Object</span></span>
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

### <span data-ttu-id="5844d-113">Beispiel 3 – nach Ressourcen-ID einrichten</span><span class="sxs-lookup"><span data-stu-id="5844d-113">Example 3 - Set by resource Id</span></span>
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

## <span data-ttu-id="5844d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5844d-114">PARAMETERS</span></span>

### <span data-ttu-id="5844d-115">– Aktion</span><span class="sxs-lookup"><span data-stu-id="5844d-115">-Action</span></span>
<span data-ttu-id="5844d-116">Warnungsaktion für geplante Abfrageregel</span><span class="sxs-lookup"><span data-stu-id="5844d-116">The scheduled query rule Alerting Action</span></span>

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

### <span data-ttu-id="5844d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5844d-117">-AsJob</span></span>
<span data-ttu-id="5844d-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5844d-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5844d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5844d-119">-DefaultProfile</span></span>
<span data-ttu-id="5844d-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5844d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5844d-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5844d-121">-Description</span></span>
<span data-ttu-id="5844d-122">Die Beschreibung für diese Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="5844d-122">The description for this alert</span></span>

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

### <span data-ttu-id="5844d-123">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="5844d-123">-Enabled</span></span>
<span data-ttu-id="5844d-124">Der Azure-Warnungszustand – gültige Werte – $true, $false</span><span class="sxs-lookup"><span data-stu-id="5844d-124">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="5844d-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5844d-125">-InputObject</span></span>
<span data-ttu-id="5844d-126">Die geplante Abfrageregel Ressource</span><span class="sxs-lookup"><span data-stu-id="5844d-126">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="5844d-127">-Standort</span><span class="sxs-lookup"><span data-stu-id="5844d-127">-Location</span></span>
<span data-ttu-id="5844d-128">Der Speicherort für diese Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="5844d-128">The location for this alert</span></span>

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

### <span data-ttu-id="5844d-129">-Name</span><span class="sxs-lookup"><span data-stu-id="5844d-129">-Name</span></span>
<span data-ttu-id="5844d-130">Der Warnungsname</span><span class="sxs-lookup"><span data-stu-id="5844d-130">The alert name</span></span>

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

### <span data-ttu-id="5844d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5844d-131">-ResourceGroupName</span></span>
<span data-ttu-id="5844d-132">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5844d-132">The resource group name</span></span>

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

### <span data-ttu-id="5844d-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5844d-133">-ResourceId</span></span>
<span data-ttu-id="5844d-134">Die Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="5844d-134">The resource Id</span></span>

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

### <span data-ttu-id="5844d-135">-Terminplan</span><span class="sxs-lookup"><span data-stu-id="5844d-135">-Schedule</span></span>
<span data-ttu-id="5844d-136">Zeitplan für regelmäßige Abfrageregeln</span><span class="sxs-lookup"><span data-stu-id="5844d-136">The scheduled query rule schedule</span></span>

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

### <span data-ttu-id="5844d-137">-Source</span><span class="sxs-lookup"><span data-stu-id="5844d-137">-Source</span></span>
<span data-ttu-id="5844d-138">Die geplante Abfrageregel Quelle</span><span class="sxs-lookup"><span data-stu-id="5844d-138">The scheduled query rule source</span></span>

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

### <span data-ttu-id="5844d-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="5844d-139">-Tag</span></span>
<span data-ttu-id="5844d-140">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="5844d-140">Resource tags</span></span>

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

### <span data-ttu-id="5844d-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5844d-141">-Confirm</span></span>
<span data-ttu-id="5844d-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5844d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5844d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5844d-143">-WhatIf</span></span>
<span data-ttu-id="5844d-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5844d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5844d-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5844d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5844d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5844d-146">CommonParameters</span></span>
<span data-ttu-id="5844d-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5844d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5844d-148">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5844d-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5844d-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5844d-149">INPUTS</span></span>

### <span data-ttu-id="5844d-150">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="5844d-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="5844d-151">System. String</span><span class="sxs-lookup"><span data-stu-id="5844d-151">System.String</span></span>

### <span data-ttu-id="5844d-152">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="5844d-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

### <span data-ttu-id="5844d-153">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="5844d-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

### <span data-ttu-id="5844d-154">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="5844d-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="5844d-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5844d-155">OUTPUTS</span></span>

### <span data-ttu-id="5844d-156">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="5844d-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="5844d-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="5844d-157">NOTES</span></span>

## <span data-ttu-id="5844d-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5844d-158">RELATED LINKS</span></span>
