---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
ms.openlocfilehash: ffaac0bdd4a144cc3979da052c0c40cb824862f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171449"
---
# <span data-ttu-id="9ee2a-101">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="9ee2a-101">Stop-AzBatchJob</span></span>

## <span data-ttu-id="9ee2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ee2a-102">SYNOPSIS</span></span>
<span data-ttu-id="9ee2a-103">Beendet einen Stapelauftrag.</span><span class="sxs-lookup"><span data-stu-id="9ee2a-103">Stops a Batch job.</span></span>

## <span data-ttu-id="9ee2a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ee2a-104">SYNTAX</span></span>

```
Stop-AzBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ee2a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ee2a-105">DESCRIPTION</span></span>
<span data-ttu-id="9ee2a-106">Das **Cmdlet "Stop-AzBatchJob"** beendet einen Azure Batch-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="9ee2a-106">The **Stop-AzBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="9ee2a-107">Mit diesem Befehl wird der Auftrag als abgeschlossen markiert.</span><span class="sxs-lookup"><span data-stu-id="9ee2a-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="9ee2a-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9ee2a-108">EXAMPLES</span></span>

### <span data-ttu-id="9ee2a-109">Beispiel 1: Beenden eines Stapelauftrags</span><span class="sxs-lookup"><span data-stu-id="9ee2a-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="9ee2a-110">Dieser Befehl beendet den Auftrag mit der ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="9ee2a-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="9ee2a-111">Der Befehl gibt einen Grund an, warum Sie den Auftrag beendet haben.</span><span class="sxs-lookup"><span data-stu-id="9ee2a-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="9ee2a-112">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der Variablen einen Kontext $Context zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="9ee2a-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="9ee2a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ee2a-113">PARAMETERS</span></span>

### <span data-ttu-id="9ee2a-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9ee2a-114">-BatchContext</span></span>
<span data-ttu-id="9ee2a-115">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9ee2a-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9ee2a-116">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ee2a-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9ee2a-117">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9ee2a-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9ee2a-118">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ee2a-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9ee2a-119">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9ee2a-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9ee2a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ee2a-120">-DefaultProfile</span></span>
<span data-ttu-id="9ee2a-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ee2a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ee2a-122">-ID</span><span class="sxs-lookup"><span data-stu-id="9ee2a-122">-Id</span></span>
<span data-ttu-id="9ee2a-123">Gibt die ID des Auftrags an, der von diesem Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="9ee2a-123">Specifies the ID of the job that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee2a-124">-Terminate Umson</span><span class="sxs-lookup"><span data-stu-id="9ee2a-124">-TerminateReason</span></span>
<span data-ttu-id="9ee2a-125">Gibt den Grund an, warum Sie den Auftrag beendet haben.</span><span class="sxs-lookup"><span data-stu-id="9ee2a-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="9ee2a-126">Dieses Cmdlet speichert diesen Text als **"Terminate Voll"-Eigenschaft** des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="9ee2a-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee2a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ee2a-127">CommonParameters</span></span>
<span data-ttu-id="9ee2a-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ee2a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ee2a-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ee2a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ee2a-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9ee2a-130">INPUTS</span></span>

### <span data-ttu-id="9ee2a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="9ee2a-131">System.String</span></span>

### <span data-ttu-id="9ee2a-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9ee2a-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9ee2a-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9ee2a-133">OUTPUTS</span></span>

### <span data-ttu-id="9ee2a-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="9ee2a-134">System.Void</span></span>

## <span data-ttu-id="9ee2a-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9ee2a-135">NOTES</span></span>

## <span data-ttu-id="9ee2a-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9ee2a-136">RELATED LINKS</span></span>

[<span data-ttu-id="9ee2a-137">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="9ee2a-137">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="9ee2a-138">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="9ee2a-138">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="9ee2a-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="9ee2a-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9ee2a-140">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="9ee2a-140">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="9ee2a-141">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="9ee2a-141">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="9ee2a-142">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="9ee2a-142">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="9ee2a-143">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="9ee2a-143">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
