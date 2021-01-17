---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
ms.openlocfilehash: 247b2494e002ae6340f38aa626b9661dbf7722ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473276"
---
# <span data-ttu-id="6f670-101">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6f670-101">Remove-AzBatchJobSchedule</span></span>

## <span data-ttu-id="6f670-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f670-102">SYNOPSIS</span></span>
<span data-ttu-id="6f670-103">Entfernt einen Stapelauftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="6f670-103">Removes a Batch job schedule.</span></span>

## <span data-ttu-id="6f670-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f670-104">SYNTAX</span></span>

```
Remove-AzBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f670-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f670-105">DESCRIPTION</span></span>
<span data-ttu-id="6f670-106">Das **Cmdlet "Remove-AzBatchJobSchedule"** entfernt einen Azure Batch-Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="6f670-106">The **Remove-AzBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="6f670-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6f670-107">EXAMPLES</span></span>

### <span data-ttu-id="6f670-108">Beispiel 1: Löschen eines Stapelauftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="6f670-108">Example 1: Delete a Batch job schedule</span></span>
```
PS C:\>Remove-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
```

<span data-ttu-id="6f670-109">Mit diesem Befehl wird der Auftragszeitplan mit der ID "MeinJobSchedule" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6f670-109">This command deletes the job schedule that has the ID MyJobSchedule.</span></span>
<span data-ttu-id="6f670-110">Der Befehl fordert Sie zur Bestätigung auf, bevor der Auftrag gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="6f670-110">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="6f670-111">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der Variablen einen Kontext $Context zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="6f670-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="6f670-112">Beispiel 2: Löschen eines Stapelauftrags ohne Bestätigung mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="6f670-112">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context | Remove-AzBatchJobSchedule -Force -BatchContext $Context
```

<span data-ttu-id="6f670-113">Mit diesem Befehl wird der Auftragszeitplan mit der ID "MyJobSchedule" mithilfe des cmdlets Get-AzBatchJobSchedule erhalten.</span><span class="sxs-lookup"><span data-stu-id="6f670-113">This command gets the job schedule that has the ID MyJobSchedule by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="6f670-114">Der Befehl übergibt diesen Auftragszeitplan mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f670-114">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6f670-115">Dieser Auftragszeitplan wird mit dem Befehl gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6f670-115">The command deletes that job schedule.</span></span>
<span data-ttu-id="6f670-116">Da der Befehl den Parameter *"Force"* enthält, werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="6f670-116">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6f670-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f670-117">PARAMETERS</span></span>

### <span data-ttu-id="6f670-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6f670-118">-BatchContext</span></span>
<span data-ttu-id="6f670-119">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6f670-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6f670-120">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="6f670-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6f670-121">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6f670-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6f670-122">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="6f670-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6f670-123">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6f670-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6f670-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f670-124">-DefaultProfile</span></span>
<span data-ttu-id="6f670-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f670-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f670-126">-Force</span><span class="sxs-lookup"><span data-stu-id="6f670-126">-Force</span></span>
<span data-ttu-id="6f670-127">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="6f670-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6f670-128">-ID</span><span class="sxs-lookup"><span data-stu-id="6f670-128">-Id</span></span>
<span data-ttu-id="6f670-129">Gibt die ID des zu entfernenden Auftragsplans an.</span><span class="sxs-lookup"><span data-stu-id="6f670-129">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="6f670-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f670-130">-Confirm</span></span>
<span data-ttu-id="6f670-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6f670-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f670-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6f670-132">-WhatIf</span></span>
<span data-ttu-id="6f670-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6f670-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f670-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f670-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f670-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f670-135">CommonParameters</span></span>
<span data-ttu-id="6f670-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f670-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f670-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f670-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f670-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6f670-138">INPUTS</span></span>

### <span data-ttu-id="6f670-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6f670-139">System.String</span></span>

### <span data-ttu-id="6f670-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6f670-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6f670-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6f670-141">OUTPUTS</span></span>

### <span data-ttu-id="6f670-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="6f670-142">System.Void</span></span>

## <span data-ttu-id="6f670-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6f670-143">NOTES</span></span>

## <span data-ttu-id="6f670-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6f670-144">RELATED LINKS</span></span>

[<span data-ttu-id="6f670-145">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6f670-145">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="6f670-146">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6f670-146">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="6f670-147">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6f670-147">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="6f670-148">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6f670-148">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="6f670-149">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6f670-149">Set-AzBatchJobSchedule</span></span>](./Set-AzBatchJobSchedule.md)

[<span data-ttu-id="6f670-150">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6f670-150">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


