---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/Start-AzureBatchComputeNodeServiceLogUpload
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchComputeNodeServiceLogUpload.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchComputeNodeServiceLogUpload.md
ms.openlocfilehash: 8f171b42e3f1e1f087890ec451d5a3ff13cb8c57
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498405"
---
# <span data-ttu-id="aab0e-101">Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="aab0e-101">Start-AzureBatchComputeNodeServiceLogUpload</span></span>

## <span data-ttu-id="aab0e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aab0e-102">SYNOPSIS</span></span>
<span data-ttu-id="aab0e-103">Hochladen von Protokolldateien des Compute-Knoten Diensts in einen Azure-Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="aab0e-103">Upload compute node service log files to an Azure Storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aab0e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aab0e-104">SYNTAX</span></span>

### <span data-ttu-id="aab0e-105">AzureBatchComputeNodeServiceLogUpload (Standard)</span><span class="sxs-lookup"><span data-stu-id="aab0e-105">AzureBatchComputeNodeServiceLogUpload (Default)</span></span>
```
Start-AzureBatchComputeNodeServiceLogUpload [-ContainerUrl] <String> [-StartTime] <DateTime>
 [-EndTime <DateTime>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aab0e-106">ID</span><span class="sxs-lookup"><span data-stu-id="aab0e-106">Id</span></span>
```
Start-AzureBatchComputeNodeServiceLogUpload [-PoolId] <String> [-ComputeNodeId] <String>
 [-ContainerUrl] <String> [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aab0e-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="aab0e-107">ParentObject</span></span>
```
Start-AzureBatchComputeNodeServiceLogUpload [-ComputeNode] <PSComputeNode> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aab0e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aab0e-108">DESCRIPTION</span></span>
<span data-ttu-id="aab0e-109">Dieses Cmdlet sammelt Azure-Batch Dienst-Protokolldateien von Compute-Knoten, wenn ein Fehler auftritt und die Azure-Unterstützung eskaliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="aab0e-109">This cmdlet gathers Azure Batch service log files from compute nodes if you are experiencing an error and wish to escalate to Azure support.</span></span> <span data-ttu-id="aab0e-110">Die Azure-Batch Dienst-Protokolldateien sollten für Azure-Unterstützung freigegeben werden, um Probleme mit dem Batch Dienst zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="aab0e-110">The Azure Batch service log files should be shared with Azure support to aid in debugging issues with the Batch service.</span></span> 

## <span data-ttu-id="aab0e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aab0e-111">EXAMPLES</span></span>

### <span data-ttu-id="aab0e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aab0e-112">Example 1</span></span>

```powershell
PS C:\> $storageContext = New-AzureStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzureStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Start-AzureBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    4 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="aab0e-113">Upload Compute Node-Dienstprotokolle, die am oder nach dem 1. Januar 2018 Mitternacht geschrieben wurden, die vom Compute-Knoten abgerufen wurden, angegebene Pool-ID des Pools, in dem sich der Compute-Knoten befindet, und Compute Node-ID.</span><span class="sxs-lookup"><span data-stu-id="aab0e-113">Upload compute node service logs written on or after January 1, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="aab0e-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="aab0e-114">Example 2</span></span>

```powershell
PS C:\> $storageContext = New-AzureStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzureStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Start-AzureBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="aab0e-115">Upload Compute Node-Dienstprotokolle, die am oder nach dem 1. Januar, 2018 Mitternacht und vor dem 10. Januar 2018 Uhr geschrieben wurden, die vom Compute-Knoten abgerufen wurden, angegebene Pool-ID des Pools, in dem sich der Compute-Knoten befindet, und Compute Node-ID.</span><span class="sxs-lookup"><span data-stu-id="aab0e-115">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="aab0e-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="aab0e-116">Example 3</span></span>

```powershell
PS C:\> $storageContext = New-AzureStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzureStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Get-AzureBatchComputeNode -BatchContext $batchContext -Id "tvm-1612030122_1-20180405t234700z" -PoolId "contosopool" | Start-AzureBatchComputeNodeServiceLogUpload -BatchContext $batchContext -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="aab0e-117">Upload Compute Node-Dienstprotokolle, die am oder nach dem 1. Januar, 2018 Mitternacht und vor dem 10. Januar 2018 Uhr geschrieben wurden, die vom Compute Node-Objekt abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="aab0e-117">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node object.</span></span>

## <span data-ttu-id="aab0e-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="aab0e-118">PARAMETERS</span></span>

### <span data-ttu-id="aab0e-119">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="aab0e-119">-BatchContext</span></span>
<span data-ttu-id="aab0e-120">Die BatchAccountContext-Instanz, die bei der Interaktion mit dem Batch Dienst verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="aab0e-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="aab0e-121">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="aab0e-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="aab0e-122">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="aab0e-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="aab0e-123">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="aab0e-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="aab0e-124">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="aab0e-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="aab0e-125">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="aab0e-125">-ComputeNode</span></span>
<span data-ttu-id="aab0e-126">Gibt das **PSComputeNode** -Objekt an, aus dem Dienstprotokolle abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="aab0e-126">Specifies the **PSComputeNode** object from which service logs are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aab0e-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="aab0e-127">-ComputeNodeId</span></span>
<span data-ttu-id="aab0e-128">Die ID des Compute-Knotens.</span><span class="sxs-lookup"><span data-stu-id="aab0e-128">The id of the compute node.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab0e-129">-ContainerUrl</span><span class="sxs-lookup"><span data-stu-id="aab0e-129">-ContainerUrl</span></span>
<span data-ttu-id="aab0e-130">Die Container-URL zum Azure-Speicher.</span><span class="sxs-lookup"><span data-stu-id="aab0e-130">The container url to Azure Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab0e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aab0e-131">-DefaultProfile</span></span>
<span data-ttu-id="aab0e-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aab0e-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aab0e-133">-EndTime</span><span class="sxs-lookup"><span data-stu-id="aab0e-133">-EndTime</span></span>
<span data-ttu-id="aab0e-134">Die Endzeit des Dienst Protokolls, das hochgeladen werden soll (optional).</span><span class="sxs-lookup"><span data-stu-id="aab0e-134">The end time of service log to be uploaded (optional).</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab0e-135">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="aab0e-135">-PoolId</span></span>
<span data-ttu-id="aab0e-136">Die ID des Pools, der den Compute-Knoten enthält.</span><span class="sxs-lookup"><span data-stu-id="aab0e-136">The id of the pool that contains the compute node.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab0e-137">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="aab0e-137">-StartTime</span></span>
<span data-ttu-id="aab0e-138">Die Startzeit des Dienst Protokolls, das hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="aab0e-138">The start time of service log to be uploaded.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab0e-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aab0e-139">-Confirm</span></span>
<span data-ttu-id="aab0e-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aab0e-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab0e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aab0e-141">-WhatIf</span></span>
<span data-ttu-id="aab0e-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aab0e-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aab0e-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aab0e-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab0e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab0e-144">CommonParameters</span></span>
<span data-ttu-id="aab0e-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aab0e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aab0e-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aab0e-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aab0e-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aab0e-147">INPUTS</span></span>

### <span data-ttu-id="aab0e-148">Microsoft.Azure.Commands.Batch. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="aab0e-148">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="aab0e-149">Parameter: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aab0e-149">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="aab0e-150">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="aab0e-150">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="aab0e-151">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aab0e-151">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="aab0e-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aab0e-152">OUTPUTS</span></span>

### <span data-ttu-id="aab0e-153">Microsoft.Azure.Commands.Batch. Models. PSStartComputeNodeServiceLogUploadResult</span><span class="sxs-lookup"><span data-stu-id="aab0e-153">Microsoft.Azure.Commands.Batch.Models.PSStartComputeNodeServiceLogUploadResult</span></span>

## <span data-ttu-id="aab0e-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="aab0e-154">NOTES</span></span>

## <span data-ttu-id="aab0e-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aab0e-155">RELATED LINKS</span></span>
