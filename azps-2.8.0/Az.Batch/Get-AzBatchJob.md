---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
ms.openlocfilehash: 332bdb8d32b42d391518d50aef82436675cf3f9e
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847720"
---
# <span data-ttu-id="94dfe-101">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="94dfe-101">Get-AzBatchJob</span></span>

## <span data-ttu-id="94dfe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="94dfe-102">SYNOPSIS</span></span>
<span data-ttu-id="94dfe-103">Ruft Stapelverarbeitungsaufträge für ein Stapelverarbeitungs Konto oder einen Auftragszeitplan ab.</span><span class="sxs-lookup"><span data-stu-id="94dfe-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

## <span data-ttu-id="94dfe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="94dfe-104">SYNTAX</span></span>

### <span data-ttu-id="94dfe-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="94dfe-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="94dfe-106">ID</span><span class="sxs-lookup"><span data-stu-id="94dfe-106">Id</span></span>
```
Get-AzBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94dfe-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="94dfe-107">ParentObject</span></span>
```
Get-AzBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94dfe-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94dfe-108">DESCRIPTION</span></span>
<span data-ttu-id="94dfe-109">Das Cmdlet " **Get-AzBatchJob** " Ruft die Azure-Stapelverarbeitungsaufträge für das vom *BatchAccountContext* -Parameter angegebene Batch Konto ab.</span><span class="sxs-lookup"><span data-stu-id="94dfe-109">The **Get-AzBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="94dfe-110">Sie können den *ID-* Parameter verwenden, um einen einzelnen Auftrag zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="94dfe-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="94dfe-111">Sie können den *Filter* -Parameter verwenden, um die Aufträge abzurufen, die einem OData-Filter (Open Data Protocol) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="94dfe-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="94dfe-112">Wenn Sie eine Auftragsplan-ID oder eine **PSCloudJobSchedule** -Instanz angeben, gibt dieses Cmdlet nur die Aufträge für diesen Auftragszeitplan zurück.</span><span class="sxs-lookup"><span data-stu-id="94dfe-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="94dfe-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94dfe-113">EXAMPLES</span></span>

### <span data-ttu-id="94dfe-114">Beispiel 1: Abrufen eines stapelverarbeitungsauftrags nach ID</span><span class="sxs-lookup"><span data-stu-id="94dfe-114">Example 1: Get a Batch job by ID</span></span>
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

<span data-ttu-id="94dfe-115">Dieser Befehl ruft den Auftrag ab, der die ID Job01.</span><span class="sxs-lookup"><span data-stu-id="94dfe-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="94dfe-116">Verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="94dfe-116">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="94dfe-117">Beispiel 2: Abrufen aller aktiven Aufträge für einen Auftragszeitplan</span><span class="sxs-lookup"><span data-stu-id="94dfe-117">Example 2: Get all active jobs for a job schedule</span></span>
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

<span data-ttu-id="94dfe-118">Dieser Befehl ruft die aktiven Aufträge für den Auftragszeitplan ab, der die ID JobSchedule27.</span><span class="sxs-lookup"><span data-stu-id="94dfe-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="94dfe-119">Beispiel 3: Ruft alle Aufträge unter einem Auftragszeitplan mithilfe der Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="94dfe-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
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

<span data-ttu-id="94dfe-120">Dieser Befehl ruft den Auftragszeitplan mit der ID-JobSchedule27 mithilfe des Get-AzBatchJobSchedule-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="94dfe-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="94dfe-121">Der Befehl übergibt diesen Auftragszeitplan mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94dfe-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="94dfe-122">Der Befehl ruft alle Aufträge für diesen Auftragszeitplan ab.</span><span class="sxs-lookup"><span data-stu-id="94dfe-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="94dfe-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="94dfe-123">PARAMETERS</span></span>

### <span data-ttu-id="94dfe-124">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="94dfe-124">-BatchContext</span></span>
<span data-ttu-id="94dfe-125">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="94dfe-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="94dfe-126">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="94dfe-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="94dfe-127">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="94dfe-127">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="94dfe-128">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="94dfe-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="94dfe-129">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="94dfe-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="94dfe-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94dfe-130">-DefaultProfile</span></span>
<span data-ttu-id="94dfe-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="94dfe-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94dfe-132">– Erweitern</span><span class="sxs-lookup"><span data-stu-id="94dfe-132">-Expand</span></span>
<span data-ttu-id="94dfe-133">Gibt eine Open Data Protocol (OData) expand-Klausel an.</span><span class="sxs-lookup"><span data-stu-id="94dfe-133">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="94dfe-134">Geben Sie einen Wert für diesen Parameter an, um zugeordnete Entitäten der Haupt Entität abzurufen, die Sie erhalten.</span><span class="sxs-lookup"><span data-stu-id="94dfe-134">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="94dfe-135">-Filter</span><span class="sxs-lookup"><span data-stu-id="94dfe-135">-Filter</span></span>
<span data-ttu-id="94dfe-136">Gibt eine OData-Filterklausel für Jobs an.</span><span class="sxs-lookup"><span data-stu-id="94dfe-136">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="94dfe-137">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Aufträge für das Stapelverarbeitungs Konto oder den Auftragszeitplan zurück.</span><span class="sxs-lookup"><span data-stu-id="94dfe-137">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="94dfe-138">-ID</span><span class="sxs-lookup"><span data-stu-id="94dfe-138">-Id</span></span>
<span data-ttu-id="94dfe-139">Gibt die ID des Auftrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="94dfe-139">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="94dfe-140">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="94dfe-140">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="94dfe-141">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="94dfe-141">-JobSchedule</span></span>
<span data-ttu-id="94dfe-142">Gibt ein **PSCloudJobSchedule** -Objekt an, das den Auftragszeitplan darstellt, der die Aufträge enthält.</span><span class="sxs-lookup"><span data-stu-id="94dfe-142">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="94dfe-143">Verwenden Sie das Get-AzBatchJobSchedule-Cmdlet, um ein **PSCloudJobSchedule** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="94dfe-143">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="94dfe-144">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="94dfe-144">-JobScheduleId</span></span>
<span data-ttu-id="94dfe-145">Gibt die ID des Auftragszeitplans an, der die Aufträge enthält.</span><span class="sxs-lookup"><span data-stu-id="94dfe-145">Specifies the ID of the job schedule which contains the jobs.</span></span>

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

### <span data-ttu-id="94dfe-146">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="94dfe-146">-MaxCount</span></span>
<span data-ttu-id="94dfe-147">Gibt die maximale Anzahl von Aufträgen an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="94dfe-147">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="94dfe-148">Wenn Sie den Wert 0 (null) oder weniger angeben, verwendet das Cmdlet keine Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="94dfe-148">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="94dfe-149">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="94dfe-149">The default value is 1000.</span></span>

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

### <span data-ttu-id="94dfe-150">-Wählen Sie</span><span class="sxs-lookup"><span data-stu-id="94dfe-150">-Select</span></span>
<span data-ttu-id="94dfe-151">Gibt eine OData-Auswahl Klausel an.</span><span class="sxs-lookup"><span data-stu-id="94dfe-151">Specifies an OData select clause.</span></span>
<span data-ttu-id="94dfe-152">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften und nicht alle Objekteigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="94dfe-152">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="94dfe-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94dfe-153">CommonParameters</span></span>
<span data-ttu-id="94dfe-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94dfe-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94dfe-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94dfe-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94dfe-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="94dfe-156">INPUTS</span></span>

### <span data-ttu-id="94dfe-157">System. String</span><span class="sxs-lookup"><span data-stu-id="94dfe-157">System.String</span></span>

### <span data-ttu-id="94dfe-158">Microsoft.Azure.Commands.Batch. Models. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="94dfe-158">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="94dfe-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="94dfe-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="94dfe-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="94dfe-160">OUTPUTS</span></span>

### <span data-ttu-id="94dfe-161">Microsoft.Azure.Commands.Batch. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="94dfe-161">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

## <span data-ttu-id="94dfe-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="94dfe-162">NOTES</span></span>

## <span data-ttu-id="94dfe-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="94dfe-163">RELATED LINKS</span></span>

[<span data-ttu-id="94dfe-164">Deaktivieren-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="94dfe-164">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="94dfe-165">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="94dfe-165">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="94dfe-166">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="94dfe-166">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="94dfe-167">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="94dfe-167">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="94dfe-168">Neu – AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="94dfe-168">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="94dfe-169">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="94dfe-169">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="94dfe-170">Stopp-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="94dfe-170">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="94dfe-171">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="94dfe-171">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


