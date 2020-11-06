---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: 3081721db5cb113d48417ddf28d8a96512d27f99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502626"
---
# <span data-ttu-id="bbc21-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bbc21-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="bbc21-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bbc21-102">SYNOPSIS</span></span>
<span data-ttu-id="bbc21-103">Aktiviert einen Stapel Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="bbc21-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbc21-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bbc21-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbc21-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bbc21-105">DESCRIPTION</span></span>
<span data-ttu-id="bbc21-106">Das Cmdlet **enable-AzureBatchJobSchedule** aktiviert einen Azure-Batch Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="bbc21-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="bbc21-107">Nachdem Sie einen Projektplan aktiviert haben, können Aufträge entsprechend diesem Zeitplan erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bbc21-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="bbc21-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bbc21-108">EXAMPLES</span></span>

### <span data-ttu-id="bbc21-109">Beispiel 1: Aktivieren eines Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="bbc21-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="bbc21-110">Dieser Befehl aktiviert den Auftragszeitplan mit der ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="bbc21-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="bbc21-111">Verwenden Sie das Cmdlet **Get-AzureRmBatchAccountKeys** , um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="bbc21-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="bbc21-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="bbc21-112">PARAMETERS</span></span>

### <span data-ttu-id="bbc21-113">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="bbc21-113">-BatchContext</span></span>
<span data-ttu-id="bbc21-114">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="bbc21-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bbc21-115">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="bbc21-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bbc21-116">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bbc21-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bbc21-117">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="bbc21-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bbc21-118">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="bbc21-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bbc21-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbc21-119">-DefaultProfile</span></span>
<span data-ttu-id="bbc21-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bbc21-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbc21-121">-ID</span><span class="sxs-lookup"><span data-stu-id="bbc21-121">-Id</span></span>
<span data-ttu-id="bbc21-122">Gibt die ID des Auftragszeitplans an, den dieses Cmdlet aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bbc21-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="bbc21-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbc21-123">CommonParameters</span></span>
<span data-ttu-id="bbc21-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbc21-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbc21-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbc21-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbc21-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bbc21-126">INPUTS</span></span>

### <span data-ttu-id="bbc21-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bbc21-127">BatchAccountContext</span></span>
<span data-ttu-id="bbc21-128">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="bbc21-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="bbc21-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bbc21-129">String</span></span>
<span data-ttu-id="bbc21-130">Der Parameter "ID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="bbc21-130">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="bbc21-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bbc21-131">OUTPUTS</span></span>

## <span data-ttu-id="bbc21-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="bbc21-132">NOTES</span></span>

## <span data-ttu-id="bbc21-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bbc21-133">RELATED LINKS</span></span>

[<span data-ttu-id="bbc21-134">Deaktivieren-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bbc21-134">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="bbc21-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bbc21-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="bbc21-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bbc21-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="bbc21-137">Neu – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bbc21-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="bbc21-138">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bbc21-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="bbc21-139">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bbc21-139">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="bbc21-140">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbc21-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


