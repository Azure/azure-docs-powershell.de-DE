---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
ms.openlocfilehash: b0709c7b839ca992d415cd5ba9fff58e769120fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471184"
---
# <span data-ttu-id="0ccf6-101">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="0ccf6-101">Get-AzBatchJob</span></span>

## <span data-ttu-id="0ccf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ccf6-102">SYNOPSIS</span></span>
<span data-ttu-id="0ccf6-103">Ruft Stapelaufträge für ein Batchkonto oder einen Auftragszeitplan ab.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

## <span data-ttu-id="0ccf6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ccf6-104">SYNTAX</span></span>

### <span data-ttu-id="0ccf6-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="0ccf6-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ccf6-106">ID</span><span class="sxs-lookup"><span data-stu-id="0ccf6-106">Id</span></span>
```
Get-AzBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ccf6-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="0ccf6-107">ParentObject</span></span>
```
Get-AzBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ccf6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ccf6-108">DESCRIPTION</span></span>
<span data-ttu-id="0ccf6-109">Das **Cmdlet "Get-AzBatchJob"** ruft die Azure -Batchaufträge für das Batchkonto ab, das vom Parameter *"BatchAccountContext" angegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-109">The **Get-AzBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="0ccf6-110">Sie können den Parameter *"Id"* verwenden, um einen einzelnen Auftrag zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="0ccf6-111">Sie können den Parameter *"Filter"* verwenden, um die Aufträge zu erhalten, die einem Open Data Protocol (OData)-Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="0ccf6-112">Wenn Sie eine Auftragszeitplan-ID oder eine **PSCloudJobSchedule-Instanz** liefern, gibt dieses Cmdlet nur die Aufträge für diesen Stellenplan zurück.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="0ccf6-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0ccf6-113">EXAMPLES</span></span>

### <span data-ttu-id="0ccf6-114">Beispiel 1: Erhalten eines Stapelauftrags nach ID</span><span class="sxs-lookup"><span data-stu-id="0ccf6-114">Example 1: Get a Batch job by ID</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job01" -BatchContext $Context
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

<span data-ttu-id="0ccf6-115">Dieser Befehl ruft den Auftrag ab, der die ID "Job01" hat.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="0ccf6-116">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der Variablen einen Kontext $Context zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="0ccf6-117">Beispiel 2: Alle aktiven Aufträge für einen Stellenplan erhalten</span><span class="sxs-lookup"><span data-stu-id="0ccf6-117">Example 2: Get all active jobs for a job schedule</span></span>
```
PS C:\>Get-AzBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
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

<span data-ttu-id="0ccf6-118">Dieser Befehl ruft die aktiven Aufträge für den Auftragszeitplan ab, der die ID "JobSchedule27" hat.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="0ccf6-119">Beispiel 3: Ruft alle Aufträge unter einem Auftragszeitplan mithilfe der Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzBatchJob -BatchContext $Context
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

<span data-ttu-id="0ccf6-120">Mit diesem Befehl wird der Auftragszeitplan mit der ID "JobSchedule27" mithilfe des Cmdlets "Get-AzBatchJobSchedule" ruft.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="0ccf6-121">Der Befehl übergibt diesen Auftragszeitplan mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0ccf6-122">Der Befehl ruft alle Aufträge für diesen Stellenplan ab.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="0ccf6-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ccf6-123">PARAMETERS</span></span>

### <span data-ttu-id="0ccf6-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0ccf6-124">-BatchContext</span></span>
<span data-ttu-id="0ccf6-125">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0ccf6-126">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0ccf6-127">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0ccf6-128">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0ccf6-129">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0ccf6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ccf6-130">-DefaultProfile</span></span>
<span data-ttu-id="0ccf6-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ccf6-132">-Expand</span><span class="sxs-lookup"><span data-stu-id="0ccf6-132">-Expand</span></span>
<span data-ttu-id="0ccf6-133">Gibt eine Open Data Protocol (OData)-Erweiterungsklausel an.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-133">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="0ccf6-134">Geben Sie einen Wert für diesen Parameter an, um zugeordnete Entitäten der erhaltenen Hauptentität zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-134">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="0ccf6-135">-Filter</span><span class="sxs-lookup"><span data-stu-id="0ccf6-135">-Filter</span></span>
<span data-ttu-id="0ccf6-136">Gibt eine OData-Filterklausel für Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-136">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="0ccf6-137">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Aufträge für das Batchkonto oder den Auftragszeitplan zurück.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-137">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="0ccf6-138">-ID</span><span class="sxs-lookup"><span data-stu-id="0ccf6-138">-Id</span></span>
<span data-ttu-id="0ccf6-139">Gibt die ID des Auftrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-139">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="0ccf6-140">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-140">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="0ccf6-141">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="0ccf6-141">-JobSchedule</span></span>
<span data-ttu-id="0ccf6-142">Gibt ein **PSCloudJobSchedule-Objekt an,** das den Auftragszeitplan darstellt, der die Aufträge enthält.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-142">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="0ccf6-143">Verwenden Sie zum Abrufen **eines PSCloudJobSchedule-Objekts** das Get-AzBatchJobSchedule Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-143">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="0ccf6-144">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="0ccf6-144">-JobScheduleId</span></span>
<span data-ttu-id="0ccf6-145">Gibt die ID des Auftragsplans an, der die Aufträge enthält.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-145">Specifies the ID of the job schedule which contains the jobs.</span></span>

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

### <span data-ttu-id="0ccf6-146">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0ccf6-146">-MaxCount</span></span>
<span data-ttu-id="0ccf6-147">Gibt die maximale Anzahl von Aufträgen an, die zurückgeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-147">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="0ccf6-148">Wenn Sie einen Wert von Null (0) oder kleiner angeben, wird für das Cmdlet keine Obergrenze verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-148">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="0ccf6-149">Der Standardwert ist "1000".</span><span class="sxs-lookup"><span data-stu-id="0ccf6-149">The default value is 1000.</span></span>

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

### <span data-ttu-id="0ccf6-150">-Select</span><span class="sxs-lookup"><span data-stu-id="0ccf6-150">-Select</span></span>
<span data-ttu-id="0ccf6-151">Gibt eine OData-Auswahlklausel an.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-151">Specifies an OData select clause.</span></span>
<span data-ttu-id="0ccf6-152">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften und nicht alle Objekteigenschaften zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-152">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="0ccf6-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ccf6-153">CommonParameters</span></span>
<span data-ttu-id="0ccf6-154">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ccf6-155">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ccf6-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ccf6-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0ccf6-156">INPUTS</span></span>

### <span data-ttu-id="0ccf6-157">System.String</span><span class="sxs-lookup"><span data-stu-id="0ccf6-157">System.String</span></span>

### <span data-ttu-id="0ccf6-158">Microsoft.Azure.Commands.Batch. Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0ccf6-158">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="0ccf6-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0ccf6-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0ccf6-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0ccf6-160">OUTPUTS</span></span>

### <span data-ttu-id="0ccf6-161">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="0ccf6-161">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

## <span data-ttu-id="0ccf6-162">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0ccf6-162">NOTES</span></span>

## <span data-ttu-id="0ccf6-163">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0ccf6-163">RELATED LINKS</span></span>

[<span data-ttu-id="0ccf6-164">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="0ccf6-164">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="0ccf6-165">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="0ccf6-165">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="0ccf6-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="0ccf6-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="0ccf6-167">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0ccf6-167">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="0ccf6-168">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="0ccf6-168">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="0ccf6-169">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="0ccf6-169">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="0ccf6-170">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="0ccf6-170">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="0ccf6-171">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0ccf6-171">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
