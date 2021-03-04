---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: 294669fe5b9e5aeb01dfbfa7ab538a0f6d411cca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949619"
---
# <span data-ttu-id="bec3a-101">Get-AzBatchTaskCount</span><span class="sxs-lookup"><span data-stu-id="bec3a-101">Get-AzBatchTaskCount</span></span>

## <span data-ttu-id="bec3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bec3a-102">SYNOPSIS</span></span>
<span data-ttu-id="bec3a-103">Ruft die Anzahl der Aufgaben für den angegebenen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="bec3a-103">Gets the task counts for the specified job.</span></span>

## <span data-ttu-id="bec3a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bec3a-104">SYNTAX</span></span>

### <span data-ttu-id="bec3a-105">ID</span><span class="sxs-lookup"><span data-stu-id="bec3a-105">Id</span></span>
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bec3a-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="bec3a-106">ParentObject</span></span>
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bec3a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bec3a-107">DESCRIPTION</span></span>
<span data-ttu-id="bec3a-108">Das **Cmdlet Get-AzBatchTaskCount** ruft die Azure Batch-Aufgabenanzahl für einen Batchauftrag ab.</span><span class="sxs-lookup"><span data-stu-id="bec3a-108">The **Get-AzBatchTaskCount** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="bec3a-109">Geben Sie einen Auftrag entweder über den *Parameter "JobId"* oder den *Parameter "Auftrag"* an.</span><span class="sxs-lookup"><span data-stu-id="bec3a-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="bec3a-110">Vorgangszählungen stellen eine Anzahl der Vorgänge nach aktivem, ausgeführten oder abgeschlossenen Vorgangszustand und eine Anzahl von Vorgängen, die erfolgreich oder fehlgeschlagen sind, zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="bec3a-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="bec3a-111">Aufgaben im Vorbereitungszustand werden als ausgeführt gezählt.</span><span class="sxs-lookup"><span data-stu-id="bec3a-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="bec3a-112">Wenn der Gültigkeitsprüfungsstatus nicht mehr validiert ist, konnte der Batchdienst die Statuszählungen nicht mit den Vorgangszuständen überprüfen, wie in der LISTENaufgaben-API gemeldet.</span><span class="sxs-lookup"><span data-stu-id="bec3a-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="bec3a-113">Der Gültigkeitsprüfungsstatus ist möglicherweise nicht mehr aktiviert, wenn der Auftrag mehr als 200.000 Vorgänge enthält.</span><span class="sxs-lookup"><span data-stu-id="bec3a-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="bec3a-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bec3a-114">EXAMPLES</span></span>

### <span data-ttu-id="bec3a-115">Beispiel 1: Erhalten von Aufgabenanzahlen nach ID</span><span class="sxs-lookup"><span data-stu-id="bec3a-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="bec3a-116">Mit diesem Befehl werden die Aufgabenanzahlen für "Auftrag01" ermittelt.</span><span class="sxs-lookup"><span data-stu-id="bec3a-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="bec3a-117">Verwenden Sie Get-AzBatchAccountKey-Cmdlet, um der Variablen $Context Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="bec3a-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="bec3a-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bec3a-118">PARAMETERS</span></span>

### <span data-ttu-id="bec3a-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bec3a-119">-BatchContext</span></span>
<span data-ttu-id="bec3a-120">Die BatchAccountContext-Instanz, die bei der Interaktion mit dem Batchdienst verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bec3a-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="bec3a-121">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="bec3a-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="bec3a-122">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bec3a-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="bec3a-123">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="bec3a-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="bec3a-124">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="bec3a-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bec3a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec3a-125">-DefaultProfile</span></span>
<span data-ttu-id="bec3a-126">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bec3a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bec3a-127">-Job</span><span class="sxs-lookup"><span data-stu-id="bec3a-127">-Job</span></span>
<span data-ttu-id="bec3a-128">Gibt den Auftrag an, der Aufgaben enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="bec3a-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="bec3a-129">Um ein **PSCloudJob-Objekt** zu erhalten, verwenden Sie das Get-AzBatchJob Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bec3a-129">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="bec3a-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="bec3a-130">-JobId</span></span>
<span data-ttu-id="bec3a-131">Die ID des Auftrags, für den aufgabenanzahlt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bec3a-131">The id of the job for which to get task counts.</span></span>

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

### <span data-ttu-id="bec3a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec3a-132">CommonParameters</span></span>
<span data-ttu-id="bec3a-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bec3a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec3a-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bec3a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec3a-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bec3a-135">INPUTS</span></span>

### <span data-ttu-id="bec3a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bec3a-136">System.String</span></span>

### <span data-ttu-id="bec3a-137">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="bec3a-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="bec3a-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bec3a-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="bec3a-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bec3a-139">OUTPUTS</span></span>

### <span data-ttu-id="bec3a-140">Microsoft.Azure.Commands.Batch. Models.PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="bec3a-140">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="bec3a-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bec3a-141">NOTES</span></span>

## <span data-ttu-id="bec3a-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bec3a-142">RELATED LINKS</span></span>

[<span data-ttu-id="bec3a-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="bec3a-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="bec3a-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="bec3a-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="bec3a-145">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bec3a-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
