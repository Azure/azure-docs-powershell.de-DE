---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: 85226072ca3e94a1e9cd10cd5a29e4fbee229c5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925187"
---
# <span data-ttu-id="9bd4b-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9bd4b-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="9bd4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bd4b-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd4b-103">Beendet einen Stapelverarbeitungszeitplan.</span><span class="sxs-lookup"><span data-stu-id="9bd4b-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="9bd4b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9bd4b-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bd4b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9bd4b-105">DESCRIPTION</span></span>
<span data-ttu-id="9bd4b-106">Das **Cmdlet Stop-AzBatchJobSchedule** beendet einen Azure Batch-Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="9bd4b-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="9bd4b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9bd4b-107">EXAMPLES</span></span>

### <span data-ttu-id="9bd4b-108">Beispiel 1: Beenden eines Auftragsplans</span><span class="sxs-lookup"><span data-stu-id="9bd4b-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="9bd4b-109">Mit diesem Befehl wird der Auftragszeitplan beendet, der die ID JobSchedule17 hat.</span><span class="sxs-lookup"><span data-stu-id="9bd4b-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="9bd4b-110">Verwenden Sie Get-AzBatchAccountKey-Cmdlet, um der Variablen $Context Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="9bd4b-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="9bd4b-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9bd4b-111">PARAMETERS</span></span>

### <span data-ttu-id="9bd4b-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9bd4b-112">-BatchContext</span></span>
<span data-ttu-id="9bd4b-113">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9bd4b-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9bd4b-114">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="9bd4b-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9bd4b-115">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9bd4b-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9bd4b-116">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="9bd4b-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9bd4b-117">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="9bd4b-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9bd4b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd4b-118">-DefaultProfile</span></span>
<span data-ttu-id="9bd4b-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9bd4b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bd4b-120">-ID</span><span class="sxs-lookup"><span data-stu-id="9bd4b-120">-Id</span></span>
<span data-ttu-id="9bd4b-121">Gibt die ID des Auftragszeitplans an, den dieses Cmdlet beendet.</span><span class="sxs-lookup"><span data-stu-id="9bd4b-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="9bd4b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd4b-122">CommonParameters</span></span>
<span data-ttu-id="9bd4b-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bd4b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd4b-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bd4b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd4b-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9bd4b-125">INPUTS</span></span>

### <span data-ttu-id="9bd4b-126">System.String</span><span class="sxs-lookup"><span data-stu-id="9bd4b-126">System.String</span></span>

### <span data-ttu-id="9bd4b-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9bd4b-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9bd4b-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9bd4b-128">OUTPUTS</span></span>

### <span data-ttu-id="9bd4b-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="9bd4b-129">System.Void</span></span>

## <span data-ttu-id="9bd4b-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9bd4b-130">NOTES</span></span>

## <span data-ttu-id="9bd4b-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9bd4b-131">RELATED LINKS</span></span>

[<span data-ttu-id="9bd4b-132">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9bd4b-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="9bd4b-133">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9bd4b-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="9bd4b-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="9bd4b-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9bd4b-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9bd4b-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="9bd4b-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9bd4b-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="9bd4b-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9bd4b-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="9bd4b-138">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="9bd4b-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
