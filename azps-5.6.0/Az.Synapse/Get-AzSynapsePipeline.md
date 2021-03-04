---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6161a0ca463973fad1ac7bac5df6487cf23cd0e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926211"
---
# <span data-ttu-id="10feb-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="10feb-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="10feb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10feb-102">SYNOPSIS</span></span>
<span data-ttu-id="10feb-103">Ruft Informationen zu Pipelines im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="10feb-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="10feb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10feb-104">SYNTAX</span></span>

### <span data-ttu-id="10feb-105">GetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="10feb-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10feb-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="10feb-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10feb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10feb-107">DESCRIPTION</span></span>
<span data-ttu-id="10feb-108">Das **Get-AzSynapsePipeline-Cmdlet** ruft Informationen zu Pipelines im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="10feb-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="10feb-109">Wenn Sie den Namen einer Pipeline angeben, ruft dieses Cmdlet Informationen zu dieser Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="10feb-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="10feb-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Pipelines im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="10feb-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="10feb-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="10feb-111">EXAMPLES</span></span>

### <span data-ttu-id="10feb-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="10feb-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="10feb-113">Dieser Befehl ruft Informationen zu allen Pipelines im Arbeitsbereich namens ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="10feb-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="10feb-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="10feb-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="10feb-115">Dieser Befehl ruft Informationen zur Pipeline namens ContosoPipeline im Arbeitsbereich namens ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="10feb-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="10feb-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="10feb-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="10feb-117">Dieser Befehl ruft Informationen zur Pipeline namens ContosoPipeline im Arbeitsbereich namens ContosoWorkspace über die Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="10feb-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="10feb-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="10feb-118">PARAMETERS</span></span>

### <span data-ttu-id="10feb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10feb-119">-DefaultProfile</span></span>
<span data-ttu-id="10feb-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10feb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10feb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="10feb-121">-Name</span></span>
<span data-ttu-id="10feb-122">Der Name der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="10feb-122">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10feb-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="10feb-123">-WorkspaceName</span></span>
<span data-ttu-id="10feb-124">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="10feb-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="10feb-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="10feb-125">-WorkspaceObject</span></span>
<span data-ttu-id="10feb-126">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="10feb-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="10feb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10feb-127">CommonParameters</span></span>
<span data-ttu-id="10feb-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10feb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10feb-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10feb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10feb-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="10feb-130">INPUTS</span></span>

### <span data-ttu-id="10feb-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="10feb-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="10feb-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="10feb-132">OUTPUTS</span></span>

### <span data-ttu-id="10feb-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="10feb-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="10feb-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="10feb-134">NOTES</span></span>

## <span data-ttu-id="10feb-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="10feb-135">RELATED LINKS</span></span>
