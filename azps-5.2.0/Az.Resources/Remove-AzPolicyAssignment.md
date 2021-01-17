---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 00ec24c13a5c51db7da63cd1d94c01f251a7e289
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98308139"
---
# <span data-ttu-id="c5717-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c5717-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="c5717-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5717-102">SYNOPSIS</span></span>
<span data-ttu-id="c5717-103">Entfernt eine Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="c5717-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="c5717-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5717-104">SYNTAX</span></span>

### <span data-ttu-id="c5717-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c5717-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5717-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5717-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5717-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5717-107">InputObjectParameterSet</span></span>
```
Remove-AzPolicyAssignment -InputObject <PsPolicyAssignment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5717-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5717-108">DESCRIPTION</span></span>
<span data-ttu-id="c5717-109">Das **Cmdlet "Remove-AzPolicyAssignment"** entfernt die angegebene Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="c5717-109">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="c5717-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c5717-110">EXAMPLES</span></span>

### <span data-ttu-id="c5717-111">Beispiel 1: Entfernen der Richtlinienzuweisung nach Name und Bereich</span><span class="sxs-lookup"><span data-stu-id="c5717-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Confirm
```

<span data-ttu-id="c5717-112">Der erste Befehl ruft eine Ressourcengruppe namens "ResourceGroup11" mithilfe des cmdlets Get-AzResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="c5717-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="c5717-113">Der Befehl speichert dieses Objekt in der $ResourceGroup Variable.</span><span class="sxs-lookup"><span data-stu-id="c5717-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c5717-114">Mit dem zweiten Befehl wird die Richtlinienzuordnung namens "PolicyAssignment07" entfernt, die auf Ressourcengruppenebene zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="c5717-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="c5717-115">Die **Eigenschaft "ResourceId"** von $ResourceGroup die Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c5717-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="c5717-116">Beispiel 2: Entfernen der Richtlinienzuweisung nach ID</span><span class="sxs-lookup"><span data-stu-id="c5717-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Confirm
```

<span data-ttu-id="c5717-117">Der erste Befehl ruft eine Ressourcengruppe namens "ResourceGroup11" ab und speichert dieses Objekt dann in der $ResourceGroup Variable.</span><span class="sxs-lookup"><span data-stu-id="c5717-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c5717-118">Der zweite Befehl ruft die Richtlinienzuordnung auf Ressourcengruppenebene ab und speichert sie dann in der $PolicyAssignment Variable.</span><span class="sxs-lookup"><span data-stu-id="c5717-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="c5717-119">Die **Eigenschaft "ResourceId"** von $ResourceGroup die Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c5717-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="c5717-120">Der letzte Befehl entfernt die Richtlinienzuordnung, die von der **Eigenschaft "ResourceId"** des $PolicyAssignment wird.</span><span class="sxs-lookup"><span data-stu-id="c5717-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="c5717-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5717-121">PARAMETERS</span></span>

### <span data-ttu-id="c5717-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c5717-122">-ApiVersion</span></span>
<span data-ttu-id="c5717-123">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="c5717-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c5717-124">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="c5717-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c5717-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5717-125">-DefaultProfile</span></span>
<span data-ttu-id="c5717-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c5717-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5717-127">-ID</span><span class="sxs-lookup"><span data-stu-id="c5717-127">-Id</span></span>
<span data-ttu-id="c5717-128">Gibt die vollqualifizierte Ressourcen-ID für die Richtlinienzuordnung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c5717-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c5717-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5717-129">-InputObject</span></span>
<span data-ttu-id="c5717-130">Das Richtlinienzuweisungsobjekt, das entfernt werden soll, das von einem anderen Cmdlet ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c5717-130">The policy assignment object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="c5717-131">-Name</span><span class="sxs-lookup"><span data-stu-id="c5717-131">-Name</span></span>
<span data-ttu-id="c5717-132">Gibt den Namen der Richtlinienzuweisung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c5717-132">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c5717-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="c5717-133">-Pre</span></span>
<span data-ttu-id="c5717-134">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c5717-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c5717-135">-Scope</span><span class="sxs-lookup"><span data-stu-id="c5717-135">-Scope</span></span>
<span data-ttu-id="c5717-136">Gibt den Bereich an, auf den die Richtlinie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c5717-136">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="c5717-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5717-137">-Confirm</span></span>
<span data-ttu-id="c5717-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c5717-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5717-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c5717-139">-WhatIf</span></span>
<span data-ttu-id="c5717-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c5717-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5717-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c5717-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5717-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5717-142">CommonParameters</span></span>
<span data-ttu-id="c5717-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5717-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5717-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5717-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5717-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c5717-145">INPUTS</span></span>

### <span data-ttu-id="c5717-146">System.String</span><span class="sxs-lookup"><span data-stu-id="c5717-146">System.String</span></span>

## <span data-ttu-id="c5717-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c5717-147">OUTPUTS</span></span>

### <span data-ttu-id="c5717-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c5717-148">System.Boolean</span></span>

## <span data-ttu-id="c5717-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c5717-149">NOTES</span></span>

## <span data-ttu-id="c5717-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c5717-150">RELATED LINKS</span></span>

[<span data-ttu-id="c5717-151">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c5717-151">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="c5717-152">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c5717-152">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="c5717-153">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c5717-153">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


