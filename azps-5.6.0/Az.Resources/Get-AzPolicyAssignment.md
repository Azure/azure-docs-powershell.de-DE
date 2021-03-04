---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: 010f8be0a96499415ac78c584ebad1c10acf4523
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920456"
---
# <span data-ttu-id="98e10-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="98e10-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="98e10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98e10-102">SYNOPSIS</span></span>
<span data-ttu-id="98e10-103">Ruft Richtlinienzuordnungen ab.</span><span class="sxs-lookup"><span data-stu-id="98e10-103">Gets policy assignments.</span></span>

## <span data-ttu-id="98e10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98e10-104">SYNTAX</span></span>

### <span data-ttu-id="98e10-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="98e10-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98e10-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="98e10-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98e10-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="98e10-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98e10-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98e10-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98e10-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98e10-109">DESCRIPTION</span></span>
<span data-ttu-id="98e10-110">Das **Cmdlet Get-AzPolicyAssignment** ruft alle Richtlinienzuordnungen oder bestimmten Zuordnungen ab.</span><span class="sxs-lookup"><span data-stu-id="98e10-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="98e10-111">Identifizieren Sie eine Richtlinienzuordnung, die nach Name und Umfang oder nach ID ermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="98e10-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="98e10-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="98e10-112">EXAMPLES</span></span>

### <span data-ttu-id="98e10-113">Beispiel 1: Alle Richtlinienzuordnungen erhalten</span><span class="sxs-lookup"><span data-stu-id="98e10-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="98e10-114">Dieser Befehl ruft alle Richtlinienzuweisungen ab.</span><span class="sxs-lookup"><span data-stu-id="98e10-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="98e10-115">Beispiel 2: Erhalten einer bestimmten Richtlinienzuordnung</span><span class="sxs-lookup"><span data-stu-id="98e10-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="98e10-116">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 ab, indem er das cmdlet Get-AzResourceGroup verwendet und in der $ResourceGroup speichert.</span><span class="sxs-lookup"><span data-stu-id="98e10-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="98e10-117">Der zweite Befehl ruft die Richtlinienzuordnung mit dem Namen "PolicyAssignment07" für den Bereich ab, den die **ResourceId-Eigenschaft** $ResourceGroup identifiziert.</span><span class="sxs-lookup"><span data-stu-id="98e10-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="98e10-118">Beispiel 3: Erhalten aller Richtlinienzuweisungen, die einer Verwaltungsgruppe zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="98e10-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="98e10-119">Der erste Befehl gibt die ID der zu abfragenden Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="98e10-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="98e10-120">Der zweite Befehl ruft alle Richtlinienzuordnungen ab, die der Verwaltungsgruppe mit der ID "myManagementGroup" zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="98e10-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="98e10-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="98e10-121">PARAMETERS</span></span>

### <span data-ttu-id="98e10-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="98e10-122">-ApiVersion</span></span>
<span data-ttu-id="98e10-123">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="98e10-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="98e10-124">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="98e10-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="98e10-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98e10-125">-DefaultProfile</span></span>
<span data-ttu-id="98e10-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="98e10-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98e10-127">-ID</span><span class="sxs-lookup"><span data-stu-id="98e10-127">-Id</span></span>
<span data-ttu-id="98e10-128">Gibt die vollqualifizierte Ressourcen-ID für die Richtlinienzuordnung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="98e10-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="98e10-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="98e10-129">-IncludeDescendent</span></span>
<span data-ttu-id="98e10-130">Bewirkt, dass in der Liste der zurückgegebenen Richtlinienzuordnungen alle Zuordnungen im Zusammenhang mit dem angegebenen Bereich enthalten sind, einschließlich der Zuordnungen aus Ahnenbereichs und denen aus absteigenden Bereich.</span><span class="sxs-lookup"><span data-stu-id="98e10-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="98e10-131">-Name</span><span class="sxs-lookup"><span data-stu-id="98e10-131">-Name</span></span>
<span data-ttu-id="98e10-132">Gibt den Namen der Richtlinienzuordnung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="98e10-132">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="98e10-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="98e10-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="98e10-134">Gibt die ID der Richtliniendefinition der Richtlinienzuordnungen an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="98e10-134">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="98e10-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="98e10-135">-Pre</span></span>
<span data-ttu-id="98e10-136">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="98e10-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="98e10-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="98e10-137">-Scope</span></span>
<span data-ttu-id="98e10-138">Gibt den Bereich an, in dem die Richtlinie für die Zuordnung angewendet wird, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="98e10-138">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="98e10-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98e10-139">CommonParameters</span></span>
<span data-ttu-id="98e10-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98e10-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98e10-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98e10-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98e10-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="98e10-142">INPUTS</span></span>

### <span data-ttu-id="98e10-143">System.String</span><span class="sxs-lookup"><span data-stu-id="98e10-143">System.String</span></span>

### <span data-ttu-id="98e10-144">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="98e10-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="98e10-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="98e10-145">OUTPUTS</span></span>

### <span data-ttu-id="98e10-146">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="98e10-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="98e10-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="98e10-147">NOTES</span></span>

## <span data-ttu-id="98e10-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="98e10-148">RELATED LINKS</span></span>

[<span data-ttu-id="98e10-149">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="98e10-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="98e10-150">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="98e10-150">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="98e10-151">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="98e10-151">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


