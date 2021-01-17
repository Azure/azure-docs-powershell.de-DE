---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: d1f493556a1ff1007073611338b937ef0715c164
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362366"
---
# <span data-ttu-id="5467f-101">Get-AzBatchTaskCount</span><span class="sxs-lookup"><span data-stu-id="5467f-101">Get-AzBatchTaskCount</span></span>

## <span data-ttu-id="5467f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5467f-102">SYNOPSIS</span></span>
<span data-ttu-id="5467f-103">Ruft die Anzahl der Aufgaben für den angegebenen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="5467f-103">Gets the task counts for the specified job.</span></span>

## <span data-ttu-id="5467f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5467f-104">SYNTAX</span></span>

### <span data-ttu-id="5467f-105">ID</span><span class="sxs-lookup"><span data-stu-id="5467f-105">Id</span></span>
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5467f-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="5467f-106">ParentObject</span></span>
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5467f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5467f-107">DESCRIPTION</span></span>
<span data-ttu-id="5467f-108">Das **Cmdlet "Get-AzBatchTaskCount"** ruft die Azure Batch-Aufgabenanzahl für einen Stapelauftrag ab.</span><span class="sxs-lookup"><span data-stu-id="5467f-108">The **Get-AzBatchTaskCount** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="5467f-109">Geben Sie einen Auftrag entweder mit dem *Parameter "JobId"* oder dem *Parameter "Job"* an.</span><span class="sxs-lookup"><span data-stu-id="5467f-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="5467f-110">Die Aufgabenanzahl gibt die Anzahl der Aufgaben nach aktivem, ausgeführten oder abgeschlossenen Aufgabenstatus sowie die Anzahl der Aufgaben an, die erfolgreich waren oder fehlgeschlagen sind.</span><span class="sxs-lookup"><span data-stu-id="5467f-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="5467f-111">Aufgaben im Status "Vorbereiten" werden als ausgeführt gezählt.</span><span class="sxs-lookup"><span data-stu-id="5467f-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="5467f-112">Wenn die Gültigkeitsprüfung "validationStatus" nicht überprüft wurde, konnte der Batchdienst die Statusanzahl nicht mit den Aufgabenzuständen überprüfen, wie in der Listenaufgaben-API gemeldet.</span><span class="sxs-lookup"><span data-stu-id="5467f-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="5467f-113">Der Gültigkeitsprüfungsstatus ist möglicherweise nichtvalidiert, wenn der Auftrag mehr als 200.000 Vorgänge enthält.</span><span class="sxs-lookup"><span data-stu-id="5467f-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="5467f-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5467f-114">EXAMPLES</span></span>

### <span data-ttu-id="5467f-115">Beispiel 1: Erhalten der Vorgangsanzahl nach ID</span><span class="sxs-lookup"><span data-stu-id="5467f-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="5467f-116">Dieser Befehl ruft die Aufgabenanzahl für Auftrag Job01 ab.</span><span class="sxs-lookup"><span data-stu-id="5467f-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="5467f-117">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der Variablen einen Kontext $Context zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="5467f-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="5467f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5467f-118">PARAMETERS</span></span>

### <span data-ttu-id="5467f-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5467f-119">-BatchContext</span></span>
<span data-ttu-id="5467f-120">Die BatchAccountContext-Instanz, die bei der Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5467f-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="5467f-121">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="5467f-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="5467f-122">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5467f-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="5467f-123">Bei verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="5467f-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="5467f-124">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5467f-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5467f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5467f-125">-DefaultProfile</span></span>
<span data-ttu-id="5467f-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5467f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5467f-127">-Job</span><span class="sxs-lookup"><span data-stu-id="5467f-127">-Job</span></span>
<span data-ttu-id="5467f-128">Gibt den Auftrag an, der Aufgaben enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5467f-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="5467f-129">Zum Abrufen eines **PSCloudJob-Objekts** verwenden Sie das Get-AzBatchJob-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5467f-129">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="5467f-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="5467f-130">-JobId</span></span>
<span data-ttu-id="5467f-131">Die ID des Auftrags, für den die Vorgangsanzahl ermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5467f-131">The id of the job for which to get task counts.</span></span>

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

### <span data-ttu-id="5467f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5467f-132">CommonParameters</span></span>
<span data-ttu-id="5467f-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5467f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5467f-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5467f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5467f-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5467f-135">INPUTS</span></span>

### <span data-ttu-id="5467f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5467f-136">System.String</span></span>

### <span data-ttu-id="5467f-137">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="5467f-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="5467f-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5467f-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5467f-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5467f-139">OUTPUTS</span></span>

### <span data-ttu-id="5467f-140">Microsoft.Azure.Commands.Batch. Models.PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="5467f-140">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="5467f-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5467f-141">NOTES</span></span>

## <span data-ttu-id="5467f-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5467f-142">RELATED LINKS</span></span>

[<span data-ttu-id="5467f-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5467f-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5467f-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="5467f-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="5467f-145">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="5467f-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
