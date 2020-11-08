---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: e4a0e3ad4ffac7e610f5807c7687cdc1bf548770
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174917"
---
# <span data-ttu-id="1f5ae-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="1f5ae-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="1f5ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1f5ae-102">SYNOPSIS</span></span>
<span data-ttu-id="1f5ae-103">Erstellt und startet eine Richtlinien Bereinigung für eine Richtlinien Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="1f5ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f5ae-104">SYNTAX</span></span>

### <span data-ttu-id="1f5ae-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1f5ae-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f5ae-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1f5ae-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f5ae-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f5ae-107">DESCRIPTION</span></span>
<span data-ttu-id="1f5ae-108">Das Cmdlet **Start-AzPolicyRemediation** erstellt eine Richtlinien Bereinigung für eine bestimmte Richtlinien Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="1f5ae-109">Alle nicht kompatiblen Ressourcen, die sich am oder unterhalb des Bereichs der Behebung befinden, werden wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="1f5ae-110">Die Behebung wird nur für Richtlinien mit dem "deployIfNotExists"-Effekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="1f5ae-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f5ae-111">EXAMPLES</span></span>

### <span data-ttu-id="1f5ae-112">Beispiel 1: Starten einer Behebung im Abonnement Bereich</span><span class="sxs-lookup"><span data-stu-id="1f5ae-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="1f5ae-113">Mit diesem Befehl wird im Abonnement "mein Abonnement" eine neue Richtlinien Korrektur für die angegebene Richtlinien Aufgabe erstellt.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="1f5ae-114">Beispiel 2: Starten einer Behebung im Verwaltungsgruppen Bereich mit optionalen Filtern</span><span class="sxs-lookup"><span data-stu-id="1f5ae-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="1f5ae-115">Mit diesem Befehl wird in der Verwaltungsgruppe "mg1" für die angegebene Richtlinienzuweisung eine neue Richtlinien Bereinigung erstellt.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="1f5ae-116">Es werden nur Ressourcen in den Speicherorten "westus" oder "eastus" behoben.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="1f5ae-117">Beispiel 3: Starten einer Behebung im Ressourcengruppen Bereich für eine Richtliniensatz-Definitions Aufgabe</span><span class="sxs-lookup"><span data-stu-id="1f5ae-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="1f5ae-118">Mit diesem Befehl wird in der Ressourcengruppe "myRG" für die angegebene Richtlinienzuweisung eine neue Richtlinien Bereinigung erstellt.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="1f5ae-119">Die Richtlinienzuweisung weist eine Richtliniensatz Definition (auch als Initiative bezeichnet) zu.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="1f5ae-120">Die Richtlinien Definitions Referenz-ID gibt an, welche Richtlinie innerhalb der Initiative wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="1f5ae-121">Beispiel 4: Starten einer Bereinigung und warten, bis Sie im Hintergrund ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="1f5ae-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="1f5ae-122">Mit diesem Befehl wird eine neue Richtlinien Bereinigung im Abonnement "mein Abonnement" für die angegebene Richtlinien Aufgabe gestartet.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="1f5ae-123">Sie wartet auf die Fertigstellung der Wiederherstellung, bevor der endgültige Behebungs Status zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

### <span data-ttu-id="1f5ae-124">Beispiel 5: Starten einer Behebung, die nicht richtlinienkonforme Ressourcen erkennt, bevor eine Wiederherstellung erfolgt</span><span class="sxs-lookup"><span data-stu-id="1f5ae-124">Example 5: Start a remediation that will discover non-compliant resources before remediating</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -ResourceDiscoveryMode ReEvaluateCompliance
```

<span data-ttu-id="1f5ae-125">Mit diesem Befehl wird im Abonnement "mein Abonnement" eine neue Richtlinien Korrektur für die angegebene Richtlinien Aufgabe erstellt.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-125">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="1f5ae-126">Der Kompatibilitätsstatus von Ressourcen im Abonnement wird anhand der Richtlinienzuweisung erneut ausgewertet, und die nicht kompatiblen Ressourcen werden wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-126">The compliance state of resources in the subscription will be re-evaluated against the policy assignment and non-compliant resources will be remediated.</span></span>

## <span data-ttu-id="1f5ae-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f5ae-127">PARAMETERS</span></span>

### <span data-ttu-id="1f5ae-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f5ae-128">-AsJob</span></span>
<span data-ttu-id="1f5ae-129">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-129">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="1f5ae-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f5ae-130">-DefaultProfile</span></span>
<span data-ttu-id="1f5ae-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f5ae-132">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="1f5ae-132">-LocationFilter</span></span>
<span data-ttu-id="1f5ae-133">Die Ressourcenspeicherorte, die in die Behebung einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-133">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="1f5ae-134">Ressourcen, die sich nicht an diesen Speicherorten befinden, werden nicht wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-134">Resources that don't reside in these locations will not be remediated.</span></span>

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

### <span data-ttu-id="1f5ae-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="1f5ae-135">-ManagementGroupName</span></span>
<span data-ttu-id="1f5ae-136">Verwaltungsgruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-136">Management group ID.</span></span>

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

### <span data-ttu-id="1f5ae-137">-Name</span><span class="sxs-lookup"><span data-stu-id="1f5ae-137">-Name</span></span>
<span data-ttu-id="1f5ae-138">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="1f5ae-138">Resource name.</span></span>

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

### <span data-ttu-id="1f5ae-139">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="1f5ae-139">-PolicyAssignmentId</span></span>
<span data-ttu-id="1f5ae-140">Richtlinien Zuordnungs-ID.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-140">Policy assignment ID.</span></span>
<span data-ttu-id="1f5ae-141">Z.b..</span><span class="sxs-lookup"><span data-stu-id="1f5ae-141">E.g.</span></span>
<span data-ttu-id="1f5ae-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="1f5ae-143">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="1f5ae-143">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="1f5ae-144">Ruft die Richtlinien Definitions Verweis-ID der einzelnen Definition ab, die wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-144">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="1f5ae-145">Erforderlich, wenn die Richtlinienzuweisung eine Richtliniensatz Definition zuweist.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-145">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="1f5ae-146">-ResourceDiscoveryMode</span><span class="sxs-lookup"><span data-stu-id="1f5ae-146">-ResourceDiscoveryMode</span></span>
<span data-ttu-id="1f5ae-147">Beschreibt, wie die Behebungs Aufgabe Ressourcen ermittelt, die wiederhergestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-147">Describes how the remediation task will discover resources that need to be remediated.</span></span>
<span data-ttu-id="1f5ae-148">ReEvaluateCompliance wird nicht unterstützt, wenn die Bereiche der Verwaltungsgruppe erneut vermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-148">ReEvaluateCompliance is not supported when remediating management group scopes.</span></span>

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

### <span data-ttu-id="1f5ae-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f5ae-149">-ResourceGroupName</span></span>
<span data-ttu-id="1f5ae-150">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-150">Resource group name.</span></span>

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

### <span data-ttu-id="1f5ae-151">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1f5ae-151">-ResourceId</span></span>
<span data-ttu-id="1f5ae-152">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-152">Resource ID.</span></span>

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

### <span data-ttu-id="1f5ae-153">-Scope</span><span class="sxs-lookup"><span data-stu-id="1f5ae-153">-Scope</span></span>
<span data-ttu-id="1f5ae-154">Der Bereich der Ressource.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-154">Scope of the resource.</span></span>
<span data-ttu-id="1f5ae-155">Z.b..</span><span class="sxs-lookup"><span data-stu-id="1f5ae-155">E.g.</span></span>
<span data-ttu-id="1f5ae-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="1f5ae-157">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1f5ae-157">-Confirm</span></span>
<span data-ttu-id="1f5ae-158">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f5ae-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f5ae-159">-WhatIf</span></span>
<span data-ttu-id="1f5ae-160">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f5ae-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f5ae-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f5ae-162">CommonParameters</span></span>
<span data-ttu-id="1f5ae-163">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f5ae-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f5ae-164">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f5ae-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f5ae-165">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1f5ae-165">INPUTS</span></span>

### <span data-ttu-id="1f5ae-166">System. String</span><span class="sxs-lookup"><span data-stu-id="1f5ae-166">System.String</span></span>

### <span data-ttu-id="1f5ae-167">System. String []</span><span class="sxs-lookup"><span data-stu-id="1f5ae-167">System.String[]</span></span>

## <span data-ttu-id="1f5ae-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1f5ae-168">OUTPUTS</span></span>

### <span data-ttu-id="1f5ae-169">Microsoft. Azure. Commands. PolicyInsights. Models. Remediation. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="1f5ae-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="1f5ae-170">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f5ae-170">NOTES</span></span>

## <span data-ttu-id="1f5ae-171">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1f5ae-171">RELATED LINKS</span></span>
