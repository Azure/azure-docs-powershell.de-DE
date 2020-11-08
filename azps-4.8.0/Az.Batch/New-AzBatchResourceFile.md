---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167302"
---
# <span data-ttu-id="3e582-101">New-AzBatchResourceFile</span><span class="sxs-lookup"><span data-stu-id="3e582-101">New-AzBatchResourceFile</span></span>

## <span data-ttu-id="3e582-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3e582-102">SYNOPSIS</span></span>
<span data-ttu-id="3e582-103">Erstellt eine Ressourcendatei zur Verwendung durch `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="3e582-103">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="3e582-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e582-104">SYNTAX</span></span>

### <span data-ttu-id="3e582-105">HttpUrl (Standard)</span><span class="sxs-lookup"><span data-stu-id="3e582-105">HttpUrl (Default)</span></span>
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e582-106">StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="3e582-106">StorageContainerUrl</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e582-107">AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="3e582-107">AutoStorageContainerName</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e582-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e582-108">DESCRIPTION</span></span>
<span data-ttu-id="3e582-109">Erstellt eine Ressourcendatei zur Verwendung durch `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="3e582-109">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="3e582-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e582-110">EXAMPLES</span></span>

### <span data-ttu-id="3e582-111">Beispiel 1: Erstellen einer Ressourcendatei aus einer HTTP-URL, die auf eine einzelne Datei zeigt</span><span class="sxs-lookup"><span data-stu-id="3e582-111">Example 1: Create a resource file from an HTTP URL pointing at a single file</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="3e582-112">Erstellt einen `PSResourceFile` Verweis auf eine HTTP-URL.</span><span class="sxs-lookup"><span data-stu-id="3e582-112">Creates a `PSResourceFile` referencing an HTTP url.</span></span>

### <span data-ttu-id="3e582-113">Beispiel 2: Erstellen einer Ressourcendatei aus einer Azure-Speichercontainer-URL</span><span class="sxs-lookup"><span data-stu-id="3e582-113">Example 2: Create a resource file from an Azure Storage container URL</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="3e582-114">Erstellt einen `PSResourceFile` Verweis auf eine Azure-Speichercontainer-URL.</span><span class="sxs-lookup"><span data-stu-id="3e582-114">Creates a `PSResourceFile` referencing an Azure Storage container URL.</span></span> <span data-ttu-id="3e582-115">Alle Dateien im Container werden in den angegebenen Ordner heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="3e582-115">All files in the container will be downloaded to the specified folder.</span></span>

### <span data-ttu-id="3e582-116">Beispiel 3: Erstellen einer Ressourcendatei aus dem Namen eines automatischen Speichercontainers</span><span class="sxs-lookup"><span data-stu-id="3e582-116">Example 3: Create a resource file from an Auto Storage container name</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="3e582-117">Erstellt einen `PSResourceFile` Verweis auf den Namen eines automatischen Speichercontainers.</span><span class="sxs-lookup"><span data-stu-id="3e582-117">Creates a `PSResourceFile` referencing an Auto Storage container name.</span></span> <span data-ttu-id="3e582-118">Alle Dateien im Container werden in den angegebenen Ordner heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="3e582-118">All files in the container will be downloaded to the specified folder.</span></span>

## <span data-ttu-id="3e582-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e582-119">PARAMETERS</span></span>

### <span data-ttu-id="3e582-120">-AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="3e582-120">-AutoStorageContainerName</span></span>
<span data-ttu-id="3e582-121">Der Name des Speichercontainers im Auto Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="3e582-121">The storage container name in the auto storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AutoStorageContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e582-122">-BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="3e582-122">-BlobPrefix</span></span>
<span data-ttu-id="3e582-123">Ruft das BLOB-Präfix ab, das verwendet werden soll, wenn BLOBs aus einem Azure-Speichercontainer heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="3e582-123">Gets the blob prefix to use when downloading blobs from an Azure Storage container.</span></span>
<span data-ttu-id="3e582-124">Es werden nur die BLOBs heruntergeladen, deren Namen mit dem angegebenen Präfix beginnen.</span><span class="sxs-lookup"><span data-stu-id="3e582-124">Only the blobs whose names begin with the specified prefix will be downloaded.</span></span>
<span data-ttu-id="3e582-125">Bei diesem Präfix kann es sich um einen partiellen Dateinamen oder ein Unterverzeichnis handeln.</span><span class="sxs-lookup"><span data-stu-id="3e582-125">This prefix can be a partial filename or a subdirectory.</span></span>
<span data-ttu-id="3e582-126">Wenn kein Präfix angegeben ist, werden alle Dateien im Container heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="3e582-126">If a prefix is not specified, all the files in the container will be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e582-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e582-127">-DefaultProfile</span></span>
<span data-ttu-id="3e582-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3e582-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e582-129">-FileMode</span><span class="sxs-lookup"><span data-stu-id="3e582-129">-FileMode</span></span>
<span data-ttu-id="3e582-130">Ruft das Attribut "Datei-Berechtigungsmodus" im oktalen Format ab.</span><span class="sxs-lookup"><span data-stu-id="3e582-130">Gets the file permission mode attribute in octal format.</span></span>
<span data-ttu-id="3e582-131">Diese Eigenschaft gilt nur, wenn die Ressourcendatei auf einen Linux-Knoten heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="3e582-131">This property is applicable only if the resource file is downloaded to a Linux node.</span></span>
<span data-ttu-id="3e582-132">Wenn diese Eigenschaft für einen Linux-Knoten nicht angegeben ist, lautet der Standardwert 0770.</span><span class="sxs-lookup"><span data-stu-id="3e582-132">If this property is not specified for a Linux node, then the default value is 0770.</span></span>

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

### <span data-ttu-id="3e582-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="3e582-133">-FilePath</span></span>
<span data-ttu-id="3e582-134">Die Position auf dem Compute-Knoten, an den die Datei (en) bezogen auf das Arbeitsverzeichnis der Aufgabe heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3e582-134">The location on the compute node to which to download the file(s), relative to the task's working directory.</span></span> <span data-ttu-id="3e582-135">Wenn der HttpUrl-Parameter angegeben wird, ist der Dateipfad erforderlich und beschreibt den Pfad, in den die Datei heruntergeladen wird, einschließlich des Datei namens.</span><span class="sxs-lookup"><span data-stu-id="3e582-135">If the HttpUrl parameter is specified, the FilePath is required and describes the path which the file will be downloaded to, including the filename.</span></span> <span data-ttu-id="3e582-136">Wenn andernfalls die AutoStorageContainerName-oder StorageContainerUrl-Parameter angegeben werden, ist filePath optional und das Verzeichnis, in das die Dateien heruntergeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3e582-136">Otherwise, if the AutoStorageContainerName or StorageContainerUrl parameters are specified, FilePath is optional and is the directory to download the files to.</span></span> <span data-ttu-id="3e582-137">In dem Fall, in dem filePath als Verzeichnis verwendet wird, wird jede Verzeichnisstruktur, die den Eingabedaten bereits zugeordnet ist, vollständig aufbewahrt und an das angegebene filePath-Verzeichnis angefügt.</span><span class="sxs-lookup"><span data-stu-id="3e582-137">In the case where FilePath is used as a directory, any directory structure already associated with the input data will be retained in full and appended to the specified FilePath directory.</span></span> <span data-ttu-id="3e582-138">Der angegebene relative Pfad kann nicht aus dem Arbeitsverzeichnis des Vorgangs ausbrechen (beispielsweise mit "..").</span><span class="sxs-lookup"><span data-stu-id="3e582-138">The specified relative path cannot break out of the task's working directory (for example by using '..').</span></span>

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e582-139">-HttpUrl</span><span class="sxs-lookup"><span data-stu-id="3e582-139">-HttpUrl</span></span>
<span data-ttu-id="3e582-140">Die URL der Datei, die heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3e582-140">The URL of the file to download.</span></span>
<span data-ttu-id="3e582-141">Wenn die URL Azure-BLOB-Speicher ist, muss Sie mithilfe des anonymen Zugriffs lesbar sein. Das bedeutet, dass der Batch Dienst beim Herunterladen des BLOBs keine Anmeldeinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="3e582-141">If the URL is Azure Blob Storage, it must be readable using anonymous access; that is, the Batch service does not present any credentials when downloading the blob.</span></span>
<span data-ttu-id="3e582-142">Es gibt zwei Möglichkeiten zum Abrufen einer solchen URL für ein BLOB im Azure-Speicher: Fügen Sie eine freigegebene zugriffssignatur (SAS) mit Leseberechtigungen für das BLOB hinzu, oder legen Sie die ACL für das BLOB oder dessen Container so ein, dass der öffentliche Zugriff zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="3e582-142">There are two ways to get such a URL for a blob in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the blob, or set the ACL for the blob or its container to allow public access.</span></span>

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e582-143">-StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="3e582-143">-StorageContainerUrl</span></span>
<span data-ttu-id="3e582-144">Die URL des BLOB-Containers im Azure BLOB-Speicher.</span><span class="sxs-lookup"><span data-stu-id="3e582-144">The URL of the blob container within Azure Blob Storage.</span></span>
<span data-ttu-id="3e582-145">Diese URL muss mithilfe des anonymen Zugriffs lesbar und listenbar sein. Das bedeutet, dass der Batch Dienst beim Herunterladen von BLOBs aus dem Container keine Anmeldeinformationen darstellt.</span><span class="sxs-lookup"><span data-stu-id="3e582-145">This URL must be readable and listable using anonymous access; that is, the Batch service does not present any credentials when downloading blobs from the container.</span></span>
<span data-ttu-id="3e582-146">Es gibt zwei Möglichkeiten zum Abrufen einer solchen URL für einen Container im Azure-Speicher: Fügen Sie eine freigegebene zugriffssignatur (SAS) mit Leseberechtigungen für den Container hinzu, oder legen Sie die ACL für den Container so ein, dass der öffentliche Zugriff zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="3e582-146">There are two ways to get such a URL for a container in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the container, or set the ACL for the container to allow public access.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e582-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e582-147">CommonParameters</span></span>
<span data-ttu-id="3e582-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e582-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e582-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e582-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e582-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3e582-150">INPUTS</span></span>

### <span data-ttu-id="3e582-151">Keine</span><span class="sxs-lookup"><span data-stu-id="3e582-151">None</span></span>

## <span data-ttu-id="3e582-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3e582-152">OUTPUTS</span></span>

### <span data-ttu-id="3e582-153">Microsoft.Azure.Commands.Batch. Models. PSResourceFile</span><span class="sxs-lookup"><span data-stu-id="3e582-153">Microsoft.Azure.Commands.Batch.Models.PSResourceFile</span></span>

## <span data-ttu-id="3e582-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="3e582-154">NOTES</span></span>

## <span data-ttu-id="3e582-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3e582-155">RELATED LINKS</span></span>

[<span data-ttu-id="3e582-156">Neu – AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3e582-156">New-AzBatchTask</span></span>](./New-AzBatchTask.md)