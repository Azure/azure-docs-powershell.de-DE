---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
ms.openlocfilehash: df22eb6fa435c3cf8bca4b339e460b3415991964
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926216"
---
# <span data-ttu-id="ea41c-101">Get-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="ea41c-101">Get-AzSynapseNotebook</span></span>

## <span data-ttu-id="ea41c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea41c-102">SYNOPSIS</span></span>
<span data-ttu-id="ea41c-103">Ruft Informationen zu Notizbüchern in einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="ea41c-103">Gets information about notebooks in a workspace.</span></span>

## <span data-ttu-id="ea41c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea41c-104">SYNTAX</span></span>

### <span data-ttu-id="ea41c-105">GetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ea41c-105">GetByName (Default)</span></span>
```
Get-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea41c-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="ea41c-106">GetByObject</span></span>
```
Get-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea41c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea41c-107">DESCRIPTION</span></span>
<span data-ttu-id="ea41c-108">Das **Cmdlet Get-AzSynapseNotebook** ruft Informationen zu Notizbüchern in einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="ea41c-108">The **Get-AzSynapseNotebook** cmdlet gets information about notebooks in a workspace.</span></span> <span data-ttu-id="ea41c-109">Wenn Sie den Namen eines Notizbuchs angeben, erhält das Cmdlet Informationen zu diesem Notizbuch.</span><span class="sxs-lookup"><span data-stu-id="ea41c-109">If you specify the name of a notebook, the cmdlet gets information about that notebook.</span></span> <span data-ttu-id="ea41c-110">Wenn Sie keinen Namen angeben, ruft das Cmdlet Informationen zu allen Notizbüchern im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="ea41c-110">If you do not specify a name, the cmdlet gets information about all notebooks in the workspace.</span></span>

## <span data-ttu-id="ea41c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ea41c-111">EXAMPLES</span></span>

### <span data-ttu-id="ea41c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ea41c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace | Format-Table

WorkspaceName    Properties                                         Name
-------------    ----------                                         --
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook1
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook2
```

<span data-ttu-id="ea41c-113">Ruft eine Liste aller Notizbücher im Arbeitsbereich ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="ea41c-113">Gets a list of all notebooks in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="ea41c-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ea41c-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="ea41c-115">Ruft ein einzelnes Notizbuch namens ContosoNotebook im Arbeitsbereich ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="ea41c-115">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="ea41c-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ea41c-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="ea41c-117">Ruft ein einzelnes Notizbuch namens ContosoNotebook im Arbeitsbereich ContosoWorkspace über die Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="ea41c-117">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="ea41c-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ea41c-118">PARAMETERS</span></span>

### <span data-ttu-id="ea41c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea41c-119">-DefaultProfile</span></span>
<span data-ttu-id="ea41c-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea41c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea41c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ea41c-121">-Name</span></span>
<span data-ttu-id="ea41c-122">Der Name des Notizbuchs.</span><span class="sxs-lookup"><span data-stu-id="ea41c-122">The notebook name.</span></span>

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

### <span data-ttu-id="ea41c-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ea41c-123">-WorkspaceName</span></span>
<span data-ttu-id="ea41c-124">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="ea41c-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ea41c-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ea41c-125">-WorkspaceObject</span></span>
<span data-ttu-id="ea41c-126">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ea41c-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ea41c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea41c-127">CommonParameters</span></span>
<span data-ttu-id="ea41c-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea41c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea41c-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea41c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea41c-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ea41c-130">INPUTS</span></span>

### <span data-ttu-id="ea41c-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ea41c-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ea41c-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ea41c-132">OUTPUTS</span></span>

### <span data-ttu-id="ea41c-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="ea41c-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="ea41c-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ea41c-134">NOTES</span></span>

## <span data-ttu-id="ea41c-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ea41c-135">RELATED LINKS</span></span>
