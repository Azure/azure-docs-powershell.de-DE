---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
ms.openlocfilehash: 904c3a40f8f153a97bf8016f3708a310adfea3bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664392"
---
# <span data-ttu-id="2d3e9-101">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2d3e9-101">New-AzureBatchTask</span></span>

## <span data-ttu-id="2d3e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d3e9-102">SYNOPSIS</span></span>
<span data-ttu-id="2d3e9-103">Erstellt eine Batch Aufgabe unter einem Auftrag.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-103">Creates a Batch task under a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d3e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d3e9-104">SYNTAX</span></span>

### <span data-ttu-id="2d3e9-105">JobId_Single (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d3e9-105">JobId_Single (Default)</span></span>
```
New-AzureBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d3e9-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="2d3e9-106">JobId_Bulk</span></span>
```
New-AzureBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d3e9-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="2d3e9-107">JobObject_Bulk</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d3e9-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="2d3e9-108">JobObject_Single</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d3e9-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d3e9-109">DESCRIPTION</span></span>
<span data-ttu-id="2d3e9-110">Das Cmdlet **New-AzureBatchTask** erstellt eine Azure-Batch Aufgabe unter dem Auftrag, der durch den *JobID* -Parameter oder den *Job* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-110">The **New-AzureBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="2d3e9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d3e9-111">EXAMPLES</span></span>

### <span data-ttu-id="2d3e9-112">Beispiel 1: Erstellen einer Batch Aufgabe</span><span class="sxs-lookup"><span data-stu-id="2d3e9-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="2d3e9-113">Mit diesem Befehl wird eine Aufgabe erstellt, die die ID Task23 unter dem Auftrag mit dem Auftrags-000001.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="2d3e9-114">Der Task führt den angegebenen Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-114">The task runs the specified command.</span></span>
<span data-ttu-id="2d3e9-115">Verwenden Sie das Cmdlet **Get-AzureRmBatchAccountKeys** , um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-115">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="2d3e9-116">Beispiel 2: Erstellen einer Batch Aufgabe</span><span class="sxs-lookup"><span data-stu-id="2d3e9-116">Example 2: Create a Batch task</span></span>
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

<span data-ttu-id="2d3e9-117">Dieser Befehl ruft mit dem Cmdlet **Get-AzureBatchJob** den Stapelverarbeitungsauftrag ab, der die ID Job-000001 hat.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzureBatchJob** cmdlet.</span></span>
<span data-ttu-id="2d3e9-118">Der Befehl übergibt diesen Auftrag mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2d3e9-119">Der Befehl erstellt eine Aufgabe mit der ID Task26 unter diesem Auftrag.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="2d3e9-120">Die Aufgabe führt den angegebenen Befehl mithilfe von erhöhten Berechtigungen aus.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="2d3e9-121">Beispiel 3: Hinzufügen einer Sammlung von Aufgaben zum angegebenen Auftrag mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="2d3e9-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="2d3e9-122">Der erste Befehl erstellt einen Objektverweis auf die Kontoschlüssel für das Batch Konto mit dem Namen ContosoBatchAccount mithilfe von **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="2d3e9-123">Der Befehl speichert diesen Objektverweis in der $Context Variablen.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-123">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="2d3e9-124">Die nächsten beiden Befehle erstellen **PSCloudTask** -Objekte mithilfe des New-Object-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="2d3e9-125">Die Befehle speichern die Aufgaben in den Variablen $Task 01 und $Task 02.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="2d3e9-126">Der endgültige Befehl ruft den Stapelverarbeitungsauftrag ab, der die ID Job-000001 mithilfe von **Get-AzureBatchJob**.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzureBatchJob**.</span></span>
<span data-ttu-id="2d3e9-127">Anschließend übergibt der Befehl diesen Auftrag mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2d3e9-128">Der Befehl fügt eine Sammlung von Aufgaben unter diesem Auftrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="2d3e9-129">Der Befehl verwendet den in $context gespeicherten Kontext.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="2d3e9-130">Beispiel 4: Hinzufügen einer Sammlung von Aufgaben zum angegebenen Auftrag</span><span class="sxs-lookup"><span data-stu-id="2d3e9-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzureBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="2d3e9-131">Der erste Befehl erstellt einen Objektverweis auf die Kontoschlüssel für das Batch Konto mit dem Namen ContosoBatchAccount mithilfe von **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="2d3e9-132">Der Befehl speichert diesen Objektverweis in der $Context Variablen.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-132">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="2d3e9-133">Die nächsten beiden Befehle erstellen **PSCloudTask** -Objekte mithilfe des New-Object-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="2d3e9-134">Die Befehle speichern die Aufgaben in den Variablen $Task 01 und $Task 02.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="2d3e9-135">Der letzte Befehl fügt die Aufgaben, die in $Task 01 und $Task 02 gespeichert sind, unter dem Job hinzu, der die ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

### <span data-ttu-id="2d3e9-136">Beispiel 5: Hinzufügen einer Aufgabe mit Ausgabedateien</span><span class="sxs-lookup"><span data-stu-id="2d3e9-136">Example 5: Add a task with output files</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### <span data-ttu-id="2d3e9-137">Beispiel 6: Hinzufügen einer Aufgabe mit Authentifizierungstoken-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="2d3e9-137">Example 6: Add a task with authentication token settings</span></span>
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### <span data-ttu-id="2d3e9-138">Beispiel 7: Hinzufügen einer Aufgabe, die in einem Container ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="2d3e9-138">Example 7: Add a task which runs in a container</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## <span data-ttu-id="2d3e9-139">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d3e9-139">PARAMETERS</span></span>

### <span data-ttu-id="2d3e9-140">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="2d3e9-140">-AffinityInformation</span></span>
<span data-ttu-id="2d3e9-141">Gibt einen Orts Hinweis an, der vom Stapelverarbeitungs Dienst zum Auswählen eines Knotens verwendet wird, für den die Aufgabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-141">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

```yaml
Type: PSAffinityInformation
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e9-142">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="2d3e9-142">-ApplicationPackageReferences</span></span>
```yaml
Type: PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e9-143">-AuthenticationTokenSettings</span><span class="sxs-lookup"><span data-stu-id="2d3e9-143">-AuthenticationTokenSettings</span></span>
<span data-ttu-id="2d3e9-144">Die Einstellungen für ein Authentifizierungstoken, das die Aufgabe für die Ausführung von Batch Dienstvorgängen verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-144">The settings for an authentication token that the task can use to perform Batch service operations.</span></span>

<span data-ttu-id="2d3e9-145">Wenn dies eingestellt ist, stellt der Stapelverarbeitungs Dienst der Aufgabe ein Authentifizierungstoken zur Verfügung, das zum Authentifizieren von Batch Dienstvorgängen verwendet werden kann, ohne dass eine Kontozugriffs Taste erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-145">If this is set, the Batch service provides the task with an authentication token which can be used to authenticate Batch service operations without requiring an account access key.</span></span> <span data-ttu-id="2d3e9-146">Das Token wird über die AZ_BATCH_AUTHENTICATION_TOKEN Umgebungsvariable bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-146">The token is provided via the AZ_BATCH_AUTHENTICATION_TOKEN environment variable.</span></span> <span data-ttu-id="2d3e9-147">Die Vorgänge, die die Aufgabe mithilfe des Tokens ausführen kann, hängen von den Einstellungen ab.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-147">The operations that the task can carry out using the token depend on the settings.</span></span> <span data-ttu-id="2d3e9-148">Beispielsweise kann ein Vorgang Auftrags Berechtigungen anfordern, um dem Auftrag weitere Aufgaben hinzuzufügen oder den Status des Auftrags oder anderer Aufgaben zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-148">For example, a task can request job permissions in order to add other tasks to the job, or check the status of the job or of other tasks.</span></span>

```yaml
Type: PSAuthenticationTokenSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e9-149">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="2d3e9-149">-BatchContext</span></span>
<span data-ttu-id="2d3e9-150">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-150">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2d3e9-151">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-151">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2d3e9-152">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-152">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2d3e9-153">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-153">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2d3e9-154">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-154">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e9-155">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="2d3e9-155">-CommandLine</span></span>
<span data-ttu-id="2d3e9-156">Gibt die Befehlszeile für die Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-156">Specifies the command line for the task.</span></span>

```yaml
Type: String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e9-157">-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="2d3e9-157">-Constraints</span></span>
<span data-ttu-id="2d3e9-158">Gibt die Ausführungs Einschränkungen an, die für diese Aufgabe gelten.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-158">Specifies the execution constraints that apply to this task.</span></span>

```yaml
Type: PSTaskConstraints
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e9-159">-ContainerSettings</span><span class="sxs-lookup"><span data-stu-id="2d3e9-159">-ContainerSettings</span></span>
<span data-ttu-id="2d3e9-160">Die Einstellungen für den Container, unter dem die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-160">The settings for the container under which the task runs.</span></span>

<span data-ttu-id="2d3e9-161">Wenn der Pool, auf dem diese Aufgabe ausgeführt wird, containerConfiguration festgelegte ist, muss dieser ebenfalls festgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-161">If the pool that will run this task has containerConfiguration set, this must be set as well.</span></span> <span data-ttu-id="2d3e9-162">Wenn der Pool, in dem diese Aufgabe ausgeführt wird, nicht containerConfiguration festgelegten Wert aufweist, darf dieser nicht festgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-162">If the pool that will run this task doesn't have containerConfiguration set, this must not be set.</span></span> <span data-ttu-id="2d3e9-163">Wenn dies angegeben ist, werden alle Verzeichnisse rekursiv unterhalb der AZ_BATCH_NODE_ROOT_DIR (der Stamm von Azure-Batch Verzeichnissen auf dem Knoten) dem Container zugeordnet, alle Vorgangs Umgebungsvariablen werden dem Container zugeordnet, und die Task Befehlszeile wird im Container ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-163">When this is specified, all directories recursively below the AZ_BATCH_NODE_ROOT_DIR (the root of Azure Batch directories on the node) are mapped into the container, all task environment variables are mapped into the container, and the task command line is executed in the container.</span></span>

```yaml
Type: PSTaskContainerSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e9-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d3e9-164">-DefaultProfile</span></span>
<span data-ttu-id="2d3e9-165">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e9-166">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="2d3e9-166">-DependsOn</span></span>
<span data-ttu-id="2d3e9-167">Gibt an, dass die Aufgabe von anderen Aufgaben abhängt.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-167">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="2d3e9-168">Die Aufgabe wird erst geplant, wenn alle abhängigen Aufgaben erfolgreich abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-168">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

```yaml
Type: TaskDependencies
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e9-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2d3e9-169">-DisplayName</span></span>
<span data-ttu-id="2d3e9-170">Gibt den Anzeigenamen der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-170">Specifies the display name of the task.</span></span>

```yaml
Type: String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e9-171">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="2d3e9-171">-EnvironmentSettings</span></span>
<span data-ttu-id="2d3e9-172">Gibt die Umgebungseinstellungen als Schlüssel-Wert-Paare an, die dieses Cmdlet der Aufgabe hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-172">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="2d3e9-173">Der Schlüssel ist der Name der Umgebungseinstellung.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-173">The key is the environment setting name.</span></span>
<span data-ttu-id="2d3e9-174">Der Wert ist die Umgebungseinstellung.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-174">The value is the environment setting.</span></span>

```yaml
Type: IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: EnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e9-175">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="2d3e9-175">-ExitConditions</span></span>
```yaml
Type: PSExitConditions
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e9-176">-ID</span><span class="sxs-lookup"><span data-stu-id="2d3e9-176">-Id</span></span>
<span data-ttu-id="2d3e9-177">Gibt die ID der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-177">Specifies the ID of the task.</span></span>

```yaml
Type: String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e9-178">-Job</span><span class="sxs-lookup"><span data-stu-id="2d3e9-178">-Job</span></span>
<span data-ttu-id="2d3e9-179">Gibt den Auftrag an, unter dem dieses Cmdlet die Aufgabe erstellt.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-179">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="2d3e9-180">Verwenden Sie das Get-AzureBatchJob-Cmdlet, um ein **PSCloudJob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-180">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: JobObject_Bulk, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e9-181">-JobId</span><span class="sxs-lookup"><span data-stu-id="2d3e9-181">-JobId</span></span>
<span data-ttu-id="2d3e9-182">Gibt die ID des Auftrags an, unter dem dieses Cmdlet die Aufgabe erstellt.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-182">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

```yaml
Type: String
Parameter Sets: JobId_Single, JobId_Bulk
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e9-183">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="2d3e9-183">-MultiInstanceSettings</span></span>
<span data-ttu-id="2d3e9-184">Gibt Informationen dazu an, wie eine Aufgabe mit mehreren Instanzen ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-184">Specifies information about how to run a multi-instance task.</span></span>

```yaml
Type: PSMultiInstanceSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e9-185">-Outputdatei</span><span class="sxs-lookup"><span data-stu-id="2d3e9-185">-OutputFile</span></span>
<span data-ttu-id="2d3e9-186">Ruft eine Liste der Dateien ab, die vom Batch Dienst nach dem Ausführen der Befehlszeile vom Compute-Knoten hochgeladen werden, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-186">Gets or sets a list of files that the Batch service will upload from the compute node after running the command line.</span></span>

<span data-ttu-id="2d3e9-187">Bei Aufgaben mit mehreren Instanzen werden die Dateien nur vom Compute-Knoten hochgeladen, auf dem die primäre Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-187">For multi-instance tasks, the files will only be uploaded from the compute node on which the primary task is executed.</span></span>

```yaml
Type: PSOutputFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e9-188">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="2d3e9-188">-ResourceFiles</span></span>
<span data-ttu-id="2d3e9-189">Gibt Ressourcendateien als Schlüssel-Wert-Paare an, die für die Aufgabe erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-189">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="2d3e9-190">Der Schlüssel ist der Ressourcen Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-190">The key is the resource file path.</span></span>
<span data-ttu-id="2d3e9-191">Der Wert ist die BLOB-Quelle der Ressourcendatei.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-191">The value is the resource file blob source.</span></span>

```yaml
Type: IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ResourceFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e9-192">-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="2d3e9-192">-Tasks</span></span>
<span data-ttu-id="2d3e9-193">Gibt die Sammlung von Aufgaben an, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-193">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="2d3e9-194">Jede Aufgabe muss über eine eindeutige ID verfügen.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-194">Each task must have a unique ID.</span></span>

```yaml
Type: PSCloudTask[]
Parameter Sets: JobId_Bulk, JobObject_Bulk
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e9-195">-User Identity</span><span class="sxs-lookup"><span data-stu-id="2d3e9-195">-UserIdentity</span></span>
<span data-ttu-id="2d3e9-196">Die Benutzeridentität, unter der die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-196">The user identity under which the task runs.</span></span>

```yaml
Type: PSUserIdentity
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3e9-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d3e9-197">CommonParameters</span></span>
<span data-ttu-id="2d3e9-198">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d3e9-199">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d3e9-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d3e9-200">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d3e9-200">INPUTS</span></span>

### <span data-ttu-id="2d3e9-201">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2d3e9-201">BatchAccountContext</span></span>
<span data-ttu-id="2d3e9-202">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-202">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="2d3e9-203">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="2d3e9-203">PSCloudJob</span></span>
<span data-ttu-id="2d3e9-204">Der Parameter ' Job ' akzeptiert den Wert vom Typ ' PSCloudJob ' aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2d3e9-204">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="2d3e9-205">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d3e9-205">OUTPUTS</span></span>

## <span data-ttu-id="2d3e9-206">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d3e9-206">NOTES</span></span>

## <span data-ttu-id="2d3e9-207">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d3e9-207">RELATED LINKS</span></span>

[<span data-ttu-id="2d3e9-208">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2d3e9-208">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="2d3e9-209">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="2d3e9-209">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="2d3e9-210">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2d3e9-210">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="2d3e9-211">Neu – AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2d3e9-211">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="2d3e9-212">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2d3e9-212">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="2d3e9-213">Stopp-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2d3e9-213">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="2d3e9-214">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2d3e9-214">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


