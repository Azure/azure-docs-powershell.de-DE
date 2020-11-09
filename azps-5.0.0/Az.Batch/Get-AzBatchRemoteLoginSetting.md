---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 0e2360e6c4d0ba7d993f1f1aa21feb1b44115e6b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299710"
---
# <span data-ttu-id="27421-101">Get-AzBatchRemoteLoginSetting</span><span class="sxs-lookup"><span data-stu-id="27421-101">Get-AzBatchRemoteLoginSetting</span></span>

## <span data-ttu-id="27421-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="27421-102">SYNOPSIS</span></span>
<span data-ttu-id="27421-103">Ruft die Remote Anmeldeeinstellungen für einen Compute-Knoten ab.</span><span class="sxs-lookup"><span data-stu-id="27421-103">Gets remote logon settings for a compute node.</span></span>

## <span data-ttu-id="27421-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="27421-104">SYNTAX</span></span>

### <span data-ttu-id="27421-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="27421-105">Id (Default)</span></span>
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27421-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="27421-106">InputObject</span></span>
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27421-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="27421-107">DESCRIPTION</span></span>
<span data-ttu-id="27421-108">Das Cmdlet " **Get-AzBatchRemoteLoginSetting** " ruft Remote Anmeldeeinstellungen für einen Compute-Knoten in einem auf Infrastruktur basierenden virtuellen Computerpool ab.</span><span class="sxs-lookup"><span data-stu-id="27421-108">The **Get-AzBatchRemoteLoginSetting** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="27421-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="27421-109">EXAMPLES</span></span>

### <span data-ttu-id="27421-110">Beispiel 1: Abrufen von Remote Anmeldeeinstellungen für alle Knoten in einem Pool</span><span class="sxs-lookup"><span data-stu-id="27421-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="27421-111">Der erste Befehl ruft einen Batch Konto Kontext ab, der Zugriffstasten für Ihr Abonnement enthält, indem **Sie Get-AzBatchAccountKey** verwenden.</span><span class="sxs-lookup"><span data-stu-id="27421-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="27421-112">Der Befehl speichert den Kontext in der $Context Variablen, die im nächsten Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="27421-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="27421-113">Der zweite Befehl ruft jeden Compute-Knoten im Pool ab, der die ID-ContosoPool mithilfe von **Get-AzBatchComputeNode**.</span><span class="sxs-lookup"><span data-stu-id="27421-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzBatchComputeNode**.</span></span>
<span data-ttu-id="27421-114">Der Befehl übergibt die einzelnen Computerknoten mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27421-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="27421-115">Der Befehl ruft die Remote Anmeldeeinstellungen für jeden Compute-Knoten ab.</span><span class="sxs-lookup"><span data-stu-id="27421-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="27421-116">Beispiel 2: Abrufen der Remote Anmeldeeinstellungen für einen Knoten</span><span class="sxs-lookup"><span data-stu-id="27421-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="27421-117">Der erste Befehl ruft einen Batch Konto Kontext ab, der Zugriffstasten für Ihr Abonnement enthält, und speichert ihn dann in der $Context-Variablen.</span><span class="sxs-lookup"><span data-stu-id="27421-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>
<span data-ttu-id="27421-118">Der zweite Befehl ruft die Remote Anmeldeeinstellungen für den Compute-Knoten ab, auf dem sich die angegebene ID im Pool mit der ID ContosoPool befindet.</span><span class="sxs-lookup"><span data-stu-id="27421-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="27421-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="27421-119">PARAMETERS</span></span>

### <span data-ttu-id="27421-120">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="27421-120">-BatchContext</span></span>
<span data-ttu-id="27421-121">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="27421-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="27421-122">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um eine **BatchAccountContext** zu erhalten, die Zugriffstasten für Ihr Abonnement enthält.</span><span class="sxs-lookup"><span data-stu-id="27421-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzBatchAccountKey cmdlet.</span></span>

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

### <span data-ttu-id="27421-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="27421-123">-ComputeNode</span></span>
<span data-ttu-id="27421-124">Gibt einen Compute-Knoten als **PSComputeNode** -Objekt an, für das dieses Cmdlet Remote Anmeldeeinstellungen erhält.</span><span class="sxs-lookup"><span data-stu-id="27421-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="27421-125">Verwenden Sie das Get-AzBatchComputeNode-Cmdlet, um ein Compute-Node-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="27421-125">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="27421-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="27421-126">-ComputeNodeId</span></span>
<span data-ttu-id="27421-127">Gibt die ID des Compute-Knotens an, für den die Remote Anmeldeeinstellungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="27421-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="27421-128">für die dieses Cmdlet Remote Anmeldeeinstellungen erhält.</span><span class="sxs-lookup"><span data-stu-id="27421-128">for which this cmdlet gets remote logon settings.</span></span>

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

### <span data-ttu-id="27421-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27421-129">-DefaultProfile</span></span>
<span data-ttu-id="27421-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="27421-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27421-131">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="27421-131">-PoolId</span></span>
<span data-ttu-id="27421-132">Gibt die ID des Pools an, der den virtuellen Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="27421-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

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

### <span data-ttu-id="27421-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27421-133">CommonParameters</span></span>
<span data-ttu-id="27421-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27421-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27421-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27421-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27421-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="27421-136">INPUTS</span></span>

### <span data-ttu-id="27421-137">Microsoft.Azure.Commands.Batch. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="27421-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="27421-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="27421-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="27421-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="27421-139">OUTPUTS</span></span>

### <span data-ttu-id="27421-140">Microsoft.Azure.Commands.Batch. Models. PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="27421-140">Microsoft.Azure.Commands.Batch.Models.PSRemoteLoginSettings</span></span>

## <span data-ttu-id="27421-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="27421-141">NOTES</span></span>

## <span data-ttu-id="27421-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="27421-142">RELATED LINKS</span></span>

[<span data-ttu-id="27421-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="27421-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="27421-144">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="27421-144">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="27421-145">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="27421-145">Get-AzBatchRemoteDesktopProtocolFile</span></span>](./Get-AzBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="27421-146">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="27421-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
