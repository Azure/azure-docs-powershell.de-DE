---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: c012fe266bc25752729b14192c4d9c0a42cd8961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505258"
---
# <span data-ttu-id="0fbf0-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0fbf0-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="0fbf0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0fbf0-102">SYNOPSIS</span></span>
<span data-ttu-id="0fbf0-103">Aktiviert einen Stapel Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="0fbf0-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fbf0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fbf0-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fbf0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fbf0-105">DESCRIPTION</span></span>
<span data-ttu-id="0fbf0-106">Das Cmdlet **enable-AzureBatchJobSchedule** aktiviert einen Azure-Batch Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="0fbf0-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="0fbf0-107">Nachdem Sie einen Projektplan aktiviert haben, können Aufträge entsprechend diesem Zeitplan erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0fbf0-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="0fbf0-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0fbf0-108">EXAMPLES</span></span>

### <span data-ttu-id="0fbf0-109">Beispiel 1: Aktivieren eines Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="0fbf0-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="0fbf0-110">Dieser Befehl aktiviert den Auftragszeitplan mit der ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="0fbf0-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="0fbf0-111">Verwenden Sie das Cmdlet **Get-AzureRmBatchAccountKeys** , um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="0fbf0-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="0fbf0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fbf0-112">PARAMETERS</span></span>

### <span data-ttu-id="0fbf0-113">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="0fbf0-113">-BatchContext</span></span>
<span data-ttu-id="0fbf0-114">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="0fbf0-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0fbf0-115">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fbf0-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="0fbf0-116">-ID</span><span class="sxs-lookup"><span data-stu-id="0fbf0-116">-Id</span></span>
<span data-ttu-id="0fbf0-117">Gibt die ID des Auftragszeitplans an, den dieses Cmdlet aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0fbf0-117">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="0fbf0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fbf0-118">-DefaultProfile</span></span>
<span data-ttu-id="0fbf0-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0fbf0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fbf0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fbf0-120">CommonParameters</span></span>
<span data-ttu-id="0fbf0-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fbf0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fbf0-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fbf0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fbf0-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0fbf0-123">INPUTS</span></span>

### <span data-ttu-id="0fbf0-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0fbf0-124">BatchAccountContext</span></span>
<span data-ttu-id="0fbf0-125">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0fbf0-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="0fbf0-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0fbf0-126">String</span></span>
<span data-ttu-id="0fbf0-127">Der Parameter "ID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0fbf0-127">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="0fbf0-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0fbf0-128">OUTPUTS</span></span>

## <span data-ttu-id="0fbf0-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="0fbf0-129">NOTES</span></span>

## <span data-ttu-id="0fbf0-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0fbf0-130">RELATED LINKS</span></span>

[<span data-ttu-id="0fbf0-131">Deaktivieren-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0fbf0-131">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="0fbf0-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0fbf0-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="0fbf0-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0fbf0-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="0fbf0-134">Neu – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0fbf0-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="0fbf0-135">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0fbf0-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="0fbf0-136">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0fbf0-136">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="0fbf0-137">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0fbf0-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


