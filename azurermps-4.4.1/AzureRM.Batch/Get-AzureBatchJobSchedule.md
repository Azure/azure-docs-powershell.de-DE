---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
ms.openlocfilehash: 139282332fb1c5d0ace02ddd7b998c1875af931a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497134"
---
# <span data-ttu-id="937d9-101">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="937d9-101">Get-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="937d9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="937d9-102">SYNOPSIS</span></span>
<span data-ttu-id="937d9-103">Ruft Stapel Auftragszeitpläne ab.</span><span class="sxs-lookup"><span data-stu-id="937d9-103">Gets Batch job schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="937d9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="937d9-104">SYNTAX</span></span>

### <span data-ttu-id="937d9-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="937d9-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="937d9-106">ID</span><span class="sxs-lookup"><span data-stu-id="937d9-106">Id</span></span>
```
Get-AzureBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="937d9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="937d9-107">DESCRIPTION</span></span>
<span data-ttu-id="937d9-108">Das Cmdlet " **Get-AzureBatchJobSchedule** " ruft Azure-batchauftrags Zeitpläne für das vom *batchcontext* -Parameter angegebene Batch Konto ab.</span><span class="sxs-lookup"><span data-stu-id="937d9-108">The **Get-AzureBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="937d9-109">Geben Sie eine ID an, um einen einzelnen Auftragszeitplan abzurufen.</span><span class="sxs-lookup"><span data-stu-id="937d9-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="937d9-110">Geben Sie den *Filter* -Parameter an, um die Auftragszeitpläne abzurufen, die einem Open Data Protocol (OData)-Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="937d9-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="937d9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="937d9-111">EXAMPLES</span></span>

### <span data-ttu-id="937d9-112">Beispiel 1: Abrufen eines Auftragszeitplans durch Angabe einer ID</span><span class="sxs-lookup"><span data-stu-id="937d9-112">Example 1: Get a job schedule by specifying an ID</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Id "JobSchedule23" -BatchContext $Context
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

<span data-ttu-id="937d9-113">Dieser Befehl ruft den Auftragszeitplan ab, der die ID JobSchedule23.</span><span class="sxs-lookup"><span data-stu-id="937d9-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="937d9-114">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="937d9-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="937d9-115">Beispiel 2: Abrufen von Auftrags Terminplänen mithilfe eines Filters</span><span class="sxs-lookup"><span data-stu-id="937d9-115">Example 2: Get job schedules by using a filter</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Filter "startswith(id,'Job')" -BatchContext $Context
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

<span data-ttu-id="937d9-116">Dieser Befehl ruft alle Auftragszeitpläne ab, die IDs aufweisen, die mit Job beginnen, indem Sie den Parameter *Filter* angeben.</span><span class="sxs-lookup"><span data-stu-id="937d9-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="937d9-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="937d9-117">PARAMETERS</span></span>

### <span data-ttu-id="937d9-118">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="937d9-118">-BatchContext</span></span>
<span data-ttu-id="937d9-119">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="937d9-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="937d9-120">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="937d9-120">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="937d9-121">– Erweitern</span><span class="sxs-lookup"><span data-stu-id="937d9-121">-Expand</span></span>
<span data-ttu-id="937d9-122">Gibt eine Open Data Protocol (OData) expand-Klausel an.</span><span class="sxs-lookup"><span data-stu-id="937d9-122">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="937d9-123">Geben Sie einen Wert für diesen Parameter an, um zugeordnete Entitäten der Haupt Entität abzurufen, die Sie erhalten.</span><span class="sxs-lookup"><span data-stu-id="937d9-123">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="937d9-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="937d9-124">-Filter</span></span>
<span data-ttu-id="937d9-125">Gibt eine OData-Filterklausel an.</span><span class="sxs-lookup"><span data-stu-id="937d9-125">Specifies an OData filter clause.</span></span>
<span data-ttu-id="937d9-126">Dieses Cmdlet gibt Auftragszeitpläne zurück, die dem Filter entsprechen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="937d9-126">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="937d9-127">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Auftragszeitpläne für den Batch Kontext zurück.</span><span class="sxs-lookup"><span data-stu-id="937d9-127">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

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

### <span data-ttu-id="937d9-128">-ID</span><span class="sxs-lookup"><span data-stu-id="937d9-128">-Id</span></span>
<span data-ttu-id="937d9-129">Gibt die ID des Auftragszeitplans an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="937d9-129">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="937d9-130">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="937d9-130">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="937d9-131">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="937d9-131">-MaxCount</span></span>
<span data-ttu-id="937d9-132">Gibt die maximale Anzahl von Auftrags Terminen an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="937d9-132">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="937d9-133">Wenn Sie den Wert 0 (null) oder weniger angeben, verwendet das Cmdlet keine Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="937d9-133">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="937d9-134">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="937d9-134">The default value is 1000.</span></span>

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

### <span data-ttu-id="937d9-135">-Wählen Sie</span><span class="sxs-lookup"><span data-stu-id="937d9-135">-Select</span></span>
<span data-ttu-id="937d9-136">Gibt eine OData-Auswahl Klausel an.</span><span class="sxs-lookup"><span data-stu-id="937d9-136">Specifies an OData select clause.</span></span>
<span data-ttu-id="937d9-137">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften und nicht alle Objekteigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="937d9-137">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="937d9-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="937d9-138">-DefaultProfile</span></span>
<span data-ttu-id="937d9-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="937d9-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="937d9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="937d9-140">CommonParameters</span></span>
<span data-ttu-id="937d9-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="937d9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="937d9-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="937d9-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="937d9-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="937d9-143">INPUTS</span></span>

### <span data-ttu-id="937d9-144">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="937d9-144">BatchAccountContext</span></span>
<span data-ttu-id="937d9-145">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="937d9-145">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="937d9-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="937d9-146">String</span></span>
<span data-ttu-id="937d9-147">Der Parameter "ID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="937d9-147">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="937d9-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="937d9-148">OUTPUTS</span></span>

### <span data-ttu-id="937d9-149">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="937d9-149">PSCloudJobSchedule</span></span>

## <span data-ttu-id="937d9-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="937d9-150">NOTES</span></span>

## <span data-ttu-id="937d9-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="937d9-151">RELATED LINKS</span></span>

[<span data-ttu-id="937d9-152">Deaktivieren-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="937d9-152">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="937d9-153">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="937d9-153">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="937d9-154">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="937d9-154">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="937d9-155">Neu – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="937d9-155">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="937d9-156">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="937d9-156">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="937d9-157">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="937d9-157">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="937d9-158">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="937d9-158">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


