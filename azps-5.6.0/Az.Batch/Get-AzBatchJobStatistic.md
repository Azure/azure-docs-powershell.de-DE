---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchjobstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
ms.openlocfilehash: ec52f8b48433e52e86551a8346f4ec9a61b5727d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936315"
---
# <span data-ttu-id="5f896-101">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="5f896-101">Get-AzBatchJobStatistic</span></span>

## <span data-ttu-id="5f896-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f896-102">SYNOPSIS</span></span>
<span data-ttu-id="5f896-103">Ruft Auftragszusammenfassungsstatistiken für ein Batchkonto ab.</span><span class="sxs-lookup"><span data-stu-id="5f896-103">Gets job summary statistics for a Batch account.</span></span>

## <span data-ttu-id="5f896-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f896-104">SYNTAX</span></span>

```
Get-AzBatchJobStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f896-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f896-105">DESCRIPTION</span></span>
<span data-ttu-id="5f896-106">Das **Get-AzBatchJobStatistic-Cmdlet** ruft zusammenfassungsstatistiken für alle Aufträge in einem Azure Batch-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="5f896-106">The **Get-AzBatchJobStatistic** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="5f896-107">Statistiken werden für alle Aufträge aggregiert, die jemals im Konto vorhanden waren, von der Kontoerstellung bis zur letzten Aktualisierungszeit der Statistik.</span><span class="sxs-lookup"><span data-stu-id="5f896-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="5f896-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5f896-108">EXAMPLES</span></span>

### <span data-ttu-id="5f896-109">Beispiel 1: Zusammenfassungsstatistiken für alle Aufträge</span><span class="sxs-lookup"><span data-stu-id="5f896-109">Example 1: Get summary statistics for all jobs</span></span>
```
PS C:\>Get-AzBatchJobStatistic -BatchContext $Context
FailedTaskCount    : 330
KernelCpuTime      : 00:24:31.8440000
LastUpdateTime     : 5/16/2016 6:00:00 PM
ReadIOGiB          : 38.1271341182292
ReadIOps           : 26546054
StartTime          : 11/3/2015 9:47:14 PM
SucceededTaskCount : 766
TaskRetryCount     : 0
Url                : https://accountname.westus.batch.azure.com/lifetimejobstats
UserCpuTime        : 20:55:50.3200000
WaitTime           : 03:54:49.8530000
WallClockTime      : 20:55:50.3200000
WriteIOGiB         : 0.159623090177774
WriteIOps          : 146946
```

<span data-ttu-id="5f896-110">Mit dem ersten Befehl wird mithilfe von **Get-AzBatchAccountKey** ein Objektverweis auf die Kontoschlüssel für das Batchkonto namens ContosoBatchAccount erstellt.</span><span class="sxs-lookup"><span data-stu-id="5f896-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="5f896-111">Der Befehl speichert diesen Objektverweis in der $Context-Variable.</span><span class="sxs-lookup"><span data-stu-id="5f896-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="5f896-112">Der zweite Befehl ruft die Zusammenfassungsstatistik für alle Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="5f896-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="5f896-113">Der Befehl verwendet den $Context des ersten Befehls.</span><span class="sxs-lookup"><span data-stu-id="5f896-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="5f896-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5f896-114">PARAMETERS</span></span>

### <span data-ttu-id="5f896-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5f896-115">-BatchContext</span></span>
<span data-ttu-id="5f896-116">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5f896-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5f896-117">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f896-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5f896-118">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5f896-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5f896-119">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f896-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5f896-120">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="5f896-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5f896-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f896-121">-DefaultProfile</span></span>
<span data-ttu-id="5f896-122">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f896-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f896-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f896-123">CommonParameters</span></span>
<span data-ttu-id="5f896-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f896-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f896-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f896-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f896-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5f896-126">INPUTS</span></span>

### <span data-ttu-id="5f896-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5f896-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5f896-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5f896-128">OUTPUTS</span></span>

### <span data-ttu-id="5f896-129">Microsoft.Azure.Commands.Batch. Models.PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="5f896-129">Microsoft.Azure.Commands.Batch.Models.PSJobStatistics</span></span>

## <span data-ttu-id="5f896-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5f896-130">NOTES</span></span>

## <span data-ttu-id="5f896-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5f896-131">RELATED LINKS</span></span>

[<span data-ttu-id="5f896-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5f896-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5f896-133">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="5f896-133">Get-AzBatchPoolStatistic</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="5f896-134">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="5f896-134">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)
