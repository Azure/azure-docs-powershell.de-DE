---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: 15b847034300d01df354cc7512305ffd3cab8279
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658385"
---
# <span data-ttu-id="92404-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="92404-101">Set-AzActionRule</span></span>

## <span data-ttu-id="92404-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="92404-102">SYNOPSIS</span></span>
<span data-ttu-id="92404-103">Erstellen oder Aktualisieren einer Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="92404-103">Create or update an action rule.</span></span>

## <span data-ttu-id="92404-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="92404-104">SYNTAX</span></span>

### <span data-ttu-id="92404-105">BySimplifiedFormatDiagnosticsActionRule (Standard)</span><span class="sxs-lookup"><span data-stu-id="92404-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92404-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="92404-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92404-107">BySimplifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="92404-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92404-108">BySimplifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="92404-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92404-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92404-109">DESCRIPTION</span></span>
<span data-ttu-id="92404-110">Mit " **AzActionRule** " wird eine Aktionsregel erstellt oder aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="92404-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="92404-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92404-111">EXAMPLES</span></span>

### <span data-ttu-id="92404-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="92404-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="92404-113">Dieses Cmdlet erstellt eine Aktionsregel für Unterdrückung.</span><span class="sxs-lookup"><span data-stu-id="92404-113">This cmdlet creates an action rule for supression.</span></span>

### <span data-ttu-id="92404-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="92404-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="92404-115">Mit diesem Cmdlet wird eine Aktionsregel für die Aktionsgruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="92404-115">This cmdlet creates an action rule for action group.</span></span>

### <span data-ttu-id="92404-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="92404-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="92404-117">Dieses Cmdlet erstellt eine Aktionsregel für Diagnoseeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="92404-117">This cmdlet creates an action rule for diagnostics settings.</span></span>

## <span data-ttu-id="92404-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="92404-118">PARAMETERS</span></span>

### <span data-ttu-id="92404-119">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="92404-119">-ActionGroupId</span></span>
<span data-ttu-id="92404-120">Die Gruppen-ID der Aktion, die benachrichtigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="92404-120">Action Group Id which is to be notified.</span></span>

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

### <span data-ttu-id="92404-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="92404-121">-ActionRuleType</span></span>
<span data-ttu-id="92404-122">JSON-Format der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="92404-122">Action rule Json format</span></span>

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

### <span data-ttu-id="92404-123">-AlertContextCondition</span><span class="sxs-lookup"><span data-stu-id="92404-123">-AlertContextCondition</span></span>
<span data-ttu-id="92404-124">Erwartetes Format-{ \< Operation \> : \< durch Kommas getrennte Liste von Werten \> } für zB.</span><span class="sxs-lookup"><span data-stu-id="92404-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="92404-125">Enthält: Smartgroups</span><span class="sxs-lookup"><span data-stu-id="92404-125">Contains:smartgroups</span></span>

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

### <span data-ttu-id="92404-126">-AlertRuleIdCondition</span><span class="sxs-lookup"><span data-stu-id="92404-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="92404-127">Erwartetes Format-{ \< Operation \> : \< durch Kommas getrennte Liste von Werten \> } für zB.</span><span class="sxs-lookup"><span data-stu-id="92404-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="92404-128">Equals:/Subscriptions/ad825170-845c-47dB-8f00-11978947b089/resourceGroups/abvarma/Providers/Microsoft. Insights/metricAlerts/Test-mrmc-VM-abvarma</span><span class="sxs-lookup"><span data-stu-id="92404-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

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

### <span data-ttu-id="92404-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92404-129">-DefaultProfile</span></span>
<span data-ttu-id="92404-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="92404-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92404-131">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92404-131">-Description</span></span>
<span data-ttu-id="92404-132">Beschreibung der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="92404-132">Description of Action Rule</span></span>

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

### <span data-ttu-id="92404-133">-DescriptionCondition</span><span class="sxs-lookup"><span data-stu-id="92404-133">-DescriptionCondition</span></span>
<span data-ttu-id="92404-134">Erwartetes Format-{ \< Operation \> : \< durch Kommas getrennte Liste von Werten \> } für zB.</span><span class="sxs-lookup"><span data-stu-id="92404-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="92404-135">Enthält: Test Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="92404-135">Contains:Test Alert</span></span>

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

### <span data-ttu-id="92404-136">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="92404-136">-InputObject</span></span>
<span data-ttu-id="92404-137">Die Ressource "Aktionsregel"</span><span class="sxs-lookup"><span data-stu-id="92404-137">The action rule resource</span></span>

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

### <span data-ttu-id="92404-138">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="92404-138">-MonitorCondition</span></span>
<span data-ttu-id="92404-139">Erwartetes Format-{ \< Operation \> : \< durch Kommas getrennte Liste von Werten \> } für zB.</span><span class="sxs-lookup"><span data-stu-id="92404-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="92404-140">NotEquals: behoben</span><span class="sxs-lookup"><span data-stu-id="92404-140">NotEquals:Resolved</span></span>

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

### <span data-ttu-id="92404-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="92404-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="92404-142">Erwartetes Format-{ \< Operation \> : \< durch Kommas getrennte Liste von Werten \> } für zB.</span><span class="sxs-lookup"><span data-stu-id="92404-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="92404-143">Equals: Plattform, Protokollanalyse</span><span class="sxs-lookup"><span data-stu-id="92404-143">Equals:Platform,Log Analytics</span></span>

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

### <span data-ttu-id="92404-144">-Name</span><span class="sxs-lookup"><span data-stu-id="92404-144">-Name</span></span>
<span data-ttu-id="92404-145">Name der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="92404-145">Action rule Name</span></span>

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

### <span data-ttu-id="92404-146">-ReccurenceType</span><span class="sxs-lookup"><span data-stu-id="92404-146">-ReccurenceType</span></span>
<span data-ttu-id="92404-147">Gibt die Dauer an, zu der die Unterdrückung angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="92404-147">Specifies the duration when the suppression should be applied.</span></span>

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

### <span data-ttu-id="92404-148">-ReccurentValue</span><span class="sxs-lookup"><span data-stu-id="92404-148">-ReccurentValue</span></span>
<span data-ttu-id="92404-149">Reccurent-Werte (falls zutreffend). Im Fall von Weekly- \[ 1, 2 \] bei monatlichen- \[ 1, 3, 5, 30\]</span><span class="sxs-lookup"><span data-stu-id="92404-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

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

### <span data-ttu-id="92404-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92404-150">-ResourceGroupName</span></span>
<span data-ttu-id="92404-151">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="92404-151">Resource Group Name</span></span>

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

### <span data-ttu-id="92404-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="92404-152">-Scope</span></span>
<span data-ttu-id="92404-153">Durch trennzeichengetrennte Liste von Werten</span><span class="sxs-lookup"><span data-stu-id="92404-153">Comma separated list of values</span></span>

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

### <span data-ttu-id="92404-154">-SeverityCondition</span><span class="sxs-lookup"><span data-stu-id="92404-154">-SeverityCondition</span></span>
<span data-ttu-id="92404-155">Erwartetes Format-{ \< Operation \> : \< durch Kommas getrennte Liste von Werten \> } für zB.</span><span class="sxs-lookup"><span data-stu-id="92404-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="92404-156">Entspricht: Sev0, Sev1</span><span class="sxs-lookup"><span data-stu-id="92404-156">Equals:Sev0,Sev1</span></span>

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

### <span data-ttu-id="92404-157">-Status</span><span class="sxs-lookup"><span data-stu-id="92404-157">-Status</span></span>
<span data-ttu-id="92404-158">Status der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="92404-158">Status of Action Rule.</span></span>

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

### <span data-ttu-id="92404-159">-SuppressionEndTime</span><span class="sxs-lookup"><span data-stu-id="92404-159">-SuppressionEndTime</span></span>
<span data-ttu-id="92404-160">Endzeit des Unterdrückungs Zeitraums.</span><span class="sxs-lookup"><span data-stu-id="92404-160">Suppression End Time.</span></span>
<span data-ttu-id="92404-161">Das Format 12/09/2018 06:00:00 + sollte im Fall von Reccurent Unterdrückung Schedule-einmal, täglich, wöchentlich oder monatlich erwähnt werden.</span><span class="sxs-lookup"><span data-stu-id="92404-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="92404-162">-SuppressionStartTime</span><span class="sxs-lookup"><span data-stu-id="92404-162">-SuppressionStartTime</span></span>
<span data-ttu-id="92404-163">Anfangszeit der Unterdrückung</span><span class="sxs-lookup"><span data-stu-id="92404-163">Suppression Start Time.</span></span>
<span data-ttu-id="92404-164">Das Format 12/09/2018 06:00:00 + sollte im Fall von Reccurent Unterdrückung Schedule-einmal, täglich, wöchentlich oder monatlich erwähnt werden.</span><span class="sxs-lookup"><span data-stu-id="92404-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="92404-165">-TargetResourceTypeCondition</span><span class="sxs-lookup"><span data-stu-id="92404-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="92404-166">Erwartetes Format-{ \< Operation \> : \< durch Kommas getrennte Liste von Werten \> } für zB.</span><span class="sxs-lookup"><span data-stu-id="92404-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="92404-167">Enthält: virtuelle Computer, Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="92404-167">Contains:Virtual Machines,Storage Account</span></span>

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

### <span data-ttu-id="92404-168">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="92404-168">-Confirm</span></span>
<span data-ttu-id="92404-169">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="92404-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92404-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92404-170">-WhatIf</span></span>
<span data-ttu-id="92404-171">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92404-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92404-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92404-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92404-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92404-173">CommonParameters</span></span>
<span data-ttu-id="92404-174">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92404-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92404-175">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92404-175">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92404-176">Eingaben</span><span class="sxs-lookup"><span data-stu-id="92404-176">INPUTS</span></span>

### <span data-ttu-id="92404-177">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="92404-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="92404-178">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="92404-178">OUTPUTS</span></span>

### <span data-ttu-id="92404-179">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="92404-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="92404-180">Notizen</span><span class="sxs-lookup"><span data-stu-id="92404-180">NOTES</span></span>

## <span data-ttu-id="92404-181">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="92404-181">RELATED LINKS</span></span>
