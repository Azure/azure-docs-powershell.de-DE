---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
ms.openlocfilehash: 94a35c3923debf5ea983e9d1ad276b124ae8c89c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497905"
---
# <span data-ttu-id="a3140-101">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a3140-101">New-AzureBatchJob</span></span>

## <span data-ttu-id="a3140-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3140-102">SYNOPSIS</span></span>
<span data-ttu-id="a3140-103">Erstellt einen Auftrag im Stapelverarbeitungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="a3140-103">Creates a job in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3140-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3140-104">SYNTAX</span></span>

```
New-AzureBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3140-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3140-105">DESCRIPTION</span></span>
<span data-ttu-id="a3140-106">Das Cmdlet **New-AzureBatchJob** erstellt einen Auftrag im Azure-Batch Dienst in dem durch den *BatchAccountContext* -Parameter angegebenen Konto.</span><span class="sxs-lookup"><span data-stu-id="a3140-106">The **New-AzureBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="a3140-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3140-107">EXAMPLES</span></span>

### <span data-ttu-id="a3140-108">Beispiel 1: Erstellen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="a3140-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation" 
PS C:\> $PoolInformation.PoolId = "Pool22" 
PS C:\> New-AzureBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="a3140-109">Der erste Befehl erstellt ein **PSPoolInformation** -Objekt mithilfe des New-Object-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="a3140-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="a3140-110">Der Befehl speichert das Objekt in der $PoolInformation Variablen.</span><span class="sxs-lookup"><span data-stu-id="a3140-110">The command stores that object in the $PoolInformation variable.</span></span>

<span data-ttu-id="a3140-111">Der zweite Befehl weist die ID-Pool22 der Eigenschaft **Pool** -ID des Objekts in $PoolInformation zu.</span><span class="sxs-lookup"><span data-stu-id="a3140-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>

<span data-ttu-id="a3140-112">Der endgültige Befehl erstellt einen Auftrag mit der ID ContosoJob35.</span><span class="sxs-lookup"><span data-stu-id="a3140-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="a3140-113">Aufgaben, die dem Auftrag hinzugefügt wurden, werden im Pool mit der ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="a3140-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="a3140-114">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="a3140-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="a3140-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3140-115">PARAMETERS</span></span>

### <span data-ttu-id="a3140-116">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="a3140-116">-BatchContext</span></span>
<span data-ttu-id="a3140-117">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3140-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a3140-118">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3140-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="a3140-119">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="a3140-119">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="a3140-120">Gibt die allgemeinen Umgebungsvariablen als Schlüssel-Wert-Paare an, die von diesem Cmdlet für alle Aufgaben im Auftrag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a3140-120">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="a3140-121">Der Schlüssel ist der Name der Umgebungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="a3140-121">The key is the environment variable name.</span></span>
<span data-ttu-id="a3140-122">Der Wert ist der Wert der Umgebungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="a3140-122">The value is the environment variable value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3140-123">-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="a3140-123">-Constraints</span></span>
<span data-ttu-id="a3140-124">Gibt die Ausführungs Einschränkungen für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="a3140-124">Specifies the execution constraints for the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3140-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a3140-125">-DisplayName</span></span>
<span data-ttu-id="a3140-126">Gibt den Anzeigenamen für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="a3140-126">Specifies the display name for the job.</span></span>

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

### <span data-ttu-id="a3140-127">-ID</span><span class="sxs-lookup"><span data-stu-id="a3140-127">-Id</span></span>
<span data-ttu-id="a3140-128">Gibt eine ID für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="a3140-128">Specifies an ID for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3140-129">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="a3140-129">-JobManagerTask</span></span>
<span data-ttu-id="a3140-130">Gibt den Job-Manager-Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="a3140-130">Specifies the Job Manager task.</span></span>
<span data-ttu-id="a3140-131">Der Stapelverarbeitungs Dienst führt beim Starten des Auftrags den Job-Manager-Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="a3140-131">The Batch service runs the Job Manager task when the job is started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobManagerTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3140-132">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="a3140-132">-JobPreparationTask</span></span>
<span data-ttu-id="a3140-133">Gibt den Job Preparation-Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="a3140-133">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="a3140-134">Der Stapelverarbeitungs Dienst führt den Job Preparation-Vorgang auf einem Compute-Knoten aus, bevor er alle Aufgaben dieses Auftrags auf diesem Compute-Knoten startet.</span><span class="sxs-lookup"><span data-stu-id="a3140-134">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3140-135">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="a3140-135">-JobReleaseTask</span></span>
<span data-ttu-id="a3140-136">Gibt die Aufgabe der Auftragsfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="a3140-136">Specifies the Job Release task.</span></span>
<span data-ttu-id="a3140-137">Der Stapelverarbeitungs Dienst führt den Auftragsfreigabe Task aus, wenn der Auftrag beendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3140-137">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="a3140-138">Der Stapelverarbeitungs Dienst führt die Aufgabe "Auftragsfreigabe" auf jedem Compute-Knoten aus, an dem die Aufgabe des Auftrags ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a3140-138">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobReleaseTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3140-139">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="a3140-139">-Metadata</span></span>
<span data-ttu-id="a3140-140">Gibt Metadaten als Schlüssel-Wert-Paare an, die dem Auftrag hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a3140-140">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="a3140-141">Der Schlüssel ist der Name der Metadaten.</span><span class="sxs-lookup"><span data-stu-id="a3140-141">The key is the metadata name.</span></span>
<span data-ttu-id="a3140-142">Der Wert ist der Wert für Metadaten.</span><span class="sxs-lookup"><span data-stu-id="a3140-142">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3140-143">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="a3140-143">-OnAllTasksComplete</span></span>
<span data-ttu-id="a3140-144">Gibt eine Aktion an, die vom Batch Dienst ausgeführt wird, wenn sich alle Aufgaben im Auftrag im Status abgeschlossen befinden.</span><span class="sxs-lookup"><span data-stu-id="a3140-144">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnAllTasksComplete]
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, TerminateJob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3140-145">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="a3140-145">-OnTaskFailure</span></span>
<span data-ttu-id="a3140-146">Gibt eine Aktion an, die der Batch Dienst ausführt, wenn eine Aufgabe im Auftrag fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="a3140-146">Specifies an action the Batch service takes if any task in the job fails.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnTaskFailure]
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, PerformExitOptionsJobAction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3140-147">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="a3140-147">-PoolInformation</span></span>
<span data-ttu-id="a3140-148">Gibt die Details des Pools an, in dem der Stapelverarbeitungs Dienst die Aufgaben des Auftrags ausführt.</span><span class="sxs-lookup"><span data-stu-id="a3140-148">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3140-149">-Priorität</span><span class="sxs-lookup"><span data-stu-id="a3140-149">-Priority</span></span>
<span data-ttu-id="a3140-150">Gibt die Priorität des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="a3140-150">Specifies the priority of the job.</span></span>
<span data-ttu-id="a3140-151">Gültige Werte sind: ganze Zahlen von-1000 bis 1000.</span><span class="sxs-lookup"><span data-stu-id="a3140-151">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="a3140-152">Der Wert-1000 hat die niedrigste Priorität.</span><span class="sxs-lookup"><span data-stu-id="a3140-152">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="a3140-153">Ein Wert von 1000 hat die höchste Priorität.</span><span class="sxs-lookup"><span data-stu-id="a3140-153">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="a3140-154">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="a3140-154">The default value is 0.</span></span>

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

### <span data-ttu-id="a3140-155">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="a3140-155">-UsesTaskDependencies</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3140-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3140-156">-DefaultProfile</span></span>
<span data-ttu-id="a3140-157">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a3140-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3140-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3140-158">CommonParameters</span></span>
<span data-ttu-id="a3140-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3140-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3140-160">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3140-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3140-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3140-161">INPUTS</span></span>

### <span data-ttu-id="a3140-162">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a3140-162">BatchAccountContext</span></span>
<span data-ttu-id="a3140-163">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a3140-163">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="a3140-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3140-164">OUTPUTS</span></span>

## <span data-ttu-id="a3140-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3140-165">NOTES</span></span>

## <span data-ttu-id="a3140-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3140-166">RELATED LINKS</span></span>

[<span data-ttu-id="a3140-167">Deaktivieren-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a3140-167">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="a3140-168">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a3140-168">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="a3140-169">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a3140-169">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a3140-170">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a3140-170">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="a3140-171">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a3140-171">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="a3140-172">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a3140-172">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="a3140-173">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a3140-173">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="a3140-174">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a3140-174">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


