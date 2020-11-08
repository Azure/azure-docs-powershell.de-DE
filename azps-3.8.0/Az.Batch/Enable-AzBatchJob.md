---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
ms.openlocfilehash: dc3b169df0b29ec47dc54864c5a2999a220a60de
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94007391"
---
# <span data-ttu-id="cce11-101">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="cce11-101">Enable-AzBatchJob</span></span>

## <span data-ttu-id="cce11-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cce11-102">SYNOPSIS</span></span>
<span data-ttu-id="cce11-103">Aktiviert eine Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="cce11-103">Enables a Batch job.</span></span>

## <span data-ttu-id="cce11-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cce11-104">SYNTAX</span></span>

```
Enable-AzBatchJob [-Id] <String> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cce11-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cce11-105">DESCRIPTION</span></span>
<span data-ttu-id="cce11-106">Das Cmdlet **enable-AzBatchJob** aktiviert eine Azure-Batch Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="cce11-106">The **Enable-AzBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="cce11-107">Nachdem Sie einen Auftrag aktiviert haben, können neue Aufgaben ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cce11-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="cce11-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cce11-108">EXAMPLES</span></span>

### <span data-ttu-id="cce11-109">Beispiel 1: Aktivieren eines stapelverarbeitungsauftrags</span><span class="sxs-lookup"><span data-stu-id="cce11-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="cce11-110">Mit diesem Befehl können Sie den Auftrag mit der ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="cce11-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="cce11-111">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="cce11-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="cce11-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="cce11-112">PARAMETERS</span></span>

### <span data-ttu-id="cce11-113">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="cce11-113">-BatchContext</span></span>
<span data-ttu-id="cce11-114">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="cce11-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cce11-115">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="cce11-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cce11-116">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cce11-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cce11-117">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="cce11-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cce11-118">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="cce11-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cce11-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cce11-119">-DefaultProfile</span></span>
<span data-ttu-id="cce11-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cce11-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cce11-121">-ID</span><span class="sxs-lookup"><span data-stu-id="cce11-121">-Id</span></span>
<span data-ttu-id="cce11-122">Gibt die ID des Auftrags an, den dieses Cmdlet aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cce11-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="cce11-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cce11-123">CommonParameters</span></span>
<span data-ttu-id="cce11-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cce11-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cce11-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cce11-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cce11-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cce11-126">INPUTS</span></span>

### <span data-ttu-id="cce11-127">System. String</span><span class="sxs-lookup"><span data-stu-id="cce11-127">System.String</span></span>

### <span data-ttu-id="cce11-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cce11-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cce11-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cce11-129">OUTPUTS</span></span>

### <span data-ttu-id="cce11-130">System. void</span><span class="sxs-lookup"><span data-stu-id="cce11-130">System.Void</span></span>

## <span data-ttu-id="cce11-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="cce11-131">NOTES</span></span>

## <span data-ttu-id="cce11-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cce11-132">RELATED LINKS</span></span>

[<span data-ttu-id="cce11-133">Deaktivieren-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="cce11-133">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="cce11-134">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="cce11-134">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="cce11-135">Neu – AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="cce11-135">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="cce11-136">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="cce11-136">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="cce11-137">Stopp-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="cce11-137">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="cce11-138">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cce11-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


