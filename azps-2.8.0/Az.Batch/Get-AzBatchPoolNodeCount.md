---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolnodecount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
ms.openlocfilehash: 0390e6f156e305c3ba5f34d78dcf33520098bee3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93657906"
---
# <span data-ttu-id="d028e-101">Get-AzBatchPoolNodeCount</span><span class="sxs-lookup"><span data-stu-id="d028e-101">Get-AzBatchPoolNodeCount</span></span>

## <span data-ttu-id="d028e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d028e-102">SYNOPSIS</span></span>
<span data-ttu-id="d028e-103">Ruft Batch-Knoten Zähler pro Knotenzustand nach Pool-ID ab.</span><span class="sxs-lookup"><span data-stu-id="d028e-103">Gets Batch node counts per node state grouped by pool id.</span></span>

## <span data-ttu-id="d028e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d028e-104">SYNTAX</span></span>

### <span data-ttu-id="d028e-105">AzureBatchPoolNodeCounts (Standard)</span><span class="sxs-lookup"><span data-stu-id="d028e-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzBatchPoolNodeCount -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d028e-106">Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="d028e-106">PoolId</span></span>
```
Get-AzBatchPoolNodeCount [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d028e-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="d028e-107">ParentObject</span></span>
```
Get-AzBatchPoolNodeCount [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d028e-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="d028e-108">ODataFilter</span></span>
```
Get-AzBatchPoolNodeCount [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d028e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d028e-109">DESCRIPTION</span></span>
<span data-ttu-id="d028e-110">Das Get-AzBatchPoolNodeCount-Cmdlet ermöglicht es Kunden, die Knotenanzahl pro Knotenstatus nach Pool gruppiert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d028e-110">The Get-AzBatchPoolNodeCount cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="d028e-111">Mögliche Knoten Zustände sind das Erstellen, idlen, leavingPool, offline, verdrängte, Neustarten, reimaging, ausführen, starten, startTaskFailed, unbekannt, unbrauchbar und waitingForStartTask.</span><span class="sxs-lookup"><span data-stu-id="d028e-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="d028e-112">Das Cmdlet verwendet Pool-ID oder Pool-Parameter, um nur Pool mit der angegebenen Pool-ID zu filtern.</span><span class="sxs-lookup"><span data-stu-id="d028e-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="d028e-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d028e-113">EXAMPLES</span></span>

### <span data-ttu-id="d028e-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d028e-114">Example 1</span></span>

```powershell
PS C:\> $batchContext = Get-AzBatchAccountKeys -AccountName "contosobatch"
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="d028e-115">Listenknoten Anzahl pro Knotenstatus für Pools unter aktuellem Batch Konto Kontext.</span><span class="sxs-lookup"><span data-stu-id="d028e-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="d028e-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d028e-116">Example 2</span></span>

```powershell
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0

PS C:\> $poolnodecounts = Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"
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

PS C:\> Get-AzBatchPool -Id "contosopool1" -BatchContext $batchContext | Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
```

<span data-ttu-id="d028e-117">Zeigt die Anzahl der Knoten pro Knotenstatus für eine Pool-ID an.</span><span class="sxs-lookup"><span data-stu-id="d028e-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="d028e-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="d028e-118">PARAMETERS</span></span>

### <span data-ttu-id="d028e-119">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="d028e-119">-BatchContext</span></span>
<span data-ttu-id="d028e-120">Die BatchAccountContext-Instanz, die bei der Interaktion mit dem Batch Dienst verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d028e-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="d028e-121">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d028e-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="d028e-122">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d028e-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="d028e-123">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="d028e-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="d028e-124">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="d028e-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d028e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d028e-125">-DefaultProfile</span></span>
<span data-ttu-id="d028e-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d028e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d028e-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d028e-127">-MaxCount</span></span>
<span data-ttu-id="d028e-128">Gibt die maximale Anzahl von Pools an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d028e-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="d028e-129">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="d028e-129">The default value is 10.</span></span>

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

### <span data-ttu-id="d028e-130">-Pool</span><span class="sxs-lookup"><span data-stu-id="d028e-130">-Pool</span></span>
<span data-ttu-id="d028e-131">Gibt die **PSCloudPool** an, für die die Knotenanzahl abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d028e-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

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

### <span data-ttu-id="d028e-132">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="d028e-132">-PoolId</span></span>
<span data-ttu-id="d028e-133">Die ID des Pools, für den die Knotenanzahl abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d028e-133">The id of the pool for which to get node counts.</span></span>

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

### <span data-ttu-id="d028e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d028e-134">CommonParameters</span></span>
<span data-ttu-id="d028e-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d028e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d028e-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d028e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d028e-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d028e-137">INPUTS</span></span>

### <span data-ttu-id="d028e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d028e-138">System.String</span></span>

### <span data-ttu-id="d028e-139">Microsoft.Azure.Commands.Batch. Models. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="d028e-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="d028e-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d028e-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d028e-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d028e-141">OUTPUTS</span></span>

### <span data-ttu-id="d028e-142">Microsoft.Azure.Commands.Batch. Models. PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="d028e-142">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="d028e-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="d028e-143">NOTES</span></span>

## <span data-ttu-id="d028e-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d028e-144">RELATED LINKS</span></span>

[<span data-ttu-id="d028e-145">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d028e-145">Get-AzBatchAccountKeys</span></span>]()

[<span data-ttu-id="d028e-146">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d028e-146">Get-AzBatchJob</span></span>]()

[<span data-ttu-id="d028e-147">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="d028e-147">Azure Batch Cmdlets</span></span>]()

