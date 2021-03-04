---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 0fa0069686a34fbd1ee60d31df96386a5d7959d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933539"
---
# <span data-ttu-id="40135-101">Get-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="40135-101">Get-AzSynapseDataFlow</span></span>

## <span data-ttu-id="40135-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40135-102">SYNOPSIS</span></span>
<span data-ttu-id="40135-103">Ruft Informationen zu Datenflüssen im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="40135-103">Gets information about data flows in workspace.</span></span>

## <span data-ttu-id="40135-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40135-104">SYNTAX</span></span>

### <span data-ttu-id="40135-105">GetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="40135-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="40135-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="40135-106">GetByObject</span></span>
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40135-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40135-107">DESCRIPTION</span></span>
<span data-ttu-id="40135-108">Das **Get-AzSynapseDataFlow-Cmdlet** ruft Informationen zu Datenflüssen im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="40135-108">The **Get-AzSynapseDataFlow** cmdlet gets information about data flows in workspace.</span></span>
<span data-ttu-id="40135-109">Wenn Sie den Namen eines Datenflusses angeben, ruft dieses Cmdlet Informationen zu diesem Datenfluss ab.</span><span class="sxs-lookup"><span data-stu-id="40135-109">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="40135-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datenflüssen im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="40135-110">If you do not specify a name, this cmdlet gets information about all the data flows in the workspace.</span></span>

## <span data-ttu-id="40135-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="40135-111">EXAMPLES</span></span>

### <span data-ttu-id="40135-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="40135-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="40135-113">Dieser Befehl ruft Informationen zu allen Datenflüssen im Arbeitsbereich namens ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="40135-113">This command gets information about all data flows in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="40135-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="40135-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="40135-115">Dieser Befehl ruft Informationen zum Datenfluss namens ContosoDataFlow im Arbeitsbereich namens ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="40135-115">This command gets information about the data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="40135-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="40135-116">PARAMETERS</span></span>

### <span data-ttu-id="40135-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40135-117">-DefaultProfile</span></span>
<span data-ttu-id="40135-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40135-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40135-119">-Name</span><span class="sxs-lookup"><span data-stu-id="40135-119">-Name</span></span>
<span data-ttu-id="40135-120">Der Name des Datenflusses.</span><span class="sxs-lookup"><span data-stu-id="40135-120">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40135-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="40135-121">-WorkspaceName</span></span>
<span data-ttu-id="40135-122">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="40135-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="40135-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="40135-123">-WorkspaceObject</span></span>
<span data-ttu-id="40135-124">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="40135-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="40135-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40135-125">CommonParameters</span></span>
<span data-ttu-id="40135-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40135-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40135-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40135-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40135-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="40135-128">INPUTS</span></span>

### <span data-ttu-id="40135-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="40135-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="40135-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="40135-130">OUTPUTS</span></span>

### <span data-ttu-id="40135-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="40135-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="40135-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="40135-132">NOTES</span></span>

## <span data-ttu-id="40135-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="40135-133">RELATED LINKS</span></span>
