---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
ms.openlocfilehash: fcb3586d1c27fd95c6bf386943830b92635162e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505793"
---
# <span data-ttu-id="5a1c0-101">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5a1c0-101">Disable-AzureBatchJob</span></span>

## <span data-ttu-id="5a1c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a1c0-102">SYNOPSIS</span></span>
<span data-ttu-id="5a1c0-103">Deaktiviert eine Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="5a1c0-103">Disables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a1c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a1c0-104">SYNTAX</span></span>

```
Disable-AzureBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a1c0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a1c0-105">DESCRIPTION</span></span>
<span data-ttu-id="5a1c0-106">Das Cmdlet **Disable-AzureBatchJob** deaktiviert eine Azure-Batch Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="5a1c0-106">The **Disable-AzureBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="5a1c0-107">Nachdem Sie einen Auftrag aktiviert haben, können neue Aufgaben ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5a1c0-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="5a1c0-108">Deaktivierte Aufträge führen keine neuen Aufgaben aus.</span><span class="sxs-lookup"><span data-stu-id="5a1c0-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="5a1c0-109">Sie können einen deaktivierten Auftrag später aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5a1c0-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="5a1c0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a1c0-110">EXAMPLES</span></span>

### <span data-ttu-id="5a1c0-111">Beispiel 1: Deaktivieren eines stapelverarbeitungsauftrags</span><span class="sxs-lookup"><span data-stu-id="5a1c0-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzureBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="5a1c0-112">Mit diesem Befehl wird der Auftrag mit der ID Job-000001 deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5a1c0-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="5a1c0-113">Der Befehl beendet die aktiven Aufgaben für den Auftrag.</span><span class="sxs-lookup"><span data-stu-id="5a1c0-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="5a1c0-114">Verwenden Sie das Cmdlet **Get-AzureRmBatchAccountKeys** , um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="5a1c0-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="5a1c0-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a1c0-115">PARAMETERS</span></span>

### <span data-ttu-id="5a1c0-116">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="5a1c0-116">-BatchContext</span></span>
<span data-ttu-id="5a1c0-117">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a1c0-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5a1c0-118">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a1c0-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5a1c0-119">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5a1c0-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5a1c0-120">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a1c0-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5a1c0-121">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="5a1c0-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a1c0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a1c0-122">-DefaultProfile</span></span>
<span data-ttu-id="5a1c0-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5a1c0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a1c0-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="5a1c0-124">-DisableJobOption</span></span>
<span data-ttu-id="5a1c0-125">Gibt an, was mit aktiven Aufgaben zu tun ist, die dem Auftrag zugeordnet sind, den dieses Cmdlet deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5a1c0-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="5a1c0-126">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="5a1c0-126">Valid values are:</span></span> 

- <span data-ttu-id="5a1c0-127">Erneute Warteschlange</span><span class="sxs-lookup"><span data-stu-id="5a1c0-127">Requeue</span></span> 
- <span data-ttu-id="5a1c0-128">Beenden</span><span class="sxs-lookup"><span data-stu-id="5a1c0-128">Terminate</span></span> 
- <span data-ttu-id="5a1c0-129">Warte</span><span class="sxs-lookup"><span data-stu-id="5a1c0-129">Wait</span></span>

```yaml
Type: DisableJobOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a1c0-130">-ID</span><span class="sxs-lookup"><span data-stu-id="5a1c0-130">-Id</span></span>
<span data-ttu-id="5a1c0-131">Gibt die ID des Auftrags an, den dieses Cmdlet deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5a1c0-131">Specifies the ID of the job that this cmdlet disables.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a1c0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a1c0-132">CommonParameters</span></span>
<span data-ttu-id="5a1c0-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a1c0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a1c0-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a1c0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a1c0-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a1c0-135">INPUTS</span></span>

### <span data-ttu-id="5a1c0-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5a1c0-136">BatchAccountContext</span></span>
<span data-ttu-id="5a1c0-137">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5a1c0-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="5a1c0-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5a1c0-138">String</span></span>
<span data-ttu-id="5a1c0-139">Der Parameter "ID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5a1c0-139">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5a1c0-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a1c0-140">OUTPUTS</span></span>

## <span data-ttu-id="5a1c0-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a1c0-141">NOTES</span></span>

## <span data-ttu-id="5a1c0-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a1c0-142">RELATED LINKS</span></span>

[<span data-ttu-id="5a1c0-143">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5a1c0-143">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="5a1c0-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5a1c0-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5a1c0-145">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5a1c0-145">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="5a1c0-146">Neu – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5a1c0-146">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="5a1c0-147">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5a1c0-147">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="5a1c0-148">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5a1c0-148">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="5a1c0-149">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="5a1c0-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


