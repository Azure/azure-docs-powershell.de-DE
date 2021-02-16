---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 00ec24c13a5c51db7da63cd1d94c01f251a7e289
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169081"
---
# <span data-ttu-id="5a8dd-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="5a8dd-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="5a8dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a8dd-102">SYNOPSIS</span></span>
<span data-ttu-id="5a8dd-103">Entfernt eine Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="5a8dd-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="5a8dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a8dd-104">SYNTAX</span></span>

### <span data-ttu-id="5a8dd-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a8dd-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a8dd-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a8dd-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a8dd-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a8dd-107">InputObjectParameterSet</span></span>
```
Remove-AzPolicyAssignment -InputObject <PsPolicyAssignment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a8dd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a8dd-108">DESCRIPTION</span></span>
<span data-ttu-id="5a8dd-109">Das **Cmdlet "Remove-AzPolicyAssignment"** entfernt die angegebene Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="5a8dd-109">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="5a8dd-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5a8dd-110">EXAMPLES</span></span>

### <span data-ttu-id="5a8dd-111">Beispiel 1: Entfernen der Richtlinienzuweisung nach Name und Bereich</span><span class="sxs-lookup"><span data-stu-id="5a8dd-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Confirm
```

<span data-ttu-id="5a8dd-112">Der erste Befehl ruft eine Ressourcengruppe namens "ResourceGroup11" mithilfe des cmdlets Get-AzResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="5a8dd-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="5a8dd-113">Der Befehl speichert dieses Objekt in der $ResourceGroup Variable.</span><span class="sxs-lookup"><span data-stu-id="5a8dd-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="5a8dd-114">Mit dem zweiten Befehl wird die Richtlinienzuordnung namens "PolicyAssignment07" entfernt, die auf Ressourcengruppenebene zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="5a8dd-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="5a8dd-115">Die **Eigenschaft "ResourceId"** des $ResourceGroup die Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="5a8dd-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="5a8dd-116">Beispiel 2: Entfernen der Richtlinienzuweisung nach ID</span><span class="sxs-lookup"><span data-stu-id="5a8dd-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Confirm
```

<span data-ttu-id="5a8dd-117">Der erste Befehl ruft eine Ressourcengruppe namens "ResourceGroup11" ab und speichert dieses Objekt dann in der $ResourceGroup Variable.</span><span class="sxs-lookup"><span data-stu-id="5a8dd-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="5a8dd-118">Der zweite Befehl ruft die Richtlinienzuordnung auf Ressourcengruppenebene ab und speichert sie dann in der $PolicyAssignment Variable.</span><span class="sxs-lookup"><span data-stu-id="5a8dd-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="5a8dd-119">Die **Eigenschaft "ResourceId"** des $ResourceGroup die Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="5a8dd-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="5a8dd-120">Der letzte Befehl entfernt die Richtlinienzuordnung, die von der **Eigenschaft "ResourceId"** des $PolicyAssignment wird.</span><span class="sxs-lookup"><span data-stu-id="5a8dd-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="5a8dd-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a8dd-121">PARAMETERS</span></span>

### <span data-ttu-id="5a8dd-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5a8dd-122">-ApiVersion</span></span>
<span data-ttu-id="5a8dd-123">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="5a8dd-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5a8dd-124">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="5a8dd-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5a8dd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a8dd-125">-DefaultProfile</span></span>
<span data-ttu-id="5a8dd-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5a8dd-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a8dd-127">-ID</span><span class="sxs-lookup"><span data-stu-id="5a8dd-127">-Id</span></span>
<span data-ttu-id="5a8dd-128">Gibt die vollqualifizierte Ressourcen-ID für die Richtlinienzuordnung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5a8dd-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5a8dd-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a8dd-129">-InputObject</span></span>
<span data-ttu-id="5a8dd-130">Das Richtlinienzuweisungsobjekt, das entfernt werden soll, das von einem anderen Cmdlet ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5a8dd-130">The policy assignment object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="5a8dd-131">-Name</span><span class="sxs-lookup"><span data-stu-id="5a8dd-131">-Name</span></span>
<span data-ttu-id="5a8dd-132">Gibt den Namen der Richtlinienzuweisung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5a8dd-132">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5a8dd-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="5a8dd-133">-Pre</span></span>
<span data-ttu-id="5a8dd-134">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a8dd-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5a8dd-135">-Scope</span><span class="sxs-lookup"><span data-stu-id="5a8dd-135">-Scope</span></span>
<span data-ttu-id="5a8dd-136">Gibt den Bereich an, auf den die Richtlinie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5a8dd-136">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="5a8dd-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a8dd-137">-Confirm</span></span>
<span data-ttu-id="5a8dd-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a8dd-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a8dd-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5a8dd-139">-WhatIf</span></span>
<span data-ttu-id="5a8dd-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a8dd-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a8dd-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a8dd-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a8dd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a8dd-142">CommonParameters</span></span>
<span data-ttu-id="5a8dd-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a8dd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a8dd-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a8dd-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a8dd-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5a8dd-145">INPUTS</span></span>

### <span data-ttu-id="5a8dd-146">System.String</span><span class="sxs-lookup"><span data-stu-id="5a8dd-146">System.String</span></span>

## <span data-ttu-id="5a8dd-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5a8dd-147">OUTPUTS</span></span>

### <span data-ttu-id="5a8dd-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5a8dd-148">System.Boolean</span></span>

## <span data-ttu-id="5a8dd-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5a8dd-149">NOTES</span></span>

## <span data-ttu-id="5a8dd-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5a8dd-150">RELATED LINKS</span></span>

[<span data-ttu-id="5a8dd-151">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="5a8dd-151">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="5a8dd-152">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="5a8dd-152">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="5a8dd-153">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="5a8dd-153">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


