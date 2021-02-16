---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
ms.openlocfilehash: 56f1878507424c1396130aa91a5fc7b086f101c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158433"
---
# <span data-ttu-id="8219a-101">Update-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="8219a-101">Update-AzSentinelAlertRule</span></span>

## <span data-ttu-id="8219a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8219a-102">SYNOPSIS</span></span>
<span data-ttu-id="8219a-103">Erstellen sie eine Analyse (Warnungsregel).</span><span class="sxs-lookup"><span data-stu-id="8219a-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="8219a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8219a-104">SYNTAX</span></span>

### <span data-ttu-id="8219a-105">AlertRuleId (Standard)</span><span class="sxs-lookup"><span data-stu-id="8219a-105">AlertRuleId (Default)</span></span>
```
Update-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled] [-DisplayName <String>]
 [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8219a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8219a-106">InputObject</span></span>
```
Update-AzSentinelAlertRule [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled]
 [-DisplayName <String>] [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] -InputObject <PSSentinelAlertRule>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8219a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8219a-107">ResourceId</span></span>
```
Update-AzSentinelAlertRule [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled]
 [-DisplayName <String>] [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8219a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8219a-108">DESCRIPTION</span></span>
<span data-ttu-id="8219a-109">Das **Cmdlet "Update-AzSentinelAlertRule"** aktualisiert eine analytische (Warnungsregel) im angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="8219a-109">The **Update-AzSentinelAlertRule** cmdlet updates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="8219a-110">Sie können "-InputObject", "-ResourceId" oder "-AlertId" verwenden.</span><span class="sxs-lookup"><span data-stu-id="8219a-110">You can use an -InputObject or -ResourceId or -AlertId.</span></span>  <span data-ttu-id="8219a-111">Sie können 1 oder mehr Proprtery-Schreibwaren aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="8219a-111">You can update 1 or more proprtery parmaters.</span></span>
<span data-ttu-id="8219a-112">Sie können den Parameter *"Bestätigen"* und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="8219a-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>


## <span data-ttu-id="8219a-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8219a-113">EXAMPLES</span></span>

### <span data-ttu-id="8219a-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8219a-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -Disabled -DisplayName "Disabled-AlertRuleDisplayName"
```

<span data-ttu-id="8219a-115">In diesem Beispiel wird **eine Warnungs-Benachrichtigung** aktualisiert, die die Einstellung auf *"Deaktiviert"* festgelegt hat, und in *"Disabled-AlertRuleDisplayName" umbenannt.*</span><span class="sxs-lookup"><span data-stu-id="8219a-115">This example updates an **AlertRule** setting it to *Disabled* and renames to *Disabled-AlertRuleDisplayName*.</span></span>  <span data-ttu-id="8219a-116">Alle anderen Eigenschaften bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="8219a-116">All other properties will remain the same.</span></span>

### <span data-ttu-id="8219a-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8219a-117">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
PS C:\> Update-AzSentinelAlertRule -InputObject $AlertRule -Disabled
```

<span data-ttu-id="8219a-118">In diesem Beispiel wird **eine AlertRule mit** einer Eingabeobjekteinstellung auf "Deaktiviert" *aktualisiert.*</span><span class="sxs-lookup"><span data-stu-id="8219a-118">This example updates an **AlertRule** using an InputObject setting it to *Disabled*.</span></span>  <span data-ttu-id="8219a-119">Alle anderen Eigenschaften bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="8219a-119">All other properties will remain the same.</span></span>


## <span data-ttu-id="8219a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8219a-120">PARAMETERS</span></span>

### <span data-ttu-id="8219a-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="8219a-121">-AlertRuleId</span></span>
<span data-ttu-id="8219a-122">Warnungsregel-ID.</span><span class="sxs-lookup"><span data-stu-id="8219a-122">Alert Rule Id.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="8219a-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="8219a-124">Warnungsregelvorlage.</span><span class="sxs-lookup"><span data-stu-id="8219a-124">Alert Rule Template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8219a-125">-DefaultProfile</span></span>
<span data-ttu-id="8219a-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8219a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-127">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8219a-127">-Description</span></span>
<span data-ttu-id="8219a-128">Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="8219a-128">Description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-129">-Disabled</span><span class="sxs-lookup"><span data-stu-id="8219a-129">-Disabled</span></span>
<span data-ttu-id="8219a-130">Warnungsregel deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8219a-130">Alert Rule Disabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8219a-131">-DisplayName</span></span>
<span data-ttu-id="8219a-132">Anzeigename der Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="8219a-132">Alert Rule Display Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-133">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="8219a-133">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="8219a-134">Warnungsregelanzeigenamen schließen Filter aus.</span><span class="sxs-lookup"><span data-stu-id="8219a-134">Alert Rule Display Names Exclude Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-135">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="8219a-135">-DisplayNamesFilter</span></span>
<span data-ttu-id="8219a-136">Filter für Warnungsregelanzeigenamen</span><span class="sxs-lookup"><span data-stu-id="8219a-136">Alert Rule Display Names Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-137">-Enabled</span><span class="sxs-lookup"><span data-stu-id="8219a-137">-Enabled</span></span>
<span data-ttu-id="8219a-138">Warnungsregel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8219a-138">Alert Rule Enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8219a-139">-InputObject</span></span>
<span data-ttu-id="8219a-140">InputObject.</span><span class="sxs-lookup"><span data-stu-id="8219a-140">InputObject.</span></span>

```yaml
Type: PSSentinelAlertRule
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="8219a-141">-ProductFilter</span></span>
<span data-ttu-id="8219a-142">Warnungsregel: Produktfilter.</span><span class="sxs-lookup"><span data-stu-id="8219a-142">Alert Rule Product Filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Azure Active Directory Identity Protection, Azure Advanced Threat Protection, Azure Security Center, Azure Security Center for IoT, Microsoft Cloud App Security, Microsoft Defender Advanced Threat Protection, Office 365 Advanced Threat Protection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-143">-Query</span><span class="sxs-lookup"><span data-stu-id="8219a-143">-Query</span></span>
<span data-ttu-id="8219a-144">Warnungsregelabfrage.</span><span class="sxs-lookup"><span data-stu-id="8219a-144">Alert Rule Query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="8219a-145">-QueryFrequency</span></span>
<span data-ttu-id="8219a-146">Häufigkeit der Warnungsregelabfrage.</span><span class="sxs-lookup"><span data-stu-id="8219a-146">Alert Rule Query Frequency.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="8219a-147">-QueryPeriod</span></span>
<span data-ttu-id="8219a-148">Zeitraum für Warnungsregelabfragen.</span><span class="sxs-lookup"><span data-stu-id="8219a-148">Alert Rule Query Period.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8219a-149">-ResourceGroupName</span></span>
<span data-ttu-id="8219a-150">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="8219a-150">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8219a-151">-ResourceId</span></span>
<span data-ttu-id="8219a-152">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="8219a-152">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="8219a-153">-SeveritiesFilter</span></span>
<span data-ttu-id="8219a-154">Filter für den Schweregrad von Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="8219a-154">Alert Rule Severities Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-155">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="8219a-155">-Severity</span></span>
<span data-ttu-id="8219a-156">Schweregrad des Vorfalls.</span><span class="sxs-lookup"><span data-stu-id="8219a-156">Incident Severity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-157">-Veranlagungsdisabled</span><span class="sxs-lookup"><span data-stu-id="8219a-157">-SuppressionDisabled</span></span>
<span data-ttu-id="8219a-158">Warnungsregel deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8219a-158">Alert Rule Suppression Disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-159">-1-1-1-4</span><span class="sxs-lookup"><span data-stu-id="8219a-159">-SuppressionDuration</span></span>
<span data-ttu-id="8219a-160">Warnungsregel, Dauer der Warnregel.</span><span class="sxs-lookup"><span data-stu-id="8219a-160">Alert Rule Suppression Duration.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-161">-Nenabled</span><span class="sxs-lookup"><span data-stu-id="8219a-161">-SuppressionEnabled</span></span>
<span data-ttu-id="8219a-162">Warnungsregel nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8219a-162">Alert Rule Suppression Enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-163">-Taktiken</span><span class="sxs-lookup"><span data-stu-id="8219a-163">-Tactics</span></span>
<span data-ttu-id="8219a-164">Warnungsregeltaktiken.</span><span class="sxs-lookup"><span data-stu-id="8219a-164">Alert Rule Tactics.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-165">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="8219a-165">-TriggerOperator</span></span>
<span data-ttu-id="8219a-166">Warnungsregelauslöseroperator.</span><span class="sxs-lookup"><span data-stu-id="8219a-166">Alert Rule Trigger Operator.</span></span>

```yaml
Type: TriggerOperator
Parameter Sets: (All)
Aliases:
Accepted values: GreaterThan, LessThan, Equal, NotEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-167">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="8219a-167">-TriggerThreshold</span></span>
<span data-ttu-id="8219a-168">Schwellenwert für warnungsregelauslöser.</span><span class="sxs-lookup"><span data-stu-id="8219a-168">Alert Rule Trigger Threshold.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-169">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8219a-169">-WorkspaceName</span></span>
<span data-ttu-id="8219a-170">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="8219a-170">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8219a-171">-Confirm</span></span>
<span data-ttu-id="8219a-172">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8219a-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-173">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8219a-173">-WhatIf</span></span>
<span data-ttu-id="8219a-174">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8219a-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8219a-175">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8219a-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8219a-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8219a-176">CommonParameters</span></span>
<span data-ttu-id="8219a-177">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8219a-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8219a-178">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8219a-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8219a-179">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8219a-179">INPUTS</span></span>

### <span data-ttu-id="8219a-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="8219a-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="8219a-181">System.String</span><span class="sxs-lookup"><span data-stu-id="8219a-181">System.String</span></span>

## <span data-ttu-id="8219a-182">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8219a-182">OUTPUTS</span></span>

### <span data-ttu-id="8219a-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="8219a-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

## <span data-ttu-id="8219a-184">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8219a-184">NOTES</span></span>

## <span data-ttu-id="8219a-185">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8219a-185">RELATED LINKS</span></span>
