---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/test-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
ms.openlocfilehash: 6732fb89775cea289bf82a5675a482f94b7f95ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303197"
---
# <span data-ttu-id="c32d6-101">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="c32d6-101">Test-AzBatchAutoScale</span></span>

## <span data-ttu-id="c32d6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c32d6-102">SYNOPSIS</span></span>
<span data-ttu-id="c32d6-103">Ruft das Ergebnis einer automatischen Skalierungs Formel in einem Pool ab.</span><span class="sxs-lookup"><span data-stu-id="c32d6-103">Gets the result of an automatic scaling formula on a pool.</span></span>

## <span data-ttu-id="c32d6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c32d6-104">SYNTAX</span></span>

```
Test-AzBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c32d6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c32d6-105">DESCRIPTION</span></span>
<span data-ttu-id="c32d6-106">Das Cmdlet " **Test-AzBatchAutoScale** " Ruft das Ergebnis einer automatischen Skalierungs Formel für den angegebenen Pool ab.</span><span class="sxs-lookup"><span data-stu-id="c32d6-106">The **Test-AzBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="c32d6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c32d6-107">EXAMPLES</span></span>

### <span data-ttu-id="c32d6-108">Beispiel 1: Auswerten einer AutoScale-Formel in einem Pool</span><span class="sxs-lookup"><span data-stu-id="c32d6-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="c32d6-109">Der erste Befehl speichert eine Formel in der $Formula Variablen für die Verwendung im Beispiel.</span><span class="sxs-lookup"><span data-stu-id="c32d6-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>
<span data-ttu-id="c32d6-110">Der zweite Befehl wertet die AutoScale-Formel im Pool mit der ID ContosoPool aus.</span><span class="sxs-lookup"><span data-stu-id="c32d6-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>
<span data-ttu-id="c32d6-111">Der endgültige Befehl zeigt die **Ergebnisse** mithilfe der standardmäßigen Punktsyntax an.</span><span class="sxs-lookup"><span data-stu-id="c32d6-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="c32d6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c32d6-112">PARAMETERS</span></span>

### <span data-ttu-id="c32d6-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="c32d6-113">-AutoScaleFormula</span></span>
<span data-ttu-id="c32d6-114">Gibt die Formel für die gewünschte Anzahl von Compute-Knoten im Pool an.</span><span class="sxs-lookup"><span data-stu-id="c32d6-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="c32d6-115">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="c32d6-115">-BatchContext</span></span>
<span data-ttu-id="c32d6-116">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="c32d6-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c32d6-117">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c32d6-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c32d6-118">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c32d6-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c32d6-119">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="c32d6-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c32d6-120">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="c32d6-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c32d6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c32d6-121">-DefaultProfile</span></span>
<span data-ttu-id="c32d6-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c32d6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c32d6-123">-ID</span><span class="sxs-lookup"><span data-stu-id="c32d6-123">-Id</span></span>
<span data-ttu-id="c32d6-124">Gibt die Objekt-ID des Pools an, für den die automatische Skalierung getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c32d6-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="c32d6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c32d6-125">CommonParameters</span></span>
<span data-ttu-id="c32d6-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c32d6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c32d6-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c32d6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c32d6-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c32d6-128">INPUTS</span></span>

### <span data-ttu-id="c32d6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c32d6-129">System.String</span></span>

### <span data-ttu-id="c32d6-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c32d6-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c32d6-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c32d6-131">OUTPUTS</span></span>

### <span data-ttu-id="c32d6-132">Microsoft.Azure.Commands.Batch. Models. PSAutoScaleRun</span><span class="sxs-lookup"><span data-stu-id="c32d6-132">Microsoft.Azure.Commands.Batch.Models.PSAutoScaleRun</span></span>

## <span data-ttu-id="c32d6-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="c32d6-133">NOTES</span></span>

## <span data-ttu-id="c32d6-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c32d6-134">RELATED LINKS</span></span>

[<span data-ttu-id="c32d6-135">Deaktivieren-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="c32d6-135">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="c32d6-136">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="c32d6-136">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="c32d6-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c32d6-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c32d6-138">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="c32d6-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
