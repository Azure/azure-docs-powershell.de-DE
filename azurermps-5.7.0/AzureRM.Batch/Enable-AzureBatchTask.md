---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: 09e2c8dd4ce1eab68eb2a4237e022034696f9769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664242"
---
# <span data-ttu-id="af595-101">Enable-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="af595-101">Enable-AzureBatchTask</span></span>

## <span data-ttu-id="af595-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="af595-102">SYNOPSIS</span></span>
<span data-ttu-id="af595-103">Reaktiviert eine Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="af595-103">Reactivates a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af595-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="af595-104">SYNTAX</span></span>

### <span data-ttu-id="af595-105">ID</span><span class="sxs-lookup"><span data-stu-id="af595-105">Id</span></span>
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af595-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="af595-106">InputObject</span></span>
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af595-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="af595-107">DESCRIPTION</span></span>
<span data-ttu-id="af595-108">Mit dem Cmdlet **enable-AzureBatchTask** wird eine Aufgabe erneut aktiviert.</span><span class="sxs-lookup"><span data-stu-id="af595-108">The **Enable-AzureBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="af595-109">Wenn ein Vorgang seine Wiederholungsanzahl erschöpft hat, ermöglicht dieses Cmdlet dennoch die Ausführung.</span><span class="sxs-lookup"><span data-stu-id="af595-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="af595-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="af595-110">EXAMPLES</span></span>

### <span data-ttu-id="af595-111">Beispiel 1: Reaktivieren einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="af595-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="af595-112">Mit diesem Befehl wird die Aufgabe task2 in Job Job7 erneut aktiviert.</span><span class="sxs-lookup"><span data-stu-id="af595-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="af595-113">Beispiel 2: Reaktivieren einer Aufgabe mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="af595-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="af595-114">Dieser Befehl ruft die Batch Aufgabe mit der ID Task3 in dem Auftrag ab, der die ID-Job8 mit dem Get-AzureBatchTask-Cmdlet aufweist.</span><span class="sxs-lookup"><span data-stu-id="af595-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="af595-115">Der Befehl übergibt diesen Vorgang mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af595-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="af595-116">Der Befehl aktiviert diese Aufgabe erneut.</span><span class="sxs-lookup"><span data-stu-id="af595-116">The command reactivates that task.</span></span>

## <span data-ttu-id="af595-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="af595-117">PARAMETERS</span></span>

### <span data-ttu-id="af595-118">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="af595-118">-BatchContext</span></span>
<span data-ttu-id="af595-119">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="af595-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="af595-120">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="af595-120">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="af595-121">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="af595-121">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="af595-122">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="af595-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="af595-123">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="af595-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="af595-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af595-124">-DefaultProfile</span></span>
<span data-ttu-id="af595-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="af595-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af595-126">-ID</span><span class="sxs-lookup"><span data-stu-id="af595-126">-Id</span></span>
<span data-ttu-id="af595-127">Gibt die ID der Aufgabe an, die erneut aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="af595-127">Specifies the ID of the task to reactivate.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af595-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="af595-128">-JobId</span></span>
<span data-ttu-id="af595-129">Gibt die ID des Auftrags an, der die Aufgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="af595-129">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af595-130">– Aufgabe</span><span class="sxs-lookup"><span data-stu-id="af595-130">-Task</span></span>
<span data-ttu-id="af595-131">Gibt die Aufgabe an, die dieses Cmdlet reaktiviert.</span><span class="sxs-lookup"><span data-stu-id="af595-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="af595-132">Verwenden Sie das Get-AzureBatchTask-Cmdlet, um ein **PSCloudTask** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="af595-132">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af595-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="af595-133">-Confirm</span></span>
<span data-ttu-id="af595-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="af595-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af595-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af595-135">-WhatIf</span></span>
<span data-ttu-id="af595-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af595-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af595-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="af595-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af595-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af595-138">CommonParameters</span></span>
<span data-ttu-id="af595-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af595-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af595-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af595-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af595-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="af595-141">INPUTS</span></span>

### <span data-ttu-id="af595-142">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="af595-142">BatchAccountContext</span></span>
<span data-ttu-id="af595-143">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="af595-143">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="af595-144">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="af595-144">PSCloudTask</span></span>
<span data-ttu-id="af595-145">Der Parameter "Aufgabe" akzeptiert den Wert vom Typ "PSCloudTask" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="af595-145">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="af595-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="af595-146">OUTPUTS</span></span>

## <span data-ttu-id="af595-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="af595-147">NOTES</span></span>

## <span data-ttu-id="af595-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="af595-148">RELATED LINKS</span></span>

[<span data-ttu-id="af595-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="af595-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="af595-150">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="af595-150">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="af595-151">Neu – AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="af595-151">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="af595-152">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="af595-152">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="af595-153">Satz-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="af595-153">Set-AzureBatchTask</span></span>](./Set-AzureBatchTask.md)

[<span data-ttu-id="af595-154">Stopp-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="af595-154">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)


