---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: f2ac7efad3c08a351e515eccbe519306a89f06a9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178169"
---
# <span data-ttu-id="c5473-101">Get-AzSynapseRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c5473-101">Get-AzSynapseRoleDefinition</span></span>

## <span data-ttu-id="c5473-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c5473-102">SYNOPSIS</span></span>
<span data-ttu-id="c5473-103">Ruft eine Synapse-Analyse Rollendefinition ab.</span><span class="sxs-lookup"><span data-stu-id="c5473-103">Gets a Synapse Analytics role definition.</span></span>

## <span data-ttu-id="c5473-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5473-104">SYNTAX</span></span>

### <span data-ttu-id="c5473-105">GetByWorkspaceNameAndIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c5473-105">GetByWorkspaceNameAndIdParameterSet (Default)</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5473-106">GetByWorkspaceNameAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5473-106">GetByWorkspaceNameAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5473-107">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5473-107">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5473-108">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5473-108">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5473-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5473-109">DESCRIPTION</span></span>
<span data-ttu-id="c5473-110">Das Cmdlet " **Get-AzSynapseRoleDefinition** " Ruft eine Azure Synapse-Analyse Rollen Definition ab.</span><span class="sxs-lookup"><span data-stu-id="c5473-110">The **Get-AzSynapseRoleDefinition** cmdlet gets an Azure Synapse Analytics Role Definition.</span></span>
<span data-ttu-id="c5473-111">Wenn Sie keinen Rollennamen oder keine Rollen-ID angeben, ruft dieses Cmdlet alle Rollendefinitionen ab.</span><span class="sxs-lookup"><span data-stu-id="c5473-111">If you do not specify a role name or a role Id, this cmdlet gets all role definitions.</span></span>

## <span data-ttu-id="c5473-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5473-112">EXAMPLES</span></span>

### <span data-ttu-id="c5473-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c5473-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="c5473-114">Dieser Befehl ruft alle Rollendefinitionen unter einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="c5473-114">This command gets all role definitions under a workspace.</span></span>

### <span data-ttu-id="c5473-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c5473-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

<span data-ttu-id="c5473-116">Dieser Befehl ruft die Rollendefinition unter Workspace ContosoWorkspace mit dem Namen ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="c5473-116">This command gets the role definition under workspace ContosoWorkspace with name ContosoRole.</span></span>

### <span data-ttu-id="c5473-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c5473-117">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

<span data-ttu-id="c5473-118">Dieser Befehl ruft alle Rollendefinitionen unter einem Arbeitsbereich durch Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="c5473-118">This command gets all role definitions under a workspace through pipeline.</span></span>

## <span data-ttu-id="c5473-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5473-119">PARAMETERS</span></span>

### <span data-ttu-id="c5473-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5473-120">-DefaultProfile</span></span>
<span data-ttu-id="c5473-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c5473-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5473-122">-ID</span><span class="sxs-lookup"><span data-stu-id="c5473-122">-Id</span></span>
<span data-ttu-id="c5473-123">Die ID der Rolle, die dem Prinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c5473-123">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5473-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c5473-124">-Name</span></span>
<span data-ttu-id="c5473-125">Der Name der Rolle, die dem Prinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c5473-125">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5473-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c5473-126">-WorkspaceName</span></span>
<span data-ttu-id="c5473-127">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="c5473-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5473-128">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="c5473-128">-WorkspaceObject</span></span>
<span data-ttu-id="c5473-129">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="c5473-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5473-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5473-130">CommonParameters</span></span>
<span data-ttu-id="c5473-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5473-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5473-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5473-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5473-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c5473-133">INPUTS</span></span>

### <span data-ttu-id="c5473-134">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c5473-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c5473-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c5473-135">OUTPUTS</span></span>

### <span data-ttu-id="c5473-136">Microsoft. Azure. Commands. Synapse. Models. PSSynapseRole</span><span class="sxs-lookup"><span data-stu-id="c5473-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span></span>

## <span data-ttu-id="c5473-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="c5473-137">NOTES</span></span>

## <span data-ttu-id="c5473-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c5473-138">RELATED LINKS</span></span>
