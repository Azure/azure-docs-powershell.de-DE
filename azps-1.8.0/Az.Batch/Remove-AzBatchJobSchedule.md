---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
ms.openlocfilehash: 398671292e67520977a683c3da9178b33dc69329
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661662"
---
# <span data-ttu-id="741ba-101">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="741ba-101">Remove-AzBatchJobSchedule</span></span>

## <span data-ttu-id="741ba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="741ba-102">SYNOPSIS</span></span>
<span data-ttu-id="741ba-103">Entfernt einen stapelverarbeitungsauftrags Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="741ba-103">Removes a Batch job schedule.</span></span>

## <span data-ttu-id="741ba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="741ba-104">SYNTAX</span></span>

```
Remove-AzBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="741ba-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="741ba-105">DESCRIPTION</span></span>
<span data-ttu-id="741ba-106">Das Cmdlet **Remove-AzBatchJobSchedule** entfernt einen Azure-Batch Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="741ba-106">The **Remove-AzBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="741ba-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="741ba-107">EXAMPLES</span></span>

### <span data-ttu-id="741ba-108">Beispiel 1: Löschen eines stapelverarbeitungsauftrags-Zeitplans</span><span class="sxs-lookup"><span data-stu-id="741ba-108">Example 1: Delete a Batch job schedule</span></span>
```
PS C:\>Remove-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
```

<span data-ttu-id="741ba-109">Dieser Befehl löscht den Auftragszeitplan mit der ID MyJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="741ba-109">This command deletes the job schedule that has the ID MyJobSchedule.</span></span>
<span data-ttu-id="741ba-110">Der Befehl fordert Sie auf, die Bestätigung zu bestätigen, bevor Sie den Auftrag löschen.</span><span class="sxs-lookup"><span data-stu-id="741ba-110">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="741ba-111">Verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="741ba-111">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="741ba-112">Beispiel 2: Löschen eines stapelverarbeitungsauftrags ohne Bestätigung mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="741ba-112">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context | Remove-AzBatchJobSchedule -Force -BatchContext $Context
```

<span data-ttu-id="741ba-113">Dieser Befehl ruft den Auftragszeitplan mit der ID-MyJobSchedule mithilfe des Get-AzBatchJobSchedule-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="741ba-113">This command gets the job schedule that has the ID MyJobSchedule by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="741ba-114">Der Befehl übergibt diesen Auftragszeitplan mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="741ba-114">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="741ba-115">Der Befehl löscht diesen Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="741ba-115">The command deletes that job schedule.</span></span>
<span data-ttu-id="741ba-116">Da der Befehl den Parameter *Force* enthält, werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="741ba-116">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="741ba-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="741ba-117">PARAMETERS</span></span>

### <span data-ttu-id="741ba-118">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="741ba-118">-BatchContext</span></span>
<span data-ttu-id="741ba-119">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="741ba-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="741ba-120">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="741ba-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="741ba-121">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="741ba-121">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="741ba-122">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="741ba-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="741ba-123">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="741ba-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="741ba-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="741ba-124">-DefaultProfile</span></span>
<span data-ttu-id="741ba-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="741ba-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="741ba-126">-Force</span><span class="sxs-lookup"><span data-stu-id="741ba-126">-Force</span></span>
<span data-ttu-id="741ba-127">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="741ba-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="741ba-128">-ID</span><span class="sxs-lookup"><span data-stu-id="741ba-128">-Id</span></span>
<span data-ttu-id="741ba-129">Gibt die ID des Auftragszeitplans an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="741ba-129">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="741ba-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="741ba-130">-Confirm</span></span>
<span data-ttu-id="741ba-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="741ba-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="741ba-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="741ba-132">-WhatIf</span></span>
<span data-ttu-id="741ba-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="741ba-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="741ba-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="741ba-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="741ba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="741ba-135">CommonParameters</span></span>
<span data-ttu-id="741ba-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="741ba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="741ba-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="741ba-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="741ba-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="741ba-138">INPUTS</span></span>

### <span data-ttu-id="741ba-139">System. String</span><span class="sxs-lookup"><span data-stu-id="741ba-139">System.String</span></span>

### <span data-ttu-id="741ba-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="741ba-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="741ba-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="741ba-141">OUTPUTS</span></span>

### <span data-ttu-id="741ba-142">System. void</span><span class="sxs-lookup"><span data-stu-id="741ba-142">System.Void</span></span>

## <span data-ttu-id="741ba-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="741ba-143">NOTES</span></span>

## <span data-ttu-id="741ba-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="741ba-144">RELATED LINKS</span></span>

[<span data-ttu-id="741ba-145">Deaktivieren-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="741ba-145">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="741ba-146">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="741ba-146">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="741ba-147">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="741ba-147">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="741ba-148">Neu – AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="741ba-148">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="741ba-149">Satz-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="741ba-149">Set-AzBatchJobSchedule</span></span>](./Set-AzBatchJobSchedule.md)

[<span data-ttu-id="741ba-150">Stopp-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="741ba-150">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


