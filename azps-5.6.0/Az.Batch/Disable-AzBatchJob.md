---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/powershell/module/az.batch/disable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
ms.openlocfilehash: fabc983e8c7b70685477a640d408beb65251b253
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943168"
---
# <span data-ttu-id="4fc4e-101">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4fc4e-101">Disable-AzBatchJob</span></span>

## <span data-ttu-id="4fc4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fc4e-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc4e-103">Deaktiviert einen Batchauftrag.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-103">Disables a Batch job.</span></span>

## <span data-ttu-id="4fc4e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4fc4e-104">SYNTAX</span></span>

```
Disable-AzBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fc4e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4fc4e-105">DESCRIPTION</span></span>
<span data-ttu-id="4fc4e-106">Das **Cmdlet Disable-AzBatchJob** deaktiviert einen Azure Batch-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-106">The **Disable-AzBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="4fc4e-107">Nachdem Sie einen Auftrag aktiviert haben, können neue Aufgaben ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="4fc4e-108">Deaktivierte Aufträge führen keine neuen Aufgaben aus.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="4fc4e-109">Sie können einen deaktivierten Auftrag später aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="4fc4e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4fc4e-110">EXAMPLES</span></span>

### <span data-ttu-id="4fc4e-111">Beispiel 1: Deaktivieren eines Stapelauftrags</span><span class="sxs-lookup"><span data-stu-id="4fc4e-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="4fc4e-112">Mit diesem Befehl wird der Auftrag deaktiviert, der die ID Job-000001 hat.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="4fc4e-113">Mit dem Befehl werden aktive Aufgaben für den Auftrag beendet.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="4fc4e-114">Verwenden Sie **das Get-AzBatchAccountKey-Cmdlet,** um der Variablen "$Context" einen Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="4fc4e-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4fc4e-115">PARAMETERS</span></span>

### <span data-ttu-id="4fc4e-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4fc4e-116">-BatchContext</span></span>
<span data-ttu-id="4fc4e-117">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4fc4e-118">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4fc4e-119">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4fc4e-120">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4fc4e-121">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4fc4e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fc4e-122">-DefaultProfile</span></span>
<span data-ttu-id="4fc4e-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fc4e-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="4fc4e-124">-DisableJobOption</span></span>
<span data-ttu-id="4fc4e-125">Gibt an, was mit aktiven Aufgaben zu tun ist, die dem Auftrag zugeordnet sind, den dieses Cmdlet deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="4fc4e-126">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="4fc4e-126">Valid values are:</span></span>
- <span data-ttu-id="4fc4e-127">Requeue</span><span class="sxs-lookup"><span data-stu-id="4fc4e-127">Requeue</span></span>
- <span data-ttu-id="4fc4e-128">Beenden</span><span class="sxs-lookup"><span data-stu-id="4fc4e-128">Terminate</span></span>
- <span data-ttu-id="4fc4e-129">Warte</span><span class="sxs-lookup"><span data-stu-id="4fc4e-129">Wait</span></span>

```yaml
Type: Microsoft.Azure.Batch.Common.DisableJobOption
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc4e-130">-ID</span><span class="sxs-lookup"><span data-stu-id="4fc4e-130">-Id</span></span>
<span data-ttu-id="4fc4e-131">Gibt die ID des Auftrags an, den dieses Cmdlet deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-131">Specifies the ID of the job that this cmdlet disables.</span></span>

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

### <span data-ttu-id="4fc4e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc4e-132">CommonParameters</span></span>
<span data-ttu-id="4fc4e-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc4e-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4fc4e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc4e-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4fc4e-135">INPUTS</span></span>

### <span data-ttu-id="4fc4e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="4fc4e-136">System.String</span></span>

### <span data-ttu-id="4fc4e-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4fc4e-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4fc4e-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4fc4e-138">OUTPUTS</span></span>

### <span data-ttu-id="4fc4e-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="4fc4e-139">System.Void</span></span>

## <span data-ttu-id="4fc4e-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4fc4e-140">NOTES</span></span>

## <span data-ttu-id="4fc4e-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4fc4e-141">RELATED LINKS</span></span>

[<span data-ttu-id="4fc4e-142">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4fc4e-142">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="4fc4e-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4fc4e-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4fc4e-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4fc4e-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="4fc4e-145">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4fc4e-145">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="4fc4e-146">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4fc4e-146">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="4fc4e-147">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4fc4e-147">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="4fc4e-148">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="4fc4e-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
