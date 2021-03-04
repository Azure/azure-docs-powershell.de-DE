---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: e85976b4d4b5de508e1a4f25338b21abdb0c097f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934347"
---
# <span data-ttu-id="fc94f-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="fc94f-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="fc94f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc94f-102">SYNOPSIS</span></span>
<span data-ttu-id="fc94f-103">Ruft den Status batch job preparation and release task ab.</span><span class="sxs-lookup"><span data-stu-id="fc94f-103">Gets Batch job preparation and release task status.</span></span>

## <span data-ttu-id="fc94f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc94f-104">SYNTAX</span></span>

### <span data-ttu-id="fc94f-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="fc94f-105">Id (Default)</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc94f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fc94f-106">InputObject</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc94f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc94f-107">DESCRIPTION</span></span>
<span data-ttu-id="fc94f-108">Das **Cmdlet Get-AzBatchJobPreparationAndReleaseTaskStatus** ruft den Azure Batch-Auftragsvorbereitungs- und -freigabestatus für einen Batchauftrag ab.</span><span class="sxs-lookup"><span data-stu-id="fc94f-108">The **Get-AzBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="fc94f-109">Sie müssen den Parameter *Id* oder eine **PSCloudJob-Instanz** für dieses Cmdlet angeben.</span><span class="sxs-lookup"><span data-stu-id="fc94f-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="fc94f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fc94f-110">EXAMPLES</span></span>

### <span data-ttu-id="fc94f-111">Beispiel 1: Anzeigen des Vorbereitungs- und Freigabestatus eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="fc94f-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="fc94f-112">Dieser Befehl ruft den Vorgangsvorbereitungs- und Freigabestatus für "Test" ab.</span><span class="sxs-lookup"><span data-stu-id="fc94f-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="fc94f-113">Verwenden Sie Get-AzBatchAccountKey-Cmdlet, um der Variablen $Context Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="fc94f-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="fc94f-114">Beispiel 2: Anzeigen des Auftragsvorbereitungs- und Freigabestatus eines Auftrags mit angegebener Option "Filter" und "Auswählen"</span><span class="sxs-lookup"><span data-stu-id="fc94f-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="fc94f-115">Dieser Befehl ruft den Vorgangsvorbereitungs- und Freigabeaufgabenstatus für den Auftrag "Test" auf knoten "tvm-2316545714_1-20170613t201733z" ab und verwendet die Select-Klausel, um nur die JobPreparationTaskExecutionInformationsinformationen zurücksennen zu lassen.</span><span class="sxs-lookup"><span data-stu-id="fc94f-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="fc94f-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fc94f-116">PARAMETERS</span></span>

### <span data-ttu-id="fc94f-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fc94f-117">-BatchContext</span></span>
<span data-ttu-id="fc94f-118">Die BatchAccountContext-Instanz, die bei der Interaktion mit dem Batchdienst verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc94f-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="fc94f-119">Verwenden Sie Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fc94f-119">Use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

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

### <span data-ttu-id="fc94f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc94f-120">-DefaultProfile</span></span>
<span data-ttu-id="fc94f-121">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc94f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc94f-122">-Erweitern</span><span class="sxs-lookup"><span data-stu-id="fc94f-122">-Expand</span></span>
<span data-ttu-id="fc94f-123">Gibt eine Open Data Protocol (OData)-Erweiterungsklausel an.</span><span class="sxs-lookup"><span data-stu-id="fc94f-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="fc94f-124">Geben Sie einen Wert für diesen Parameter an, um zugeordnete Entitäten der Hauptentität zu erhalten, die Sie erhalten.</span><span class="sxs-lookup"><span data-stu-id="fc94f-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="fc94f-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="fc94f-125">-Filter</span></span>
<span data-ttu-id="fc94f-126">Gibt eine OData-Filterklausel an.</span><span class="sxs-lookup"><span data-stu-id="fc94f-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="fc94f-127">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Status der Auftragsvorbereitung und -freigabe für den Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="fc94f-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

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

### <span data-ttu-id="fc94f-128">-ID</span><span class="sxs-lookup"><span data-stu-id="fc94f-128">-Id</span></span>
<span data-ttu-id="fc94f-129">Gibt die ID des Auftrags an, dessen Vorbereitungs- und Freigabeaufgaben abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fc94f-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="fc94f-130">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="fc94f-130">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="fc94f-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc94f-131">-InputObject</span></span>
<span data-ttu-id="fc94f-132">Gibt ein **PSCloudJob-Objekt** an, das den Auftrag darstellt, aus dem der Status des Vorbereitungs- und Freigabeauftrags zu erhalten ist.</span><span class="sxs-lookup"><span data-stu-id="fc94f-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="fc94f-133">Um ein **PSCloudJob-Objekt** zu erhalten, verwenden Sie das Get-AzBatchJob Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc94f-133">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="fc94f-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="fc94f-134">-MaxCount</span></span>
<span data-ttu-id="fc94f-135">Gibt die maximale Anzahl von Aufträgen an, die als Vorbereitungs- und Freigabeaufgabe angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fc94f-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="fc94f-136">Wenn Sie einen Wert von Null (0) oder kleiner angeben, wird für das Cmdlet keine Obergrenze verwendet.</span><span class="sxs-lookup"><span data-stu-id="fc94f-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="fc94f-137">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="fc94f-137">The default value is 1000.</span></span>

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

### <span data-ttu-id="fc94f-138">-Select</span><span class="sxs-lookup"><span data-stu-id="fc94f-138">-Select</span></span>
<span data-ttu-id="fc94f-139">Gibt eine OData-Auswahlklausel an.</span><span class="sxs-lookup"><span data-stu-id="fc94f-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="fc94f-140">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften anstelle aller Objekteigenschaften zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fc94f-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="fc94f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc94f-141">CommonParameters</span></span>
<span data-ttu-id="fc94f-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc94f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc94f-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc94f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc94f-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fc94f-144">INPUTS</span></span>

### <span data-ttu-id="fc94f-145">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="fc94f-145">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="fc94f-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fc94f-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="fc94f-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fc94f-147">OUTPUTS</span></span>

### <span data-ttu-id="fc94f-148">Microsoft.Azure.Commands.Batch. Models.PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="fc94f-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="fc94f-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fc94f-149">NOTES</span></span>

## <span data-ttu-id="fc94f-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fc94f-150">RELATED LINKS</span></span>

[<span data-ttu-id="fc94f-151">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="fc94f-151">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="fc94f-152">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fc94f-152">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
