---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 229877db7a3077a4b1951a06914c842e63384ba6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177126"
---
# <span data-ttu-id="cf5d8-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="cf5d8-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="cf5d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cf5d8-102">SYNOPSIS</span></span>
<span data-ttu-id="cf5d8-103">Beendet die Größe eines Pool-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="cf5d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf5d8-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf5d8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf5d8-105">DESCRIPTION</span></span>
<span data-ttu-id="cf5d8-106">Das Cmdlet **Stop-AzBatchPoolResize** beendet eine Azure Batch-Größenänderung in einem Pool.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="cf5d8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf5d8-107">EXAMPLES</span></span>

### <span data-ttu-id="cf5d8-108">Beispiel 1: Beenden der Größenänderung eines Pools</span><span class="sxs-lookup"><span data-stu-id="cf5d8-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="cf5d8-109">Dieser Befehl beendet einen Größen Änderungsvorgang für den Pool mit der ID ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="cf5d8-110">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="cf5d8-111">Beispiel 2: Beenden der Größenänderung eines Pools mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="cf5d8-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="cf5d8-112">Mit diesem Befehl wird die Größe eines Pools mithilfe des Pipelineoperators beendet.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="cf5d8-113">Der Befehl ruft den Pool mit der ID-ContosoPool06 mithilfe des Get-AzBatchPool-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="cf5d8-114">Der Befehl übergibt das Pool-Objekt an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="cf5d8-115">Der Befehl beendet den Größen Änderungsvorgang für diesen Pool.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="cf5d8-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf5d8-116">PARAMETERS</span></span>

### <span data-ttu-id="cf5d8-117">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="cf5d8-117">-BatchContext</span></span>
<span data-ttu-id="cf5d8-118">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cf5d8-119">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cf5d8-120">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cf5d8-121">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cf5d8-122">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cf5d8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf5d8-123">-DefaultProfile</span></span>
<span data-ttu-id="cf5d8-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf5d8-125">-ID</span><span class="sxs-lookup"><span data-stu-id="cf5d8-125">-Id</span></span>
<span data-ttu-id="cf5d8-126">Gibt die ID des Pools an, für den das Cmdlet einen Größen Änderungsvorgang beendet.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf5d8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf5d8-127">CommonParameters</span></span>
<span data-ttu-id="cf5d8-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf5d8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf5d8-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf5d8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf5d8-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cf5d8-130">INPUTS</span></span>

### <span data-ttu-id="cf5d8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="cf5d8-131">System.String</span></span>

### <span data-ttu-id="cf5d8-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cf5d8-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cf5d8-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cf5d8-133">OUTPUTS</span></span>

### <span data-ttu-id="cf5d8-134">System. void</span><span class="sxs-lookup"><span data-stu-id="cf5d8-134">System.Void</span></span>

## <span data-ttu-id="cf5d8-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="cf5d8-135">NOTES</span></span>

## <span data-ttu-id="cf5d8-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cf5d8-136">RELATED LINKS</span></span>

[<span data-ttu-id="cf5d8-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="cf5d8-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="cf5d8-138">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="cf5d8-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="cf5d8-139">Anfang-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="cf5d8-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="cf5d8-140">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cf5d8-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
