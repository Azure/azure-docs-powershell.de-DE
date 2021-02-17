---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
ms.openlocfilehash: 9daa0e1a1b1bc6ec980f3c3f65d79840648fdaf8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171540"
---
# <span data-ttu-id="53a26-101">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="53a26-101">Get-AzBatchJobSchedule</span></span>

## <span data-ttu-id="53a26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53a26-102">SYNOPSIS</span></span>
<span data-ttu-id="53a26-103">Ruft Stapelauftragszeitpläne ab.</span><span class="sxs-lookup"><span data-stu-id="53a26-103">Gets Batch job schedules.</span></span>

## <span data-ttu-id="53a26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53a26-104">SYNTAX</span></span>

### <span data-ttu-id="53a26-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="53a26-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53a26-106">ID</span><span class="sxs-lookup"><span data-stu-id="53a26-106">Id</span></span>
```
Get-AzBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53a26-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53a26-107">DESCRIPTION</span></span>
<span data-ttu-id="53a26-108">Das **Cmdlet "Get-AzBatchJobSchedule"** ruft Projektzeitpläne für den Azure Batch ab, die vom Parameter *"BatchContext" angegeben* werden.</span><span class="sxs-lookup"><span data-stu-id="53a26-108">The **Get-AzBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="53a26-109">Geben Sie eine ID an, um einen einzelnen Auftragszeitplan zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="53a26-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="53a26-110">Geben Sie den *Parameter "Filter"* an, um die Auftragszeitpläne zu erhalten, die einem Open Data Protocol (OData)-Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="53a26-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="53a26-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="53a26-111">EXAMPLES</span></span>

### <span data-ttu-id="53a26-112">Beispiel 1: Erhalten eines Auftragsplans durch Angeben einer ID</span><span class="sxs-lookup"><span data-stu-id="53a26-112">Example 1: Get a job schedule by specifying an ID</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule23" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 :
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    :
PreviousState               : Invalid
PreviousStateTransitionTime :
Schedule                    :
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23
```

<span data-ttu-id="53a26-113">Dieser Befehl ruft den Auftragszeitplan mit der ID "JobSchedule23" ab.</span><span class="sxs-lookup"><span data-stu-id="53a26-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="53a26-114">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der Variablen einen Kontext $Context zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="53a26-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="53a26-115">Beispiel 2: Erhalten von Stellenplänen mithilfe eines Filters</span><span class="sxs-lookup"><span data-stu-id="53a26-115">Example 2: Get job schedules by using a filter</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Filter "startswith(id,'Job')" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 :
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    :
PreviousState               : Invalid
PreviousStateTransitionTime :
Schedule                    :
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23

CreationTime                : 7/26/2015 5:39:33 PM
DisplayName                 :
ETag                        : 0x8D295E12B1084B4
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule26
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/26/2015 5:39:33 PM
Metadata                    :
PreviousState               : Invalid
PreviousStateTransitionTime :
Schedule                    :
State                       : Active
StateTransitionTime         : 7/26/2015 5:39:33 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule26
```

<span data-ttu-id="53a26-116">Dieser Befehl ruft alle Auftragsterminpläne ab, die IDs haben, die mit "Auftrag" beginnen, indem der Parameter *"Filter" angegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="53a26-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="53a26-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53a26-117">PARAMETERS</span></span>

### <span data-ttu-id="53a26-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="53a26-118">-BatchContext</span></span>
<span data-ttu-id="53a26-119">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="53a26-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="53a26-120">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="53a26-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="53a26-121">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="53a26-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="53a26-122">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="53a26-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="53a26-123">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="53a26-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="53a26-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a26-124">-DefaultProfile</span></span>
<span data-ttu-id="53a26-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="53a26-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53a26-126">-Expand</span><span class="sxs-lookup"><span data-stu-id="53a26-126">-Expand</span></span>
<span data-ttu-id="53a26-127">Gibt eine Open Data Protocol (OData)-Erweiterungsklausel an.</span><span class="sxs-lookup"><span data-stu-id="53a26-127">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="53a26-128">Geben Sie einen Wert für diesen Parameter an, um zugeordnete Entitäten der erhaltenen Hauptentität zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="53a26-128">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="53a26-129">-Filter</span><span class="sxs-lookup"><span data-stu-id="53a26-129">-Filter</span></span>
<span data-ttu-id="53a26-130">Gibt eine OData-Filterklausel an.</span><span class="sxs-lookup"><span data-stu-id="53a26-130">Specifies an OData filter clause.</span></span>
<span data-ttu-id="53a26-131">Dieses Cmdlet gibt Auftragsterminpläne zurück, die dem von diesem Parameter angegebenen Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="53a26-131">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="53a26-132">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Auftragsterminpläne für den Kontext "Batch" zurück.</span><span class="sxs-lookup"><span data-stu-id="53a26-132">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53a26-133">-ID</span><span class="sxs-lookup"><span data-stu-id="53a26-133">-Id</span></span>
<span data-ttu-id="53a26-134">Gibt die ID des Auftragsplans an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="53a26-134">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="53a26-135">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="53a26-135">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53a26-136">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="53a26-136">-MaxCount</span></span>
<span data-ttu-id="53a26-137">Gibt die maximale Anzahl der zurückzukehrenden Stellenpläne an.</span><span class="sxs-lookup"><span data-stu-id="53a26-137">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="53a26-138">Wenn Sie einen Wert von Null (0) oder kleiner angeben, wird für das Cmdlet keine Obergrenze verwendet.</span><span class="sxs-lookup"><span data-stu-id="53a26-138">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="53a26-139">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="53a26-139">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53a26-140">-Select</span><span class="sxs-lookup"><span data-stu-id="53a26-140">-Select</span></span>
<span data-ttu-id="53a26-141">Gibt eine OData-Auswahlklausel an.</span><span class="sxs-lookup"><span data-stu-id="53a26-141">Specifies an OData select clause.</span></span>
<span data-ttu-id="53a26-142">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften und nicht alle Objekteigenschaften zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="53a26-142">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="53a26-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a26-143">CommonParameters</span></span>
<span data-ttu-id="53a26-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53a26-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a26-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53a26-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a26-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="53a26-146">INPUTS</span></span>

### <span data-ttu-id="53a26-147">System.String</span><span class="sxs-lookup"><span data-stu-id="53a26-147">System.String</span></span>

### <span data-ttu-id="53a26-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="53a26-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="53a26-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="53a26-149">OUTPUTS</span></span>

### <span data-ttu-id="53a26-150">Microsoft.Azure.Commands.Batch. Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="53a26-150">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

## <span data-ttu-id="53a26-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="53a26-151">NOTES</span></span>

## <span data-ttu-id="53a26-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="53a26-152">RELATED LINKS</span></span>

[<span data-ttu-id="53a26-153">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="53a26-153">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="53a26-154">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="53a26-154">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="53a26-155">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="53a26-155">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="53a26-156">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="53a26-156">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="53a26-157">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="53a26-157">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="53a26-158">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="53a26-158">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="53a26-159">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="53a26-159">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
