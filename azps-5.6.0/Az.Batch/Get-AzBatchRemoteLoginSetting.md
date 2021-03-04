---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 9cb2207381e7f874884bc53b5b85572fdffbd1a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919035"
---
# <span data-ttu-id="ec4d0-101">Get-AzBatchRemoteLoginSetting</span><span class="sxs-lookup"><span data-stu-id="ec4d0-101">Get-AzBatchRemoteLoginSetting</span></span>

## <span data-ttu-id="ec4d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec4d0-102">SYNOPSIS</span></span>
<span data-ttu-id="ec4d0-103">Ruft Remoteanmeldungseinstellungen für einen Computeknoten ab.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-103">Gets remote logon settings for a compute node.</span></span>

## <span data-ttu-id="ec4d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec4d0-104">SYNTAX</span></span>

### <span data-ttu-id="ec4d0-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-105">Id (Default)</span></span>
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec4d0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ec4d0-106">InputObject</span></span>
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec4d0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec4d0-107">DESCRIPTION</span></span>
<span data-ttu-id="ec4d0-108">Das **Get-AzBatchRemoteLoginSetting-Cmdlet** ruft Remoteanmeldungseinstellungen für einen Computeknoten in einem infrastrukturbasierten Pool für virtuelle Computer ab.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-108">The **Get-AzBatchRemoteLoginSetting** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="ec4d0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ec4d0-109">EXAMPLES</span></span>

### <span data-ttu-id="ec4d0-110">Beispiel 1: Remoteanmeldungseinstellungen für alle Knoten in einem Pool</span><span class="sxs-lookup"><span data-stu-id="ec4d0-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="ec4d0-111">Der erste Befehl ruft mithilfe von **Get-AzBatchAccountKey einen Batchkontokontext** ab, der Zugriffstasten für Ihr Abonnement enthält.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="ec4d0-112">Der Befehl speichert den Kontext in der $Context, die im nächsten Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="ec4d0-113">Der zweite Befehl ruft jeden Computeknoten im Pool ab, der über die ID ContosoPool verfügt, indem **Get-AzBatchComputeNode verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="ec4d0-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzBatchComputeNode**.</span></span>
<span data-ttu-id="ec4d0-114">Der Befehl übergibt jeden Computerknoten mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ec4d0-115">Der Befehl ruft die Remoteanmeldungseinstellungen für jeden Computeknoten ab.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="ec4d0-116">Beispiel 2: Remoteanmeldungseinstellungen für einen Knoten erhalten</span><span class="sxs-lookup"><span data-stu-id="ec4d0-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="ec4d0-117">Der erste Befehl ruft einen Batchkontokontext ab, der Zugriffstasten für Ihr Abonnement enthält, und speichert ihn dann in der $Context Variablen.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>
<span data-ttu-id="ec4d0-118">Der zweite Befehl ruft die Remoteanmeldungseinstellungen für den Computeknoten ab, der die angegebene ID im Pool mit der ID ContosoPool hat.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="ec4d0-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ec4d0-119">PARAMETERS</span></span>

### <span data-ttu-id="ec4d0-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ec4d0-120">-BatchContext</span></span>
<span data-ttu-id="ec4d0-121">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ec4d0-122">Um einen **BatchAccountContext zu erhalten,** der Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzBatchAccountKey Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzBatchAccountKey cmdlet.</span></span>

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

### <span data-ttu-id="ec4d0-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="ec4d0-123">-ComputeNode</span></span>
<span data-ttu-id="ec4d0-124">Gibt einen Computeknoten als **PSComputeNode-Objekt** an, für den dieses Cmdlet Remoteanmeldungseinstellungen erhält.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="ec4d0-125">Verwenden Sie zum Abrufen eines Computeknotenobjekts das Get-AzBatchComputeNode Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-125">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="ec4d0-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="ec4d0-126">-ComputeNodeId</span></span>
<span data-ttu-id="ec4d0-127">Gibt die ID des Computeknotens an, für den die Einstellungen für die Remoteanmeldung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="ec4d0-128">für die dieses Cmdlet Remoteanmeldungseinstellungen erhält.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-128">for which this cmdlet gets remote logon settings.</span></span>

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

### <span data-ttu-id="ec4d0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec4d0-129">-DefaultProfile</span></span>
<span data-ttu-id="ec4d0-130">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec4d0-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ec4d0-131">-PoolId</span></span>
<span data-ttu-id="ec4d0-132">Gibt die ID des Pools an, der den virtuellen Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

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

### <span data-ttu-id="ec4d0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec4d0-133">CommonParameters</span></span>
<span data-ttu-id="ec4d0-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec4d0-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec4d0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec4d0-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ec4d0-136">INPUTS</span></span>

### <span data-ttu-id="ec4d0-137">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="ec4d0-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="ec4d0-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ec4d0-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ec4d0-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ec4d0-139">OUTPUTS</span></span>

### <span data-ttu-id="ec4d0-140">Microsoft.Azure.Commands.Batch. Models.PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="ec4d0-140">Microsoft.Azure.Commands.Batch.Models.PSRemoteLoginSettings</span></span>

## <span data-ttu-id="ec4d0-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ec4d0-141">NOTES</span></span>

## <span data-ttu-id="ec4d0-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ec4d0-142">RELATED LINKS</span></span>

[<span data-ttu-id="ec4d0-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ec4d0-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ec4d0-144">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ec4d0-144">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="ec4d0-145">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="ec4d0-145">Get-AzBatchRemoteDesktopProtocolFile</span></span>](./Get-AzBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="ec4d0-146">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="ec4d0-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
