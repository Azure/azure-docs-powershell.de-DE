---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
ms.openlocfilehash: c2aa673b9cd0f8cccc3f1a8721313f5a3236270d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497141"
---
# <span data-ttu-id="5e240-101">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5e240-101">Get-AzureBatchJob</span></span>

## <span data-ttu-id="5e240-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e240-102">SYNOPSIS</span></span>
<span data-ttu-id="5e240-103">Ruft Stapelverarbeitungsaufträge für ein Stapelverarbeitungs Konto oder einen Auftragszeitplan ab.</span><span class="sxs-lookup"><span data-stu-id="5e240-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e240-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e240-104">SYNTAX</span></span>

### <span data-ttu-id="5e240-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e240-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e240-106">ID</span><span class="sxs-lookup"><span data-stu-id="5e240-106">Id</span></span>
```
Get-AzureBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e240-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="5e240-107">ParentObject</span></span>
```
Get-AzureBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e240-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e240-108">DESCRIPTION</span></span>
<span data-ttu-id="5e240-109">Das Cmdlet " **Get-AzureBatchJob** " Ruft die Azure-Stapelverarbeitungsaufträge für das vom *BatchAccountContext* -Parameter angegebene Batch Konto ab.</span><span class="sxs-lookup"><span data-stu-id="5e240-109">The **Get-AzureBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="5e240-110">Sie können den *ID-* Parameter verwenden, um einen einzelnen Auftrag zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5e240-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="5e240-111">Sie können den *Filter* -Parameter verwenden, um die Aufträge abzurufen, die einem OData-Filter (Open Data Protocol) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5e240-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="5e240-112">Wenn Sie eine Auftragsplan-ID oder eine **PSCloudJobSchedule** -Instanz angeben, gibt dieses Cmdlet nur die Aufträge für diesen Auftragszeitplan zurück.</span><span class="sxs-lookup"><span data-stu-id="5e240-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="5e240-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e240-113">EXAMPLES</span></span>

### <span data-ttu-id="5e240-114">Beispiel 1: Abrufen eines stapelverarbeitungsauftrags nach ID</span><span class="sxs-lookup"><span data-stu-id="5e240-114">Example 1: Get a Batch job by ID</span></span>
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

<span data-ttu-id="5e240-115">Dieser Befehl ruft den Auftrag ab, der die ID Job01.</span><span class="sxs-lookup"><span data-stu-id="5e240-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="5e240-116">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="5e240-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="5e240-117">Beispiel 2: Abrufen aller aktiven Aufträge für einen Auftragszeitplan</span><span class="sxs-lookup"><span data-stu-id="5e240-117">Example 2: Get all active jobs for a job schedule</span></span>
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

<span data-ttu-id="5e240-118">Dieser Befehl ruft die aktiven Aufträge für den Auftragszeitplan ab, der die ID JobSchedule27.</span><span class="sxs-lookup"><span data-stu-id="5e240-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="5e240-119">Beispiel 3: Ruft alle Aufträge unter einem Auftragszeitplan mithilfe der Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="5e240-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
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

<span data-ttu-id="5e240-120">Dieser Befehl ruft den Auftragszeitplan mit der ID-JobSchedule27 mithilfe des Get-AzureBatchJobSchedule-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="5e240-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzureBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="5e240-121">Der Befehl übergibt diesen Auftragszeitplan mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e240-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5e240-122">Der Befehl ruft alle Aufträge für diesen Auftragszeitplan ab.</span><span class="sxs-lookup"><span data-stu-id="5e240-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="5e240-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e240-123">PARAMETERS</span></span>

### <span data-ttu-id="5e240-124">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="5e240-124">-BatchContext</span></span>
<span data-ttu-id="5e240-125">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="5e240-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5e240-126">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e240-126">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="5e240-127">– Erweitern</span><span class="sxs-lookup"><span data-stu-id="5e240-127">-Expand</span></span>
<span data-ttu-id="5e240-128">Gibt eine Open Data Protocol (OData) expand-Klausel an.</span><span class="sxs-lookup"><span data-stu-id="5e240-128">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="5e240-129">Geben Sie einen Wert für diesen Parameter an, um zugeordnete Entitäten der Haupt Entität abzurufen, die Sie erhalten.</span><span class="sxs-lookup"><span data-stu-id="5e240-129">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="5e240-130">-Filter</span><span class="sxs-lookup"><span data-stu-id="5e240-130">-Filter</span></span>
<span data-ttu-id="5e240-131">Gibt eine OData-Filterklausel für Jobs an.</span><span class="sxs-lookup"><span data-stu-id="5e240-131">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="5e240-132">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Aufträge für das Stapelverarbeitungs Konto oder den Auftragszeitplan zurück.</span><span class="sxs-lookup"><span data-stu-id="5e240-132">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="5e240-133">-ID</span><span class="sxs-lookup"><span data-stu-id="5e240-133">-Id</span></span>
<span data-ttu-id="5e240-134">Gibt die ID des Auftrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5e240-134">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="5e240-135">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="5e240-135">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="5e240-136">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="5e240-136">-JobSchedule</span></span>
<span data-ttu-id="5e240-137">Gibt ein **PSCloudJobSchedule** -Objekt an, das den Auftragszeitplan darstellt, der die Aufträge enthält.</span><span class="sxs-lookup"><span data-stu-id="5e240-137">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="5e240-138">Verwenden Sie das Get-AzureBatchJobSchedule-Cmdlet, um ein **PSCloudJobSchedule** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5e240-138">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="5e240-139">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="5e240-139">-JobScheduleId</span></span>
<span data-ttu-id="5e240-140">Gibt die ID des Auftragszeitplans an, der die Aufträge enthält.</span><span class="sxs-lookup"><span data-stu-id="5e240-140">Specifies the ID of the job schedule which contains the jobs.</span></span>

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

### <span data-ttu-id="5e240-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="5e240-141">-MaxCount</span></span>
<span data-ttu-id="5e240-142">Gibt die maximale Anzahl von Aufträgen an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5e240-142">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="5e240-143">Wenn Sie den Wert 0 (null) oder weniger angeben, verwendet das Cmdlet keine Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="5e240-143">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="5e240-144">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="5e240-144">The default value is 1000.</span></span>

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

### <span data-ttu-id="5e240-145">-Wählen Sie</span><span class="sxs-lookup"><span data-stu-id="5e240-145">-Select</span></span>
<span data-ttu-id="5e240-146">Gibt eine OData-Auswahl Klausel an.</span><span class="sxs-lookup"><span data-stu-id="5e240-146">Specifies an OData select clause.</span></span>
<span data-ttu-id="5e240-147">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften und nicht alle Objekteigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5e240-147">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="5e240-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e240-148">-DefaultProfile</span></span>
<span data-ttu-id="5e240-149">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e240-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e240-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e240-150">CommonParameters</span></span>
<span data-ttu-id="5e240-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e240-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e240-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e240-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e240-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e240-153">INPUTS</span></span>

### <span data-ttu-id="5e240-154">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5e240-154">BatchAccountContext</span></span>
<span data-ttu-id="5e240-155">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5e240-155">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="5e240-156">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5e240-156">PSCloudJobSchedule</span></span>
<span data-ttu-id="5e240-157">Der Parameter "JobSchedule" akzeptiert den Wert vom Typ "PSCloudJobSchedule" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5e240-157">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="5e240-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e240-158">OUTPUTS</span></span>

### <span data-ttu-id="5e240-159">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="5e240-159">PSCloudJob</span></span>

## <span data-ttu-id="5e240-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e240-160">NOTES</span></span>

## <span data-ttu-id="5e240-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e240-161">RELATED LINKS</span></span>

[<span data-ttu-id="5e240-162">Deaktivieren-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5e240-162">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="5e240-163">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5e240-163">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="5e240-164">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5e240-164">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5e240-165">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5e240-165">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="5e240-166">Neu – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5e240-166">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="5e240-167">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5e240-167">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="5e240-168">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5e240-168">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="5e240-169">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="5e240-169">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


