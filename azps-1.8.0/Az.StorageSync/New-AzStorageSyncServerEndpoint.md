---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 4581cfea88982eee4144730b92662374ec0a5790
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658693"
---
# <span data-ttu-id="825e4-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="825e4-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="825e4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="825e4-102">SYNOPSIS</span></span>
<span data-ttu-id="825e4-103">Mit diesem Befehl wird ein neuer Serverendpunkt auf einem registrierten Server erstellt.</span><span class="sxs-lookup"><span data-stu-id="825e4-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="825e4-104">Dadurch kann der angegebene Pfad auf dem Server mit der Synchronisierung der Dateien mit anderen Endpunkten in der Synchronisierungsgruppe beginnen.</span><span class="sxs-lookup"><span data-stu-id="825e4-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="825e4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="825e4-105">SYNTAX</span></span>

### <span data-ttu-id="825e4-106">Objectparameterset (Standard)</span><span class="sxs-lookup"><span data-stu-id="825e4-106">ObjectParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="825e4-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="825e4-107">StringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="825e4-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="825e4-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="825e4-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="825e4-109">DESCRIPTION</span></span>
<span data-ttu-id="825e4-110">Mit diesem Befehl wird ein neuer Serverendpunkt auf einem registrierten Server erstellt.</span><span class="sxs-lookup"><span data-stu-id="825e4-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="825e4-111">Dadurch kann der angegebene Pfad auf dem Server mit der Synchronisierung der Dateien mit anderen Endpunkten in der Synchronisierungsgruppe beginnen.</span><span class="sxs-lookup"><span data-stu-id="825e4-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="825e4-112">Wenn sich bereits Dateien auf anderen Endpunkten in der Synchronisierungsgruppe befinden und dieser neu hinzugefügte Speicherort ebenfalls Dateien enthält, versucht ein Abstimmungsprozess zu ermitteln, ob die Dateien in den gleichen Ordnern wie auf anderen Endpunkten tatsächlich dieselben sind.</span><span class="sxs-lookup"><span data-stu-id="825e4-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="825e4-113">Die Namespaces werden zusammengeführt, und die Abstimmung hilft, Konfliktdateien zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="825e4-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="825e4-114">Wenn Dateien auf anderen Serverendpunkten vorhanden sind, ist es häufig besser, mit einem leeren Speicherort auf diesem Server zu beginnen, damit die Dateien aus der Cloud in einem automatischen Prozess mit dem Namen fast Disaster Recovery auf dem Server herunterkommen.</span><span class="sxs-lookup"><span data-stu-id="825e4-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="825e4-115">Namespace-Metadaten werden zuerst synchronisiert, dann wird der Datenstrom jeder Datei heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="825e4-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="825e4-116">Wenn eine Datei von einem Benutzer oder einer Anwendung außerhalb der Download Reihenfolge angefordert wird, wird diese Datei mit Priorität zurückgerufen, um die Zugriffsanforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="825e4-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="825e4-117">Optional können Sie auf diesem Serverendpunkt Cloud-Tiering verwenden, um zu ermitteln, ob dieser Endpunkt zu einem Cache des vollständigen Satzes von Dateien aus der Cloud werden soll.</span><span class="sxs-lookup"><span data-stu-id="825e4-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="825e4-118">Wenn die Cloud-tierung verwendet wird, wird der Download der Dateiinhalte an dem Punkt beendet, der durch die Richtlinien für die Cloud-tierung definiert ist.</span><span class="sxs-lookup"><span data-stu-id="825e4-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="825e4-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="825e4-119">EXAMPLES</span></span>

### <span data-ttu-id="825e4-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="825e4-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="825e4-121">Mit diesem Befehl wird ein neuer Serverendpunkt auf einem registrierten Server erstellt und in eine Synchronisierungsgruppe eingefügt.</span><span class="sxs-lookup"><span data-stu-id="825e4-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="825e4-122">Auf diese Weise ist Sie Teil einer Topologie mit anderen Endpunkten, und die Datei Metadaten und-Inhalte werden sofort mit der Synchronisierung zwischen allen Speicherorten gestartet, auf die als Endpunkte in der Synchronisierungsgruppe verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="825e4-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="825e4-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="825e4-123">PARAMETERS</span></span>

### <span data-ttu-id="825e4-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="825e4-124">-AsJob</span></span>
<span data-ttu-id="825e4-125">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="825e4-125">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="825e4-126">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="825e4-126">-OfflineDataTransfer</span></span>
<span data-ttu-id="825e4-127">Daten Parameter für Cloud-seeddaten</span><span class="sxs-lookup"><span data-stu-id="825e4-127">Cloud Seeded Data Parameter</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="825e4-128">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="825e4-128">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="825e4-129">URI-Parameter für die Cloud-seeddaten-Datendatei Freigabe</span><span class="sxs-lookup"><span data-stu-id="825e4-129">Cloud Seeded Data File Share Uri Parameter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="825e4-130">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="825e4-130">-CloudTiering</span></span>
<span data-ttu-id="825e4-131">Cloud-Tiering-Parameter</span><span class="sxs-lookup"><span data-stu-id="825e4-131">Cloud Tiering Parameter</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="825e4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="825e4-132">-DefaultProfile</span></span>
<span data-ttu-id="825e4-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="825e4-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="825e4-134">-Name</span><span class="sxs-lookup"><span data-stu-id="825e4-134">-Name</span></span>
<span data-ttu-id="825e4-135">Der Name des ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="825e4-135">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="825e4-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="825e4-136">-ParentObject</span></span>
<span data-ttu-id="825e4-137">SyncGroup-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="825e4-137">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="825e4-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="825e4-138">-ParentResourceId</span></span>
<span data-ttu-id="825e4-139">SyncGroup übergeordnete Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="825e4-139">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="825e4-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="825e4-140">-ResourceGroupName</span></span>
<span data-ttu-id="825e4-141">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="825e4-141">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="825e4-142">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="825e4-142">-ServerLocalPath</span></span>
<span data-ttu-id="825e4-143">Parameter des lokalen ServerPath-Servers</span><span class="sxs-lookup"><span data-stu-id="825e4-143">Server Local Path Parameter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="825e4-144">-ServerResourceId</span><span class="sxs-lookup"><span data-stu-id="825e4-144">-ServerResourceId</span></span>
<span data-ttu-id="825e4-145">RegisteredServer-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="825e4-145">RegisteredServer Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="825e4-146">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="825e4-146">-StorageSyncServiceName</span></span>
<span data-ttu-id="825e4-147">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="825e4-147">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="825e4-148">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="825e4-148">-SyncGroupName</span></span>
<span data-ttu-id="825e4-149">Der Name des SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="825e4-149">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="825e4-150">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="825e4-150">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="825e4-151">Statusdateien, die älter als Tag-Parameter sind</span><span class="sxs-lookup"><span data-stu-id="825e4-151">Tier Files Older Than Days Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="825e4-152">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="825e4-152">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="825e4-153">Volumen freier Speicherplatz Prozent Parameter</span><span class="sxs-lookup"><span data-stu-id="825e4-153">Volume Free Space Percent Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="825e4-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="825e4-154">CommonParameters</span></span>
<span data-ttu-id="825e4-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="825e4-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="825e4-156">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="825e4-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="825e4-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="825e4-157">INPUTS</span></span>

### <span data-ttu-id="825e4-158">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="825e4-158">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="825e4-159">System. String</span><span class="sxs-lookup"><span data-stu-id="825e4-159">System.String</span></span>

## <span data-ttu-id="825e4-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="825e4-160">OUTPUTS</span></span>

### <span data-ttu-id="825e4-161">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="825e4-161">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="825e4-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="825e4-162">NOTES</span></span>

## <span data-ttu-id="825e4-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="825e4-163">RELATED LINKS</span></span>
