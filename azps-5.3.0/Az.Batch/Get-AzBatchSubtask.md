---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
ms.openlocfilehash: 4a1278734e6c9f40dc7495acb92f847d7b2cd32d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471162"
---
# <span data-ttu-id="8220e-101">Get-AzBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="8220e-101">Get-AzBatchSubtask</span></span>

## <span data-ttu-id="8220e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8220e-102">SYNOPSIS</span></span>
<span data-ttu-id="8220e-103">Ruft die Teilvorganginformationen des angegebenen Vorgangs ab.</span><span class="sxs-lookup"><span data-stu-id="8220e-103">Gets the subtask information of the specified task.</span></span>

## <span data-ttu-id="8220e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8220e-104">SYNTAX</span></span>

### <span data-ttu-id="8220e-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="8220e-105">ODataFilter (Default)</span></span>
```
Get-AzBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8220e-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="8220e-106">ParentObject</span></span>
```
Get-AzBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8220e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8220e-107">DESCRIPTION</span></span>
<span data-ttu-id="8220e-108">Das **Cmdlet "Get-AzBatchSubtask"** ruft die Teilvorgangsinformationen zur angegebenen Aufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="8220e-108">The **Get-AzBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="8220e-109">Teilvorgänge bieten eine parallele Verarbeitung für einzelne Aufgaben und ermöglichen eine präzise Überwachung der Ausführung und des Fortschritts von Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="8220e-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="8220e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8220e-110">EXAMPLES</span></span>

### <span data-ttu-id="8220e-111">Beispiel 1: Zurückgeben aller Teilvorgänge für einen angegebenen Vorgang</span><span class="sxs-lookup"><span data-stu-id="8220e-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="8220e-112">Diese Befehle geben alle Teilvorgänge für den Vorgang mit der ID myTask zurück.</span><span class="sxs-lookup"><span data-stu-id="8220e-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="8220e-113">Dazu erstellt der erste Befehl im Beispiel einen Objektverweis auf die Kontoschlüssel für das Batchkonto "contosobatchaccount".</span><span class="sxs-lookup"><span data-stu-id="8220e-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="8220e-114">Dieser Objektverweis wird in einer Variablen namens "$context.</span><span class="sxs-lookup"><span data-stu-id="8220e-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="8220e-115">Der zweite Befehl verwendet dann diesen Objektverweis und das **Cmdlet "Get-AzBatchSubtask",** um alle Teilvorgänge für "myTask" zurückzukehren, eine Aufgabe, die als Teil von Job-01 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8220e-115">The second command then uses that object reference and the **Get-AzBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="8220e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8220e-116">PARAMETERS</span></span>

### <span data-ttu-id="8220e-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8220e-117">-BatchContext</span></span>
<span data-ttu-id="8220e-118">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8220e-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8220e-119">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="8220e-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8220e-120">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8220e-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8220e-121">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="8220e-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8220e-122">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8220e-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8220e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8220e-123">-DefaultProfile</span></span>
<span data-ttu-id="8220e-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8220e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8220e-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="8220e-125">-JobId</span></span>
<span data-ttu-id="8220e-126">Gibt die ID des Auftrags an, der den Vorgang enthält, dessen Teilvorgänge dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="8220e-126">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8220e-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="8220e-127">-MaxCount</span></span>
<span data-ttu-id="8220e-128">Gibt die maximale Anzahl der zurückzukehrenden Teilvorgänge an.</span><span class="sxs-lookup"><span data-stu-id="8220e-128">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="8220e-129">Wenn Sie einen Wert von Null (0) oder kleiner angeben, wird für das Cmdlet keine Obergrenze verwendet.</span><span class="sxs-lookup"><span data-stu-id="8220e-129">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="8220e-130">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="8220e-130">The default value is 1000.</span></span>

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

### <span data-ttu-id="8220e-131">-Task</span><span class="sxs-lookup"><span data-stu-id="8220e-131">-Task</span></span>
<span data-ttu-id="8220e-132">Gibt einen Objektverweis auf den Vorgang an, der die von diesem Cmdlet zurückgegebenen Teilvorgänge enthält.</span><span class="sxs-lookup"><span data-stu-id="8220e-132">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="8220e-133">Dieser Objektverweis wird mithilfe des cmdlets Get-AzBatchTask erstellt und das zurückgegebene Objekt in einer Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8220e-133">This object reference is created by using the Get-AzBatchTask cmdlet and storing the returned object in a variable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8220e-134">-TaskId</span><span class="sxs-lookup"><span data-stu-id="8220e-134">-TaskId</span></span>
<span data-ttu-id="8220e-135">Gibt die ID des Vorgangs an, dessen Teilvorgänge dieses Cmdlet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8220e-135">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8220e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8220e-136">CommonParameters</span></span>
<span data-ttu-id="8220e-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8220e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8220e-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8220e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8220e-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8220e-139">INPUTS</span></span>

### <span data-ttu-id="8220e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8220e-140">System.String</span></span>

### <span data-ttu-id="8220e-141">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="8220e-141">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="8220e-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8220e-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8220e-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8220e-143">OUTPUTS</span></span>

### <span data-ttu-id="8220e-144">Microsoft.Azure.Commands.Batch. Models.PSSubtaskInformation</span><span class="sxs-lookup"><span data-stu-id="8220e-144">Microsoft.Azure.Commands.Batch.Models.PSSubtaskInformation</span></span>

## <span data-ttu-id="8220e-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8220e-145">NOTES</span></span>

## <span data-ttu-id="8220e-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8220e-146">RELATED LINKS</span></span>

[<span data-ttu-id="8220e-147">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="8220e-147">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)


