---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
ms.openlocfilehash: 545979c621a807c2a866fc5cf1d29aa0b659dc82
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299067"
---
# <span data-ttu-id="5fe61-101">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="5fe61-101">Enable-AzBatchJob</span></span>

## <span data-ttu-id="5fe61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fe61-102">SYNOPSIS</span></span>
<span data-ttu-id="5fe61-103">Aktiviert einen Stapelauftrag.</span><span class="sxs-lookup"><span data-stu-id="5fe61-103">Enables a Batch job.</span></span>

## <span data-ttu-id="5fe61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5fe61-104">SYNTAX</span></span>

```
Enable-AzBatchJob [-Id] <String> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5fe61-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fe61-105">DESCRIPTION</span></span>
<span data-ttu-id="5fe61-106">Das **Cmdlet "Enable-AzBatchJob"** aktiviert einen Azure Batch-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="5fe61-106">The **Enable-AzBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="5fe61-107">Nachdem Sie einen Auftrag aktiviert haben, können neue Aufgaben ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5fe61-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="5fe61-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5fe61-108">EXAMPLES</span></span>

### <span data-ttu-id="5fe61-109">Beispiel 1: Aktivieren eines Stapelauftrags</span><span class="sxs-lookup"><span data-stu-id="5fe61-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="5fe61-110">Dieser Befehl aktiviert den Auftrag mit der ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="5fe61-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="5fe61-111">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der Variablen einen Kontext $Context zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="5fe61-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="5fe61-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fe61-112">PARAMETERS</span></span>

### <span data-ttu-id="5fe61-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5fe61-113">-BatchContext</span></span>
<span data-ttu-id="5fe61-114">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5fe61-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5fe61-115">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fe61-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5fe61-116">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5fe61-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5fe61-117">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fe61-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5fe61-118">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5fe61-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5fe61-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fe61-119">-DefaultProfile</span></span>
<span data-ttu-id="5fe61-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5fe61-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fe61-121">-ID</span><span class="sxs-lookup"><span data-stu-id="5fe61-121">-Id</span></span>
<span data-ttu-id="5fe61-122">Gibt die ID des Auftrags an, den dieses Cmdlet aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5fe61-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="5fe61-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe61-123">CommonParameters</span></span>
<span data-ttu-id="5fe61-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fe61-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe61-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fe61-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe61-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5fe61-126">INPUTS</span></span>

### <span data-ttu-id="5fe61-127">System.String</span><span class="sxs-lookup"><span data-stu-id="5fe61-127">System.String</span></span>

### <span data-ttu-id="5fe61-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5fe61-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5fe61-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5fe61-129">OUTPUTS</span></span>

### <span data-ttu-id="5fe61-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="5fe61-130">System.Void</span></span>

## <span data-ttu-id="5fe61-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5fe61-131">NOTES</span></span>

## <span data-ttu-id="5fe61-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5fe61-132">RELATED LINKS</span></span>

[<span data-ttu-id="5fe61-133">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="5fe61-133">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="5fe61-134">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="5fe61-134">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="5fe61-135">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="5fe61-135">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="5fe61-136">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="5fe61-136">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="5fe61-137">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="5fe61-137">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="5fe61-138">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="5fe61-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
