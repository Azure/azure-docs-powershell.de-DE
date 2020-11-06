---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 7cf3a056ec4266cccac577920f2f5b9292ce03be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502634"
---
# <span data-ttu-id="bb855-101">Enable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="bb855-101">Enable-AzureBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="bb855-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bb855-102">SYNOPSIS</span></span>
<span data-ttu-id="bb855-103">Aktiviert die Aufgabenplanung auf dem angegebenen Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="bb855-103">Enables task scheduling on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb855-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb855-104">SYNTAX</span></span>

### <span data-ttu-id="bb855-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="bb855-105">Id (Default)</span></span>
```
Enable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb855-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="bb855-106">InputObject</span></span>
```
Enable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb855-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb855-107">DESCRIPTION</span></span>
<span data-ttu-id="bb855-108">Das Cmdlet **enable-AzureBatchComputeNodeScheduling** ermöglicht die Aufgabenplanung auf dem angegebenen Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="bb855-108">The **Enable-AzureBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="bb855-109">Ein Compute-Knoten ist ein Azure Virtual Machine, der einer bestimmten Anwendungsauslastung gewidmet ist.</span><span class="sxs-lookup"><span data-stu-id="bb855-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="bb855-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bb855-110">EXAMPLES</span></span>

### <span data-ttu-id="bb855-111">Beispiel 1: Aktivieren der Vorgangsplanung auf einem Compute-Knoten</span><span class="sxs-lookup"><span data-stu-id="bb855-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzureBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="bb855-112">Diese Befehle ermöglichen die Aufgabenplanung auf dem Compute-Knoten TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="bb855-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="bb855-113">Dazu wird mit dem ersten Befehl im Beispiel ein Objektverweis erstellt, der die Kontoschlüssel für das Stapelverarbeitungs Konto contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="bb855-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="bb855-114">Dieser Objektverweis wird in einer Variablen mit dem Namen $Context gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bb855-114">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="bb855-115">Der zweite Befehl verwendet dann diesen Objektverweis und das Cmdlet **enable-AzureBatchComputeNodeScheduling** , um eine Verbindung mit dem Pool MyPool herzustellen und die Aufgabenplanung auf TVM-1783593343_34-20151117t222514z zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="bb855-115">The second command then uses this object reference and the **Enable-AzureBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="bb855-116">Beispiel 2: Aktivieren der Vorgangsplanung für Compute-Knoten in einem Pool</span><span class="sxs-lookup"><span data-stu-id="bb855-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzureBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="bb855-117">Mit diesen Befehlen können Sie die Aufgabenplanung für alle Compute-Knoten in der Pool-Pool06.</span><span class="sxs-lookup"><span data-stu-id="bb855-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="bb855-118">Zum Ausführen dieser Aufgabe wird mit dem ersten Befehl im Beispiel ein Objektverweis erstellt, der die Kontoschlüssel für das Stapelverarbeitungs Konto contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="bb855-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="bb855-119">Dieser Objektverweis wird in einer Variablen mit dem Namen $Context gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bb855-119">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="bb855-120">Der zweite Befehl im Beispiel verwendet dann diesen Objektverweis und **Get-AzureBatchComputeNode** , um eine Auflistung aller in Pool06 gefundenen Compute-Knoten zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="bb855-120">The second command in the example then uses this object reference and **Get-AzureBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="bb855-121">Diese Sammlung wird dann an das Cmdlet **enable-AzureBatchComputeNodeScheduling** weitergeleitet, das die Aufgabenplanung für jeden Compute-Knoten in der Sammlung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="bb855-121">That collection is then piped to the **Enable-AzureBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="bb855-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb855-122">PARAMETERS</span></span>

### <span data-ttu-id="bb855-123">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="bb855-123">-BatchContext</span></span>
<span data-ttu-id="bb855-124">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="bb855-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bb855-125">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="bb855-125">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bb855-126">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bb855-126">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bb855-127">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="bb855-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bb855-128">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="bb855-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb855-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="bb855-129">-ComputeNode</span></span>
<span data-ttu-id="bb855-130">Gibt einen Objektverweis auf den Compute-Knoten an, in dem die Aufgabenplanung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="bb855-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="bb855-131">Dieser Objektverweis wird mithilfe des Get-AzureBatchComputeNode-Cmdlets erstellt und speichert das zurückgegebene Compute-Knotenobjekt in einer Variablen.</span><span class="sxs-lookup"><span data-stu-id="bb855-131">This object reference is created by using the Get-AzureBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb855-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb855-132">-DefaultProfile</span></span>
<span data-ttu-id="bb855-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bb855-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb855-134">-ID</span><span class="sxs-lookup"><span data-stu-id="bb855-134">-Id</span></span>
<span data-ttu-id="bb855-135">Gibt die ID des Compute-Knotens an, in dem die Vorgangsplanung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="bb855-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb855-136">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="bb855-136">-PoolId</span></span>
<span data-ttu-id="bb855-137">Gibt die ID des Batch Pools an, der den Compute-Knoten enthält, in dem die Vorgangsplanung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="bb855-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb855-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb855-138">CommonParameters</span></span>
<span data-ttu-id="bb855-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb855-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb855-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb855-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb855-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bb855-141">INPUTS</span></span>

### <span data-ttu-id="bb855-142">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bb855-142">BatchAccountContext</span></span>
<span data-ttu-id="bb855-143">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="bb855-143">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="bb855-144">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="bb855-144">PSComputeNode</span></span>
<span data-ttu-id="bb855-145">Der Parameter "ComputeNode" akzeptiert den Wert vom Typ "PSComputeNode" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="bb855-145">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="bb855-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bb855-146">OUTPUTS</span></span>

## <span data-ttu-id="bb855-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="bb855-147">NOTES</span></span>

## <span data-ttu-id="bb855-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bb855-148">RELATED LINKS</span></span>

[<span data-ttu-id="bb855-149">Deaktivieren-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="bb855-149">Disable-AzureBatchComputeNodeScheduling</span></span>](./Disable-AzureBatchComputeNodeScheduling.md)


