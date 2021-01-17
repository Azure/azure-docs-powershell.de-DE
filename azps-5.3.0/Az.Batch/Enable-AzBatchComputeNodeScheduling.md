---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9969388d51abb337030a8a732805ee1a15368ea7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471202"
---
# <span data-ttu-id="97c75-101">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="97c75-101">Enable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="97c75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97c75-102">SYNOPSIS</span></span>
<span data-ttu-id="97c75-103">Ermöglicht die Aufgabenplanung für den angegebenen Rechenknoten.</span><span class="sxs-lookup"><span data-stu-id="97c75-103">Enables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="97c75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97c75-104">SYNTAX</span></span>

### <span data-ttu-id="97c75-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="97c75-105">Id (Default)</span></span>
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97c75-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="97c75-106">InputObject</span></span>
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97c75-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97c75-107">DESCRIPTION</span></span>
<span data-ttu-id="97c75-108">Das **Cmdlet "Enable-AzBatchComputeNodeScheduling"** ermöglicht die Aufgabenplanung für den angegebenen Rechenknoten.</span><span class="sxs-lookup"><span data-stu-id="97c75-108">The **Enable-AzBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="97c75-109">Ein Rechenknoten ist ein virtueller Azure-Computer, der einer bestimmten Anwendungsarbeitsauslastung gewidmet ist.</span><span class="sxs-lookup"><span data-stu-id="97c75-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="97c75-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="97c75-110">EXAMPLES</span></span>

### <span data-ttu-id="97c75-111">Beispiel 1: Aktivieren der Aufgabenplanung für einen Rechenknoten</span><span class="sxs-lookup"><span data-stu-id="97c75-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="97c75-112">Diese Befehle ermöglichen die Aufgabenplanung auf dem berechneten Knoten "tvm-1783593343_34-20151117t222514z".</span><span class="sxs-lookup"><span data-stu-id="97c75-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="97c75-113">Dazu erstellt der erste Befehl im Beispiel einen Objektverweis, der die Kontoschlüssel für das Batchkonto "contosobatchaccount" enthält.</span><span class="sxs-lookup"><span data-stu-id="97c75-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="97c75-114">Dieser Objektverweis wird in einer Variablen namens "$context.</span><span class="sxs-lookup"><span data-stu-id="97c75-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="97c75-115">Der zweite Befehl verwendet dann diesen Objektverweis und das **Cmdlet "Enable-AzBatchComputeNodeScheduling",** um eine Verbindung mit dem Pool "myPool" herzustellen und die Aufgabenplanung auf tvm-1783593343_34-20151117t222514z zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="97c75-115">The second command then uses this object reference and the **Enable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="97c75-116">Beispiel 2: Aktivieren der Aufgabenplanung für Rechenknoten in einem Pool</span><span class="sxs-lookup"><span data-stu-id="97c75-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="97c75-117">Diese Befehle ermöglichen die Aufgabenplanung für alle Im Pool06 gefundenen Rechenknoten.</span><span class="sxs-lookup"><span data-stu-id="97c75-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="97c75-118">Zum Ausführen dieser Aufgabe erstellt der erste Befehl im Beispiel einen Objektverweis, der die Kontoschlüssel für das Batchkonto "contosobatchaccount" enthält.</span><span class="sxs-lookup"><span data-stu-id="97c75-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="97c75-119">Dieser Objektverweis wird in einer Variablen namens "$context.</span><span class="sxs-lookup"><span data-stu-id="97c75-119">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="97c75-120">Der zweite Befehl im Beispiel verwendet dann diesen Objektverweis und **"Get-AzBatchComputeNode",** um eine Sammlung aller In Pool06 gefundenen Berechnungsknoten zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="97c75-120">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="97c75-121">Diese Sammlung wird dann an das **Cmdlet "Enable-AzBatchComputeNodeScheduling"** weiterverteilt, das die Aufgabenplanung für jeden Rechenknoten in der Sammlung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="97c75-121">That collection is then piped to the **Enable-AzBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="97c75-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97c75-122">PARAMETERS</span></span>

### <span data-ttu-id="97c75-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="97c75-123">-BatchContext</span></span>
<span data-ttu-id="97c75-124">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="97c75-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="97c75-125">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="97c75-125">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="97c75-126">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="97c75-126">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="97c75-127">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="97c75-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="97c75-128">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="97c75-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="97c75-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="97c75-129">-ComputeNode</span></span>
<span data-ttu-id="97c75-130">Gibt einen Objektverweis auf den Rechenknoten an, für den die Aufgabenplanung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="97c75-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="97c75-131">Dieser Objektverweis wird mithilfe des cmdlets Get-AzBatchComputeNode erstellt und das zurückgegebene Rechenknotenobjekt in einer Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="97c75-131">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="97c75-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97c75-132">-DefaultProfile</span></span>
<span data-ttu-id="97c75-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97c75-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97c75-134">-ID</span><span class="sxs-lookup"><span data-stu-id="97c75-134">-Id</span></span>
<span data-ttu-id="97c75-135">Gibt die ID des Rechenknotens an, in dem die Aufgabenplanung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="97c75-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="97c75-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="97c75-136">-PoolId</span></span>
<span data-ttu-id="97c75-137">Gibt die ID des Batchpools an, der den Rechenknoten enthält, für den die Aufgabenplanung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="97c75-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="97c75-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97c75-138">CommonParameters</span></span>
<span data-ttu-id="97c75-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97c75-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97c75-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97c75-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97c75-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="97c75-141">INPUTS</span></span>

### <span data-ttu-id="97c75-142">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="97c75-142">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="97c75-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="97c75-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="97c75-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="97c75-144">OUTPUTS</span></span>

### <span data-ttu-id="97c75-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="97c75-145">System.Void</span></span>

## <span data-ttu-id="97c75-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="97c75-146">NOTES</span></span>

## <span data-ttu-id="97c75-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="97c75-147">RELATED LINKS</span></span>

[<span data-ttu-id="97c75-148">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="97c75-148">Disable-AzBatchComputeNodeScheduling</span></span>](./Disable-AzBatchComputeNodeScheduling.md)


