---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6224a871aebff834693c8eed3026a75f22879ffa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178661"
---
# <span data-ttu-id="c06d9-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="c06d9-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="c06d9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c06d9-102">SYNOPSIS</span></span>
<span data-ttu-id="c06d9-103">Ruft Informationen zu Pipelines im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="c06d9-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="c06d9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c06d9-104">SYNTAX</span></span>

### <span data-ttu-id="c06d9-105">GetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c06d9-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c06d9-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="c06d9-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c06d9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c06d9-107">DESCRIPTION</span></span>
<span data-ttu-id="c06d9-108">Das Cmdlet " **Get-AzSynapsePipeline** " Ruft Informationen zu Pipelines im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="c06d9-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="c06d9-109">Wenn Sie den Namen einer Pipeline angeben, ruft dieses Cmdlet Informationen zu dieser Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="c06d9-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="c06d9-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Pipelines im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="c06d9-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="c06d9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c06d9-111">EXAMPLES</span></span>

### <span data-ttu-id="c06d9-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c06d9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="c06d9-113">Dieser Befehl ruft Informationen zu allen Pipelines im Arbeitsbereich mit dem Namen ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="c06d9-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="c06d9-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c06d9-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="c06d9-115">Dieser Befehl ruft Informationen zur Pipeline mit dem Namen ContosoPipeline im Arbeitsbereich mit dem Namen ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="c06d9-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="c06d9-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c06d9-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="c06d9-117">Dieser Befehl ruft Informationen zur Pipeline mit dem Namen ContosoPipeline im Arbeitsbereich mit dem Namen ContosoWorkspace through Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="c06d9-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="c06d9-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="c06d9-118">PARAMETERS</span></span>

### <span data-ttu-id="c06d9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c06d9-119">-DefaultProfile</span></span>
<span data-ttu-id="c06d9-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c06d9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c06d9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c06d9-121">-Name</span></span>
<span data-ttu-id="c06d9-122">Der Name der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c06d9-122">The pipeline name.</span></span>

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

### <span data-ttu-id="c06d9-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c06d9-123">-WorkspaceName</span></span>
<span data-ttu-id="c06d9-124">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="c06d9-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c06d9-125">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="c06d9-125">-WorkspaceObject</span></span>
<span data-ttu-id="c06d9-126">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="c06d9-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c06d9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c06d9-127">CommonParameters</span></span>
<span data-ttu-id="c06d9-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c06d9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c06d9-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c06d9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c06d9-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c06d9-130">INPUTS</span></span>

### <span data-ttu-id="c06d9-131">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c06d9-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c06d9-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c06d9-132">OUTPUTS</span></span>

### <span data-ttu-id="c06d9-133">Microsoft. Azure. Commands. Synapse. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="c06d9-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="c06d9-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="c06d9-134">NOTES</span></span>

## <span data-ttu-id="c06d9-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c06d9-135">RELATED LINKS</span></span>
