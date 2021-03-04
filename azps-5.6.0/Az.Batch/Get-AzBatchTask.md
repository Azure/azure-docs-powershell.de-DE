---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
ms.openlocfilehash: 214ee3b030757da9acf632b2768a94b1ab026cc6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948976"
---
# <span data-ttu-id="7a109-101">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="7a109-101">Get-AzBatchTask</span></span>

## <span data-ttu-id="7a109-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a109-102">SYNOPSIS</span></span>
<span data-ttu-id="7a109-103">Ruft die Batchaufgaben für einen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="7a109-103">Gets the Batch tasks for a job.</span></span>

## <span data-ttu-id="7a109-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a109-104">SYNTAX</span></span>

### <span data-ttu-id="7a109-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="7a109-105">ODataFilter (Default)</span></span>
```
Get-AzBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a109-106">ID</span><span class="sxs-lookup"><span data-stu-id="7a109-106">Id</span></span>
```
Get-AzBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a109-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="7a109-107">ParentObject</span></span>
```
Get-AzBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a109-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a109-108">DESCRIPTION</span></span>
<span data-ttu-id="7a109-109">Das **Get-AzBatchTask-Cmdlet** ruft Azure Batch-Aufgaben für einen Batchauftrag ab.</span><span class="sxs-lookup"><span data-stu-id="7a109-109">The **Get-AzBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="7a109-110">Geben Sie einen Auftrag entweder über den *Parameter "JobId"* oder den *Parameter "Auftrag"* an.</span><span class="sxs-lookup"><span data-stu-id="7a109-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="7a109-111">Um eine einzelne Aufgabe zu erhalten, geben Sie den *Parameter Id* an.</span><span class="sxs-lookup"><span data-stu-id="7a109-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="7a109-112">Sie können den Parameter *Filter angeben,* um die Aufgaben zu erhalten, die einem OData-Filter (Open Data Protocol) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7a109-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="7a109-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7a109-113">EXAMPLES</span></span>

### <span data-ttu-id="7a109-114">Beispiel 1: Erhalten einer Aufgabe nach ID</span><span class="sxs-lookup"><span data-stu-id="7a109-114">Example 1: Get a task by ID</span></span>
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

<span data-ttu-id="7a109-115">Dieser Befehl ruft die Aufgabe mit der ID Task03 unter Job01 ab.</span><span class="sxs-lookup"><span data-stu-id="7a109-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="7a109-116">Verwenden Sie Get-AzBatchAccountKey-Cmdlet, um der Variablen $Context Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="7a109-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="7a109-117">Beispiel 2: Alle abgeschlossenen Vorgänge aus einem angegebenen Auftrag erhalten</span><span class="sxs-lookup"><span data-stu-id="7a109-117">Example 2: Get all completed tasks from a specified job</span></span>
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

<span data-ttu-id="7a109-118">Dieser Befehl ruft die abgeschlossenen Aufgaben aus dem Auftrag ab, der die ID Job02 hat.</span><span class="sxs-lookup"><span data-stu-id="7a109-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="7a109-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7a109-119">PARAMETERS</span></span>

### <span data-ttu-id="7a109-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7a109-120">-BatchContext</span></span>
<span data-ttu-id="7a109-121">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7a109-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7a109-122">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a109-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7a109-123">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7a109-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7a109-124">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a109-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7a109-125">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="7a109-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7a109-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a109-126">-DefaultProfile</span></span>
<span data-ttu-id="7a109-127">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a109-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a109-128">-Erweitern</span><span class="sxs-lookup"><span data-stu-id="7a109-128">-Expand</span></span>
<span data-ttu-id="7a109-129">Gibt eine OData-Erweiterungsklausel an.</span><span class="sxs-lookup"><span data-stu-id="7a109-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="7a109-130">Geben Sie einen Wert für diesen Parameter an, um zugeordnete Entitäten der Hauptentität zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7a109-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

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

### <span data-ttu-id="7a109-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="7a109-131">-Filter</span></span>
<span data-ttu-id="7a109-132">Gibt eine OData-Filterklausel für Aufgaben an.</span><span class="sxs-lookup"><span data-stu-id="7a109-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="7a109-133">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Vorgänge für das Batchkonto oder den Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="7a109-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

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

### <span data-ttu-id="7a109-134">-ID</span><span class="sxs-lookup"><span data-stu-id="7a109-134">-Id</span></span>
<span data-ttu-id="7a109-135">Gibt die ID der Aufgabe an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="7a109-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="7a109-136">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="7a109-136">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="7a109-137">-Job</span><span class="sxs-lookup"><span data-stu-id="7a109-137">-Job</span></span>
<span data-ttu-id="7a109-138">Gibt den Auftrag an, der Aufgaben enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="7a109-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="7a109-139">Um ein **PSCloudJob-Objekt** zu erhalten, verwenden Sie das Get-AzBatchJob Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a109-139">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="7a109-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="7a109-140">-JobId</span></span>
<span data-ttu-id="7a109-141">Gibt die ID des Auftrags an, der die Aufgaben enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="7a109-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7a109-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="7a109-142">-MaxCount</span></span>
<span data-ttu-id="7a109-143">Gibt die maximale Anzahl von Zurücksendaufgaben an.</span><span class="sxs-lookup"><span data-stu-id="7a109-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="7a109-144">Wenn Sie einen Wert von Null (0) oder kleiner angeben, wird für das Cmdlet keine Obergrenze verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a109-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="7a109-145">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="7a109-145">The default value is 1000.</span></span>

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

### <span data-ttu-id="7a109-146">-Select</span><span class="sxs-lookup"><span data-stu-id="7a109-146">-Select</span></span>
<span data-ttu-id="7a109-147">Gibt eine OData-Auswahlklausel an.</span><span class="sxs-lookup"><span data-stu-id="7a109-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="7a109-148">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften anstelle aller Objekteigenschaften zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7a109-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="7a109-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a109-149">CommonParameters</span></span>
<span data-ttu-id="7a109-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a109-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a109-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a109-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a109-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7a109-152">INPUTS</span></span>

### <span data-ttu-id="7a109-153">System.String</span><span class="sxs-lookup"><span data-stu-id="7a109-153">System.String</span></span>

### <span data-ttu-id="7a109-154">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="7a109-154">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="7a109-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7a109-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7a109-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7a109-156">OUTPUTS</span></span>

### <span data-ttu-id="7a109-157">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="7a109-157">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

## <span data-ttu-id="7a109-158">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7a109-158">NOTES</span></span>

## <span data-ttu-id="7a109-159">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7a109-159">RELATED LINKS</span></span>

[<span data-ttu-id="7a109-160">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="7a109-160">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="7a109-161">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="7a109-161">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="7a109-162">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="7a109-162">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="7a109-163">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="7a109-163">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="7a109-164">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="7a109-164">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="7a109-165">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7a109-165">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
