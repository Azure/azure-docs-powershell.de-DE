---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: d4ce9ef88f7043a369d8e566de75651944ea1e88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950064"
---
# <span data-ttu-id="35288-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="35288-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="35288-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35288-102">SYNOPSIS</span></span>
<span data-ttu-id="35288-103">Löscht eine benutzerdefinierte Rolle in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="35288-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="35288-104">Die zu löschende Rolle wird mithilfe der ID-Eigenschaft der Rolle angegeben.</span><span class="sxs-lookup"><span data-stu-id="35288-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="35288-105">Wenn der benutzerdefinierten Rolle bereits Rollenzuweisungen vorgenommen wurden, kann "Löschen" fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="35288-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="35288-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35288-106">SYNTAX</span></span>

### <span data-ttu-id="35288-107">RoleDefinitionIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="35288-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35288-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="35288-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35288-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35288-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35288-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="35288-110">DESCRIPTION</span></span>
<span data-ttu-id="35288-111">Das Remove-AzRoleDefinition-Cmdlet löscht eine benutzerdefinierte Rolle in Azure Role-Based Access Control.</span><span class="sxs-lookup"><span data-stu-id="35288-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="35288-112">Geben Sie den Parameter ID einer vorhandenen benutzerdefinierten Rolle an, um diese benutzerdefinierte Rolle zu löschen.</span><span class="sxs-lookup"><span data-stu-id="35288-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="35288-113">Standardmäßig werden Remove-AzRoleDefinition zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="35288-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="35288-114">Verwenden Sie zum Unterdrücken der Eingabeaufforderung den Parameter Erzwingen.</span><span class="sxs-lookup"><span data-stu-id="35288-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="35288-115">Wenn für die benutzerdefinierte Rolle Rollenzuweisungen vorhanden sind, die gelöscht werden sollen, kann der Löscheinsatz fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="35288-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="35288-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="35288-116">EXAMPLES</span></span>

### <span data-ttu-id="35288-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="35288-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="35288-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="35288-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="35288-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="35288-119">PARAMETERS</span></span>

### <span data-ttu-id="35288-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35288-120">-DefaultProfile</span></span>
<span data-ttu-id="35288-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="35288-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35288-122">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="35288-122">-Force</span></span>
<span data-ttu-id="35288-123">Wenn festgelegt, wird vor dem Löschen der benutzerdefinierten Rolle keine Bestätigung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="35288-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="35288-124">-ID</span><span class="sxs-lookup"><span data-stu-id="35288-124">-Id</span></span>
<span data-ttu-id="35288-125">ID der zu löschende Rollendefinition</span><span class="sxs-lookup"><span data-stu-id="35288-125">Id of the Role definition to be deleted</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35288-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35288-126">-InputObject</span></span>
<span data-ttu-id="35288-127">Das Objekt, das die zu entfernende Rollendefinition darstellt.</span><span class="sxs-lookup"><span data-stu-id="35288-127">The object representing the role definition to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35288-128">-Name</span><span class="sxs-lookup"><span data-stu-id="35288-128">-Name</span></span>
<span data-ttu-id="35288-129">Name der rollendefinition, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="35288-129">Name of the Role definition to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35288-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35288-130">-PassThru</span></span>
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

### <span data-ttu-id="35288-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="35288-131">-Scope</span></span>
<span data-ttu-id="35288-132">Bereich "Rollendefinition".</span><span class="sxs-lookup"><span data-stu-id="35288-132">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionIdParameterSet, RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35288-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="35288-133">-Confirm</span></span>
<span data-ttu-id="35288-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="35288-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35288-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35288-135">-WhatIf</span></span>
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

### <span data-ttu-id="35288-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35288-136">CommonParameters</span></span>
<span data-ttu-id="35288-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35288-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35288-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35288-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35288-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="35288-139">INPUTS</span></span>

### <span data-ttu-id="35288-140">System.Guid</span><span class="sxs-lookup"><span data-stu-id="35288-140">System.Guid</span></span>

### <span data-ttu-id="35288-141">System.String</span><span class="sxs-lookup"><span data-stu-id="35288-141">System.String</span></span>

### <span data-ttu-id="35288-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="35288-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="35288-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="35288-143">OUTPUTS</span></span>

### <span data-ttu-id="35288-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="35288-144">System.Boolean</span></span>

## <span data-ttu-id="35288-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="35288-145">NOTES</span></span>
<span data-ttu-id="35288-146">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="35288-146">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="35288-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="35288-147">RELATED LINKS</span></span>

[<span data-ttu-id="35288-148">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="35288-148">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="35288-149">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="35288-149">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="35288-150">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="35288-150">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

