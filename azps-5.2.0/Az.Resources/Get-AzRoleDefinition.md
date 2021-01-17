---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: 5cd9a76f71f63b1d16003cce467d2d91eddc5b04
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365894"
---
# <span data-ttu-id="86321-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="86321-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="86321-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86321-102">SYNOPSIS</span></span>
<span data-ttu-id="86321-103">Listet alle Azure-RBAC-Rollen auf, die zur Zuweisung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="86321-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="86321-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86321-104">SYNTAX</span></span>

### <span data-ttu-id="86321-105">RoleDefinitionNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="86321-105">RoleDefinitionNameParameterSet (Default)</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86321-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86321-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86321-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="86321-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="86321-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86321-108">DESCRIPTION</span></span>
<span data-ttu-id="86321-109">Verwenden Sie den Get-AzRoleDefinition mit einem bestimmten Rollennamen, um die Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="86321-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="86321-110">Um einzelne Vorgänge zu prüfen, auf die eine Rolle Zugriff gewährt, überprüfen Sie die Eigenschaften "Actions" und "NotActions" der Rolle.</span><span class="sxs-lookup"><span data-stu-id="86321-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="86321-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="86321-111">EXAMPLES</span></span>

### <span data-ttu-id="86321-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="86321-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="86321-113">Übernehmen der Rollendefinition "Reader"</span><span class="sxs-lookup"><span data-stu-id="86321-113">Get the Reader role definition</span></span>

### <span data-ttu-id="86321-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="86321-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="86321-115">Listet alle Rollendefinitionen für RBAC auf.</span><span class="sxs-lookup"><span data-stu-id="86321-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="86321-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86321-116">PARAMETERS</span></span>

### <span data-ttu-id="86321-117">-Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="86321-117">-Custom</span></span>
<span data-ttu-id="86321-118">Falls angegeben, werden nur die benutzerdefinierten erstellten Rollen im Verzeichnis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="86321-118">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="86321-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86321-119">-DefaultProfile</span></span>
<span data-ttu-id="86321-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="86321-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86321-121">-ID</span><span class="sxs-lookup"><span data-stu-id="86321-121">-Id</span></span>
<span data-ttu-id="86321-122">Rollendefinitions-ID.</span><span class="sxs-lookup"><span data-stu-id="86321-122">Role definition Id.</span></span>

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

### <span data-ttu-id="86321-123">-Name</span><span class="sxs-lookup"><span data-stu-id="86321-123">-Name</span></span>
<span data-ttu-id="86321-124">Name der Rollendefinition.</span><span class="sxs-lookup"><span data-stu-id="86321-124">Role definition name.</span></span>
<span data-ttu-id="86321-125">Für z. B. Leser, Mitwirkender, Mitwirkender virtueller Computer.</span><span class="sxs-lookup"><span data-stu-id="86321-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="86321-126">-Scope</span><span class="sxs-lookup"><span data-stu-id="86321-126">-Scope</span></span>
<span data-ttu-id="86321-127">Bereich "Rollendefinition".</span><span class="sxs-lookup"><span data-stu-id="86321-127">Role definition scope.</span></span>

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

### <span data-ttu-id="86321-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86321-128">CommonParameters</span></span>
<span data-ttu-id="86321-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86321-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86321-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86321-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86321-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="86321-131">INPUTS</span></span>

### <span data-ttu-id="86321-132">System.String</span><span class="sxs-lookup"><span data-stu-id="86321-132">System.String</span></span>

### <span data-ttu-id="86321-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="86321-133">System.Guid</span></span>

### <span data-ttu-id="86321-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="86321-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="86321-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="86321-135">OUTPUTS</span></span>

### <span data-ttu-id="86321-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="86321-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="86321-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="86321-137">NOTES</span></span>
<span data-ttu-id="86321-138">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="86321-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="86321-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="86321-139">RELATED LINKS</span></span>

[<span data-ttu-id="86321-140">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="86321-140">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="86321-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="86321-141">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="86321-142">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="86321-142">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="86321-143">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="86321-143">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

