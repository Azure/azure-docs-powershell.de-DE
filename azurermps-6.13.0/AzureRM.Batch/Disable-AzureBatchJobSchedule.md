---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
ms.openlocfilehash: e1eb586ff23f5f56cd9fc117f5039d3ccc841367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498465"
---
# <span data-ttu-id="f4725-101">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f4725-101">Disable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="f4725-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f4725-102">SYNOPSIS</span></span>
<span data-ttu-id="f4725-103">Deaktiviert einen stapelverarbeitungsauftrags Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="f4725-103">Disables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4725-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4725-104">SYNTAX</span></span>

```
Disable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4725-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4725-105">DESCRIPTION</span></span>
<span data-ttu-id="f4725-106">Das Cmdlet **Disable-AzureBatchJobSchedule** deaktiviert einen Azure-Batch Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="f4725-106">The **Disable-AzureBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="f4725-107">Wenn Sie einen Terminplan deaktivieren, werden keine Aufträge entsprechend diesem Zeitplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="f4725-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="f4725-108">Sie können einen deaktivierten Zeitplan später aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f4725-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="f4725-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4725-109">EXAMPLES</span></span>

### <span data-ttu-id="f4725-110">Beispiel 1: Deaktivieren eines Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="f4725-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="f4725-111">Dieser Befehl deaktiviert den Auftragszeitplan mit der ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="f4725-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="f4725-112">Verwenden Sie das Cmdlet **Get-AzureRmBatchAccountKeys** , um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="f4725-112">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="f4725-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4725-113">PARAMETERS</span></span>

### <span data-ttu-id="f4725-114">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="f4725-114">-BatchContext</span></span>
<span data-ttu-id="f4725-115">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4725-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f4725-116">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4725-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f4725-117">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f4725-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f4725-118">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4725-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f4725-119">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="f4725-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f4725-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4725-120">-DefaultProfile</span></span>
<span data-ttu-id="f4725-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f4725-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4725-122">-ID</span><span class="sxs-lookup"><span data-stu-id="f4725-122">-Id</span></span>
<span data-ttu-id="f4725-123">Gibt die ID des Auftragszeitplans an, der vom Cmdlet deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="f4725-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="f4725-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4725-124">CommonParameters</span></span>
<span data-ttu-id="f4725-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4725-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4725-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4725-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4725-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f4725-127">INPUTS</span></span>

### <span data-ttu-id="f4725-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f4725-128">System.String</span></span>

### <span data-ttu-id="f4725-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f4725-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="f4725-130">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f4725-130">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="f4725-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f4725-131">OUTPUTS</span></span>

### <span data-ttu-id="f4725-132">System. void</span><span class="sxs-lookup"><span data-stu-id="f4725-132">System.Void</span></span>

## <span data-ttu-id="f4725-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="f4725-133">NOTES</span></span>

## <span data-ttu-id="f4725-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f4725-134">RELATED LINKS</span></span>

[<span data-ttu-id="f4725-135">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f4725-135">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="f4725-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f4725-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="f4725-137">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f4725-137">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="f4725-138">Neu – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f4725-138">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="f4725-139">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f4725-139">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="f4725-140">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f4725-140">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="f4725-141">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="f4725-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


