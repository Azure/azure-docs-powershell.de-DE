---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: 51e9053737b95113144d5421492f64623b425ff6
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93848012"
---
# <span data-ttu-id="32d7b-101">Get-AzBatchTaskCount</span><span class="sxs-lookup"><span data-stu-id="32d7b-101">Get-AzBatchTaskCount</span></span>

## <span data-ttu-id="32d7b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="32d7b-102">SYNOPSIS</span></span>
<span data-ttu-id="32d7b-103">Ruft die Aufgabenanzahl für den angegebenen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="32d7b-103">Gets the task counts for the specified job.</span></span>

## <span data-ttu-id="32d7b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="32d7b-104">SYNTAX</span></span>

### <span data-ttu-id="32d7b-105">ID</span><span class="sxs-lookup"><span data-stu-id="32d7b-105">Id</span></span>
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32d7b-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="32d7b-106">ParentObject</span></span>
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32d7b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32d7b-107">DESCRIPTION</span></span>
<span data-ttu-id="32d7b-108">Das Cmdlet " **Get-AzBatchTaskCount** " Ruft die Azure-Batch Aufgabenanzahl für einen Stapelverarbeitungsauftrag ab.</span><span class="sxs-lookup"><span data-stu-id="32d7b-108">The **Get-AzBatchTaskCount** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="32d7b-109">Geben Sie einen Auftrag entweder mit dem *JobID* -Parameter oder dem *Job* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="32d7b-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="32d7b-110">Vorgangs Zählungen stellen die Anzahl der Aufgaben durch den aktiven, ausgeführten oder abgeschlossenen Vorgangsstatus sowie die Anzahl der Vorgänge bereit, die erfolgreich oder fehlgeschlagen sind.</span><span class="sxs-lookup"><span data-stu-id="32d7b-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="32d7b-111">Aufgaben im Status "vorbereiten" werden als ausgeführt gezählt.</span><span class="sxs-lookup"><span data-stu-id="32d7b-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="32d7b-112">Wenn die validationStatus-Funktion nicht überprüft wird, konnte der Batch Dienst die Zustands Zählungen nicht für die Vorgangs Zustände überprüfen, wie in der API für Listen Aufgaben angegeben.</span><span class="sxs-lookup"><span data-stu-id="32d7b-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="32d7b-113">Die validationStatus kann nicht überprüft werden, wenn der Auftrag mehr als 200.000 Aufgaben enthält.</span><span class="sxs-lookup"><span data-stu-id="32d7b-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="32d7b-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="32d7b-114">EXAMPLES</span></span>

### <span data-ttu-id="32d7b-115">Beispiel 1: Abrufen von Aufgaben Zählungen nach ID</span><span class="sxs-lookup"><span data-stu-id="32d7b-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="32d7b-116">Dieser Befehl ruft die Aufgabenanzahl für Job Job01 ab.</span><span class="sxs-lookup"><span data-stu-id="32d7b-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="32d7b-117">Verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="32d7b-117">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="32d7b-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="32d7b-118">PARAMETERS</span></span>

### <span data-ttu-id="32d7b-119">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="32d7b-119">-BatchContext</span></span>
<span data-ttu-id="32d7b-120">Die BatchAccountContext-Instanz, die bei der Interaktion mit dem Batch Dienst verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="32d7b-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="32d7b-121">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="32d7b-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="32d7b-122">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="32d7b-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="32d7b-123">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="32d7b-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="32d7b-124">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="32d7b-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="32d7b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32d7b-125">-DefaultProfile</span></span>
<span data-ttu-id="32d7b-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="32d7b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32d7b-127">-Job</span><span class="sxs-lookup"><span data-stu-id="32d7b-127">-Job</span></span>
<span data-ttu-id="32d7b-128">Gibt den Auftrag an, der Aufgaben enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="32d7b-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="32d7b-129">Verwenden Sie das Get-AzBatchJob-Cmdlet, um ein **PSCloudJob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="32d7b-129">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32d7b-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="32d7b-130">-JobId</span></span>
<span data-ttu-id="32d7b-131">Die ID des Auftrags, für den die Vorgangsanzahl abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="32d7b-131">The id of the job for which to get task counts.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32d7b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32d7b-132">CommonParameters</span></span>
<span data-ttu-id="32d7b-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32d7b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32d7b-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32d7b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32d7b-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="32d7b-135">INPUTS</span></span>

### <span data-ttu-id="32d7b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="32d7b-136">System.String</span></span>

### <span data-ttu-id="32d7b-137">Microsoft.Azure.Commands.Batch. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="32d7b-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="32d7b-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="32d7b-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="32d7b-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="32d7b-139">OUTPUTS</span></span>

### <span data-ttu-id="32d7b-140">Microsoft.Azure.Commands.Batch. Models. PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="32d7b-140">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="32d7b-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="32d7b-141">NOTES</span></span>

## <span data-ttu-id="32d7b-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="32d7b-142">RELATED LINKS</span></span>

[<span data-ttu-id="32d7b-143">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="32d7b-143">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="32d7b-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="32d7b-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="32d7b-145">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="32d7b-145">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)
