---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 1eef03db73e6b1afcb2c9ca92f507e8b0f3ff0ae
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93662106"
---
# <span data-ttu-id="3a7ac-101">Enable-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3a7ac-101">Enable-AzBatchTask</span></span>

## <span data-ttu-id="3a7ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a7ac-102">SYNOPSIS</span></span>
<span data-ttu-id="3a7ac-103">Reaktiviert eine Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="3a7ac-103">Reactivates a task.</span></span>

## <span data-ttu-id="3a7ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a7ac-104">SYNTAX</span></span>

### <span data-ttu-id="3a7ac-105">ID</span><span class="sxs-lookup"><span data-stu-id="3a7ac-105">Id</span></span>
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a7ac-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3a7ac-106">InputObject</span></span>
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a7ac-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a7ac-107">DESCRIPTION</span></span>
<span data-ttu-id="3a7ac-108">Mit dem Cmdlet **enable-AzBatchTask** wird eine Aufgabe erneut aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3a7ac-108">The **Enable-AzBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="3a7ac-109">Wenn ein Vorgang seine Wiederholungsanzahl erschöpft hat, ermöglicht dieses Cmdlet dennoch die Ausführung.</span><span class="sxs-lookup"><span data-stu-id="3a7ac-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="3a7ac-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a7ac-110">EXAMPLES</span></span>

### <span data-ttu-id="3a7ac-111">Beispiel 1: Reaktivieren einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="3a7ac-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="3a7ac-112">Mit diesem Befehl wird die Aufgabe task2 in Job Job7 erneut aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3a7ac-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="3a7ac-113">Beispiel 2: Reaktivieren einer Aufgabe mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="3a7ac-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="3a7ac-114">Dieser Befehl ruft die Batch Aufgabe mit der ID Task3 in dem Auftrag ab, der die ID-Job8 mit dem Get-AzBatchTask-Cmdlet aufweist.</span><span class="sxs-lookup"><span data-stu-id="3a7ac-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="3a7ac-115">Der Befehl übergibt diesen Vorgang mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a7ac-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3a7ac-116">Der Befehl aktiviert diese Aufgabe erneut.</span><span class="sxs-lookup"><span data-stu-id="3a7ac-116">The command reactivates that task.</span></span>

## <span data-ttu-id="3a7ac-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a7ac-117">PARAMETERS</span></span>

### <span data-ttu-id="3a7ac-118">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="3a7ac-118">-BatchContext</span></span>
<span data-ttu-id="3a7ac-119">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a7ac-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3a7ac-120">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a7ac-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3a7ac-121">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3a7ac-121">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3a7ac-122">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a7ac-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3a7ac-123">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="3a7ac-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3a7ac-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a7ac-124">-DefaultProfile</span></span>
<span data-ttu-id="3a7ac-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3a7ac-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a7ac-126">-ID</span><span class="sxs-lookup"><span data-stu-id="3a7ac-126">-Id</span></span>
<span data-ttu-id="3a7ac-127">Gibt die ID der Aufgabe an, die erneut aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3a7ac-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="3a7ac-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="3a7ac-128">-JobId</span></span>
<span data-ttu-id="3a7ac-129">Gibt die ID des Auftrags an, der die Aufgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="3a7ac-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="3a7ac-130">– Aufgabe</span><span class="sxs-lookup"><span data-stu-id="3a7ac-130">-Task</span></span>
<span data-ttu-id="3a7ac-131">Gibt die Aufgabe an, die dieses Cmdlet reaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3a7ac-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="3a7ac-132">Verwenden Sie das Get-AzBatchTask-Cmdlet, um ein **PSCloudTask** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3a7ac-132">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="3a7ac-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3a7ac-133">-Confirm</span></span>
<span data-ttu-id="3a7ac-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3a7ac-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a7ac-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a7ac-135">-WhatIf</span></span>
<span data-ttu-id="3a7ac-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a7ac-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a7ac-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a7ac-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a7ac-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a7ac-138">CommonParameters</span></span>
<span data-ttu-id="3a7ac-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a7ac-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a7ac-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a7ac-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a7ac-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a7ac-141">INPUTS</span></span>

### <span data-ttu-id="3a7ac-142">System. String</span><span class="sxs-lookup"><span data-stu-id="3a7ac-142">System.String</span></span>

### <span data-ttu-id="3a7ac-143">Microsoft.Azure.Commands.Batch. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="3a7ac-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="3a7ac-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3a7ac-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3a7ac-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a7ac-145">OUTPUTS</span></span>

### <span data-ttu-id="3a7ac-146">System. void</span><span class="sxs-lookup"><span data-stu-id="3a7ac-146">System.Void</span></span>

## <span data-ttu-id="3a7ac-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a7ac-147">NOTES</span></span>

## <span data-ttu-id="3a7ac-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a7ac-148">RELATED LINKS</span></span>

[<span data-ttu-id="3a7ac-149">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3a7ac-149">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="3a7ac-150">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3a7ac-150">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="3a7ac-151">Neu – AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3a7ac-151">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="3a7ac-152">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3a7ac-152">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="3a7ac-153">Satz-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3a7ac-153">Set-AzBatchTask</span></span>](./Set-AzBatchTask.md)

[<span data-ttu-id="3a7ac-154">Stopp-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3a7ac-154">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)


