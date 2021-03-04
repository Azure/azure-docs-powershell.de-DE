---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/copy-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Copy-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Copy-AzStorageBlob.md
ms.openlocfilehash: 76e89c90da10e8e232a564fb5fb7e5f8cc807327
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937307"
---
# <span data-ttu-id="6c151-101">Copy-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6c151-101">Copy-AzStorageBlob</span></span>

## <span data-ttu-id="6c151-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c151-102">SYNOPSIS</span></span>
<span data-ttu-id="6c151-103">Kopieren Sie einen Blob synchron.</span><span class="sxs-lookup"><span data-stu-id="6c151-103">Copy a blob synchronously.</span></span>

## <span data-ttu-id="6c151-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c151-104">SYNTAX</span></span>

### <span data-ttu-id="6c151-105">Containername (Standard)</span><span class="sxs-lookup"><span data-stu-id="6c151-105">ContainerName (Default)</span></span>
```
Copy-AzStorageBlob [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c151-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="6c151-106">BlobInstance</span></span>
```
Copy-AzStorageBlob [-BlobBaseClient <BlobBaseClient>] -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c151-107">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="6c151-107">UriPipeline</span></span>
```
Copy-AzStorageBlob -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c151-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c151-108">DESCRIPTION</span></span>
<span data-ttu-id="6c151-109">Das **Copy-AzStorageBlob-Cmdlet** kopiert einen Blob synchron und unterstützt derzeit nur block blob.</span><span class="sxs-lookup"><span data-stu-id="6c151-109">The **Copy-AzStorageBlob** cmdlet copies a blob synchronously, currently only support block blob.</span></span>

## <span data-ttu-id="6c151-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6c151-110">EXAMPLES</span></span>

### <span data-ttu-id="6c151-111">Beispiel 1: Kopieren eines benannten Blobs in einen anderen</span><span class="sxs-lookup"><span data-stu-id="6c151-111">Example 1: Copy a named blob to another</span></span>
```
C:\PS> $destBlob = Copy-AzStorageBlob -SrcContainer "sourcecontainername" -SrcBlob "srcblobname" -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="6c151-112">Mit diesem Befehl wird ein Blob aus dem Quellcontainer in den Zielcontainer mit einem neuen Blobnamen kopiert.</span><span class="sxs-lookup"><span data-stu-id="6c151-112">This command copies a blob from source container to the destination container with a new blob name.</span></span> 

### <span data-ttu-id="6c151-113">Beispiel 2: Kopieren eines Blobs aus einem Blobobjekt</span><span class="sxs-lookup"><span data-stu-id="6c151-113">Example 2: Copy blob from a blob object</span></span>
```
C:\PS> $srcBlob = Get-AzStorageBlob -Container $containerName -Blob $blobName  -Context $ctx 
C:\PS> $destBlob =  $srcBlob | Copy-AzStorageBlob  -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="6c151-114">Mit diesem Befehl wird ein Blob aus dem Quell-Blob-Objekt in den Zielcontainer mit einem neuen Blobnamen kopiert.</span><span class="sxs-lookup"><span data-stu-id="6c151-114">This command copies a blob from source blob object to the destination container with a new blob name.</span></span>

### <span data-ttu-id="6c151-115">Beispiel 3: Kopieren eines Blobs aus einem Blob-Uri</span><span class="sxs-lookup"><span data-stu-id="6c151-115">Example 3: Copy blob from a blob Uri</span></span>
```
C:\PS> $srcBlobUri = New-AzStorageBlobSASToken -Container $srcContainerName -Blob $srcBlobName -Permission rt -ExpiryTime (Get-Date).AddDays(7) -FullUri 
C:\PS> $destBlob = Copy-AzStorageBlob -AbsoluteUri $srcBlobUri -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="6c151-116">Der erste Befehl erstellt einen Blob-Uri des Quellblobs mit sas-Token der Berechtigung "rt".</span><span class="sxs-lookup"><span data-stu-id="6c151-116">The first command creates a blob Uri of the source blob, with sas token of permission "rt".</span></span> <span data-ttu-id="6c151-117">Der zweite Befehl kopiert den Quell-Blob-Uri in das Zielblob.</span><span class="sxs-lookup"><span data-stu-id="6c151-117">The second command copies from source blob Uri to the destination blob.</span></span>

### <span data-ttu-id="6c151-118">Beispiel 4: Aktualisieren eines Blockblobverschlüsselungsbereichs</span><span class="sxs-lookup"><span data-stu-id="6c151-118">Example 4: Update a block blob encryption scope</span></span>
```
C:\PS> $blob = Copy-AzStorageBlob -SrcContainer $containerName -SrcBlob $blobname -DestContainer $containername -EncryptionScope $newScopeName -Force
```

<span data-ttu-id="6c151-119">Mit diesem Befehl wird ein Blockblobverschlüsselungsbereich aktualisiert, indem er mit einem neuen Verschlüsselungsbereich in sich selbst kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="6c151-119">This command update a block blob encryption scope by copy it to itself with a new encryption scope.</span></span>

## <span data-ttu-id="6c151-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6c151-120">PARAMETERS</span></span>

### <span data-ttu-id="6c151-121">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="6c151-121">-AbsoluteUri</span></span>
<span data-ttu-id="6c151-122">Quell-Blob-URI</span><span class="sxs-lookup"><span data-stu-id="6c151-122">Source blob uri</span></span>

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c151-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c151-123">-AsJob</span></span>
<span data-ttu-id="6c151-124">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6c151-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c151-125">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="6c151-125">-BlobBaseClient</span></span>
<span data-ttu-id="6c151-126">BlobBaseClient-Objekt</span><span class="sxs-lookup"><span data-stu-id="6c151-126">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c151-127">-Context</span><span class="sxs-lookup"><span data-stu-id="6c151-127">-Context</span></span>
<span data-ttu-id="6c151-128">Source Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="6c151-128">Source Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c151-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c151-129">-DefaultProfile</span></span>
<span data-ttu-id="6c151-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c151-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c151-131">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="6c151-131">-DestBlob</span></span>
<span data-ttu-id="6c151-132">Name des Zielblobs</span><span class="sxs-lookup"><span data-stu-id="6c151-132">Destination blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c151-133">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="6c151-133">-DestContainer</span></span>
<span data-ttu-id="6c151-134">Name des Zielcontainers</span><span class="sxs-lookup"><span data-stu-id="6c151-134">Destination container name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c151-135">-DestContext</span><span class="sxs-lookup"><span data-stu-id="6c151-135">-DestContext</span></span>
<span data-ttu-id="6c151-136">Zielspeicherkontextobjekt</span><span class="sxs-lookup"><span data-stu-id="6c151-136">Destination Storage context object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c151-137">-EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="6c151-137">-EncryptionScope</span></span>
<span data-ttu-id="6c151-138">Verschlüsselungsbereich, der beim Erstellen von Anforderungen an den Dest-Blob verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c151-138">Encryption scope to be used when making requests to the dest blob.</span></span>

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

### <span data-ttu-id="6c151-139">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="6c151-139">-Force</span></span>
<span data-ttu-id="6c151-140">Erzwingen des Überschreibens des vorhandenen Blobs oder der vorhandenen Datei</span><span class="sxs-lookup"><span data-stu-id="6c151-140">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="6c151-141">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="6c151-141">-RehydratePriority</span></span>
<span data-ttu-id="6c151-142">Block Blob RehydratePriority.</span><span class="sxs-lookup"><span data-stu-id="6c151-142">Block Blob RehydratePriority.</span></span>
<span data-ttu-id="6c151-143">Gibt die Priorität an, mit der ein archiviertes Blob neu hydratisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c151-143">Indicates the priority with which to rehydrate an archived blob.</span></span>
<span data-ttu-id="6c151-144">Gültige Werte sind Hoch/Standard.</span><span class="sxs-lookup"><span data-stu-id="6c151-144">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:
Accepted values: Standard, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c151-145">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="6c151-145">-SrcBlob</span></span>
<span data-ttu-id="6c151-146">Blobname</span><span class="sxs-lookup"><span data-stu-id="6c151-146">Blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c151-147">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="6c151-147">-SrcContainer</span></span>
<span data-ttu-id="6c151-148">Name des Quellcontainers</span><span class="sxs-lookup"><span data-stu-id="6c151-148">Source Container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c151-149">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="6c151-149">-StandardBlobTier</span></span>
<span data-ttu-id="6c151-150">Block Blob Tier, gültige Werte sind Hot/Cool/Archive.</span><span class="sxs-lookup"><span data-stu-id="6c151-150">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="6c151-151">Details finden Sie unter https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="6c151-151">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool, Archive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c151-152">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6c151-152">-Confirm</span></span>
<span data-ttu-id="6c151-153">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6c151-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c151-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c151-154">-WhatIf</span></span>
<span data-ttu-id="6c151-155">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6c151-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c151-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c151-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c151-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c151-157">CommonParameters</span></span>
<span data-ttu-id="6c151-158">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c151-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c151-159">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c151-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c151-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6c151-160">INPUTS</span></span>

### <span data-ttu-id="6c151-161">Azure.Storage.Blobs.Specialized.BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="6c151-161">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="6c151-162">System.String</span><span class="sxs-lookup"><span data-stu-id="6c151-162">System.String</span></span>

### <span data-ttu-id="6c151-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6c151-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6c151-164">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6c151-164">OUTPUTS</span></span>

### <span data-ttu-id="6c151-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6c151-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="6c151-166">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6c151-166">NOTES</span></span>

## <span data-ttu-id="6c151-167">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6c151-167">RELATED LINKS</span></span>
