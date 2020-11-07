---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: 8e7636d83b953997ac1f9269e45fbf3c2278612f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665109"
---
# <span data-ttu-id="2688e-101">Enable-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2688e-101">Enable-AzureBatchTask</span></span>

## <span data-ttu-id="2688e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2688e-102">SYNOPSIS</span></span>
<span data-ttu-id="2688e-103">Reaktiviert eine Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="2688e-103">Reactivates a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2688e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2688e-104">SYNTAX</span></span>

### <span data-ttu-id="2688e-105">ID</span><span class="sxs-lookup"><span data-stu-id="2688e-105">Id</span></span>
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2688e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2688e-106">InputObject</span></span>
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2688e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2688e-107">DESCRIPTION</span></span>
<span data-ttu-id="2688e-108">Mit dem Cmdlet **enable-AzureBatchTask** wird eine Aufgabe erneut aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2688e-108">The **Enable-AzureBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="2688e-109">Wenn ein Vorgang seine Wiederholungsanzahl erschöpft hat, ermöglicht dieses Cmdlet dennoch die Ausführung.</span><span class="sxs-lookup"><span data-stu-id="2688e-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="2688e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2688e-110">EXAMPLES</span></span>

### <span data-ttu-id="2688e-111">Beispiel 1: Reaktivieren einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="2688e-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="2688e-112">Mit diesem Befehl wird die Aufgabe task2 in Job Job7 erneut aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2688e-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="2688e-113">Beispiel 2: Reaktivieren einer Aufgabe mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="2688e-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="2688e-114">Dieser Befehl ruft die Batch Aufgabe mit der ID Task3 in dem Auftrag ab, der die ID-Job8 mit dem Get-AzureBatchTask-Cmdlet aufweist.</span><span class="sxs-lookup"><span data-stu-id="2688e-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="2688e-115">Der Befehl übergibt diesen Vorgang mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2688e-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2688e-116">Der Befehl aktiviert diese Aufgabe erneut.</span><span class="sxs-lookup"><span data-stu-id="2688e-116">The command reactivates that task.</span></span>

## <span data-ttu-id="2688e-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="2688e-117">PARAMETERS</span></span>

### <span data-ttu-id="2688e-118">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="2688e-118">-BatchContext</span></span>
<span data-ttu-id="2688e-119">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="2688e-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2688e-120">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2688e-120">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="2688e-121">-ID</span><span class="sxs-lookup"><span data-stu-id="2688e-121">-Id</span></span>
<span data-ttu-id="2688e-122">Gibt die ID der Aufgabe an, die erneut aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2688e-122">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="2688e-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="2688e-123">-JobId</span></span>
<span data-ttu-id="2688e-124">Gibt die ID des Auftrags an, der die Aufgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="2688e-124">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="2688e-125">– Aufgabe</span><span class="sxs-lookup"><span data-stu-id="2688e-125">-Task</span></span>
<span data-ttu-id="2688e-126">Gibt die Aufgabe an, die dieses Cmdlet reaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2688e-126">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="2688e-127">Verwenden Sie das Get-AzureBatchTask-Cmdlet, um ein **PSCloudTask** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2688e-127">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="2688e-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2688e-128">-Confirm</span></span>
<span data-ttu-id="2688e-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2688e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2688e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2688e-130">-WhatIf</span></span>
<span data-ttu-id="2688e-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2688e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2688e-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2688e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2688e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2688e-133">-DefaultProfile</span></span>
<span data-ttu-id="2688e-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2688e-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2688e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2688e-135">CommonParameters</span></span>
<span data-ttu-id="2688e-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2688e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2688e-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2688e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2688e-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2688e-138">INPUTS</span></span>

### <span data-ttu-id="2688e-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2688e-139">BatchAccountContext</span></span>
<span data-ttu-id="2688e-140">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2688e-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="2688e-141">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="2688e-141">PSCloudTask</span></span>
<span data-ttu-id="2688e-142">Der Parameter "Aufgabe" akzeptiert den Wert vom Typ "PSCloudTask" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2688e-142">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="2688e-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2688e-143">OUTPUTS</span></span>

## <span data-ttu-id="2688e-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="2688e-144">NOTES</span></span>

## <span data-ttu-id="2688e-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2688e-145">RELATED LINKS</span></span>

[<span data-ttu-id="2688e-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2688e-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="2688e-147">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2688e-147">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="2688e-148">Neu – AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2688e-148">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="2688e-149">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2688e-149">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="2688e-150">Satz-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2688e-150">Set-AzureBatchTask</span></span>](./Set-AzureBatchTask.md)

[<span data-ttu-id="2688e-151">Stopp-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2688e-151">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)


