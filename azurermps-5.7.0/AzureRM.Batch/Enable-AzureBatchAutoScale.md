---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
ms.openlocfilehash: 73c1efe9e25fa02dc06f367eae1d010562eba56e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505790"
---
# <span data-ttu-id="5d4c2-101">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="5d4c2-101">Enable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="5d4c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d4c2-102">SYNOPSIS</span></span>
<span data-ttu-id="5d4c2-103">Aktiviert die automatische Skalierung eines Pools.</span><span class="sxs-lookup"><span data-stu-id="5d4c2-103">Enables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d4c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d4c2-104">SYNTAX</span></span>

```
Enable-AzureBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d4c2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d4c2-105">DESCRIPTION</span></span>
<span data-ttu-id="5d4c2-106">Das Cmdlet **enable-AzureBatchAutoScale** ermöglicht die automatische Skalierung des angegebenen Pools.</span><span class="sxs-lookup"><span data-stu-id="5d4c2-106">The **Enable-AzureBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="5d4c2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d4c2-107">EXAMPLES</span></span>

### <span data-ttu-id="5d4c2-108">Beispiel 1: Aktivieren der automatischen Skalierung für einen Pool</span><span class="sxs-lookup"><span data-stu-id="5d4c2-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzureBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="5d4c2-109">Der erste Befehl definiert eine Formel und speichert Sie dann in der $Formula Variablen.</span><span class="sxs-lookup"><span data-stu-id="5d4c2-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>

<span data-ttu-id="5d4c2-110">Mit dem zweiten Befehl wird die automatische Skalierung im Pool mit dem Namen MyPool mithilfe der Formel in $Formula aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5d4c2-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="5d4c2-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d4c2-111">PARAMETERS</span></span>

### <span data-ttu-id="5d4c2-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="5d4c2-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="5d4c2-113">Gibt die Zeitspanne (in Minuten) an, die verstreicht, bevor die Poolgröße automatisch entsprechend der AutoSkalieren-Formel angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="5d4c2-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="5d4c2-114">Der Standardwert ist 15 Minuten und der Mindestwert 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="5d4c2-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4c2-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="5d4c2-115">-AutoScaleFormula</span></span>
<span data-ttu-id="5d4c2-116">Gibt die Formel für die gewünschte Anzahl von Compute-Knoten im Pool an.</span><span class="sxs-lookup"><span data-stu-id="5d4c2-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4c2-117">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="5d4c2-117">-BatchContext</span></span>
<span data-ttu-id="5d4c2-118">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="5d4c2-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5d4c2-119">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5d4c2-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5d4c2-120">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5d4c2-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5d4c2-121">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="5d4c2-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5d4c2-122">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="5d4c2-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5d4c2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d4c2-123">-DefaultProfile</span></span>
<span data-ttu-id="5d4c2-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5d4c2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d4c2-125">-ID</span><span class="sxs-lookup"><span data-stu-id="5d4c2-125">-Id</span></span>
<span data-ttu-id="5d4c2-126">Gibt die Objekt-ID des Pools an, für den die automatische Skalierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d4c2-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="5d4c2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d4c2-127">CommonParameters</span></span>
<span data-ttu-id="5d4c2-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d4c2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d4c2-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d4c2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d4c2-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d4c2-130">INPUTS</span></span>

### <span data-ttu-id="5d4c2-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5d4c2-131">BatchAccountContext</span></span>
<span data-ttu-id="5d4c2-132">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5d4c2-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="5d4c2-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5d4c2-133">String</span></span>
<span data-ttu-id="5d4c2-134">Der Parameter "ID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5d4c2-134">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5d4c2-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d4c2-135">OUTPUTS</span></span>

## <span data-ttu-id="5d4c2-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d4c2-136">NOTES</span></span>

## <span data-ttu-id="5d4c2-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d4c2-137">RELATED LINKS</span></span>

[<span data-ttu-id="5d4c2-138">Deaktivieren-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="5d4c2-138">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="5d4c2-139">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="5d4c2-139">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="5d4c2-140">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="5d4c2-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


