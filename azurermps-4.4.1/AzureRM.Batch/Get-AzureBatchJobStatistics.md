---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
ms.openlocfilehash: 03b7e3999fbc482223365b59867c02c75e9d5ba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497133"
---
# <span data-ttu-id="ad85d-101">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="ad85d-101">Get-AzureBatchJobStatistics</span></span>

## <span data-ttu-id="ad85d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad85d-102">SYNOPSIS</span></span>
<span data-ttu-id="ad85d-103">Ruft Auftrags Zusammenfassungs Statistiken für ein Stapelverarbeitungs Konto ab.</span><span class="sxs-lookup"><span data-stu-id="ad85d-103">Gets job summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad85d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad85d-104">SYNTAX</span></span>

```
Get-AzureBatchJobStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad85d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad85d-105">DESCRIPTION</span></span>
<span data-ttu-id="ad85d-106">Das Cmdlet " **Get-AzureBatchJobStatistics** " ruft Lebensdauer Zusammenfassungs Statistiken für alle Aufträge in einem Azure-Batch Konto ab.</span><span class="sxs-lookup"><span data-stu-id="ad85d-106">The **Get-AzureBatchJobStatistics** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="ad85d-107">Statistiken werden für alle Aufträge aggregiert, die je im Konto vorhanden waren, von der Kontoerstellung bis zur letzten Aktualisierungszeit der Statistik.</span><span class="sxs-lookup"><span data-stu-id="ad85d-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="ad85d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad85d-108">EXAMPLES</span></span>

### <span data-ttu-id="ad85d-109">Beispiel 1: Abrufen von Zusammenfassungs Statistiken für alle Aufträge</span><span class="sxs-lookup"><span data-stu-id="ad85d-109">Example 1: Get summary statistics for all jobs</span></span>
```
PS C:\>Get-AzureBatchJobStatistics -BatchContext $Context
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

<span data-ttu-id="ad85d-110">Der erste Befehl erstellt einen Objektverweis auf die Kontoschlüssel für das Batch Konto mit dem Namen ContosoBatchAccount mithilfe von **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="ad85d-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="ad85d-111">Der Befehl speichert diesen Objektverweis in der $Context Variablen.</span><span class="sxs-lookup"><span data-stu-id="ad85d-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="ad85d-112">Der zweite Befehl ruft die Zusammenfassungs Statistiken für alle Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="ad85d-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="ad85d-113">Der Befehl verwendet den $context-Wert aus dem ersten Befehl.</span><span class="sxs-lookup"><span data-stu-id="ad85d-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="ad85d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad85d-114">PARAMETERS</span></span>

### <span data-ttu-id="ad85d-115">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="ad85d-115">-BatchContext</span></span>
<span data-ttu-id="ad85d-116">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad85d-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ad85d-117">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad85d-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="ad85d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad85d-118">-DefaultProfile</span></span>
<span data-ttu-id="ad85d-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ad85d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad85d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad85d-120">CommonParameters</span></span>
<span data-ttu-id="ad85d-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad85d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad85d-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad85d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad85d-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad85d-123">INPUTS</span></span>

### <span data-ttu-id="ad85d-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ad85d-124">BatchAccountContext</span></span>
<span data-ttu-id="ad85d-125">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ad85d-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="ad85d-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad85d-126">OUTPUTS</span></span>

### <span data-ttu-id="ad85d-127">PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="ad85d-127">PSJobStatistics</span></span>

## <span data-ttu-id="ad85d-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad85d-128">NOTES</span></span>

## <span data-ttu-id="ad85d-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad85d-129">RELATED LINKS</span></span>

[<span data-ttu-id="ad85d-130">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ad85d-130">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ad85d-131">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="ad85d-131">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="ad85d-132">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="ad85d-132">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)


