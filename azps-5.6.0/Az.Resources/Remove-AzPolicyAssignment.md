---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 83c6cc2ba8103b95aed6d6d365c700e656ac16a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945766"
---
# <span data-ttu-id="c8de3-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c8de3-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="c8de3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8de3-102">SYNOPSIS</span></span>
<span data-ttu-id="c8de3-103">Entfernt eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="c8de3-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="c8de3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8de3-104">SYNTAX</span></span>

### <span data-ttu-id="c8de3-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c8de3-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8de3-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8de3-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8de3-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8de3-107">InputObjectParameterSet</span></span>
```
Remove-AzPolicyAssignment -InputObject <PsPolicyAssignment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8de3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8de3-108">DESCRIPTION</span></span>
<span data-ttu-id="c8de3-109">Das **Cmdlet Remove-AzPolicyAssignment** entfernt die angegebene Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="c8de3-109">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="c8de3-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c8de3-110">EXAMPLES</span></span>

### <span data-ttu-id="c8de3-111">Beispiel 1: Entfernen der Richtlinienzuordnung nach Name und Bereich</span><span class="sxs-lookup"><span data-stu-id="c8de3-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Confirm
```

<span data-ttu-id="c8de3-112">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 ab, indem er das cmdlet Get-AzResourceGroup verwendet.</span><span class="sxs-lookup"><span data-stu-id="c8de3-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="c8de3-113">Der Befehl speichert dieses Objekt in der $ResourceGroup-Variable.</span><span class="sxs-lookup"><span data-stu-id="c8de3-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c8de3-114">Mit dem zweiten Befehl wird die Richtlinienzuordnung mit dem Namen "PolicyAssignment07" entfernt, die auf Ressourcengruppenebene zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="c8de3-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="c8de3-115">Die **ResourceId-Eigenschaft** $ResourceGroup die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c8de3-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="c8de3-116">Beispiel 2: Entfernen der Richtlinienzuordnung nach ID</span><span class="sxs-lookup"><span data-stu-id="c8de3-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Confirm
```

<span data-ttu-id="c8de3-117">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="c8de3-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c8de3-118">Der zweite Befehl ruft die Richtlinienzuordnung auf Ressourcengruppenebene ab und speichert sie dann in $PolicyAssignment Variablen.</span><span class="sxs-lookup"><span data-stu-id="c8de3-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="c8de3-119">Die **ResourceId-Eigenschaft** $ResourceGroup die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c8de3-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="c8de3-120">Mit dem letzten Befehl wird die Richtlinienzuordnung entfernt, die von der **ResourceId-Eigenschaft** $PolicyAssignment wird.</span><span class="sxs-lookup"><span data-stu-id="c8de3-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="c8de3-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c8de3-121">PARAMETERS</span></span>

### <span data-ttu-id="c8de3-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c8de3-122">-ApiVersion</span></span>
<span data-ttu-id="c8de3-123">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="c8de3-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c8de3-124">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="c8de3-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c8de3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8de3-125">-DefaultProfile</span></span>
<span data-ttu-id="c8de3-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c8de3-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8de3-127">-ID</span><span class="sxs-lookup"><span data-stu-id="c8de3-127">-Id</span></span>
<span data-ttu-id="c8de3-128">Gibt die vollqualifizierte Ressourcen-ID für die Richtlinienzuordnung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c8de3-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c8de3-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8de3-129">-InputObject</span></span>
<span data-ttu-id="c8de3-130">Das Zu entfernende Richtlinienzuordnungsobjekt, das aus einem anderen Cmdlet ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c8de3-130">The policy assignment object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8de3-131">-Name</span><span class="sxs-lookup"><span data-stu-id="c8de3-131">-Name</span></span>
<span data-ttu-id="c8de3-132">Gibt den Namen der Richtlinienzuordnung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c8de3-132">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8de3-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="c8de3-133">-Pre</span></span>
<span data-ttu-id="c8de3-134">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8de3-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c8de3-135">-Scope</span><span class="sxs-lookup"><span data-stu-id="c8de3-135">-Scope</span></span>
<span data-ttu-id="c8de3-136">Gibt den Bereich an, in dem die Richtlinie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c8de3-136">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="c8de3-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c8de3-137">-Confirm</span></span>
<span data-ttu-id="c8de3-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8de3-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8de3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8de3-139">-WhatIf</span></span>
<span data-ttu-id="c8de3-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8de3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8de3-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8de3-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8de3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8de3-142">CommonParameters</span></span>
<span data-ttu-id="c8de3-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8de3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8de3-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8de3-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8de3-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c8de3-145">INPUTS</span></span>

### <span data-ttu-id="c8de3-146">System.String</span><span class="sxs-lookup"><span data-stu-id="c8de3-146">System.String</span></span>

## <span data-ttu-id="c8de3-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c8de3-147">OUTPUTS</span></span>

### <span data-ttu-id="c8de3-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c8de3-148">System.Boolean</span></span>

## <span data-ttu-id="c8de3-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c8de3-149">NOTES</span></span>

## <span data-ttu-id="c8de3-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c8de3-150">RELATED LINKS</span></span>

[<span data-ttu-id="c8de3-151">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c8de3-151">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="c8de3-152">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c8de3-152">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="c8de3-153">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c8de3-153">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


