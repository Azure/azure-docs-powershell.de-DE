---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 5e26bd47c9c53b88442505aeb66d81a96c137b1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476230"
---
# <span data-ttu-id="e2c7a-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e2c7a-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="e2c7a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e2c7a-102">SYNOPSIS</span></span>
<span data-ttu-id="e2c7a-103">Legt einen Auftragszeitplan fest.</span><span class="sxs-lookup"><span data-stu-id="e2c7a-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2c7a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2c7a-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2c7a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2c7a-105">DESCRIPTION</span></span>
<span data-ttu-id="e2c7a-106">Das Cmdlet " **Set-AzureBatchJobSchedule** " legt einen Auftragszeitplan im Azure-Batch Dienst fest.</span><span class="sxs-lookup"><span data-stu-id="e2c7a-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="e2c7a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e2c7a-107">EXAMPLES</span></span>

## <span data-ttu-id="e2c7a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2c7a-108">PARAMETERS</span></span>

### <span data-ttu-id="e2c7a-109">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="e2c7a-109">-BatchContext</span></span>
<span data-ttu-id="e2c7a-110">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="e2c7a-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e2c7a-111">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="e2c7a-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e2c7a-112">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e2c7a-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e2c7a-113">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="e2c7a-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e2c7a-114">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="e2c7a-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e2c7a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2c7a-115">-DefaultProfile</span></span>
<span data-ttu-id="e2c7a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e2c7a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2c7a-117">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="e2c7a-117">-JobSchedule</span></span>
<span data-ttu-id="e2c7a-118">Gibt ein **PSCloudJobSchedule** -Objekt an, das einen Auftragszeitplan darstellt.</span><span class="sxs-lookup"><span data-stu-id="e2c7a-118">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="e2c7a-119">Verwenden Sie das Get-AzureBatchJobSchedule-Cmdlet, um ein **PSCloudJobSchedule** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e2c7a-119">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2c7a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2c7a-120">CommonParameters</span></span>
<span data-ttu-id="e2c7a-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2c7a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2c7a-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2c7a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2c7a-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e2c7a-123">INPUTS</span></span>

### <span data-ttu-id="e2c7a-124">Microsoft.Azure.Commands.Batch. Models. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e2c7a-124">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>
<span data-ttu-id="e2c7a-125">Parameter: JobSchedule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e2c7a-125">Parameters: JobSchedule (ByValue)</span></span>

### <span data-ttu-id="e2c7a-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e2c7a-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="e2c7a-127">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e2c7a-127">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="e2c7a-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e2c7a-128">OUTPUTS</span></span>

### <span data-ttu-id="e2c7a-129">System. void</span><span class="sxs-lookup"><span data-stu-id="e2c7a-129">System.Void</span></span>

## <span data-ttu-id="e2c7a-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="e2c7a-130">NOTES</span></span>

## <span data-ttu-id="e2c7a-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e2c7a-131">RELATED LINKS</span></span>

[<span data-ttu-id="e2c7a-132">Deaktivieren-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e2c7a-132">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="e2c7a-133">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e2c7a-133">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="e2c7a-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e2c7a-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="e2c7a-135">Neu – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e2c7a-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="e2c7a-136">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e2c7a-136">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="e2c7a-137">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e2c7a-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


