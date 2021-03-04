---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
ms.openlocfilehash: 01e34258d7c3e94975032d0e77087b05acf3f264
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924267"
---
# <span data-ttu-id="20834-101">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="20834-101">Enable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="20834-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20834-102">SYNOPSIS</span></span>
<span data-ttu-id="20834-103">Aktiviert einen Batchauftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="20834-103">Enables a Batch job schedule.</span></span>

## <span data-ttu-id="20834-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20834-104">SYNTAX</span></span>

```
Enable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20834-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20834-105">DESCRIPTION</span></span>
<span data-ttu-id="20834-106">Das **Cmdlet Enable-AzBatchJobSchedule** ermöglicht einen Azure Batch-Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="20834-106">The **Enable-AzBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="20834-107">Nachdem Sie einen Stellenplan aktiviert haben, können Aufträge entsprechend diesem Zeitplan erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="20834-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="20834-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="20834-108">EXAMPLES</span></span>

### <span data-ttu-id="20834-109">Beispiel 1: Aktivieren eines Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="20834-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="20834-110">Dieser Befehl aktiviert den Auftragszeitplan mit der ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="20834-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="20834-111">Verwenden Sie **das Get-AzBatchAccountKey-Cmdlet,** um der Variablen "$Context" einen Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="20834-111">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="20834-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="20834-112">PARAMETERS</span></span>

### <span data-ttu-id="20834-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="20834-113">-BatchContext</span></span>
<span data-ttu-id="20834-114">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="20834-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="20834-115">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="20834-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="20834-116">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="20834-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="20834-117">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="20834-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="20834-118">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="20834-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="20834-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20834-119">-DefaultProfile</span></span>
<span data-ttu-id="20834-120">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="20834-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20834-121">-ID</span><span class="sxs-lookup"><span data-stu-id="20834-121">-Id</span></span>
<span data-ttu-id="20834-122">Gibt die ID des Auftragszeitplans an, den dieses Cmdlet aktiviert.</span><span class="sxs-lookup"><span data-stu-id="20834-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="20834-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20834-123">CommonParameters</span></span>
<span data-ttu-id="20834-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20834-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20834-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20834-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20834-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="20834-126">INPUTS</span></span>

### <span data-ttu-id="20834-127">System.String</span><span class="sxs-lookup"><span data-stu-id="20834-127">System.String</span></span>

### <span data-ttu-id="20834-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="20834-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="20834-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="20834-129">OUTPUTS</span></span>

### <span data-ttu-id="20834-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="20834-130">System.Void</span></span>

## <span data-ttu-id="20834-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="20834-131">NOTES</span></span>

## <span data-ttu-id="20834-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="20834-132">RELATED LINKS</span></span>

[<span data-ttu-id="20834-133">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="20834-133">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="20834-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="20834-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="20834-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="20834-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="20834-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="20834-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="20834-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="20834-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="20834-138">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="20834-138">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="20834-139">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="20834-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
