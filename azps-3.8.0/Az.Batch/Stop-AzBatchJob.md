---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
ms.openlocfilehash: fa9945e80bfc3b94cf29e0751bc1ceedb36d12bd
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94007443"
---
# <span data-ttu-id="19323-101">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="19323-101">Stop-AzBatchJob</span></span>

## <span data-ttu-id="19323-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19323-102">SYNOPSIS</span></span>
<span data-ttu-id="19323-103">Beendet eine Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="19323-103">Stops a Batch job.</span></span>

## <span data-ttu-id="19323-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19323-104">SYNTAX</span></span>

```
Stop-AzBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19323-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19323-105">DESCRIPTION</span></span>
<span data-ttu-id="19323-106">Das Cmdlet **Stop-AzBatchJob** beendet eine Azure-Batch Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="19323-106">The **Stop-AzBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="19323-107">Mit diesem Befehl wird der Auftrag als erledigt markiert.</span><span class="sxs-lookup"><span data-stu-id="19323-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="19323-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19323-108">EXAMPLES</span></span>

### <span data-ttu-id="19323-109">Beispiel 1: Beenden einer Stapelverarbeitung</span><span class="sxs-lookup"><span data-stu-id="19323-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="19323-110">Dieser Befehl beendet den Auftrag mit der ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="19323-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="19323-111">Der Befehl gibt einen Grund an, den Sie zum Beenden des Auftrags ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="19323-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="19323-112">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="19323-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="19323-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="19323-113">PARAMETERS</span></span>

### <span data-ttu-id="19323-114">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="19323-114">-BatchContext</span></span>
<span data-ttu-id="19323-115">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="19323-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="19323-116">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="19323-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="19323-117">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="19323-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="19323-118">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="19323-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="19323-119">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="19323-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="19323-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19323-120">-DefaultProfile</span></span>
<span data-ttu-id="19323-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="19323-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19323-122">-ID</span><span class="sxs-lookup"><span data-stu-id="19323-122">-Id</span></span>
<span data-ttu-id="19323-123">Gibt die ID des Auftrags an, der vom Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="19323-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="19323-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="19323-124">-TerminateReason</span></span>
<span data-ttu-id="19323-125">Gibt den Grund an, zu dem Sie den Auftrag beendet haben.</span><span class="sxs-lookup"><span data-stu-id="19323-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="19323-126">Dieses Cmdlet speichert diesen Text als **TerminateReason** -Eigenschaft des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="19323-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

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

### <span data-ttu-id="19323-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19323-127">CommonParameters</span></span>
<span data-ttu-id="19323-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19323-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19323-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19323-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19323-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19323-130">INPUTS</span></span>

### <span data-ttu-id="19323-131">System. String</span><span class="sxs-lookup"><span data-stu-id="19323-131">System.String</span></span>

### <span data-ttu-id="19323-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="19323-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="19323-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19323-133">OUTPUTS</span></span>

### <span data-ttu-id="19323-134">System. void</span><span class="sxs-lookup"><span data-stu-id="19323-134">System.Void</span></span>

## <span data-ttu-id="19323-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="19323-135">NOTES</span></span>

## <span data-ttu-id="19323-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19323-136">RELATED LINKS</span></span>

[<span data-ttu-id="19323-137">Deaktivieren-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="19323-137">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="19323-138">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="19323-138">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="19323-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="19323-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="19323-140">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="19323-140">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="19323-141">Neu – AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="19323-141">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="19323-142">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="19323-142">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="19323-143">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="19323-143">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


