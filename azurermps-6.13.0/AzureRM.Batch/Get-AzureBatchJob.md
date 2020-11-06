---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
ms.openlocfilehash: 1a5f971e52da27eb2abeca02c4362eee9b9755c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498433"
---
# <span data-ttu-id="90543-101">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="90543-101">Get-AzureBatchJob</span></span>

## <span data-ttu-id="90543-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90543-102">SYNOPSIS</span></span>
<span data-ttu-id="90543-103">Ruft Stapelverarbeitungsaufträge für ein Stapelverarbeitungs Konto oder einen Auftragszeitplan ab.</span><span class="sxs-lookup"><span data-stu-id="90543-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90543-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90543-104">SYNTAX</span></span>

### <span data-ttu-id="90543-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="90543-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="90543-106">ID</span><span class="sxs-lookup"><span data-stu-id="90543-106">Id</span></span>
```
Get-AzureBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90543-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="90543-107">ParentObject</span></span>
```
Get-AzureBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90543-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90543-108">DESCRIPTION</span></span>
<span data-ttu-id="90543-109">Das Cmdlet " **Get-AzureBatchJob** " Ruft die Azure-Stapelverarbeitungsaufträge für das vom *BatchAccountContext* -Parameter angegebene Batch Konto ab.</span><span class="sxs-lookup"><span data-stu-id="90543-109">The **Get-AzureBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="90543-110">Sie können den *ID-* Parameter verwenden, um einen einzelnen Auftrag zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="90543-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="90543-111">Sie können den *Filter* -Parameter verwenden, um die Aufträge abzurufen, die einem OData-Filter (Open Data Protocol) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="90543-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="90543-112">Wenn Sie eine Auftragsplan-ID oder eine **PSCloudJobSchedule** -Instanz angeben, gibt dieses Cmdlet nur die Aufträge für diesen Auftragszeitplan zurück.</span><span class="sxs-lookup"><span data-stu-id="90543-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="90543-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90543-113">EXAMPLES</span></span>

### <span data-ttu-id="90543-114">Beispiel 1: Abrufen eines stapelverarbeitungsauftrags nach ID</span><span class="sxs-lookup"><span data-stu-id="90543-114">Example 1: Get a Batch job by ID</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job01" -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:12:07 PM
DisplayName                 : 
ETag                        : 0x8D29535B2941439
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : Job01
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:12:07 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:12:07 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01
```

<span data-ttu-id="90543-115">Dieser Befehl ruft den Auftrag ab, der die ID Job01.</span><span class="sxs-lookup"><span data-stu-id="90543-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="90543-116">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="90543-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="90543-117">Beispiel 2: Abrufen aller aktiven Aufträge für einen Auftragszeitplan</span><span class="sxs-lookup"><span data-stu-id="90543-117">Example 2: Get all active jobs for a job schedule</span></span>
```
PS C:\>Get-AzureBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 : 
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="90543-118">Dieser Befehl ruft die aktiven Aufträge für den Auftragszeitplan ab, der die ID JobSchedule27.</span><span class="sxs-lookup"><span data-stu-id="90543-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="90543-119">Beispiel 3: Ruft alle Aufträge unter einem Auftragszeitplan mithilfe der Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="90543-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzureBatchJob -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 : 
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="90543-120">Dieser Befehl ruft den Auftragszeitplan mit der ID-JobSchedule27 mithilfe des Get-AzureBatchJobSchedule-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="90543-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzureBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="90543-121">Der Befehl übergibt diesen Auftragszeitplan mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90543-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="90543-122">Der Befehl ruft alle Aufträge für diesen Auftragszeitplan ab.</span><span class="sxs-lookup"><span data-stu-id="90543-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="90543-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="90543-123">PARAMETERS</span></span>

### <span data-ttu-id="90543-124">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="90543-124">-BatchContext</span></span>
<span data-ttu-id="90543-125">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="90543-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="90543-126">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="90543-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="90543-127">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="90543-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="90543-128">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="90543-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="90543-129">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="90543-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="90543-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90543-130">-DefaultProfile</span></span>
<span data-ttu-id="90543-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="90543-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90543-132">– Erweitern</span><span class="sxs-lookup"><span data-stu-id="90543-132">-Expand</span></span>
<span data-ttu-id="90543-133">Gibt eine Open Data Protocol (OData) expand-Klausel an.</span><span class="sxs-lookup"><span data-stu-id="90543-133">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="90543-134">Geben Sie einen Wert für diesen Parameter an, um zugeordnete Entitäten der Haupt Entität abzurufen, die Sie erhalten.</span><span class="sxs-lookup"><span data-stu-id="90543-134">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90543-135">-Filter</span><span class="sxs-lookup"><span data-stu-id="90543-135">-Filter</span></span>
<span data-ttu-id="90543-136">Gibt eine OData-Filterklausel für Jobs an.</span><span class="sxs-lookup"><span data-stu-id="90543-136">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="90543-137">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Aufträge für das Stapelverarbeitungs Konto oder den Auftragszeitplan zurück.</span><span class="sxs-lookup"><span data-stu-id="90543-137">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90543-138">-ID</span><span class="sxs-lookup"><span data-stu-id="90543-138">-Id</span></span>
<span data-ttu-id="90543-139">Gibt die ID des Auftrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="90543-139">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="90543-140">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="90543-140">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90543-141">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="90543-141">-JobSchedule</span></span>
<span data-ttu-id="90543-142">Gibt ein **PSCloudJobSchedule** -Objekt an, das den Auftragszeitplan darstellt, der die Aufträge enthält.</span><span class="sxs-lookup"><span data-stu-id="90543-142">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="90543-143">Verwenden Sie das Get-AzureBatchJobSchedule-Cmdlet, um ein **PSCloudJobSchedule** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="90543-143">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90543-144">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="90543-144">-JobScheduleId</span></span>
<span data-ttu-id="90543-145">Gibt die ID des Auftragszeitplans an, der die Aufträge enthält.</span><span class="sxs-lookup"><span data-stu-id="90543-145">Specifies the ID of the job schedule which contains the jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90543-146">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="90543-146">-MaxCount</span></span>
<span data-ttu-id="90543-147">Gibt die maximale Anzahl von Aufträgen an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="90543-147">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="90543-148">Wenn Sie den Wert 0 (null) oder weniger angeben, verwendet das Cmdlet keine Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="90543-148">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="90543-149">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="90543-149">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90543-150">-Wählen Sie</span><span class="sxs-lookup"><span data-stu-id="90543-150">-Select</span></span>
<span data-ttu-id="90543-151">Gibt eine OData-Auswahl Klausel an.</span><span class="sxs-lookup"><span data-stu-id="90543-151">Specifies an OData select clause.</span></span>
<span data-ttu-id="90543-152">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften und nicht alle Objekteigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="90543-152">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90543-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90543-153">CommonParameters</span></span>
<span data-ttu-id="90543-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90543-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90543-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90543-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90543-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90543-156">INPUTS</span></span>

### <span data-ttu-id="90543-157">System. String</span><span class="sxs-lookup"><span data-stu-id="90543-157">System.String</span></span>

### <span data-ttu-id="90543-158">Microsoft.Azure.Commands.Batch. Models. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="90543-158">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>
<span data-ttu-id="90543-159">Parameter: JobSchedule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="90543-159">Parameters: JobSchedule (ByValue)</span></span>

### <span data-ttu-id="90543-160">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="90543-160">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="90543-161">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="90543-161">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="90543-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90543-162">OUTPUTS</span></span>

### <span data-ttu-id="90543-163">Microsoft.Azure.Commands.Batch. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="90543-163">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

## <span data-ttu-id="90543-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="90543-164">NOTES</span></span>

## <span data-ttu-id="90543-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90543-165">RELATED LINKS</span></span>

[<span data-ttu-id="90543-166">Deaktivieren-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="90543-166">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="90543-167">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="90543-167">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="90543-168">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="90543-168">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="90543-169">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="90543-169">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="90543-170">Neu – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="90543-170">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="90543-171">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="90543-171">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="90543-172">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="90543-172">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="90543-173">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="90543-173">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


