---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
ms.openlocfilehash: 0d210056670baa974c7bf11e9c44142c11f2721e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501934"
---
# <span data-ttu-id="9f4f8-101">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="9f4f8-101">Remove-AzureBatchJob</span></span>

## <span data-ttu-id="9f4f8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9f4f8-102">SYNOPSIS</span></span>
<span data-ttu-id="9f4f8-103">Löscht eine Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="9f4f8-103">Deletes a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f4f8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f4f8-104">SYNTAX</span></span>

```
Remove-AzureBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f4f8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f4f8-105">DESCRIPTION</span></span>
<span data-ttu-id="9f4f8-106">Das Cmdlet **Remove-AzureBatchJob** löscht eine Azure-Batch Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="9f4f8-106">The **Remove-AzureBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="9f4f8-107">Mit diesem Cmdlet werden Sie zur Bestätigung aufgefordert, bevor ein Auftrag entfernt wird, es sei denn, Sie geben den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="9f4f8-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="9f4f8-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9f4f8-108">EXAMPLES</span></span>

### <span data-ttu-id="9f4f8-109">Beispiel 1: Löschen eines stapelverarbeitungsauftrags</span><span class="sxs-lookup"><span data-stu-id="9f4f8-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="9f4f8-110">Mit diesem Befehl wird der Auftrag gelöscht, der die ID Job-000001 hat.</span><span class="sxs-lookup"><span data-stu-id="9f4f8-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="9f4f8-111">Der Befehl fordert Sie auf, die Bestätigung zu bestätigen, bevor Sie den Auftrag löschen.</span><span class="sxs-lookup"><span data-stu-id="9f4f8-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="9f4f8-112">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="9f4f8-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="9f4f8-113">Beispiel 2: Löschen eines stapelverarbeitungsauftrags ohne Bestätigung mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="9f4f8-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzureBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="9f4f8-114">Dieser Befehl ruft den Auftrag mit dem ID-Auftrags-000002 mithilfe des Get-AzureBatchJob-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="9f4f8-114">This command gets the job that has the ID Job-000002 by using the Get-AzureBatchJob cmdlet.</span></span>
<span data-ttu-id="9f4f8-115">Der Befehl übergibt diesen Auftrag mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f4f8-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9f4f8-116">Der Befehl löscht diesen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="9f4f8-116">The command deletes that job.</span></span>
<span data-ttu-id="9f4f8-117">Da der Befehl den Parameter *Force* enthält, werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="9f4f8-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9f4f8-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f4f8-118">PARAMETERS</span></span>

### <span data-ttu-id="9f4f8-119">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="9f4f8-119">-BatchContext</span></span>
<span data-ttu-id="9f4f8-120">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f4f8-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9f4f8-121">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f4f8-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="9f4f8-122">-Force</span><span class="sxs-lookup"><span data-stu-id="9f4f8-122">-Force</span></span>
<span data-ttu-id="9f4f8-123">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9f4f8-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9f4f8-124">-ID</span><span class="sxs-lookup"><span data-stu-id="9f4f8-124">-Id</span></span>
<span data-ttu-id="9f4f8-125">Gibt die ID des Auftrags an, den dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="9f4f8-125">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="9f4f8-126">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="9f4f8-126">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="9f4f8-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9f4f8-127">-Confirm</span></span>
<span data-ttu-id="9f4f8-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f4f8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f4f8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f4f8-129">-WhatIf</span></span>
<span data-ttu-id="9f4f8-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f4f8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f4f8-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f4f8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f4f8-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f4f8-132">-DefaultProfile</span></span>
<span data-ttu-id="9f4f8-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9f4f8-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f4f8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f4f8-134">CommonParameters</span></span>
<span data-ttu-id="9f4f8-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f4f8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f4f8-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f4f8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f4f8-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9f4f8-137">INPUTS</span></span>

### <span data-ttu-id="9f4f8-138">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9f4f8-138">BatchAccountContext</span></span>
<span data-ttu-id="9f4f8-139">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9f4f8-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="9f4f8-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9f4f8-140">OUTPUTS</span></span>

## <span data-ttu-id="9f4f8-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="9f4f8-141">NOTES</span></span>

## <span data-ttu-id="9f4f8-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9f4f8-142">RELATED LINKS</span></span>

[<span data-ttu-id="9f4f8-143">Deaktivieren-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="9f4f8-143">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="9f4f8-144">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="9f4f8-144">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="9f4f8-145">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="9f4f8-145">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="9f4f8-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9f4f8-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="9f4f8-147">Neu – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="9f4f8-147">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="9f4f8-148">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="9f4f8-148">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="9f4f8-149">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="9f4f8-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


