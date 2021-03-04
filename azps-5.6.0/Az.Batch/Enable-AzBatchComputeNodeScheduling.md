---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 2897a21f25ac0a91fec11d83b77c8219d12f88ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941288"
---
# <span data-ttu-id="b66db-101">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="b66db-101">Enable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="b66db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b66db-102">SYNOPSIS</span></span>
<span data-ttu-id="b66db-103">Ermöglicht die Aufgabenplanung für den angegebenen Computeknoten.</span><span class="sxs-lookup"><span data-stu-id="b66db-103">Enables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="b66db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b66db-104">SYNTAX</span></span>

### <span data-ttu-id="b66db-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="b66db-105">Id (Default)</span></span>
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b66db-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b66db-106">InputObject</span></span>
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b66db-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b66db-107">DESCRIPTION</span></span>
<span data-ttu-id="b66db-108">Das **Cmdlet Enable-AzBatchComputeNodeScheduling** ermöglicht die Aufgabenplanung für den angegebenen Computeknoten.</span><span class="sxs-lookup"><span data-stu-id="b66db-108">The **Enable-AzBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="b66db-109">Ein Computeknoten ist ein virtueller Azure-Computer, der einer bestimmten Anwendungsarbeitsauslastung gewidmet ist.</span><span class="sxs-lookup"><span data-stu-id="b66db-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="b66db-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b66db-110">EXAMPLES</span></span>

### <span data-ttu-id="b66db-111">Beispiel 1: Aktivieren der Aufgabenplanung auf einem Computeknoten</span><span class="sxs-lookup"><span data-stu-id="b66db-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="b66db-112">Diese Befehle ermöglichen die Aufgabenplanung auf dem Computeknoten tvm-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="b66db-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="b66db-113">Dazu erstellt der erste Befehl im Beispiel einen Objektverweis, der die Kontoschlüssel für das Batchkonto contosobatchaccount enthält.</span><span class="sxs-lookup"><span data-stu-id="b66db-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="b66db-114">Dieser Objektverweis wird in einer Variablen mit dem Namen $context.</span><span class="sxs-lookup"><span data-stu-id="b66db-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="b66db-115">Der zweite Befehl verwendet dann diesen Objektverweis und das **Cmdlet Enable-AzBatchComputeNodeScheduling,** um eine Verbindung mit dem Pool myPool herzustellen und die Aufgabenplanung in tvm-1783593343_34-2015117t222514z zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b66db-115">The second command then uses this object reference and the **Enable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="b66db-116">Beispiel 2: Aktivieren der Aufgabenplanung für Computeknoten in einem Pool</span><span class="sxs-lookup"><span data-stu-id="b66db-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="b66db-117">Diese Befehle ermöglichen die Aufgabenplanung für alle Im Pool06 gefundenen Computeknoten.</span><span class="sxs-lookup"><span data-stu-id="b66db-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="b66db-118">Um diese Aufgabe auszuführen, erstellt der erste Befehl im Beispiel einen Objektverweis, der die Kontoschlüssel für das Batchkonto contosobatchaccount enthält.</span><span class="sxs-lookup"><span data-stu-id="b66db-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="b66db-119">Dieser Objektverweis wird in einer Variablen mit dem Namen $context.</span><span class="sxs-lookup"><span data-stu-id="b66db-119">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="b66db-120">Der zweite Befehl im Beispiel verwendet dann diesen Objektverweis und **Get-AzBatchComputeNode,** um eine Sammlung aller in Pool06 gefundenen Computeknoten zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="b66db-120">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="b66db-121">Diese Sammlung wird dann an das **Cmdlet Enable-AzBatchComputeNodeScheduling** verschoben, das die Aufgabenplanung für jeden Computeknoten in der Auflistung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="b66db-121">That collection is then piped to the **Enable-AzBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="b66db-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b66db-122">PARAMETERS</span></span>

### <span data-ttu-id="b66db-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b66db-123">-BatchContext</span></span>
<span data-ttu-id="b66db-124">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b66db-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b66db-125">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="b66db-125">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b66db-126">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b66db-126">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b66db-127">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="b66db-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b66db-128">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="b66db-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b66db-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="b66db-129">-ComputeNode</span></span>
<span data-ttu-id="b66db-130">Gibt einen Objektbezug auf den Computeknoten an, auf dem die Aufgabenplanung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b66db-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="b66db-131">Dieser Objektverweis wird mithilfe des cmdlets Get-AzBatchComputeNode erstellt und das zurückgegebene Computeknotenobjekt in einer Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b66db-131">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="b66db-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b66db-132">-DefaultProfile</span></span>
<span data-ttu-id="b66db-133">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b66db-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b66db-134">-ID</span><span class="sxs-lookup"><span data-stu-id="b66db-134">-Id</span></span>
<span data-ttu-id="b66db-135">Gibt die ID des Computeknotens an, in dem die Aufgabenplanung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b66db-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="b66db-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="b66db-136">-PoolId</span></span>
<span data-ttu-id="b66db-137">Gibt die ID des Batchpools an, der den Computeknoten enthält, in dem die Aufgabenplanung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b66db-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="b66db-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b66db-138">CommonParameters</span></span>
<span data-ttu-id="b66db-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b66db-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b66db-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b66db-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b66db-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b66db-141">INPUTS</span></span>

### <span data-ttu-id="b66db-142">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="b66db-142">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="b66db-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b66db-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b66db-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b66db-144">OUTPUTS</span></span>

### <span data-ttu-id="b66db-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="b66db-145">System.Void</span></span>

## <span data-ttu-id="b66db-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b66db-146">NOTES</span></span>

## <span data-ttu-id="b66db-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b66db-147">RELATED LINKS</span></span>

[<span data-ttu-id="b66db-148">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="b66db-148">Disable-AzBatchComputeNodeScheduling</span></span>](./Disable-AzBatchComputeNodeScheduling.md)


