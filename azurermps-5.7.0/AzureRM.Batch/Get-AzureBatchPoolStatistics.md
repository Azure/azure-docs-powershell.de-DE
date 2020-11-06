---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpoolstatistics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolStatistics.md
ms.openlocfilehash: e51f10fb7d1043e7a0f9addb9c874224ce952dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478766"
---
# <span data-ttu-id="d505f-101">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="d505f-101">Get-AzureBatchPoolStatistics</span></span>

## <span data-ttu-id="d505f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d505f-102">SYNOPSIS</span></span>
<span data-ttu-id="d505f-103">Ruft Pool Zusammenfassungs Statistiken für ein Stapelverarbeitungs Konto ab.</span><span class="sxs-lookup"><span data-stu-id="d505f-103">Gets pool summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d505f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d505f-104">SYNTAX</span></span>

```
Get-AzureBatchPoolStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d505f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d505f-105">DESCRIPTION</span></span>
<span data-ttu-id="d505f-106">Das Cmdlet " **Get-AzureBatchPoolStatistics** " Ruft die Lebensdauer Statistik für alle Pools im angegebenen Konto ab.</span><span class="sxs-lookup"><span data-stu-id="d505f-106">The **Get-AzureBatchPoolStatistics** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="d505f-107">Statistiken werden über alle Pools aggregiert, die je im Konto vorhanden waren, von der Kontoerstellung bis zum letzten Aktualisierungszeitpunkt der Statistik.</span><span class="sxs-lookup"><span data-stu-id="d505f-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="d505f-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d505f-108">EXAMPLES</span></span>

### <span data-ttu-id="d505f-109">Beispiel 1: Abrufen von Ressourcenstatistiken aller Pools in einem Konto</span><span class="sxs-lookup"><span data-stu-id="d505f-109">Example 1: Get resource statistics of all pools in an account</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $PoolStatistics = Get-AzureBatchPoolStatistics -BatchContext $Context
PS C:\> $PoolStatistics.ResourceStatistics 
AverageCpuPercentage : 0.351232518750755
AverageDiskGiB       : 55.2569014701165
AverageMemoryGiB     : 2.87273772318252
DiskReadGiB          : 45.1326256990433
DiskReadIOps         : 878278
DiskWriteGiB         : 1230.72120628133
DiskWriteIOps        : 176832212
LastUpdateTime       : 5/16/2016 4:30:00 PM
NetworkReadGiB       : 29.3502839952707
NetworkWriteGiB      : 25.5208827350289
PeakDiskGiB          : 21.9638671875
PeakMemoryGiB        : 1.11184692382813
StartTime            : 2/10/2016 7:07:24 PM
```

<span data-ttu-id="d505f-110">Der erste Befehl erstellt einen Objektverweis auf die Kontoschlüssel für das Batch Konto mit dem Namen ContosoBatchAccount mithilfe von **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="d505f-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="d505f-111">Der Befehl speichert diesen Objektverweis in der $Context Variablen.</span><span class="sxs-lookup"><span data-stu-id="d505f-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="d505f-112">Mit dem zweiten Befehl werden die Statistiken aller Pools des angegebenen Kontos abgerufen und dann im $PoolStatistics gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d505f-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>

<span data-ttu-id="d505f-113">Der endgültige Befehl zeigt die **ResourceStatistics** -Eigenschaft von $PoolStatistics an.</span><span class="sxs-lookup"><span data-stu-id="d505f-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="d505f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d505f-114">PARAMETERS</span></span>

### <span data-ttu-id="d505f-115">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="d505f-115">-BatchContext</span></span>
<span data-ttu-id="d505f-116">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="d505f-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d505f-117">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d505f-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d505f-118">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d505f-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d505f-119">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="d505f-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d505f-120">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="d505f-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d505f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d505f-121">-DefaultProfile</span></span>
<span data-ttu-id="d505f-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d505f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d505f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d505f-123">CommonParameters</span></span>
<span data-ttu-id="d505f-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d505f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d505f-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d505f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d505f-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d505f-126">INPUTS</span></span>

### <span data-ttu-id="d505f-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d505f-127">BatchAccountContext</span></span>
<span data-ttu-id="d505f-128">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d505f-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="d505f-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d505f-129">OUTPUTS</span></span>

### <span data-ttu-id="d505f-130">PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="d505f-130">PSPoolStatistics</span></span>

## <span data-ttu-id="d505f-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="d505f-131">NOTES</span></span>

## <span data-ttu-id="d505f-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d505f-132">RELATED LINKS</span></span>

[<span data-ttu-id="d505f-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d505f-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d505f-134">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="d505f-134">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)

[<span data-ttu-id="d505f-135">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="d505f-135">Get-AzureBatchJobStatistics</span></span>](./Get-AzureBatchJobStatistics.md)


