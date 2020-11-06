---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: be73b757bf20a2f688d7f7293ac4022e7bc8f4aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498446"
---
# <span data-ttu-id="2d0a5-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="2d0a5-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="2d0a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d0a5-102">SYNOPSIS</span></span>
<span data-ttu-id="2d0a5-103">Aktiviert eine Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="2d0a5-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d0a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d0a5-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d0a5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d0a5-105">DESCRIPTION</span></span>
<span data-ttu-id="2d0a5-106">Das Cmdlet **enable-AzureBatchJob** aktiviert eine Azure-Batch Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="2d0a5-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="2d0a5-107">Nachdem Sie einen Auftrag aktiviert haben, können neue Aufgaben ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2d0a5-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="2d0a5-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d0a5-108">EXAMPLES</span></span>

### <span data-ttu-id="2d0a5-109">Beispiel 1: Aktivieren eines stapelverarbeitungsauftrags</span><span class="sxs-lookup"><span data-stu-id="2d0a5-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="2d0a5-110">Mit diesem Befehl können Sie den Auftrag mit der ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="2d0a5-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="2d0a5-111">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="2d0a5-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="2d0a5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d0a5-112">PARAMETERS</span></span>

### <span data-ttu-id="2d0a5-113">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="2d0a5-113">-BatchContext</span></span>
<span data-ttu-id="2d0a5-114">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d0a5-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2d0a5-115">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d0a5-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2d0a5-116">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2d0a5-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2d0a5-117">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d0a5-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2d0a5-118">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="2d0a5-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2d0a5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d0a5-119">-DefaultProfile</span></span>
<span data-ttu-id="2d0a5-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2d0a5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d0a5-121">-ID</span><span class="sxs-lookup"><span data-stu-id="2d0a5-121">-Id</span></span>
<span data-ttu-id="2d0a5-122">Gibt die ID des Auftrags an, den dieses Cmdlet aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2d0a5-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="2d0a5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d0a5-123">CommonParameters</span></span>
<span data-ttu-id="2d0a5-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d0a5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d0a5-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d0a5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d0a5-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d0a5-126">INPUTS</span></span>

### <span data-ttu-id="2d0a5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2d0a5-127">System.String</span></span>

### <span data-ttu-id="2d0a5-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2d0a5-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="2d0a5-129">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2d0a5-129">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="2d0a5-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d0a5-130">OUTPUTS</span></span>

### <span data-ttu-id="2d0a5-131">System. void</span><span class="sxs-lookup"><span data-stu-id="2d0a5-131">System.Void</span></span>

## <span data-ttu-id="2d0a5-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d0a5-132">NOTES</span></span>

## <span data-ttu-id="2d0a5-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d0a5-133">RELATED LINKS</span></span>

[<span data-ttu-id="2d0a5-134">Deaktivieren-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="2d0a5-134">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="2d0a5-135">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="2d0a5-135">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="2d0a5-136">Neu – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="2d0a5-136">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="2d0a5-137">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="2d0a5-137">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="2d0a5-138">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="2d0a5-138">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="2d0a5-139">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2d0a5-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


