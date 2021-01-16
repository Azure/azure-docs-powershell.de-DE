---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
ms.openlocfilehash: f997c1574a81badf9d97bb4afecc104990aa725b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296158"
---
# <span data-ttu-id="c25c2-101">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c25c2-101">New-AzBatchJob</span></span>

## <span data-ttu-id="c25c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c25c2-102">SYNOPSIS</span></span>
<span data-ttu-id="c25c2-103">Erstellt einen Auftrag im Batchdienst.</span><span class="sxs-lookup"><span data-stu-id="c25c2-103">Creates a job in the Batch service.</span></span>

## <span data-ttu-id="c25c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c25c2-104">SYNTAX</span></span>

```
New-AzBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c25c2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c25c2-105">DESCRIPTION</span></span>
<span data-ttu-id="c25c2-106">Das **Cmdlet "New-AzBatchJob"** erstellt einen Auftrag im Azure Batch-Dienst in dem Konto, das vom Parameter *"BatchAccountContext" angegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="c25c2-106">The **New-AzBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="c25c2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c25c2-107">EXAMPLES</span></span>

### <span data-ttu-id="c25c2-108">Beispiel 1: Erstellen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="c25c2-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $PoolInformation.PoolId = "Pool22"
PS C:\> New-AzBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="c25c2-109">Der erste Befehl erstellt ein **PSPoolInformation-Objekt** mithilfe des New-Object Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="c25c2-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="c25c2-110">Der Befehl speichert dieses Objekt in der $PoolInformation Variable.</span><span class="sxs-lookup"><span data-stu-id="c25c2-110">The command stores that object in the $PoolInformation variable.</span></span>
<span data-ttu-id="c25c2-111">Der zweite Befehl weist die ID Pool22 der **Eigenschaft "PoolId"** des Objekts in der $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="c25c2-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>
<span data-ttu-id="c25c2-112">Der letzte Befehl erstellt einen Auftrag mit der ID ContosoJob35.</span><span class="sxs-lookup"><span data-stu-id="c25c2-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="c25c2-113">Aufgaben, die dem Auftrag hinzugefügt wurden, werden für den Pool ausgeführt, der den ID Pool22 hat.</span><span class="sxs-lookup"><span data-stu-id="c25c2-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="c25c2-114">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der Variablen $Context Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="c25c2-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="c25c2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c25c2-115">PARAMETERS</span></span>

### <span data-ttu-id="c25c2-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c25c2-116">-BatchContext</span></span>
<span data-ttu-id="c25c2-117">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c25c2-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c25c2-118">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="c25c2-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c25c2-119">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c25c2-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c25c2-120">Bei verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="c25c2-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c25c2-121">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c25c2-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c25c2-122">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="c25c2-122">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="c25c2-123">Gibt die allgemeinen Umgebungsvariablen als Schlüssel-Wert-Paare an, die von diesem Cmdlet für alle Aufgaben im Auftrag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c25c2-123">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="c25c2-124">Der Schlüssel ist der Name der Umgebungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="c25c2-124">The key is the environment variable name.</span></span>
<span data-ttu-id="c25c2-125">Der Wert ist der Umgebungsvariablenwert.</span><span class="sxs-lookup"><span data-stu-id="c25c2-125">The value is the environment variable value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: CommonEnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c25c2-126">-Constraints</span><span class="sxs-lookup"><span data-stu-id="c25c2-126">-Constraints</span></span>
<span data-ttu-id="c25c2-127">Gibt die Ausführungseinschränkungen für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="c25c2-127">Specifies the execution constraints for the job.</span></span>

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

### <span data-ttu-id="c25c2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c25c2-128">-DefaultProfile</span></span>
<span data-ttu-id="c25c2-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c25c2-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c25c2-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c25c2-130">-DisplayName</span></span>
<span data-ttu-id="c25c2-131">Gibt den Anzeigenamen für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="c25c2-131">Specifies the display name for the job.</span></span>

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

### <span data-ttu-id="c25c2-132">-ID</span><span class="sxs-lookup"><span data-stu-id="c25c2-132">-Id</span></span>
<span data-ttu-id="c25c2-133">Gibt eine ID für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="c25c2-133">Specifies an ID for the job.</span></span>

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

### <span data-ttu-id="c25c2-134">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="c25c2-134">-JobManagerTask</span></span>
<span data-ttu-id="c25c2-135">Gibt den Vorgang "Job-Manager" an.</span><span class="sxs-lookup"><span data-stu-id="c25c2-135">Specifies the Job Manager task.</span></span>
<span data-ttu-id="c25c2-136">Der Batchdienst führt die Aufgabe "Job Manager" aus, wenn der Auftrag gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c25c2-136">The Batch service runs the Job Manager task when the job is started.</span></span>

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

### <span data-ttu-id="c25c2-137">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="c25c2-137">-JobPreparationTask</span></span>
<span data-ttu-id="c25c2-138">Gibt den Vorgang "Auftragsvorbereitung" an.</span><span class="sxs-lookup"><span data-stu-id="c25c2-138">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="c25c2-139">Der Batchdienst führt die Aufgabe "Auftragsvorbereitung" für einen Rechenknoten aus, bevor er Aufgaben dieses Auftrags für den berechneten Knoten startet.</span><span class="sxs-lookup"><span data-stu-id="c25c2-139">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

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

### <span data-ttu-id="c25c2-140">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="c25c2-140">-JobReleaseTask</span></span>
<span data-ttu-id="c25c2-141">Gibt den Vorgang "Job Release" an.</span><span class="sxs-lookup"><span data-stu-id="c25c2-141">Specifies the Job Release task.</span></span>
<span data-ttu-id="c25c2-142">Der Batchdienst führt die Aufgabe "Auftragsfreigabe" aus, wenn der Auftrag endet.</span><span class="sxs-lookup"><span data-stu-id="c25c2-142">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="c25c2-143">Der Batchdienst führt die Aufgabe "Job Release" für jeden Rechenknoten aus, in dem er eine Aufgabe des Auftrags ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="c25c2-143">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

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

### <span data-ttu-id="c25c2-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c25c2-144">-Metadata</span></span>
<span data-ttu-id="c25c2-145">Gibt Metadaten als Schlüssel-Wert-Paare an, die dem Auftrag hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c25c2-145">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="c25c2-146">Der Schlüssel ist der Metadatenname.</span><span class="sxs-lookup"><span data-stu-id="c25c2-146">The key is the metadata name.</span></span>
<span data-ttu-id="c25c2-147">Der Wert ist der Metadatenwert.</span><span class="sxs-lookup"><span data-stu-id="c25c2-147">The value is the metadata value.</span></span>

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

### <span data-ttu-id="c25c2-148">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="c25c2-148">-OnAllTasksComplete</span></span>
<span data-ttu-id="c25c2-149">Gibt eine Aktion an, die vom Batchdienst ausgeführt wird, wenn sich alle Aufgaben im Auftrag im Status "Abgeschlossen" befinden.</span><span class="sxs-lookup"><span data-stu-id="c25c2-149">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

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

### <span data-ttu-id="c25c2-150">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="c25c2-150">-OnTaskFailure</span></span>
<span data-ttu-id="c25c2-151">Gibt eine Aktion an, die vom Batchdienst ausgeführt wird, wenn eine Aufgabe im Auftrag fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="c25c2-151">Specifies an action the Batch service takes if any task in the job fails.</span></span>

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

### <span data-ttu-id="c25c2-152">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="c25c2-152">-PoolInformation</span></span>
<span data-ttu-id="c25c2-153">Gibt die Details des Pools an, für den der Batchdienst die Aufgaben des Auftrags führt.</span><span class="sxs-lookup"><span data-stu-id="c25c2-153">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

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

### <span data-ttu-id="c25c2-154">-Priority</span><span class="sxs-lookup"><span data-stu-id="c25c2-154">-Priority</span></span>
<span data-ttu-id="c25c2-155">Gibt die Priorität des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="c25c2-155">Specifies the priority of the job.</span></span>
<span data-ttu-id="c25c2-156">Gültige Werte sind: ganze Zahlen von -1000 bis 1000.</span><span class="sxs-lookup"><span data-stu-id="c25c2-156">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="c25c2-157">Der Wert "-1000" hat die niedrigste Priorität.</span><span class="sxs-lookup"><span data-stu-id="c25c2-157">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="c25c2-158">Der Wert "1000" hat die höchste Priorität.</span><span class="sxs-lookup"><span data-stu-id="c25c2-158">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="c25c2-159">Der Standardwert ist "0".</span><span class="sxs-lookup"><span data-stu-id="c25c2-159">The default value is 0.</span></span>

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

### <span data-ttu-id="c25c2-160">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="c25c2-160">-UsesTaskDependencies</span></span>
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

### <span data-ttu-id="c25c2-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c25c2-161">CommonParameters</span></span>
<span data-ttu-id="c25c2-162">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c25c2-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c25c2-163">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c25c2-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c25c2-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c25c2-164">INPUTS</span></span>

### <span data-ttu-id="c25c2-165">System.String</span><span class="sxs-lookup"><span data-stu-id="c25c2-165">System.String</span></span>

### <span data-ttu-id="c25c2-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c25c2-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c25c2-167">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c25c2-167">OUTPUTS</span></span>

### <span data-ttu-id="c25c2-168">System.Void</span><span class="sxs-lookup"><span data-stu-id="c25c2-168">System.Void</span></span>

## <span data-ttu-id="c25c2-169">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c25c2-169">NOTES</span></span>

## <span data-ttu-id="c25c2-170">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c25c2-170">RELATED LINKS</span></span>

[<span data-ttu-id="c25c2-171">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c25c2-171">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="c25c2-172">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c25c2-172">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="c25c2-173">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c25c2-173">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c25c2-174">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c25c2-174">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="c25c2-175">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c25c2-175">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="c25c2-176">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c25c2-176">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="c25c2-177">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c25c2-177">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="c25c2-178">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="c25c2-178">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
