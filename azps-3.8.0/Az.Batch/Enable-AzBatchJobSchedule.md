---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
ms.openlocfilehash: 0684652dd5e5a0232e5808119ae8453be8f9ade8
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94007390"
---
# <span data-ttu-id="f7478-101">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f7478-101">Enable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="f7478-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7478-102">SYNOPSIS</span></span>
<span data-ttu-id="f7478-103">Aktiviert einen Stapel Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="f7478-103">Enables a Batch job schedule.</span></span>

## <span data-ttu-id="f7478-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7478-104">SYNTAX</span></span>

```
Enable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7478-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7478-105">DESCRIPTION</span></span>
<span data-ttu-id="f7478-106">Das Cmdlet **enable-AzBatchJobSchedule** aktiviert einen Azure-Batch Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="f7478-106">The **Enable-AzBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="f7478-107">Nachdem Sie einen Projektplan aktiviert haben, können Aufträge entsprechend diesem Zeitplan erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f7478-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="f7478-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7478-108">EXAMPLES</span></span>

### <span data-ttu-id="f7478-109">Beispiel 1: Aktivieren eines Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="f7478-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="f7478-110">Dieser Befehl aktiviert den Auftragszeitplan mit der ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="f7478-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="f7478-111">Verwenden Sie das Cmdlet **Get-AzBatchAccountKey** , um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="f7478-111">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="f7478-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7478-112">PARAMETERS</span></span>

### <span data-ttu-id="f7478-113">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="f7478-113">-BatchContext</span></span>
<span data-ttu-id="f7478-114">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="f7478-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f7478-115">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="f7478-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f7478-116">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f7478-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f7478-117">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="f7478-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f7478-118">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="f7478-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f7478-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7478-119">-DefaultProfile</span></span>
<span data-ttu-id="f7478-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f7478-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7478-121">-ID</span><span class="sxs-lookup"><span data-stu-id="f7478-121">-Id</span></span>
<span data-ttu-id="f7478-122">Gibt die ID des Auftragszeitplans an, den dieses Cmdlet aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f7478-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="f7478-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7478-123">CommonParameters</span></span>
<span data-ttu-id="f7478-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7478-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7478-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7478-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7478-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7478-126">INPUTS</span></span>

### <span data-ttu-id="f7478-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f7478-127">System.String</span></span>

### <span data-ttu-id="f7478-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f7478-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f7478-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7478-129">OUTPUTS</span></span>

### <span data-ttu-id="f7478-130">System. void</span><span class="sxs-lookup"><span data-stu-id="f7478-130">System.Void</span></span>

## <span data-ttu-id="f7478-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7478-131">NOTES</span></span>

## <span data-ttu-id="f7478-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7478-132">RELATED LINKS</span></span>

[<span data-ttu-id="f7478-133">Deaktivieren-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f7478-133">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="f7478-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f7478-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f7478-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f7478-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="f7478-136">Neu – AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f7478-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="f7478-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f7478-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="f7478-138">Stopp-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f7478-138">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="f7478-139">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="f7478-139">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


