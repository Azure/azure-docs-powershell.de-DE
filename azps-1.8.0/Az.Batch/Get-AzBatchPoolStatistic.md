---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
ms.openlocfilehash: d75efbd2ef369444fb655d1a011d7a1dbfab9100
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93662082"
---
# <span data-ttu-id="049d6-101">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="049d6-101">Get-AzBatchPoolStatistic</span></span>

## <span data-ttu-id="049d6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="049d6-102">SYNOPSIS</span></span>
<span data-ttu-id="049d6-103">Ruft Pool Zusammenfassungs Statistiken für ein Stapelverarbeitungs Konto ab.</span><span class="sxs-lookup"><span data-stu-id="049d6-103">Gets pool summary statistics for a Batch account.</span></span>

## <span data-ttu-id="049d6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="049d6-104">SYNTAX</span></span>

```
Get-AzBatchPoolStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="049d6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="049d6-105">DESCRIPTION</span></span>
<span data-ttu-id="049d6-106">Das Cmdlet " **Get-AzBatchPoolStatistic** " Ruft die Lebensdauer Statistik für alle Pools im angegebenen Konto ab.</span><span class="sxs-lookup"><span data-stu-id="049d6-106">The **Get-AzBatchPoolStatistic** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="049d6-107">Statistiken werden über alle Pools aggregiert, die je im Konto vorhanden waren, von der Kontoerstellung bis zum letzten Aktualisierungszeitpunkt der Statistik.</span><span class="sxs-lookup"><span data-stu-id="049d6-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="049d6-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="049d6-108">EXAMPLES</span></span>

### <span data-ttu-id="049d6-109">Beispiel 1: Abrufen von Ressourcenstatistiken aller Pools in einem Konto</span><span class="sxs-lookup"><span data-stu-id="049d6-109">Example 1: Get resource statistics of all pools in an account</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $PoolStatistics = Get-AzBatchPoolStatistic -BatchContext $Context
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

<span data-ttu-id="049d6-110">Der erste Befehl erstellt einen Objektverweis auf die Kontoschlüssel für das Batch Konto mit dem Namen ContosoBatchAccount mithilfe von **Get-AzBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="049d6-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="049d6-111">Der Befehl speichert diesen Objektverweis in der $Context Variablen.</span><span class="sxs-lookup"><span data-stu-id="049d6-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="049d6-112">Mit dem zweiten Befehl werden die Statistiken aller Pools des angegebenen Kontos abgerufen und dann im $PoolStatistics gespeichert.</span><span class="sxs-lookup"><span data-stu-id="049d6-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>
<span data-ttu-id="049d6-113">Der endgültige Befehl zeigt die **ResourceStatistics** -Eigenschaft von $PoolStatistics an.</span><span class="sxs-lookup"><span data-stu-id="049d6-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="049d6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="049d6-114">PARAMETERS</span></span>

### <span data-ttu-id="049d6-115">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="049d6-115">-BatchContext</span></span>
<span data-ttu-id="049d6-116">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="049d6-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="049d6-117">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="049d6-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="049d6-118">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="049d6-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="049d6-119">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="049d6-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="049d6-120">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="049d6-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="049d6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="049d6-121">-DefaultProfile</span></span>
<span data-ttu-id="049d6-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="049d6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="049d6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="049d6-123">CommonParameters</span></span>
<span data-ttu-id="049d6-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="049d6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="049d6-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="049d6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="049d6-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="049d6-126">INPUTS</span></span>

### <span data-ttu-id="049d6-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="049d6-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="049d6-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="049d6-128">OUTPUTS</span></span>

### <span data-ttu-id="049d6-129">Microsoft.Azure.Commands.Batch. Models. PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="049d6-129">Microsoft.Azure.Commands.Batch.Models.PSPoolStatistics</span></span>

## <span data-ttu-id="049d6-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="049d6-130">NOTES</span></span>

## <span data-ttu-id="049d6-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="049d6-131">RELATED LINKS</span></span>

[<span data-ttu-id="049d6-132">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="049d6-132">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="049d6-133">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="049d6-133">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)

[<span data-ttu-id="049d6-134">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="049d6-134">Get-AzBatchJobStatistic</span></span>](./Get-AzBatchJobStatistic.md)


