---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
ms.openlocfilehash: 8b84028bc9da854b5aa749867a8759b71d9f7b63
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358362"
---
# <span data-ttu-id="2745f-101">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2745f-101">Stop-AzBatchTask</span></span>

## <span data-ttu-id="2745f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2745f-102">SYNOPSIS</span></span>
<span data-ttu-id="2745f-103">Beendet eine Batchaufgabe.</span><span class="sxs-lookup"><span data-stu-id="2745f-103">Stops a Batch task.</span></span>

## <span data-ttu-id="2745f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2745f-104">SYNTAX</span></span>

### <span data-ttu-id="2745f-105">ID</span><span class="sxs-lookup"><span data-stu-id="2745f-105">Id</span></span>
```
Stop-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2745f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2745f-106">InputObject</span></span>
```
Stop-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2745f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2745f-107">DESCRIPTION</span></span>
<span data-ttu-id="2745f-108">Das **Cmdlet "Stop-AzBatchTask"** beendet eine Azure-Batch-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="2745f-108">The **Stop-AzBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="2745f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2745f-109">EXAMPLES</span></span>

### <span data-ttu-id="2745f-110">Beispiel 1: Löschen einer Batchaufgabe nach ID</span><span class="sxs-lookup"><span data-stu-id="2745f-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="2745f-111">Mit diesem Befehl wird eine Aufgabe beendet, die die ID "Task23" unter dem Auftrag mit der ID Job-000001 hat.</span><span class="sxs-lookup"><span data-stu-id="2745f-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="2745f-112">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="2745f-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="2745f-113">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der Variablen $Context Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="2745f-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="2745f-114">Beispiel 2: Beenden einer Batchaufgabe mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="2745f-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="2745f-115">Mit diesem Befehl wird die Aufgabe "Batch" mit der ID Task26 in dem Auftrag mit der ID Job-000001 mithilfe des cmdlets Get-AzBatchTask batchen.</span><span class="sxs-lookup"><span data-stu-id="2745f-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="2745f-116">Der Befehl übergibt diese Aufgabe mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2745f-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2745f-117">Der Befehl beendet diese Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="2745f-117">The command stops that task.</span></span>

## <span data-ttu-id="2745f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2745f-118">PARAMETERS</span></span>

### <span data-ttu-id="2745f-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2745f-119">-BatchContext</span></span>
<span data-ttu-id="2745f-120">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2745f-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2745f-121">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="2745f-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2745f-122">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2745f-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2745f-123">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="2745f-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2745f-124">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2745f-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2745f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2745f-125">-DefaultProfile</span></span>
<span data-ttu-id="2745f-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2745f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2745f-127">-ID</span><span class="sxs-lookup"><span data-stu-id="2745f-127">-Id</span></span>
<span data-ttu-id="2745f-128">Gibt die ID der Aufgabe an, die dieses Cmdlet beendet.</span><span class="sxs-lookup"><span data-stu-id="2745f-128">Specifies the ID of the task that this cmdlet stops.</span></span>

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

### <span data-ttu-id="2745f-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="2745f-129">-JobId</span></span>
<span data-ttu-id="2745f-130">Gibt die ID des Auftrags an, der den Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="2745f-130">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="2745f-131">-Task</span><span class="sxs-lookup"><span data-stu-id="2745f-131">-Task</span></span>
<span data-ttu-id="2745f-132">Gibt die Aufgabe an, die dieses Cmdlet beendet.</span><span class="sxs-lookup"><span data-stu-id="2745f-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="2745f-133">Verwenden Sie zum Abrufen **eines PSCloudTask-Objekts** das Get-AzBatchTask-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2745f-133">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="2745f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2745f-134">CommonParameters</span></span>
<span data-ttu-id="2745f-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2745f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2745f-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2745f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2745f-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2745f-137">INPUTS</span></span>

### <span data-ttu-id="2745f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2745f-138">System.String</span></span>

### <span data-ttu-id="2745f-139">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="2745f-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="2745f-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2745f-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2745f-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2745f-141">OUTPUTS</span></span>

### <span data-ttu-id="2745f-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="2745f-142">System.Void</span></span>

## <span data-ttu-id="2745f-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2745f-143">NOTES</span></span>

## <span data-ttu-id="2745f-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2745f-144">RELATED LINKS</span></span>

[<span data-ttu-id="2745f-145">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2745f-145">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="2745f-146">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2745f-146">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="2745f-147">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2745f-147">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="2745f-148">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2745f-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
