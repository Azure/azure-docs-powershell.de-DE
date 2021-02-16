---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
ms.openlocfilehash: e067eea86e3a4350d08c5c0f9ec34b4af65b07f8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168220"
---
# <span data-ttu-id="1ce9b-101">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="1ce9b-101">Remove-AzBatchTask</span></span>

## <span data-ttu-id="1ce9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ce9b-102">SYNOPSIS</span></span>
<span data-ttu-id="1ce9b-103">Löscht eine Batchaufgabe.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-103">Deletes a Batch task.</span></span>

## <span data-ttu-id="1ce9b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ce9b-104">SYNTAX</span></span>

### <span data-ttu-id="1ce9b-105">ID</span><span class="sxs-lookup"><span data-stu-id="1ce9b-105">Id</span></span>
```
Remove-AzBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ce9b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1ce9b-106">InputObject</span></span>
```
Remove-AzBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ce9b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ce9b-107">DESCRIPTION</span></span>
<span data-ttu-id="1ce9b-108">Das **Cmdlet "Remove-AzBatchTask"** löscht eine Azure-Batch-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-108">The **Remove-AzBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="1ce9b-109">Dieses Cmdlet fordert Sie zur Bestätigung auf, es sei denn, Sie geben den Parameter *"Force"* an.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="1ce9b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1ce9b-110">EXAMPLES</span></span>

### <span data-ttu-id="1ce9b-111">Beispiel 1: Löschen einer Batchaufgabe nach ID</span><span class="sxs-lookup"><span data-stu-id="1ce9b-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="1ce9b-112">Mit diesem Befehl wird eine Aufgabe gelöscht, die die ID Task23 unter dem Auftrag mit der ID Job-0000001 hat.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="1ce9b-113">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="1ce9b-114">Verwenden Sie **das Cmdlet "Get-AzBatchAccountKey",** um der Variablen "$Context" einen Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="1ce9b-115">Beispiel 2: Löschen einer Batchaufgabe mithilfe der Pipeline ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="1ce9b-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="1ce9b-116">Mit diesem Befehl wird mithilfe des Cmdlets **"Get-AzBatchTask"** die Aufgabe "Batch" mit der ID Task26 in dem Auftrag mit der ID Job-000001 erhalten.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzBatchTask** cmdlet.</span></span>
<span data-ttu-id="1ce9b-117">Der Befehl übergibt diese Aufgabe mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1ce9b-118">Mit dem Befehl wird diese Aufgabe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-118">The command deletes that task.</span></span>
<span data-ttu-id="1ce9b-119">Dieser Befehl gibt den Parameter *"Force"* an.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="1ce9b-120">Daher fordert Sie der Befehl nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="1ce9b-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ce9b-121">PARAMETERS</span></span>

### <span data-ttu-id="1ce9b-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1ce9b-122">-BatchContext</span></span>
<span data-ttu-id="1ce9b-123">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1ce9b-124">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-124">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1ce9b-125">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-125">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1ce9b-126">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1ce9b-127">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1ce9b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ce9b-128">-DefaultProfile</span></span>
<span data-ttu-id="1ce9b-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ce9b-130">-Force</span><span class="sxs-lookup"><span data-stu-id="1ce9b-130">-Force</span></span>
<span data-ttu-id="1ce9b-131">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1ce9b-132">-ID</span><span class="sxs-lookup"><span data-stu-id="1ce9b-132">-Id</span></span>
<span data-ttu-id="1ce9b-133">Gibt die ID der Aufgabe an, die von diesem Cmdlet gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="1ce9b-134">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="1ce9b-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ce9b-135">-InputObject</span></span>
<span data-ttu-id="1ce9b-136">Gibt die Aufgabe an, die mit diesem Cmdlet gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="1ce9b-137">Verwenden Sie zum Abrufen **eines PSCloudTask-Objekts** das Get-AzBatchTask-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-137">To obtain a **PSCloudTask** object, use  the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="1ce9b-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="1ce9b-138">-JobId</span></span>
<span data-ttu-id="1ce9b-139">Gibt die ID des Auftrags an, der den Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="1ce9b-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ce9b-140">-Confirm</span></span>
<span data-ttu-id="1ce9b-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ce9b-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1ce9b-142">-WhatIf</span></span>
<span data-ttu-id="1ce9b-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ce9b-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ce9b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ce9b-145">CommonParameters</span></span>
<span data-ttu-id="1ce9b-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ce9b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ce9b-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ce9b-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ce9b-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1ce9b-148">INPUTS</span></span>

### <span data-ttu-id="1ce9b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="1ce9b-149">System.String</span></span>

### <span data-ttu-id="1ce9b-150">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="1ce9b-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="1ce9b-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1ce9b-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1ce9b-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1ce9b-152">OUTPUTS</span></span>

### <span data-ttu-id="1ce9b-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="1ce9b-153">System.Void</span></span>

## <span data-ttu-id="1ce9b-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1ce9b-154">NOTES</span></span>

## <span data-ttu-id="1ce9b-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1ce9b-155">RELATED LINKS</span></span>

[<span data-ttu-id="1ce9b-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="1ce9b-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="1ce9b-157">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="1ce9b-157">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="1ce9b-158">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="1ce9b-158">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="1ce9b-159">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="1ce9b-159">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="1ce9b-160">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="1ce9b-160">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="1ce9b-161">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="1ce9b-161">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
