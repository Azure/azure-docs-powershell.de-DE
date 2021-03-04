---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: aeb86609e06417147f5ef4600c430665f28da454
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937483"
---
# <span data-ttu-id="9a6df-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="9a6df-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="9a6df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a6df-102">SYNOPSIS</span></span>
<span data-ttu-id="9a6df-103">Erstellt und startet eine Richtliniensanierung für eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="9a6df-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="9a6df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a6df-104">SYNTAX</span></span>

### <span data-ttu-id="9a6df-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9a6df-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a6df-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9a6df-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a6df-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a6df-107">DESCRIPTION</span></span>
<span data-ttu-id="9a6df-108">Das **Cmdlet Start-AzPolicyRemediation** erstellt eine Richtliniensanierung für eine bestimmte Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="9a6df-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="9a6df-109">Alle nicht kompatiblen Ressourcen am oder unterhalb des Umfangs der Behebung werden behoben.</span><span class="sxs-lookup"><span data-stu-id="9a6df-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="9a6df-110">Die Behebung wird nur für Richtlinien mit dem Effekt "deployIfNotExists" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9a6df-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="9a6df-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9a6df-111">EXAMPLES</span></span>

### <span data-ttu-id="9a6df-112">Beispiel 1: Starten einer Behebung im Abonnementbereich</span><span class="sxs-lookup"><span data-stu-id="9a6df-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="9a6df-113">Mit diesem Befehl wird eine neue Richtliniensanierung im Abonnement "Mein Abonnement" für die angegebene Richtlinienzuordnung erstellt.</span><span class="sxs-lookup"><span data-stu-id="9a6df-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="9a6df-114">Beispiel 2: Starten einer Behebung im Bereich der Verwaltungsgruppe mit optionalen Filtern</span><span class="sxs-lookup"><span data-stu-id="9a6df-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="9a6df-115">Mit diesem Befehl wird eine neue Richtliniensanierung in der Verwaltungsgruppe "mg1" für die angegebene Richtlinienzuordnung erstellt.</span><span class="sxs-lookup"><span data-stu-id="9a6df-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="9a6df-116">Nur Ressourcen in den Speicherorten "westus" oder "eastus" werden behoben.</span><span class="sxs-lookup"><span data-stu-id="9a6df-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="9a6df-117">Beispiel 3: Starten einer Behebung im Ressourcengruppenbereich für eine Zuordnung zur Definition des Richtliniensatzs</span><span class="sxs-lookup"><span data-stu-id="9a6df-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="9a6df-118">Mit diesem Befehl wird eine neue Richtliniensanierung in der Ressourcengruppe "myRG" für die angegebene Richtlinienzuordnung erstellt.</span><span class="sxs-lookup"><span data-stu-id="9a6df-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="9a6df-119">Die Richtlinienzuordnung weist eine Richtliniensatzdefinition (auch als Initiative bekannt) zu.</span><span class="sxs-lookup"><span data-stu-id="9a6df-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="9a6df-120">Die Richtliniendefinitionsreferenz-ID gibt an, welche Richtlinie innerhalb der Initiative behoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a6df-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="9a6df-121">Beispiel 4: Starten einer Behebung und Warten, bis sie im Hintergrund abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="9a6df-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="9a6df-122">Mit diesem Befehl wird eine neue Richtliniensanierung im Abonnement "Mein Abonnement" für die angegebene Richtlinienzuordnung gestartet.</span><span class="sxs-lookup"><span data-stu-id="9a6df-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="9a6df-123">Sie wartet, bis die Behebung abgeschlossen ist, bevor sie den endgültigen Behebungsstatus zurück gibt.</span><span class="sxs-lookup"><span data-stu-id="9a6df-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

### <span data-ttu-id="9a6df-124">Beispiel 5: Starten einer Behebung, bei der nicht kompatible Ressourcen ermittelt werden, bevor sie behoben werden</span><span class="sxs-lookup"><span data-stu-id="9a6df-124">Example 5: Start a remediation that will discover non-compliant resources before remediating</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -ResourceDiscoveryMode ReEvaluateCompliance
```

<span data-ttu-id="9a6df-125">Mit diesem Befehl wird eine neue Richtliniensanierung im Abonnement "Mein Abonnement" für die angegebene Richtlinienzuordnung erstellt.</span><span class="sxs-lookup"><span data-stu-id="9a6df-125">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="9a6df-126">Der Compliancestatus der Ressourcen im Abonnement wird anhand der Richtlinienzuordnung neu ausgewertet, und nicht kompatible Ressourcen werden behoben.</span><span class="sxs-lookup"><span data-stu-id="9a6df-126">The compliance state of resources in the subscription will be re-evaluated against the policy assignment and non-compliant resources will be remediated.</span></span>

## <span data-ttu-id="9a6df-127">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9a6df-127">PARAMETERS</span></span>

### <span data-ttu-id="9a6df-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a6df-128">-AsJob</span></span>
<span data-ttu-id="9a6df-129">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="9a6df-129">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="9a6df-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a6df-130">-DefaultProfile</span></span>
<span data-ttu-id="9a6df-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9a6df-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a6df-132">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="9a6df-132">-LocationFilter</span></span>
<span data-ttu-id="9a6df-133">Die Ressourcenstandorte, die in die Behebung einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9a6df-133">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="9a6df-134">Ressourcen, die sich nicht an diesen Speicherorten befinden, werden nicht behoben.</span><span class="sxs-lookup"><span data-stu-id="9a6df-134">Resources that don't reside in these locations will not be remediated.</span></span>

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

### <span data-ttu-id="9a6df-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="9a6df-135">-ManagementGroupName</span></span>
<span data-ttu-id="9a6df-136">Verwaltungsgruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="9a6df-136">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6df-137">-Name</span><span class="sxs-lookup"><span data-stu-id="9a6df-137">-Name</span></span>
<span data-ttu-id="9a6df-138">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="9a6df-138">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6df-139">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="9a6df-139">-PolicyAssignmentId</span></span>
<span data-ttu-id="9a6df-140">Richtlinienzuordnungs-ID.</span><span class="sxs-lookup"><span data-stu-id="9a6df-140">Policy assignment ID.</span></span>
<span data-ttu-id="9a6df-141">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9a6df-141">E.g.</span></span>
<span data-ttu-id="9a6df-142">"/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}".</span><span class="sxs-lookup"><span data-stu-id="9a6df-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="9a6df-143">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="9a6df-143">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="9a6df-144">Ruft die Richtliniendefinitionsreferenz-ID der einzelnen Definition ab, die behoben wird.</span><span class="sxs-lookup"><span data-stu-id="9a6df-144">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="9a6df-145">Erforderlich, wenn die Richtlinienzuordnung eine Richtliniensatzdefinition zu weist.</span><span class="sxs-lookup"><span data-stu-id="9a6df-145">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="9a6df-146">-ResourceDiscoveryMode</span><span class="sxs-lookup"><span data-stu-id="9a6df-146">-ResourceDiscoveryMode</span></span>
<span data-ttu-id="9a6df-147">Beschreibt, wie der Behebungsaufgabe Ressourcen ermittelt, die behoben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="9a6df-147">Describes how the remediation task will discover resources that need to be remediated.</span></span>
<span data-ttu-id="9a6df-148">ReEvaluateCompliance wird nicht unterstützt, wenn Verwaltungsgruppenbereiche behoben werden.</span><span class="sxs-lookup"><span data-stu-id="9a6df-148">ReEvaluateCompliance is not supported when remediating management group scopes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ExistingNonCompliant, ReEvaluateCompliance

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6df-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a6df-149">-ResourceGroupName</span></span>
<span data-ttu-id="9a6df-150">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9a6df-150">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6df-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a6df-151">-ResourceId</span></span>
<span data-ttu-id="9a6df-152">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9a6df-152">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6df-153">-Scope</span><span class="sxs-lookup"><span data-stu-id="9a6df-153">-Scope</span></span>
<span data-ttu-id="9a6df-154">Bereich der Ressource.</span><span class="sxs-lookup"><span data-stu-id="9a6df-154">Scope of the resource.</span></span>
<span data-ttu-id="9a6df-155">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9a6df-155">E.g.</span></span>
<span data-ttu-id="9a6df-156">"/subscriptions/{subscriptionId}/resourceGroups/{rgName}".</span><span class="sxs-lookup"><span data-stu-id="9a6df-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6df-157">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9a6df-157">-Confirm</span></span>
<span data-ttu-id="9a6df-158">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9a6df-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a6df-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a6df-159">-WhatIf</span></span>
<span data-ttu-id="9a6df-160">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9a6df-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a6df-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a6df-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a6df-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a6df-162">CommonParameters</span></span>
<span data-ttu-id="9a6df-163">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a6df-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a6df-164">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a6df-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a6df-165">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9a6df-165">INPUTS</span></span>

### <span data-ttu-id="9a6df-166">System.String</span><span class="sxs-lookup"><span data-stu-id="9a6df-166">System.String</span></span>

### <span data-ttu-id="9a6df-167">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9a6df-167">System.String[]</span></span>

## <span data-ttu-id="9a6df-168">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9a6df-168">OUTPUTS</span></span>

### <span data-ttu-id="9a6df-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="9a6df-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="9a6df-170">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9a6df-170">NOTES</span></span>

## <span data-ttu-id="9a6df-171">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9a6df-171">RELATED LINKS</span></span>
