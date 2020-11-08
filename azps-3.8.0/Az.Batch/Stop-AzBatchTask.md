---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
ms.openlocfilehash: 7d1b3b05f3432a5fc512c7dff03eb51c4223701d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94007436"
---
# <span data-ttu-id="92593-101">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="92593-101">Stop-AzBatchTask</span></span>

## <span data-ttu-id="92593-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="92593-102">SYNOPSIS</span></span>
<span data-ttu-id="92593-103">Beendet eine Batch Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="92593-103">Stops a Batch task.</span></span>

## <span data-ttu-id="92593-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="92593-104">SYNTAX</span></span>

### <span data-ttu-id="92593-105">ID</span><span class="sxs-lookup"><span data-stu-id="92593-105">Id</span></span>
```
Stop-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92593-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="92593-106">InputObject</span></span>
```
Stop-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92593-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92593-107">DESCRIPTION</span></span>
<span data-ttu-id="92593-108">Das Cmdlet **Stop-AzBatchTask** beendet eine Azure-Batch Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="92593-108">The **Stop-AzBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="92593-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92593-109">EXAMPLES</span></span>

### <span data-ttu-id="92593-110">Beispiel 1: Löschen einer stapelverarbeitungsaufgabe nach ID</span><span class="sxs-lookup"><span data-stu-id="92593-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="92593-111">Dieser Befehl beendet eine Aufgabe mit der ID Task23 unter dem Auftrag, der die ID Job-000001 hat.</span><span class="sxs-lookup"><span data-stu-id="92593-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="92593-112">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="92593-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="92593-113">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="92593-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="92593-114">Beispiel 2: Beenden einer Batch Aufgabe mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="92593-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="92593-115">Dieser Befehl ruft die Batch Aufgabe mit der ID Task26 in dem Auftrag ab, der die ID Job-000001 mit dem Get-AzBatchTask-Cmdlet aufweist.</span><span class="sxs-lookup"><span data-stu-id="92593-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="92593-116">Der Befehl übergibt diesen Vorgang mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92593-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="92593-117">Der Befehl beendet die Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="92593-117">The command stops that task.</span></span>

## <span data-ttu-id="92593-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="92593-118">PARAMETERS</span></span>

### <span data-ttu-id="92593-119">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="92593-119">-BatchContext</span></span>
<span data-ttu-id="92593-120">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="92593-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="92593-121">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="92593-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="92593-122">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="92593-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="92593-123">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="92593-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="92593-124">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="92593-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="92593-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92593-125">-DefaultProfile</span></span>
<span data-ttu-id="92593-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="92593-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92593-127">-ID</span><span class="sxs-lookup"><span data-stu-id="92593-127">-Id</span></span>
<span data-ttu-id="92593-128">Gibt die ID der Aufgabe an, die mit diesem Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="92593-128">Specifies the ID of the task that this cmdlet stops.</span></span>

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

### <span data-ttu-id="92593-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="92593-129">-JobId</span></span>
<span data-ttu-id="92593-130">Gibt die ID des Auftrags an, der die Aufgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="92593-130">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="92593-131">– Aufgabe</span><span class="sxs-lookup"><span data-stu-id="92593-131">-Task</span></span>
<span data-ttu-id="92593-132">Gibt die Aufgabe an, die mit diesem Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="92593-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="92593-133">Verwenden Sie das Get-AzBatchTask-Cmdlet, um ein **PSCloudTask** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="92593-133">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="92593-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92593-134">CommonParameters</span></span>
<span data-ttu-id="92593-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92593-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92593-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92593-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92593-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="92593-137">INPUTS</span></span>

### <span data-ttu-id="92593-138">System. String</span><span class="sxs-lookup"><span data-stu-id="92593-138">System.String</span></span>

### <span data-ttu-id="92593-139">Microsoft.Azure.Commands.Batch. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="92593-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="92593-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="92593-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="92593-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="92593-141">OUTPUTS</span></span>

### <span data-ttu-id="92593-142">System. void</span><span class="sxs-lookup"><span data-stu-id="92593-142">System.Void</span></span>

## <span data-ttu-id="92593-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="92593-143">NOTES</span></span>

## <span data-ttu-id="92593-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="92593-144">RELATED LINKS</span></span>

[<span data-ttu-id="92593-145">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="92593-145">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="92593-146">Neu – AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="92593-146">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="92593-147">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="92593-147">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="92593-148">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="92593-148">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


