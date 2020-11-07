---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
ms.openlocfilehash: 2e19e6b1733ccc3dfe0a802756e2c0a517232803
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665112"
---
# <span data-ttu-id="b49f7-101">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b49f7-101">Disable-AzureBatchJob</span></span>

## <span data-ttu-id="b49f7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b49f7-102">SYNOPSIS</span></span>
<span data-ttu-id="b49f7-103">Deaktiviert eine Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="b49f7-103">Disables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b49f7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b49f7-104">SYNTAX</span></span>

```
Disable-AzureBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b49f7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b49f7-105">DESCRIPTION</span></span>
<span data-ttu-id="b49f7-106">Das Cmdlet **Disable-AzureBatchJob** deaktiviert eine Azure-Batch Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="b49f7-106">The **Disable-AzureBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="b49f7-107">Nachdem Sie einen Auftrag aktiviert haben, können neue Aufgaben ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b49f7-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="b49f7-108">Deaktivierte Aufträge führen keine neuen Aufgaben aus.</span><span class="sxs-lookup"><span data-stu-id="b49f7-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="b49f7-109">Sie können einen deaktivierten Auftrag später aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b49f7-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="b49f7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b49f7-110">EXAMPLES</span></span>

### <span data-ttu-id="b49f7-111">Beispiel 1: Deaktivieren eines stapelverarbeitungsauftrags</span><span class="sxs-lookup"><span data-stu-id="b49f7-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzureBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="b49f7-112">Mit diesem Befehl wird der Auftrag mit der ID Job-000001 deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b49f7-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="b49f7-113">Der Befehl beendet die aktiven Aufgaben für den Auftrag.</span><span class="sxs-lookup"><span data-stu-id="b49f7-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="b49f7-114">Verwenden Sie das Cmdlet **Get-AzureRmBatchAccountKeys** , um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="b49f7-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="b49f7-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b49f7-115">PARAMETERS</span></span>

### <span data-ttu-id="b49f7-116">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="b49f7-116">-BatchContext</span></span>
<span data-ttu-id="b49f7-117">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="b49f7-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b49f7-118">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b49f7-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="b49f7-119">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="b49f7-119">-DisableJobOption</span></span>
<span data-ttu-id="b49f7-120">Gibt an, was mit aktiven Aufgaben zu tun ist, die dem Auftrag zugeordnet sind, den dieses Cmdlet deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b49f7-120">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="b49f7-121">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b49f7-121">Valid values are:</span></span> 

- <span data-ttu-id="b49f7-122">Erneute Warteschlange</span><span class="sxs-lookup"><span data-stu-id="b49f7-122">Requeue</span></span> 
- <span data-ttu-id="b49f7-123">Beenden</span><span class="sxs-lookup"><span data-stu-id="b49f7-123">Terminate</span></span> 
- <span data-ttu-id="b49f7-124">Warte</span><span class="sxs-lookup"><span data-stu-id="b49f7-124">Wait</span></span>

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

### <span data-ttu-id="b49f7-125">-ID</span><span class="sxs-lookup"><span data-stu-id="b49f7-125">-Id</span></span>
<span data-ttu-id="b49f7-126">Gibt die ID des Auftrags an, den dieses Cmdlet deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b49f7-126">Specifies the ID of the job that this cmdlet disables.</span></span>

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

### <span data-ttu-id="b49f7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b49f7-127">-DefaultProfile</span></span>
<span data-ttu-id="b49f7-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b49f7-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b49f7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b49f7-129">CommonParameters</span></span>
<span data-ttu-id="b49f7-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b49f7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b49f7-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b49f7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b49f7-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b49f7-132">INPUTS</span></span>

### <span data-ttu-id="b49f7-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b49f7-133">BatchAccountContext</span></span>
<span data-ttu-id="b49f7-134">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b49f7-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b49f7-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b49f7-135">String</span></span>
<span data-ttu-id="b49f7-136">Der Parameter "ID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b49f7-136">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="b49f7-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b49f7-137">OUTPUTS</span></span>

## <span data-ttu-id="b49f7-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="b49f7-138">NOTES</span></span>

## <span data-ttu-id="b49f7-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b49f7-139">RELATED LINKS</span></span>

[<span data-ttu-id="b49f7-140">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b49f7-140">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="b49f7-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b49f7-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b49f7-142">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b49f7-142">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="b49f7-143">Neu – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b49f7-143">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="b49f7-144">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b49f7-144">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="b49f7-145">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b49f7-145">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="b49f7-146">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="b49f7-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


