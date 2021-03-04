---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
ms.openlocfilehash: 7d586af76115ddf7cada5a443dd10d51463fe576
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933536"
---
# <span data-ttu-id="54e8a-101">Get-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="54e8a-101">Get-AzSynapseDataset</span></span>

## <span data-ttu-id="54e8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="54e8a-103">Ruft Informationen zu Datasets im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="54e8a-103">Gets information about datasets in workspace.</span></span>

## <span data-ttu-id="54e8a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54e8a-104">SYNTAX</span></span>

### <span data-ttu-id="54e8a-105">GetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="54e8a-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataset -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54e8a-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="54e8a-106">GetByObject</span></span>
```
Get-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54e8a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54e8a-107">DESCRIPTION</span></span>
<span data-ttu-id="54e8a-108">Das **Get-AzSynapseDataset-Cmdlet** ruft Informationen zu Datasets im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="54e8a-108">The **Get-AzSynapseDataset** cmdlet gets information about datasets in workspace.</span></span>
<span data-ttu-id="54e8a-109">Wenn Sie den Namen eines Datasets angeben, ruft dieses Cmdlet Informationen zu diesem Dataset ab.</span><span class="sxs-lookup"><span data-stu-id="54e8a-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="54e8a-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datasets im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="54e8a-110">If you do not specify a name, this cmdlet gets information about all the datasets in the workspace.</span></span>

## <span data-ttu-id="54e8a-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="54e8a-111">EXAMPLES</span></span>

### <span data-ttu-id="54e8a-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="54e8a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="54e8a-113">Dieser Befehl ruft Informationen zu allen Datasets im Arbeitsbereich namens ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="54e8a-113">This command gets information about all datasets in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="54e8a-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="54e8a-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="54e8a-115">Dieser Befehl ruft Informationen zum Dataset namens ContosoDataset im Arbeitsbereich namens ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="54e8a-115">This command gets information about the dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="54e8a-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="54e8a-116">PARAMETERS</span></span>

### <span data-ttu-id="54e8a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54e8a-117">-DefaultProfile</span></span>
<span data-ttu-id="54e8a-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54e8a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54e8a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="54e8a-119">-Name</span></span>
<span data-ttu-id="54e8a-120">Der Name des Datasets.</span><span class="sxs-lookup"><span data-stu-id="54e8a-120">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54e8a-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="54e8a-121">-WorkspaceName</span></span>
<span data-ttu-id="54e8a-122">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="54e8a-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="54e8a-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="54e8a-123">-WorkspaceObject</span></span>
<span data-ttu-id="54e8a-124">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="54e8a-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="54e8a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54e8a-125">CommonParameters</span></span>
<span data-ttu-id="54e8a-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54e8a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54e8a-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54e8a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54e8a-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="54e8a-128">INPUTS</span></span>

### <span data-ttu-id="54e8a-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="54e8a-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="54e8a-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="54e8a-130">OUTPUTS</span></span>

### <span data-ttu-id="54e8a-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="54e8a-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="54e8a-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="54e8a-132">NOTES</span></span>

## <span data-ttu-id="54e8a-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="54e8a-133">RELATED LINKS</span></span>
