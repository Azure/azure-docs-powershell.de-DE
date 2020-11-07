---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: 6c44688bcd11b624738c299dc04c1a0cb0da9494
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665107"
---
# <span data-ttu-id="61b9a-101">Get-AzureBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="61b9a-101">Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="61b9a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="61b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="61b9a-103">Ruft die Vorbereitung des stapelverarbeitungsauftrags ab und gibt den Aufgabenstatus frei.</span><span class="sxs-lookup"><span data-stu-id="61b9a-103">Gets Batch job preparation and release task status.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61b9a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="61b9a-104">SYNTAX</span></span>

### <span data-ttu-id="61b9a-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="61b9a-105">Id (Default)</span></span>
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61b9a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="61b9a-106">InputObject</span></span>
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61b9a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61b9a-107">DESCRIPTION</span></span>
<span data-ttu-id="61b9a-108">Das Cmdlet " **Get-AzureBatchJobPreparationAndReleaseTaskStatus** " Ruft den Azure Batch Job Preparation ab und gibt den Aufgabenstatus für einen Stapelverarbeitungsauftrag frei.</span><span class="sxs-lookup"><span data-stu-id="61b9a-108">The **Get-AzureBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="61b9a-109">Sie müssen den *ID-* Parameter oder eine **PSCloudJob** -Instanz für dieses Cmdlet angeben.</span><span class="sxs-lookup"><span data-stu-id="61b9a-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="61b9a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61b9a-110">EXAMPLES</span></span>

### <span data-ttu-id="61b9a-111">Beispiel 1: Abrufen des Auftrags Vorbereitungs-und Freigabestatus eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="61b9a-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="61b9a-112">Dieser Befehl ruft die Job-Vorbereitung ab und gibt den Aufgabenstatus für Job "Test" frei.</span><span class="sxs-lookup"><span data-stu-id="61b9a-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="61b9a-113">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="61b9a-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="61b9a-114">Beispiel 2: Abrufen des Auftrags Vorbereitungs-und Freigabestatus eines Auftrags mit Filter und Auswählen von "angegeben"</span><span class="sxs-lookup"><span data-stu-id="61b9a-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="61b9a-115">Dieser Befehl ruft den Job-Vorbereitungs-und Freigabe Aufgabenstatus für Job "Test" auf dem Knoten "TVM-2316545714_1-20170613t201733z" ab und verwendet die SELECT-Klausel, um anzugeben, dass nur die JobPreparationTaskExecutionInformation-Informationen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="61b9a-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="61b9a-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="61b9a-116">PARAMETERS</span></span>

### <span data-ttu-id="61b9a-117">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="61b9a-117">-BatchContext</span></span>
<span data-ttu-id="61b9a-118">Die BatchAccountContext-Instanz, die bei der Interaktion mit dem Batch Dienst verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="61b9a-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="61b9a-119">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="61b9a-119">Use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

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

### <span data-ttu-id="61b9a-120">– Erweitern</span><span class="sxs-lookup"><span data-stu-id="61b9a-120">-Expand</span></span>
<span data-ttu-id="61b9a-121">Gibt eine Open Data Protocol (OData) expand-Klausel an.</span><span class="sxs-lookup"><span data-stu-id="61b9a-121">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="61b9a-122">Geben Sie einen Wert für diesen Parameter an, um zugeordnete Entitäten der Haupt Entität abzurufen, die Sie erhalten.</span><span class="sxs-lookup"><span data-stu-id="61b9a-122">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="61b9a-123">-Filter</span><span class="sxs-lookup"><span data-stu-id="61b9a-123">-Filter</span></span>
<span data-ttu-id="61b9a-124">Gibt eine OData-Filterklausel an.</span><span class="sxs-lookup"><span data-stu-id="61b9a-124">Specifies an OData filter clause.</span></span>
<span data-ttu-id="61b9a-125">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Job-Vorbereitungen zurück und gibt den Aufgabenstatus für den Auftrag frei.</span><span class="sxs-lookup"><span data-stu-id="61b9a-125">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

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

### <span data-ttu-id="61b9a-126">-ID</span><span class="sxs-lookup"><span data-stu-id="61b9a-126">-Id</span></span>
<span data-ttu-id="61b9a-127">Gibt die ID des Auftrags an, dessen Vorbereitungs-und Freigabe Aufgaben abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="61b9a-127">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="61b9a-128">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="61b9a-128">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61b9a-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="61b9a-129">-InputObject</span></span>
<span data-ttu-id="61b9a-130">Gibt ein **PSCloudJob** -Objekt an, das den Auftrag darstellt, aus dem der Status der Vorbereitung und Freigabe des Vorgangs abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="61b9a-130">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="61b9a-131">Verwenden Sie das Get-AzureBatchJob-Cmdlet, um ein **PSCloudJob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="61b9a-131">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61b9a-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="61b9a-132">-MaxCount</span></span>
<span data-ttu-id="61b9a-133">Gibt die maximale Anzahl von Aufträgen für die Vorbereitung und Freigabe des Vorgangsstatus zurück.</span><span class="sxs-lookup"><span data-stu-id="61b9a-133">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="61b9a-134">Wenn Sie den Wert 0 (null) oder weniger angeben, verwendet das Cmdlet keine Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="61b9a-134">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="61b9a-135">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="61b9a-135">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61b9a-136">-Wählen Sie</span><span class="sxs-lookup"><span data-stu-id="61b9a-136">-Select</span></span>
<span data-ttu-id="61b9a-137">Gibt eine OData-Auswahl Klausel an.</span><span class="sxs-lookup"><span data-stu-id="61b9a-137">Specifies an OData select clause.</span></span>
<span data-ttu-id="61b9a-138">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften und nicht alle Objekteigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="61b9a-138">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="61b9a-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61b9a-139">-DefaultProfile</span></span>
<span data-ttu-id="61b9a-140">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="61b9a-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61b9a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61b9a-141">CommonParameters</span></span>
<span data-ttu-id="61b9a-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61b9a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61b9a-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61b9a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61b9a-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="61b9a-144">INPUTS</span></span>

### <span data-ttu-id="61b9a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="61b9a-145">System.String</span></span>
<span data-ttu-id="61b9a-146">Microsoft.Azure.Commands.Batch. Models. PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="61b9a-146">Microsoft.Azure.Commands.Batch.Models.PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="61b9a-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="61b9a-147">OUTPUTS</span></span>

### <span data-ttu-id="61b9a-148">Microsoft.Azure.Commands.Batch. Models. PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="61b9a-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="61b9a-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="61b9a-149">NOTES</span></span>

## <span data-ttu-id="61b9a-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="61b9a-150">RELATED LINKS</span></span>

[<span data-ttu-id="61b9a-151">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="61b9a-151">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="61b9a-152">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="61b9a-152">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
