---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
ms.openlocfilehash: f67660cdc64c814d04ec4a987b711c802ca222d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498397"
---
# <span data-ttu-id="1ced9-101">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1ced9-101">Stop-AzureBatchJob</span></span>

## <span data-ttu-id="1ced9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1ced9-102">SYNOPSIS</span></span>
<span data-ttu-id="1ced9-103">Beendet eine Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="1ced9-103">Stops a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ced9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ced9-104">SYNTAX</span></span>

```
Stop-AzureBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ced9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ced9-105">DESCRIPTION</span></span>
<span data-ttu-id="1ced9-106">Das Cmdlet **Stop-AzureBatchJob** beendet eine Azure-Batch Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="1ced9-106">The **Stop-AzureBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="1ced9-107">Mit diesem Befehl wird der Auftrag als erledigt markiert.</span><span class="sxs-lookup"><span data-stu-id="1ced9-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="1ced9-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ced9-108">EXAMPLES</span></span>

### <span data-ttu-id="1ced9-109">Beispiel 1: Beenden einer Stapelverarbeitung</span><span class="sxs-lookup"><span data-stu-id="1ced9-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzureBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="1ced9-110">Dieser Befehl beendet den Auftrag mit der ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="1ced9-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="1ced9-111">Der Befehl gibt einen Grund an, den Sie zum Beenden des Auftrags ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="1ced9-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="1ced9-112">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="1ced9-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="1ced9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ced9-113">PARAMETERS</span></span>

### <span data-ttu-id="1ced9-114">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="1ced9-114">-BatchContext</span></span>
<span data-ttu-id="1ced9-115">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ced9-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1ced9-116">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ced9-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1ced9-117">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1ced9-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1ced9-118">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ced9-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1ced9-119">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="1ced9-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1ced9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ced9-120">-DefaultProfile</span></span>
<span data-ttu-id="1ced9-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1ced9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ced9-122">-ID</span><span class="sxs-lookup"><span data-stu-id="1ced9-122">-Id</span></span>
<span data-ttu-id="1ced9-123">Gibt die ID des Auftrags an, der vom Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="1ced9-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="1ced9-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="1ced9-124">-TerminateReason</span></span>
<span data-ttu-id="1ced9-125">Gibt den Grund an, zu dem Sie den Auftrag beendet haben.</span><span class="sxs-lookup"><span data-stu-id="1ced9-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="1ced9-126">Dieses Cmdlet speichert diesen Text als **TerminateReason** -Eigenschaft des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="1ced9-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ced9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ced9-127">CommonParameters</span></span>
<span data-ttu-id="1ced9-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ced9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ced9-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ced9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ced9-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1ced9-130">INPUTS</span></span>

### <span data-ttu-id="1ced9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1ced9-131">System.String</span></span>

### <span data-ttu-id="1ced9-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1ced9-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="1ced9-133">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1ced9-133">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="1ced9-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1ced9-134">OUTPUTS</span></span>

### <span data-ttu-id="1ced9-135">System. void</span><span class="sxs-lookup"><span data-stu-id="1ced9-135">System.Void</span></span>

## <span data-ttu-id="1ced9-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="1ced9-136">NOTES</span></span>

## <span data-ttu-id="1ced9-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1ced9-137">RELATED LINKS</span></span>

[<span data-ttu-id="1ced9-138">Deaktivieren-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1ced9-138">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="1ced9-139">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1ced9-139">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="1ced9-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="1ced9-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="1ced9-141">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1ced9-141">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="1ced9-142">Neu – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1ced9-142">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="1ced9-143">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1ced9-143">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="1ced9-144">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="1ced9-144">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


