---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
ms.openlocfilehash: 8919c554fb32a102991b9c40236e897662709ccb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460028"
---
# <span data-ttu-id="a5d7e-101">Get-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="a5d7e-101">Get-AzSynapseDataset</span></span>

## <span data-ttu-id="a5d7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5d7e-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d7e-103">Ruft Informationen zu Datasets im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="a5d7e-103">Gets information about datasets in workspace.</span></span>

## <span data-ttu-id="a5d7e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5d7e-104">SYNTAX</span></span>

### <span data-ttu-id="a5d7e-105">GetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5d7e-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataset -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5d7e-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="a5d7e-106">GetByObject</span></span>
```
Get-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5d7e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5d7e-107">DESCRIPTION</span></span>
<span data-ttu-id="a5d7e-108">Das **Cmdlet "Get-AzSynapseDataset"** ruft Informationen zu Datasets im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="a5d7e-108">The **Get-AzSynapseDataset** cmdlet gets information about datasets in workspace.</span></span>
<span data-ttu-id="a5d7e-109">Wenn Sie den Namen eines Datasets angeben, ruft dieses Cmdlet Informationen zu diesem Dataset ab.</span><span class="sxs-lookup"><span data-stu-id="a5d7e-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="a5d7e-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datasets im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="a5d7e-110">If you do not specify a name, this cmdlet gets information about all the datasets in the workspace.</span></span>

## <span data-ttu-id="a5d7e-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a5d7e-111">EXAMPLES</span></span>

### <span data-ttu-id="a5d7e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a5d7e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a5d7e-113">Dieser Befehl ruft Informationen zu allen Datasets im Arbeitsbereich namens ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="a5d7e-113">This command gets information about all datasets in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a5d7e-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a5d7e-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="a5d7e-115">Dieser Befehl ruft Informationen über das Dataset mit dem Namen "ContosoDataset" im Arbeitsbereich "ContosoWorkspace" ab.</span><span class="sxs-lookup"><span data-stu-id="a5d7e-115">This command gets information about the dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="a5d7e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5d7e-116">PARAMETERS</span></span>

### <span data-ttu-id="a5d7e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d7e-117">-DefaultProfile</span></span>
<span data-ttu-id="a5d7e-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5d7e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5d7e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a5d7e-119">-Name</span></span>
<span data-ttu-id="a5d7e-120">Der Datasetname.</span><span class="sxs-lookup"><span data-stu-id="a5d7e-120">The dataset name.</span></span>

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

### <span data-ttu-id="a5d7e-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a5d7e-121">-WorkspaceName</span></span>
<span data-ttu-id="a5d7e-122">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a5d7e-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a5d7e-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a5d7e-123">-WorkspaceObject</span></span>
<span data-ttu-id="a5d7e-124">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a5d7e-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a5d7e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d7e-125">CommonParameters</span></span>
<span data-ttu-id="a5d7e-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5d7e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d7e-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5d7e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d7e-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a5d7e-128">INPUTS</span></span>

### <span data-ttu-id="a5d7e-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a5d7e-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a5d7e-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a5d7e-130">OUTPUTS</span></span>

### <span data-ttu-id="a5d7e-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="a5d7e-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="a5d7e-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a5d7e-132">NOTES</span></span>

## <span data-ttu-id="a5d7e-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a5d7e-133">RELATED LINKS</span></span>
