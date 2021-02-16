---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171468"
---
# <span data-ttu-id="5ff65-101">New-AzBatchResourceFile</span><span class="sxs-lookup"><span data-stu-id="5ff65-101">New-AzBatchResourceFile</span></span>

## <span data-ttu-id="5ff65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ff65-102">SYNOPSIS</span></span>
<span data-ttu-id="5ff65-103">Erstellt eine Ressourcendatei zur Verwendung durch `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="5ff65-103">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="5ff65-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ff65-104">SYNTAX</span></span>

### <span data-ttu-id="5ff65-105">HttpUrl (Standard)</span><span class="sxs-lookup"><span data-stu-id="5ff65-105">HttpUrl (Default)</span></span>
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ff65-106">StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="5ff65-106">StorageContainerUrl</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ff65-107">AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="5ff65-107">AutoStorageContainerName</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ff65-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ff65-108">DESCRIPTION</span></span>
<span data-ttu-id="5ff65-109">Erstellt eine Ressourcendatei zur Verwendung durch `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="5ff65-109">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="5ff65-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5ff65-110">EXAMPLES</span></span>

### <span data-ttu-id="5ff65-111">Beispiel 1: Erstellen einer Ressourcendatei aus einer HTTP-URL, die auf eine einzelne Datei zeigt</span><span class="sxs-lookup"><span data-stu-id="5ff65-111">Example 1: Create a resource file from an HTTP URL pointing at a single file</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="5ff65-112">Erstellt einen `PSResourceFile` Verweisen auf eine HTTP-URL.</span><span class="sxs-lookup"><span data-stu-id="5ff65-112">Creates a `PSResourceFile` referencing an HTTP url.</span></span>

### <span data-ttu-id="5ff65-113">Beispiel 2: Erstellen einer Ressourcendatei aus einer Azure Storage-Container-URL</span><span class="sxs-lookup"><span data-stu-id="5ff65-113">Example 2: Create a resource file from an Azure Storage container URL</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="5ff65-114">Erstellt einen `PSResourceFile` Verweisen auf eine Azure Storage-Container-URL.</span><span class="sxs-lookup"><span data-stu-id="5ff65-114">Creates a `PSResourceFile` referencing an Azure Storage container URL.</span></span> <span data-ttu-id="5ff65-115">Alle Dateien im Container werden in den angegebenen Ordner heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="5ff65-115">All files in the container will be downloaded to the specified folder.</span></span>

### <span data-ttu-id="5ff65-116">Beispiel 3: Erstellen einer Ressourcendatei aus einem Containernamen für den automatischen Speicher</span><span class="sxs-lookup"><span data-stu-id="5ff65-116">Example 3: Create a resource file from an Auto Storage container name</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="5ff65-117">Erstellt einen `PSResourceFile` Verweisen auf einen Containernamen für den automatischen Speicher.</span><span class="sxs-lookup"><span data-stu-id="5ff65-117">Creates a `PSResourceFile` referencing an Auto Storage container name.</span></span> <span data-ttu-id="5ff65-118">Alle Dateien im Container werden in den angegebenen Ordner heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="5ff65-118">All files in the container will be downloaded to the specified folder.</span></span>

## <span data-ttu-id="5ff65-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ff65-119">PARAMETERS</span></span>

### <span data-ttu-id="5ff65-120">-AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="5ff65-120">-AutoStorageContainerName</span></span>
<span data-ttu-id="5ff65-121">Der Name des Speichercontainers im Konto für den automatischen Speicher.</span><span class="sxs-lookup"><span data-stu-id="5ff65-121">The storage container name in the auto storage account.</span></span>

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

### <span data-ttu-id="5ff65-122">-BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="5ff65-122">-BlobPrefix</span></span>
<span data-ttu-id="5ff65-123">Ruft das BLOB-Präfix ab, das beim Herunterladen von Blobs aus einem Azure Storage-Container verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ff65-123">Gets the blob prefix to use when downloading blobs from an Azure Storage container.</span></span>
<span data-ttu-id="5ff65-124">Nur blobs, deren Namen mit dem angegebenen Präfix beginnen, werden heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="5ff65-124">Only the blobs whose names begin with the specified prefix will be downloaded.</span></span>
<span data-ttu-id="5ff65-125">Dieses Präfix kann ein Teildateiname oder ein Unterverzeichnis sein.</span><span class="sxs-lookup"><span data-stu-id="5ff65-125">This prefix can be a partial filename or a subdirectory.</span></span>
<span data-ttu-id="5ff65-126">Wenn kein Präfix angegeben ist, werden alle Dateien im Container heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="5ff65-126">If a prefix is not specified, all the files in the container will be downloaded.</span></span>

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

### <span data-ttu-id="5ff65-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ff65-127">-DefaultProfile</span></span>
<span data-ttu-id="5ff65-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5ff65-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ff65-129">-FileMode</span><span class="sxs-lookup"><span data-stu-id="5ff65-129">-FileMode</span></span>
<span data-ttu-id="5ff65-130">Ruft das Attribut für den Dateiberechtigungsmodus im oktalen Format ab.</span><span class="sxs-lookup"><span data-stu-id="5ff65-130">Gets the file permission mode attribute in octal format.</span></span>
<span data-ttu-id="5ff65-131">Diese Eigenschaft gilt nur, wenn die Ressourcendatei auf einen Linux-Knoten heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="5ff65-131">This property is applicable only if the resource file is downloaded to a Linux node.</span></span>
<span data-ttu-id="5ff65-132">Wenn diese Eigenschaft für einen Linux-Knoten nicht angegeben ist, ist der Standardwert 0770.</span><span class="sxs-lookup"><span data-stu-id="5ff65-132">If this property is not specified for a Linux node, then the default value is 0770.</span></span>

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

### <span data-ttu-id="5ff65-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="5ff65-133">-FilePath</span></span>
<span data-ttu-id="5ff65-134">Der Speicherort auf dem Berechnungsknoten, an den die Datei(en) heruntergeladen werden, relativ zum Arbeitsverzeichnis der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="5ff65-134">The location on the compute node to which to download the file(s), relative to the task's working directory.</span></span> <span data-ttu-id="5ff65-135">Wenn der Parameter "HttpUrl" angegeben wird, ist "FilePath" erforderlich und beschreibt den Pfad, auf den die Datei heruntergeladen wird, einschließlich des Dateinamens.</span><span class="sxs-lookup"><span data-stu-id="5ff65-135">If the HttpUrl parameter is specified, the FilePath is required and describes the path which the file will be downloaded to, including the filename.</span></span> <span data-ttu-id="5ff65-136">Wenn andernfalls die Parameter "AutoStorageContainerName" oder "StorageContainerUrl" angegeben werden, ist "FilePath" optional und das Verzeichnis, in das die Dateien heruntergeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5ff65-136">Otherwise, if the AutoStorageContainerName or StorageContainerUrl parameters are specified, FilePath is optional and is the directory to download the files to.</span></span> <span data-ttu-id="5ff65-137">In dem Fall, in dem FilePath als Verzeichnis verwendet wird, wird jede Verzeichnisstruktur, die den Eingabedaten bereits zugeordnet ist, vollständig aufbewahrt und an das angegebene Verzeichnis "FilePath" angefügt.</span><span class="sxs-lookup"><span data-stu-id="5ff65-137">In the case where FilePath is used as a directory, any directory structure already associated with the input data will be retained in full and appended to the specified FilePath directory.</span></span> <span data-ttu-id="5ff65-138">Der angegebene relative Pfad kann nicht aus dem Arbeitsverzeichnis des Vorgangs herausbrechen (z. B. mithilfe von '..').</span><span class="sxs-lookup"><span data-stu-id="5ff65-138">The specified relative path cannot break out of the task's working directory (for example by using '..').</span></span>

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

### <span data-ttu-id="5ff65-139">-HttpUrl</span><span class="sxs-lookup"><span data-stu-id="5ff65-139">-HttpUrl</span></span>
<span data-ttu-id="5ff65-140">Die URL der herunterzuladende Datei.</span><span class="sxs-lookup"><span data-stu-id="5ff65-140">The URL of the file to download.</span></span>
<span data-ttu-id="5ff65-141">Wenn es sich bei der URL um Azure Blob Storage handelt, muss sie über anonymen Zugriff lesbar sein. Das heißt, der Batchdienst stellt beim Herunterladen des BLOB keine Anmeldeinformationen bereit.</span><span class="sxs-lookup"><span data-stu-id="5ff65-141">If the URL is Azure Blob Storage, it must be readable using anonymous access; that is, the Batch service does not present any credentials when downloading the blob.</span></span>
<span data-ttu-id="5ff65-142">Es gibt zwei Möglichkeiten, eine solche URL für ein BLOB im Azure-Speicher zu erhalten: Fügen Sie eine SAS (Shared Access Signature) hinzu, die Leseberechtigungen für das BLOB erteilt, oder legen Sie die ACL für das BLOB oder seinen Container so ein, dass der öffentliche Zugriff zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="5ff65-142">There are two ways to get such a URL for a blob in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the blob, or set the ACL for the blob or its container to allow public access.</span></span>

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

### <span data-ttu-id="5ff65-143">-StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="5ff65-143">-StorageContainerUrl</span></span>
<span data-ttu-id="5ff65-144">Die URL des BLOB-Containers im Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="5ff65-144">The URL of the blob container within Azure Blob Storage.</span></span>
<span data-ttu-id="5ff65-145">Diese URL muss über anonymen Zugriff lesbar und auflistenbar sein. Das bedeutet, dass der Batchdienst beim Herunterladen von BLOBS aus dem Container keine Anmeldeinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="5ff65-145">This URL must be readable and listable using anonymous access; that is, the Batch service does not present any credentials when downloading blobs from the container.</span></span>
<span data-ttu-id="5ff65-146">Es gibt zwei Möglichkeiten zum Erhalten einer solchen URL für einen Container im Azure-Speicher: Fügen Sie eine SAS (Shared Access Signature) hinzu, die Leseberechtigungen für den Container erteilt, oder legen Sie die ACL für den Container so ein, dass der öffentliche Zugriff zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="5ff65-146">There are two ways to get such a URL for a container in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the container, or set the ACL for the container to allow public access.</span></span>

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

### <span data-ttu-id="5ff65-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ff65-147">CommonParameters</span></span>
<span data-ttu-id="5ff65-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ff65-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ff65-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ff65-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ff65-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5ff65-150">INPUTS</span></span>

### <span data-ttu-id="5ff65-151">Keine</span><span class="sxs-lookup"><span data-stu-id="5ff65-151">None</span></span>

## <span data-ttu-id="5ff65-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5ff65-152">OUTPUTS</span></span>

### <span data-ttu-id="5ff65-153">Microsoft.Azure.Commands.Batch. Models.PSResourceFile</span><span class="sxs-lookup"><span data-stu-id="5ff65-153">Microsoft.Azure.Commands.Batch.Models.PSResourceFile</span></span>

## <span data-ttu-id="5ff65-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5ff65-154">NOTES</span></span>

## <span data-ttu-id="5ff65-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5ff65-155">RELATED LINKS</span></span>

[<span data-ttu-id="5ff65-156">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5ff65-156">New-AzBatchTask</span></span>](./New-AzBatchTask.md)