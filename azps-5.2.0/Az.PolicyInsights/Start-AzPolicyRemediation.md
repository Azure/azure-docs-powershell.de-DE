---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: e4a0e3ad4ffac7e610f5807c7687cdc1bf548770
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369240"
---
# <span data-ttu-id="b59a1-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="b59a1-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="b59a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b59a1-102">SYNOPSIS</span></span>
<span data-ttu-id="b59a1-103">Erstellt und startet eine Richtlinienbehebung für eine Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="b59a1-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="b59a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b59a1-104">SYNTAX</span></span>

### <span data-ttu-id="b59a1-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b59a1-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b59a1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b59a1-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b59a1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b59a1-107">DESCRIPTION</span></span>
<span data-ttu-id="b59a1-108">Das **Cmdlet "Start-AzPolicyRemediation"** erstellt eine Richtlinienbehebung für eine bestimmte Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="b59a1-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="b59a1-109">Alle nicht kompatiblen Ressourcen im oder unter dem Bereich der Problembehebung werden behoben.</span><span class="sxs-lookup"><span data-stu-id="b59a1-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="b59a1-110">Die Wartung wird nur für Richtlinien mit dem Effekt "deployIfNotExists" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b59a1-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="b59a1-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b59a1-111">EXAMPLES</span></span>

### <span data-ttu-id="b59a1-112">Beispiel 1: Starten einer Wartung im Abonnementbereich</span><span class="sxs-lookup"><span data-stu-id="b59a1-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="b59a1-113">Mit diesem Befehl wird eine neue Richtlinienbehebung im Abonnement "Mein Abonnement" für die angegebene Richtlinienzuweisung erstellt.</span><span class="sxs-lookup"><span data-stu-id="b59a1-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="b59a1-114">Beispiel 2: Starten einer Wartung im Bereich der Verwaltungsgruppe mit optionalen Filtern</span><span class="sxs-lookup"><span data-stu-id="b59a1-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="b59a1-115">Mit diesem Befehl wird eine neue Richtlinienbehebung in der Verwaltungsgruppe "mg1" für die angegebene Richtlinienzuweisung erstellt.</span><span class="sxs-lookup"><span data-stu-id="b59a1-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="b59a1-116">Nur Ressourcen an den Standorten "westus" oder "eastus" werden behoben.</span><span class="sxs-lookup"><span data-stu-id="b59a1-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="b59a1-117">Beispiel 3: Starten einer Wartung im Bereich "Ressourcengruppe" für eine Richtliniensatzdefinitionszuordnung</span><span class="sxs-lookup"><span data-stu-id="b59a1-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="b59a1-118">Mit diesem Befehl wird eine neue Richtlinienbehebung in der Ressourcengruppe "myRG" für die angegebene Richtlinienzuordnung erstellt.</span><span class="sxs-lookup"><span data-stu-id="b59a1-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="b59a1-119">Durch die Richtlinienzuweisung wird eine Definition für einen Richtliniensatz (auch als Initiative bekannt) zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="b59a1-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="b59a1-120">Die Referenz-ID der Richtliniendefinition gibt an, welche Richtlinie innerhalb der Initiative behoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b59a1-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="b59a1-121">Beispiel 4: Starten einer Wartung und Warten, bis sie im Hintergrund abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="b59a1-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="b59a1-122">Mit diesem Befehl wird eine neue Richtlinienbehebung im Abonnement "Mein Abonnement" für die angegebene Richtlinienzuweisung gestartet.</span><span class="sxs-lookup"><span data-stu-id="b59a1-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="b59a1-123">Es wartet, bis die Wartung abgeschlossen ist, bevor der endgültige Wartungsstatus angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b59a1-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

### <span data-ttu-id="b59a1-124">Beispiel 5: Starten einer Problembehebung, mit der nicht kompatible Ressourcen vor der Problembehebung ermittelt werden</span><span class="sxs-lookup"><span data-stu-id="b59a1-124">Example 5: Start a remediation that will discover non-compliant resources before remediating</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -ResourceDiscoveryMode ReEvaluateCompliance
```

<span data-ttu-id="b59a1-125">Mit diesem Befehl wird eine neue Richtlinienbehebung im Abonnement "Mein Abonnement" für die angegebene Richtlinienzuweisung erstellt.</span><span class="sxs-lookup"><span data-stu-id="b59a1-125">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="b59a1-126">Der Compliancestatus von Ressourcen im Abonnement wird anhand der Richtlinienzuweisung erneut ausgewertet, und nicht kompatible Ressourcen werden behoben.</span><span class="sxs-lookup"><span data-stu-id="b59a1-126">The compliance state of resources in the subscription will be re-evaluated against the policy assignment and non-compliant resources will be remediated.</span></span>

## <span data-ttu-id="b59a1-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b59a1-127">PARAMETERS</span></span>

### <span data-ttu-id="b59a1-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b59a1-128">-AsJob</span></span>
<span data-ttu-id="b59a1-129">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="b59a1-129">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="b59a1-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b59a1-130">-DefaultProfile</span></span>
<span data-ttu-id="b59a1-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b59a1-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b59a1-132">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="b59a1-132">-LocationFilter</span></span>
<span data-ttu-id="b59a1-133">Die Ressourcenpositionen, die in die Wartung eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b59a1-133">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="b59a1-134">Ressourcen, die sich nicht an diesen Speicherorten befinden, werden nicht behoben.</span><span class="sxs-lookup"><span data-stu-id="b59a1-134">Resources that don't reside in these locations will not be remediated.</span></span>

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

### <span data-ttu-id="b59a1-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="b59a1-135">-ManagementGroupName</span></span>
<span data-ttu-id="b59a1-136">ID der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b59a1-136">Management group ID.</span></span>

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

### <span data-ttu-id="b59a1-137">-Name</span><span class="sxs-lookup"><span data-stu-id="b59a1-137">-Name</span></span>
<span data-ttu-id="b59a1-138">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="b59a1-138">Resource name.</span></span>

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

### <span data-ttu-id="b59a1-139">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="b59a1-139">-PolicyAssignmentId</span></span>
<span data-ttu-id="b59a1-140">Richtlinienzuweisungs-ID.</span><span class="sxs-lookup"><span data-stu-id="b59a1-140">Policy assignment ID.</span></span>
<span data-ttu-id="b59a1-141">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="b59a1-141">E.g.</span></span>
<span data-ttu-id="b59a1-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="b59a1-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="b59a1-143">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="b59a1-143">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="b59a1-144">Ruft die Verweis-ID der Richtliniendefinition der einzelnen Definition ab, die behoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b59a1-144">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="b59a1-145">Erforderlich, wenn die Richtlinienzuweisung eine Richtliniensatzdefinition zu weist.</span><span class="sxs-lookup"><span data-stu-id="b59a1-145">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="b59a1-146">-ResourceDiscoveryMode</span><span class="sxs-lookup"><span data-stu-id="b59a1-146">-ResourceDiscoveryMode</span></span>
<span data-ttu-id="b59a1-147">Beschreibt, wie der Wartungsaufgabe Ressourcen findet, die behoben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b59a1-147">Describes how the remediation task will discover resources that need to be remediated.</span></span>
<span data-ttu-id="b59a1-148">"ReEvaluateCompliance" wird beim Remediating von Managementgruppenumfang nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b59a1-148">ReEvaluateCompliance is not supported when remediating management group scopes.</span></span>

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

### <span data-ttu-id="b59a1-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b59a1-149">-ResourceGroupName</span></span>
<span data-ttu-id="b59a1-150">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="b59a1-150">Resource group name.</span></span>

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

### <span data-ttu-id="b59a1-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b59a1-151">-ResourceId</span></span>
<span data-ttu-id="b59a1-152">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b59a1-152">Resource ID.</span></span>

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

### <span data-ttu-id="b59a1-153">-Scope</span><span class="sxs-lookup"><span data-stu-id="b59a1-153">-Scope</span></span>
<span data-ttu-id="b59a1-154">Umfang der Ressource.</span><span class="sxs-lookup"><span data-stu-id="b59a1-154">Scope of the resource.</span></span>
<span data-ttu-id="b59a1-155">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="b59a1-155">E.g.</span></span>
<span data-ttu-id="b59a1-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="b59a1-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="b59a1-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b59a1-157">-Confirm</span></span>
<span data-ttu-id="b59a1-158">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b59a1-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b59a1-159">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b59a1-159">-WhatIf</span></span>
<span data-ttu-id="b59a1-160">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b59a1-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b59a1-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b59a1-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b59a1-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b59a1-162">CommonParameters</span></span>
<span data-ttu-id="b59a1-163">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b59a1-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b59a1-164">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b59a1-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b59a1-165">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b59a1-165">INPUTS</span></span>

### <span data-ttu-id="b59a1-166">System.String</span><span class="sxs-lookup"><span data-stu-id="b59a1-166">System.String</span></span>

### <span data-ttu-id="b59a1-167">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b59a1-167">System.String[]</span></span>

## <span data-ttu-id="b59a1-168">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b59a1-168">OUTPUTS</span></span>

### <span data-ttu-id="b59a1-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="b59a1-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="b59a1-170">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b59a1-170">NOTES</span></span>

## <span data-ttu-id="b59a1-171">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b59a1-171">RELATED LINKS</span></span>
