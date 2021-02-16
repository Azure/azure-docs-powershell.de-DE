---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
ms.openlocfilehash: 97a07b515cff6cfd8521033dbe7380eb2a7bc1d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168993"
---
# <span data-ttu-id="215ee-101">New-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="215ee-101">New-AzSentinelAlertRule</span></span>

## <span data-ttu-id="215ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="215ee-102">SYNOPSIS</span></span>
<span data-ttu-id="215ee-103">Erstellen sie eine Analytische (Warnungsregel).</span><span class="sxs-lookup"><span data-stu-id="215ee-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="215ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="215ee-104">SYNTAX</span></span>

### <span data-ttu-id="215ee-105">ScheduledAlertRule (Standard)</span><span class="sxs-lookup"><span data-stu-id="215ee-105">ScheduledAlertRule (Default)</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Scheduled]
 [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled] -DisplayName <String>
 [-Description <String>] [-SuppressionDuration <TimeSpan>] [-SuppressionEnabled] -Query <String>
 -QueryFrequency <TimeSpan> -QueryPeriod <TimeSpan> -Severity <String>
 [-Tactics <System.Collections.Generic.IList`1[System.String]>] [-TriggerOperator <TriggerOperator>]
 -TriggerThreshold <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="215ee-106">FusionAlertRule</span><span class="sxs-lookup"><span data-stu-id="215ee-106">FusionAlertRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Fusion] [-AlertRuleId <String>]
 -AlertRuleTemplateName <String> [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="215ee-107">MicrosoftSecurityIncidentCreationRule</span><span class="sxs-lookup"><span data-stu-id="215ee-107">MicrosoftSecurityIncidentCreationRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-MicrosoftSecurityIncidentCreation] [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled]
 -DisplayName <String> -ProductFilter <String> [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="215ee-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="215ee-108">DESCRIPTION</span></span>
<span data-ttu-id="215ee-109">Das **Cmdlet "New-AzSentinelAlertRule"** erstellt eine analytische (Warnungsregel) im angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="215ee-109">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="215ee-110">Sie müssen einen der drei Parameter *, Fusion*, *Scheduled* oder *MicrosoftSecurityIncidentCreation*– angeben, um die Art der zu erstellende Warnungsregel anzugeben.</span><span class="sxs-lookup"><span data-stu-id="215ee-110">You must specify one of the three parameters, *Fusion*, *Scheduled* or *MicrosoftSecurityIncidentCreation*, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="215ee-111">Jede Art hat unterschiedliche erforderliche Parameter.</span><span class="sxs-lookup"><span data-stu-id="215ee-111">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="215ee-112">Sie können den Parameter *"Bestätigen"* und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="215ee-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="215ee-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="215ee-113">EXAMPLES</span></span>

### <span data-ttu-id="215ee-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="215ee-114">Example 1</span></span>
```powershell
PS C:\>$AlertRuleTemplateName = "f71aba3d-28fb-450b-b192-4e76a83015c8"
PS C:\>$AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Fusion -Enabled -AlertRuleTemplateName $AlertRuleTemplateName
```

<span data-ttu-id="215ee-115">In diesem Beispiel wird eine **AlertRule** der Art *Fusion* basierend auf der Vorlage für die erweiterte *Multistage-Angriffserkennung* erstellt und dann in der $AlertRule gespeichert.</span><span class="sxs-lookup"><span data-stu-id="215ee-115">This example creates a **AlertRule** of the *Fusion* kind based on the Template for *Advanced Multistage Attack Detection*, and then stores it in the $AlertRule variable.</span></span>

### <span data-ttu-id="215ee-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="215ee-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplateName = "a2e0eb51-1f11-461a-999b-cd0ebe5c7a72"
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftSecurityIncidentCreation -Enabled -AlertRuleTemplateName $AlertRuleTemplateName -DisplayName "Create incidents based on Azure Security Center for IoT" -ProductFilter "Azure Security Center for IoT"
```

<span data-ttu-id="215ee-117">In diesem Beispiel wird eine **AlertRule** der Art *"MicrosoftSecurityIncidentCreation"* erstellt, die auf der Vorlage zum Erstellen von Vorfällen basiert, die auf Azure Security Center für *IoT-Warnungen* basiert, und speichert sie dann im $AlertRule varianzaible.</span><span class="sxs-lookup"><span data-stu-id="215ee-117">This example creates a **AlertRule** of the *MicrosoftSecurityIncidentCreation* kind based on the template for *Create incidents based on Azure Security Center for IoT alerts*, and then stores it in the $AlertRule varaible.</span></span>

### <span data-ttu-id="215ee-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="215ee-118">Example 2</span></span>
```powershell
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Scheduled -Enabled -DisplayName "Powershell Exection Alert (Several Times per Hour)" -Severity Low -Query "SecurityEvent | where EventId == 4688" -QueryFrequency (New-TimeSpan -Hours 1) -QueryPeriod (New-TimeSpan -Hours 1) -TriggerThreshold 10
```

<span data-ttu-id="215ee-119">In diesem Beispiel wird **ein DataConnector** der Art *"Geplant"* erstellt und dann im $AlertRule gespeichert.</span><span class="sxs-lookup"><span data-stu-id="215ee-119">This example creates a **DataConnector** of the *Scheduled* kind, and then stores it in the $AlertRule varaible.</span></span>

## <span data-ttu-id="215ee-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="215ee-120">PARAMETERS</span></span>

### <span data-ttu-id="215ee-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="215ee-121">-AlertRuleId</span></span>
<span data-ttu-id="215ee-122">Warnungsregel-ID.</span><span class="sxs-lookup"><span data-stu-id="215ee-122">Alert Rule Id.</span></span>

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

### <span data-ttu-id="215ee-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="215ee-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="215ee-124">Warnungsregelvorlage.</span><span class="sxs-lookup"><span data-stu-id="215ee-124">Alert Rule Template.</span></span>

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

### <span data-ttu-id="215ee-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="215ee-125">-DefaultProfile</span></span>
<span data-ttu-id="215ee-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="215ee-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="215ee-127">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="215ee-127">-Description</span></span>
<span data-ttu-id="215ee-128">Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="215ee-128">Description.</span></span>

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

### <span data-ttu-id="215ee-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="215ee-129">-DisplayName</span></span>
<span data-ttu-id="215ee-130">Anzeigename der Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="215ee-130">Alert Rule Display Name.</span></span>

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

### <span data-ttu-id="215ee-131">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="215ee-131">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="215ee-132">Warnungsregelanzeigenamen schließen Filter aus.</span><span class="sxs-lookup"><span data-stu-id="215ee-132">Alert Rule Display Names Exclude Filter.</span></span>

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

### <span data-ttu-id="215ee-133">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="215ee-133">-DisplayNamesFilter</span></span>
<span data-ttu-id="215ee-134">Filter für Warnungsregelanzeigenamen</span><span class="sxs-lookup"><span data-stu-id="215ee-134">Alert Rule Display Names Filter.</span></span>

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

### <span data-ttu-id="215ee-135">-Enabled</span><span class="sxs-lookup"><span data-stu-id="215ee-135">-Enabled</span></span>
<span data-ttu-id="215ee-136">Warnungsregel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="215ee-136">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="215ee-137">-Fusion</span><span class="sxs-lookup"><span data-stu-id="215ee-137">-Fusion</span></span>
<span data-ttu-id="215ee-138">Warnungsregel-Art.</span><span class="sxs-lookup"><span data-stu-id="215ee-138">Alert Rule Kind.</span></span>

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

### <span data-ttu-id="215ee-139">-MicrosoftSecurityIncidentCreation</span><span class="sxs-lookup"><span data-stu-id="215ee-139">-MicrosoftSecurityIncidentCreation</span></span>
<span data-ttu-id="215ee-140">Warnungsregel-Art.</span><span class="sxs-lookup"><span data-stu-id="215ee-140">Alert Rule Kind.</span></span>

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

### <span data-ttu-id="215ee-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="215ee-141">-ProductFilter</span></span>
<span data-ttu-id="215ee-142">Warnungsregel: Produktfilter.</span><span class="sxs-lookup"><span data-stu-id="215ee-142">Alert Rule Product Filter.</span></span>

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

### <span data-ttu-id="215ee-143">-Query</span><span class="sxs-lookup"><span data-stu-id="215ee-143">-Query</span></span>
<span data-ttu-id="215ee-144">Warnungsregelabfrage.</span><span class="sxs-lookup"><span data-stu-id="215ee-144">Alert Rule Query.</span></span>

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

### <span data-ttu-id="215ee-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="215ee-145">-QueryFrequency</span></span>
<span data-ttu-id="215ee-146">Häufigkeit der Warnungsregelabfrage.</span><span class="sxs-lookup"><span data-stu-id="215ee-146">Alert Rule Query Frequency.</span></span>

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

### <span data-ttu-id="215ee-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="215ee-147">-QueryPeriod</span></span>
<span data-ttu-id="215ee-148">Zeitraum für Warnungsregelabfragen.</span><span class="sxs-lookup"><span data-stu-id="215ee-148">Alert Rule Query Period.</span></span>

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

### <span data-ttu-id="215ee-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="215ee-149">-ResourceGroupName</span></span>
<span data-ttu-id="215ee-150">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="215ee-150">Resource group name.</span></span>

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

### <span data-ttu-id="215ee-151">-Geplant</span><span class="sxs-lookup"><span data-stu-id="215ee-151">-Scheduled</span></span>
<span data-ttu-id="215ee-152">Warnungsregel-Art.</span><span class="sxs-lookup"><span data-stu-id="215ee-152">Alert Rule Kind.</span></span>

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

### <span data-ttu-id="215ee-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="215ee-153">-SeveritiesFilter</span></span>
<span data-ttu-id="215ee-154">Filter für den Schweregrad von Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="215ee-154">Alert Rule Severities Filter.</span></span>

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

### <span data-ttu-id="215ee-155">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="215ee-155">-Severity</span></span>
<span data-ttu-id="215ee-156">Schweregrad des Vorfalls.</span><span class="sxs-lookup"><span data-stu-id="215ee-156">Incident Severity.</span></span>

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

### <span data-ttu-id="215ee-157">-1-1-1-4</span><span class="sxs-lookup"><span data-stu-id="215ee-157">-SuppressionDuration</span></span>
<span data-ttu-id="215ee-158">Warnungsregel, Dauer der Warnregel.</span><span class="sxs-lookup"><span data-stu-id="215ee-158">Alert Rule Suppression Duration.</span></span>

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

### <span data-ttu-id="215ee-159">-Nenabled</span><span class="sxs-lookup"><span data-stu-id="215ee-159">-SuppressionEnabled</span></span>
<span data-ttu-id="215ee-160">Warnungsregel nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="215ee-160">Alert Rule Suppression Enabled.</span></span>

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

### <span data-ttu-id="215ee-161">-Taktiken</span><span class="sxs-lookup"><span data-stu-id="215ee-161">-Tactics</span></span>
<span data-ttu-id="215ee-162">Warnungsregeltaktiken.</span><span class="sxs-lookup"><span data-stu-id="215ee-162">Alert Rule Tactics.</span></span>

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

### <span data-ttu-id="215ee-163">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="215ee-163">-TriggerOperator</span></span>
<span data-ttu-id="215ee-164">Warnungsregelauslöseroperator.</span><span class="sxs-lookup"><span data-stu-id="215ee-164">Alert Rule Trigger Operator.</span></span>

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

### <span data-ttu-id="215ee-165">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="215ee-165">-TriggerThreshold</span></span>
<span data-ttu-id="215ee-166">Schwellenwert für warnungsregelauslöser.</span><span class="sxs-lookup"><span data-stu-id="215ee-166">Alert Rule Trigger Threshold.</span></span>

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

### <span data-ttu-id="215ee-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="215ee-167">-WorkspaceName</span></span>
<span data-ttu-id="215ee-168">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="215ee-168">Workspace Name.</span></span>

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

### <span data-ttu-id="215ee-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="215ee-169">-Confirm</span></span>
<span data-ttu-id="215ee-170">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="215ee-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="215ee-171">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="215ee-171">-WhatIf</span></span>
<span data-ttu-id="215ee-172">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="215ee-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="215ee-173">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="215ee-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="215ee-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="215ee-174">CommonParameters</span></span>
<span data-ttu-id="215ee-175">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="215ee-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="215ee-176">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="215ee-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="215ee-177">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="215ee-177">INPUTS</span></span>

### <span data-ttu-id="215ee-178">Keine</span><span class="sxs-lookup"><span data-stu-id="215ee-178">None</span></span>
## <span data-ttu-id="215ee-179">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="215ee-179">OUTPUTS</span></span>

### <span data-ttu-id="215ee-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="215ee-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="215ee-181">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="215ee-181">NOTES</span></span>

## <span data-ttu-id="215ee-182">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="215ee-182">RELATED LINKS</span></span>
