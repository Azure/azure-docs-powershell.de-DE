---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 9979a0fa16b8cfbe59eb8412a76cbbebcb2fca4a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471199"
---
# <span data-ttu-id="661b6-101">Enable-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="661b6-101">Enable-AzBatchTask</span></span>

## <span data-ttu-id="661b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="661b6-102">SYNOPSIS</span></span>
<span data-ttu-id="661b6-103">Reaktiviert einen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="661b6-103">Reactivates a task.</span></span>

## <span data-ttu-id="661b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="661b6-104">SYNTAX</span></span>

### <span data-ttu-id="661b6-105">ID</span><span class="sxs-lookup"><span data-stu-id="661b6-105">Id</span></span>
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="661b6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="661b6-106">InputObject</span></span>
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="661b6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="661b6-107">DESCRIPTION</span></span>
<span data-ttu-id="661b6-108">Das **Cmdlet "Enable-AzBatchTask"** reaktiviert eine Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="661b6-108">The **Enable-AzBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="661b6-109">Wenn die Anzahl der Wiederholungen für eine Aufgabe aufgebraucht ist, kann sie mit diesem Cmdlet trotzdem ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="661b6-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="661b6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="661b6-110">EXAMPLES</span></span>

### <span data-ttu-id="661b6-111">Beispiel 1: Reaktivieren eines Vorgangs</span><span class="sxs-lookup"><span data-stu-id="661b6-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="661b6-112">Mit diesem Befehl wird der Vorgang "Aufgabe2" in Auftrag7 reaktiviert.</span><span class="sxs-lookup"><span data-stu-id="661b6-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="661b6-113">Beispiel 2: Reaktivieren einer Aufgabe mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="661b6-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="661b6-114">Mit diesem Befehl wird mithilfe des Cmdlets "Stapel" die Aufgabe "Batch" mit der ID "Aufgabe3" in dem Auftrag mit der ID "Auftrag8" Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="661b6-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="661b6-115">Der Befehl übergibt diese Aufgabe mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="661b6-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="661b6-116">Der Befehl reaktiviert diese Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="661b6-116">The command reactivates that task.</span></span>

## <span data-ttu-id="661b6-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="661b6-117">PARAMETERS</span></span>

### <span data-ttu-id="661b6-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="661b6-118">-BatchContext</span></span>
<span data-ttu-id="661b6-119">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="661b6-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="661b6-120">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="661b6-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="661b6-121">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="661b6-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="661b6-122">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="661b6-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="661b6-123">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="661b6-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="661b6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="661b6-124">-DefaultProfile</span></span>
<span data-ttu-id="661b6-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="661b6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="661b6-126">-ID</span><span class="sxs-lookup"><span data-stu-id="661b6-126">-Id</span></span>
<span data-ttu-id="661b6-127">Gibt die ID der erneut zu aktivierenden Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="661b6-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="661b6-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="661b6-128">-JobId</span></span>
<span data-ttu-id="661b6-129">Gibt die ID des Auftrags an, der den Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="661b6-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="661b6-130">-Task</span><span class="sxs-lookup"><span data-stu-id="661b6-130">-Task</span></span>
<span data-ttu-id="661b6-131">Gibt die Aufgabe an, die dieses Cmdlet reaktiviert.</span><span class="sxs-lookup"><span data-stu-id="661b6-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="661b6-132">Verwenden Sie zum Abrufen **eines PSCloudTask-Objekts** das Get-AzBatchTask-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="661b6-132">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="661b6-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="661b6-133">-Confirm</span></span>
<span data-ttu-id="661b6-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="661b6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="661b6-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="661b6-135">-WhatIf</span></span>
<span data-ttu-id="661b6-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="661b6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="661b6-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="661b6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="661b6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="661b6-138">CommonParameters</span></span>
<span data-ttu-id="661b6-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="661b6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="661b6-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="661b6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="661b6-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="661b6-141">INPUTS</span></span>

### <span data-ttu-id="661b6-142">System.String</span><span class="sxs-lookup"><span data-stu-id="661b6-142">System.String</span></span>

### <span data-ttu-id="661b6-143">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="661b6-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="661b6-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="661b6-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="661b6-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="661b6-145">OUTPUTS</span></span>

### <span data-ttu-id="661b6-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="661b6-146">System.Void</span></span>

## <span data-ttu-id="661b6-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="661b6-147">NOTES</span></span>

## <span data-ttu-id="661b6-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="661b6-148">RELATED LINKS</span></span>

[<span data-ttu-id="661b6-149">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="661b6-149">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="661b6-150">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="661b6-150">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="661b6-151">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="661b6-151">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="661b6-152">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="661b6-152">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="661b6-153">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="661b6-153">Set-AzBatchTask</span></span>](./Set-AzBatchTask.md)

[<span data-ttu-id="661b6-154">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="661b6-154">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)


