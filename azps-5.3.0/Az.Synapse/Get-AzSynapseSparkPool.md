---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
ms.openlocfilehash: fd1dbcc2e70b4d44de0c105af2332a9e4836d3bc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383983"
---
# <span data-ttu-id="349b6-101">Get-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="349b6-101">Get-AzSynapseSparkPool</span></span>

## <span data-ttu-id="349b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="349b6-102">SYNOPSIS</span></span>
<span data-ttu-id="349b6-103">Ruft einen Synapse Analytics Spark-Pool ab.</span><span class="sxs-lookup"><span data-stu-id="349b6-103">Gets a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="349b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="349b6-104">SYNTAX</span></span>

### <span data-ttu-id="349b6-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="349b6-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="349b6-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="349b6-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkPool [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="349b6-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="349b6-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSparkPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="349b6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="349b6-108">DESCRIPTION</span></span>
<span data-ttu-id="349b6-109">Das **Cmdlet "Get-AzSynapseSparkPool"** ruft Informationen zu einem Azure Synapse Analytics Spark-Pool ab.</span><span class="sxs-lookup"><span data-stu-id="349b6-109">The **Get-AzSynapseSparkPool** cmdlet gets information about an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="349b6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="349b6-110">EXAMPLES</span></span>

### <span data-ttu-id="349b6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="349b6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="349b6-112">Dieser Befehl ruft alle Sparkpools unter einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="349b6-112">This command gets all Spark pools under a workspace.</span></span>

### <span data-ttu-id="349b6-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="349b6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="349b6-114">Mit diesem Befehl wird der Sparkpool unter dem Arbeitsbereich "ContosoWorkspace" mit dem Namen "ContosoSparkPool" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="349b6-114">This command gets the Spark pool under workspace ContosoWorkspace with name ContosoSparkPool.</span></span>

### <span data-ttu-id="349b6-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="349b6-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSparkPool
```

<span data-ttu-id="349b6-116">Dieser Befehl ruft alle Sparkpools unter einem Arbeitsbereich über die Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="349b6-116">This command gets all Spark pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="349b6-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="349b6-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool"
```

<span data-ttu-id="349b6-118">Dieser Befehl ruft den Sparkpool mit der angegebenen Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="349b6-118">This command gets the Spark pool with the specified resource ID.</span></span>

## <span data-ttu-id="349b6-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="349b6-119">PARAMETERS</span></span>

### <span data-ttu-id="349b6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="349b6-120">-DefaultProfile</span></span>
<span data-ttu-id="349b6-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="349b6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="349b6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="349b6-122">-Name</span></span>
<span data-ttu-id="349b6-123">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="349b6-123">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: SparkPoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349b6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="349b6-124">-ResourceGroupName</span></span>
<span data-ttu-id="349b6-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="349b6-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349b6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="349b6-126">-ResourceId</span></span>
<span data-ttu-id="349b6-127">Ressourcenbezeichner des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="349b6-127">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349b6-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="349b6-128">-WorkspaceName</span></span>
<span data-ttu-id="349b6-129">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="349b6-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349b6-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="349b6-130">-WorkspaceObject</span></span>
<span data-ttu-id="349b6-131">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="349b6-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="349b6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="349b6-132">CommonParameters</span></span>
<span data-ttu-id="349b6-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="349b6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="349b6-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="349b6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="349b6-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="349b6-135">INPUTS</span></span>

### <span data-ttu-id="349b6-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="349b6-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="349b6-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="349b6-137">OUTPUTS</span></span>

### <span data-ttu-id="349b6-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="349b6-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="349b6-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="349b6-139">NOTES</span></span>

## <span data-ttu-id="349b6-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="349b6-140">RELATED LINKS</span></span>
