---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: e4a0e3ad4ffac7e610f5807c7687cdc1bf548770
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177073"
---
# <span data-ttu-id="500ea-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="500ea-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="500ea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="500ea-102">SYNOPSIS</span></span>
<span data-ttu-id="500ea-103">Erstellt und startet eine Richtlinien Bereinigung für eine Richtlinien Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="500ea-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="500ea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="500ea-104">SYNTAX</span></span>

### <span data-ttu-id="500ea-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="500ea-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="500ea-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="500ea-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="500ea-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="500ea-107">DESCRIPTION</span></span>
<span data-ttu-id="500ea-108">Das Cmdlet **Start-AzPolicyRemediation** erstellt eine Richtlinien Bereinigung für eine bestimmte Richtlinien Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="500ea-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="500ea-109">Alle nicht kompatiblen Ressourcen, die sich am oder unterhalb des Bereichs der Behebung befinden, werden wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="500ea-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="500ea-110">Die Behebung wird nur für Richtlinien mit dem "deployIfNotExists"-Effekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="500ea-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="500ea-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="500ea-111">EXAMPLES</span></span>

### <span data-ttu-id="500ea-112">Beispiel 1: Starten einer Behebung im Abonnement Bereich</span><span class="sxs-lookup"><span data-stu-id="500ea-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="500ea-113">Mit diesem Befehl wird im Abonnement "mein Abonnement" eine neue Richtlinien Korrektur für die angegebene Richtlinien Aufgabe erstellt.</span><span class="sxs-lookup"><span data-stu-id="500ea-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="500ea-114">Beispiel 2: Starten einer Behebung im Verwaltungsgruppen Bereich mit optionalen Filtern</span><span class="sxs-lookup"><span data-stu-id="500ea-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="500ea-115">Mit diesem Befehl wird in der Verwaltungsgruppe "mg1" für die angegebene Richtlinienzuweisung eine neue Richtlinien Bereinigung erstellt.</span><span class="sxs-lookup"><span data-stu-id="500ea-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="500ea-116">Es werden nur Ressourcen in den Speicherorten "westus" oder "eastus" behoben.</span><span class="sxs-lookup"><span data-stu-id="500ea-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="500ea-117">Beispiel 3: Starten einer Behebung im Ressourcengruppen Bereich für eine Richtliniensatz-Definitions Aufgabe</span><span class="sxs-lookup"><span data-stu-id="500ea-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="500ea-118">Mit diesem Befehl wird in der Ressourcengruppe "myRG" für die angegebene Richtlinienzuweisung eine neue Richtlinien Bereinigung erstellt.</span><span class="sxs-lookup"><span data-stu-id="500ea-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="500ea-119">Die Richtlinienzuweisung weist eine Richtliniensatz Definition (auch als Initiative bezeichnet) zu.</span><span class="sxs-lookup"><span data-stu-id="500ea-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="500ea-120">Die Richtlinien Definitions Referenz-ID gibt an, welche Richtlinie innerhalb der Initiative wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="500ea-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="500ea-121">Beispiel 4: Starten einer Bereinigung und warten, bis Sie im Hintergrund ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="500ea-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="500ea-122">Mit diesem Befehl wird eine neue Richtlinien Bereinigung im Abonnement "mein Abonnement" für die angegebene Richtlinien Aufgabe gestartet.</span><span class="sxs-lookup"><span data-stu-id="500ea-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="500ea-123">Sie wartet auf die Fertigstellung der Wiederherstellung, bevor der endgültige Behebungs Status zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="500ea-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

### <span data-ttu-id="500ea-124">Beispiel 5: Starten einer Behebung, die nicht richtlinienkonforme Ressourcen erkennt, bevor eine Wiederherstellung erfolgt</span><span class="sxs-lookup"><span data-stu-id="500ea-124">Example 5: Start a remediation that will discover non-compliant resources before remediating</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -ResourceDiscoveryMode ReEvaluateCompliance
```

<span data-ttu-id="500ea-125">Mit diesem Befehl wird im Abonnement "mein Abonnement" eine neue Richtlinien Korrektur für die angegebene Richtlinien Aufgabe erstellt.</span><span class="sxs-lookup"><span data-stu-id="500ea-125">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="500ea-126">Der Kompatibilitätsstatus von Ressourcen im Abonnement wird anhand der Richtlinienzuweisung erneut ausgewertet, und die nicht kompatiblen Ressourcen werden wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="500ea-126">The compliance state of resources in the subscription will be re-evaluated against the policy assignment and non-compliant resources will be remediated.</span></span>

## <span data-ttu-id="500ea-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="500ea-127">PARAMETERS</span></span>

### <span data-ttu-id="500ea-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="500ea-128">-AsJob</span></span>
<span data-ttu-id="500ea-129">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="500ea-129">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="500ea-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="500ea-130">-DefaultProfile</span></span>
<span data-ttu-id="500ea-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="500ea-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="500ea-132">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="500ea-132">-LocationFilter</span></span>
<span data-ttu-id="500ea-133">Die Ressourcenspeicherorte, die in die Behebung einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="500ea-133">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="500ea-134">Ressourcen, die sich nicht an diesen Speicherorten befinden, werden nicht wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="500ea-134">Resources that don't reside in these locations will not be remediated.</span></span>

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

### <span data-ttu-id="500ea-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="500ea-135">-ManagementGroupName</span></span>
<span data-ttu-id="500ea-136">Verwaltungsgruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="500ea-136">Management group ID.</span></span>

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

### <span data-ttu-id="500ea-137">-Name</span><span class="sxs-lookup"><span data-stu-id="500ea-137">-Name</span></span>
<span data-ttu-id="500ea-138">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="500ea-138">Resource name.</span></span>

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

### <span data-ttu-id="500ea-139">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="500ea-139">-PolicyAssignmentId</span></span>
<span data-ttu-id="500ea-140">Richtlinien Zuordnungs-ID.</span><span class="sxs-lookup"><span data-stu-id="500ea-140">Policy assignment ID.</span></span>
<span data-ttu-id="500ea-141">Z.b..</span><span class="sxs-lookup"><span data-stu-id="500ea-141">E.g.</span></span>
<span data-ttu-id="500ea-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="500ea-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="500ea-143">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="500ea-143">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="500ea-144">Ruft die Richtlinien Definitions Verweis-ID der einzelnen Definition ab, die wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="500ea-144">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="500ea-145">Erforderlich, wenn die Richtlinienzuweisung eine Richtliniensatz Definition zuweist.</span><span class="sxs-lookup"><span data-stu-id="500ea-145">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="500ea-146">-ResourceDiscoveryMode</span><span class="sxs-lookup"><span data-stu-id="500ea-146">-ResourceDiscoveryMode</span></span>
<span data-ttu-id="500ea-147">Beschreibt, wie die Behebungs Aufgabe Ressourcen ermittelt, die wiederhergestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="500ea-147">Describes how the remediation task will discover resources that need to be remediated.</span></span>
<span data-ttu-id="500ea-148">ReEvaluateCompliance wird nicht unterstützt, wenn die Bereiche der Verwaltungsgruppe erneut vermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="500ea-148">ReEvaluateCompliance is not supported when remediating management group scopes.</span></span>

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

### <span data-ttu-id="500ea-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="500ea-149">-ResourceGroupName</span></span>
<span data-ttu-id="500ea-150">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="500ea-150">Resource group name.</span></span>

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

### <span data-ttu-id="500ea-151">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="500ea-151">-ResourceId</span></span>
<span data-ttu-id="500ea-152">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="500ea-152">Resource ID.</span></span>

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

### <span data-ttu-id="500ea-153">-Scope</span><span class="sxs-lookup"><span data-stu-id="500ea-153">-Scope</span></span>
<span data-ttu-id="500ea-154">Der Bereich der Ressource.</span><span class="sxs-lookup"><span data-stu-id="500ea-154">Scope of the resource.</span></span>
<span data-ttu-id="500ea-155">Z.b..</span><span class="sxs-lookup"><span data-stu-id="500ea-155">E.g.</span></span>
<span data-ttu-id="500ea-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="500ea-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="500ea-157">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="500ea-157">-Confirm</span></span>
<span data-ttu-id="500ea-158">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="500ea-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="500ea-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="500ea-159">-WhatIf</span></span>
<span data-ttu-id="500ea-160">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="500ea-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="500ea-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="500ea-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="500ea-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="500ea-162">CommonParameters</span></span>
<span data-ttu-id="500ea-163">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="500ea-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="500ea-164">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="500ea-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="500ea-165">Eingaben</span><span class="sxs-lookup"><span data-stu-id="500ea-165">INPUTS</span></span>

### <span data-ttu-id="500ea-166">System. String</span><span class="sxs-lookup"><span data-stu-id="500ea-166">System.String</span></span>

### <span data-ttu-id="500ea-167">System. String []</span><span class="sxs-lookup"><span data-stu-id="500ea-167">System.String[]</span></span>

## <span data-ttu-id="500ea-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="500ea-168">OUTPUTS</span></span>

### <span data-ttu-id="500ea-169">Microsoft. Azure. Commands. PolicyInsights. Models. Remediation. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="500ea-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="500ea-170">Notizen</span><span class="sxs-lookup"><span data-stu-id="500ea-170">NOTES</span></span>

## <span data-ttu-id="500ea-171">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="500ea-171">RELATED LINKS</span></span>
