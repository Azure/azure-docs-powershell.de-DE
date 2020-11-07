---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 90b7b0b1d7909210d86ec1d5ac6b465f6e9fb239
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849887"
---
# <span data-ttu-id="bd4f0-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="bd4f0-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="bd4f0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bd4f0-102">SYNOPSIS</span></span>
<span data-ttu-id="bd4f0-103">Löscht eine benutzerdefinierte Rolle in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="bd4f0-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="bd4f0-104">Die zu löschende Rolle wird mit der ID-Eigenschaft der Rolle angegeben.</span><span class="sxs-lookup"><span data-stu-id="bd4f0-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="bd4f0-105">DELETE schlägt fehl, wenn vorhandene Rollenzuweisungen an der benutzerdefinierten Rolle vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="bd4f0-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd4f0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd4f0-106">SYNTAX</span></span>

### <span data-ttu-id="bd4f0-107">RoleDefinitionIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bd4f0-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd4f0-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd4f0-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd4f0-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd4f0-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd4f0-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd4f0-110">DESCRIPTION</span></span>
<span data-ttu-id="bd4f0-111">Das Remove-AzureRmRoleDefinition-Cmdlet löscht eine benutzerdefinierte Rolle in Azure Role-Based Zugriffssteuerung.</span><span class="sxs-lookup"><span data-stu-id="bd4f0-111">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="bd4f0-112">Stellen Sie den ID-Parameter einer vorhandenen benutzerdefinierten Rolle bereit, um diese benutzerdefinierte Rolle zu löschen.</span><span class="sxs-lookup"><span data-stu-id="bd4f0-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="bd4f0-113">Standardmäßig werden Sie von Remove-AzureRmRoleDefinition zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="bd4f0-113">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="bd4f0-114">Verwenden Sie den Parameter Force, um die Eingabeaufforderung zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="bd4f0-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="bd4f0-115">Wenn vorhandene Rollenzuweisungen an der zu löschenden benutzerdefinierten Rolle vorgenommen wurden, schlägt der Löschvorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="bd4f0-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="bd4f0-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bd4f0-116">EXAMPLES</span></span>

### <span data-ttu-id="bd4f0-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bd4f0-117">Example 1</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="bd4f0-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bd4f0-118">Example 2</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="bd4f0-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd4f0-119">PARAMETERS</span></span>

### <span data-ttu-id="bd4f0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd4f0-120">-DefaultProfile</span></span>
<span data-ttu-id="bd4f0-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="bd4f0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd4f0-122">-Force</span><span class="sxs-lookup"><span data-stu-id="bd4f0-122">-Force</span></span>
<span data-ttu-id="bd4f0-123">Wenn diese Einstellung eingestellt ist, wird keine Bestätigung angefordert, bevor die benutzerdefinierte Rolle gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="bd4f0-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="bd4f0-124">-ID</span><span class="sxs-lookup"><span data-stu-id="bd4f0-124">-Id</span></span>
<span data-ttu-id="bd4f0-125">Die ID der zu löschenden Rollendefinition</span><span class="sxs-lookup"><span data-stu-id="bd4f0-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="bd4f0-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bd4f0-126">-InputObject</span></span>
<span data-ttu-id="bd4f0-127">Das Objekt, das die zu entfernende Rollendefinition darstellt.</span><span class="sxs-lookup"><span data-stu-id="bd4f0-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="bd4f0-128">-Name</span><span class="sxs-lookup"><span data-stu-id="bd4f0-128">-Name</span></span>
<span data-ttu-id="bd4f0-129">Der Name der Rollendefinition, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd4f0-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="bd4f0-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd4f0-130">-PassThru</span></span>
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

### <span data-ttu-id="bd4f0-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="bd4f0-131">-Scope</span></span>
<span data-ttu-id="bd4f0-132">Rollen Definitionsbereich.</span><span class="sxs-lookup"><span data-stu-id="bd4f0-132">Role definition scope.</span></span>

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

### <span data-ttu-id="bd4f0-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bd4f0-133">-Confirm</span></span>
<span data-ttu-id="bd4f0-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bd4f0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd4f0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd4f0-135">-WhatIf</span></span>
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

### <span data-ttu-id="bd4f0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd4f0-136">CommonParameters</span></span>
<span data-ttu-id="bd4f0-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd4f0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd4f0-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd4f0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd4f0-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bd4f0-139">INPUTS</span></span>

### <span data-ttu-id="bd4f0-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="bd4f0-140">System.Guid</span></span>

### <span data-ttu-id="bd4f0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bd4f0-141">System.String</span></span>

### <span data-ttu-id="bd4f0-142">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="bd4f0-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="bd4f0-143">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bd4f0-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="bd4f0-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bd4f0-144">OUTPUTS</span></span>

### <span data-ttu-id="bd4f0-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bd4f0-145">System.Boolean</span></span>

## <span data-ttu-id="bd4f0-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="bd4f0-146">NOTES</span></span>
<span data-ttu-id="bd4f0-147">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="bd4f0-147">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="bd4f0-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bd4f0-148">RELATED LINKS</span></span>

[<span data-ttu-id="bd4f0-149">Neu – AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="bd4f0-149">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="bd4f0-150">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="bd4f0-150">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="bd4f0-151">Satz-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="bd4f0-151">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

