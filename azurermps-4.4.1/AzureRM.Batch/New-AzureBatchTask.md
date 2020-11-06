---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
ms.openlocfilehash: dd8825be6491b0a0c8c8589f77180b38f9f230d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497898"
---
# <span data-ttu-id="37386-101">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="37386-101">New-AzureBatchTask</span></span>

## <span data-ttu-id="37386-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37386-102">SYNOPSIS</span></span>
<span data-ttu-id="37386-103">Erstellt eine Batch Aufgabe unter einem Auftrag.</span><span class="sxs-lookup"><span data-stu-id="37386-103">Creates a Batch task under a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37386-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37386-104">SYNTAX</span></span>

### <span data-ttu-id="37386-105">JobId_Single (Standard)</span><span class="sxs-lookup"><span data-stu-id="37386-105">JobId_Single (Default)</span></span>
```
New-AzureBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37386-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="37386-106">JobId_Bulk</span></span>
```
New-AzureBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37386-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="37386-107">JobObject_Bulk</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37386-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="37386-108">JobObject_Single</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37386-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37386-109">DESCRIPTION</span></span>
<span data-ttu-id="37386-110">Das Cmdlet **New-AzureBatchTask** erstellt eine Azure-Batch Aufgabe unter dem Auftrag, der durch den *JobID* -Parameter oder den *Job* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="37386-110">The **New-AzureBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="37386-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37386-111">EXAMPLES</span></span>

### <span data-ttu-id="37386-112">Beispiel 1: Erstellen einer Batch Aufgabe</span><span class="sxs-lookup"><span data-stu-id="37386-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="37386-113">Mit diesem Befehl wird eine Aufgabe erstellt, die die ID Task23 unter dem Auftrag mit dem Auftrags-000001.</span><span class="sxs-lookup"><span data-stu-id="37386-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="37386-114">Der Task führt den angegebenen Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="37386-114">The task runs the specified command.</span></span>
<span data-ttu-id="37386-115">Verwenden Sie das Cmdlet **Get-AzureRmBatchAccountKeys** , um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="37386-115">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="37386-116">Beispiel 2: Erstellen einer Batch Aufgabe</span><span class="sxs-lookup"><span data-stu-id="37386-116">Example 2: Create a Batch task</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -RunElevated -BatchContext $Context
```

<span data-ttu-id="37386-117">Dieser Befehl ruft mit dem Cmdlet **Get-AzureBatchJob** den Stapelverarbeitungsauftrag ab, der die ID Job-000001 hat.</span><span class="sxs-lookup"><span data-stu-id="37386-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzureBatchJob** cmdlet.</span></span>
<span data-ttu-id="37386-118">Der Befehl übergibt diesen Auftrag mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37386-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="37386-119">Der Befehl erstellt eine Aufgabe mit der ID Task26 unter diesem Auftrag.</span><span class="sxs-lookup"><span data-stu-id="37386-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="37386-120">Die Aufgabe führt den angegebenen Befehl mithilfe von erhöhten Berechtigungen aus.</span><span class="sxs-lookup"><span data-stu-id="37386-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="37386-121">Beispiel 3: Hinzufügen einer Sammlung von Aufgaben zum angegebenen Auftrag mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="37386-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="37386-122">Der erste Befehl erstellt einen Objektverweis auf die Kontoschlüssel für das Batch Konto mit dem Namen ContosoBatchAccount mithilfe von **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="37386-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="37386-123">Der Befehl speichert diesen Objektverweis in der $Context Variablen.</span><span class="sxs-lookup"><span data-stu-id="37386-123">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="37386-124">Die nächsten beiden Befehle erstellen **PSCloudTask** -Objekte mithilfe des New-Object-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="37386-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="37386-125">Die Befehle speichern die Aufgaben in den Variablen $Task 01 und $Task 02.</span><span class="sxs-lookup"><span data-stu-id="37386-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="37386-126">Der endgültige Befehl ruft den Stapelverarbeitungsauftrag ab, der die ID Job-000001 mithilfe von **Get-AzureBatchJob**.</span><span class="sxs-lookup"><span data-stu-id="37386-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzureBatchJob**.</span></span>
<span data-ttu-id="37386-127">Anschließend übergibt der Befehl diesen Auftrag mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37386-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="37386-128">Der Befehl fügt eine Sammlung von Aufgaben unter diesem Auftrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="37386-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="37386-129">Der Befehl verwendet den in $context gespeicherten Kontext.</span><span class="sxs-lookup"><span data-stu-id="37386-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="37386-130">Beispiel 4: Hinzufügen einer Sammlung von Aufgaben zum angegebenen Auftrag</span><span class="sxs-lookup"><span data-stu-id="37386-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzureBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="37386-131">Der erste Befehl erstellt einen Objektverweis auf die Kontoschlüssel für das Batch Konto mit dem Namen ContosoBatchAccount mithilfe von **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="37386-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="37386-132">Der Befehl speichert diesen Objektverweis in der $Context Variablen.</span><span class="sxs-lookup"><span data-stu-id="37386-132">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="37386-133">Die nächsten beiden Befehle erstellen **PSCloudTask** -Objekte mithilfe des New-Object-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="37386-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="37386-134">Die Befehle speichern die Aufgaben in den Variablen $Task 01 und $Task 02.</span><span class="sxs-lookup"><span data-stu-id="37386-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="37386-135">Der letzte Befehl fügt die Aufgaben, die in $Task 01 und $Task 02 gespeichert sind, unter dem Job hinzu, der die ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="37386-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

## <span data-ttu-id="37386-136">Parameter</span><span class="sxs-lookup"><span data-stu-id="37386-136">PARAMETERS</span></span>

### <span data-ttu-id="37386-137">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="37386-137">-AffinityInformation</span></span>
<span data-ttu-id="37386-138">Gibt einen Orts Hinweis an, der vom Stapelverarbeitungs Dienst zum Auswählen eines Knotens verwendet wird, für den die Aufgabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="37386-138">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

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

### <span data-ttu-id="37386-139">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="37386-139">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37386-140">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="37386-140">-BatchContext</span></span>
<span data-ttu-id="37386-141">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="37386-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="37386-142">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37386-142">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="37386-143">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="37386-143">-CommandLine</span></span>
<span data-ttu-id="37386-144">Gibt die Befehlszeile für die Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="37386-144">Specifies the command line for the task.</span></span>

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

### <span data-ttu-id="37386-145">-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="37386-145">-Constraints</span></span>
<span data-ttu-id="37386-146">Gibt die Ausführungs Einschränkungen an, die für diese Aufgabe gelten.</span><span class="sxs-lookup"><span data-stu-id="37386-146">Specifies the execution constraints that apply to this task.</span></span>

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

### <span data-ttu-id="37386-147">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="37386-147">-DependsOn</span></span>
<span data-ttu-id="37386-148">Gibt an, dass die Aufgabe von anderen Aufgaben abhängt.</span><span class="sxs-lookup"><span data-stu-id="37386-148">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="37386-149">Die Aufgabe wird erst geplant, wenn alle abhängigen Aufgaben erfolgreich abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="37386-149">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

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

### <span data-ttu-id="37386-150">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="37386-150">-DisplayName</span></span>
<span data-ttu-id="37386-151">Gibt den Anzeigenamen der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="37386-151">Specifies the display name of the task.</span></span>

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

### <span data-ttu-id="37386-152">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="37386-152">-EnvironmentSettings</span></span>
<span data-ttu-id="37386-153">Gibt die Umgebungseinstellungen als Schlüssel-Wert-Paare an, die dieses Cmdlet der Aufgabe hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="37386-153">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="37386-154">Der Schlüssel ist der Name der Umgebungseinstellung.</span><span class="sxs-lookup"><span data-stu-id="37386-154">The key is the environment setting name.</span></span>
<span data-ttu-id="37386-155">Der Wert ist die Umgebungseinstellung.</span><span class="sxs-lookup"><span data-stu-id="37386-155">The value is the environment setting.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37386-156">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="37386-156">-ExitConditions</span></span>
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

### <span data-ttu-id="37386-157">-ID</span><span class="sxs-lookup"><span data-stu-id="37386-157">-Id</span></span>
<span data-ttu-id="37386-158">Gibt die ID der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="37386-158">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="37386-159">-Job</span><span class="sxs-lookup"><span data-stu-id="37386-159">-Job</span></span>
<span data-ttu-id="37386-160">Gibt den Auftrag an, unter dem dieses Cmdlet die Aufgabe erstellt.</span><span class="sxs-lookup"><span data-stu-id="37386-160">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="37386-161">Verwenden Sie das Get-AzureBatchJob-Cmdlet, um ein **PSCloudJob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="37386-161">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="37386-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="37386-162">-JobId</span></span>
<span data-ttu-id="37386-163">Gibt die ID des Auftrags an, unter dem dieses Cmdlet die Aufgabe erstellt.</span><span class="sxs-lookup"><span data-stu-id="37386-163">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

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

### <span data-ttu-id="37386-164">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="37386-164">-MultiInstanceSettings</span></span>
<span data-ttu-id="37386-165">Gibt Informationen dazu an, wie eine Aufgabe mit mehreren Instanzen ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="37386-165">Specifies information about how to run a multi-instance task.</span></span>

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

### <span data-ttu-id="37386-166">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="37386-166">-ResourceFiles</span></span>
<span data-ttu-id="37386-167">Gibt Ressourcendateien als Schlüssel-Wert-Paare an, die für die Aufgabe erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="37386-167">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="37386-168">Der Schlüssel ist der Ressourcen Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="37386-168">The key is the resource file path.</span></span>
<span data-ttu-id="37386-169">Der Wert ist die BLOB-Quelle der Ressourcendatei.</span><span class="sxs-lookup"><span data-stu-id="37386-169">The value is the resource file blob source.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37386-170">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="37386-170">-RunElevated</span></span>
<span data-ttu-id="37386-171">Gibt an, dass der Aufgabenprozess mit Administratorrechten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37386-171">Indicates that the task process runs with administrator privileges.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37386-172">-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="37386-172">-Tasks</span></span>
<span data-ttu-id="37386-173">Gibt die Sammlung von Aufgaben an, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="37386-173">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="37386-174">Jede Aufgabe muss über eine eindeutige ID verfügen.</span><span class="sxs-lookup"><span data-stu-id="37386-174">Each task must have a unique ID.</span></span>

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

### <span data-ttu-id="37386-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37386-175">-DefaultProfile</span></span>
<span data-ttu-id="37386-176">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="37386-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37386-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37386-177">CommonParameters</span></span>
<span data-ttu-id="37386-178">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37386-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37386-179">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37386-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37386-180">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37386-180">INPUTS</span></span>

### <span data-ttu-id="37386-181">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="37386-181">BatchAccountContext</span></span>
<span data-ttu-id="37386-182">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="37386-182">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="37386-183">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="37386-183">PSCloudJob</span></span>
<span data-ttu-id="37386-184">Der Parameter ' Job ' akzeptiert den Wert vom Typ ' PSCloudJob ' aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="37386-184">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="37386-185">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37386-185">OUTPUTS</span></span>

## <span data-ttu-id="37386-186">Notizen</span><span class="sxs-lookup"><span data-stu-id="37386-186">NOTES</span></span>

## <span data-ttu-id="37386-187">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37386-187">RELATED LINKS</span></span>

[<span data-ttu-id="37386-188">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="37386-188">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="37386-189">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="37386-189">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="37386-190">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="37386-190">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="37386-191">Neu – AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="37386-191">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="37386-192">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="37386-192">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="37386-193">Stopp-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="37386-193">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="37386-194">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="37386-194">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


