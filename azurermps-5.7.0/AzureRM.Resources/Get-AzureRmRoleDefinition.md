---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
ms.openlocfilehash: c1850cdc410df064a97950bb38f3734657649467
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501406"
---
# <span data-ttu-id="77198-101">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="77198-101">Get-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="77198-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="77198-102">SYNOPSIS</span></span>
<span data-ttu-id="77198-103">Listet alle Azure-RBAC-Rollen auf, die für die Zuweisung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="77198-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77198-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="77198-104">SYNTAX</span></span>

### <span data-ttu-id="77198-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="77198-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77198-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77198-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="77198-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="77198-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77198-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77198-108">DESCRIPTION</span></span>
<span data-ttu-id="77198-109">Verwenden Sie den Befehl Get-AzureRmRoleDefinition mit einem bestimmten Rollennamen, um dessen Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="77198-109">Use the Get-AzureRmRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="77198-110">Überprüfen Sie die Aktionen und notacts-Eigenschaften der Rolle, um einzelne Vorgänge zu prüfen, denen eine Rolle Zugriff gewährt.</span><span class="sxs-lookup"><span data-stu-id="77198-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="77198-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77198-111">EXAMPLES</span></span>

### <span data-ttu-id="77198-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="77198-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRoleDefinition -Name Reader
```

<span data-ttu-id="77198-113">Abrufen der Rollendefinition für Reader</span><span class="sxs-lookup"><span data-stu-id="77198-113">Get the Reader role definition</span></span>

### <span data-ttu-id="77198-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="77198-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRoleDefinition
```

<span data-ttu-id="77198-115">Listet alle RBAC-Rollendefinitionen auf</span><span class="sxs-lookup"><span data-stu-id="77198-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="77198-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="77198-116">PARAMETERS</span></span>

### <span data-ttu-id="77198-117">-AtScopeAndBelow</span><span class="sxs-lookup"><span data-stu-id="77198-117">-AtScopeAndBelow</span></span>
<span data-ttu-id="77198-118">Wenn angegeben, werden alle Rollendefinitionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="77198-118">If specified, displays all role definitions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RoleDefinitionNameParameterSet, RoleDefinitionCustomParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77198-119">– Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="77198-119">-Custom</span></span>
<span data-ttu-id="77198-120">Wenn angegeben, werden nur die benutzerdefinierten erstellten Rollen im Verzeichnis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="77198-120">If specified, only displays the custom created roles in the directory.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77198-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77198-121">-DefaultProfile</span></span>
<span data-ttu-id="77198-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="77198-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77198-123">-ID</span><span class="sxs-lookup"><span data-stu-id="77198-123">-Id</span></span>
<span data-ttu-id="77198-124">Rollen Definitions-ID.</span><span class="sxs-lookup"><span data-stu-id="77198-124">Role definition Id.</span></span>

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

### <span data-ttu-id="77198-125">-Name</span><span class="sxs-lookup"><span data-stu-id="77198-125">-Name</span></span>
<span data-ttu-id="77198-126">Name der Rollendefinition</span><span class="sxs-lookup"><span data-stu-id="77198-126">Role definition name.</span></span>
<span data-ttu-id="77198-127">Für z.b. Leser, Mitwirkender, Teilnehmer der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="77198-127">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

```yaml
Type: String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77198-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="77198-128">-Scope</span></span>
<span data-ttu-id="77198-129">Rollen Definitionsbereich.</span><span class="sxs-lookup"><span data-stu-id="77198-129">Role definition scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77198-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77198-130">CommonParameters</span></span>
<span data-ttu-id="77198-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77198-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77198-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77198-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77198-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="77198-133">INPUTS</span></span>

### <span data-ttu-id="77198-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="77198-134">String</span></span>
<span data-ttu-id="77198-135">Der Parameter "Scope" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="77198-135">Parameter 'Scope' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="77198-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="77198-136">OUTPUTS</span></span>

### <span data-ttu-id="77198-137">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition]</span><span class="sxs-lookup"><span data-stu-id="77198-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition]</span></span>

## <span data-ttu-id="77198-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="77198-138">NOTES</span></span>
<span data-ttu-id="77198-139">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="77198-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="77198-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="77198-140">RELATED LINKS</span></span>

[<span data-ttu-id="77198-141">Neu – AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="77198-141">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="77198-142">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="77198-142">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="77198-143">Neu – AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="77198-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="77198-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="77198-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

