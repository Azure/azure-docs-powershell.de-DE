---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
ms.openlocfilehash: 6669cdfad83c8e5f4299abe0d1297f7e0659a42c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503413"
---
# <span data-ttu-id="1b14c-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1b14c-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="1b14c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1b14c-102">SYNOPSIS</span></span>
<span data-ttu-id="1b14c-103">Löscht eine benutzerdefinierte Rolle in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="1b14c-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="1b14c-104">Die zu löschende Rolle wird mit der ID-Eigenschaft der Rolle angegeben.</span><span class="sxs-lookup"><span data-stu-id="1b14c-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="1b14c-105">DELETE schlägt fehl, wenn vorhandene Rollenzuweisungen an der benutzerdefinierten Rolle vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="1b14c-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b14c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b14c-106">SYNTAX</span></span>

### <span data-ttu-id="1b14c-107">RoleDefinitionIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1b14c-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b14c-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b14c-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b14c-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b14c-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b14c-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b14c-110">DESCRIPTION</span></span>
<span data-ttu-id="1b14c-111">Das Remove-AzureRmRoleDefinition-Cmdlet löscht eine benutzerdefinierte Rolle in Azure Role-Based Zugriffssteuerung.</span><span class="sxs-lookup"><span data-stu-id="1b14c-111">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="1b14c-112">Stellen Sie den ID-Parameter einer vorhandenen benutzerdefinierten Rolle bereit, um diese benutzerdefinierte Rolle zu löschen.</span><span class="sxs-lookup"><span data-stu-id="1b14c-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="1b14c-113">Standardmäßig werden Sie von Remove-AzureRmRoleDefinition zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="1b14c-113">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="1b14c-114">Verwenden Sie den Parameter Force, um die Eingabeaufforderung zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="1b14c-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="1b14c-115">Wenn vorhandene Rollenzuweisungen an der zu löschenden benutzerdefinierten Rolle vorgenommen wurden, schlägt der Löschvorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="1b14c-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="1b14c-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1b14c-116">EXAMPLES</span></span>

### <span data-ttu-id="1b14c-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1b14c-117">Example 1</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="1b14c-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1b14c-118">Example 2</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="1b14c-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b14c-119">PARAMETERS</span></span>

### <span data-ttu-id="1b14c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b14c-120">-DefaultProfile</span></span>
<span data-ttu-id="1b14c-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1b14c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b14c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="1b14c-122">-Force</span></span>
<span data-ttu-id="1b14c-123">Wenn diese Einstellung eingestellt ist, wird keine Bestätigung angefordert, bevor die benutzerdefinierte Rolle gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="1b14c-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="1b14c-124">-ID</span><span class="sxs-lookup"><span data-stu-id="1b14c-124">-Id</span></span>
<span data-ttu-id="1b14c-125">Die ID der zu löschenden Rollendefinition</span><span class="sxs-lookup"><span data-stu-id="1b14c-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="1b14c-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1b14c-126">-InputObject</span></span>
<span data-ttu-id="1b14c-127">Das Objekt, das die zu entfernende Rollendefinition darstellt.</span><span class="sxs-lookup"><span data-stu-id="1b14c-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="1b14c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="1b14c-128">-Name</span></span>
<span data-ttu-id="1b14c-129">Der Name der Rollendefinition, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b14c-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="1b14c-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b14c-130">-PassThru</span></span>
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

### <span data-ttu-id="1b14c-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="1b14c-131">-Scope</span></span>
<span data-ttu-id="1b14c-132">Rollen Definitionsbereich.</span><span class="sxs-lookup"><span data-stu-id="1b14c-132">Role definition scope.</span></span>

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

### <span data-ttu-id="1b14c-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1b14c-133">-Confirm</span></span>
<span data-ttu-id="1b14c-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1b14c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b14c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b14c-135">-WhatIf</span></span>
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

### <span data-ttu-id="1b14c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b14c-136">CommonParameters</span></span>
<span data-ttu-id="1b14c-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b14c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b14c-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b14c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b14c-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1b14c-139">INPUTS</span></span>

### <span data-ttu-id="1b14c-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1b14c-140">System.Guid</span></span>

### <span data-ttu-id="1b14c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1b14c-141">System.String</span></span>

### <span data-ttu-id="1b14c-142">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1b14c-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="1b14c-143">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1b14c-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1b14c-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1b14c-144">OUTPUTS</span></span>

### <span data-ttu-id="1b14c-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1b14c-145">System.Boolean</span></span>

## <span data-ttu-id="1b14c-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="1b14c-146">NOTES</span></span>
<span data-ttu-id="1b14c-147">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="1b14c-147">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="1b14c-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1b14c-148">RELATED LINKS</span></span>

[<span data-ttu-id="1b14c-149">Neu – AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1b14c-149">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="1b14c-150">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1b14c-150">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="1b14c-151">Satz-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1b14c-151">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

