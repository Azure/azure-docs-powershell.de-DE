---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
ms.openlocfilehash: 348924c4243245200666dae6f4e54061783182ce
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94007412"
---
# <span data-ttu-id="eaef8-101">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="eaef8-101">Remove-AzBatchJob</span></span>

## <span data-ttu-id="eaef8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eaef8-102">SYNOPSIS</span></span>
<span data-ttu-id="eaef8-103">Löscht eine Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="eaef8-103">Deletes a Batch job.</span></span>

## <span data-ttu-id="eaef8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eaef8-104">SYNTAX</span></span>

```
Remove-AzBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaef8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eaef8-105">DESCRIPTION</span></span>
<span data-ttu-id="eaef8-106">Das Cmdlet **Remove-AzBatchJob** löscht eine Azure-Batch Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="eaef8-106">The **Remove-AzBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="eaef8-107">Mit diesem Cmdlet werden Sie zur Bestätigung aufgefordert, bevor ein Auftrag entfernt wird, es sei denn, Sie geben den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="eaef8-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="eaef8-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eaef8-108">EXAMPLES</span></span>

### <span data-ttu-id="eaef8-109">Beispiel 1: Löschen eines stapelverarbeitungsauftrags</span><span class="sxs-lookup"><span data-stu-id="eaef8-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="eaef8-110">Mit diesem Befehl wird der Auftrag gelöscht, der die ID Job-000001 hat.</span><span class="sxs-lookup"><span data-stu-id="eaef8-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="eaef8-111">Der Befehl fordert Sie auf, die Bestätigung zu bestätigen, bevor Sie den Auftrag löschen.</span><span class="sxs-lookup"><span data-stu-id="eaef8-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="eaef8-112">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="eaef8-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="eaef8-113">Beispiel 2: Löschen eines stapelverarbeitungsauftrags ohne Bestätigung mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="eaef8-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="eaef8-114">Dieser Befehl ruft den Auftrag mit dem ID-Auftrags-000002 mithilfe des Get-AzBatchJob-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="eaef8-114">This command gets the job that has the ID Job-000002 by using the Get-AzBatchJob cmdlet.</span></span>
<span data-ttu-id="eaef8-115">Der Befehl übergibt diesen Auftrag mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eaef8-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="eaef8-116">Der Befehl löscht diesen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="eaef8-116">The command deletes that job.</span></span>
<span data-ttu-id="eaef8-117">Da der Befehl den Parameter *Force* enthält, werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="eaef8-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="eaef8-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="eaef8-118">PARAMETERS</span></span>

### <span data-ttu-id="eaef8-119">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="eaef8-119">-BatchContext</span></span>
<span data-ttu-id="eaef8-120">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="eaef8-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="eaef8-121">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="eaef8-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="eaef8-122">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="eaef8-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="eaef8-123">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="eaef8-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="eaef8-124">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="eaef8-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="eaef8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaef8-125">-DefaultProfile</span></span>
<span data-ttu-id="eaef8-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eaef8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaef8-127">-Force</span><span class="sxs-lookup"><span data-stu-id="eaef8-127">-Force</span></span>
<span data-ttu-id="eaef8-128">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="eaef8-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eaef8-129">-ID</span><span class="sxs-lookup"><span data-stu-id="eaef8-129">-Id</span></span>
<span data-ttu-id="eaef8-130">Gibt die ID des Auftrags an, den dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="eaef8-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="eaef8-131">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="eaef8-131">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="eaef8-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eaef8-132">-Confirm</span></span>
<span data-ttu-id="eaef8-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eaef8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaef8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaef8-134">-WhatIf</span></span>
<span data-ttu-id="eaef8-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eaef8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaef8-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eaef8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaef8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaef8-137">CommonParameters</span></span>
<span data-ttu-id="eaef8-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaef8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaef8-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eaef8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaef8-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eaef8-140">INPUTS</span></span>

### <span data-ttu-id="eaef8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="eaef8-141">System.String</span></span>

### <span data-ttu-id="eaef8-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="eaef8-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="eaef8-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eaef8-143">OUTPUTS</span></span>

### <span data-ttu-id="eaef8-144">System. void</span><span class="sxs-lookup"><span data-stu-id="eaef8-144">System.Void</span></span>

## <span data-ttu-id="eaef8-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="eaef8-145">NOTES</span></span>

## <span data-ttu-id="eaef8-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eaef8-146">RELATED LINKS</span></span>

[<span data-ttu-id="eaef8-147">Deaktivieren-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="eaef8-147">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="eaef8-148">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="eaef8-148">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="eaef8-149">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="eaef8-149">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="eaef8-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="eaef8-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="eaef8-151">Neu – AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="eaef8-151">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="eaef8-152">Stopp-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="eaef8-152">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="eaef8-153">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="eaef8-153">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


