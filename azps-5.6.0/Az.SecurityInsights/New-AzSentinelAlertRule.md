---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
ms.openlocfilehash: 0efb30f9c740362ac6e8c432179599c7d4aef88d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930800"
---
# <span data-ttu-id="dc837-101">New-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="dc837-101">New-AzSentinelAlertRule</span></span>

## <span data-ttu-id="dc837-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc837-102">SYNOPSIS</span></span>
<span data-ttu-id="dc837-103">Erstellen sie eine Analyse (Warnungsregel).</span><span class="sxs-lookup"><span data-stu-id="dc837-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="dc837-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc837-104">SYNTAX</span></span>

### <span data-ttu-id="dc837-105">ScheduledAlertRule (Standard)</span><span class="sxs-lookup"><span data-stu-id="dc837-105">ScheduledAlertRule (Default)</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Scheduled]
 [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled] -DisplayName <String>
 [-Description <String>] [-SuppressionDuration <TimeSpan>] [-SuppressionEnabled] -Query <String>
 -QueryFrequency <TimeSpan> -QueryPeriod <TimeSpan> -Severity <String>
 [-Tactics <System.Collections.Generic.IList`1[System.String]>] [-TriggerOperator <TriggerOperator>]
 -TriggerThreshold <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc837-106">FusionAlertRule</span><span class="sxs-lookup"><span data-stu-id="dc837-106">FusionAlertRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Fusion] [-AlertRuleId <String>]
 -AlertRuleTemplateName <String> [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc837-107">MicrosoftSecurityIncidentCreationRule</span><span class="sxs-lookup"><span data-stu-id="dc837-107">MicrosoftSecurityIncidentCreationRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-MicrosoftSecurityIncidentCreation] [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled]
 -DisplayName <String> -ProductFilter <String> [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc837-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc837-108">DESCRIPTION</span></span>
<span data-ttu-id="dc837-109">Das **Cmdlet New-AzSentinelAlertRule** erstellt im angegebenen Arbeitsbereich eine Analytische (Warnungsregel).</span><span class="sxs-lookup"><span data-stu-id="dc837-109">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="dc837-110">Sie müssen einen der drei Parameter *, Fusion*, *Scheduled* oder *MicrosoftSecurityIncidentCreation*, angeben, um die Art der zu erstellende Warnungsregel anzugeben.</span><span class="sxs-lookup"><span data-stu-id="dc837-110">You must specify one of the three parameters, *Fusion*, *Scheduled* or *MicrosoftSecurityIncidentCreation*, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="dc837-111">Jede Art verfügt über unterschiedliche erforderliche Paramater.</span><span class="sxs-lookup"><span data-stu-id="dc837-111">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="dc837-112">Sie können den Parameter *Bestätigen* und die $ConfirmPreference Windows PowerShell verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="dc837-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="dc837-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dc837-113">EXAMPLES</span></span>

### <span data-ttu-id="dc837-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dc837-114">Example 1</span></span>
```powershell
PS C:\>$AlertRuleTemplateName = "f71aba3d-28fb-450b-b192-4e76a83015c8"
PS C:\>$AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Fusion -Enabled -AlertRuleTemplateName $AlertRuleTemplateName
```

<span data-ttu-id="dc837-115">In diesem Beispiel wird eine  **AlertRule** der Fusion-Art basierend auf der Vorlage für die erweiterte mehrstufige *Angriffserkennung* erstellt und dann in der $AlertRule gespeichert.</span><span class="sxs-lookup"><span data-stu-id="dc837-115">This example creates a **AlertRule** of the *Fusion* kind based on the Template for *Advanced Multistage Attack Detection*, and then stores it in the $AlertRule variable.</span></span>

### <span data-ttu-id="dc837-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="dc837-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplateName = "a2e0eb51-1f11-461a-999b-cd0ebe5c7a72"
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftSecurityIncidentCreation -Enabled -AlertRuleTemplateName $AlertRuleTemplateName -DisplayName "Create incidents based on Azure Security Center for IoT" -ProductFilter "Azure Security Center for IoT"
```

<span data-ttu-id="dc837-117">In diesem Beispiel wird eine **AlertRule** der *MicrosoftSecurityIncidentCreation-Art* erstellt, die auf der Vorlage für Erstellen von Vorfällen basierend auf *Azure Security Center für IoT-Benachrichtigungen* basiert, und speichert sie dann im $AlertRule varaible.</span><span class="sxs-lookup"><span data-stu-id="dc837-117">This example creates a **AlertRule** of the *MicrosoftSecurityIncidentCreation* kind based on the template for *Create incidents based on Azure Security Center for IoT alerts*, and then stores it in the $AlertRule varaible.</span></span>

### <span data-ttu-id="dc837-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="dc837-118">Example 2</span></span>
```powershell
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Scheduled -Enabled -DisplayName "Powershell Exection Alert (Several Times per Hour)" -Severity Low -Query "SecurityEvent | where EventId == 4688" -QueryFrequency (New-TimeSpan -Hours 1) -QueryPeriod (New-TimeSpan -Hours 1) -TriggerThreshold 10
```

<span data-ttu-id="dc837-119">In diesem Beispiel wird ein **DataConnector** der Art *Scheduled* erstellt und dann im $AlertRule varaible gespeichert.</span><span class="sxs-lookup"><span data-stu-id="dc837-119">This example creates a **DataConnector** of the *Scheduled* kind, and then stores it in the $AlertRule varaible.</span></span>

## <span data-ttu-id="dc837-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dc837-120">PARAMETERS</span></span>

### <span data-ttu-id="dc837-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="dc837-121">-AlertRuleId</span></span>
<span data-ttu-id="dc837-122">Warnungsregel-ID.</span><span class="sxs-lookup"><span data-stu-id="dc837-122">Alert Rule Id.</span></span>

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

### <span data-ttu-id="dc837-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="dc837-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="dc837-124">Warnungsregelvorlage.</span><span class="sxs-lookup"><span data-stu-id="dc837-124">Alert Rule Template.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: FusionAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc837-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc837-125">-DefaultProfile</span></span>
<span data-ttu-id="dc837-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc837-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc837-127">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc837-127">-Description</span></span>
<span data-ttu-id="dc837-128">Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="dc837-128">Description.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc837-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dc837-129">-DisplayName</span></span>
<span data-ttu-id="dc837-130">Anzeigename der Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="dc837-130">Alert Rule Display Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc837-131">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="dc837-131">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="dc837-132">Warnungsregel Anzeigenamen Ausschließen Filter.</span><span class="sxs-lookup"><span data-stu-id="dc837-132">Alert Rule Display Names Exclude Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc837-133">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="dc837-133">-DisplayNamesFilter</span></span>
<span data-ttu-id="dc837-134">Warnungsregel Anzeigennamen filter.</span><span class="sxs-lookup"><span data-stu-id="dc837-134">Alert Rule Display Names Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc837-135">-Enabled</span><span class="sxs-lookup"><span data-stu-id="dc837-135">-Enabled</span></span>
<span data-ttu-id="dc837-136">Warnungsregel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="dc837-136">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="dc837-137">-Fusion</span><span class="sxs-lookup"><span data-stu-id="dc837-137">-Fusion</span></span>
<span data-ttu-id="dc837-138">Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="dc837-138">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FusionAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc837-139">-MicrosoftSecurityIncidentCreation</span><span class="sxs-lookup"><span data-stu-id="dc837-139">-MicrosoftSecurityIncidentCreation</span></span>
<span data-ttu-id="dc837-140">Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="dc837-140">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc837-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="dc837-141">-ProductFilter</span></span>
<span data-ttu-id="dc837-142">Produktfilter für Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="dc837-142">Alert Rule Product Filter.</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:
Accepted values: Azure Active Directory Identity Protection, Azure Advanced Threat Protection, Azure Security Center, Azure Security Center for IoT, Microsoft Cloud App Security, Microsoft Defender Advanced Threat Protection, Office 365 Advanced Threat Protection

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc837-143">-Query</span><span class="sxs-lookup"><span data-stu-id="dc837-143">-Query</span></span>
<span data-ttu-id="dc837-144">Warnungsregelabfrage.</span><span class="sxs-lookup"><span data-stu-id="dc837-144">Alert Rule Query.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc837-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="dc837-145">-QueryFrequency</span></span>
<span data-ttu-id="dc837-146">Abfragehäufigkeit der Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="dc837-146">Alert Rule Query Frequency.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc837-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="dc837-147">-QueryPeriod</span></span>
<span data-ttu-id="dc837-148">Abfragezeitraum für Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="dc837-148">Alert Rule Query Period.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc837-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc837-149">-ResourceGroupName</span></span>
<span data-ttu-id="dc837-150">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dc837-150">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc837-151">-Geplant</span><span class="sxs-lookup"><span data-stu-id="dc837-151">-Scheduled</span></span>
<span data-ttu-id="dc837-152">Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="dc837-152">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc837-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="dc837-153">-SeveritiesFilter</span></span>
<span data-ttu-id="dc837-154">Warnungsregelschwerefilter.</span><span class="sxs-lookup"><span data-stu-id="dc837-154">Alert Rule Severities Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc837-155">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="dc837-155">-Severity</span></span>
<span data-ttu-id="dc837-156">Schweregrad des Vorfalls.</span><span class="sxs-lookup"><span data-stu-id="dc837-156">Incident Severity.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc837-157">-VerdrängungDuration</span><span class="sxs-lookup"><span data-stu-id="dc837-157">-SuppressionDuration</span></span>
<span data-ttu-id="dc837-158">Warnungsregelunterdrückungsdauer.</span><span class="sxs-lookup"><span data-stu-id="dc837-158">Alert Rule Suppression Duration.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc837-159">-VerdrängungEnabled</span><span class="sxs-lookup"><span data-stu-id="dc837-159">-SuppressionEnabled</span></span>
<span data-ttu-id="dc837-160">Warnungsregelunterdrückung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="dc837-160">Alert Rule Suppression Enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc837-161">-Tactics</span><span class="sxs-lookup"><span data-stu-id="dc837-161">-Tactics</span></span>
<span data-ttu-id="dc837-162">Warnungsregeltaktik.</span><span class="sxs-lookup"><span data-stu-id="dc837-162">Alert Rule Tactics.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc837-163">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="dc837-163">-TriggerOperator</span></span>
<span data-ttu-id="dc837-164">Warnungsregeltriggeroperator.</span><span class="sxs-lookup"><span data-stu-id="dc837-164">Alert Rule Trigger Operator.</span></span>

```yaml
Type: Microsoft.Azure.Management.SecurityInsights.Models.TriggerOperator
Parameter Sets: ScheduledAlertRule
Aliases:
Accepted values: Equal, GreaterThan, LessThan, NotEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc837-165">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="dc837-165">-TriggerThreshold</span></span>
<span data-ttu-id="dc837-166">Schwellenwert für Benachrichtigungsregeltrigger.</span><span class="sxs-lookup"><span data-stu-id="dc837-166">Alert Rule Trigger Threshold.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc837-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dc837-167">-WorkspaceName</span></span>
<span data-ttu-id="dc837-168">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="dc837-168">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc837-169">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dc837-169">-Confirm</span></span>
<span data-ttu-id="dc837-170">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dc837-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc837-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc837-171">-WhatIf</span></span>
<span data-ttu-id="dc837-172">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc837-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc837-173">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dc837-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc837-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc837-174">CommonParameters</span></span>
<span data-ttu-id="dc837-175">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc837-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc837-176">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc837-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc837-177">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dc837-177">INPUTS</span></span>

### <span data-ttu-id="dc837-178">Keine</span><span class="sxs-lookup"><span data-stu-id="dc837-178">None</span></span>
## <span data-ttu-id="dc837-179">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dc837-179">OUTPUTS</span></span>

### <span data-ttu-id="dc837-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="dc837-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="dc837-181">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dc837-181">NOTES</span></span>

## <span data-ttu-id="dc837-182">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dc837-182">RELATED LINKS</span></span>
