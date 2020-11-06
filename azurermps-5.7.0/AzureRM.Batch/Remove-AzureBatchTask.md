---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
ms.openlocfilehash: 775425b0da46ef6c2b22e1c28725b323b3071974
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503074"
---
# <span data-ttu-id="ac8d8-101">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ac8d8-101">Remove-AzureBatchTask</span></span>

## <span data-ttu-id="ac8d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac8d8-102">SYNOPSIS</span></span>
<span data-ttu-id="ac8d8-103">Löscht eine Batch Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-103">Deletes a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac8d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac8d8-104">SYNTAX</span></span>

### <span data-ttu-id="ac8d8-105">ID</span><span class="sxs-lookup"><span data-stu-id="ac8d8-105">Id</span></span>
```
Remove-AzureBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac8d8-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ac8d8-106">InputObject</span></span>
```
Remove-AzureBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac8d8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac8d8-107">DESCRIPTION</span></span>
<span data-ttu-id="ac8d8-108">Das Cmdlet **Remove-AzureBatchTask** löscht eine Azure-Batch Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-108">The **Remove-AzureBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="ac8d8-109">Dieses Cmdlet fordert Sie zur Bestätigung auf, es sei denn, Sie geben den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="ac8d8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac8d8-110">EXAMPLES</span></span>

### <span data-ttu-id="ac8d8-111">Beispiel 1: Löschen einer stapelverarbeitungsaufgabe nach ID</span><span class="sxs-lookup"><span data-stu-id="ac8d8-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="ac8d8-112">Dieser Befehl löscht eine Aufgabe mit der ID Task23 unter dem Job, der die ID Job-000001 hat.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="ac8d8-113">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="ac8d8-114">Verwenden Sie das Cmdlet **Get-AzureRmBatchAccountKeys** , um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ac8d8-115">Beispiel 2: Löschen einer Batch Aufgabe mithilfe der Pipeline ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="ac8d8-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzureBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="ac8d8-116">Dieser Befehl ruft die Batch Aufgabe mit der ID Task26 in dem Auftrag ab, der die ID Job-000001 mit dem Cmdlet **Get-AzureBatchTask** enthält.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzureBatchTask** cmdlet.</span></span>
<span data-ttu-id="ac8d8-117">Der Befehl übergibt diesen Vorgang mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ac8d8-118">Der Befehl löscht diese Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-118">The command deletes that task.</span></span>
<span data-ttu-id="ac8d8-119">Mit diesem Befehl wird der *Force* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ac8d8-120">Daher werden Sie vom Befehl nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ac8d8-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac8d8-121">PARAMETERS</span></span>

### <span data-ttu-id="ac8d8-122">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="ac8d8-122">-BatchContext</span></span>
<span data-ttu-id="ac8d8-123">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ac8d8-124">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-124">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ac8d8-125">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-125">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ac8d8-126">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ac8d8-127">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ac8d8-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac8d8-128">-DefaultProfile</span></span>
<span data-ttu-id="ac8d8-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac8d8-130">-Force</span><span class="sxs-lookup"><span data-stu-id="ac8d8-130">-Force</span></span>
<span data-ttu-id="ac8d8-131">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-131">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8d8-132">-ID</span><span class="sxs-lookup"><span data-stu-id="ac8d8-132">-Id</span></span>
<span data-ttu-id="ac8d8-133">Gibt die ID der vom Cmdlet gelöschten Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="ac8d8-134">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="ac8d8-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ac8d8-135">-InputObject</span></span>
<span data-ttu-id="ac8d8-136">Gibt die Aufgabe an, die dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="ac8d8-137">Verwenden Sie das Get-AzureBatchTask-Cmdlet, um ein **PSCloudTask** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-137">To obtain a **PSCloudTask** object, use  the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="ac8d8-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="ac8d8-138">-JobId</span></span>
<span data-ttu-id="ac8d8-139">Gibt die ID des Auftrags an, der die Aufgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="ac8d8-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ac8d8-140">-Confirm</span></span>
<span data-ttu-id="ac8d8-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac8d8-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac8d8-142">-WhatIf</span></span>
<span data-ttu-id="ac8d8-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac8d8-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac8d8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac8d8-145">CommonParameters</span></span>
<span data-ttu-id="ac8d8-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac8d8-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac8d8-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac8d8-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac8d8-148">INPUTS</span></span>

### <span data-ttu-id="ac8d8-149">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ac8d8-149">BatchAccountContext</span></span>
<span data-ttu-id="ac8d8-150">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-150">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ac8d8-151">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="ac8d8-151">PSCloudTask</span></span>
<span data-ttu-id="ac8d8-152">Der Parameter "Inputobject" akzeptiert den Wert vom Typ "PSCloudTask" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ac8d8-152">Parameter 'InputObject' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="ac8d8-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac8d8-153">OUTPUTS</span></span>

## <span data-ttu-id="ac8d8-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac8d8-154">NOTES</span></span>

## <span data-ttu-id="ac8d8-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac8d8-155">RELATED LINKS</span></span>

[<span data-ttu-id="ac8d8-156">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ac8d8-156">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ac8d8-157">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ac8d8-157">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="ac8d8-158">Neu – AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ac8d8-158">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="ac8d8-159">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ac8d8-159">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="ac8d8-160">Stopp-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ac8d8-160">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="ac8d8-161">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="ac8d8-161">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


