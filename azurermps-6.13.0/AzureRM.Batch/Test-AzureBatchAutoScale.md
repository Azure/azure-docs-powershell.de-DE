---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/test-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
ms.openlocfilehash: 3dc458c5b23e3bd6f8bde39e02152e8c2b76f6f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500269"
---
# <span data-ttu-id="801a1-101">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="801a1-101">Test-AzureBatchAutoScale</span></span>

## <span data-ttu-id="801a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="801a1-102">SYNOPSIS</span></span>
<span data-ttu-id="801a1-103">Ruft das Ergebnis einer automatischen Skalierungs Formel in einem Pool ab.</span><span class="sxs-lookup"><span data-stu-id="801a1-103">Gets the result of an automatic scaling formula on a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="801a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="801a1-104">SYNTAX</span></span>

```
Test-AzureBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="801a1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="801a1-105">DESCRIPTION</span></span>
<span data-ttu-id="801a1-106">Das Cmdlet " **Test-AzureBatchAutoScale** " Ruft das Ergebnis einer automatischen Skalierungs Formel für den angegebenen Pool ab.</span><span class="sxs-lookup"><span data-stu-id="801a1-106">The **Test-AzureBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="801a1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="801a1-107">EXAMPLES</span></span>

### <span data-ttu-id="801a1-108">Beispiel 1: Auswerten einer AutoScale-Formel in einem Pool</span><span class="sxs-lookup"><span data-stu-id="801a1-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzureBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="801a1-109">Der erste Befehl speichert eine Formel in der $Formula Variablen für die Verwendung im Beispiel.</span><span class="sxs-lookup"><span data-stu-id="801a1-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>
<span data-ttu-id="801a1-110">Der zweite Befehl wertet die AutoScale-Formel im Pool mit der ID ContosoPool aus.</span><span class="sxs-lookup"><span data-stu-id="801a1-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>
<span data-ttu-id="801a1-111">Der endgültige Befehl zeigt die **Ergebnisse** mithilfe der standardmäßigen Punktsyntax an.</span><span class="sxs-lookup"><span data-stu-id="801a1-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="801a1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="801a1-112">PARAMETERS</span></span>

### <span data-ttu-id="801a1-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="801a1-113">-AutoScaleFormula</span></span>
<span data-ttu-id="801a1-114">Gibt die Formel für die gewünschte Anzahl von Compute-Knoten im Pool an.</span><span class="sxs-lookup"><span data-stu-id="801a1-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="801a1-115">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="801a1-115">-BatchContext</span></span>
<span data-ttu-id="801a1-116">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="801a1-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="801a1-117">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="801a1-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="801a1-118">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="801a1-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="801a1-119">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="801a1-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="801a1-120">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="801a1-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="801a1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="801a1-121">-DefaultProfile</span></span>
<span data-ttu-id="801a1-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="801a1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="801a1-123">-ID</span><span class="sxs-lookup"><span data-stu-id="801a1-123">-Id</span></span>
<span data-ttu-id="801a1-124">Gibt die Objekt-ID des Pools an, für den die automatische Skalierung getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="801a1-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="801a1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="801a1-125">CommonParameters</span></span>
<span data-ttu-id="801a1-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="801a1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="801a1-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="801a1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="801a1-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="801a1-128">INPUTS</span></span>

### <span data-ttu-id="801a1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="801a1-129">System.String</span></span>

### <span data-ttu-id="801a1-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="801a1-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="801a1-131">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="801a1-131">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="801a1-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="801a1-132">OUTPUTS</span></span>

### <span data-ttu-id="801a1-133">Microsoft.Azure.Commands.Batch. Models. PSAutoScaleRun</span><span class="sxs-lookup"><span data-stu-id="801a1-133">Microsoft.Azure.Commands.Batch.Models.PSAutoScaleRun</span></span>

## <span data-ttu-id="801a1-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="801a1-134">NOTES</span></span>

## <span data-ttu-id="801a1-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="801a1-135">RELATED LINKS</span></span>

[<span data-ttu-id="801a1-136">Deaktivieren-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="801a1-136">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="801a1-137">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="801a1-137">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="801a1-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="801a1-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="801a1-139">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="801a1-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


