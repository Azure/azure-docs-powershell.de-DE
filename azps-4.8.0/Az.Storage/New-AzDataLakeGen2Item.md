---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
ms.openlocfilehash: 26f3dbc3462688458647e2e9676916063ffa3586
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165481"
---
# <span data-ttu-id="0aeb7-101">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="0aeb7-101">New-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="0aeb7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0aeb7-102">SYNOPSIS</span></span>
<span data-ttu-id="0aeb7-103">Erstellen Sie eine Datei oder ein Verzeichnis in einem Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-103">Create a file or directory in a filesystem.</span></span>

## <span data-ttu-id="0aeb7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0aeb7-104">SYNTAX</span></span>

### <span data-ttu-id="0aeb7-105">Datei (Standard)</span><span class="sxs-lookup"><span data-stu-id="0aeb7-105">File (Default)</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -Source <String> [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aeb7-106">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="0aeb7-106">Directory</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Directory] [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aeb7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0aeb7-107">DESCRIPTION</span></span>
<span data-ttu-id="0aeb7-108">Das Cmdlet **New-AzDataLakeGen2Item** erstellt eine Datei oder ein Verzeichnis in einem Dateisystem in einem Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-108">The **New-AzDataLakeGen2Item** cmdlet creates a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="0aeb7-109">Dieses Cmdlet funktioniert nur, wenn der Hierarchical-Namespace für das Speicherkonto aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="0aeb7-110">Diese Art von Konto kann erstellt werden, indem Sie das Cmdlet "New-AzStorageAccount" mit "-EnableHierarchicalNamespace $true" ausführen.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="0aeb7-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0aeb7-111">EXAMPLES</span></span>

### <span data-ttu-id="0aeb7-112">Beispiel 1: Erstellen eines Verzeichnisses mit der angegebenen Berechtigung, umask, Eigenschaften und Metadaten</span><span class="sxs-lookup"><span data-stu-id="0aeb7-112">Example 1: Create a directory with specified permission, Umask, properties, and metadata</span></span>
```
PS C:\>New-AzDataLakeGen2Item -FileSystem "testfilesystem" -Path "dir1/dir2/" -Directory -Permission rwxrwxrwx -Umask ---rw---- -Property @{"CacheControl" = "READ"; "ContentDisposition" = "True"} -Metadata  @{"tag1" = "value1"; "tag2" = "value2" }

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2            True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="0aeb7-113">Dieser Befehl erstellt ein Verzeichnis mit der angegebenen Berechtigung, umask, Eigenschaften und Metadaten.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-113">This command creates a directory with specified Permission, Umask, properties, and metadata</span></span>

### <span data-ttu-id="0aeb7-114">Beispiel 2: erstellen (hochladen) einer Data Lake-Datei aus einer lokalen Quelldatei und Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0aeb7-114">Example 2: Create(upload) a data lake file from a local source file, and the cmdlet runs in background</span></span>
```
PS C:\> $task = New-AzDataLakeGen2Item  -FileSystem "testfilesystem" -Path "dir1/dir2/file1" -Source "c:\sourcefile.txt" -Force -asjob
PS C:\> $task | Wait-Job
PS C:\> $task.Output

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group                
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2/file1      False        14400000        2020-03-23 09:19:13Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="0aeb7-115">Mit diesem Befehl wird eine Data Lake-Datei aus einer lokalen Quelldatei erstellt (hochgeladen), und das Cmdlet wird im Hintergrund ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-115">This command creates(upload) a data lake file from a local source file, and the cmdlet runs in background.</span></span>

## <span data-ttu-id="0aeb7-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="0aeb7-116">PARAMETERS</span></span>

### <span data-ttu-id="0aeb7-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0aeb7-117">-AsJob</span></span>
<span data-ttu-id="0aeb7-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0aeb7-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0aeb7-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0aeb7-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0aeb7-120">Der Gesamtumfang der gleichzeitigen asynchronen Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-120">The total amount of concurrent async tasks.</span></span> <span data-ttu-id="0aeb7-121">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-121">The default value is 10.</span></span>

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

### <span data-ttu-id="0aeb7-122">-Context</span><span class="sxs-lookup"><span data-stu-id="0aeb7-122">-Context</span></span>
<span data-ttu-id="0aeb7-123">Azure-Speicherkontext Objekt</span><span class="sxs-lookup"><span data-stu-id="0aeb7-123">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="0aeb7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aeb7-124">-DefaultProfile</span></span>
<span data-ttu-id="0aeb7-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0aeb7-126">-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="0aeb7-126">-Directory</span></span>
<span data-ttu-id="0aeb7-127">Gibt an, dass es sich bei diesem neuen Element um ein Verzeichnis und nicht um eine Datei handelt.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-127">Indicates that this new item is a directory and not a file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Directory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aeb7-128">-Dateisystem</span><span class="sxs-lookup"><span data-stu-id="0aeb7-128">-FileSystem</span></span>
<span data-ttu-id="0aeb7-129">Dateisystemname</span><span class="sxs-lookup"><span data-stu-id="0aeb7-129">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0aeb7-130">-Force</span><span class="sxs-lookup"><span data-stu-id="0aeb7-130">-Force</span></span>
<span data-ttu-id="0aeb7-131">Wenn übergeben, wird neues Element ohne Eingabeaufforderung erstellt</span><span class="sxs-lookup"><span data-stu-id="0aeb7-131">If passed then new item is created without any prompt</span></span>

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

### <span data-ttu-id="0aeb7-132">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="0aeb7-132">-Metadata</span></span>
<span data-ttu-id="0aeb7-133">Gibt Metadaten für das erstellte Verzeichnis oder die Datei an.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-133">Specifies metadata for the created directory or file.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aeb7-134">-Path</span><span class="sxs-lookup"><span data-stu-id="0aeb7-134">-Path</span></span>
<span data-ttu-id="0aeb7-135">Der Pfad im angegebenen Dateisystem, der erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-135">The path in the specified Filesystem that should be create.</span></span>
<span data-ttu-id="0aeb7-136">Kann eine Datei oder ein Verzeichnis im Format "Verzeichnis/file.txt" oder "Verzeichnis1/directory2/" sein.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-136">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0aeb7-137">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="0aeb7-137">-Permission</span></span>
<span data-ttu-id="0aeb7-138">Legt POSIX-Zugriffsberechtigungen für den Dateibesitzer, die Datei mit der besitzenden Gruppe und andere fest.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-138">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="0aeb7-139">Jeder Klasse kann eine Lese-, Schreib-oder Ausführungsberechtigung erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-139">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="0aeb7-140">Symbolic (rwxrw-RW-) wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-140">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="0aeb7-141">-Property</span><span class="sxs-lookup"><span data-stu-id="0aeb7-141">-Property</span></span>
<span data-ttu-id="0aeb7-142">Gibt Eigenschaften für das erstellte Verzeichnis oder die Datei an.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-142">Specifies properties for the created directory or file.</span></span> <span data-ttu-id="0aeb7-143">Die unterstützten Eigenschaften für File sind: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-143">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="0aeb7-144">Die unterstützten Eigenschaften für Directory sind: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-144">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aeb7-145">-Source</span><span class="sxs-lookup"><span data-stu-id="0aeb7-145">-Source</span></span>
<span data-ttu-id="0aeb7-146">Geben Sie den Pfad für die lokale Quelldatei an, der in eine datalake-Gen2-Datei hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-146">Specify the local source file path which will be upload to a Datalake Gen2 file.</span></span>

```yaml
Type: System.String
Parameter Sets: File
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0aeb7-147">-Umask</span><span class="sxs-lookup"><span data-stu-id="0aeb7-147">-Umask</span></span>
<span data-ttu-id="0aeb7-148">Wenn Sie ein neues Element erstellen und das übergeordnete Verzeichnis keine Standard-ACL hat, schränkt die umask die Berechtigungen für die zu erstellende Datei oder das Verzeichnis ein.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-148">When creating New Item and the parent directory does not have a default ACL, the umask restricts the permissions of the file or directory to be created.</span></span>
<span data-ttu-id="0aeb7-149">Die resultierende Berechtigung wird von p & ^ u angegeben, wobei p die Berechtigung und Sie die umask sind.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-149">The resulting permission is given by p & ^u, where p is the permission and u is the umask.</span></span>
<span data-ttu-id="0aeb7-150">Symbolic (rwxrw-RW-) wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-150">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="0aeb7-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0aeb7-151">-Confirm</span></span>
<span data-ttu-id="0aeb7-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aeb7-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aeb7-153">-WhatIf</span></span>
<span data-ttu-id="0aeb7-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aeb7-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aeb7-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aeb7-156">CommonParameters</span></span>
<span data-ttu-id="0aeb7-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0aeb7-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aeb7-158">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aeb7-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aeb7-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0aeb7-159">INPUTS</span></span>

### <span data-ttu-id="0aeb7-160">System. String</span><span class="sxs-lookup"><span data-stu-id="0aeb7-160">System.String</span></span>

### <span data-ttu-id="0aeb7-161">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0aeb7-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0aeb7-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0aeb7-162">OUTPUTS</span></span>

### <span data-ttu-id="0aeb7-163">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="0aeb7-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="0aeb7-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="0aeb7-164">NOTES</span></span>

## <span data-ttu-id="0aeb7-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0aeb7-165">RELATED LINKS</span></span>
