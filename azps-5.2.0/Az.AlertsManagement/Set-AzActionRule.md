---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: 75a2071e8f60ed15420b69815eba22d6f82e9f82
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292565"
---
# <span data-ttu-id="850f2-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="850f2-101">Set-AzActionRule</span></span>

## <span data-ttu-id="850f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="850f2-102">SYNOPSIS</span></span>
<span data-ttu-id="850f2-103">Erstellen oder aktualisieren Sie eine Aktionsregel.</span><span class="sxs-lookup"><span data-stu-id="850f2-103">Create or update an action rule.</span></span>

## <span data-ttu-id="850f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="850f2-104">SYNTAX</span></span>

### <span data-ttu-id="850f2-105">BySimplifiedFormatDiagnosticsActionRule (Standard)</span><span class="sxs-lookup"><span data-stu-id="850f2-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="850f2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="850f2-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="850f2-107">BySimplifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="850f2-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="850f2-108">BySimplifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="850f2-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="850f2-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="850f2-109">DESCRIPTION</span></span>
<span data-ttu-id="850f2-110">**Set-AzActionRule** erstellt oder aktualisiert eine Aktionsregel.</span><span class="sxs-lookup"><span data-stu-id="850f2-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="850f2-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="850f2-111">EXAMPLES</span></span>

### <span data-ttu-id="850f2-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="850f2-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="850f2-113">Dieses Cmdlet erstellt eine Aktionsregel für die Supression mit einem Abonnementbereich.</span><span class="sxs-lookup"><span data-stu-id="850f2-113">This cmdlet creates an action rule for supression, with a subscription scope.</span></span>

### <span data-ttu-id="850f2-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="850f2-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="850f2-115">Dieses Cmdlet erstellt eine Aktionsregel für eine Aktionsgruppe mit einer Liste des Bereichs "Ressourcengruppen".</span><span class="sxs-lookup"><span data-stu-id="850f2-115">This cmdlet creates an action rule for action group, with a list of resource groups scope.</span></span>

### <span data-ttu-id="850f2-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="850f2-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab/providers/microsoft.insights/metricAlerts/Total Requests Exceeded" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="850f2-117">Dieses Cmdlet erstellt eine Aktionsregel für Diagnoseeinstellungen mit einem Ressourcenbereich.</span><span class="sxs-lookup"><span data-stu-id="850f2-117">This cmdlet creates an action rule for diagnostics settings, with a resource scope.</span></span>

## <span data-ttu-id="850f2-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="850f2-118">PARAMETERS</span></span>

### <span data-ttu-id="850f2-119">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="850f2-119">-ActionGroupId</span></span>
<span data-ttu-id="850f2-120">Id der Aktionsgruppe, die benachrichtigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="850f2-120">Action Group Id which is to be notified.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatActionGroupActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850f2-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="850f2-121">-ActionRuleType</span></span>
<span data-ttu-id="850f2-122">Aktionsregel-Json-Format</span><span class="sxs-lookup"><span data-stu-id="850f2-122">Action rule Json format</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850f2-123">-AlertContextCondition</span><span class="sxs-lookup"><span data-stu-id="850f2-123">-AlertContextCondition</span></span>
<span data-ttu-id="850f2-124">Erwartetes Format – { \<operation\> : \<comma separated list of values\> } Für z. B.</span><span class="sxs-lookup"><span data-stu-id="850f2-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="850f2-125">Contains:smartgroups</span><span class="sxs-lookup"><span data-stu-id="850f2-125">Contains:smartgroups</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850f2-126">-AlertRuleIdCondition</span><span class="sxs-lookup"><span data-stu-id="850f2-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="850f2-127">Erwartetes Format – { \<operation\> : \<comma separated list of values\> } Für z. B.</span><span class="sxs-lookup"><span data-stu-id="850f2-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="850f2-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span><span class="sxs-lookup"><span data-stu-id="850f2-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850f2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="850f2-129">-DefaultProfile</span></span>
<span data-ttu-id="850f2-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="850f2-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="850f2-131">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="850f2-131">-Description</span></span>
<span data-ttu-id="850f2-132">Beschreibung der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="850f2-132">Description of Action Rule</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850f2-133">-DescriptionCondition</span><span class="sxs-lookup"><span data-stu-id="850f2-133">-DescriptionCondition</span></span>
<span data-ttu-id="850f2-134">Erwartetes Format – { \<operation\> : \<comma separated list of values\> } Für z. B.</span><span class="sxs-lookup"><span data-stu-id="850f2-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="850f2-135">Contains:Test Alert</span><span class="sxs-lookup"><span data-stu-id="850f2-135">Contains:Test Alert</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850f2-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="850f2-136">-InputObject</span></span>
<span data-ttu-id="850f2-137">Die Aktionsregelressource</span><span class="sxs-lookup"><span data-stu-id="850f2-137">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="850f2-138">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="850f2-138">-MonitorCondition</span></span>
<span data-ttu-id="850f2-139">Erwartetes Format – { \<operation\> : \<comma separated list of values\> } Für z. B.</span><span class="sxs-lookup"><span data-stu-id="850f2-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="850f2-140">NotEquals:Resolved</span><span class="sxs-lookup"><span data-stu-id="850f2-140">NotEquals:Resolved</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850f2-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="850f2-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="850f2-142">Erwartetes Format – { \<operation\> : \<comma separated list of values\> } Für z. B.</span><span class="sxs-lookup"><span data-stu-id="850f2-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="850f2-143">Equals:Platform,Log Analytics</span><span class="sxs-lookup"><span data-stu-id="850f2-143">Equals:Platform,Log Analytics</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850f2-144">-Name</span><span class="sxs-lookup"><span data-stu-id="850f2-144">-Name</span></span>
<span data-ttu-id="850f2-145">Name der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="850f2-145">Action rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850f2-146">-ReccurenceType</span><span class="sxs-lookup"><span data-stu-id="850f2-146">-ReccurenceType</span></span>
<span data-ttu-id="850f2-147">Gibt die Dauer an, für die der Wert angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="850f2-147">Specifies the duration when the suppression should be applied.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850f2-148">-ReccurentValue</span><span class="sxs-lookup"><span data-stu-id="850f2-148">-ReccurentValue</span></span>
<span data-ttu-id="850f2-149">Erkennbare Werte(en), falls zutreffend. Bei wöchentlicher - \[ 1.2 \] bei monatlicher - \[ 1.3.5.30\]</span><span class="sxs-lookup"><span data-stu-id="850f2-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850f2-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="850f2-150">-ResourceGroupName</span></span>
<span data-ttu-id="850f2-151">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="850f2-151">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850f2-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="850f2-152">-Scope</span></span>
<span data-ttu-id="850f2-153">Durch Kommas getrennte Liste von Werten</span><span class="sxs-lookup"><span data-stu-id="850f2-153">Comma separated list of values</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850f2-154">-SeverityCondition</span><span class="sxs-lookup"><span data-stu-id="850f2-154">-SeverityCondition</span></span>
<span data-ttu-id="850f2-155">Erwartetes Format – { \<operation\> : \<comma separated list of values\> } Für z. B.</span><span class="sxs-lookup"><span data-stu-id="850f2-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="850f2-156">Equals:Sev0,Sev1</span><span class="sxs-lookup"><span data-stu-id="850f2-156">Equals:Sev0,Sev1</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850f2-157">-Status</span><span class="sxs-lookup"><span data-stu-id="850f2-157">-Status</span></span>
<span data-ttu-id="850f2-158">Status der Aktionsregel.</span><span class="sxs-lookup"><span data-stu-id="850f2-158">Status of Action Rule.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850f2-159">-1295</span><span class="sxs-lookup"><span data-stu-id="850f2-159">-SuppressionEndTime</span></span>
<span data-ttu-id="850f2-160">Endzeit für Ende der Endzeit.</span><span class="sxs-lookup"><span data-stu-id="850f2-160">Suppression End Time.</span></span>
<span data-ttu-id="850f2-161">Format 09.12.2018 06:00:00 + sollte im Fall von Reccurent Supression Schedule - Once, Daily, Weekly oder Monthly erwähnt werden.</span><span class="sxs-lookup"><span data-stu-id="850f2-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850f2-162">-VornausstartZeit</span><span class="sxs-lookup"><span data-stu-id="850f2-162">-SuppressionStartTime</span></span>
<span data-ttu-id="850f2-163">Startzeit der 1-1-Prozent-Zeit.</span><span class="sxs-lookup"><span data-stu-id="850f2-163">Suppression Start Time.</span></span>
<span data-ttu-id="850f2-164">Format 09.12.2018 06:00:00 + sollte im Fall von Reccurent Supression Schedule - Once, Daily, Weekly oder Monthly erwähnt werden.</span><span class="sxs-lookup"><span data-stu-id="850f2-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850f2-165">-TargetResourceTypeCondition</span><span class="sxs-lookup"><span data-stu-id="850f2-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="850f2-166">Erwartetes Format – { \<operation\> : \<comma separated list of values\> } Für z. B.</span><span class="sxs-lookup"><span data-stu-id="850f2-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="850f2-167">Contains:Virtual Machines,Storage Account</span><span class="sxs-lookup"><span data-stu-id="850f2-167">Contains:Virtual Machines,Storage Account</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850f2-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="850f2-168">-Confirm</span></span>
<span data-ttu-id="850f2-169">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="850f2-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="850f2-170">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="850f2-170">-WhatIf</span></span>
<span data-ttu-id="850f2-171">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="850f2-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="850f2-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="850f2-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="850f2-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="850f2-173">CommonParameters</span></span>
<span data-ttu-id="850f2-174">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="850f2-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="850f2-175">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="850f2-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="850f2-176">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="850f2-176">INPUTS</span></span>

### <span data-ttu-id="850f2-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="850f2-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="850f2-178">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="850f2-178">OUTPUTS</span></span>

### <span data-ttu-id="850f2-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="850f2-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="850f2-180">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="850f2-180">NOTES</span></span>

## <span data-ttu-id="850f2-181">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="850f2-181">RELATED LINKS</span></span>
