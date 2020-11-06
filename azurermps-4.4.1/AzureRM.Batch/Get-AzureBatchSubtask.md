---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
ms.openlocfilehash: 58bed6fda4040c1af48469f4aa85f717c26c898c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505650"
---
# <span data-ttu-id="ca218-101">Get-AzureBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="ca218-101">Get-AzureBatchSubtask</span></span>

## <span data-ttu-id="ca218-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ca218-102">SYNOPSIS</span></span>
<span data-ttu-id="ca218-103">Ruft die Untervorgangs Informationen der angegebenen Aufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="ca218-103">Gets the subtask information of the specified task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca218-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca218-104">SYNTAX</span></span>

### <span data-ttu-id="ca218-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="ca218-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca218-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="ca218-106">ParentObject</span></span>
```
Get-AzureBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca218-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca218-107">DESCRIPTION</span></span>
<span data-ttu-id="ca218-108">Mit dem Cmdlet **Get-AzureBatchSubtask werden** die Teilvorgangsinformationen zur angegebenen Aufgabe abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ca218-108">The **Get-AzureBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="ca218-109">Teilvorgänge bieten parallele Verarbeitung für einzelne Aufgaben und ermöglichen eine präzise Überwachung der Aufgabenausführung und des Fortschritts.</span><span class="sxs-lookup"><span data-stu-id="ca218-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="ca218-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ca218-110">EXAMPLES</span></span>

### <span data-ttu-id="ca218-111">Beispiel 1: Zurückgeben aller Teilvorgänge für eine angegebene Aufgabe</span><span class="sxs-lookup"><span data-stu-id="ca218-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="ca218-112">Mit diesen Befehlen werden alle Teilvorgänge für die Aufgabe mit der ID MyTask zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ca218-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="ca218-113">Dazu erstellt der erste Befehl im Beispiel einen Objektverweis auf die Kontoschlüssel für das Stapelverarbeitungs Konto contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="ca218-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="ca218-114">Dieser Objektverweis wird in einer Variablen mit dem Namen $Context gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ca218-114">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="ca218-115">Der zweite Befehl verwendet dann diesen Objektverweis und das Cmdlet " **Get-AzureBatchSubtask** ", um alle Teilvorgänge für MyTask zurückzugeben, eine Aufgabe, die als Teil von Job Job-01 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca218-115">The second command then uses that object reference and the **Get-AzureBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="ca218-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca218-116">PARAMETERS</span></span>

### <span data-ttu-id="ca218-117">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="ca218-117">-BatchContext</span></span>
<span data-ttu-id="ca218-118">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="ca218-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ca218-119">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca218-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="ca218-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="ca218-120">-JobId</span></span>
<span data-ttu-id="ca218-121">Gibt die ID des Auftrags an, der die Aufgabe enthält, deren Teilvorgänge dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ca218-121">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

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

### <span data-ttu-id="ca218-122">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ca218-122">-MaxCount</span></span>
<span data-ttu-id="ca218-123">Gibt die maximale Anzahl von Teilvorgängen an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ca218-123">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="ca218-124">Wenn Sie den Wert 0 (null) oder weniger angeben, verwendet das Cmdlet keine Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="ca218-124">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="ca218-125">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="ca218-125">The default value is 1000.</span></span>

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

### <span data-ttu-id="ca218-126">– Aufgabe</span><span class="sxs-lookup"><span data-stu-id="ca218-126">-Task</span></span>
<span data-ttu-id="ca218-127">Gibt einen Objektverweis auf die Aufgabe an, die die Teilvorgänge enthält, die dieses Cmdlet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ca218-127">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="ca218-128">Dieser Objektverweis wird mithilfe des Get-AzureBatchTask-Cmdlets erstellt und speichert das zurückgegebene Objekt in einer Variablen.</span><span class="sxs-lookup"><span data-stu-id="ca218-128">This object reference is created by using the Get-AzureBatchTask cmdlet and storing the returned object in a variable.</span></span>

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

### <span data-ttu-id="ca218-129">-Task-Nr</span><span class="sxs-lookup"><span data-stu-id="ca218-129">-TaskId</span></span>
<span data-ttu-id="ca218-130">Gibt die ID der Aufgabe an, deren Teilvorgänge dieses Cmdlet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ca218-130">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

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

### <span data-ttu-id="ca218-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca218-131">-DefaultProfile</span></span>
<span data-ttu-id="ca218-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ca218-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca218-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca218-133">CommonParameters</span></span>
<span data-ttu-id="ca218-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca218-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca218-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca218-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca218-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ca218-136">INPUTS</span></span>

### <span data-ttu-id="ca218-137">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ca218-137">BatchAccountContext</span></span>
<span data-ttu-id="ca218-138">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ca218-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ca218-139">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="ca218-139">PSCloudTask</span></span>
<span data-ttu-id="ca218-140">Der Parameter "Aufgabe" akzeptiert den Wert vom Typ "PSCloudTask" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ca218-140">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="ca218-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ca218-141">OUTPUTS</span></span>

###  
<span data-ttu-id="ca218-142">Dieses Cmdlet gibt Instanzen des **PSSubtaskInformation** -Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="ca218-142">This cmdlet returns instances of the **PSSubtaskInformation** object.</span></span>

## <span data-ttu-id="ca218-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="ca218-143">NOTES</span></span>

## <span data-ttu-id="ca218-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ca218-144">RELATED LINKS</span></span>

[<span data-ttu-id="ca218-145">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ca218-145">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)


