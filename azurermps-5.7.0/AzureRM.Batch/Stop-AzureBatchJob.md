---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
ms.openlocfilehash: 0f33807c112ea770e3d02d972d52ca7a166bb791
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478718"
---
# <span data-ttu-id="e0dc5-101">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e0dc5-101">Stop-AzureBatchJob</span></span>

## <span data-ttu-id="e0dc5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e0dc5-102">SYNOPSIS</span></span>
<span data-ttu-id="e0dc5-103">Beendet eine Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-103">Stops a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0dc5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0dc5-104">SYNTAX</span></span>

```
Stop-AzureBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0dc5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0dc5-105">DESCRIPTION</span></span>
<span data-ttu-id="e0dc5-106">Das Cmdlet **Stop-AzureBatchJob** beendet eine Azure-Batch Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-106">The **Stop-AzureBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="e0dc5-107">Mit diesem Befehl wird der Auftrag als erledigt markiert.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="e0dc5-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e0dc5-108">EXAMPLES</span></span>

### <span data-ttu-id="e0dc5-109">Beispiel 1: Beenden einer Stapelverarbeitung</span><span class="sxs-lookup"><span data-stu-id="e0dc5-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzureBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="e0dc5-110">Dieser Befehl beendet den Auftrag mit der ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="e0dc5-111">Der Befehl gibt einen Grund an, den Sie zum Beenden des Auftrags ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="e0dc5-112">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="e0dc5-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0dc5-113">PARAMETERS</span></span>

### <span data-ttu-id="e0dc5-114">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="e0dc5-114">-BatchContext</span></span>
<span data-ttu-id="e0dc5-115">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e0dc5-116">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e0dc5-117">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e0dc5-118">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e0dc5-119">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e0dc5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0dc5-120">-DefaultProfile</span></span>
<span data-ttu-id="e0dc5-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0dc5-122">-ID</span><span class="sxs-lookup"><span data-stu-id="e0dc5-122">-Id</span></span>
<span data-ttu-id="e0dc5-123">Gibt die ID des Auftrags an, der vom Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="e0dc5-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="e0dc5-124">-TerminateReason</span></span>
<span data-ttu-id="e0dc5-125">Gibt den Grund an, zu dem Sie den Auftrag beendet haben.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="e0dc5-126">Dieses Cmdlet speichert diesen Text als **TerminateReason** -Eigenschaft des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

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

### <span data-ttu-id="e0dc5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0dc5-127">CommonParameters</span></span>
<span data-ttu-id="e0dc5-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0dc5-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0dc5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0dc5-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e0dc5-130">INPUTS</span></span>

### <span data-ttu-id="e0dc5-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e0dc5-131">BatchAccountContext</span></span>
<span data-ttu-id="e0dc5-132">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="e0dc5-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e0dc5-133">String</span></span>
<span data-ttu-id="e0dc5-134">Der Parameter "ID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-134">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="e0dc5-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e0dc5-135">OUTPUTS</span></span>

## <span data-ttu-id="e0dc5-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="e0dc5-136">NOTES</span></span>

## <span data-ttu-id="e0dc5-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e0dc5-137">RELATED LINKS</span></span>

[<span data-ttu-id="e0dc5-138">Deaktivieren-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e0dc5-138">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="e0dc5-139">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e0dc5-139">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="e0dc5-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e0dc5-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="e0dc5-141">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e0dc5-141">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="e0dc5-142">Neu – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e0dc5-142">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="e0dc5-143">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e0dc5-143">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="e0dc5-144">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e0dc5-144">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


