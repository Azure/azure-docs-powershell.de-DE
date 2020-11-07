---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 0f9d20cdd1d2acabbd644fda91f5f8d22ff1ccd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665106"
---
# <span data-ttu-id="2d4f7-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2d4f7-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="2d4f7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d4f7-102">SYNOPSIS</span></span>
<span data-ttu-id="2d4f7-103">Legt einen Auftragszeitplan fest.</span><span class="sxs-lookup"><span data-stu-id="2d4f7-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d4f7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d4f7-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d4f7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d4f7-105">DESCRIPTION</span></span>
<span data-ttu-id="2d4f7-106">Das Cmdlet " **Set-AzureBatchJobSchedule** " legt einen Auftragszeitplan im Azure-Batch Dienst fest.</span><span class="sxs-lookup"><span data-stu-id="2d4f7-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="2d4f7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d4f7-107">EXAMPLES</span></span>

## <span data-ttu-id="2d4f7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d4f7-108">PARAMETERS</span></span>

### <span data-ttu-id="2d4f7-109">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="2d4f7-109">-BatchContext</span></span>
<span data-ttu-id="2d4f7-110">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d4f7-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2d4f7-111">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d4f7-111">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="2d4f7-112">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="2d4f7-112">-JobSchedule</span></span>
<span data-ttu-id="2d4f7-113">Gibt ein **PSCloudJobSchedule** -Objekt an, das einen Auftragszeitplan darstellt.</span><span class="sxs-lookup"><span data-stu-id="2d4f7-113">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="2d4f7-114">Verwenden Sie das Get-AzureBatchJobSchedule-Cmdlet, um ein **PSCloudJobSchedule** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2d4f7-114">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="2d4f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d4f7-115">-DefaultProfile</span></span>
<span data-ttu-id="2d4f7-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2d4f7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d4f7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d4f7-117">CommonParameters</span></span>
<span data-ttu-id="2d4f7-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d4f7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d4f7-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d4f7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d4f7-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d4f7-120">INPUTS</span></span>

### <span data-ttu-id="2d4f7-121">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2d4f7-121">BatchAccountContext</span></span>
<span data-ttu-id="2d4f7-122">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2d4f7-122">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="2d4f7-123">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2d4f7-123">PSCloudJobSchedule</span></span>
<span data-ttu-id="2d4f7-124">Der Parameter "JobSchedule" akzeptiert den Wert vom Typ "PSCloudJobSchedule" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2d4f7-124">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="2d4f7-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d4f7-125">OUTPUTS</span></span>

## <span data-ttu-id="2d4f7-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d4f7-126">NOTES</span></span>

## <span data-ttu-id="2d4f7-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d4f7-127">RELATED LINKS</span></span>

[<span data-ttu-id="2d4f7-128">Deaktivieren-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2d4f7-128">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="2d4f7-129">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2d4f7-129">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="2d4f7-130">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2d4f7-130">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="2d4f7-131">Neu – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2d4f7-131">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="2d4f7-132">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2d4f7-132">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="2d4f7-133">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2d4f7-133">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


