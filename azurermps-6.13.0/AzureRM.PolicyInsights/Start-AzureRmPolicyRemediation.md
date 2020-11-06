---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/start-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Start-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Start-AzureRmPolicyRemediation.md
ms.openlocfilehash: d5a0d4cd14f86c782defd7b70a1edee209982d2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480205"
---
# <span data-ttu-id="d57c3-101">Start-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="d57c3-101">Start-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="d57c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d57c3-102">SYNOPSIS</span></span>
<span data-ttu-id="d57c3-103">Erstellt und startet eine Richtlinien Bereinigung für eine Richtlinien Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="d57c3-103">Creates and starts a policy remediation for a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d57c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d57c3-104">SYNTAX</span></span>

### <span data-ttu-id="d57c3-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d57c3-105">ByName (Default)</span></span>
```
Start-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d57c3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d57c3-106">ByResourceId</span></span>
```
Start-AzureRmPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d57c3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d57c3-107">DESCRIPTION</span></span>
<span data-ttu-id="d57c3-108">Das Cmdlet **Start-AzureRmPolicyRemediation** erstellt eine Richtlinien Bereinigung für eine bestimmte Richtlinien Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="d57c3-108">The **Start-AzureRmPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="d57c3-109">Alle nicht kompatiblen Ressourcen, die sich am oder unterhalb des Bereichs der Behebung befinden, werden wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="d57c3-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="d57c3-110">Die Behebung wird nur für Richtlinien mit dem "deployIfNotExists"-Effekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d57c3-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="d57c3-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d57c3-111">EXAMPLES</span></span>

### <span data-ttu-id="d57c3-112">Beispiel 1: Starten einer Behebung im Abonnement Bereich</span><span class="sxs-lookup"><span data-stu-id="d57c3-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzureRmSubscription -Subscription "My Subscription"
PS C:\> Start-AzureRmPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="d57c3-113">Mit diesem Befehl wird im Abonnement "mein Abonnement" eine neue Richtlinien Korrektur für die angegebene Richtlinien Aufgabe erstellt.</span><span class="sxs-lookup"><span data-stu-id="d57c3-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="d57c3-114">Beispiel 2: Starten einer Behebung im Verwaltungsgruppen Bereich mit optionalen Filtern</span><span class="sxs-lookup"><span data-stu-id="d57c3-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzureRmPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="d57c3-115">Mit diesem Befehl wird in der Verwaltungsgruppe "mg1" für die angegebene Richtlinienzuweisung eine neue Richtlinien Bereinigung erstellt.</span><span class="sxs-lookup"><span data-stu-id="d57c3-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="d57c3-116">Es werden nur Ressourcen in den Speicherorten "westus" oder "eastus" behoben.</span><span class="sxs-lookup"><span data-stu-id="d57c3-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="d57c3-117">Beispiel 3: Starten einer Behebung im Ressourcengruppen Bereich für eine Richtliniensatz-Definitions Aufgabe</span><span class="sxs-lookup"><span data-stu-id="d57c3-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzureRmPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="d57c3-118">Mit diesem Befehl wird in der Ressourcengruppe "myRG" für die angegebene Richtlinienzuweisung eine neue Richtlinien Bereinigung erstellt.</span><span class="sxs-lookup"><span data-stu-id="d57c3-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="d57c3-119">Die Richtlinienzuweisung weist eine Richtliniensatz Definition (auch als Initiative bezeichnet) zu.</span><span class="sxs-lookup"><span data-stu-id="d57c3-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="d57c3-120">Die Richtlinien Definitions Referenz-ID gibt an, welche Richtlinie innerhalb der Initiative wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d57c3-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="d57c3-121">Beispiel 4: Starten einer Bereinigung und warten, bis Sie im Hintergrund ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="d57c3-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzureRmSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzureRmPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="d57c3-122">Mit diesem Befehl wird eine neue Richtlinien Bereinigung im Abonnement "mein Abonnement" für die angegebene Richtlinien Aufgabe gestartet.</span><span class="sxs-lookup"><span data-stu-id="d57c3-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="d57c3-123">Sie wartet auf die Fertigstellung der Wiederherstellung, bevor der endgültige Behebungs Status zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d57c3-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

## <span data-ttu-id="d57c3-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="d57c3-124">PARAMETERS</span></span>

### <span data-ttu-id="d57c3-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d57c3-125">-AsJob</span></span>
<span data-ttu-id="d57c3-126">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="d57c3-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="d57c3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d57c3-127">-DefaultProfile</span></span>
<span data-ttu-id="d57c3-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d57c3-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d57c3-129">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="d57c3-129">-LocationFilter</span></span>
<span data-ttu-id="d57c3-130">Die Ressourcenspeicherorte, die in die Behebung einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d57c3-130">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="d57c3-131">Ressourcen, die sich nicht an diesen Speicherorten befinden, werden nicht wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="d57c3-131">Resources that don't reside in these locations will not be remediated.</span></span>

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

### <span data-ttu-id="d57c3-132">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d57c3-132">-ManagementGroupName</span></span>
<span data-ttu-id="d57c3-133">Verwaltungsgruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="d57c3-133">Management group ID.</span></span>

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

### <span data-ttu-id="d57c3-134">-Name</span><span class="sxs-lookup"><span data-stu-id="d57c3-134">-Name</span></span>
<span data-ttu-id="d57c3-135">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="d57c3-135">Resource name.</span></span>

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

### <span data-ttu-id="d57c3-136">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="d57c3-136">-PolicyAssignmentId</span></span>
<span data-ttu-id="d57c3-137">Richtlinien Zuordnungs-ID.</span><span class="sxs-lookup"><span data-stu-id="d57c3-137">Policy assignment ID.</span></span>
<span data-ttu-id="d57c3-138">Z.b..</span><span class="sxs-lookup"><span data-stu-id="d57c3-138">E.g.</span></span>
<span data-ttu-id="d57c3-139">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="d57c3-139">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="d57c3-140">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="d57c3-140">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="d57c3-141">Ruft die Richtlinien Definitions Verweis-ID der einzelnen Definition ab, die wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d57c3-141">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="d57c3-142">Erforderlich, wenn die Richtlinienzuweisung eine Richtliniensatz Definition zuweist.</span><span class="sxs-lookup"><span data-stu-id="d57c3-142">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="d57c3-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d57c3-143">-ResourceGroupName</span></span>
<span data-ttu-id="d57c3-144">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d57c3-144">Resource group name.</span></span>

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

### <span data-ttu-id="d57c3-145">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d57c3-145">-ResourceId</span></span>
<span data-ttu-id="d57c3-146">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="d57c3-146">Resource ID.</span></span>

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

### <span data-ttu-id="d57c3-147">-Scope</span><span class="sxs-lookup"><span data-stu-id="d57c3-147">-Scope</span></span>
<span data-ttu-id="d57c3-148">Der Bereich der Ressource.</span><span class="sxs-lookup"><span data-stu-id="d57c3-148">Scope of the resource.</span></span>
<span data-ttu-id="d57c3-149">Z.b..</span><span class="sxs-lookup"><span data-stu-id="d57c3-149">E.g.</span></span>
<span data-ttu-id="d57c3-150">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="d57c3-150">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="d57c3-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d57c3-151">-Confirm</span></span>
<span data-ttu-id="d57c3-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d57c3-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d57c3-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d57c3-153">-WhatIf</span></span>
<span data-ttu-id="d57c3-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d57c3-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d57c3-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d57c3-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d57c3-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d57c3-156">CommonParameters</span></span>
<span data-ttu-id="d57c3-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d57c3-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d57c3-158">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d57c3-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d57c3-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d57c3-159">INPUTS</span></span>

### <span data-ttu-id="d57c3-160">System. String</span><span class="sxs-lookup"><span data-stu-id="d57c3-160">System.String</span></span>

### <span data-ttu-id="d57c3-161">System. String []</span><span class="sxs-lookup"><span data-stu-id="d57c3-161">System.String[]</span></span>

## <span data-ttu-id="d57c3-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d57c3-162">OUTPUTS</span></span>

### <span data-ttu-id="d57c3-163">Microsoft. Azure. Commands. PolicyInsights. Models. Remediation. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="d57c3-163">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="d57c3-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="d57c3-164">NOTES</span></span>

## <span data-ttu-id="d57c3-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d57c3-165">RELATED LINKS</span></span>
