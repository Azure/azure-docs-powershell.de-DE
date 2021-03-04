---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: 12bfa9ab7e35bab3421bee71cf5ea0787c95a86d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918032"
---
# <span data-ttu-id="a37bf-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a37bf-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="a37bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a37bf-102">SYNOPSIS</span></span>
<span data-ttu-id="a37bf-103">Entfernt den angegebenen Speicherblob.</span><span class="sxs-lookup"><span data-stu-id="a37bf-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="a37bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a37bf-104">SYNTAX</span></span>

### <span data-ttu-id="a37bf-105">NamePipeline (Standard)</span><span class="sxs-lookup"><span data-stu-id="a37bf-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a37bf-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="a37bf-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a37bf-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="a37bf-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot]
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a37bf-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a37bf-108">DESCRIPTION</span></span>
<span data-ttu-id="a37bf-109">Das **Cmdlet Remove-AzStorageBlob** entfernt den angegebenen Blob aus einem Speicherkonto in Azure.</span><span class="sxs-lookup"><span data-stu-id="a37bf-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="a37bf-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a37bf-110">EXAMPLES</span></span>

### <span data-ttu-id="a37bf-111">Beispiel 1: Entfernen eines Speicherblobs nach Name</span><span class="sxs-lookup"><span data-stu-id="a37bf-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="a37bf-112">Mit diesem Befehl wird ein blob entfernt, das durch seinen Namen identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="a37bf-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="a37bf-113">Beispiel 2: Entfernen eines Speicherblobs mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="a37bf-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="a37bf-114">Dieser Befehl verwendet die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a37bf-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="a37bf-115">Beispiel 3: Entfernen von Speicherblobs mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="a37bf-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="a37bf-116">Bei diesem Befehl werden das Sternchen (\*) und die Pipeline verwendet, um die Blobs oder Blobs abzurufen und dann zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="a37bf-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

### <span data-ttu-id="a37bf-117">Beispiel 4: Entfernen einer einzelnen Blobversion</span><span class="sxs-lookup"><span data-stu-id="a37bf-117">Example 4: Remove a single blob version</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z"
```

<span data-ttu-id="a37bf-118">Mit diesem Befehl wird ein einzelner Blobs verion mit VersionId entfernt.</span><span class="sxs-lookup"><span data-stu-id="a37bf-118">This command removes a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="a37bf-119">Beispiel 5: Entfernen einer einzelnen Blobmomentaufnahme</span><span class="sxs-lookup"><span data-stu-id="a37bf-119">Example 5: Remove a single blob snapshot</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"
```

<span data-ttu-id="a37bf-120">Mit diesem Befehl wird eine einzelne Blobs-Momentaufnahme mit SnapshotTime entfernt.</span><span class="sxs-lookup"><span data-stu-id="a37bf-120">This command removes a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="a37bf-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a37bf-121">PARAMETERS</span></span>

### <span data-ttu-id="a37bf-122">-Blob</span><span class="sxs-lookup"><span data-stu-id="a37bf-122">-Blob</span></span>
<span data-ttu-id="a37bf-123">Gibt den Namen des Blobs an, den Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="a37bf-123">Specifies the name of the blob you want to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a37bf-124">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="a37bf-124">-BlobBaseClient</span></span>
<span data-ttu-id="a37bf-125">BlobBaseClient-Objekt</span><span class="sxs-lookup"><span data-stu-id="a37bf-125">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a37bf-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a37bf-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a37bf-127">Gibt das clientseitige Zeitintervall in Sekunden für eine Dienstanforderung an.</span><span class="sxs-lookup"><span data-stu-id="a37bf-127">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a37bf-128">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a37bf-128">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a37bf-129">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="a37bf-129">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a37bf-130">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a37bf-130">-CloudBlob</span></span>
<span data-ttu-id="a37bf-131">Gibt einen Cloudblob an.</span><span class="sxs-lookup"><span data-stu-id="a37bf-131">Specifies a cloud blob.</span></span>
<span data-ttu-id="a37bf-132">Um ein **CloudBlob-Objekt zu** erhalten, verwenden Sie das Get-AzStorageBlob Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a37bf-132">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a37bf-133">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a37bf-133">-CloudBlobContainer</span></span>
<span data-ttu-id="a37bf-134">Gibt ein **CloudBlobContainer-Objekt** aus der Azure Storage Client-Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="a37bf-134">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="a37bf-135">Sie können das cmdlet Get-AzStorageContainer verwenden, um es zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a37bf-135">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a37bf-136">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a37bf-136">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a37bf-137">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="a37bf-137">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a37bf-138">Mit diesem Parameter können Sie die Parallelität einschränken, um die lokale CPU- und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="a37bf-138">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a37bf-139">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="a37bf-139">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a37bf-140">Dieser Parameter kann dazu beitragen, Netzwerkverbindungsprobleme in Umgebungen mit geringer Bandbreite zu verringern, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="a37bf-140">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a37bf-141">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="a37bf-141">The default value is 10.</span></span>

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

### <span data-ttu-id="a37bf-142">-Container</span><span class="sxs-lookup"><span data-stu-id="a37bf-142">-Container</span></span>
<span data-ttu-id="a37bf-143">Gibt den Namen des Containers an.</span><span class="sxs-lookup"><span data-stu-id="a37bf-143">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a37bf-144">-Context</span><span class="sxs-lookup"><span data-stu-id="a37bf-144">-Context</span></span>
<span data-ttu-id="a37bf-145">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="a37bf-145">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a37bf-146">Sie können das cmdlet New-AzStorageContext verwenden, um es zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a37bf-146">You can use the New-AzStorageContext cmdlet to create it.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a37bf-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a37bf-147">-DefaultProfile</span></span>
<span data-ttu-id="a37bf-148">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a37bf-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a37bf-149">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="a37bf-149">-DeleteSnapshot</span></span>
<span data-ttu-id="a37bf-150">Gibt an, dass alle Momentaufnahmen gelöscht werden, nicht aber das Basisblob.</span><span class="sxs-lookup"><span data-stu-id="a37bf-150">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="a37bf-151">Wenn dieser Parameter nicht angegeben ist, werden der Basisblob und seine Momentaufnahmen zusammen gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a37bf-151">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="a37bf-152">Der Benutzer wird aufgefordert, den Löschvorgang zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="a37bf-152">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="a37bf-153">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="a37bf-153">-Force</span></span>
<span data-ttu-id="a37bf-154">Gibt an, dass dieses Cmdlet den Blob und dessen Momentaufnahme ohne Bestätigung entfernt.</span><span class="sxs-lookup"><span data-stu-id="a37bf-154">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="a37bf-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a37bf-155">-PassThru</span></span>
<span data-ttu-id="a37bf-156">Gibt an, dass dieses Cmdlet einen **booleschen** Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="a37bf-156">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a37bf-157">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a37bf-157">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a37bf-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a37bf-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a37bf-159">Gibt das Azure-Profil für das zu lesende Cmdlet an.</span><span class="sxs-lookup"><span data-stu-id="a37bf-159">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="a37bf-160">Wenn nicht angegeben, liest das Cmdlet aus dem Standardprofil vor.</span><span class="sxs-lookup"><span data-stu-id="a37bf-160">If not specified, the cmdlet reads from the default profile.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a37bf-161">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="a37bf-161">-SnapshotTime</span></span>
<span data-ttu-id="a37bf-162">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="a37bf-162">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a37bf-163">-VersionId</span><span class="sxs-lookup"><span data-stu-id="a37bf-163">-VersionId</span></span>
<span data-ttu-id="a37bf-164">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="a37bf-164">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a37bf-165">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a37bf-165">-Confirm</span></span>
<span data-ttu-id="a37bf-166">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a37bf-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a37bf-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a37bf-167">-WhatIf</span></span>
<span data-ttu-id="a37bf-168">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a37bf-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a37bf-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a37bf-169">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a37bf-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a37bf-170">CommonParameters</span></span>
<span data-ttu-id="a37bf-171">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a37bf-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a37bf-172">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a37bf-172">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a37bf-173">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a37bf-173">INPUTS</span></span>

### <span data-ttu-id="a37bf-174">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a37bf-174">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="a37bf-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a37bf-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="a37bf-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a37bf-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a37bf-177">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a37bf-177">OUTPUTS</span></span>

### <span data-ttu-id="a37bf-178">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a37bf-178">System.Boolean</span></span>

## <span data-ttu-id="a37bf-179">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a37bf-179">NOTES</span></span>

## <span data-ttu-id="a37bf-180">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a37bf-180">RELATED LINKS</span></span>

[<span data-ttu-id="a37bf-181">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a37bf-181">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="a37bf-182">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a37bf-182">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="a37bf-183">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a37bf-183">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
