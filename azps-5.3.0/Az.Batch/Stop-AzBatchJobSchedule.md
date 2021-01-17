---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: b236f163a6c5c849fcbfcea0a19dac955e15c798
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471084"
---
# <span data-ttu-id="6b478-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6b478-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="6b478-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b478-102">SYNOPSIS</span></span>
<span data-ttu-id="6b478-103">Beendet einen Stapelauftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="6b478-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="6b478-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b478-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b478-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b478-105">DESCRIPTION</span></span>
<span data-ttu-id="6b478-106">Das **Cmdlet "Stop-AzBatchJobSchedule"** beendet einen Azure Batch-Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="6b478-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="6b478-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6b478-107">EXAMPLES</span></span>

### <span data-ttu-id="6b478-108">Beispiel 1: Beenden eines Stellenplans</span><span class="sxs-lookup"><span data-stu-id="6b478-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="6b478-109">Dieser Befehl beendet den Auftragszeitplan mit der ID "JobSchedule17".</span><span class="sxs-lookup"><span data-stu-id="6b478-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="6b478-110">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der Variablen $Context Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="6b478-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="6b478-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b478-111">PARAMETERS</span></span>

### <span data-ttu-id="6b478-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6b478-112">-BatchContext</span></span>
<span data-ttu-id="6b478-113">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6b478-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6b478-114">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b478-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6b478-115">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6b478-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6b478-116">Bei verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b478-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6b478-117">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b478-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6b478-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b478-118">-DefaultProfile</span></span>
<span data-ttu-id="6b478-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b478-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b478-120">-ID</span><span class="sxs-lookup"><span data-stu-id="6b478-120">-Id</span></span>
<span data-ttu-id="6b478-121">Gibt die ID des Auftragsplans an, der mit diesem Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="6b478-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="6b478-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b478-122">CommonParameters</span></span>
<span data-ttu-id="6b478-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b478-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b478-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b478-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b478-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6b478-125">INPUTS</span></span>

### <span data-ttu-id="6b478-126">System.String</span><span class="sxs-lookup"><span data-stu-id="6b478-126">System.String</span></span>

### <span data-ttu-id="6b478-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6b478-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6b478-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6b478-128">OUTPUTS</span></span>

### <span data-ttu-id="6b478-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="6b478-129">System.Void</span></span>

## <span data-ttu-id="6b478-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6b478-130">NOTES</span></span>

## <span data-ttu-id="6b478-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6b478-131">RELATED LINKS</span></span>

[<span data-ttu-id="6b478-132">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6b478-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="6b478-133">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6b478-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="6b478-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6b478-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6b478-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6b478-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="6b478-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6b478-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="6b478-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6b478-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="6b478-138">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6b478-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
