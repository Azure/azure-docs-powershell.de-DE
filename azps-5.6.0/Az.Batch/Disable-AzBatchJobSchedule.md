---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: 54b9f9b60c1d424e6fd62ede85e517b40df1d062
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949624"
---
# <span data-ttu-id="b2d05-101">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b2d05-101">Disable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="b2d05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2d05-102">SYNOPSIS</span></span>
<span data-ttu-id="b2d05-103">Deaktiviert einen Batchauftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="b2d05-103">Disables a Batch job schedule.</span></span>

## <span data-ttu-id="b2d05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2d05-104">SYNTAX</span></span>

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2d05-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2d05-105">DESCRIPTION</span></span>
<span data-ttu-id="b2d05-106">Das **Cmdlet Disable-AzBatchJobSchedule** deaktiviert einen Azure Batch-Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="b2d05-106">The **Disable-AzBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="b2d05-107">Wenn Sie einen Zeitplan deaktivieren, werden Aufträge nicht gemäß diesem Zeitplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="b2d05-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="b2d05-108">Sie können einen deaktivierten Zeitplan später aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b2d05-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="b2d05-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b2d05-109">EXAMPLES</span></span>

### <span data-ttu-id="b2d05-110">Beispiel 1: Deaktivieren eines Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="b2d05-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="b2d05-111">Mit diesem Befehl wird der Auftragszeitplan deaktiviert, der die ID JobSchedule17 hat.</span><span class="sxs-lookup"><span data-stu-id="b2d05-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="b2d05-112">Verwenden Sie **das Get-AzBatchAccountKey-Cmdlet,** um der Variablen "$Context" einen Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="b2d05-112">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="b2d05-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b2d05-113">PARAMETERS</span></span>

### <span data-ttu-id="b2d05-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b2d05-114">-BatchContext</span></span>
<span data-ttu-id="b2d05-115">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2d05-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b2d05-116">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="b2d05-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b2d05-117">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b2d05-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b2d05-118">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="b2d05-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b2d05-119">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="b2d05-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b2d05-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2d05-120">-DefaultProfile</span></span>
<span data-ttu-id="b2d05-121">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2d05-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2d05-122">-ID</span><span class="sxs-lookup"><span data-stu-id="b2d05-122">-Id</span></span>
<span data-ttu-id="b2d05-123">Gibt die ID des Auftragszeitplans an, den dieses Cmdlet deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b2d05-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="b2d05-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2d05-124">CommonParameters</span></span>
<span data-ttu-id="b2d05-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2d05-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2d05-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2d05-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2d05-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b2d05-127">INPUTS</span></span>

### <span data-ttu-id="b2d05-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b2d05-128">System.String</span></span>

### <span data-ttu-id="b2d05-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b2d05-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b2d05-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b2d05-130">OUTPUTS</span></span>

### <span data-ttu-id="b2d05-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="b2d05-131">System.Void</span></span>

## <span data-ttu-id="b2d05-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b2d05-132">NOTES</span></span>

## <span data-ttu-id="b2d05-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b2d05-133">RELATED LINKS</span></span>

[<span data-ttu-id="b2d05-134">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b2d05-134">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="b2d05-135">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b2d05-135">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b2d05-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b2d05-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="b2d05-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b2d05-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="b2d05-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b2d05-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="b2d05-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b2d05-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="b2d05-140">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="b2d05-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
