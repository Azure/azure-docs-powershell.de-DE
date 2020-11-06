---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
ms.openlocfilehash: 848f0cf3d2d36b9ff5c80792c23d126956dccfbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505657"
---
# <span data-ttu-id="c1233-101">Get-AzureBatchRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="c1233-101">Get-AzureBatchRemoteLoginSettings</span></span>

## <span data-ttu-id="c1233-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c1233-102">SYNOPSIS</span></span>
<span data-ttu-id="c1233-103">Ruft die Remote Anmeldeeinstellungen für einen Compute-Knoten ab.</span><span class="sxs-lookup"><span data-stu-id="c1233-103">Gets remote logon settings for a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1233-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1233-104">SYNTAX</span></span>

### <span data-ttu-id="c1233-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="c1233-105">Id (Default)</span></span>
```
Get-AzureBatchRemoteLoginSettings [-PoolId] <String> [-ComputeNodeId] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1233-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c1233-106">InputObject</span></span>
```
Get-AzureBatchRemoteLoginSettings [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1233-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1233-107">DESCRIPTION</span></span>
<span data-ttu-id="c1233-108">Das Cmdlet " **Get-AzureBatchRemoteLoginSettings** " ruft Remote Anmeldeeinstellungen für einen Compute-Knoten in einem auf Infrastruktur basierenden virtuellen Computerpool ab.</span><span class="sxs-lookup"><span data-stu-id="c1233-108">The **Get-AzureBatchRemoteLoginSettings** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="c1233-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1233-109">EXAMPLES</span></span>

### <span data-ttu-id="c1233-110">Beispiel 1: Abrufen von Remote Anmeldeeinstellungen für alle Knoten in einem Pool</span><span class="sxs-lookup"><span data-stu-id="c1233-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzureBatchRemoteLoginSettings -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="c1233-111">Der erste Befehl ruft einen Batch Konto Kontext ab, der Zugriffstasten für Ihr Abonnement enthält, indem **Sie Get-AzureRmBatchAccountKeys** verwenden.</span><span class="sxs-lookup"><span data-stu-id="c1233-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="c1233-112">Der Befehl speichert den Kontext in der $Context Variablen, die im nächsten Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c1233-112">The command stores the context in the $Context variable to use in the next command.</span></span>

<span data-ttu-id="c1233-113">Der zweite Befehl ruft jeden Compute-Knoten im Pool ab, der die ID-ContosoPool mithilfe von **Get-AzureBatchComputeNode**.</span><span class="sxs-lookup"><span data-stu-id="c1233-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzureBatchComputeNode**.</span></span>
<span data-ttu-id="c1233-114">Der Befehl übergibt die einzelnen Computerknoten mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1233-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c1233-115">Der Befehl ruft die Remote Anmeldeeinstellungen für jeden Compute-Knoten ab.</span><span class="sxs-lookup"><span data-stu-id="c1233-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="c1233-116">Beispiel 2: Abrufen der Remote Anmeldeeinstellungen für einen Knoten</span><span class="sxs-lookup"><span data-stu-id="c1233-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchRemoteLoginSettings -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="c1233-117">Der erste Befehl ruft einen Batch Konto Kontext ab, der Zugriffstasten für Ihr Abonnement enthält, und speichert ihn dann in der $Context-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c1233-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>

<span data-ttu-id="c1233-118">Der zweite Befehl ruft die Remote Anmeldeeinstellungen für den Compute-Knoten ab, auf dem sich die angegebene ID im Pool mit der ID ContosoPool befindet.</span><span class="sxs-lookup"><span data-stu-id="c1233-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="c1233-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1233-119">PARAMETERS</span></span>

### <span data-ttu-id="c1233-120">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="c1233-120">-BatchContext</span></span>
<span data-ttu-id="c1233-121">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="c1233-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c1233-122">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um eine **BatchAccountContext** zu erhalten, die Zugriffstasten für Ihr Abonnement enthält.</span><span class="sxs-lookup"><span data-stu-id="c1233-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="c1233-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="c1233-123">-ComputeNode</span></span>
<span data-ttu-id="c1233-124">Gibt einen Compute-Knoten als **PSComputeNode** -Objekt an, für das dieses Cmdlet Remote Anmeldeeinstellungen erhält.</span><span class="sxs-lookup"><span data-stu-id="c1233-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="c1233-125">Verwenden Sie das Get-AzureBatchComputeNode-Cmdlet, um ein Compute-Node-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c1233-125">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="c1233-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="c1233-126">-ComputeNodeId</span></span>
<span data-ttu-id="c1233-127">Gibt die ID des Compute-Knotens an, für den die Remote Anmeldeeinstellungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c1233-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="c1233-128">für die dieses Cmdlet Remote Anmeldeeinstellungen erhält.</span><span class="sxs-lookup"><span data-stu-id="c1233-128">for which this cmdlet gets remote logon settings.</span></span>

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

### <span data-ttu-id="c1233-129">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="c1233-129">-PoolId</span></span>
<span data-ttu-id="c1233-130">Gibt die ID des Pools an, der den virtuellen Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="c1233-130">Specifies the ID of the pool that contains the virtual machine.</span></span>

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

### <span data-ttu-id="c1233-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1233-131">-DefaultProfile</span></span>
<span data-ttu-id="c1233-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c1233-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1233-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1233-133">CommonParameters</span></span>
<span data-ttu-id="c1233-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1233-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1233-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1233-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1233-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c1233-136">INPUTS</span></span>

### <span data-ttu-id="c1233-137">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c1233-137">BatchAccountContext</span></span>
<span data-ttu-id="c1233-138">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c1233-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="c1233-139">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="c1233-139">PSComputeNode</span></span>
<span data-ttu-id="c1233-140">Der Parameter "ComputeNode" akzeptiert den Wert vom Typ "PSComputeNode" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c1233-140">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="c1233-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c1233-141">OUTPUTS</span></span>

### <span data-ttu-id="c1233-142">PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="c1233-142">PSRemoteLoginSettings</span></span>

## <span data-ttu-id="c1233-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="c1233-143">NOTES</span></span>

## <span data-ttu-id="c1233-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c1233-144">RELATED LINKS</span></span>

[<span data-ttu-id="c1233-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c1233-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c1233-146">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="c1233-146">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="c1233-147">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="c1233-147">Get-AzureBatchRemoteDesktopProtocolFile</span></span>](./Get-AzureBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="c1233-148">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="c1233-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


