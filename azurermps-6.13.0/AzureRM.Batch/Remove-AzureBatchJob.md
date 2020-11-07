---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
ms.openlocfilehash: fa7dede61cd19ec0ea0a4ccd59f2eca3e0cc8f41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663010"
---
# <span data-ttu-id="99213-101">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="99213-101">Remove-AzureBatchJob</span></span>

## <span data-ttu-id="99213-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="99213-102">SYNOPSIS</span></span>
<span data-ttu-id="99213-103">Löscht eine Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="99213-103">Deletes a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99213-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="99213-104">SYNTAX</span></span>

```
Remove-AzureBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99213-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99213-105">DESCRIPTION</span></span>
<span data-ttu-id="99213-106">Das Cmdlet **Remove-AzureBatchJob** löscht eine Azure-Batch Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="99213-106">The **Remove-AzureBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="99213-107">Mit diesem Cmdlet werden Sie zur Bestätigung aufgefordert, bevor ein Auftrag entfernt wird, es sei denn, Sie geben den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="99213-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="99213-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="99213-108">EXAMPLES</span></span>

### <span data-ttu-id="99213-109">Beispiel 1: Löschen eines stapelverarbeitungsauftrags</span><span class="sxs-lookup"><span data-stu-id="99213-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="99213-110">Mit diesem Befehl wird der Auftrag gelöscht, der die ID Job-000001 hat.</span><span class="sxs-lookup"><span data-stu-id="99213-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="99213-111">Der Befehl fordert Sie auf, die Bestätigung zu bestätigen, bevor Sie den Auftrag löschen.</span><span class="sxs-lookup"><span data-stu-id="99213-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="99213-112">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="99213-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="99213-113">Beispiel 2: Löschen eines stapelverarbeitungsauftrags ohne Bestätigung mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="99213-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzureBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="99213-114">Dieser Befehl ruft den Auftrag mit dem ID-Auftrags-000002 mithilfe des Get-AzureBatchJob-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="99213-114">This command gets the job that has the ID Job-000002 by using the Get-AzureBatchJob cmdlet.</span></span>
<span data-ttu-id="99213-115">Der Befehl übergibt diesen Auftrag mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99213-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="99213-116">Der Befehl löscht diesen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="99213-116">The command deletes that job.</span></span>
<span data-ttu-id="99213-117">Da der Befehl den Parameter *Force* enthält, werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="99213-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="99213-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="99213-118">PARAMETERS</span></span>

### <span data-ttu-id="99213-119">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="99213-119">-BatchContext</span></span>
<span data-ttu-id="99213-120">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="99213-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="99213-121">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="99213-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="99213-122">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="99213-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="99213-123">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="99213-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="99213-124">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="99213-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="99213-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99213-125">-DefaultProfile</span></span>
<span data-ttu-id="99213-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="99213-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99213-127">-Force</span><span class="sxs-lookup"><span data-stu-id="99213-127">-Force</span></span>
<span data-ttu-id="99213-128">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="99213-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="99213-129">-ID</span><span class="sxs-lookup"><span data-stu-id="99213-129">-Id</span></span>
<span data-ttu-id="99213-130">Gibt die ID des Auftrags an, den dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="99213-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="99213-131">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="99213-131">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="99213-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="99213-132">-Confirm</span></span>
<span data-ttu-id="99213-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="99213-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99213-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99213-134">-WhatIf</span></span>
<span data-ttu-id="99213-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99213-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99213-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="99213-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99213-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99213-137">CommonParameters</span></span>
<span data-ttu-id="99213-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99213-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99213-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99213-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99213-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="99213-140">INPUTS</span></span>

### <span data-ttu-id="99213-141">System. String</span><span class="sxs-lookup"><span data-stu-id="99213-141">System.String</span></span>

### <span data-ttu-id="99213-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="99213-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="99213-143">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="99213-143">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="99213-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="99213-144">OUTPUTS</span></span>

### <span data-ttu-id="99213-145">System. void</span><span class="sxs-lookup"><span data-stu-id="99213-145">System.Void</span></span>

## <span data-ttu-id="99213-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="99213-146">NOTES</span></span>

## <span data-ttu-id="99213-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="99213-147">RELATED LINKS</span></span>

[<span data-ttu-id="99213-148">Deaktivieren-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="99213-148">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="99213-149">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="99213-149">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="99213-150">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="99213-150">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="99213-151">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="99213-151">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="99213-152">Neu – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="99213-152">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="99213-153">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="99213-153">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="99213-154">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="99213-154">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


