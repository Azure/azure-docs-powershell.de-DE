---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
ms.openlocfilehash: fb1f9cf884b3443ec9746eca7cef603c7b9f3a38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505797"
---
# <span data-ttu-id="c3ddb-101">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c3ddb-101">Disable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="c3ddb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3ddb-102">SYNOPSIS</span></span>
<span data-ttu-id="c3ddb-103">Deaktiviert einen stapelverarbeitungsauftrags Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="c3ddb-103">Disables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3ddb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3ddb-104">SYNTAX</span></span>

```
Disable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3ddb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3ddb-105">DESCRIPTION</span></span>
<span data-ttu-id="c3ddb-106">Das Cmdlet **Disable-AzureBatchJobSchedule** deaktiviert einen Azure-Batch Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="c3ddb-106">The **Disable-AzureBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="c3ddb-107">Wenn Sie einen Terminplan deaktivieren, werden keine Aufträge entsprechend diesem Zeitplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="c3ddb-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="c3ddb-108">Sie können einen deaktivierten Zeitplan später aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c3ddb-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="c3ddb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3ddb-109">EXAMPLES</span></span>

### <span data-ttu-id="c3ddb-110">Beispiel 1: Deaktivieren eines Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="c3ddb-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="c3ddb-111">Dieser Befehl deaktiviert den Auftragszeitplan mit der ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="c3ddb-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="c3ddb-112">Verwenden Sie das Cmdlet **Get-AzureRmBatchAccountKeys** , um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="c3ddb-112">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="c3ddb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3ddb-113">PARAMETERS</span></span>

### <span data-ttu-id="c3ddb-114">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="c3ddb-114">-BatchContext</span></span>
<span data-ttu-id="c3ddb-115">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3ddb-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c3ddb-116">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3ddb-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c3ddb-117">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c3ddb-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c3ddb-118">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3ddb-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c3ddb-119">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="c3ddb-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c3ddb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3ddb-120">-DefaultProfile</span></span>
<span data-ttu-id="c3ddb-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3ddb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3ddb-122">-ID</span><span class="sxs-lookup"><span data-stu-id="c3ddb-122">-Id</span></span>
<span data-ttu-id="c3ddb-123">Gibt die ID des Auftragszeitplans an, der vom Cmdlet deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="c3ddb-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="c3ddb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3ddb-124">CommonParameters</span></span>
<span data-ttu-id="c3ddb-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3ddb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3ddb-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3ddb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3ddb-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3ddb-127">INPUTS</span></span>

### <span data-ttu-id="c3ddb-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c3ddb-128">BatchAccountContext</span></span>
<span data-ttu-id="c3ddb-129">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c3ddb-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="c3ddb-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c3ddb-130">String</span></span>
<span data-ttu-id="c3ddb-131">Der Parameter "ID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c3ddb-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="c3ddb-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3ddb-132">OUTPUTS</span></span>

## <span data-ttu-id="c3ddb-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3ddb-133">NOTES</span></span>

## <span data-ttu-id="c3ddb-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3ddb-134">RELATED LINKS</span></span>

[<span data-ttu-id="c3ddb-135">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c3ddb-135">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="c3ddb-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c3ddb-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c3ddb-137">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c3ddb-137">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="c3ddb-138">Neu – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c3ddb-138">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="c3ddb-139">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c3ddb-139">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="c3ddb-140">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c3ddb-140">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="c3ddb-141">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="c3ddb-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


