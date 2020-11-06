---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
ms.openlocfilehash: ae4f8e11ac213943d8cfcec162b43abde60fe753
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502474"
---
# <span data-ttu-id="a0e0f-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a0e0f-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="a0e0f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0e0f-102">SYNOPSIS</span></span>
<span data-ttu-id="a0e0f-103">Löscht eine benutzerdefinierte Rolle in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="a0e0f-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="a0e0f-104">Die zu löschende Rolle wird mit der ID-Eigenschaft der Rolle angegeben.</span><span class="sxs-lookup"><span data-stu-id="a0e0f-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="a0e0f-105">DELETE schlägt fehl, wenn vorhandene Rollenzuweisungen an der benutzerdefinierten Rolle vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="a0e0f-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0e0f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0e0f-106">SYNTAX</span></span>

### <span data-ttu-id="a0e0f-107">RoleDefinitionIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0e0f-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0e0f-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0e0f-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0e0f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0e0f-109">DESCRIPTION</span></span>
<span data-ttu-id="a0e0f-110">Das Remove-AzureRmRoleDefinition-Cmdlet löscht eine benutzerdefinierte Rolle in Azure Role-Based Zugriffssteuerung.</span><span class="sxs-lookup"><span data-stu-id="a0e0f-110">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="a0e0f-111">Stellen Sie den ID-Parameter einer vorhandenen benutzerdefinierten Rolle bereit, um diese benutzerdefinierte Rolle zu löschen.</span><span class="sxs-lookup"><span data-stu-id="a0e0f-111">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="a0e0f-112">Standardmäßig werden Sie von Remove-AzureRmRoleDefinition zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="a0e0f-112">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="a0e0f-113">Verwenden Sie den Parameter Force, um die Eingabeaufforderung zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="a0e0f-113">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="a0e0f-114">Wenn vorhandene Rollenzuweisungen an der zu löschenden benutzerdefinierten Rolle vorgenommen wurden, schlägt der Löschvorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="a0e0f-114">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="a0e0f-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0e0f-115">EXAMPLES</span></span>

### <span data-ttu-id="a0e0f-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a0e0f-116">Example 1</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="a0e0f-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a0e0f-117">Example 2</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="a0e0f-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0e0f-118">PARAMETERS</span></span>

### <span data-ttu-id="a0e0f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0e0f-119">-DefaultProfile</span></span>
<span data-ttu-id="a0e0f-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a0e0f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0e0f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a0e0f-121">-Force</span></span>
<span data-ttu-id="a0e0f-122">Wenn diese Einstellung eingestellt ist, wird keine Bestätigung angefordert, bevor die benutzerdefinierte Rolle gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="a0e0f-122">If set, does not prompt for a confirmation before deleting the custom role</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0e0f-123">-ID</span><span class="sxs-lookup"><span data-stu-id="a0e0f-123">-Id</span></span>
<span data-ttu-id="a0e0f-124">Die ID der zu löschenden Rollendefinition</span><span class="sxs-lookup"><span data-stu-id="a0e0f-124">Id of the Role definition to be deleted</span></span>

```yaml
Type: Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0e0f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a0e0f-125">-Name</span></span>
<span data-ttu-id="a0e0f-126">Der Name der Rollendefinition, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0e0f-126">Name of the Role definition to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0e0f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0e0f-127">-PassThru</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0e0f-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="a0e0f-128">-Scope</span></span>
<span data-ttu-id="a0e0f-129">Rollen Definitionsbereich.</span><span class="sxs-lookup"><span data-stu-id="a0e0f-129">Role definition scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0e0f-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a0e0f-130">-Confirm</span></span>
<span data-ttu-id="a0e0f-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0e0f-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0e0f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0e0f-132">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0e0f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0e0f-133">CommonParameters</span></span>
<span data-ttu-id="a0e0f-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0e0f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0e0f-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0e0f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0e0f-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0e0f-136">INPUTS</span></span>

### <span data-ttu-id="a0e0f-137">Keine</span><span class="sxs-lookup"><span data-stu-id="a0e0f-137">None</span></span>
<span data-ttu-id="a0e0f-138">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a0e0f-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a0e0f-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0e0f-139">OUTPUTS</span></span>

### <span data-ttu-id="a0e0f-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0e0f-140">System.Boolean</span></span>

## <span data-ttu-id="a0e0f-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0e0f-141">NOTES</span></span>
<span data-ttu-id="a0e0f-142">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="a0e0f-142">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a0e0f-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0e0f-143">RELATED LINKS</span></span>

[<span data-ttu-id="a0e0f-144">Neu – AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a0e0f-144">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="a0e0f-145">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a0e0f-145">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="a0e0f-146">Satz-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a0e0f-146">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

