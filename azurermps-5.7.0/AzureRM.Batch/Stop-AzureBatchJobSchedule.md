---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 719c743281102f83c08f55093d221856be4194bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662380"
---
# <span data-ttu-id="81e71-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="81e71-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="81e71-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="81e71-102">SYNOPSIS</span></span>
<span data-ttu-id="81e71-103">Beendet einen stapelverarbeitungsauftrags Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="81e71-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81e71-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="81e71-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81e71-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81e71-105">DESCRIPTION</span></span>
<span data-ttu-id="81e71-106">Das Cmdlet **Stop-AzureBatchJobSchedule** beendet einen Azure-Batch Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="81e71-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="81e71-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81e71-107">EXAMPLES</span></span>

### <span data-ttu-id="81e71-108">Beispiel 1: Beenden eines Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="81e71-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="81e71-109">Dieser Befehl beendet den Auftragszeitplan mit der ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="81e71-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="81e71-110">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="81e71-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="81e71-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="81e71-111">PARAMETERS</span></span>

### <span data-ttu-id="81e71-112">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="81e71-112">-BatchContext</span></span>
<span data-ttu-id="81e71-113">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="81e71-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="81e71-114">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="81e71-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="81e71-115">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="81e71-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="81e71-116">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="81e71-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="81e71-117">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="81e71-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="81e71-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81e71-118">-DefaultProfile</span></span>
<span data-ttu-id="81e71-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="81e71-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81e71-120">-ID</span><span class="sxs-lookup"><span data-stu-id="81e71-120">-Id</span></span>
<span data-ttu-id="81e71-121">Gibt die ID des Auftragszeitplans an, der vom Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="81e71-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="81e71-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81e71-122">CommonParameters</span></span>
<span data-ttu-id="81e71-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81e71-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81e71-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81e71-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81e71-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="81e71-125">INPUTS</span></span>

### <span data-ttu-id="81e71-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="81e71-126">BatchAccountContext</span></span>
<span data-ttu-id="81e71-127">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="81e71-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="81e71-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="81e71-128">String</span></span>
<span data-ttu-id="81e71-129">Der Parameter "ID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="81e71-129">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="81e71-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="81e71-130">OUTPUTS</span></span>

## <span data-ttu-id="81e71-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="81e71-131">NOTES</span></span>

## <span data-ttu-id="81e71-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="81e71-132">RELATED LINKS</span></span>

[<span data-ttu-id="81e71-133">Deaktivieren-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="81e71-133">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="81e71-134">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="81e71-134">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="81e71-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="81e71-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="81e71-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="81e71-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="81e71-137">Neu – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="81e71-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="81e71-138">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="81e71-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="81e71-139">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="81e71-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


