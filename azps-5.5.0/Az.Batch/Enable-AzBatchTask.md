---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 9979a0fa16b8cfbe59eb8412a76cbbebcb2fca4a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166780"
---
# <span data-ttu-id="2d049-101">Enable-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2d049-101">Enable-AzBatchTask</span></span>

## <span data-ttu-id="2d049-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d049-102">SYNOPSIS</span></span>
<span data-ttu-id="2d049-103">Reaktiviert einen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="2d049-103">Reactivates a task.</span></span>

## <span data-ttu-id="2d049-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d049-104">SYNTAX</span></span>

### <span data-ttu-id="2d049-105">ID</span><span class="sxs-lookup"><span data-stu-id="2d049-105">Id</span></span>
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d049-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2d049-106">InputObject</span></span>
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d049-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d049-107">DESCRIPTION</span></span>
<span data-ttu-id="2d049-108">Das **Cmdlet "Enable-AzBatchTask"** aktiviert eine Aufgabe erneut.</span><span class="sxs-lookup"><span data-stu-id="2d049-108">The **Enable-AzBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="2d049-109">Wenn die Anzahl der Wiederholungen für eine Aufgabe aufgebraucht ist, kann sie mit diesem Cmdlet trotzdem ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2d049-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="2d049-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2d049-110">EXAMPLES</span></span>

### <span data-ttu-id="2d049-111">Beispiel 1: Reaktivieren eines Vorgangs</span><span class="sxs-lookup"><span data-stu-id="2d049-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="2d049-112">Mit diesem Befehl wird der Vorgang "Aufgabe2" in Auftrag7 reaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2d049-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="2d049-113">Beispiel 2: Reaktivieren einer Aufgabe mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="2d049-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="2d049-114">Mit diesem Befehl wird mithilfe des Cmdlets "Stapel" die Aufgabe "Batch" mit der ID "Aufgabe3" in dem Auftrag mit der ID "Auftrag8" Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="2d049-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="2d049-115">Der Befehl übergibt diese Aufgabe mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d049-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2d049-116">Der Befehl reaktiviert diese Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="2d049-116">The command reactivates that task.</span></span>

## <span data-ttu-id="2d049-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d049-117">PARAMETERS</span></span>

### <span data-ttu-id="2d049-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2d049-118">-BatchContext</span></span>
<span data-ttu-id="2d049-119">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2d049-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2d049-120">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d049-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2d049-121">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2d049-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2d049-122">Bei verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d049-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2d049-123">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2d049-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2d049-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d049-124">-DefaultProfile</span></span>
<span data-ttu-id="2d049-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d049-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d049-126">-ID</span><span class="sxs-lookup"><span data-stu-id="2d049-126">-Id</span></span>
<span data-ttu-id="2d049-127">Gibt die ID der erneut zu aktivierenden Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="2d049-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="2d049-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="2d049-128">-JobId</span></span>
<span data-ttu-id="2d049-129">Gibt die ID des Auftrags an, der den Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="2d049-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="2d049-130">-Task</span><span class="sxs-lookup"><span data-stu-id="2d049-130">-Task</span></span>
<span data-ttu-id="2d049-131">Gibt die Aufgabe an, die dieses Cmdlet reaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2d049-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="2d049-132">Verwenden Sie zum Abrufen **eines PSCloudTask-Objekts** das Get-AzBatchTask-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d049-132">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="2d049-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d049-133">-Confirm</span></span>
<span data-ttu-id="2d049-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d049-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d049-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2d049-135">-WhatIf</span></span>
<span data-ttu-id="2d049-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d049-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d049-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d049-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d049-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d049-138">CommonParameters</span></span>
<span data-ttu-id="2d049-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d049-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d049-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d049-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d049-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2d049-141">INPUTS</span></span>

### <span data-ttu-id="2d049-142">System.String</span><span class="sxs-lookup"><span data-stu-id="2d049-142">System.String</span></span>

### <span data-ttu-id="2d049-143">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="2d049-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="2d049-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2d049-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2d049-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2d049-145">OUTPUTS</span></span>

### <span data-ttu-id="2d049-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="2d049-146">System.Void</span></span>

## <span data-ttu-id="2d049-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2d049-147">NOTES</span></span>

## <span data-ttu-id="2d049-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2d049-148">RELATED LINKS</span></span>

[<span data-ttu-id="2d049-149">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="2d049-149">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="2d049-150">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2d049-150">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="2d049-151">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2d049-151">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="2d049-152">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2d049-152">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="2d049-153">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2d049-153">Set-AzBatchTask</span></span>](./Set-AzBatchTask.md)

[<span data-ttu-id="2d049-154">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2d049-154">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)


