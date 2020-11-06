---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchtaskcounts
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
ms.openlocfilehash: d0b98081675cd11d8d3eb60a6495ac87a1111034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478742"
---
# <span data-ttu-id="5bdf3-101">Get-AzureBatchTaskCounts</span><span class="sxs-lookup"><span data-stu-id="5bdf3-101">Get-AzureBatchTaskCounts</span></span>

## <span data-ttu-id="5bdf3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5bdf3-102">SYNOPSIS</span></span>
<span data-ttu-id="5bdf3-103">Ruft die Aufgabenanzahl für den angegebenen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-103">Gets the task counts for the specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bdf3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bdf3-104">SYNTAX</span></span>

### <span data-ttu-id="5bdf3-105">ID</span><span class="sxs-lookup"><span data-stu-id="5bdf3-105">Id</span></span>
```
Get-AzureBatchTaskCounts [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="5bdf3-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="5bdf3-106">ParentObject</span></span>
```
Get-AzureBatchTaskCounts [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="5bdf3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5bdf3-107">DESCRIPTION</span></span>
<span data-ttu-id="5bdf3-108">Das Cmdlet " **Get-AzureBatchTaskCounts** " Ruft die Azure-Batch Aufgabenanzahl für einen Stapelverarbeitungsauftrag ab.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-108">The **Get-AzureBatchTaskCounts** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="5bdf3-109">Geben Sie einen Auftrag entweder mit dem *JobID* -Parameter oder dem *Job* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="5bdf3-110">Vorgangs Zählungen stellen die Anzahl der Aufgaben durch den aktiven, ausgeführten oder abgeschlossenen Vorgangsstatus sowie die Anzahl der Vorgänge bereit, die erfolgreich oder fehlgeschlagen sind.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="5bdf3-111">Aufgaben im Status "vorbereiten" werden als ausgeführt gezählt.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="5bdf3-112">Wenn die validationStatus-Funktion nicht überprüft wird, konnte der Batch Dienst die Zustands Zählungen nicht für die Vorgangs Zustände überprüfen, wie in der API für Listen Aufgaben angegeben.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="5bdf3-113">Die validationStatus kann nicht überprüft werden, wenn der Auftrag mehr als 200.000 Aufgaben enthält.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="5bdf3-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5bdf3-114">EXAMPLES</span></span>

### <span data-ttu-id="5bdf3-115">Beispiel 1: Abrufen von Aufgaben Zählungen nach ID</span><span class="sxs-lookup"><span data-stu-id="5bdf3-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzureBatchTaskCounts -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="5bdf3-116">Dieser Befehl ruft die Aufgabenanzahl für Job Job01 ab.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="5bdf3-117">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-117">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="5bdf3-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bdf3-118">PARAMETERS</span></span>

### <span data-ttu-id="5bdf3-119">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="5bdf3-119">-BatchContext</span></span>
<span data-ttu-id="5bdf3-120">Die BatchAccountContext-Instanz, die bei der Interaktion mit dem Batch Dienst verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="5bdf3-121">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="5bdf3-122">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="5bdf3-123">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="5bdf3-124">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5bdf3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bdf3-125">-DefaultProfile</span></span>
<span data-ttu-id="5bdf3-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bdf3-127">-Job</span><span class="sxs-lookup"><span data-stu-id="5bdf3-127">-Job</span></span>
<span data-ttu-id="5bdf3-128">Gibt den Auftrag an, der Aufgaben enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="5bdf3-129">Verwenden Sie das Get-AzureBatchJob-Cmdlet, um ein **PSCloudJob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-129">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bdf3-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="5bdf3-130">-JobId</span></span>
<span data-ttu-id="5bdf3-131">Die ID des Auftrags, für den die Vorgangsanzahl abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5bdf3-131">The id of the job for which to get task counts.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="5bdf3-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5bdf3-132">INPUTS</span></span>

### <span data-ttu-id="5bdf3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5bdf3-133">System.String</span></span>
<span data-ttu-id="5bdf3-134">Microsoft.Azure.Commands.Batch. Models. PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5bdf3-134">Microsoft.Azure.Commands.Batch.Models.PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>


## <span data-ttu-id="5bdf3-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5bdf3-135">OUTPUTS</span></span>

### <span data-ttu-id="5bdf3-136">Microsoft.Azure.Commands.Batch. Models. PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="5bdf3-136">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>


## <span data-ttu-id="5bdf3-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="5bdf3-137">NOTES</span></span>

## <span data-ttu-id="5bdf3-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5bdf3-138">RELATED LINKS</span></span>

[<span data-ttu-id="5bdf3-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5bdf3-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5bdf3-140">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5bdf3-140">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="5bdf3-141">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="5bdf3-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
