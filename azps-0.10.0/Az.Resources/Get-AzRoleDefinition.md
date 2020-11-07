---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: d43ec874af02d57abedddb1b49b3cc8723af5c2e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843396"
---
# <span data-ttu-id="10c9a-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="10c9a-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="10c9a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="10c9a-102">SYNOPSIS</span></span>
<span data-ttu-id="10c9a-103">Listet alle Azure-RBAC-Rollen auf, die für die Zuweisung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="10c9a-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="10c9a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="10c9a-104">SYNTAX</span></span>

### <span data-ttu-id="10c9a-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="10c9a-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10c9a-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10c9a-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10c9a-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="10c9a-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10c9a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10c9a-108">DESCRIPTION</span></span>
<span data-ttu-id="10c9a-109">Verwenden Sie den Befehl Get-AzRoleDefinition mit einem bestimmten Rollennamen, um dessen Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="10c9a-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="10c9a-110">Überprüfen Sie die Aktionen und notacts-Eigenschaften der Rolle, um einzelne Vorgänge zu prüfen, denen eine Rolle Zugriff gewährt.</span><span class="sxs-lookup"><span data-stu-id="10c9a-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="10c9a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="10c9a-111">EXAMPLES</span></span>

### <span data-ttu-id="10c9a-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="10c9a-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="10c9a-113">Abrufen der Rollendefinition für Reader</span><span class="sxs-lookup"><span data-stu-id="10c9a-113">Get the Reader role definition</span></span>

### <span data-ttu-id="10c9a-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="10c9a-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="10c9a-115">Listet alle RBAC-Rollendefinitionen auf</span><span class="sxs-lookup"><span data-stu-id="10c9a-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="10c9a-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="10c9a-116">PARAMETERS</span></span>

### <span data-ttu-id="10c9a-117">– Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="10c9a-117">-Custom</span></span>
<span data-ttu-id="10c9a-118">Wenn angegeben, werden nur die benutzerdefinierten erstellten Rollen im Verzeichnis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="10c9a-118">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="10c9a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10c9a-119">-DefaultProfile</span></span>
<span data-ttu-id="10c9a-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="10c9a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c9a-121">-ID</span><span class="sxs-lookup"><span data-stu-id="10c9a-121">-Id</span></span>
<span data-ttu-id="10c9a-122">Rollen Definitions-ID.</span><span class="sxs-lookup"><span data-stu-id="10c9a-122">Role definition Id.</span></span>

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

### <span data-ttu-id="10c9a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="10c9a-123">-Name</span></span>
<span data-ttu-id="10c9a-124">Name der Rollendefinition</span><span class="sxs-lookup"><span data-stu-id="10c9a-124">Role definition name.</span></span>
<span data-ttu-id="10c9a-125">Für z.b. Leser, Mitwirkender, Teilnehmer der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="10c9a-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="10c9a-126">-Scope</span><span class="sxs-lookup"><span data-stu-id="10c9a-126">-Scope</span></span>
<span data-ttu-id="10c9a-127">Rollen Definitionsbereich.</span><span class="sxs-lookup"><span data-stu-id="10c9a-127">Role definition scope.</span></span>

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

### <span data-ttu-id="10c9a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10c9a-128">CommonParameters</span></span>
<span data-ttu-id="10c9a-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10c9a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10c9a-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10c9a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10c9a-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="10c9a-131">INPUTS</span></span>

### <span data-ttu-id="10c9a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="10c9a-132">System.String</span></span>
<span data-ttu-id="10c9a-133">Parameter: Scope (ByValue)</span><span class="sxs-lookup"><span data-stu-id="10c9a-133">Parameters: Scope (ByValue)</span></span>

### <span data-ttu-id="10c9a-134">System. GUID</span><span class="sxs-lookup"><span data-stu-id="10c9a-134">System.Guid</span></span>

### <span data-ttu-id="10c9a-135">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="10c9a-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="10c9a-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="10c9a-136">OUTPUTS</span></span>

### <span data-ttu-id="10c9a-137">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="10c9a-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="10c9a-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="10c9a-138">NOTES</span></span>
<span data-ttu-id="10c9a-139">Schlüsselwörter: Azure, AZ, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="10c9a-139">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="10c9a-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="10c9a-140">RELATED LINKS</span></span>

[<span data-ttu-id="10c9a-141">Neu – AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="10c9a-141">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="10c9a-142">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="10c9a-142">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="10c9a-143">Neu – AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="10c9a-143">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="10c9a-144">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="10c9a-144">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

