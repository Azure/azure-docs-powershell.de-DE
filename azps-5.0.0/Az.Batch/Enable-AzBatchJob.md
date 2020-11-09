---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
ms.openlocfilehash: 545979c621a807c2a866fc5cf1d29aa0b659dc82
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303825"
---
# <span data-ttu-id="92e15-101">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="92e15-101">Enable-AzBatchJob</span></span>

## <span data-ttu-id="92e15-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="92e15-102">SYNOPSIS</span></span>
<span data-ttu-id="92e15-103">Aktiviert eine Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="92e15-103">Enables a Batch job.</span></span>

## <span data-ttu-id="92e15-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="92e15-104">SYNTAX</span></span>

```
Enable-AzBatchJob [-Id] <String> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92e15-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92e15-105">DESCRIPTION</span></span>
<span data-ttu-id="92e15-106">Das Cmdlet **enable-AzBatchJob** aktiviert eine Azure-Batch Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="92e15-106">The **Enable-AzBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="92e15-107">Nachdem Sie einen Auftrag aktiviert haben, können neue Aufgaben ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="92e15-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="92e15-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92e15-108">EXAMPLES</span></span>

### <span data-ttu-id="92e15-109">Beispiel 1: Aktivieren eines stapelverarbeitungsauftrags</span><span class="sxs-lookup"><span data-stu-id="92e15-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="92e15-110">Mit diesem Befehl können Sie den Auftrag mit der ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="92e15-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="92e15-111">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="92e15-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="92e15-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="92e15-112">PARAMETERS</span></span>

### <span data-ttu-id="92e15-113">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="92e15-113">-BatchContext</span></span>
<span data-ttu-id="92e15-114">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="92e15-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="92e15-115">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="92e15-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="92e15-116">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="92e15-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="92e15-117">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="92e15-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="92e15-118">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="92e15-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="92e15-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e15-119">-DefaultProfile</span></span>
<span data-ttu-id="92e15-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="92e15-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92e15-121">-ID</span><span class="sxs-lookup"><span data-stu-id="92e15-121">-Id</span></span>
<span data-ttu-id="92e15-122">Gibt die ID des Auftrags an, den dieses Cmdlet aktiviert.</span><span class="sxs-lookup"><span data-stu-id="92e15-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="92e15-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e15-123">CommonParameters</span></span>
<span data-ttu-id="92e15-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92e15-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e15-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92e15-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e15-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="92e15-126">INPUTS</span></span>

### <span data-ttu-id="92e15-127">System. String</span><span class="sxs-lookup"><span data-stu-id="92e15-127">System.String</span></span>

### <span data-ttu-id="92e15-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="92e15-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="92e15-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="92e15-129">OUTPUTS</span></span>

### <span data-ttu-id="92e15-130">System. void</span><span class="sxs-lookup"><span data-stu-id="92e15-130">System.Void</span></span>

## <span data-ttu-id="92e15-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="92e15-131">NOTES</span></span>

## <span data-ttu-id="92e15-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="92e15-132">RELATED LINKS</span></span>

[<span data-ttu-id="92e15-133">Deaktivieren-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="92e15-133">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="92e15-134">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="92e15-134">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="92e15-135">Neu – AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="92e15-135">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="92e15-136">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="92e15-136">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="92e15-137">Stopp-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="92e15-137">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="92e15-138">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="92e15-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
