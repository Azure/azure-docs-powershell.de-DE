---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: 37ae4192e973d218bd0cb23f9ccba16367098d30
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164764"
---
# <span data-ttu-id="b9bd4-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b9bd4-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="b9bd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="b9bd4-103">Entfernt das angegebene Speicher-BLOB.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="b9bd4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9bd4-104">SYNTAX</span></span>

### <span data-ttu-id="b9bd4-105">NamePipeline (Standard)</span><span class="sxs-lookup"><span data-stu-id="b9bd4-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9bd4-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="b9bd4-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9bd4-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="b9bd4-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot]
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9bd4-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9bd4-108">DESCRIPTION</span></span>
<span data-ttu-id="b9bd4-109">Das **Cmdlet "Remove-AzStorageBlob"** entfernt das angegebene BLOB aus einem Speicherkonto in Azure.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="b9bd4-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b9bd4-110">EXAMPLES</span></span>

### <span data-ttu-id="b9bd4-111">Beispiel 1: Entfernen eines Speicher-BLOB nach Name</span><span class="sxs-lookup"><span data-stu-id="b9bd4-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="b9bd4-112">Mit diesem Befehl wird ein blob entfernt, das durch seinen Namen identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="b9bd4-113">Beispiel 2: Entfernen eines Speicher-BLOB mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="b9bd4-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="b9bd4-114">Dieser Befehl verwendet die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="b9bd4-115">Beispiel 3: Entfernen von Speicher-BLOBs mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="b9bd4-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="b9bd4-116">Dieser Befehl verwendet das Platzhalterzeichen Sternchen (\*) und die Pipeline, um das BLOB oder die BLOB abzurufen, und entfernt diese dann.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

### <span data-ttu-id="b9bd4-117">Beispiel 4: Entfernen einer einzelnen BLOB-Version</span><span class="sxs-lookup"><span data-stu-id="b9bd4-117">Example 4: Remove a single blob version</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z"
```

<span data-ttu-id="b9bd4-118">Mit diesem Befehl wird ein einzelner BLOBS-Verion mit VersionId entfernt.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-118">This command removes a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="b9bd4-119">Beispiel 5: Entfernen einer einzelnen BLOB-Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="b9bd4-119">Example 5: Remove a single blob snapshot</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"
```

<span data-ttu-id="b9bd4-120">Mit diesem Befehl wird eine einzelne Blobs-Momentaufnahme mit SnapshotTime entfernt.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-120">This command removes a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="b9bd4-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9bd4-121">PARAMETERS</span></span>

### <span data-ttu-id="b9bd4-122">-BLOB</span><span class="sxs-lookup"><span data-stu-id="b9bd4-122">-Blob</span></span>
<span data-ttu-id="b9bd4-123">Gibt den Namen des BLOB an, das Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-123">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="b9bd4-124">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="b9bd4-124">-BlobBaseClient</span></span>
<span data-ttu-id="b9bd4-125">BlobBaseClient-Objekt</span><span class="sxs-lookup"><span data-stu-id="b9bd4-125">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="b9bd4-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b9bd4-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b9bd4-127">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-127">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b9bd4-128">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-128">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b9bd4-129">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-129">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b9bd4-130">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b9bd4-130">-CloudBlob</span></span>
<span data-ttu-id="b9bd4-131">Gibt ein Cloud-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-131">Specifies a cloud blob.</span></span>
<span data-ttu-id="b9bd4-132">Verwenden Sie zum **Abrufen eines CloudBlob-Objekts** das Get-AzStorageBlob-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-132">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="b9bd4-133">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b9bd4-133">-CloudBlobContainer</span></span>
<span data-ttu-id="b9bd4-134">Gibt ein **CloudBlobContainer-Objekt** aus der Azure Storage Client Library an.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-134">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="b9bd4-135">Sie können das Get-AzStorageContainer cmdlet verwenden, um es zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-135">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="b9bd4-136">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b9bd4-136">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b9bd4-137">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-137">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b9bd4-138">Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-138">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b9bd4-139">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-139">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b9bd4-140">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-140">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b9bd4-141">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-141">The default value is 10.</span></span>

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

### <span data-ttu-id="b9bd4-142">-Container</span><span class="sxs-lookup"><span data-stu-id="b9bd4-142">-Container</span></span>
<span data-ttu-id="b9bd4-143">Gibt den Namen des Containers an.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-143">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="b9bd4-144">-Context</span><span class="sxs-lookup"><span data-stu-id="b9bd4-144">-Context</span></span>
<span data-ttu-id="b9bd4-145">Gibt den Azure -Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-145">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b9bd4-146">Sie können das cmdlet New-AzStorageContext zum Erstellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-146">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="b9bd4-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9bd4-147">-DefaultProfile</span></span>
<span data-ttu-id="b9bd4-148">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9bd4-149">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="b9bd4-149">-DeleteSnapshot</span></span>
<span data-ttu-id="b9bd4-150">Gibt an, dass alle Momentaufnahmen gelöscht werden, aber nicht das Basis-BLOB.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-150">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="b9bd4-151">Wenn dieser Parameter nicht angegeben wird, werden das Basis-BLOB und seine Momentaufnahmen zusammen gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-151">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="b9bd4-152">Der Benutzer wird aufgefordert, den Löschvorgang zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-152">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="b9bd4-153">-Force</span><span class="sxs-lookup"><span data-stu-id="b9bd4-153">-Force</span></span>
<span data-ttu-id="b9bd4-154">Gibt an, dass dieses Cmdlet den BLOB und dessen Momentaufnahme ohne Bestätigung entfernt.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-154">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="b9bd4-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9bd4-155">-PassThru</span></span>
<span data-ttu-id="b9bd4-156">Gibt an, dass dieses Cmdlet einen **booleschen** Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-156">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="b9bd4-157">Dieses Cmdlet gibt standardmäßig keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-157">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="b9bd4-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b9bd4-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b9bd4-159">Gibt das zu lesende Azure-Profil für das Cmdlet an.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-159">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="b9bd4-160">Wenn nichts angegeben ist, liest das Cmdlet aus dem Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-160">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="b9bd4-161">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="b9bd4-161">-SnapshotTime</span></span>
<span data-ttu-id="b9bd4-162">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="b9bd4-162">Blob SnapshotTime</span></span>

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

### <span data-ttu-id="b9bd4-163">-VersionId</span><span class="sxs-lookup"><span data-stu-id="b9bd4-163">-VersionId</span></span>
<span data-ttu-id="b9bd4-164">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="b9bd4-164">Blob VersionId</span></span>

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

### <span data-ttu-id="b9bd4-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9bd4-165">-Confirm</span></span>
<span data-ttu-id="b9bd4-166">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9bd4-167">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b9bd4-167">-WhatIf</span></span>
<span data-ttu-id="b9bd4-168">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9bd4-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9bd4-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9bd4-170">CommonParameters</span></span>
<span data-ttu-id="b9bd4-171">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9bd4-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9bd4-172">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9bd4-172">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9bd4-173">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b9bd4-173">INPUTS</span></span>

### <span data-ttu-id="b9bd4-174">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b9bd4-174">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="b9bd4-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b9bd4-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="b9bd4-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b9bd4-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b9bd4-177">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b9bd4-177">OUTPUTS</span></span>

### <span data-ttu-id="b9bd4-178">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b9bd4-178">System.Boolean</span></span>

## <span data-ttu-id="b9bd4-179">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b9bd4-179">NOTES</span></span>

## <span data-ttu-id="b9bd4-180">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b9bd4-180">RELATED LINKS</span></span>

[<span data-ttu-id="b9bd4-181">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b9bd4-181">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="b9bd4-182">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b9bd4-182">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="b9bd4-183">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b9bd4-183">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
