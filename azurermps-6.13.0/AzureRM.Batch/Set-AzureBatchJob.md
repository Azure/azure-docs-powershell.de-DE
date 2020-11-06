---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: 3baaa7296ab0fdd2c1dcab606b2896b11e5773f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477937"
---
# <span data-ttu-id="57588-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="57588-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="57588-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="57588-102">SYNOPSIS</span></span>
<span data-ttu-id="57588-103">Aktualisiert eine Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="57588-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57588-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="57588-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57588-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57588-105">DESCRIPTION</span></span>
<span data-ttu-id="57588-106">Das Cmdlet " **Satz-AzureBatchJob** " aktualisiert eine Azure-Batch Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="57588-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="57588-107">Verwenden Sie das Get-AzureBatchJob-Cmdlet, um ein **PSCloudJob** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="57588-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="57588-108">Ändern Sie die Eigenschaften des Objekts, und verwenden Sie dann das aktuelle Cmdlet, um Ihre Änderungen an den Stapelverarbeitungs Dienst zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="57588-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="57588-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57588-109">EXAMPLES</span></span>

### <span data-ttu-id="57588-110">Beispiel 1: Aktualisieren eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="57588-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="57588-111">Der erste Befehl ruft einen Pool mithilfe von **Get-AzureBatchJob** ab und speichert ihn dann in der $Job-Variablen.</span><span class="sxs-lookup"><span data-stu-id="57588-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>
<span data-ttu-id="57588-112">Der zweite Befehl ändert die Priority-Spezifikation für das $Job-Objekt.</span><span class="sxs-lookup"><span data-stu-id="57588-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="57588-113">Der endgültige Befehl aktualisiert den Batch Dienst so, dass er dem lokalen Objekt in $Job entspricht.</span><span class="sxs-lookup"><span data-stu-id="57588-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="57588-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="57588-114">PARAMETERS</span></span>

### <span data-ttu-id="57588-115">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="57588-115">-BatchContext</span></span>
<span data-ttu-id="57588-116">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="57588-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="57588-117">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="57588-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="57588-118">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="57588-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="57588-119">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="57588-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="57588-120">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="57588-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="57588-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57588-121">-DefaultProfile</span></span>
<span data-ttu-id="57588-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="57588-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57588-123">-Job</span><span class="sxs-lookup"><span data-stu-id="57588-123">-Job</span></span>
<span data-ttu-id="57588-124">Gibt einen **PSCloudJob** an, mit dem dieses Cmdlet den Stapelverarbeitungs Dienst aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="57588-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57588-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57588-125">CommonParameters</span></span>
<span data-ttu-id="57588-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57588-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57588-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57588-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57588-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="57588-128">INPUTS</span></span>

### <span data-ttu-id="57588-129">Microsoft.Azure.Commands.Batch. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="57588-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>
<span data-ttu-id="57588-130">Parameter: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="57588-130">Parameters: Job (ByValue)</span></span>

### <span data-ttu-id="57588-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="57588-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="57588-132">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="57588-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="57588-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57588-133">OUTPUTS</span></span>

### <span data-ttu-id="57588-134">System. void</span><span class="sxs-lookup"><span data-stu-id="57588-134">System.Void</span></span>

## <span data-ttu-id="57588-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="57588-135">NOTES</span></span>

## <span data-ttu-id="57588-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="57588-136">RELATED LINKS</span></span>

[<span data-ttu-id="57588-137">Deaktivieren-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="57588-137">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="57588-138">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="57588-138">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="57588-139">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="57588-139">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="57588-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="57588-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="57588-141">Neu – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="57588-141">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="57588-142">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="57588-142">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="57588-143">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="57588-143">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="57588-144">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="57588-144">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


