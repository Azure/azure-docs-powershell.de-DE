---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: a2bd64daf4b9895de3ef8ca12ff0fec7295cd094
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180029"
---
# <span data-ttu-id="3deca-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3deca-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="3deca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3deca-102">SYNOPSIS</span></span>
<span data-ttu-id="3deca-103">Löscht eine benutzerdefinierte Rolle in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="3deca-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="3deca-104">Die zu löschende Rolle wird mit der ID-Eigenschaft der Rolle angegeben.</span><span class="sxs-lookup"><span data-stu-id="3deca-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="3deca-105">DELETE schlägt fehl, wenn vorhandene Rollenzuweisungen an der benutzerdefinierten Rolle vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="3deca-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="3deca-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3deca-106">SYNTAX</span></span>

### <span data-ttu-id="3deca-107">RoleDefinitionIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3deca-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3deca-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3deca-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3deca-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3deca-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3deca-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3deca-110">DESCRIPTION</span></span>
<span data-ttu-id="3deca-111">Das Remove-AzRoleDefinition-Cmdlet löscht eine benutzerdefinierte Rolle in Azure Role-Based Zugriffssteuerung.</span><span class="sxs-lookup"><span data-stu-id="3deca-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="3deca-112">Stellen Sie den ID-Parameter einer vorhandenen benutzerdefinierten Rolle bereit, um diese benutzerdefinierte Rolle zu löschen.</span><span class="sxs-lookup"><span data-stu-id="3deca-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="3deca-113">Standardmäßig werden Sie von Remove-AzRoleDefinition zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="3deca-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="3deca-114">Verwenden Sie den Parameter Force, um die Eingabeaufforderung zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="3deca-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="3deca-115">Wenn vorhandene Rollenzuweisungen an der zu löschenden benutzerdefinierten Rolle vorgenommen wurden, schlägt der Löschvorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="3deca-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="3deca-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3deca-116">EXAMPLES</span></span>

### <span data-ttu-id="3deca-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3deca-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="3deca-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3deca-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="3deca-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="3deca-119">PARAMETERS</span></span>

### <span data-ttu-id="3deca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3deca-120">-DefaultProfile</span></span>
<span data-ttu-id="3deca-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3deca-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3deca-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3deca-122">-Force</span></span>
<span data-ttu-id="3deca-123">Wenn diese Einstellung eingestellt ist, wird keine Bestätigung angefordert, bevor die benutzerdefinierte Rolle gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="3deca-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="3deca-124">-ID</span><span class="sxs-lookup"><span data-stu-id="3deca-124">-Id</span></span>
<span data-ttu-id="3deca-125">Die ID der zu löschenden Rollendefinition</span><span class="sxs-lookup"><span data-stu-id="3deca-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="3deca-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3deca-126">-InputObject</span></span>
<span data-ttu-id="3deca-127">Das Objekt, das die zu entfernende Rollendefinition darstellt.</span><span class="sxs-lookup"><span data-stu-id="3deca-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="3deca-128">-Name</span><span class="sxs-lookup"><span data-stu-id="3deca-128">-Name</span></span>
<span data-ttu-id="3deca-129">Der Name der Rollendefinition, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="3deca-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="3deca-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3deca-130">-PassThru</span></span>
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

### <span data-ttu-id="3deca-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="3deca-131">-Scope</span></span>
<span data-ttu-id="3deca-132">Rollen Definitionsbereich.</span><span class="sxs-lookup"><span data-stu-id="3deca-132">Role definition scope.</span></span>

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

### <span data-ttu-id="3deca-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3deca-133">-Confirm</span></span>
<span data-ttu-id="3deca-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3deca-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3deca-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3deca-135">-WhatIf</span></span>
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

### <span data-ttu-id="3deca-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3deca-136">CommonParameters</span></span>
<span data-ttu-id="3deca-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3deca-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3deca-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3deca-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3deca-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3deca-139">INPUTS</span></span>

### <span data-ttu-id="3deca-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="3deca-140">System.Guid</span></span>

### <span data-ttu-id="3deca-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3deca-141">System.String</span></span>

### <span data-ttu-id="3deca-142">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3deca-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="3deca-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3deca-143">OUTPUTS</span></span>

### <span data-ttu-id="3deca-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3deca-144">System.Boolean</span></span>

## <span data-ttu-id="3deca-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="3deca-145">NOTES</span></span>
<span data-ttu-id="3deca-146">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="3deca-146">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="3deca-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3deca-147">RELATED LINKS</span></span>

[<span data-ttu-id="3deca-148">Neu – AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3deca-148">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="3deca-149">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3deca-149">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="3deca-150">Satz-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3deca-150">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

