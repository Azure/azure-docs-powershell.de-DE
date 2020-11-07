---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
ms.openlocfilehash: 57c2a177b802ea7fbd152328bf57a81593c9b647
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847715"
---
# <span data-ttu-id="5d94b-101">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5d94b-101">Get-AzBatchJobSchedule</span></span>

## <span data-ttu-id="5d94b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d94b-102">SYNOPSIS</span></span>
<span data-ttu-id="5d94b-103">Ruft Stapel Auftragszeitpläne ab.</span><span class="sxs-lookup"><span data-stu-id="5d94b-103">Gets Batch job schedules.</span></span>

## <span data-ttu-id="5d94b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d94b-104">SYNTAX</span></span>

### <span data-ttu-id="5d94b-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="5d94b-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d94b-106">ID</span><span class="sxs-lookup"><span data-stu-id="5d94b-106">Id</span></span>
```
Get-AzBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d94b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d94b-107">DESCRIPTION</span></span>
<span data-ttu-id="5d94b-108">Das Cmdlet " **Get-AzBatchJobSchedule** " ruft Azure-batchauftrags Zeitpläne für das vom *batchcontext* -Parameter angegebene Batch Konto ab.</span><span class="sxs-lookup"><span data-stu-id="5d94b-108">The **Get-AzBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="5d94b-109">Geben Sie eine ID an, um einen einzelnen Auftragszeitplan abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5d94b-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="5d94b-110">Geben Sie den *Filter* -Parameter an, um die Auftragszeitpläne abzurufen, die einem Open Data Protocol (OData)-Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5d94b-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="5d94b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d94b-111">EXAMPLES</span></span>

### <span data-ttu-id="5d94b-112">Beispiel 1: Abrufen eines Auftragszeitplans durch Angabe einer ID</span><span class="sxs-lookup"><span data-stu-id="5d94b-112">Example 1: Get a job schedule by specifying an ID</span></span>
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

<span data-ttu-id="5d94b-113">Dieser Befehl ruft den Auftragszeitplan ab, der die ID JobSchedule23.</span><span class="sxs-lookup"><span data-stu-id="5d94b-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="5d94b-114">Verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="5d94b-114">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="5d94b-115">Beispiel 2: Abrufen von Auftrags Terminplänen mithilfe eines Filters</span><span class="sxs-lookup"><span data-stu-id="5d94b-115">Example 2: Get job schedules by using a filter</span></span>
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

<span data-ttu-id="5d94b-116">Dieser Befehl ruft alle Auftragszeitpläne ab, die IDs aufweisen, die mit Job beginnen, indem Sie den Parameter *Filter* angeben.</span><span class="sxs-lookup"><span data-stu-id="5d94b-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="5d94b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d94b-117">PARAMETERS</span></span>

### <span data-ttu-id="5d94b-118">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="5d94b-118">-BatchContext</span></span>
<span data-ttu-id="5d94b-119">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="5d94b-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5d94b-120">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5d94b-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5d94b-121">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5d94b-121">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5d94b-122">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="5d94b-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5d94b-123">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="5d94b-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5d94b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d94b-124">-DefaultProfile</span></span>
<span data-ttu-id="5d94b-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5d94b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d94b-126">– Erweitern</span><span class="sxs-lookup"><span data-stu-id="5d94b-126">-Expand</span></span>
<span data-ttu-id="5d94b-127">Gibt eine Open Data Protocol (OData) expand-Klausel an.</span><span class="sxs-lookup"><span data-stu-id="5d94b-127">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="5d94b-128">Geben Sie einen Wert für diesen Parameter an, um zugeordnete Entitäten der Haupt Entität abzurufen, die Sie erhalten.</span><span class="sxs-lookup"><span data-stu-id="5d94b-128">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="5d94b-129">-Filter</span><span class="sxs-lookup"><span data-stu-id="5d94b-129">-Filter</span></span>
<span data-ttu-id="5d94b-130">Gibt eine OData-Filterklausel an.</span><span class="sxs-lookup"><span data-stu-id="5d94b-130">Specifies an OData filter clause.</span></span>
<span data-ttu-id="5d94b-131">Dieses Cmdlet gibt Auftragszeitpläne zurück, die dem Filter entsprechen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5d94b-131">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="5d94b-132">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Auftragszeitpläne für den Batch Kontext zurück.</span><span class="sxs-lookup"><span data-stu-id="5d94b-132">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

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

### <span data-ttu-id="5d94b-133">-ID</span><span class="sxs-lookup"><span data-stu-id="5d94b-133">-Id</span></span>
<span data-ttu-id="5d94b-134">Gibt die ID des Auftragszeitplans an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5d94b-134">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="5d94b-135">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="5d94b-135">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="5d94b-136">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="5d94b-136">-MaxCount</span></span>
<span data-ttu-id="5d94b-137">Gibt die maximale Anzahl von Auftrags Terminen an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5d94b-137">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="5d94b-138">Wenn Sie den Wert 0 (null) oder weniger angeben, verwendet das Cmdlet keine Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="5d94b-138">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="5d94b-139">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="5d94b-139">The default value is 1000.</span></span>

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

### <span data-ttu-id="5d94b-140">-Wählen Sie</span><span class="sxs-lookup"><span data-stu-id="5d94b-140">-Select</span></span>
<span data-ttu-id="5d94b-141">Gibt eine OData-Auswahl Klausel an.</span><span class="sxs-lookup"><span data-stu-id="5d94b-141">Specifies an OData select clause.</span></span>
<span data-ttu-id="5d94b-142">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften und nicht alle Objekteigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5d94b-142">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="5d94b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d94b-143">CommonParameters</span></span>
<span data-ttu-id="5d94b-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d94b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d94b-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d94b-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d94b-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d94b-146">INPUTS</span></span>

### <span data-ttu-id="5d94b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="5d94b-147">System.String</span></span>

### <span data-ttu-id="5d94b-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5d94b-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5d94b-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d94b-149">OUTPUTS</span></span>

### <span data-ttu-id="5d94b-150">Microsoft.Azure.Commands.Batch. Models. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5d94b-150">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

## <span data-ttu-id="5d94b-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d94b-151">NOTES</span></span>

## <span data-ttu-id="5d94b-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d94b-152">RELATED LINKS</span></span>

[<span data-ttu-id="5d94b-153">Deaktivieren-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5d94b-153">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="5d94b-154">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5d94b-154">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="5d94b-155">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5d94b-155">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5d94b-156">Neu – AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5d94b-156">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="5d94b-157">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5d94b-157">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="5d94b-158">Stopp-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5d94b-158">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="5d94b-159">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="5d94b-159">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


