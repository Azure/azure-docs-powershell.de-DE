---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 229877db7a3077a4b1951a06914c842e63384ba6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473273"
---
# <span data-ttu-id="4787b-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="4787b-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="4787b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4787b-102">SYNOPSIS</span></span>
<span data-ttu-id="4787b-103">Beendet den Größenänderungsvorgang eines Pools.</span><span class="sxs-lookup"><span data-stu-id="4787b-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="4787b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4787b-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4787b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4787b-105">DESCRIPTION</span></span>
<span data-ttu-id="4787b-106">Das **Cmdlet "Stop-AzBatchPoolResize"** beendet einen Azure Batch-Größenänderungsvorgang für einen Pool.</span><span class="sxs-lookup"><span data-stu-id="4787b-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="4787b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4787b-107">EXAMPLES</span></span>

### <span data-ttu-id="4787b-108">Beispiel 1: Beenden der Größenänderung eines Pools</span><span class="sxs-lookup"><span data-stu-id="4787b-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="4787b-109">Dieser Befehl beendet einen Größenänderungsvorgang für den Pool mit der ID ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="4787b-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="4787b-110">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der Variablen $Context Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="4787b-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="4787b-111">Beispiel 2: Beenden der Größenänderung eines Pools mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="4787b-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="4787b-112">Mit diesem Befehl wird die Größenänderung eines Pool mithilfe des Pipelineoperators beendet.</span><span class="sxs-lookup"><span data-stu-id="4787b-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="4787b-113">Der Befehl ruft den Pool mit der ID ContosoPool06 mithilfe des cmdlets Get-AzBatchPool ab.</span><span class="sxs-lookup"><span data-stu-id="4787b-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="4787b-114">Der Befehl übergibt dieses Poolobjekt an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4787b-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="4787b-115">Der Befehl beendet den Größenänderungsvorgang für diesen Pool.</span><span class="sxs-lookup"><span data-stu-id="4787b-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="4787b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4787b-116">PARAMETERS</span></span>

### <span data-ttu-id="4787b-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4787b-117">-BatchContext</span></span>
<span data-ttu-id="4787b-118">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4787b-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4787b-119">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="4787b-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4787b-120">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4787b-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4787b-121">Bei verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="4787b-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4787b-122">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4787b-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4787b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4787b-123">-DefaultProfile</span></span>
<span data-ttu-id="4787b-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4787b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4787b-125">-ID</span><span class="sxs-lookup"><span data-stu-id="4787b-125">-Id</span></span>
<span data-ttu-id="4787b-126">Gibt die ID des Pools an, für den dieses Cmdlet einen Größenänderungsvorgang beendet.</span><span class="sxs-lookup"><span data-stu-id="4787b-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="4787b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4787b-127">CommonParameters</span></span>
<span data-ttu-id="4787b-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4787b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4787b-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4787b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4787b-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4787b-130">INPUTS</span></span>

### <span data-ttu-id="4787b-131">System.String</span><span class="sxs-lookup"><span data-stu-id="4787b-131">System.String</span></span>

### <span data-ttu-id="4787b-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4787b-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4787b-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4787b-133">OUTPUTS</span></span>

### <span data-ttu-id="4787b-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="4787b-134">System.Void</span></span>

## <span data-ttu-id="4787b-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4787b-135">NOTES</span></span>

## <span data-ttu-id="4787b-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4787b-136">RELATED LINKS</span></span>

[<span data-ttu-id="4787b-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4787b-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4787b-138">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="4787b-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="4787b-139">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="4787b-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="4787b-140">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="4787b-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
