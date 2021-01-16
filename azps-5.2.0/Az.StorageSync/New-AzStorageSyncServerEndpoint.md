---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 53da56d932d3e2b57c2b2bbf17107918c9c1226d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366650"
---
# <span data-ttu-id="0dc83-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0dc83-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="0dc83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dc83-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc83-103">Mit diesem Befehl wird ein neuer Serverendpunkt auf einem registrierten Server erstellt.</span><span class="sxs-lookup"><span data-stu-id="0dc83-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="0dc83-104">Dadurch kann der angegebene Pfad auf dem Server die Synchronisierung der Dateien mit anderen Endpunkten in der Synchronisierungsgruppe starten.</span><span class="sxs-lookup"><span data-stu-id="0dc83-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="0dc83-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0dc83-105">SYNTAX</span></span>

### <span data-ttu-id="0dc83-106">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0dc83-106">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dc83-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc83-107">ObjectParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dc83-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc83-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dc83-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0dc83-109">DESCRIPTION</span></span>
<span data-ttu-id="0dc83-110">Mit diesem Befehl wird ein neuer Serverendpunkt auf einem registrierten Server erstellt.</span><span class="sxs-lookup"><span data-stu-id="0dc83-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="0dc83-111">Dadurch kann der angegebene Pfad auf dem Server die Synchronisierung der Dateien mit anderen Endpunkten in der Synchronisierungsgruppe starten.</span><span class="sxs-lookup"><span data-stu-id="0dc83-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="0dc83-112">Wenn es bereits Dateien auf anderen Endpunkten in der Synchronisierungsgruppe gibt und dieser neu hinzugefügte Speicherort auch Dateien enthält, versucht ein Abstimmungsprozess zu ermitteln, ob sich die Dateien tatsächlich in denselben Ordnern wie auf anderen Endpunkten befinden.</span><span class="sxs-lookup"><span data-stu-id="0dc83-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="0dc83-113">Die Namespaces werden zusammengeführt, und die Abstimmung hilft, Konflikte in Dateien zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="0dc83-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="0dc83-114">Wenn Dateien auf anderen Serverendpunkten vorhanden sind, ist es häufig besser, mit einem leeren Speicherort auf diesem Server zu beginnen, damit die Dateien aus der Cloud in einem automatischen Prozess, der als schnelle Notfallwiederherstellung bezeichnet wird, an den Server geleitet werden.</span><span class="sxs-lookup"><span data-stu-id="0dc83-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="0dc83-115">Namespacemetadaten werden zuerst synchronisiert, dann wird der Datenstrom jeder Datei heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="0dc83-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="0dc83-116">Wenn eine Datei von einem Benutzer oder einer Anwendung nicht in der Downloadreihenfolge angefordert wird, wird diese Datei mit Priorität zurückgerufen, um die Zugriffsanforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="0dc83-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="0dc83-117">Optional können Sie die Cloud tiering auf diesem Serverendpunkt verwenden, um festzustellen, ob dieser Endpunkt ein Cache der gesamten Gruppe von Dateien aus der Cloud werden soll.</span><span class="sxs-lookup"><span data-stu-id="0dc83-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="0dc83-118">Wenn Cloud tiering verwendet wird, wird der Download von Dateiinhalten an dem Punkt beendet, der durch die Cloudstufenrichtlinien definiert ist, die Sie festlegen können.</span><span class="sxs-lookup"><span data-stu-id="0dc83-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="0dc83-119">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0dc83-119">EXAMPLES</span></span>

### <span data-ttu-id="0dc83-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0dc83-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="0dc83-121">Mit diesem Befehl wird ein neuer Serverendpunkt auf einem registrierten Server erstellt und in eine Synchronisierungsgruppe eingefügt.</span><span class="sxs-lookup"><span data-stu-id="0dc83-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="0dc83-122">Auf diese Weise ist es Teil einer Topologie anderer Endpunkte. Dateimetadaten und -inhalte werden sofort mit der Synchronisierung aller Speicherorte gestartet, auf die als Endpunkte in der Synchronisierungsgruppe verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0dc83-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="0dc83-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0dc83-123">PARAMETERS</span></span>

### <span data-ttu-id="0dc83-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0dc83-124">-AsJob</span></span>
<span data-ttu-id="0dc83-125">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0dc83-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0dc83-126">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="0dc83-126">-CloudTiering</span></span>
<span data-ttu-id="0dc83-127">Cloud Tiering Parameter</span><span class="sxs-lookup"><span data-stu-id="0dc83-127">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="0dc83-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dc83-128">-DefaultProfile</span></span>
<span data-ttu-id="0dc83-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0dc83-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0dc83-130">-Name</span><span class="sxs-lookup"><span data-stu-id="0dc83-130">-Name</span></span>
<span data-ttu-id="0dc83-131">Der Name von ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0dc83-131">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="0dc83-132">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="0dc83-132">-OfflineDataTransfer</span></span>
<span data-ttu-id="0dc83-133">Parameter für Daten mit Cloud-Startwert</span><span class="sxs-lookup"><span data-stu-id="0dc83-133">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="0dc83-134">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="0dc83-134">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="0dc83-135">Cloud Seeded Data File Share Uri Parameter</span><span class="sxs-lookup"><span data-stu-id="0dc83-135">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="0dc83-136">-initialDownloadPolicy</span><span class="sxs-lookup"><span data-stu-id="0dc83-136">-initialDownloadPolicy</span></span>
<span data-ttu-id="0dc83-137">Parameter für den lokalen Cachemodus</span><span class="sxs-lookup"><span data-stu-id="0dc83-137">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="0dc83-138">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="0dc83-138">-localCacheMode</span></span>
<span data-ttu-id="0dc83-139">Parameter für den lokalen Cachemodus</span><span class="sxs-lookup"><span data-stu-id="0dc83-139">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="0dc83-140">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0dc83-140">-ParentObject</span></span>
<span data-ttu-id="0dc83-141">SyncGroup-Objekt, das normalerweise über den Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="0dc83-141">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="0dc83-142">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0dc83-142">-ParentResourceId</span></span>
<span data-ttu-id="0dc83-143">Übergeordnete Ressourcen-ID der Synchronisierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="0dc83-143">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="0dc83-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dc83-144">-ResourceGroupName</span></span>
<span data-ttu-id="0dc83-145">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="0dc83-145">Resource Group Name.</span></span>

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

### <span data-ttu-id="0dc83-146">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="0dc83-146">-ServerLocalPath</span></span>
<span data-ttu-id="0dc83-147">Parameter für lokalen Serverpfad</span><span class="sxs-lookup"><span data-stu-id="0dc83-147">Server Local Path Parameter</span></span>

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

### <span data-ttu-id="0dc83-148">-ServerResourceId</span><span class="sxs-lookup"><span data-stu-id="0dc83-148">-ServerResourceId</span></span>
<span data-ttu-id="0dc83-149">RegisteredServer Resource Id</span><span class="sxs-lookup"><span data-stu-id="0dc83-149">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="0dc83-150">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="0dc83-150">-StorageSyncServiceName</span></span>
<span data-ttu-id="0dc83-151">Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="0dc83-151">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="0dc83-152">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="0dc83-152">-SyncGroupName</span></span>
<span data-ttu-id="0dc83-153">Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0dc83-153">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="0dc83-154">-TierFilesOlderDays</span><span class="sxs-lookup"><span data-stu-id="0dc83-154">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="0dc83-155">Parameter 'Dateien stufen, die älter als Tage' sind</span><span class="sxs-lookup"><span data-stu-id="0dc83-155">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="0dc83-156">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="0dc83-156">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="0dc83-157">Parameter "Volume Free Space Percent"</span><span class="sxs-lookup"><span data-stu-id="0dc83-157">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="0dc83-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0dc83-158">-Confirm</span></span>
<span data-ttu-id="0dc83-159">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0dc83-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dc83-160">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0dc83-160">-WhatIf</span></span>
<span data-ttu-id="0dc83-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0dc83-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0dc83-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0dc83-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dc83-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc83-163">CommonParameters</span></span>
<span data-ttu-id="0dc83-164">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dc83-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc83-165">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dc83-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc83-166">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0dc83-166">INPUTS</span></span>

### <span data-ttu-id="0dc83-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0dc83-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="0dc83-168">System.String</span><span class="sxs-lookup"><span data-stu-id="0dc83-168">System.String</span></span>

## <span data-ttu-id="0dc83-169">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0dc83-169">OUTPUTS</span></span>

### <span data-ttu-id="0dc83-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0dc83-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="0dc83-171">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0dc83-171">NOTES</span></span>

## <span data-ttu-id="0dc83-172">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0dc83-172">RELATED LINKS</span></span>
