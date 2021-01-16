---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: 4d5b230b741deec10daa44dab7e4faa44ac96b61
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459447"
---
# <span data-ttu-id="6edf9-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6edf9-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="6edf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6edf9-102">SYNOPSIS</span></span>
<span data-ttu-id="6edf9-103">Ruft Richtlinienzuweisungen ab.</span><span class="sxs-lookup"><span data-stu-id="6edf9-103">Gets policy assignments.</span></span>

## <span data-ttu-id="6edf9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6edf9-104">SYNTAX</span></span>

### <span data-ttu-id="6edf9-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6edf9-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6edf9-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6edf9-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6edf9-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="6edf9-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6edf9-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6edf9-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6edf9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6edf9-109">DESCRIPTION</span></span>
<span data-ttu-id="6edf9-110">Das **Cmdlet "Get-AzPolicyAssignment"** ruft alle Richtlinienzuweisungen oder bestimmte Aufgaben ab.</span><span class="sxs-lookup"><span data-stu-id="6edf9-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="6edf9-111">Identifizieren Sie eine Richtlinienzuweisung, die nach Name und Bereich oder id ermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6edf9-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="6edf9-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6edf9-112">EXAMPLES</span></span>

### <span data-ttu-id="6edf9-113">Beispiel 1: Alle Richtlinienzuweisungen erhalten</span><span class="sxs-lookup"><span data-stu-id="6edf9-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="6edf9-114">Dieser Befehl ruft alle Richtlinienzuweisungen ab.</span><span class="sxs-lookup"><span data-stu-id="6edf9-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="6edf9-115">Beispiel 2: Erhalten einer bestimmten Richtlinienzuweisung</span><span class="sxs-lookup"><span data-stu-id="6edf9-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="6edf9-116">Der erste Befehl ruft eine Ressourcengruppe namens "ResourceGroup11" mithilfe des cmdlets Get-AzResourceGroup ab und speichert sie in der $ResourceGroup Variable.</span><span class="sxs-lookup"><span data-stu-id="6edf9-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="6edf9-117">Der zweite Befehl ruft die Richtlinienzuordnung mit dem Namen "PolicyAssignment07" für den Bereich ab, den die **Eigenschaft "ResourceId"** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6edf9-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="6edf9-118">Beispiel 3: Alle Richtlinienzuweisungen einer Verwaltungsgruppe zugewiesen bekommen</span><span class="sxs-lookup"><span data-stu-id="6edf9-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="6edf9-119">Der erste Befehl gibt die ID der zu abfragenden Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="6edf9-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="6edf9-120">Der zweite Befehl ruft alle Richtlinienzuweisungen ab, die der Verwaltungsgruppe mit der ID "myManagementGroup" zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="6edf9-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="6edf9-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6edf9-121">PARAMETERS</span></span>

### <span data-ttu-id="6edf9-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6edf9-122">-ApiVersion</span></span>
<span data-ttu-id="6edf9-123">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="6edf9-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6edf9-124">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="6edf9-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6edf9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6edf9-125">-DefaultProfile</span></span>
<span data-ttu-id="6edf9-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6edf9-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6edf9-127">-ID</span><span class="sxs-lookup"><span data-stu-id="6edf9-127">-Id</span></span>
<span data-ttu-id="6edf9-128">Gibt die vollqualifizierte Ressourcen-ID für die Richtlinienzuordnung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="6edf9-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6edf9-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="6edf9-129">-IncludeDescendent</span></span>
<span data-ttu-id="6edf9-130">Bewirkt, dass die Liste der zurückgegebenen Richtlinienzuweisungen alle Zuordnungen enthält, die mit dem angegebenen Bereich verbunden sind, einschließlich der Zuordnungen aus vorgängern Und denen aus absteigenden Bereich.</span><span class="sxs-lookup"><span data-stu-id="6edf9-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IncludeDescendentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6edf9-131">-Name</span><span class="sxs-lookup"><span data-stu-id="6edf9-131">-Name</span></span>
<span data-ttu-id="6edf9-132">Gibt den Namen der Richtlinienzuweisung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="6edf9-132">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6edf9-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="6edf9-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="6edf9-134">Gibt die ID der Richtliniendefinition der Richtlinienzuweisungen an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="6edf9-134">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6edf9-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="6edf9-135">-Pre</span></span>
<span data-ttu-id="6edf9-136">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6edf9-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6edf9-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="6edf9-137">-Scope</span></span>
<span data-ttu-id="6edf9-138">Gibt den Bereich an, in dem die Richtlinie auf die Zuordnung angewendet wird, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="6edf9-138">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IncludeDescendentParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6edf9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6edf9-139">CommonParameters</span></span>
<span data-ttu-id="6edf9-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6edf9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6edf9-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6edf9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6edf9-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6edf9-142">INPUTS</span></span>

### <span data-ttu-id="6edf9-143">System.String</span><span class="sxs-lookup"><span data-stu-id="6edf9-143">System.String</span></span>

### <span data-ttu-id="6edf9-144">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6edf9-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6edf9-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6edf9-145">OUTPUTS</span></span>

### <span data-ttu-id="6edf9-146">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="6edf9-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6edf9-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6edf9-147">NOTES</span></span>

## <span data-ttu-id="6edf9-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6edf9-148">RELATED LINKS</span></span>

[<span data-ttu-id="6edf9-149">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6edf9-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="6edf9-150">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6edf9-150">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="6edf9-151">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6edf9-151">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


