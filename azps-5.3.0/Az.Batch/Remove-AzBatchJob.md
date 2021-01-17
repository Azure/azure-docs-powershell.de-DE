---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
ms.openlocfilehash: 1b55aae98db72f7c4d4fe262329889182a189c80
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471117"
---
# <span data-ttu-id="c98ff-101">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c98ff-101">Remove-AzBatchJob</span></span>

## <span data-ttu-id="c98ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c98ff-102">SYNOPSIS</span></span>
<span data-ttu-id="c98ff-103">Löscht einen Stapelauftrag.</span><span class="sxs-lookup"><span data-stu-id="c98ff-103">Deletes a Batch job.</span></span>

## <span data-ttu-id="c98ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c98ff-104">SYNTAX</span></span>

```
Remove-AzBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c98ff-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c98ff-105">DESCRIPTION</span></span>
<span data-ttu-id="c98ff-106">Das **Cmdlet "Remove-AzBatchJob"** löscht einen Azure Batch-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="c98ff-106">The **Remove-AzBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="c98ff-107">Dieses Cmdlet fordert Sie zur Bestätigung auf, bevor ein Auftrag entfernt wird, es sei denn, Sie geben den Parameter *"Erzwingen"* an.</span><span class="sxs-lookup"><span data-stu-id="c98ff-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="c98ff-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c98ff-108">EXAMPLES</span></span>

### <span data-ttu-id="c98ff-109">Beispiel 1: Löschen eines Stapelauftrags</span><span class="sxs-lookup"><span data-stu-id="c98ff-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="c98ff-110">Mit diesem Befehl wird der Auftrag mit der ID Job-000001 gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c98ff-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="c98ff-111">Der Befehl fordert Sie zur Bestätigung auf, bevor der Auftrag gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="c98ff-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="c98ff-112">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der Variablen $Context Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="c98ff-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="c98ff-113">Beispiel 2: Löschen eines Stapelauftrags ohne Bestätigung mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="c98ff-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="c98ff-114">Dieser Befehl ruft den Auftrag mit der ID Job-000002 mithilfe des cmdlets Get-AzBatchJob ab.</span><span class="sxs-lookup"><span data-stu-id="c98ff-114">This command gets the job that has the ID Job-000002 by using the Get-AzBatchJob cmdlet.</span></span>
<span data-ttu-id="c98ff-115">Der Befehl übergibt diesen Auftrag mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c98ff-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c98ff-116">Dieser Auftrag wird mit dem Befehl gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c98ff-116">The command deletes that job.</span></span>
<span data-ttu-id="c98ff-117">Da der Befehl den Parameter *"Force"* enthält, werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="c98ff-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c98ff-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c98ff-118">PARAMETERS</span></span>

### <span data-ttu-id="c98ff-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c98ff-119">-BatchContext</span></span>
<span data-ttu-id="c98ff-120">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c98ff-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c98ff-121">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="c98ff-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c98ff-122">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c98ff-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c98ff-123">Bei verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="c98ff-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c98ff-124">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c98ff-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c98ff-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c98ff-125">-DefaultProfile</span></span>
<span data-ttu-id="c98ff-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c98ff-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c98ff-127">-Force</span><span class="sxs-lookup"><span data-stu-id="c98ff-127">-Force</span></span>
<span data-ttu-id="c98ff-128">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="c98ff-128">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98ff-129">-ID</span><span class="sxs-lookup"><span data-stu-id="c98ff-129">-Id</span></span>
<span data-ttu-id="c98ff-130">Gibt die ID des Auftrags an, den dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="c98ff-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="c98ff-131">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="c98ff-131">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c98ff-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c98ff-132">-Confirm</span></span>
<span data-ttu-id="c98ff-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c98ff-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98ff-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c98ff-134">-WhatIf</span></span>
<span data-ttu-id="c98ff-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c98ff-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c98ff-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c98ff-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98ff-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c98ff-137">CommonParameters</span></span>
<span data-ttu-id="c98ff-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c98ff-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c98ff-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c98ff-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c98ff-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c98ff-140">INPUTS</span></span>

### <span data-ttu-id="c98ff-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c98ff-141">System.String</span></span>

### <span data-ttu-id="c98ff-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c98ff-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c98ff-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c98ff-143">OUTPUTS</span></span>

### <span data-ttu-id="c98ff-144">System.Void</span><span class="sxs-lookup"><span data-stu-id="c98ff-144">System.Void</span></span>

## <span data-ttu-id="c98ff-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c98ff-145">NOTES</span></span>

## <span data-ttu-id="c98ff-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c98ff-146">RELATED LINKS</span></span>

[<span data-ttu-id="c98ff-147">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c98ff-147">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="c98ff-148">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c98ff-148">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="c98ff-149">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c98ff-149">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="c98ff-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c98ff-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c98ff-151">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c98ff-151">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="c98ff-152">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c98ff-152">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="c98ff-153">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="c98ff-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
