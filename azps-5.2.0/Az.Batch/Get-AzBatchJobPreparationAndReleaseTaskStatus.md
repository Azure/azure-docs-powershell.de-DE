---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: ffc89f298715f9e878bb3283c99e794f92662e84
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363249"
---
# <span data-ttu-id="2ec96-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="2ec96-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="2ec96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ec96-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec96-103">Ruft die Batchauftragsvorbereitung ab und gibt den Vorgangsstatus frei.</span><span class="sxs-lookup"><span data-stu-id="2ec96-103">Gets Batch job preparation and release task status.</span></span>

## <span data-ttu-id="2ec96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ec96-104">SYNTAX</span></span>

### <span data-ttu-id="2ec96-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="2ec96-105">Id (Default)</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ec96-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2ec96-106">InputObject</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ec96-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ec96-107">DESCRIPTION</span></span>
<span data-ttu-id="2ec96-108">Das **Cmdlet "Get-AzBatchJobPreparationAndReleaseTaskStatus"** ruft den Vorgangsvorbereitungs- und Freigabestatus von Azure Batch für einen Stapelauftrag ab.</span><span class="sxs-lookup"><span data-stu-id="2ec96-108">The **Get-AzBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="2ec96-109">Sie müssen den Parameter *"Id"* oder eine **"PSCloudJob"-Instanz** für dieses Cmdlet angeben.</span><span class="sxs-lookup"><span data-stu-id="2ec96-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="2ec96-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2ec96-110">EXAMPLES</span></span>

### <span data-ttu-id="2ec96-111">Beispiel 1: Vorbereiten eines Auftrags und Veröffentlichungsstatus eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="2ec96-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="2ec96-112">Dieser Befehl ruft die Auftragsvorbereitung und den Vorgangsstatus für "Test" ab.</span><span class="sxs-lookup"><span data-stu-id="2ec96-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="2ec96-113">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der Variablen $Context Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="2ec96-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="2ec96-114">Beispiel 2: Vorbereiten eines Auftrags und Freigabestatus eines Auftrags mit angegebener Option "Filtern und auswählen"</span><span class="sxs-lookup"><span data-stu-id="2ec96-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="2ec96-115">Dieser Befehl ruft den Vorgangsvorbereitungs- und Freigabestatus für den Auftrag "Test" für Knoten "tvm-2316545714_1-20170613t201733z" ab und verwendet die Select-Klausel, um nur die Informationen "JobPreparationTaskExecutionInformation" zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="2ec96-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="2ec96-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ec96-116">PARAMETERS</span></span>

### <span data-ttu-id="2ec96-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2ec96-117">-BatchContext</span></span>
<span data-ttu-id="2ec96-118">Die BatchAccountContext-Instanz, die bei der Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2ec96-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="2ec96-119">Verwenden Sie Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2ec96-119">Use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

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

### <span data-ttu-id="2ec96-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ec96-120">-DefaultProfile</span></span>
<span data-ttu-id="2ec96-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ec96-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ec96-122">-Expand</span><span class="sxs-lookup"><span data-stu-id="2ec96-122">-Expand</span></span>
<span data-ttu-id="2ec96-123">Gibt eine Open Data Protocol (OData)-Erweiterungsklausel an.</span><span class="sxs-lookup"><span data-stu-id="2ec96-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="2ec96-124">Geben Sie einen Wert für diesen Parameter an, um zugeordnete Entitäten der erhaltenen Hauptentität zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2ec96-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="2ec96-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="2ec96-125">-Filter</span></span>
<span data-ttu-id="2ec96-126">Gibt eine OData-Filterklausel an.</span><span class="sxs-lookup"><span data-stu-id="2ec96-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="2ec96-127">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Aufgabenvorbereitungs- und Freigabestatus für den Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="2ec96-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

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

### <span data-ttu-id="2ec96-128">-ID</span><span class="sxs-lookup"><span data-stu-id="2ec96-128">-Id</span></span>
<span data-ttu-id="2ec96-129">Gibt die ID des Auftrags an, dessen Vorbereitungs- und Freigabeaufgaben abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2ec96-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="2ec96-130">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="2ec96-130">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="2ec96-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ec96-131">-InputObject</span></span>
<span data-ttu-id="2ec96-132">Gibt ein **PSCloudJob-Objekt** an, das den Auftrag darstellt, von dem der Vorbereitungs- und Freigabestatus der Aufgabe zu erhalten ist.</span><span class="sxs-lookup"><span data-stu-id="2ec96-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="2ec96-133">Zum Abrufen eines **PSCloudJob-Objekts** verwenden Sie das Get-AzBatchJob-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ec96-133">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="2ec96-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2ec96-134">-MaxCount</span></span>
<span data-ttu-id="2ec96-135">Gibt die maximale Anzahl der zurückzukehrenden Aufträge für die Vorbereitung und freigaben des Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="2ec96-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="2ec96-136">Wenn Sie einen Wert von Null (0) oder kleiner angeben, wird für das Cmdlet keine Obergrenze verwendet.</span><span class="sxs-lookup"><span data-stu-id="2ec96-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="2ec96-137">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="2ec96-137">The default value is 1000.</span></span>

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

### <span data-ttu-id="2ec96-138">-Select</span><span class="sxs-lookup"><span data-stu-id="2ec96-138">-Select</span></span>
<span data-ttu-id="2ec96-139">Gibt eine OData-Auswahlklausel an.</span><span class="sxs-lookup"><span data-stu-id="2ec96-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="2ec96-140">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften und nicht alle Objekteigenschaften zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2ec96-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="2ec96-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec96-141">CommonParameters</span></span>
<span data-ttu-id="2ec96-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ec96-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ec96-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ec96-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec96-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2ec96-144">INPUTS</span></span>

### <span data-ttu-id="2ec96-145">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="2ec96-145">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="2ec96-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2ec96-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2ec96-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2ec96-147">OUTPUTS</span></span>

### <span data-ttu-id="2ec96-148">Microsoft.Azure.Commands.Batch. Models.PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="2ec96-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="2ec96-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2ec96-149">NOTES</span></span>

## <span data-ttu-id="2ec96-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2ec96-150">RELATED LINKS</span></span>

[<span data-ttu-id="2ec96-151">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2ec96-151">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="2ec96-152">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2ec96-152">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
