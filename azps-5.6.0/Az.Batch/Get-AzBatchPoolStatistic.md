---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchpoolstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
ms.openlocfilehash: 48a01d04609bfcb3d0bf70c7e454316ee3095dcc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919040"
---
# <span data-ttu-id="b5166-101">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="b5166-101">Get-AzBatchPoolStatistic</span></span>

## <span data-ttu-id="b5166-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5166-102">SYNOPSIS</span></span>
<span data-ttu-id="b5166-103">Ruft Poolzusammenfassungsstatistiken für ein Batchkonto ab.</span><span class="sxs-lookup"><span data-stu-id="b5166-103">Gets pool summary statistics for a Batch account.</span></span>

## <span data-ttu-id="b5166-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5166-104">SYNTAX</span></span>

```
Get-AzBatchPoolStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5166-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5166-105">DESCRIPTION</span></span>
<span data-ttu-id="b5166-106">Das **Get-AzBatchPoolStatistic-Cmdlet** ruft die Lebensdauerstatistiken für alle Pools im angegebenen Konto ab.</span><span class="sxs-lookup"><span data-stu-id="b5166-106">The **Get-AzBatchPoolStatistic** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="b5166-107">Statistiken werden über alle Pools aggregiert, die jemals im Konto vorhanden waren, von der Kontoerstellung bis zur letzten Aktualisierungszeit der Statistik.</span><span class="sxs-lookup"><span data-stu-id="b5166-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="b5166-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b5166-108">EXAMPLES</span></span>

### <span data-ttu-id="b5166-109">Beispiel 1: Erhalten von Ressourcenstatistiken aller Pools in einem Konto</span><span class="sxs-lookup"><span data-stu-id="b5166-109">Example 1: Get resource statistics of all pools in an account</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
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

<span data-ttu-id="b5166-110">Mit dem ersten Befehl wird mithilfe von **Get-AzBatchAccountKey** ein Objektverweis auf die Kontoschlüssel für das Batchkonto namens ContosoBatchAccount erstellt.</span><span class="sxs-lookup"><span data-stu-id="b5166-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="b5166-111">Der Befehl speichert diesen Objektverweis in der $Context-Variable.</span><span class="sxs-lookup"><span data-stu-id="b5166-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="b5166-112">Der zweite Befehl ruft die Statistiken aller Pools im angegebenen Konto ab und speichert sie dann im $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="b5166-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>
<span data-ttu-id="b5166-113">Der letzte Befehl zeigt die **ResourceStatistics-Eigenschaft** der $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="b5166-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="b5166-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b5166-114">PARAMETERS</span></span>

### <span data-ttu-id="b5166-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b5166-115">-BatchContext</span></span>
<span data-ttu-id="b5166-116">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b5166-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b5166-117">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="b5166-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b5166-118">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b5166-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b5166-119">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="b5166-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b5166-120">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="b5166-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b5166-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5166-121">-DefaultProfile</span></span>
<span data-ttu-id="b5166-122">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b5166-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5166-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5166-123">CommonParameters</span></span>
<span data-ttu-id="b5166-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5166-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5166-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5166-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5166-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b5166-126">INPUTS</span></span>

### <span data-ttu-id="b5166-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b5166-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b5166-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b5166-128">OUTPUTS</span></span>

### <span data-ttu-id="b5166-129">Microsoft.Azure.Commands.Batch. Models.PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="b5166-129">Microsoft.Azure.Commands.Batch.Models.PSPoolStatistics</span></span>

## <span data-ttu-id="b5166-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b5166-130">NOTES</span></span>

## <span data-ttu-id="b5166-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b5166-131">RELATED LINKS</span></span>

[<span data-ttu-id="b5166-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b5166-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b5166-133">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="b5166-133">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)

[<span data-ttu-id="b5166-134">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="b5166-134">Get-AzBatchJobStatistic</span></span>](./Get-AzBatchJobStatistic.md)
