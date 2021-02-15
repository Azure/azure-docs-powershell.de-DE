---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
ms.openlocfilehash: bf1a70dc697366099f1949878e81a25bd3adb0fa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164321"
---
# <span data-ttu-id="b8b45-101">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="b8b45-101">Get-AzBatchTask</span></span>

## <span data-ttu-id="b8b45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8b45-102">SYNOPSIS</span></span>
<span data-ttu-id="b8b45-103">Ruft die Stapelaufgaben für einen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="b8b45-103">Gets the Batch tasks for a job.</span></span>

## <span data-ttu-id="b8b45-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8b45-104">SYNTAX</span></span>

### <span data-ttu-id="b8b45-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="b8b45-105">ODataFilter (Default)</span></span>
```
Get-AzBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8b45-106">ID</span><span class="sxs-lookup"><span data-stu-id="b8b45-106">Id</span></span>
```
Get-AzBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8b45-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="b8b45-107">ParentObject</span></span>
```
Get-AzBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8b45-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8b45-108">DESCRIPTION</span></span>
<span data-ttu-id="b8b45-109">Das **Cmdlet "Get-AzBatchTask"** ruft Azure -Batchaufgaben für einen Stapelauftrag ab.</span><span class="sxs-lookup"><span data-stu-id="b8b45-109">The **Get-AzBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="b8b45-110">Geben Sie einen Auftrag entweder mit dem *Parameter "JobId"* oder mit dem *Parameter "Job"* an.</span><span class="sxs-lookup"><span data-stu-id="b8b45-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="b8b45-111">Um eine einzelne Aufgabe zu erhalten, geben Sie den *Parameter "Id"* an.</span><span class="sxs-lookup"><span data-stu-id="b8b45-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="b8b45-112">Sie können den *Filterparameter angeben,* um die Aufgaben zu erhalten, die einem Open Data Protocol (OData)-Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b8b45-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="b8b45-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b8b45-113">EXAMPLES</span></span>

### <span data-ttu-id="b8b45-114">Beispiel 1: Erhalten einer Aufgabe nach ID</span><span class="sxs-lookup"><span data-stu-id="b8b45-114">Example 1: Get a task by ID</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job01" -Id "Task03" -BatchContext $Context
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

<span data-ttu-id="b8b45-115">Dieser Befehl ruft den Vorgang mit der ID Task03 unter Auftrag01 ab.</span><span class="sxs-lookup"><span data-stu-id="b8b45-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="b8b45-116">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der Variablen einen Kontext $Context zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="b8b45-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="b8b45-117">Beispiel 2: Alle abgeschlossenen Aufgaben aus einem bestimmten Auftrag erhalten</span><span class="sxs-lookup"><span data-stu-id="b8b45-117">Example 2: Get all completed tasks from a specified job</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job02" -Filter "state eq 'completed'" -BatchContext $Context
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

<span data-ttu-id="b8b45-118">Dieser Befehl ruft die abgeschlossenen Aufgaben von dem Auftrag ab, der die ID "Job02" hat.</span><span class="sxs-lookup"><span data-stu-id="b8b45-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="b8b45-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8b45-119">PARAMETERS</span></span>

### <span data-ttu-id="b8b45-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b8b45-120">-BatchContext</span></span>
<span data-ttu-id="b8b45-121">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8b45-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b8b45-122">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8b45-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b8b45-123">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b8b45-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b8b45-124">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8b45-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b8b45-125">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b8b45-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b8b45-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8b45-126">-DefaultProfile</span></span>
<span data-ttu-id="b8b45-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8b45-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8b45-128">-Expand</span><span class="sxs-lookup"><span data-stu-id="b8b45-128">-Expand</span></span>
<span data-ttu-id="b8b45-129">Gibt eine OData-Erweiterungsklausel an.</span><span class="sxs-lookup"><span data-stu-id="b8b45-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="b8b45-130">Geben Sie einen Wert für diesen Parameter an, um zugeordnete Entitäten der zu erhaltende Hauptentität zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b8b45-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

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

### <span data-ttu-id="b8b45-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="b8b45-131">-Filter</span></span>
<span data-ttu-id="b8b45-132">Gibt eine OData-Filterklausel für Vorgänge an.</span><span class="sxs-lookup"><span data-stu-id="b8b45-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="b8b45-133">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Aufgaben für das Batchkonto oder den Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="b8b45-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

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

### <span data-ttu-id="b8b45-134">-ID</span><span class="sxs-lookup"><span data-stu-id="b8b45-134">-Id</span></span>
<span data-ttu-id="b8b45-135">Gibt die ID der Aufgabe an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="b8b45-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="b8b45-136">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="b8b45-136">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="b8b45-137">-Job</span><span class="sxs-lookup"><span data-stu-id="b8b45-137">-Job</span></span>
<span data-ttu-id="b8b45-138">Gibt den Auftrag an, der Aufgaben enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="b8b45-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="b8b45-139">Um ein **"PSCloudJob"-Objekt** zu erhalten, verwenden Sie das Get-AzBatchJob-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8b45-139">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="b8b45-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="b8b45-140">-JobId</span></span>
<span data-ttu-id="b8b45-141">Gibt die ID des Auftrags an, der die Aufgaben enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="b8b45-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b8b45-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b8b45-142">-MaxCount</span></span>
<span data-ttu-id="b8b45-143">Gibt die maximale Anzahl der zurückzukehrenden Vorgänge an.</span><span class="sxs-lookup"><span data-stu-id="b8b45-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="b8b45-144">Wenn Sie einen Wert von Null (0) oder kleiner angeben, wird für das Cmdlet keine Obergrenze verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8b45-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="b8b45-145">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="b8b45-145">The default value is 1000.</span></span>

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

### <span data-ttu-id="b8b45-146">-Select</span><span class="sxs-lookup"><span data-stu-id="b8b45-146">-Select</span></span>
<span data-ttu-id="b8b45-147">Gibt eine OData-Auswahlklausel an.</span><span class="sxs-lookup"><span data-stu-id="b8b45-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="b8b45-148">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften und nicht alle Objekteigenschaften zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b8b45-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="b8b45-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8b45-149">CommonParameters</span></span>
<span data-ttu-id="b8b45-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8b45-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8b45-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8b45-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8b45-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b8b45-152">INPUTS</span></span>

### <span data-ttu-id="b8b45-153">System.String</span><span class="sxs-lookup"><span data-stu-id="b8b45-153">System.String</span></span>

### <span data-ttu-id="b8b45-154">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="b8b45-154">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="b8b45-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b8b45-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b8b45-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b8b45-156">OUTPUTS</span></span>

### <span data-ttu-id="b8b45-157">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="b8b45-157">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

## <span data-ttu-id="b8b45-158">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b8b45-158">NOTES</span></span>

## <span data-ttu-id="b8b45-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b8b45-159">RELATED LINKS</span></span>

[<span data-ttu-id="b8b45-160">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b8b45-160">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b8b45-161">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b8b45-161">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="b8b45-162">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="b8b45-162">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="b8b45-163">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="b8b45-163">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="b8b45-164">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="b8b45-164">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="b8b45-165">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="b8b45-165">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
