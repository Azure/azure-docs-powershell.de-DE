---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
ms.openlocfilehash: 8e3633e88bc3c0972df0d667ed1002571d5ec142
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478746"
---
# <span data-ttu-id="0d230-101">Get-AzureBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="0d230-101">Get-AzureBatchSubtask</span></span>

## <span data-ttu-id="0d230-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d230-102">SYNOPSIS</span></span>
<span data-ttu-id="0d230-103">Ruft die Untervorgangs Informationen der angegebenen Aufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="0d230-103">Gets the subtask information of the specified task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d230-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d230-104">SYNTAX</span></span>

### <span data-ttu-id="0d230-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="0d230-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d230-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="0d230-106">ParentObject</span></span>
```
Get-AzureBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d230-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d230-107">DESCRIPTION</span></span>
<span data-ttu-id="0d230-108">Mit dem Cmdlet **Get-AzureBatchSubtask werden** die Teilvorgangsinformationen zur angegebenen Aufgabe abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0d230-108">The **Get-AzureBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="0d230-109">Teilvorgänge bieten parallele Verarbeitung für einzelne Aufgaben und ermöglichen eine präzise Überwachung der Aufgabenausführung und des Fortschritts.</span><span class="sxs-lookup"><span data-stu-id="0d230-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="0d230-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d230-110">EXAMPLES</span></span>

### <span data-ttu-id="0d230-111">Beispiel 1: Zurückgeben aller Teilvorgänge für eine angegebene Aufgabe</span><span class="sxs-lookup"><span data-stu-id="0d230-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="0d230-112">Mit diesen Befehlen werden alle Teilvorgänge für die Aufgabe mit der ID MyTask zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0d230-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="0d230-113">Dazu erstellt der erste Befehl im Beispiel einen Objektverweis auf die Kontoschlüssel für das Stapelverarbeitungs Konto contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="0d230-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="0d230-114">Dieser Objektverweis wird in einer Variablen mit dem Namen $Context gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0d230-114">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="0d230-115">Der zweite Befehl verwendet dann diesen Objektverweis und das Cmdlet " **Get-AzureBatchSubtask** ", um alle Teilvorgänge für MyTask zurückzugeben, eine Aufgabe, die als Teil von Job Job-01 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d230-115">The second command then uses that object reference and the **Get-AzureBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="0d230-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d230-116">PARAMETERS</span></span>

### <span data-ttu-id="0d230-117">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="0d230-117">-BatchContext</span></span>
<span data-ttu-id="0d230-118">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="0d230-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0d230-119">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0d230-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0d230-120">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0d230-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0d230-121">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="0d230-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0d230-122">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="0d230-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0d230-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d230-123">-DefaultProfile</span></span>
<span data-ttu-id="0d230-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0d230-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d230-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="0d230-125">-JobId</span></span>
<span data-ttu-id="0d230-126">Gibt die ID des Auftrags an, der die Aufgabe enthält, deren Teilvorgänge dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="0d230-126">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d230-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0d230-127">-MaxCount</span></span>
<span data-ttu-id="0d230-128">Gibt die maximale Anzahl von Teilvorgängen an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0d230-128">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="0d230-129">Wenn Sie den Wert 0 (null) oder weniger angeben, verwendet das Cmdlet keine Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="0d230-129">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="0d230-130">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="0d230-130">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d230-131">– Aufgabe</span><span class="sxs-lookup"><span data-stu-id="0d230-131">-Task</span></span>
<span data-ttu-id="0d230-132">Gibt einen Objektverweis auf die Aufgabe an, die die Teilvorgänge enthält, die dieses Cmdlet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0d230-132">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="0d230-133">Dieser Objektverweis wird mithilfe des Get-AzureBatchTask-Cmdlets erstellt und speichert das zurückgegebene Objekt in einer Variablen.</span><span class="sxs-lookup"><span data-stu-id="0d230-133">This object reference is created by using the Get-AzureBatchTask cmdlet and storing the returned object in a variable.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d230-134">-Task-Nr</span><span class="sxs-lookup"><span data-stu-id="0d230-134">-TaskId</span></span>
<span data-ttu-id="0d230-135">Gibt die ID der Aufgabe an, deren Teilvorgänge dieses Cmdlet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0d230-135">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d230-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d230-136">CommonParameters</span></span>
<span data-ttu-id="0d230-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d230-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d230-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d230-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d230-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d230-139">INPUTS</span></span>

### <span data-ttu-id="0d230-140">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0d230-140">BatchAccountContext</span></span>
<span data-ttu-id="0d230-141">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0d230-141">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="0d230-142">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="0d230-142">PSCloudTask</span></span>
<span data-ttu-id="0d230-143">Der Parameter "Aufgabe" akzeptiert den Wert vom Typ "PSCloudTask" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0d230-143">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="0d230-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d230-144">OUTPUTS</span></span>

###  
<span data-ttu-id="0d230-145">Dieses Cmdlet gibt Instanzen des **PSSubtaskInformation** -Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="0d230-145">This cmdlet returns instances of the **PSSubtaskInformation** object.</span></span>

## <span data-ttu-id="0d230-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d230-146">NOTES</span></span>

## <span data-ttu-id="0d230-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d230-147">RELATED LINKS</span></span>

[<span data-ttu-id="0d230-148">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="0d230-148">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)


