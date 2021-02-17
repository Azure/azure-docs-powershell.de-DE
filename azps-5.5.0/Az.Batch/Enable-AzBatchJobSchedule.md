---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
ms.openlocfilehash: 03decd5b1d32defb25692220c63ffe768445697e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171582"
---
# <span data-ttu-id="7933d-101">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7933d-101">Enable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="7933d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7933d-102">SYNOPSIS</span></span>
<span data-ttu-id="7933d-103">Aktiviert einen Stapelauftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="7933d-103">Enables a Batch job schedule.</span></span>

## <span data-ttu-id="7933d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7933d-104">SYNTAX</span></span>

```
Enable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7933d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7933d-105">DESCRIPTION</span></span>
<span data-ttu-id="7933d-106">Das **Cmdlet "Enable-AzBatchJobSchedule"** aktiviert einen Azure Batch-Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="7933d-106">The **Enable-AzBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="7933d-107">Nachdem Sie einen Stellenplan aktiviert haben, können Aufträge entsprechend diesem Zeitplan erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7933d-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="7933d-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7933d-108">EXAMPLES</span></span>

### <span data-ttu-id="7933d-109">Beispiel 1: Aktivieren eines Stellenplans</span><span class="sxs-lookup"><span data-stu-id="7933d-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="7933d-110">Dieser Befehl aktiviert den Auftragszeitplan mit der ID "JobSchedule17".</span><span class="sxs-lookup"><span data-stu-id="7933d-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="7933d-111">Verwenden Sie **das Cmdlet "Get-AzBatchAccountKey",** um der Variablen "$Context" einen Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="7933d-111">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="7933d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7933d-112">PARAMETERS</span></span>

### <span data-ttu-id="7933d-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7933d-113">-BatchContext</span></span>
<span data-ttu-id="7933d-114">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7933d-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7933d-115">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="7933d-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7933d-116">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7933d-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7933d-117">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="7933d-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7933d-118">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7933d-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7933d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7933d-119">-DefaultProfile</span></span>
<span data-ttu-id="7933d-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7933d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7933d-121">-ID</span><span class="sxs-lookup"><span data-stu-id="7933d-121">-Id</span></span>
<span data-ttu-id="7933d-122">Gibt die ID des Auftragsplans an, den dieses Cmdlet aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7933d-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="7933d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7933d-123">CommonParameters</span></span>
<span data-ttu-id="7933d-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7933d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7933d-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7933d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7933d-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7933d-126">INPUTS</span></span>

### <span data-ttu-id="7933d-127">System.String</span><span class="sxs-lookup"><span data-stu-id="7933d-127">System.String</span></span>

### <span data-ttu-id="7933d-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7933d-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7933d-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7933d-129">OUTPUTS</span></span>

### <span data-ttu-id="7933d-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="7933d-130">System.Void</span></span>

## <span data-ttu-id="7933d-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7933d-131">NOTES</span></span>

## <span data-ttu-id="7933d-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7933d-132">RELATED LINKS</span></span>

[<span data-ttu-id="7933d-133">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7933d-133">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="7933d-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="7933d-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="7933d-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7933d-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="7933d-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7933d-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="7933d-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7933d-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="7933d-138">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7933d-138">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="7933d-139">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7933d-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
