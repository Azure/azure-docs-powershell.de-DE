---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 219ff64309cc11fd5e65d614f67d2d531737c8b1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849915"
---
# <span data-ttu-id="93d74-101">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="93d74-101">Get-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="93d74-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93d74-102">SYNOPSIS</span></span>
<span data-ttu-id="93d74-103">Listet alle Azure-RBAC-Rollen auf, die für die Zuweisung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="93d74-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93d74-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93d74-104">SYNTAX</span></span>

### <span data-ttu-id="93d74-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="93d74-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="93d74-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93d74-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="93d74-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="93d74-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93d74-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93d74-108">DESCRIPTION</span></span>
<span data-ttu-id="93d74-109">Verwenden Sie den Befehl Get-AzureRmRoleDefinition mit einem bestimmten Rollennamen, um dessen Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="93d74-109">Use the Get-AzureRmRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="93d74-110">Überprüfen Sie die Aktionen und notacts-Eigenschaften der Rolle, um einzelne Vorgänge zu prüfen, denen eine Rolle Zugriff gewährt.</span><span class="sxs-lookup"><span data-stu-id="93d74-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="93d74-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93d74-111">EXAMPLES</span></span>

### <span data-ttu-id="93d74-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="93d74-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRoleDefinition -Name Reader
```

<span data-ttu-id="93d74-113">Abrufen der Rollendefinition für Reader</span><span class="sxs-lookup"><span data-stu-id="93d74-113">Get the Reader role definition</span></span>

### <span data-ttu-id="93d74-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="93d74-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRoleDefinition
```

<span data-ttu-id="93d74-115">Listet alle RBAC-Rollendefinitionen auf</span><span class="sxs-lookup"><span data-stu-id="93d74-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="93d74-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="93d74-116">PARAMETERS</span></span>

### <span data-ttu-id="93d74-117">– Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="93d74-117">-Custom</span></span>
<span data-ttu-id="93d74-118">Wenn angegeben, werden nur die benutzerdefinierten erstellten Rollen im Verzeichnis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="93d74-118">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="93d74-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93d74-119">-DefaultProfile</span></span>
<span data-ttu-id="93d74-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="93d74-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93d74-121">-ID</span><span class="sxs-lookup"><span data-stu-id="93d74-121">-Id</span></span>
<span data-ttu-id="93d74-122">Rollen Definitions-ID.</span><span class="sxs-lookup"><span data-stu-id="93d74-122">Role definition Id.</span></span>

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

### <span data-ttu-id="93d74-123">-Name</span><span class="sxs-lookup"><span data-stu-id="93d74-123">-Name</span></span>
<span data-ttu-id="93d74-124">Name der Rollendefinition</span><span class="sxs-lookup"><span data-stu-id="93d74-124">Role definition name.</span></span>
<span data-ttu-id="93d74-125">Für z.b. Leser, Mitwirkender, Teilnehmer der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="93d74-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="93d74-126">-Scope</span><span class="sxs-lookup"><span data-stu-id="93d74-126">-Scope</span></span>
<span data-ttu-id="93d74-127">Rollen Definitionsbereich.</span><span class="sxs-lookup"><span data-stu-id="93d74-127">Role definition scope.</span></span>

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

### <span data-ttu-id="93d74-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93d74-128">CommonParameters</span></span>
<span data-ttu-id="93d74-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93d74-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93d74-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93d74-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93d74-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93d74-131">INPUTS</span></span>

### <span data-ttu-id="93d74-132">System. String</span><span class="sxs-lookup"><span data-stu-id="93d74-132">System.String</span></span>
<span data-ttu-id="93d74-133">Parameter: Scope (ByValue)</span><span class="sxs-lookup"><span data-stu-id="93d74-133">Parameters: Scope (ByValue)</span></span>

### <span data-ttu-id="93d74-134">System. GUID</span><span class="sxs-lookup"><span data-stu-id="93d74-134">System.Guid</span></span>

### <span data-ttu-id="93d74-135">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="93d74-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="93d74-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93d74-136">OUTPUTS</span></span>

### <span data-ttu-id="93d74-137">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="93d74-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="93d74-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="93d74-138">NOTES</span></span>
<span data-ttu-id="93d74-139">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="93d74-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="93d74-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93d74-140">RELATED LINKS</span></span>

[<span data-ttu-id="93d74-141">Neu – AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="93d74-141">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="93d74-142">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="93d74-142">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="93d74-143">Neu – AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="93d74-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="93d74-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="93d74-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

