---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: 2b53d9baf6461024f22cf2f44d75c071b57fb618
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94007513"
---
# <span data-ttu-id="b4948-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="b4948-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="b4948-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4948-102">SYNOPSIS</span></span>
<span data-ttu-id="b4948-103">Ruft die Vorbereitung des stapelverarbeitungsauftrags ab und gibt den Aufgabenstatus frei.</span><span class="sxs-lookup"><span data-stu-id="b4948-103">Gets Batch job preparation and release task status.</span></span>

## <span data-ttu-id="b4948-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4948-104">SYNTAX</span></span>

### <span data-ttu-id="b4948-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="b4948-105">Id (Default)</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4948-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b4948-106">InputObject</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4948-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4948-107">DESCRIPTION</span></span>
<span data-ttu-id="b4948-108">Das Cmdlet " **Get-AzBatchJobPreparationAndReleaseTaskStatus** " Ruft den Azure Batch Job Preparation ab und gibt den Aufgabenstatus für einen Stapelverarbeitungsauftrag frei.</span><span class="sxs-lookup"><span data-stu-id="b4948-108">The **Get-AzBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="b4948-109">Sie müssen den *ID-* Parameter oder eine **PSCloudJob** -Instanz für dieses Cmdlet angeben.</span><span class="sxs-lookup"><span data-stu-id="b4948-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="b4948-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4948-110">EXAMPLES</span></span>

### <span data-ttu-id="b4948-111">Beispiel 1: Abrufen des Auftrags Vorbereitungs-und Freigabestatus eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="b4948-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="b4948-112">Dieser Befehl ruft die Job-Vorbereitung ab und gibt den Aufgabenstatus für Job "Test" frei.</span><span class="sxs-lookup"><span data-stu-id="b4948-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="b4948-113">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="b4948-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="b4948-114">Beispiel 2: Abrufen des Auftrags Vorbereitungs-und Freigabestatus eines Auftrags mit Filter und Auswählen von "angegeben"</span><span class="sxs-lookup"><span data-stu-id="b4948-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="b4948-115">Dieser Befehl ruft den Job-Vorbereitungs-und Freigabe Aufgabenstatus für Job "Test" auf dem Knoten "TVM-2316545714_1-20170613t201733z" ab und verwendet die SELECT-Klausel, um anzugeben, dass nur die JobPreparationTaskExecutionInformation-Informationen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b4948-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="b4948-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4948-116">PARAMETERS</span></span>

### <span data-ttu-id="b4948-117">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="b4948-117">-BatchContext</span></span>
<span data-ttu-id="b4948-118">Die BatchAccountContext-Instanz, die bei der Interaktion mit dem Batch Dienst verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4948-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="b4948-119">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b4948-119">Use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

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

### <span data-ttu-id="b4948-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4948-120">-DefaultProfile</span></span>
<span data-ttu-id="b4948-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b4948-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4948-122">– Erweitern</span><span class="sxs-lookup"><span data-stu-id="b4948-122">-Expand</span></span>
<span data-ttu-id="b4948-123">Gibt eine Open Data Protocol (OData) expand-Klausel an.</span><span class="sxs-lookup"><span data-stu-id="b4948-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="b4948-124">Geben Sie einen Wert für diesen Parameter an, um zugeordnete Entitäten der Haupt Entität abzurufen, die Sie erhalten.</span><span class="sxs-lookup"><span data-stu-id="b4948-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="b4948-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="b4948-125">-Filter</span></span>
<span data-ttu-id="b4948-126">Gibt eine OData-Filterklausel an.</span><span class="sxs-lookup"><span data-stu-id="b4948-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="b4948-127">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Job-Vorbereitungen zurück und gibt den Aufgabenstatus für den Auftrag frei.</span><span class="sxs-lookup"><span data-stu-id="b4948-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

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

### <span data-ttu-id="b4948-128">-ID</span><span class="sxs-lookup"><span data-stu-id="b4948-128">-Id</span></span>
<span data-ttu-id="b4948-129">Gibt die ID des Auftrags an, dessen Vorbereitungs-und Freigabe Aufgaben abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b4948-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="b4948-130">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="b4948-130">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="b4948-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b4948-131">-InputObject</span></span>
<span data-ttu-id="b4948-132">Gibt ein **PSCloudJob** -Objekt an, das den Auftrag darstellt, aus dem der Status der Vorbereitung und Freigabe des Vorgangs abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4948-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="b4948-133">Verwenden Sie das Get-AzBatchJob-Cmdlet, um ein **PSCloudJob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b4948-133">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="b4948-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b4948-134">-MaxCount</span></span>
<span data-ttu-id="b4948-135">Gibt die maximale Anzahl von Aufträgen für die Vorbereitung und Freigabe des Vorgangsstatus zurück.</span><span class="sxs-lookup"><span data-stu-id="b4948-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="b4948-136">Wenn Sie den Wert 0 (null) oder weniger angeben, verwendet das Cmdlet keine Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="b4948-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="b4948-137">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="b4948-137">The default value is 1000.</span></span>

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

### <span data-ttu-id="b4948-138">-Wählen Sie</span><span class="sxs-lookup"><span data-stu-id="b4948-138">-Select</span></span>
<span data-ttu-id="b4948-139">Gibt eine OData-Auswahl Klausel an.</span><span class="sxs-lookup"><span data-stu-id="b4948-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="b4948-140">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften und nicht alle Objekteigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b4948-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="b4948-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4948-141">CommonParameters</span></span>
<span data-ttu-id="b4948-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4948-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4948-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4948-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4948-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4948-144">INPUTS</span></span>

### <span data-ttu-id="b4948-145">Microsoft.Azure.Commands.Batch. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="b4948-145">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="b4948-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b4948-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b4948-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4948-147">OUTPUTS</span></span>

### <span data-ttu-id="b4948-148">Microsoft.Azure.Commands.Batch. Models. PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="b4948-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="b4948-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4948-149">NOTES</span></span>

## <span data-ttu-id="b4948-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4948-150">RELATED LINKS</span></span>

[<span data-ttu-id="b4948-151">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b4948-151">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="b4948-152">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="b4948-152">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)
