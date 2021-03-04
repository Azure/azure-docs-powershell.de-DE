---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
ms.openlocfilehash: 86b6067e13a7b4d1d90e8fcb3d308af797dab354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927555"
---
# <span data-ttu-id="855b3-101">Update-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="855b3-101">Update-AzSentinelAlertRule</span></span>

## <span data-ttu-id="855b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="855b3-102">SYNOPSIS</span></span>
<span data-ttu-id="855b3-103">Erstellen sie eine Analyse (Warnungsregel).</span><span class="sxs-lookup"><span data-stu-id="855b3-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="855b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="855b3-104">SYNTAX</span></span>

### <span data-ttu-id="855b3-105">AlertRuleId (Standard)</span><span class="sxs-lookup"><span data-stu-id="855b3-105">AlertRuleId (Default)</span></span>
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

### <span data-ttu-id="855b3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="855b3-106">InputObject</span></span>
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

### <span data-ttu-id="855b3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="855b3-107">ResourceId</span></span>
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

## <span data-ttu-id="855b3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="855b3-108">DESCRIPTION</span></span>
<span data-ttu-id="855b3-109">Das **Cmdlet Update-AzSentinelAlertRule** aktualisiert eine Analytische (Warnungsregel) im angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="855b3-109">The **Update-AzSentinelAlertRule** cmdlet updates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="855b3-110">Sie können ein -InputObject oder -ResourceId oder -AlertId verwenden.</span><span class="sxs-lookup"><span data-stu-id="855b3-110">You can use an -InputObject or -ResourceId or -AlertId.</span></span>  <span data-ttu-id="855b3-111">Sie können 1 oder mehr proprtery-1-1-n aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="855b3-111">You can update 1 or more proprtery parmaters.</span></span>
<span data-ttu-id="855b3-112">Sie können den Parameter *Bestätigen* und die $ConfirmPreference Windows PowerShell verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="855b3-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>


## <span data-ttu-id="855b3-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="855b3-113">EXAMPLES</span></span>

### <span data-ttu-id="855b3-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="855b3-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -Disabled -DisplayName "Disabled-AlertRuleDisplayName"
```

<span data-ttu-id="855b3-115">In diesem Beispiel wird eine **AlertRule** aktualisiert, die sie auf *Deaktiviert festgelegt* hat, und in *Disabled-AlertRuleDisplayName umbenannt.*</span><span class="sxs-lookup"><span data-stu-id="855b3-115">This example updates an **AlertRule** setting it to *Disabled* and renames to *Disabled-AlertRuleDisplayName*.</span></span>  <span data-ttu-id="855b3-116">Alle anderen Eigenschaften bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="855b3-116">All other properties will remain the same.</span></span>

### <span data-ttu-id="855b3-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="855b3-117">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
PS C:\> Update-AzSentinelAlertRule -InputObject $AlertRule -Disabled
```

<span data-ttu-id="855b3-118">In diesem Beispiel wird eine **AlertRule aktualisiert,** indem ein InputObject-Objekt auf *Deaktiviert festlegen wird.*</span><span class="sxs-lookup"><span data-stu-id="855b3-118">This example updates an **AlertRule** using an InputObject setting it to *Disabled*.</span></span>  <span data-ttu-id="855b3-119">Alle anderen Eigenschaften bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="855b3-119">All other properties will remain the same.</span></span>


## <span data-ttu-id="855b3-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="855b3-120">PARAMETERS</span></span>

### <span data-ttu-id="855b3-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="855b3-121">-AlertRuleId</span></span>
<span data-ttu-id="855b3-122">Warnungsregel-ID.</span><span class="sxs-lookup"><span data-stu-id="855b3-122">Alert Rule Id.</span></span>

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

### <span data-ttu-id="855b3-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="855b3-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="855b3-124">Warnungsregelvorlage.</span><span class="sxs-lookup"><span data-stu-id="855b3-124">Alert Rule Template.</span></span>

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

### <span data-ttu-id="855b3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="855b3-125">-DefaultProfile</span></span>
<span data-ttu-id="855b3-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="855b3-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="855b3-127">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="855b3-127">-Description</span></span>
<span data-ttu-id="855b3-128">Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="855b3-128">Description.</span></span>

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

### <span data-ttu-id="855b3-129">-Disabled</span><span class="sxs-lookup"><span data-stu-id="855b3-129">-Disabled</span></span>
<span data-ttu-id="855b3-130">Warnungsregel deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="855b3-130">Alert Rule Disabled.</span></span>

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

### <span data-ttu-id="855b3-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="855b3-131">-DisplayName</span></span>
<span data-ttu-id="855b3-132">Anzeigename der Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="855b3-132">Alert Rule Display Name.</span></span>

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

### <span data-ttu-id="855b3-133">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="855b3-133">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="855b3-134">Warnungsregel Anzeigenamen Ausschließen Filter.</span><span class="sxs-lookup"><span data-stu-id="855b3-134">Alert Rule Display Names Exclude Filter.</span></span>

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

### <span data-ttu-id="855b3-135">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="855b3-135">-DisplayNamesFilter</span></span>
<span data-ttu-id="855b3-136">Warnungsregel Anzeigennamen filter.</span><span class="sxs-lookup"><span data-stu-id="855b3-136">Alert Rule Display Names Filter.</span></span>

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

### <span data-ttu-id="855b3-137">-Enabled</span><span class="sxs-lookup"><span data-stu-id="855b3-137">-Enabled</span></span>
<span data-ttu-id="855b3-138">Warnungsregel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="855b3-138">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="855b3-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="855b3-139">-InputObject</span></span>
<span data-ttu-id="855b3-140">InputObject.</span><span class="sxs-lookup"><span data-stu-id="855b3-140">InputObject.</span></span>

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

### <span data-ttu-id="855b3-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="855b3-141">-ProductFilter</span></span>
<span data-ttu-id="855b3-142">Produktfilter für Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="855b3-142">Alert Rule Product Filter.</span></span>

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

### <span data-ttu-id="855b3-143">-Query</span><span class="sxs-lookup"><span data-stu-id="855b3-143">-Query</span></span>
<span data-ttu-id="855b3-144">Warnungsregelabfrage.</span><span class="sxs-lookup"><span data-stu-id="855b3-144">Alert Rule Query.</span></span>

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

### <span data-ttu-id="855b3-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="855b3-145">-QueryFrequency</span></span>
<span data-ttu-id="855b3-146">Abfragehäufigkeit der Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="855b3-146">Alert Rule Query Frequency.</span></span>

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

### <span data-ttu-id="855b3-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="855b3-147">-QueryPeriod</span></span>
<span data-ttu-id="855b3-148">Abfragezeitraum für Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="855b3-148">Alert Rule Query Period.</span></span>

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

### <span data-ttu-id="855b3-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="855b3-149">-ResourceGroupName</span></span>
<span data-ttu-id="855b3-150">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="855b3-150">Resource group name.</span></span>

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

### <span data-ttu-id="855b3-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="855b3-151">-ResourceId</span></span>
<span data-ttu-id="855b3-152">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="855b3-152">Resource Id.</span></span>

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

### <span data-ttu-id="855b3-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="855b3-153">-SeveritiesFilter</span></span>
<span data-ttu-id="855b3-154">Warnungsregelschwerefilter.</span><span class="sxs-lookup"><span data-stu-id="855b3-154">Alert Rule Severities Filter.</span></span>

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

### <span data-ttu-id="855b3-155">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="855b3-155">-Severity</span></span>
<span data-ttu-id="855b3-156">Schweregrad des Vorfalls.</span><span class="sxs-lookup"><span data-stu-id="855b3-156">Incident Severity.</span></span>

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

### <span data-ttu-id="855b3-157">-VerdrängungDisabled</span><span class="sxs-lookup"><span data-stu-id="855b3-157">-SuppressionDisabled</span></span>
<span data-ttu-id="855b3-158">Warnungsregelunterdrückung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="855b3-158">Alert Rule Suppression Disabled.</span></span>

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

### <span data-ttu-id="855b3-159">-VerdrängungDuration</span><span class="sxs-lookup"><span data-stu-id="855b3-159">-SuppressionDuration</span></span>
<span data-ttu-id="855b3-160">Warnungsregelunterdrückungsdauer.</span><span class="sxs-lookup"><span data-stu-id="855b3-160">Alert Rule Suppression Duration.</span></span>

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

### <span data-ttu-id="855b3-161">-VerdrängungEnabled</span><span class="sxs-lookup"><span data-stu-id="855b3-161">-SuppressionEnabled</span></span>
<span data-ttu-id="855b3-162">Warnungsregelunterdrückung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="855b3-162">Alert Rule Suppression Enabled.</span></span>

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

### <span data-ttu-id="855b3-163">-Tactics</span><span class="sxs-lookup"><span data-stu-id="855b3-163">-Tactics</span></span>
<span data-ttu-id="855b3-164">Warnungsregeltaktik.</span><span class="sxs-lookup"><span data-stu-id="855b3-164">Alert Rule Tactics.</span></span>

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

### <span data-ttu-id="855b3-165">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="855b3-165">-TriggerOperator</span></span>
<span data-ttu-id="855b3-166">Warnungsregeltriggeroperator.</span><span class="sxs-lookup"><span data-stu-id="855b3-166">Alert Rule Trigger Operator.</span></span>

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

### <span data-ttu-id="855b3-167">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="855b3-167">-TriggerThreshold</span></span>
<span data-ttu-id="855b3-168">Schwellenwert für Benachrichtigungsregeltrigger.</span><span class="sxs-lookup"><span data-stu-id="855b3-168">Alert Rule Trigger Threshold.</span></span>

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

### <span data-ttu-id="855b3-169">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="855b3-169">-WorkspaceName</span></span>
<span data-ttu-id="855b3-170">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="855b3-170">Workspace Name.</span></span>

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

### <span data-ttu-id="855b3-171">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="855b3-171">-Confirm</span></span>
<span data-ttu-id="855b3-172">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="855b3-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="855b3-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="855b3-173">-WhatIf</span></span>
<span data-ttu-id="855b3-174">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="855b3-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="855b3-175">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="855b3-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="855b3-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="855b3-176">CommonParameters</span></span>
<span data-ttu-id="855b3-177">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="855b3-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="855b3-178">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="855b3-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="855b3-179">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="855b3-179">INPUTS</span></span>

### <span data-ttu-id="855b3-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="855b3-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="855b3-181">System.String</span><span class="sxs-lookup"><span data-stu-id="855b3-181">System.String</span></span>

## <span data-ttu-id="855b3-182">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="855b3-182">OUTPUTS</span></span>

### <span data-ttu-id="855b3-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="855b3-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

## <span data-ttu-id="855b3-184">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="855b3-184">NOTES</span></span>

## <span data-ttu-id="855b3-185">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="855b3-185">RELATED LINKS</span></span>
