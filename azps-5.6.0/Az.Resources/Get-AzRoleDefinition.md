---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: 724daa3cce0bd8fe38a645fcdd3acd2d3ce7bf1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938464"
---
# <span data-ttu-id="52942-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="52942-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="52942-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52942-102">SYNOPSIS</span></span>
<span data-ttu-id="52942-103">Listet alle Azure RBAC-Rollen auf, die für die Zuweisung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="52942-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="52942-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52942-104">SYNTAX</span></span>

### <span data-ttu-id="52942-105">RoleDefinitionNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="52942-105">RoleDefinitionNameParameterSet (Default)</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="52942-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52942-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="52942-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="52942-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52942-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52942-108">DESCRIPTION</span></span>
<span data-ttu-id="52942-109">Verwenden Sie Get-AzRoleDefinition befehl mit einem bestimmten Rollennamen, um die Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="52942-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="52942-110">Um einzelne Vorgänge zu prüfen, auf die eine Rolle Zugriff gewährt, überprüfen Sie die Eigenschaften Aktionen und NotActions der Rolle.</span><span class="sxs-lookup"><span data-stu-id="52942-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="52942-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="52942-111">EXAMPLES</span></span>

### <span data-ttu-id="52942-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="52942-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="52942-113">Herunterladen der Rollendefinition "Leser"</span><span class="sxs-lookup"><span data-stu-id="52942-113">Get the Reader role definition</span></span>

### <span data-ttu-id="52942-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="52942-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="52942-115">Listet alle ROLLENAC-Rollendefinitionen auf</span><span class="sxs-lookup"><span data-stu-id="52942-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="52942-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="52942-116">PARAMETERS</span></span>

### <span data-ttu-id="52942-117">-Custom</span><span class="sxs-lookup"><span data-stu-id="52942-117">-Custom</span></span>
<span data-ttu-id="52942-118">Wenn angegeben, werden nur die benutzerdefinierten erstellten Rollen im Verzeichnis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="52942-118">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="52942-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52942-119">-DefaultProfile</span></span>
<span data-ttu-id="52942-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="52942-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52942-121">-ID</span><span class="sxs-lookup"><span data-stu-id="52942-121">-Id</span></span>
<span data-ttu-id="52942-122">Rollendefinitions-ID.</span><span class="sxs-lookup"><span data-stu-id="52942-122">Role definition Id.</span></span>

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

### <span data-ttu-id="52942-123">-Name</span><span class="sxs-lookup"><span data-stu-id="52942-123">-Name</span></span>
<span data-ttu-id="52942-124">Name der Rollendefinition.</span><span class="sxs-lookup"><span data-stu-id="52942-124">Role definition name.</span></span>
<span data-ttu-id="52942-125">Für z. B. Reader, Mitwirkender, Mitwirkender virtueller Computer.</span><span class="sxs-lookup"><span data-stu-id="52942-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="52942-126">-Scope</span><span class="sxs-lookup"><span data-stu-id="52942-126">-Scope</span></span>
<span data-ttu-id="52942-127">Bereich "Rollendefinition".</span><span class="sxs-lookup"><span data-stu-id="52942-127">Role definition scope.</span></span>

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

### <span data-ttu-id="52942-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52942-128">CommonParameters</span></span>
<span data-ttu-id="52942-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52942-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52942-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52942-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52942-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="52942-131">INPUTS</span></span>

### <span data-ttu-id="52942-132">System.String</span><span class="sxs-lookup"><span data-stu-id="52942-132">System.String</span></span>

### <span data-ttu-id="52942-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="52942-133">System.Guid</span></span>

### <span data-ttu-id="52942-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="52942-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="52942-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="52942-135">OUTPUTS</span></span>

### <span data-ttu-id="52942-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="52942-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="52942-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="52942-137">NOTES</span></span>
<span data-ttu-id="52942-138">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="52942-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="52942-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="52942-139">RELATED LINKS</span></span>

[<span data-ttu-id="52942-140">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="52942-140">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="52942-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="52942-141">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="52942-142">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="52942-142">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="52942-143">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="52942-143">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

