---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
ms.openlocfilehash: 28a4742b2e744fb41bca9402a8c48b830554e231
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460008"
---
# <span data-ttu-id="b9aad-101">Get-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="b9aad-101">Get-AzSynapseNotebook</span></span>

## <span data-ttu-id="b9aad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9aad-102">SYNOPSIS</span></span>
<span data-ttu-id="b9aad-103">Ruft Informationen zu Notizbüchern in einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="b9aad-103">Gets information about notebooks in a workspace.</span></span>

## <span data-ttu-id="b9aad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9aad-104">SYNTAX</span></span>

### <span data-ttu-id="b9aad-105">GetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b9aad-105">GetByName (Default)</span></span>
```
Get-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9aad-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="b9aad-106">GetByObject</span></span>
```
Get-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9aad-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9aad-107">DESCRIPTION</span></span>
<span data-ttu-id="b9aad-108">Das **Cmdlet "Get-AzSynapseNotebook"** ruft Informationen zu Notizbüchern in einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="b9aad-108">The **Get-AzSynapseNotebook** cmdlet gets information about notebooks in a workspace.</span></span> <span data-ttu-id="b9aad-109">Wenn Sie den Namen eines Notizbuchs angeben, ruft das Cmdlet Informationen zu diesem Notizbuch ab.</span><span class="sxs-lookup"><span data-stu-id="b9aad-109">If you specify the name of a notebook, the cmdlet gets information about that notebook.</span></span> <span data-ttu-id="b9aad-110">Wenn Sie keinen Namen angeben, ruft das Cmdlet Informationen zu allen Notizbüchern im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="b9aad-110">If you do not specify a name, the cmdlet gets information about all notebooks in the workspace.</span></span>

## <span data-ttu-id="b9aad-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b9aad-111">EXAMPLES</span></span>

### <span data-ttu-id="b9aad-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b9aad-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace | Format-Table

WorkspaceName    Properties                                         Name
-------------    ----------                                         --
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook1
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook2
```

<span data-ttu-id="b9aad-113">Ruft eine Liste aller Notizbücher im Arbeitsbereich "ContosoWorkspace" ab.</span><span class="sxs-lookup"><span data-stu-id="b9aad-113">Gets a list of all notebooks in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="b9aad-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b9aad-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="b9aad-115">Ruft ein einzelnes Notizbuch namens "ContosoNotebook" im Arbeitsbereich "ContosoWorkspace" ab.</span><span class="sxs-lookup"><span data-stu-id="b9aad-115">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="b9aad-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b9aad-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="b9aad-117">Ruft über die Pipeline ein einzelnes Notizbuch namens "ContosoNotebook" im Arbeitsbereich "ContosoWorkspace" ab.</span><span class="sxs-lookup"><span data-stu-id="b9aad-117">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="b9aad-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9aad-118">PARAMETERS</span></span>

### <span data-ttu-id="b9aad-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9aad-119">-DefaultProfile</span></span>
<span data-ttu-id="b9aad-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b9aad-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9aad-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b9aad-121">-Name</span></span>
<span data-ttu-id="b9aad-122">Der Notizbuchname.</span><span class="sxs-lookup"><span data-stu-id="b9aad-122">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9aad-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b9aad-123">-WorkspaceName</span></span>
<span data-ttu-id="b9aad-124">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="b9aad-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9aad-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b9aad-125">-WorkspaceObject</span></span>
<span data-ttu-id="b9aad-126">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b9aad-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9aad-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9aad-127">CommonParameters</span></span>
<span data-ttu-id="b9aad-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9aad-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9aad-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9aad-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9aad-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b9aad-130">INPUTS</span></span>

### <span data-ttu-id="b9aad-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b9aad-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b9aad-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b9aad-132">OUTPUTS</span></span>

### <span data-ttu-id="b9aad-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="b9aad-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="b9aad-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b9aad-134">NOTES</span></span>

## <span data-ttu-id="b9aad-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b9aad-135">RELATED LINKS</span></span>
