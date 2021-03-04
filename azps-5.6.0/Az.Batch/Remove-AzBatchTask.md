---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
ms.openlocfilehash: 83ac1df0259d39dd1db301e836479193b17f1dee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943128"
---
# <span data-ttu-id="3bb9d-101">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3bb9d-101">Remove-AzBatchTask</span></span>

## <span data-ttu-id="3bb9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bb9d-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb9d-103">Löscht eine Batchaufgabe.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-103">Deletes a Batch task.</span></span>

## <span data-ttu-id="3bb9d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3bb9d-104">SYNTAX</span></span>

### <span data-ttu-id="3bb9d-105">ID</span><span class="sxs-lookup"><span data-stu-id="3bb9d-105">Id</span></span>
```
Remove-AzBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bb9d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3bb9d-106">InputObject</span></span>
```
Remove-AzBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bb9d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3bb9d-107">DESCRIPTION</span></span>
<span data-ttu-id="3bb9d-108">Das **Cmdlet Remove-AzBatchTask** löscht eine Azure Batch-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-108">The **Remove-AzBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="3bb9d-109">Dieses Cmdlet fordert Sie zur Bestätigung auf, es sei denn, Sie geben den Parameter *Erzwingen* an.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="3bb9d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3bb9d-110">EXAMPLES</span></span>

### <span data-ttu-id="3bb9d-111">Beispiel 1: Löschen einer Batchaufgabe nach ID</span><span class="sxs-lookup"><span data-stu-id="3bb9d-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="3bb9d-112">Mit diesem Befehl wird eine Aufgabe gelöscht, die die ID Task23 unter dem Auftrag mit der ID Job-000001 hat.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="3bb9d-113">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="3bb9d-114">Verwenden Sie **das Get-AzBatchAccountKey-Cmdlet,** um der Variablen "$Context" einen Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="3bb9d-115">Beispiel 2: Löschen einer Batchaufgabe mithilfe der Pipeline ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="3bb9d-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="3bb9d-116">Mit diesem Befehl wird die Batchaufgabe mit der ID Task26 in dem Auftrag mit der ID Job-000001 mithilfe des **Get-AzBatchTask-Cmdlets** ab.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzBatchTask** cmdlet.</span></span>
<span data-ttu-id="3bb9d-117">Der Befehl übergibt diese Aufgabe mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3bb9d-118">Mit dem Befehl wird diese Aufgabe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-118">The command deletes that task.</span></span>
<span data-ttu-id="3bb9d-119">Dieser Befehl gibt den Parameter *Kraft* an.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="3bb9d-120">Daher werden Sie mit dem Befehl nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3bb9d-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3bb9d-121">PARAMETERS</span></span>

### <span data-ttu-id="3bb9d-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3bb9d-122">-BatchContext</span></span>
<span data-ttu-id="3bb9d-123">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3bb9d-124">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-124">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3bb9d-125">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-125">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3bb9d-126">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3bb9d-127">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3bb9d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bb9d-128">-DefaultProfile</span></span>
<span data-ttu-id="3bb9d-129">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bb9d-130">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="3bb9d-130">-Force</span></span>
<span data-ttu-id="3bb9d-131">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3bb9d-132">-ID</span><span class="sxs-lookup"><span data-stu-id="3bb9d-132">-Id</span></span>
<span data-ttu-id="3bb9d-133">Gibt die ID der Aufgabe an, die von diesem Cmdlet gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="3bb9d-134">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-134">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bb9d-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bb9d-135">-InputObject</span></span>
<span data-ttu-id="3bb9d-136">Gibt die Aufgabe an, die von diesem Cmdlet gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="3bb9d-137">Zum Abrufen eines **PSCloudTask-Objekts** verwenden Sie das Get-AzBatchTask Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-137">To obtain a **PSCloudTask** object, use  the Get-AzBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bb9d-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="3bb9d-138">-JobId</span></span>
<span data-ttu-id="3bb9d-139">Gibt die ID des Auftrags an, der den Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-139">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bb9d-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3bb9d-140">-Confirm</span></span>
<span data-ttu-id="3bb9d-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bb9d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bb9d-142">-WhatIf</span></span>
<span data-ttu-id="3bb9d-143">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bb9d-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bb9d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb9d-145">CommonParameters</span></span>
<span data-ttu-id="3bb9d-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bb9d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb9d-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bb9d-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb9d-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3bb9d-148">INPUTS</span></span>

### <span data-ttu-id="3bb9d-149">System.String</span><span class="sxs-lookup"><span data-stu-id="3bb9d-149">System.String</span></span>

### <span data-ttu-id="3bb9d-150">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="3bb9d-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="3bb9d-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3bb9d-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3bb9d-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3bb9d-152">OUTPUTS</span></span>

### <span data-ttu-id="3bb9d-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="3bb9d-153">System.Void</span></span>

## <span data-ttu-id="3bb9d-154">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3bb9d-154">NOTES</span></span>

## <span data-ttu-id="3bb9d-155">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3bb9d-155">RELATED LINKS</span></span>

[<span data-ttu-id="3bb9d-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3bb9d-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="3bb9d-157">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3bb9d-157">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="3bb9d-158">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3bb9d-158">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="3bb9d-159">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3bb9d-159">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="3bb9d-160">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3bb9d-160">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="3bb9d-161">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3bb9d-161">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
