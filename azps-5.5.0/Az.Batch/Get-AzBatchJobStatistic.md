---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
ms.openlocfilehash: 11532648242438983ae1bc9222dbc3ac12fa05e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171534"
---
# <span data-ttu-id="c99af-101">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="c99af-101">Get-AzBatchJobStatistic</span></span>

## <span data-ttu-id="c99af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c99af-102">SYNOPSIS</span></span>
<span data-ttu-id="c99af-103">Ruft Auftragszusammenfassungsstatistiken für ein Batchkonto ab.</span><span class="sxs-lookup"><span data-stu-id="c99af-103">Gets job summary statistics for a Batch account.</span></span>

## <span data-ttu-id="c99af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c99af-104">SYNTAX</span></span>

```
Get-AzBatchJobStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c99af-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c99af-105">DESCRIPTION</span></span>
<span data-ttu-id="c99af-106">Das **Cmdlet "Get-AzBatchJobStatistic"** ruft Zusammenfassungsstatistiken zur Lebensdauer für alle Aufträge in einem Azure -Batchkonto ab.</span><span class="sxs-lookup"><span data-stu-id="c99af-106">The **Get-AzBatchJobStatistic** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="c99af-107">Statistiken werden für alle Aufträge aggregiert, die jemals im Konto vorhanden waren, von der Kontoerstellung bis zur letzten Aktualisierungszeit der Statistiken.</span><span class="sxs-lookup"><span data-stu-id="c99af-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="c99af-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c99af-108">EXAMPLES</span></span>

### <span data-ttu-id="c99af-109">Beispiel 1: Erhalten von Zusammenfassungsstatistiken für alle Aufträge</span><span class="sxs-lookup"><span data-stu-id="c99af-109">Example 1: Get summary statistics for all jobs</span></span>
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

<span data-ttu-id="c99af-110">Der erste Befehl erstellt mithilfe von **"Get-AzBatchAccountKey"** einen Objektverweis auf die Kontoschlüssel für das Batchkonto namens "ContosoBatchAccount".</span><span class="sxs-lookup"><span data-stu-id="c99af-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="c99af-111">Der Befehl speichert diesen Objektverweis in der $Context Variable.</span><span class="sxs-lookup"><span data-stu-id="c99af-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="c99af-112">Der zweite Befehl ruft die Zusammenfassungsstatistiken für alle Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="c99af-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="c99af-113">Der Befehl verwendet den $Context wert aus dem ersten Befehl.</span><span class="sxs-lookup"><span data-stu-id="c99af-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="c99af-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c99af-114">PARAMETERS</span></span>

### <span data-ttu-id="c99af-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c99af-115">-BatchContext</span></span>
<span data-ttu-id="c99af-116">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c99af-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c99af-117">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="c99af-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c99af-118">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c99af-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c99af-119">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="c99af-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c99af-120">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c99af-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c99af-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c99af-121">-DefaultProfile</span></span>
<span data-ttu-id="c99af-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c99af-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c99af-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c99af-123">CommonParameters</span></span>
<span data-ttu-id="c99af-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c99af-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c99af-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c99af-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c99af-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c99af-126">INPUTS</span></span>

### <span data-ttu-id="c99af-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c99af-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c99af-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c99af-128">OUTPUTS</span></span>

### <span data-ttu-id="c99af-129">Microsoft.Azure.Commands.Batch. Models.PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="c99af-129">Microsoft.Azure.Commands.Batch.Models.PSJobStatistics</span></span>

## <span data-ttu-id="c99af-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c99af-130">NOTES</span></span>

## <span data-ttu-id="c99af-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c99af-131">RELATED LINKS</span></span>

[<span data-ttu-id="c99af-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c99af-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c99af-133">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="c99af-133">Get-AzBatchPoolStatistic</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="c99af-134">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="c99af-134">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)
