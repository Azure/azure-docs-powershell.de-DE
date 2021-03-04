---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
ms.openlocfilehash: 0d33ce7e41fb8058acb36a4668eeb337d54f187e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929104"
---
# <span data-ttu-id="ba269-101">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba269-101">Get-AzBatchJobSchedule</span></span>

## <span data-ttu-id="ba269-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba269-102">SYNOPSIS</span></span>
<span data-ttu-id="ba269-103">Ruft Stapelverarbeitungszeitpläne ab.</span><span class="sxs-lookup"><span data-stu-id="ba269-103">Gets Batch job schedules.</span></span>

## <span data-ttu-id="ba269-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba269-104">SYNTAX</span></span>

### <span data-ttu-id="ba269-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="ba269-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba269-106">ID</span><span class="sxs-lookup"><span data-stu-id="ba269-106">Id</span></span>
```
Get-AzBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba269-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba269-107">DESCRIPTION</span></span>
<span data-ttu-id="ba269-108">Das **Get-AzBatchJobSchedule-Cmdlet** ruft Azure Batch-Auftragszeitpläne für das batch-Konto ab, das vom *Parameter BatchContext angegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="ba269-108">The **Get-AzBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="ba269-109">Geben Sie eine ID an, um einen einzelnen Auftragszeitplan zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ba269-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="ba269-110">Geben Sie den *Parameter Filter* an, um die Auftragszeitpläne zu erhalten, die einem OData-Filter (Open Data Protocol) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ba269-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="ba269-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ba269-111">EXAMPLES</span></span>

### <span data-ttu-id="ba269-112">Beispiel 1: Erhalten eines Auftragszeitplans durch Angeben einer ID</span><span class="sxs-lookup"><span data-stu-id="ba269-112">Example 1: Get a job schedule by specifying an ID</span></span>
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

<span data-ttu-id="ba269-113">Dieser Befehl ruft den Auftragszeitplan ab, der die ID JobSchedule23 hat.</span><span class="sxs-lookup"><span data-stu-id="ba269-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="ba269-114">Verwenden Sie Get-AzBatchAccountKey-Cmdlet, um der Variablen $Context Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="ba269-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ba269-115">Beispiel 2: Erhalten von Terminplänen mithilfe eines Filters</span><span class="sxs-lookup"><span data-stu-id="ba269-115">Example 2: Get job schedules by using a filter</span></span>
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

<span data-ttu-id="ba269-116">Dieser Befehl ruft alle Auftragszeitpläne ab, die IDs haben, die mit Auftrag beginnen, indem sie den Parameter *Filter* angeben.</span><span class="sxs-lookup"><span data-stu-id="ba269-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="ba269-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ba269-117">PARAMETERS</span></span>

### <span data-ttu-id="ba269-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ba269-118">-BatchContext</span></span>
<span data-ttu-id="ba269-119">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ba269-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ba269-120">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba269-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ba269-121">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ba269-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ba269-122">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba269-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ba269-123">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="ba269-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ba269-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba269-124">-DefaultProfile</span></span>
<span data-ttu-id="ba269-125">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba269-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba269-126">-Erweitern</span><span class="sxs-lookup"><span data-stu-id="ba269-126">-Expand</span></span>
<span data-ttu-id="ba269-127">Gibt eine Open Data Protocol (OData)-Erweiterungsklausel an.</span><span class="sxs-lookup"><span data-stu-id="ba269-127">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="ba269-128">Geben Sie einen Wert für diesen Parameter an, um zugeordnete Entitäten der Hauptentität zu erhalten, die Sie erhalten.</span><span class="sxs-lookup"><span data-stu-id="ba269-128">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="ba269-129">-Filter</span><span class="sxs-lookup"><span data-stu-id="ba269-129">-Filter</span></span>
<span data-ttu-id="ba269-130">Gibt eine OData-Filterklausel an.</span><span class="sxs-lookup"><span data-stu-id="ba269-130">Specifies an OData filter clause.</span></span>
<span data-ttu-id="ba269-131">Dieses Cmdlet gibt Auftragszeitpläne zurück, die dem filter entsprechen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ba269-131">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="ba269-132">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Auftragszeitpläne für den Batchkontext zurück.</span><span class="sxs-lookup"><span data-stu-id="ba269-132">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

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

### <span data-ttu-id="ba269-133">-ID</span><span class="sxs-lookup"><span data-stu-id="ba269-133">-Id</span></span>
<span data-ttu-id="ba269-134">Gibt die ID des Auftragszeitplans an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ba269-134">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="ba269-135">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="ba269-135">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="ba269-136">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ba269-136">-MaxCount</span></span>
<span data-ttu-id="ba269-137">Gibt die maximale Anzahl von Auftragsplänen an, die zurückzukehren sind.</span><span class="sxs-lookup"><span data-stu-id="ba269-137">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="ba269-138">Wenn Sie einen Wert von Null (0) oder kleiner angeben, wird für das Cmdlet keine Obergrenze verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba269-138">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="ba269-139">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="ba269-139">The default value is 1000.</span></span>

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

### <span data-ttu-id="ba269-140">-Select</span><span class="sxs-lookup"><span data-stu-id="ba269-140">-Select</span></span>
<span data-ttu-id="ba269-141">Gibt eine OData-Auswahlklausel an.</span><span class="sxs-lookup"><span data-stu-id="ba269-141">Specifies an OData select clause.</span></span>
<span data-ttu-id="ba269-142">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften anstelle aller Objekteigenschaften zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ba269-142">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="ba269-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba269-143">CommonParameters</span></span>
<span data-ttu-id="ba269-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba269-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba269-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba269-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba269-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ba269-146">INPUTS</span></span>

### <span data-ttu-id="ba269-147">System.String</span><span class="sxs-lookup"><span data-stu-id="ba269-147">System.String</span></span>

### <span data-ttu-id="ba269-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ba269-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ba269-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ba269-149">OUTPUTS</span></span>

### <span data-ttu-id="ba269-150">Microsoft.Azure.Commands.Batch. Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba269-150">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

## <span data-ttu-id="ba269-151">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ba269-151">NOTES</span></span>

## <span data-ttu-id="ba269-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ba269-152">RELATED LINKS</span></span>

[<span data-ttu-id="ba269-153">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba269-153">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="ba269-154">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba269-154">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="ba269-155">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ba269-155">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ba269-156">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba269-156">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="ba269-157">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba269-157">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="ba269-158">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba269-158">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="ba269-159">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="ba269-159">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
