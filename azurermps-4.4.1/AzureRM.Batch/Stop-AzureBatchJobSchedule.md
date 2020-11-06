---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 58ac726d722959e3ee32bce84c0abe3c771fcbcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500102"
---
# <span data-ttu-id="c8b12-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c8b12-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="c8b12-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c8b12-102">SYNOPSIS</span></span>
<span data-ttu-id="c8b12-103">Beendet einen stapelverarbeitungsauftrags Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="c8b12-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8b12-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8b12-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8b12-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8b12-105">DESCRIPTION</span></span>
<span data-ttu-id="c8b12-106">Das Cmdlet **Stop-AzureBatchJobSchedule** beendet einen Azure-Batch Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="c8b12-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="c8b12-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8b12-107">EXAMPLES</span></span>

### <span data-ttu-id="c8b12-108">Beispiel 1: Beenden eines Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="c8b12-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="c8b12-109">Dieser Befehl beendet den Auftragszeitplan mit der ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="c8b12-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="c8b12-110">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="c8b12-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="c8b12-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b12-111">PARAMETERS</span></span>

### <span data-ttu-id="c8b12-112">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="c8b12-112">-BatchContext</span></span>
<span data-ttu-id="c8b12-113">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="c8b12-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c8b12-114">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8b12-114">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="c8b12-115">-ID</span><span class="sxs-lookup"><span data-stu-id="c8b12-115">-Id</span></span>
<span data-ttu-id="c8b12-116">Gibt die ID des Auftragszeitplans an, der vom Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="c8b12-116">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="c8b12-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8b12-117">-DefaultProfile</span></span>
<span data-ttu-id="c8b12-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c8b12-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8b12-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8b12-119">CommonParameters</span></span>
<span data-ttu-id="c8b12-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8b12-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8b12-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8b12-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8b12-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c8b12-122">INPUTS</span></span>

### <span data-ttu-id="c8b12-123">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c8b12-123">BatchAccountContext</span></span>
<span data-ttu-id="c8b12-124">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c8b12-124">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="c8b12-125">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c8b12-125">String</span></span>
<span data-ttu-id="c8b12-126">Der Parameter "ID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c8b12-126">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="c8b12-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c8b12-127">OUTPUTS</span></span>

## <span data-ttu-id="c8b12-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="c8b12-128">NOTES</span></span>

## <span data-ttu-id="c8b12-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c8b12-129">RELATED LINKS</span></span>

[<span data-ttu-id="c8b12-130">Deaktivieren-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c8b12-130">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="c8b12-131">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c8b12-131">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="c8b12-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c8b12-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c8b12-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c8b12-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="c8b12-134">Neu – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c8b12-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="c8b12-135">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c8b12-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="c8b12-136">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="c8b12-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


