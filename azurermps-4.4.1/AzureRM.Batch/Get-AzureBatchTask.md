---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
ms.openlocfilehash: fb01af87d28323e3e25c46868f94e892b835afc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502778"
---
# <span data-ttu-id="ef28f-101">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ef28f-101">Get-AzureBatchTask</span></span>

## <span data-ttu-id="ef28f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef28f-102">SYNOPSIS</span></span>
<span data-ttu-id="ef28f-103">Ruft die Stapelverarbeitungsaufgaben für einen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="ef28f-103">Gets the Batch tasks for a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef28f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef28f-104">SYNTAX</span></span>

### <span data-ttu-id="ef28f-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="ef28f-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef28f-106">ID</span><span class="sxs-lookup"><span data-stu-id="ef28f-106">Id</span></span>
```
Get-AzureBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef28f-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="ef28f-107">ParentObject</span></span>
```
Get-AzureBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef28f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef28f-108">DESCRIPTION</span></span>
<span data-ttu-id="ef28f-109">Das Cmdlet " **Get-AzureBatchTask** " ruft Azure-Batch Aufgaben für einen Stapelverarbeitungsauftrag ab.</span><span class="sxs-lookup"><span data-stu-id="ef28f-109">The **Get-AzureBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="ef28f-110">Geben Sie einen Auftrag entweder mit dem *JobID* -Parameter oder dem *Job* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="ef28f-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="ef28f-111">Um eine einzelne Aufgabe abzurufen, geben Sie den *ID-* Parameter an.</span><span class="sxs-lookup"><span data-stu-id="ef28f-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="ef28f-112">Sie können den *Filter* -Parameter angeben, um die Aufgaben abzurufen, die einem OData-Filter (Open Data Protocol) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ef28f-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="ef28f-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef28f-113">EXAMPLES</span></span>

### <span data-ttu-id="ef28f-114">Beispiel 1: Abrufen einer Aufgabe nach ID</span><span class="sxs-lookup"><span data-stu-id="ef28f-114">Example 1: Get a task by ID</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job01" -Id "Task03" -BatchContext $Context
AffinityInformation         : 
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 7/25/2015 11:24:52 PM
DisplayName                 : 
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task03
LastModified                : 7/25/2015 11:24:52 PM
PreviousState               : Running
PreviousStateTransitionTime : 7/25/2015 11:24:59 PM
ResourceFiles               : 
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 7/25/2015 11:24:59 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01/tasks/Task03
```

<span data-ttu-id="ef28f-115">Dieser Befehl ruft die Aufgabe mit der ID Task03 unter Job Job01.</span><span class="sxs-lookup"><span data-stu-id="ef28f-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="ef28f-116">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="ef28f-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ef28f-117">Beispiel 2: Abrufen aller abgeschlossenen Aufgaben aus einem angegebenen Auftrag</span><span class="sxs-lookup"><span data-stu-id="ef28f-117">Example 2: Get all completed tasks from a specified job</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job02" -Filter "state eq 'completed'" -BatchContext $Context
AffinityInformation         : 
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task17
LastModified                : 3/24/2015 10:21:51 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:22:00 PM
ResourceFiles               : 
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 3/24/2015 10:22:00 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task17

AffinityInformation         : 
CommandLine                 : cmd /c echo hello > newFile.txt
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task27
LastModified                : 3/24/2015 10:23:35 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:23:37 PM
ResourceFiles               : 
RunElevated                 : True
State                       : Completed
StateTransitionTime         : 3/24/2015 10:23:37 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task27
```

<span data-ttu-id="ef28f-118">Dieser Befehl ruft die erledigten Aufgaben aus dem Auftrag ab, der die ID Job02.</span><span class="sxs-lookup"><span data-stu-id="ef28f-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="ef28f-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef28f-119">PARAMETERS</span></span>

### <span data-ttu-id="ef28f-120">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="ef28f-120">-BatchContext</span></span>
<span data-ttu-id="ef28f-121">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef28f-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ef28f-122">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef28f-122">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="ef28f-123">– Erweitern</span><span class="sxs-lookup"><span data-stu-id="ef28f-123">-Expand</span></span>
<span data-ttu-id="ef28f-124">Gibt eine OData-expand-Klausel an.</span><span class="sxs-lookup"><span data-stu-id="ef28f-124">Specifies an OData expand clause.</span></span>
<span data-ttu-id="ef28f-125">Geben Sie einen Wert für diesen Parameter an, um zugeordnete Entitäten der Haupt Entität abzurufen, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ef28f-125">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

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

### <span data-ttu-id="ef28f-126">-Filter</span><span class="sxs-lookup"><span data-stu-id="ef28f-126">-Filter</span></span>
<span data-ttu-id="ef28f-127">Gibt eine OData-Filterklausel für Aufgaben an.</span><span class="sxs-lookup"><span data-stu-id="ef28f-127">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="ef28f-128">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Aufgaben für das Stapelverarbeitungs Konto oder den Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="ef28f-128">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

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

### <span data-ttu-id="ef28f-129">-ID</span><span class="sxs-lookup"><span data-stu-id="ef28f-129">-Id</span></span>
<span data-ttu-id="ef28f-130">Gibt die ID der Aufgabe an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ef28f-130">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="ef28f-131">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="ef28f-131">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef28f-132">-Job</span><span class="sxs-lookup"><span data-stu-id="ef28f-132">-Job</span></span>
<span data-ttu-id="ef28f-133">Gibt den Auftrag an, der Aufgaben enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ef28f-133">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="ef28f-134">Verwenden Sie das Get-AzureBatchJob-Cmdlet, um ein **PSCloudJob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ef28f-134">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="ef28f-135">-JobId</span><span class="sxs-lookup"><span data-stu-id="ef28f-135">-JobId</span></span>
<span data-ttu-id="ef28f-136">Gibt die ID des Auftrags an, der die Aufgaben enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ef28f-136">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef28f-137">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ef28f-137">-MaxCount</span></span>
<span data-ttu-id="ef28f-138">Gibt die maximale Anzahl von Aufgaben an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ef28f-138">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="ef28f-139">Wenn Sie den Wert 0 (null) oder weniger angeben, verwendet das Cmdlet keine Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="ef28f-139">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="ef28f-140">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="ef28f-140">The default value is 1000.</span></span>

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

### <span data-ttu-id="ef28f-141">-Wählen Sie</span><span class="sxs-lookup"><span data-stu-id="ef28f-141">-Select</span></span>
<span data-ttu-id="ef28f-142">Gibt eine OData-Auswahl Klausel an.</span><span class="sxs-lookup"><span data-stu-id="ef28f-142">Specifies an OData select clause.</span></span>
<span data-ttu-id="ef28f-143">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften und nicht alle Objekteigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ef28f-143">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="ef28f-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef28f-144">-DefaultProfile</span></span>
<span data-ttu-id="ef28f-145">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ef28f-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef28f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef28f-146">CommonParameters</span></span>
<span data-ttu-id="ef28f-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef28f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef28f-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef28f-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef28f-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef28f-149">INPUTS</span></span>

### <span data-ttu-id="ef28f-150">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ef28f-150">BatchAccountContext</span></span>
<span data-ttu-id="ef28f-151">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ef28f-151">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ef28f-152">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="ef28f-152">PSCloudJob</span></span>
<span data-ttu-id="ef28f-153">Der Parameter ' Job ' akzeptiert den Wert vom Typ ' PSCloudJob ' aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ef28f-153">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="ef28f-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef28f-154">OUTPUTS</span></span>

### <span data-ttu-id="ef28f-155">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="ef28f-155">PSCloudTask</span></span>

## <span data-ttu-id="ef28f-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef28f-156">NOTES</span></span>

## <span data-ttu-id="ef28f-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef28f-157">RELATED LINKS</span></span>

[<span data-ttu-id="ef28f-158">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ef28f-158">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ef28f-159">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ef28f-159">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="ef28f-160">Neu – AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ef28f-160">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="ef28f-161">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ef28f-161">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="ef28f-162">Stopp-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ef28f-162">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="ef28f-163">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="ef28f-163">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


