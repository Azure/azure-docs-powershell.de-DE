---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
ms.openlocfilehash: 043e7bf24ce994edd0ce5621d2de8b17616d43f0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471132"
---
# <span data-ttu-id="e74d4-101">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="e74d4-101">New-AzBatchTask</span></span>

## <span data-ttu-id="e74d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e74d4-102">SYNOPSIS</span></span>
<span data-ttu-id="e74d4-103">Erstellt eine Batchaufgabe unter einem Auftrag.</span><span class="sxs-lookup"><span data-stu-id="e74d4-103">Creates a Batch task under a job.</span></span>

## <span data-ttu-id="e74d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e74d4-104">SYNTAX</span></span>

### <span data-ttu-id="e74d4-105">JobId_Single (Standard)</span><span class="sxs-lookup"><span data-stu-id="e74d4-105">JobId_Single (Default)</span></span>
```
New-AzBatchTask -JobId <String> -Id <String> [-DisplayName <String>] -CommandLine <String>
 [-ResourceFiles <PSResourceFile[]>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e74d4-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="e74d4-106">JobId_Bulk</span></span>
```
New-AzBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e74d4-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="e74d4-107">JobObject_Bulk</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e74d4-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="e74d4-108">JobObject_Single</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] -CommandLine <String>
 [-ResourceFiles <PSResourceFile[]>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e74d4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e74d4-109">DESCRIPTION</span></span>
<span data-ttu-id="e74d4-110">Das **Cmdlet "New-AzBatchTask"** erstellt eine Azure-Batch-Aufgabe unter dem Auftrag, der durch den Parameter *"JobId"* oder den Parameter *"Job" angegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="e74d4-110">The **New-AzBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="e74d4-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e74d4-111">EXAMPLES</span></span>

### <span data-ttu-id="e74d4-112">Beispiel 1: Erstellen einer Stapelaufgabe</span><span class="sxs-lookup"><span data-stu-id="e74d4-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="e74d4-113">Mit diesem Befehl wird eine Aufgabe erstellt, die die ID "Aufgabe23" unter dem Auftrag mit der ID "Auftrags-000001" hat.</span><span class="sxs-lookup"><span data-stu-id="e74d4-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="e74d4-114">Die Aufgabe führt den angegebenen Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="e74d4-114">The task runs the specified command.</span></span>
<span data-ttu-id="e74d4-115">Verwenden Sie **das Cmdlet "Get-AzBatchAccountKey",** um der Variablen "$Context" einen Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="e74d4-115">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="e74d4-116">Beispiel 2: Erstellen einer Batchaufgabe</span><span class="sxs-lookup"><span data-stu-id="e74d4-116">Example 2: Create a Batch task</span></span>
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

<span data-ttu-id="e74d4-117">Dieser Befehl ruft mithilfe des **Cmdlets "Get-AzBatchJob"** den Stapelauftrag ab, der den Id Job-000001 hat.</span><span class="sxs-lookup"><span data-stu-id="e74d4-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzBatchJob** cmdlet.</span></span>
<span data-ttu-id="e74d4-118">Der Befehl übergibt diesen Auftrag mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e74d4-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e74d4-119">Der Befehl erstellt eine Aufgabe, die die ID "Task26" unter diesem Auftrag hat.</span><span class="sxs-lookup"><span data-stu-id="e74d4-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="e74d4-120">Die Aufgabe führt den angegebenen Befehl mit erhöhten Berechtigungen aus.</span><span class="sxs-lookup"><span data-stu-id="e74d4-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="e74d4-121">Beispiel 3: Hinzufügen einer Sammlung von Aufgaben zum angegebenen Auftrag mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="e74d4-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="e74d4-122">Der erste Befehl erstellt mithilfe von **"Get-AzBatchAccountKey"** einen Objektverweis auf die Kontoschlüssel für das Batchkonto namens "ContosoBatchAccount".</span><span class="sxs-lookup"><span data-stu-id="e74d4-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="e74d4-123">Der Befehl speichert diesen Objektverweis in der $Context Variable.</span><span class="sxs-lookup"><span data-stu-id="e74d4-123">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="e74d4-124">Mit den nächsten beiden Befehlen werden mit dem cmdlet New-Object A0 **PSCloudTask-Objekte** erstellt.</span><span class="sxs-lookup"><span data-stu-id="e74d4-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="e74d4-125">Die Befehle speichern die Aufgaben in den Variablen $Task 01 und $Task 02.</span><span class="sxs-lookup"><span data-stu-id="e74d4-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="e74d4-126">Der letzte Befehl ruft den Stapelauftrag mit der ID Job-000001 mithilfe von **"Get-AzBatchJob" ab.**</span><span class="sxs-lookup"><span data-stu-id="e74d4-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzBatchJob**.</span></span>
<span data-ttu-id="e74d4-127">Anschließend übergibt der Befehl diesen Auftrag mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e74d4-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e74d4-128">Der Befehl fügt eine Sammlung von Aufgaben unter diesem Auftrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="e74d4-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="e74d4-129">Der Befehl verwendet den in der Datei $Context.</span><span class="sxs-lookup"><span data-stu-id="e74d4-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="e74d4-130">Beispiel 4: Hinzufügen einer Sammlung von Aufgaben zum angegebenen Auftrag</span><span class="sxs-lookup"><span data-stu-id="e74d4-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="e74d4-131">Der erste Befehl erstellt mithilfe von **"Get-AzBatchAccountKey"** einen Objektverweis auf die Kontoschlüssel für das Batchkonto namens "ContosoBatchAccount".</span><span class="sxs-lookup"><span data-stu-id="e74d4-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="e74d4-132">Der Befehl speichert diesen Objektverweis in der $Context Variable.</span><span class="sxs-lookup"><span data-stu-id="e74d4-132">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="e74d4-133">Mit den nächsten beiden Befehlen werden mit dem cmdlet New-Object A0 **PSCloudTask-Objekte** erstellt.</span><span class="sxs-lookup"><span data-stu-id="e74d4-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="e74d4-134">Die Befehle speichern die Aufgaben in den Variablen $Task 01 und $Task 02.</span><span class="sxs-lookup"><span data-stu-id="e74d4-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="e74d4-135">Der letzte Befehl fügt die in $Task 01 und $Task 02 gespeicherten Aufgaben unter dem Auftrag mit der ID Job-0000001 hinzu.</span><span class="sxs-lookup"><span data-stu-id="e74d4-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

### <span data-ttu-id="e74d4-136">Beispiel 5: Hinzufügen einer Aufgabe mit Ausgabedateien</span><span class="sxs-lookup"><span data-stu-id="e74d4-136">Example 5: Add a task with output files</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### <span data-ttu-id="e74d4-137">Beispiel 6: Hinzufügen einer Aufgabe mit Einstellungen für das Authentifizierungstoken</span><span class="sxs-lookup"><span data-stu-id="e74d4-137">Example 6: Add a task with authentication token settings</span></span>
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### <span data-ttu-id="e74d4-138">Beispiel 7: Hinzufügen einer Aufgabe, die in einem Container ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="e74d4-138">Example 7: Add a task which runs in a container</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## <span data-ttu-id="e74d4-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e74d4-139">PARAMETERS</span></span>

### <span data-ttu-id="e74d4-140">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="e74d4-140">-AffinityInformation</span></span>
<span data-ttu-id="e74d4-141">Gibt einen Lokalen Hinweis an, den der Batchdienst zum Auswählen eines Knotens verwendet, auf dem die Aufgabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e74d4-141">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAffinityInformation
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e74d4-142">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="e74d4-142">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e74d4-143">-AuthenticationTokenSettings</span><span class="sxs-lookup"><span data-stu-id="e74d4-143">-AuthenticationTokenSettings</span></span>
<span data-ttu-id="e74d4-144">Die Einstellungen für ein Authentifizierungstoken, das von der Aufgabe zum Ausführen von Batchdienstvorgängen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e74d4-144">The settings for an authentication token that the task can use to perform Batch service operations.</span></span>
<span data-ttu-id="e74d4-145">Wenn dies festgelegt ist, stellt der Batchdienst der Aufgabe ein Authentifizierungstoken zur Verfügung, mit dem Batchdienstvorgänge authentifiziert werden können, ohne dass ein Kontozugriffsschlüssel erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e74d4-145">If this is set, the Batch service provides the task with an authentication token which can be used to authenticate Batch service operations without requiring an account access key.</span></span> <span data-ttu-id="e74d4-146">Das Token wird über die AZ_BATCH_AUTHENTICATION_TOKEN Umgebungsvariable bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e74d4-146">The token is provided via the AZ_BATCH_AUTHENTICATION_TOKEN environment variable.</span></span> <span data-ttu-id="e74d4-147">Die Vorgänge, die die Aufgabe mithilfe des Tokens durchführen kann, sind von den Einstellungen abhängig.</span><span class="sxs-lookup"><span data-stu-id="e74d4-147">The operations that the task can carry out using the token depend on the settings.</span></span> <span data-ttu-id="e74d4-148">Beispielsweise kann eine Aufgabe Auftragsberechtigungen anfordern, um dem Auftrag weitere Aufgaben hinzuzufügen oder den Status des Auftrags oder anderer Aufgaben zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e74d4-148">For example, a task can request job permissions in order to add other tasks to the job, or check the status of the job or of other tasks.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e74d4-149">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e74d4-149">-BatchContext</span></span>
<span data-ttu-id="e74d4-150">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e74d4-150">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e74d4-151">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="e74d4-151">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e74d4-152">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e74d4-152">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e74d4-153">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="e74d4-153">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e74d4-154">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e74d4-154">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e74d4-155">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="e74d4-155">-CommandLine</span></span>
<span data-ttu-id="e74d4-156">Gibt die Befehlszeile für die Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="e74d4-156">Specifies the command line for the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e74d4-157">-Constraints</span><span class="sxs-lookup"><span data-stu-id="e74d4-157">-Constraints</span></span>
<span data-ttu-id="e74d4-158">Gibt die Ausführungseinschränkungen an, die für diesen Vorgang gelten.</span><span class="sxs-lookup"><span data-stu-id="e74d4-158">Specifies the execution constraints that apply to this task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e74d4-159">-ContainerSettings</span><span class="sxs-lookup"><span data-stu-id="e74d4-159">-ContainerSettings</span></span>
<span data-ttu-id="e74d4-160">Die Einstellungen für den Container, unter dem die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e74d4-160">The settings for the container under which the task runs.</span></span>
<span data-ttu-id="e74d4-161">Wenn für den Pool, der diese Aufgabe ausführen soll, "containerConfiguration" festgelegt ist, muss dies ebenfalls festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e74d4-161">If the pool that will run this task has containerConfiguration set, this must be set as well.</span></span> <span data-ttu-id="e74d4-162">Wenn für den Pool, der diese Aufgabe ausführen wird, "containerConfiguration" nicht festgelegt ist, darf dies nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e74d4-162">If the pool that will run this task doesn't have containerConfiguration set, this must not be set.</span></span> <span data-ttu-id="e74d4-163">Wenn dies angegeben wird, werden alle Verzeichnisse unter dem AZ_BATCH_NODE_ROOT_DIR (dem Stammverzeichnis von Azure Batch im Knoten) dem Container zugeordnet, alle Aufgabenumgebungsvariablen werden dem Container zugeordnet, und die Taskbefehlszeile wird im Container ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e74d4-163">When this is specified, all directories recursively below the AZ_BATCH_NODE_ROOT_DIR (the root of Azure Batch directories on the node) are mapped into the container, all task environment variables are mapped into the container, and the task command line is executed in the container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e74d4-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e74d4-164">-DefaultProfile</span></span>
<span data-ttu-id="e74d4-165">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e74d4-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e74d4-166">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="e74d4-166">-DependsOn</span></span>
<span data-ttu-id="e74d4-167">Gibt an, dass der Vorgang von anderen Vorgängen abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="e74d4-167">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="e74d4-168">Der Vorgang wird erst geplant, wenn alle abhängigen Vorgänge erfolgreich abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="e74d4-168">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

```yaml
Type: Microsoft.Azure.Batch.TaskDependencies
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e74d4-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e74d4-169">-DisplayName</span></span>
<span data-ttu-id="e74d4-170">Gibt den Anzeigenamen der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="e74d4-170">Specifies the display name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e74d4-171">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="e74d4-171">-EnvironmentSettings</span></span>
<span data-ttu-id="e74d4-172">Gibt die Umgebungseinstellungen als Schlüssel-Wert-Paare an, die dieses Cmdlet der Aufgabe hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="e74d4-172">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="e74d4-173">Der Schlüssel ist der Name der Umgebungseinstellung.</span><span class="sxs-lookup"><span data-stu-id="e74d4-173">The key is the environment setting name.</span></span>
<span data-ttu-id="e74d4-174">Der Wert ist die Umgebungseinstellung.</span><span class="sxs-lookup"><span data-stu-id="e74d4-174">The value is the environment setting.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: EnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e74d4-175">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="e74d4-175">-ExitConditions</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSExitConditions
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e74d4-176">-ID</span><span class="sxs-lookup"><span data-stu-id="e74d4-176">-Id</span></span>
<span data-ttu-id="e74d4-177">Gibt die ID des Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="e74d4-177">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e74d4-178">-Job</span><span class="sxs-lookup"><span data-stu-id="e74d4-178">-Job</span></span>
<span data-ttu-id="e74d4-179">Gibt den Auftrag an, unter dem dieses Cmdlet die Aufgabe erstellt.</span><span class="sxs-lookup"><span data-stu-id="e74d4-179">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="e74d4-180">Zum Abrufen eines **PSCloudJob-Objekts** verwenden Sie das Get-AzBatchJob-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e74d4-180">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: JobObject_Bulk, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e74d4-181">-JobId</span><span class="sxs-lookup"><span data-stu-id="e74d4-181">-JobId</span></span>
<span data-ttu-id="e74d4-182">Gibt die ID des Auftrags an, unter dem dieses Cmdlet die Aufgabe erstellt.</span><span class="sxs-lookup"><span data-stu-id="e74d4-182">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobId_Bulk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e74d4-183">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="e74d4-183">-MultiInstanceSettings</span></span>
<span data-ttu-id="e74d4-184">Gibt Informationen zum Ausführen einer Aufgabe mit mehreren Instanzen an.</span><span class="sxs-lookup"><span data-stu-id="e74d4-184">Specifies information about how to run a multi-instance task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e74d4-185">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="e74d4-185">-OutputFile</span></span>
<span data-ttu-id="e74d4-186">Ruft eine Liste der Dateien ab oder legt sie fest, die der Batchdienst nach dem Ausführen der Befehlszeile vom Rechenknoten aus hochladet.</span><span class="sxs-lookup"><span data-stu-id="e74d4-186">Gets or sets a list of files that the Batch service will upload from the compute node after running the command line.</span></span>
<span data-ttu-id="e74d4-187">Bei Aufgaben mit mehreren Instanzen werden die Dateien nur vom Rechenknoten hochgeladen, auf dem die primäre Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e74d4-187">For multi-instance tasks, the files will only be uploaded from the compute node on which the primary task is executed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSOutputFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e74d4-188">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="e74d4-188">-ResourceFiles</span></span>
<span data-ttu-id="e74d4-189">Gibt Ressourcendateien als Schlüssel-Wert-Paare an, die für den Vorgang erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e74d4-189">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="e74d4-190">Der Schlüssel ist der Ressourcendateipfad.</span><span class="sxs-lookup"><span data-stu-id="e74d4-190">The key is the resource file path.</span></span>
<span data-ttu-id="e74d4-191">Der Wert ist die BLOB-Quelle der Ressourcendatei.</span><span class="sxs-lookup"><span data-stu-id="e74d4-191">The value is the resource file blob source.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSResourceFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ResourceFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e74d4-192">-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="e74d4-192">-Tasks</span></span>
<span data-ttu-id="e74d4-193">Gibt die Sammlung der zu hinzufügenden Aufgaben an.</span><span class="sxs-lookup"><span data-stu-id="e74d4-193">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="e74d4-194">Jede Aufgabe muss eine eindeutige ID haben.</span><span class="sxs-lookup"><span data-stu-id="e74d4-194">Each task must have a unique ID.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask[]
Parameter Sets: JobId_Bulk, JobObject_Bulk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e74d4-195">-UserIdentity</span><span class="sxs-lookup"><span data-stu-id="e74d4-195">-UserIdentity</span></span>
<span data-ttu-id="e74d4-196">Die Benutzeridentität, unter der die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e74d4-196">The user identity under which the task runs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserIdentity
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e74d4-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e74d4-197">CommonParameters</span></span>
<span data-ttu-id="e74d4-198">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e74d4-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e74d4-199">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e74d4-199">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e74d4-200">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e74d4-200">INPUTS</span></span>

### <span data-ttu-id="e74d4-201">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="e74d4-201">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="e74d4-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e74d4-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e74d4-203">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e74d4-203">OUTPUTS</span></span>

### <span data-ttu-id="e74d4-204">System.Void</span><span class="sxs-lookup"><span data-stu-id="e74d4-204">System.Void</span></span>

## <span data-ttu-id="e74d4-205">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e74d4-205">NOTES</span></span>

## <span data-ttu-id="e74d4-206">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e74d4-206">RELATED LINKS</span></span>

[<span data-ttu-id="e74d4-207">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e74d4-207">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e74d4-208">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e74d4-208">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="e74d4-209">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="e74d4-209">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="e74d4-210">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="e74d4-210">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="e74d4-211">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="e74d4-211">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="e74d4-212">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="e74d4-212">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="e74d4-213">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e74d4-213">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
