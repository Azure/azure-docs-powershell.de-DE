---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
ms.openlocfilehash: 8893ed4002e576e257cd9b885d5773c5851edde0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500105"
---
# <span data-ttu-id="ba1de-101">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ba1de-101">Stop-AzureBatchJob</span></span>

## <span data-ttu-id="ba1de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba1de-102">SYNOPSIS</span></span>
<span data-ttu-id="ba1de-103">Beendet eine Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="ba1de-103">Stops a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba1de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba1de-104">SYNTAX</span></span>

```
Stop-AzureBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba1de-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba1de-105">DESCRIPTION</span></span>
<span data-ttu-id="ba1de-106">Das Cmdlet **Stop-AzureBatchJob** beendet eine Azure-Batch Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="ba1de-106">The **Stop-AzureBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="ba1de-107">Mit diesem Befehl wird der Auftrag als erledigt markiert.</span><span class="sxs-lookup"><span data-stu-id="ba1de-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="ba1de-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba1de-108">EXAMPLES</span></span>

### <span data-ttu-id="ba1de-109">Beispiel 1: Beenden einer Stapelverarbeitung</span><span class="sxs-lookup"><span data-stu-id="ba1de-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzureBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="ba1de-110">Dieser Befehl beendet den Auftrag mit der ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="ba1de-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="ba1de-111">Der Befehl gibt einen Grund an, den Sie zum Beenden des Auftrags ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="ba1de-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="ba1de-112">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="ba1de-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="ba1de-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba1de-113">PARAMETERS</span></span>

### <span data-ttu-id="ba1de-114">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="ba1de-114">-BatchContext</span></span>
<span data-ttu-id="ba1de-115">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba1de-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ba1de-116">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba1de-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="ba1de-117">-ID</span><span class="sxs-lookup"><span data-stu-id="ba1de-117">-Id</span></span>
<span data-ttu-id="ba1de-118">Gibt die ID des Auftrags an, der vom Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="ba1de-118">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="ba1de-119">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="ba1de-119">-TerminateReason</span></span>
<span data-ttu-id="ba1de-120">Gibt den Grund an, zu dem Sie den Auftrag beendet haben.</span><span class="sxs-lookup"><span data-stu-id="ba1de-120">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="ba1de-121">Dieses Cmdlet speichert diesen Text als **TerminateReason** -Eigenschaft des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="ba1de-121">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

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

### <span data-ttu-id="ba1de-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba1de-122">-DefaultProfile</span></span>
<span data-ttu-id="ba1de-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ba1de-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba1de-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba1de-124">CommonParameters</span></span>
<span data-ttu-id="ba1de-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba1de-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba1de-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba1de-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba1de-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba1de-127">INPUTS</span></span>

### <span data-ttu-id="ba1de-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ba1de-128">BatchAccountContext</span></span>
<span data-ttu-id="ba1de-129">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ba1de-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ba1de-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ba1de-130">String</span></span>
<span data-ttu-id="ba1de-131">Der Parameter "ID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ba1de-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="ba1de-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba1de-132">OUTPUTS</span></span>

## <span data-ttu-id="ba1de-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba1de-133">NOTES</span></span>

## <span data-ttu-id="ba1de-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba1de-134">RELATED LINKS</span></span>

[<span data-ttu-id="ba1de-135">Deaktivieren-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ba1de-135">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="ba1de-136">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ba1de-136">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="ba1de-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ba1de-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ba1de-138">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ba1de-138">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="ba1de-139">Neu – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ba1de-139">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="ba1de-140">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ba1de-140">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="ba1de-141">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="ba1de-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


