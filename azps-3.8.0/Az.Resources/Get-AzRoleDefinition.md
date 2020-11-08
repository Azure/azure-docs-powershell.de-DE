---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: 5cd9a76f71f63b1d16003cce467d2d91eddc5b04
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996723"
---
# <span data-ttu-id="5a187-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5a187-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="5a187-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a187-102">SYNOPSIS</span></span>
<span data-ttu-id="5a187-103">Listet alle Azure-RBAC-Rollen auf, die für die Zuweisung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="5a187-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="5a187-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a187-104">SYNTAX</span></span>

### <span data-ttu-id="5a187-105">RoleDefinitionNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a187-105">RoleDefinitionNameParameterSet (Default)</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a187-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a187-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a187-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a187-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a187-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a187-108">DESCRIPTION</span></span>
<span data-ttu-id="5a187-109">Verwenden Sie den Befehl Get-AzRoleDefinition mit einem bestimmten Rollennamen, um dessen Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5a187-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="5a187-110">Überprüfen Sie die Aktionen und notacts-Eigenschaften der Rolle, um einzelne Vorgänge zu prüfen, denen eine Rolle Zugriff gewährt.</span><span class="sxs-lookup"><span data-stu-id="5a187-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="5a187-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a187-111">EXAMPLES</span></span>

### <span data-ttu-id="5a187-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5a187-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="5a187-113">Abrufen der Rollendefinition für Reader</span><span class="sxs-lookup"><span data-stu-id="5a187-113">Get the Reader role definition</span></span>

### <span data-ttu-id="5a187-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5a187-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="5a187-115">Listet alle RBAC-Rollendefinitionen auf</span><span class="sxs-lookup"><span data-stu-id="5a187-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="5a187-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a187-116">PARAMETERS</span></span>

### <span data-ttu-id="5a187-117">– Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="5a187-117">-Custom</span></span>
<span data-ttu-id="5a187-118">Wenn angegeben, werden nur die benutzerdefinierten erstellten Rollen im Verzeichnis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5a187-118">If specified, only displays the custom created roles in the directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a187-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a187-119">-DefaultProfile</span></span>
<span data-ttu-id="5a187-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5a187-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a187-121">-ID</span><span class="sxs-lookup"><span data-stu-id="5a187-121">-Id</span></span>
<span data-ttu-id="5a187-122">Rollen Definitions-ID.</span><span class="sxs-lookup"><span data-stu-id="5a187-122">Role definition Id.</span></span>

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

### <span data-ttu-id="5a187-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5a187-123">-Name</span></span>
<span data-ttu-id="5a187-124">Name der Rollendefinition</span><span class="sxs-lookup"><span data-stu-id="5a187-124">Role definition name.</span></span>
<span data-ttu-id="5a187-125">Für z.b. Leser, Mitwirkender, Teilnehmer der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="5a187-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a187-126">-Scope</span><span class="sxs-lookup"><span data-stu-id="5a187-126">-Scope</span></span>
<span data-ttu-id="5a187-127">Rollen Definitionsbereich.</span><span class="sxs-lookup"><span data-stu-id="5a187-127">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a187-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a187-128">CommonParameters</span></span>
<span data-ttu-id="5a187-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a187-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a187-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a187-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a187-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a187-131">INPUTS</span></span>

### <span data-ttu-id="5a187-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5a187-132">System.String</span></span>

### <span data-ttu-id="5a187-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="5a187-133">System.Guid</span></span>

### <span data-ttu-id="5a187-134">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="5a187-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5a187-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a187-135">OUTPUTS</span></span>

### <span data-ttu-id="5a187-136">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5a187-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="5a187-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a187-137">NOTES</span></span>
<span data-ttu-id="5a187-138">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="5a187-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="5a187-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a187-139">RELATED LINKS</span></span>

[<span data-ttu-id="5a187-140">Neu – AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5a187-140">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="5a187-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5a187-141">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="5a187-142">Neu – AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5a187-142">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="5a187-143">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5a187-143">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

