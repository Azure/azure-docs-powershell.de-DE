---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
ms.openlocfilehash: c2b198359bbd793353c9b416a631d94cad0709fa
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847855"
---
# <span data-ttu-id="6e5bd-101">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6e5bd-101">Remove-AzBatchTask</span></span>

## <span data-ttu-id="6e5bd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e5bd-102">SYNOPSIS</span></span>
<span data-ttu-id="6e5bd-103">Löscht eine Batch Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-103">Deletes a Batch task.</span></span>

## <span data-ttu-id="6e5bd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e5bd-104">SYNTAX</span></span>

### <span data-ttu-id="6e5bd-105">ID</span><span class="sxs-lookup"><span data-stu-id="6e5bd-105">Id</span></span>
```
Remove-AzBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e5bd-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6e5bd-106">InputObject</span></span>
```
Remove-AzBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e5bd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e5bd-107">DESCRIPTION</span></span>
<span data-ttu-id="6e5bd-108">Das Cmdlet **Remove-AzBatchTask** löscht eine Azure-Batch Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-108">The **Remove-AzBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="6e5bd-109">Dieses Cmdlet fordert Sie zur Bestätigung auf, es sei denn, Sie geben den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="6e5bd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e5bd-110">EXAMPLES</span></span>

### <span data-ttu-id="6e5bd-111">Beispiel 1: Löschen einer stapelverarbeitungsaufgabe nach ID</span><span class="sxs-lookup"><span data-stu-id="6e5bd-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="6e5bd-112">Dieser Befehl löscht eine Aufgabe mit der ID Task23 unter dem Job, der die ID Job-000001 hat.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="6e5bd-113">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="6e5bd-114">Verwenden Sie das Cmdlet **Get-AzBatchAccountKeys** , um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-114">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="6e5bd-115">Beispiel 2: Löschen einer Batch Aufgabe mithilfe der Pipeline ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="6e5bd-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="6e5bd-116">Dieser Befehl ruft die Batch Aufgabe mit der ID Task26 in dem Auftrag ab, der die ID Job-000001 mit dem Cmdlet **Get-AzBatchTask** enthält.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzBatchTask** cmdlet.</span></span>
<span data-ttu-id="6e5bd-117">Der Befehl übergibt diesen Vorgang mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6e5bd-118">Der Befehl löscht diese Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-118">The command deletes that task.</span></span>
<span data-ttu-id="6e5bd-119">Mit diesem Befehl wird der *Force* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6e5bd-120">Daher werden Sie vom Befehl nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6e5bd-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e5bd-121">PARAMETERS</span></span>

### <span data-ttu-id="6e5bd-122">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="6e5bd-122">-BatchContext</span></span>
<span data-ttu-id="6e5bd-123">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6e5bd-124">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-124">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6e5bd-125">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-125">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6e5bd-126">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6e5bd-127">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6e5bd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e5bd-128">-DefaultProfile</span></span>
<span data-ttu-id="6e5bd-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e5bd-130">-Force</span><span class="sxs-lookup"><span data-stu-id="6e5bd-130">-Force</span></span>
<span data-ttu-id="6e5bd-131">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6e5bd-132">-ID</span><span class="sxs-lookup"><span data-stu-id="6e5bd-132">-Id</span></span>
<span data-ttu-id="6e5bd-133">Gibt die ID der vom Cmdlet gelöschten Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="6e5bd-134">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-134">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e5bd-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6e5bd-135">-InputObject</span></span>
<span data-ttu-id="6e5bd-136">Gibt die Aufgabe an, die dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="6e5bd-137">Verwenden Sie das Get-AzBatchTask-Cmdlet, um ein **PSCloudTask** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-137">To obtain a **PSCloudTask** object, use  the Get-AzBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e5bd-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="6e5bd-138">-JobId</span></span>
<span data-ttu-id="6e5bd-139">Gibt die ID des Auftrags an, der die Aufgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-139">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e5bd-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6e5bd-140">-Confirm</span></span>
<span data-ttu-id="6e5bd-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e5bd-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e5bd-142">-WhatIf</span></span>
<span data-ttu-id="6e5bd-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e5bd-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e5bd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e5bd-145">CommonParameters</span></span>
<span data-ttu-id="6e5bd-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e5bd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e5bd-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e5bd-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e5bd-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e5bd-148">INPUTS</span></span>

### <span data-ttu-id="6e5bd-149">System. String</span><span class="sxs-lookup"><span data-stu-id="6e5bd-149">System.String</span></span>

### <span data-ttu-id="6e5bd-150">Microsoft.Azure.Commands.Batch. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="6e5bd-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="6e5bd-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6e5bd-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6e5bd-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e5bd-152">OUTPUTS</span></span>

### <span data-ttu-id="6e5bd-153">System. void</span><span class="sxs-lookup"><span data-stu-id="6e5bd-153">System.Void</span></span>

## <span data-ttu-id="6e5bd-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e5bd-154">NOTES</span></span>

## <span data-ttu-id="6e5bd-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e5bd-155">RELATED LINKS</span></span>

[<span data-ttu-id="6e5bd-156">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6e5bd-156">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6e5bd-157">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6e5bd-157">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="6e5bd-158">Neu – AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6e5bd-158">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="6e5bd-159">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6e5bd-159">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="6e5bd-160">Stopp-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6e5bd-160">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="6e5bd-161">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6e5bd-161">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


