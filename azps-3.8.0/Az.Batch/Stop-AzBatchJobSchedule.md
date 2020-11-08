---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: 9536de21d205a051f0a0a2ea6f4a83c759b94c8c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94007439"
---
# <span data-ttu-id="b1849-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b1849-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="b1849-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1849-102">SYNOPSIS</span></span>
<span data-ttu-id="b1849-103">Beendet einen stapelverarbeitungsauftrags Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="b1849-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="b1849-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1849-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1849-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1849-105">DESCRIPTION</span></span>
<span data-ttu-id="b1849-106">Das Cmdlet **Stop-AzBatchJobSchedule** beendet einen Azure-Batch Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="b1849-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="b1849-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1849-107">EXAMPLES</span></span>

### <span data-ttu-id="b1849-108">Beispiel 1: Beenden eines Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="b1849-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="b1849-109">Dieser Befehl beendet den Auftragszeitplan mit der ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="b1849-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="b1849-110">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="b1849-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="b1849-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1849-111">PARAMETERS</span></span>

### <span data-ttu-id="b1849-112">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="b1849-112">-BatchContext</span></span>
<span data-ttu-id="b1849-113">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1849-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b1849-114">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1849-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b1849-115">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b1849-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b1849-116">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1849-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b1849-117">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="b1849-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b1849-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1849-118">-DefaultProfile</span></span>
<span data-ttu-id="b1849-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1849-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1849-120">-ID</span><span class="sxs-lookup"><span data-stu-id="b1849-120">-Id</span></span>
<span data-ttu-id="b1849-121">Gibt die ID des Auftragszeitplans an, der vom Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="b1849-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="b1849-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1849-122">CommonParameters</span></span>
<span data-ttu-id="b1849-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1849-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1849-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1849-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1849-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1849-125">INPUTS</span></span>

### <span data-ttu-id="b1849-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b1849-126">System.String</span></span>

### <span data-ttu-id="b1849-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b1849-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b1849-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1849-128">OUTPUTS</span></span>

### <span data-ttu-id="b1849-129">System. void</span><span class="sxs-lookup"><span data-stu-id="b1849-129">System.Void</span></span>

## <span data-ttu-id="b1849-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1849-130">NOTES</span></span>

## <span data-ttu-id="b1849-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1849-131">RELATED LINKS</span></span>

[<span data-ttu-id="b1849-132">Deaktivieren-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b1849-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="b1849-133">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b1849-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="b1849-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b1849-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b1849-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b1849-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="b1849-136">Neu – AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b1849-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="b1849-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b1849-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="b1849-138">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="b1849-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


