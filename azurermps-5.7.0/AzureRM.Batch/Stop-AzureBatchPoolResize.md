---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
ms.openlocfilehash: 153e566df3e2ab6f758d139719af1e812e0476ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478713"
---
# <span data-ttu-id="62c62-101">Stop-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="62c62-101">Stop-AzureBatchPoolResize</span></span>

## <span data-ttu-id="62c62-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="62c62-102">SYNOPSIS</span></span>
<span data-ttu-id="62c62-103">Beendet die Größe eines Pool-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="62c62-103">Stops a pool resize operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62c62-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="62c62-104">SYNTAX</span></span>

```
Stop-AzureBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62c62-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62c62-105">DESCRIPTION</span></span>
<span data-ttu-id="62c62-106">Das Cmdlet **Stop-AzureBatchPoolResize** beendet eine Azure Batch-Größenänderung in einem Pool.</span><span class="sxs-lookup"><span data-stu-id="62c62-106">The **Stop-AzureBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="62c62-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="62c62-107">EXAMPLES</span></span>

### <span data-ttu-id="62c62-108">Beispiel 1: Beenden der Größenänderung eines Pools</span><span class="sxs-lookup"><span data-stu-id="62c62-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzureBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="62c62-109">Dieser Befehl beendet einen Größen Änderungsvorgang für den Pool mit der ID ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="62c62-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="62c62-110">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="62c62-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="62c62-111">Beispiel 2: Beenden der Größenänderung eines Pools mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="62c62-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzureBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="62c62-112">Mit diesem Befehl wird die Größe eines Pools mithilfe des Pipelineoperators beendet.</span><span class="sxs-lookup"><span data-stu-id="62c62-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="62c62-113">Der Befehl ruft den Pool mit der ID-ContosoPool06 mithilfe des Get-AzureBatchPool-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="62c62-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="62c62-114">Der Befehl übergibt das Pool-Objekt an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62c62-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="62c62-115">Der Befehl beendet den Größen Änderungsvorgang für diesen Pool.</span><span class="sxs-lookup"><span data-stu-id="62c62-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="62c62-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="62c62-116">PARAMETERS</span></span>

### <span data-ttu-id="62c62-117">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="62c62-117">-BatchContext</span></span>
<span data-ttu-id="62c62-118">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="62c62-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="62c62-119">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="62c62-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="62c62-120">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="62c62-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="62c62-121">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="62c62-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="62c62-122">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="62c62-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="62c62-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c62-123">-DefaultProfile</span></span>
<span data-ttu-id="62c62-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="62c62-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62c62-125">-ID</span><span class="sxs-lookup"><span data-stu-id="62c62-125">-Id</span></span>
<span data-ttu-id="62c62-126">Gibt die ID des Pools an, für den das Cmdlet einen Größen Änderungsvorgang beendet.</span><span class="sxs-lookup"><span data-stu-id="62c62-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62c62-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c62-127">CommonParameters</span></span>
<span data-ttu-id="62c62-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62c62-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c62-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62c62-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c62-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="62c62-130">INPUTS</span></span>

### <span data-ttu-id="62c62-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="62c62-131">BatchAccountContext</span></span>
<span data-ttu-id="62c62-132">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="62c62-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="62c62-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="62c62-133">String</span></span>
<span data-ttu-id="62c62-134">Der Parameter "ID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="62c62-134">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="62c62-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="62c62-135">OUTPUTS</span></span>

## <span data-ttu-id="62c62-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="62c62-136">NOTES</span></span>

## <span data-ttu-id="62c62-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="62c62-137">RELATED LINKS</span></span>

[<span data-ttu-id="62c62-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="62c62-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="62c62-139">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="62c62-139">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="62c62-140">Anfang-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="62c62-140">Start-AzureBatchPoolResize</span></span>](./Start-AzureBatchPoolResize.md)

[<span data-ttu-id="62c62-141">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="62c62-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


