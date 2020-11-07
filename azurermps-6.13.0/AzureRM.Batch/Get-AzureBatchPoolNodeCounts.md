---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpoolnodecounts
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolNodeCounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolNodeCounts.md
ms.openlocfilehash: 6cd15b6a8ee59982bf328f751a20807835f54513
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663386"
---
# <span data-ttu-id="b22ab-101">Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="b22ab-101">Get-AzureBatchPoolNodeCounts</span></span>

## <span data-ttu-id="b22ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b22ab-102">SYNOPSIS</span></span>
<span data-ttu-id="b22ab-103">Ruft Batch-Knoten Zähler pro Knotenzustand nach Pool-ID ab.</span><span class="sxs-lookup"><span data-stu-id="b22ab-103">Gets Batch node counts per node state grouped by pool id.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b22ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b22ab-104">SYNTAX</span></span>

### <span data-ttu-id="b22ab-105">AzureBatchPoolNodeCounts (Standard)</span><span class="sxs-lookup"><span data-stu-id="b22ab-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzureBatchPoolNodeCounts -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b22ab-106">Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="b22ab-106">PoolId</span></span>
```
Get-AzureBatchPoolNodeCounts [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b22ab-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="b22ab-107">ParentObject</span></span>
```
Get-AzureBatchPoolNodeCounts [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b22ab-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="b22ab-108">ODataFilter</span></span>
```
Get-AzureBatchPoolNodeCounts [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b22ab-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b22ab-109">DESCRIPTION</span></span>
<span data-ttu-id="b22ab-110">Das Get-AzureBatchPoolNodeCounts-Cmdlet ermöglicht es Kunden, die Knotenanzahl pro Knotenstatus nach Pool gruppiert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b22ab-110">The Get-AzureBatchPoolNodeCounts cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="b22ab-111">Mögliche Knoten Zustände sind das Erstellen, idlen, leavingPool, offline, verdrängte, Neustarten, reimaging, ausführen, starten, startTaskFailed, unbekannt, unbrauchbar und waitingForStartTask.</span><span class="sxs-lookup"><span data-stu-id="b22ab-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="b22ab-112">Das Cmdlet verwendet Pool-ID oder Pool-Parameter, um nur Pool mit der angegebenen Pool-ID zu filtern.</span><span class="sxs-lookup"><span data-stu-id="b22ab-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="b22ab-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b22ab-113">EXAMPLES</span></span>

### <span data-ttu-id="b22ab-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b22ab-114">Example 1</span></span>

```powershell
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Get-AzureBatchPoolNodeCounts -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="b22ab-115">Listenknoten Anzahl pro Knotenstatus für Pools unter aktuellem Batch Konto Kontext.</span><span class="sxs-lookup"><span data-stu-id="b22ab-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="b22ab-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b22ab-116">Example 2</span></span>

```powershell
PS C:\> Get-AzureBatchPoolNodeCounts -BatchContext $batchContext -PoolId "contosopool1"

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0

PS C:\> $poolnodecounts = Get-AzureBatchPoolNodeCounts -BatchContext $batchContext -PoolId "contosopool1"
PS C:\> $poolnodecounts.Dedicated

Creating            : 1
Idle                : 1
LeavingPool         : 0
Offline             : 0
Preempted           : 0
Rebooting           : 1
Reimaging           : 0
Running             : 5
Starting            : 0
StartTaskFailed     : 0
Total               : 8
Unknown             : 0
Unusable            : 0
WaitingForStartTask : 0

PS C:\> Get-AzureBatchPool -Id "contosopool1" -BatchContext $batchContext | Get-AzureBatchPoolNodeCounts -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
```

<span data-ttu-id="b22ab-117">Zeigt die Anzahl der Knoten pro Knotenstatus für eine Pool-ID an.</span><span class="sxs-lookup"><span data-stu-id="b22ab-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="b22ab-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="b22ab-118">PARAMETERS</span></span>

### <span data-ttu-id="b22ab-119">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="b22ab-119">-BatchContext</span></span>
<span data-ttu-id="b22ab-120">Die BatchAccountContext-Instanz, die bei der Interaktion mit dem Batch Dienst verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b22ab-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="b22ab-121">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b22ab-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="b22ab-122">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b22ab-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="b22ab-123">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="b22ab-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="b22ab-124">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="b22ab-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b22ab-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b22ab-125">-DefaultProfile</span></span>
<span data-ttu-id="b22ab-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b22ab-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b22ab-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b22ab-127">-MaxCount</span></span>
<span data-ttu-id="b22ab-128">Gibt die maximale Anzahl von Pools an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b22ab-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="b22ab-129">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="b22ab-129">The default value is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22ab-130">-Pool</span><span class="sxs-lookup"><span data-stu-id="b22ab-130">-Pool</span></span>
<span data-ttu-id="b22ab-131">Gibt die **PSCloudPool** an, für die die Knotenanzahl abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b22ab-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b22ab-132">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="b22ab-132">-PoolId</span></span>
<span data-ttu-id="b22ab-133">Die ID des Pools, für den die Knotenanzahl abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b22ab-133">The id of the pool for which to get node counts.</span></span>

```yaml
Type: System.String
Parameter Sets: PoolId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b22ab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b22ab-134">CommonParameters</span></span>
<span data-ttu-id="b22ab-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b22ab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b22ab-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b22ab-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b22ab-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b22ab-137">INPUTS</span></span>

### <span data-ttu-id="b22ab-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b22ab-138">System.String</span></span>

### <span data-ttu-id="b22ab-139">Microsoft.Azure.Commands.Batch. Models. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="b22ab-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>
<span data-ttu-id="b22ab-140">Parameter: Pool (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b22ab-140">Parameters: Pool (ByValue)</span></span>

### <span data-ttu-id="b22ab-141">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b22ab-141">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="b22ab-142">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b22ab-142">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="b22ab-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b22ab-143">OUTPUTS</span></span>

### <span data-ttu-id="b22ab-144">Microsoft.Azure.Commands.Batch. Models. PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="b22ab-144">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="b22ab-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="b22ab-145">NOTES</span></span>

## <span data-ttu-id="b22ab-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b22ab-146">RELATED LINKS</span></span>

[<span data-ttu-id="b22ab-147">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b22ab-147">Get-AzureRmBatchAccountKeys</span></span>]()

[<span data-ttu-id="b22ab-148">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b22ab-148">Get-AzureBatchJob</span></span>]()

[<span data-ttu-id="b22ab-149">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="b22ab-149">Azure Batch Cmdlets</span></span>]()

