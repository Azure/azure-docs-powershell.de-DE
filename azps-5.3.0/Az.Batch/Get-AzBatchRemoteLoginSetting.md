---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 0e2360e6c4d0ba7d993f1f1aa21feb1b44115e6b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471163"
---
# <span data-ttu-id="662c9-101">Get-AzBatchRemoteLoginSetting</span><span class="sxs-lookup"><span data-stu-id="662c9-101">Get-AzBatchRemoteLoginSetting</span></span>

## <span data-ttu-id="662c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="662c9-102">SYNOPSIS</span></span>
<span data-ttu-id="662c9-103">Ruft Remoteanmeldungseinstellungen für einen Rechenknoten ab.</span><span class="sxs-lookup"><span data-stu-id="662c9-103">Gets remote logon settings for a compute node.</span></span>

## <span data-ttu-id="662c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="662c9-104">SYNTAX</span></span>

### <span data-ttu-id="662c9-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="662c9-105">Id (Default)</span></span>
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="662c9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="662c9-106">InputObject</span></span>
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="662c9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="662c9-107">DESCRIPTION</span></span>
<span data-ttu-id="662c9-108">Das **Cmdlet "Get-AzBatchRemoteLoginSetting"** ruft Remoteanmeldungseinstellungen für einen Rechenknoten in einem infrastrukturbasierten Pool virtueller Computer ab.</span><span class="sxs-lookup"><span data-stu-id="662c9-108">The **Get-AzBatchRemoteLoginSetting** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="662c9-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="662c9-109">EXAMPLES</span></span>

### <span data-ttu-id="662c9-110">Beispiel 1: Remoteanmeldungseinstellungen für alle Knoten in einem Pool erhalten</span><span class="sxs-lookup"><span data-stu-id="662c9-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="662c9-111">Der erste Befehl ruft mithilfe von **"Get-AzBatchAccountKey" einen Batchkontokontext** ab, der Zugriffstasten für Ihr Abonnement enthält.</span><span class="sxs-lookup"><span data-stu-id="662c9-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="662c9-112">Der Befehl speichert den Kontext in der $Context, die im nächsten Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="662c9-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="662c9-113">Der zweite Befehl ruft jeden Rechenknoten im Pool ab, der über die ID ContosoPool verfügt, indem **"Get-AzBatchComputeNode" verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="662c9-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzBatchComputeNode**.</span></span>
<span data-ttu-id="662c9-114">Der Befehl übergibt jeden Computerknoten mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="662c9-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="662c9-115">Der Befehl ruft die Remoteanmeldungseinstellungen für jeden Rechenknoten ab.</span><span class="sxs-lookup"><span data-stu-id="662c9-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="662c9-116">Beispiel 2: Erhalten von Remoteanmeldungseinstellungen für einen Knoten</span><span class="sxs-lookup"><span data-stu-id="662c9-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="662c9-117">Der erste Befehl ruft einen Batchkontokontext ab, der Zugriffstasten für Ihr Abonnement enthält, und speichert ihn dann in $Context Variable.</span><span class="sxs-lookup"><span data-stu-id="662c9-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>
<span data-ttu-id="662c9-118">Der zweite Befehl ruft die Remoteanmeldungseinstellungen für den Rechenknoten ab, der die angegebene ID im Pool mit der ID ContosoPool hat.</span><span class="sxs-lookup"><span data-stu-id="662c9-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="662c9-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="662c9-119">PARAMETERS</span></span>

### <span data-ttu-id="662c9-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="662c9-120">-BatchContext</span></span>
<span data-ttu-id="662c9-121">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="662c9-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="662c9-122">Verwenden Sie das **cmdlet "BatchAccountContext",** das Zugriffstasten für Ihr Abonnement enthält, Get-AzBatchAccountKey BatchAccountContext.</span><span class="sxs-lookup"><span data-stu-id="662c9-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzBatchAccountKey cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="662c9-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="662c9-123">-ComputeNode</span></span>
<span data-ttu-id="662c9-124">Gibt einen Computeknoten als ein **PSComputeNode-Objekt** an, für das dieses Cmdlet Remoteanmeldungseinstellungen erhält.</span><span class="sxs-lookup"><span data-stu-id="662c9-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="662c9-125">Verwenden Sie zum Abrufen eines Rechenknotenobjekts das Get-AzBatchComputeNode Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="662c9-125">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="662c9-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="662c9-126">-ComputeNodeId</span></span>
<span data-ttu-id="662c9-127">Gibt die ID des Rechenknotens an, für den die Remoteanmeldungseinstellungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="662c9-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="662c9-128">für die dieses Cmdlet Remoteanmeldungseinstellungen erhält.</span><span class="sxs-lookup"><span data-stu-id="662c9-128">for which this cmdlet gets remote logon settings.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="662c9-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="662c9-129">-DefaultProfile</span></span>
<span data-ttu-id="662c9-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="662c9-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="662c9-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="662c9-131">-PoolId</span></span>
<span data-ttu-id="662c9-132">Gibt die ID des Pools an, der den virtuellen Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="662c9-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="662c9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="662c9-133">CommonParameters</span></span>
<span data-ttu-id="662c9-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="662c9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="662c9-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="662c9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="662c9-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="662c9-136">INPUTS</span></span>

### <span data-ttu-id="662c9-137">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="662c9-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="662c9-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="662c9-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="662c9-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="662c9-139">OUTPUTS</span></span>

### <span data-ttu-id="662c9-140">Microsoft.Azure.Commands.Batch. Models.PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="662c9-140">Microsoft.Azure.Commands.Batch.Models.PSRemoteLoginSettings</span></span>

## <span data-ttu-id="662c9-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="662c9-141">NOTES</span></span>

## <span data-ttu-id="662c9-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="662c9-142">RELATED LINKS</span></span>

[<span data-ttu-id="662c9-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="662c9-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="662c9-144">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="662c9-144">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="662c9-145">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="662c9-145">Get-AzBatchRemoteDesktopProtocolFile</span></span>](./Get-AzBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="662c9-146">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="662c9-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
