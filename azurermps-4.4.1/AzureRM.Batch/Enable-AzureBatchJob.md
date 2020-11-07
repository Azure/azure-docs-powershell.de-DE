---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: 665d7b64f3e8d83dd45ebc8de0cc36da960f8c35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665111"
---
# <span data-ttu-id="eebc1-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="eebc1-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="eebc1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eebc1-102">SYNOPSIS</span></span>
<span data-ttu-id="eebc1-103">Aktiviert eine Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="eebc1-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eebc1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eebc1-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eebc1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eebc1-105">DESCRIPTION</span></span>
<span data-ttu-id="eebc1-106">Das Cmdlet **enable-AzureBatchJob** aktiviert eine Azure-Batch Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="eebc1-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="eebc1-107">Nachdem Sie einen Auftrag aktiviert haben, können neue Aufgaben ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="eebc1-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="eebc1-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eebc1-108">EXAMPLES</span></span>

### <span data-ttu-id="eebc1-109">Beispiel 1: Aktivieren eines stapelverarbeitungsauftrags</span><span class="sxs-lookup"><span data-stu-id="eebc1-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="eebc1-110">Mit diesem Befehl können Sie den Auftrag mit der ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="eebc1-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="eebc1-111">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="eebc1-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="eebc1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="eebc1-112">PARAMETERS</span></span>

### <span data-ttu-id="eebc1-113">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="eebc1-113">-BatchContext</span></span>
<span data-ttu-id="eebc1-114">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="eebc1-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="eebc1-115">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eebc1-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="eebc1-116">-ID</span><span class="sxs-lookup"><span data-stu-id="eebc1-116">-Id</span></span>
<span data-ttu-id="eebc1-117">Gibt die ID des Auftrags an, den dieses Cmdlet aktiviert.</span><span class="sxs-lookup"><span data-stu-id="eebc1-117">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="eebc1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eebc1-118">-DefaultProfile</span></span>
<span data-ttu-id="eebc1-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eebc1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eebc1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eebc1-120">CommonParameters</span></span>
<span data-ttu-id="eebc1-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eebc1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eebc1-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eebc1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eebc1-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eebc1-123">INPUTS</span></span>

### <span data-ttu-id="eebc1-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="eebc1-124">BatchAccountContext</span></span>
<span data-ttu-id="eebc1-125">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="eebc1-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="eebc1-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eebc1-126">String</span></span>
<span data-ttu-id="eebc1-127">Der Parameter "ID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="eebc1-127">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="eebc1-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eebc1-128">OUTPUTS</span></span>

## <span data-ttu-id="eebc1-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="eebc1-129">NOTES</span></span>

## <span data-ttu-id="eebc1-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eebc1-130">RELATED LINKS</span></span>

[<span data-ttu-id="eebc1-131">Deaktivieren-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="eebc1-131">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="eebc1-132">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="eebc1-132">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="eebc1-133">Neu – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="eebc1-133">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="eebc1-134">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="eebc1-134">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="eebc1-135">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="eebc1-135">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="eebc1-136">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="eebc1-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


