---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
ms.openlocfilehash: 73d80d3547ea895e5cbd35b2d514d9a757164bed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505266"
---
# <span data-ttu-id="43b81-101">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="43b81-101">Disable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="43b81-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43b81-102">SYNOPSIS</span></span>
<span data-ttu-id="43b81-103">Deaktiviert einen stapelverarbeitungsauftrags Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="43b81-103">Disables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43b81-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43b81-104">SYNTAX</span></span>

```
Disable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43b81-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43b81-105">DESCRIPTION</span></span>
<span data-ttu-id="43b81-106">Das Cmdlet **Disable-AzureBatchJobSchedule** deaktiviert einen Azure-Batch Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="43b81-106">The **Disable-AzureBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="43b81-107">Wenn Sie einen Terminplan deaktivieren, werden keine Aufträge entsprechend diesem Zeitplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="43b81-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="43b81-108">Sie können einen deaktivierten Zeitplan später aktivieren.</span><span class="sxs-lookup"><span data-stu-id="43b81-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="43b81-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43b81-109">EXAMPLES</span></span>

### <span data-ttu-id="43b81-110">Beispiel 1: Deaktivieren eines Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="43b81-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="43b81-111">Dieser Befehl deaktiviert den Auftragszeitplan mit der ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="43b81-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="43b81-112">Verwenden Sie das Cmdlet **Get-AzureRmBatchAccountKeys** , um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="43b81-112">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="43b81-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="43b81-113">PARAMETERS</span></span>

### <span data-ttu-id="43b81-114">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="43b81-114">-BatchContext</span></span>
<span data-ttu-id="43b81-115">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="43b81-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="43b81-116">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43b81-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="43b81-117">-ID</span><span class="sxs-lookup"><span data-stu-id="43b81-117">-Id</span></span>
<span data-ttu-id="43b81-118">Gibt die ID des Auftragszeitplans an, der vom Cmdlet deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="43b81-118">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="43b81-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43b81-119">-DefaultProfile</span></span>
<span data-ttu-id="43b81-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43b81-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43b81-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43b81-121">CommonParameters</span></span>
<span data-ttu-id="43b81-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43b81-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43b81-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43b81-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43b81-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43b81-124">INPUTS</span></span>

### <span data-ttu-id="43b81-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="43b81-125">BatchAccountContext</span></span>
<span data-ttu-id="43b81-126">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="43b81-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="43b81-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="43b81-127">String</span></span>
<span data-ttu-id="43b81-128">Der Parameter "ID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="43b81-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="43b81-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43b81-129">OUTPUTS</span></span>

## <span data-ttu-id="43b81-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="43b81-130">NOTES</span></span>

## <span data-ttu-id="43b81-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43b81-131">RELATED LINKS</span></span>

[<span data-ttu-id="43b81-132">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="43b81-132">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="43b81-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="43b81-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="43b81-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="43b81-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="43b81-135">Neu – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="43b81-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="43b81-136">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="43b81-136">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="43b81-137">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="43b81-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="43b81-138">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="43b81-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


