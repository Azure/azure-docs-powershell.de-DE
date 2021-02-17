---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
ms.openlocfilehash: a25c31c0b73a42e0d64b567b6bc2529bf4ebf258
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171618"
---
# <span data-ttu-id="8e7e6-101">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="8e7e6-101">Disable-AzBatchJob</span></span>

## <span data-ttu-id="8e7e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e7e6-102">SYNOPSIS</span></span>
<span data-ttu-id="8e7e6-103">Deaktiviert einen Stapelauftrag.</span><span class="sxs-lookup"><span data-stu-id="8e7e6-103">Disables a Batch job.</span></span>

## <span data-ttu-id="8e7e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e7e6-104">SYNTAX</span></span>

```
Disable-AzBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e7e6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e7e6-105">DESCRIPTION</span></span>
<span data-ttu-id="8e7e6-106">Das **Cmdlet "Disable-AzBatchJob"** deaktiviert einen Azure Batch-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="8e7e6-106">The **Disable-AzBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="8e7e6-107">Nachdem Sie einen Auftrag aktiviert haben, können neue Aufgaben ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8e7e6-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="8e7e6-108">Mit deaktivierten Aufträgen werden keine neuen Aufgaben ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e7e6-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="8e7e6-109">Sie können einen deaktivierten Auftrag später aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8e7e6-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="8e7e6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e7e6-110">EXAMPLES</span></span>

### <span data-ttu-id="8e7e6-111">Beispiel 1: Deaktivieren eines Stapelauftrags</span><span class="sxs-lookup"><span data-stu-id="8e7e6-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="8e7e6-112">Mit diesem Befehl wird der Auftrag mit der ID Job-000001 deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8e7e6-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="8e7e6-113">Der Befehl beendet aktive Aufgaben für den Auftrag.</span><span class="sxs-lookup"><span data-stu-id="8e7e6-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="8e7e6-114">Verwenden Sie **das Cmdlet "Get-AzBatchAccountKey",** um der Variablen "$Context" einen Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="8e7e6-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="8e7e6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e7e6-115">PARAMETERS</span></span>

### <span data-ttu-id="8e7e6-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8e7e6-116">-BatchContext</span></span>
<span data-ttu-id="8e7e6-117">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8e7e6-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8e7e6-118">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e7e6-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8e7e6-119">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8e7e6-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8e7e6-120">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e7e6-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8e7e6-121">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8e7e6-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8e7e6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e7e6-122">-DefaultProfile</span></span>
<span data-ttu-id="8e7e6-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e7e6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e7e6-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="8e7e6-124">-DisableJobOption</span></span>
<span data-ttu-id="8e7e6-125">Gibt an, was mit aktiven Aufgaben zu tun ist, die mit dem Auftrag verknüpft sind, den dieses Cmdlet deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8e7e6-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="8e7e6-126">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="8e7e6-126">Valid values are:</span></span>
- <span data-ttu-id="8e7e6-127">Requeue</span><span class="sxs-lookup"><span data-stu-id="8e7e6-127">Requeue</span></span>
- <span data-ttu-id="8e7e6-128">Beenden</span><span class="sxs-lookup"><span data-stu-id="8e7e6-128">Terminate</span></span>
- <span data-ttu-id="8e7e6-129">Warte</span><span class="sxs-lookup"><span data-stu-id="8e7e6-129">Wait</span></span>

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

### <span data-ttu-id="8e7e6-130">-ID</span><span class="sxs-lookup"><span data-stu-id="8e7e6-130">-Id</span></span>
<span data-ttu-id="8e7e6-131">Gibt die ID des Auftrags an, den dieses Cmdlet deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8e7e6-131">Specifies the ID of the job that this cmdlet disables.</span></span>

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

### <span data-ttu-id="8e7e6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e7e6-132">CommonParameters</span></span>
<span data-ttu-id="8e7e6-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e7e6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e7e6-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e7e6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e7e6-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e7e6-135">INPUTS</span></span>

### <span data-ttu-id="8e7e6-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8e7e6-136">System.String</span></span>

### <span data-ttu-id="8e7e6-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8e7e6-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8e7e6-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e7e6-138">OUTPUTS</span></span>

### <span data-ttu-id="8e7e6-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="8e7e6-139">System.Void</span></span>

## <span data-ttu-id="8e7e6-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8e7e6-140">NOTES</span></span>

## <span data-ttu-id="8e7e6-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8e7e6-141">RELATED LINKS</span></span>

[<span data-ttu-id="8e7e6-142">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="8e7e6-142">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="8e7e6-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8e7e6-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8e7e6-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="8e7e6-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="8e7e6-145">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="8e7e6-145">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="8e7e6-146">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="8e7e6-146">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="8e7e6-147">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="8e7e6-147">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="8e7e6-148">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8e7e6-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
