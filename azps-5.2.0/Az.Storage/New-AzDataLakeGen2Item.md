---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
ms.openlocfilehash: 26f3dbc3462688458647e2e9676916063ffa3586
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304144"
---
# <span data-ttu-id="b1fb9-101">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="b1fb9-101">New-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="b1fb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="b1fb9-103">Erstellen Sie eine Datei oder ein Verzeichnis in einem Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-103">Create a file or directory in a filesystem.</span></span>

## <span data-ttu-id="b1fb9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1fb9-104">SYNTAX</span></span>

### <span data-ttu-id="b1fb9-105">Datei (Standard)</span><span class="sxs-lookup"><span data-stu-id="b1fb9-105">File (Default)</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -Source <String> [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1fb9-106">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="b1fb9-106">Directory</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Directory] [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1fb9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b1fb9-107">DESCRIPTION</span></span>
<span data-ttu-id="b1fb9-108">Das **Cmdlet "New-AzDataLakeGen2Item"** erstellt eine Datei oder ein Verzeichnis in einem Filesystem in einem Azure-Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-108">The **New-AzDataLakeGen2Item** cmdlet creates a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="b1fb9-109">Dieses Cmdlet funktioniert nur, wenn der hierarchische Namespace für das Konto "Storage" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="b1fb9-110">Diese Art von Konto kann durch Ausführen des Cmdlets "New-AzStorageAccount" mit "-EnableHierarchicalNamespace $true" erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="b1fb9-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b1fb9-111">EXAMPLES</span></span>

### <span data-ttu-id="b1fb9-112">Beispiel 1: Erstellen eines Verzeichnisses mit angegebenen Berechtigungen, Umask, Eigenschaften und Metadaten</span><span class="sxs-lookup"><span data-stu-id="b1fb9-112">Example 1: Create a directory with specified permission, Umask, properties, and metadata</span></span>
```
PS C:\>New-AzDataLakeGen2Item -FileSystem "testfilesystem" -Path "dir1/dir2/" -Directory -Permission rwxrwxrwx -Umask ---rw---- -Property @{"CacheControl" = "READ"; "ContentDisposition" = "True"} -Metadata  @{"tag1" = "value1"; "tag2" = "value2" }

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2            True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="b1fb9-113">Mit diesem Befehl wird ein Verzeichnis mit den angegebenen Berechtigungen, Umask, Eigenschaften und Metadaten erstellt.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-113">This command creates a directory with specified Permission, Umask, properties, and metadata</span></span>

### <span data-ttu-id="b1fb9-114">Beispiel 2: Erstellen(Hochladen) einer Datenseedatei aus einer lokalen Quelldatei, und das Cmdlet wird im Hintergrund ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-114">Example 2: Create(upload) a data lake file from a local source file, and the cmdlet runs in background</span></span>
```
PS C:\> $task = New-AzDataLakeGen2Item  -FileSystem "testfilesystem" -Path "dir1/dir2/file1" -Source "c:\sourcefile.txt" -Force -asjob
PS C:\> $task | Wait-Job
PS C:\> $task.Output

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group                
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2/file1      False        14400000        2020-03-23 09:19:13Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="b1fb9-115">Mit diesem Befehl wird eine Datenseedatei aus einer lokalen Quelldatei erstellt (hochgeladen), und das Cmdlet wird im Hintergrund ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-115">This command creates(upload) a data lake file from a local source file, and the cmdlet runs in background.</span></span>

## <span data-ttu-id="b1fb9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1fb9-116">PARAMETERS</span></span>

### <span data-ttu-id="b1fb9-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1fb9-117">-AsJob</span></span>
<span data-ttu-id="b1fb9-118">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b1fb9-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1fb9-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b1fb9-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b1fb9-120">Die Gesamtzahl paralleler asynchroner Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-120">The total amount of concurrent async tasks.</span></span> <span data-ttu-id="b1fb9-121">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-121">The default value is 10.</span></span>

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

### <span data-ttu-id="b1fb9-122">-Context</span><span class="sxs-lookup"><span data-stu-id="b1fb9-122">-Context</span></span>
<span data-ttu-id="b1fb9-123">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="b1fb9-123">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="b1fb9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1fb9-124">-DefaultProfile</span></span>
<span data-ttu-id="b1fb9-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1fb9-126">-Directory</span><span class="sxs-lookup"><span data-stu-id="b1fb9-126">-Directory</span></span>
<span data-ttu-id="b1fb9-127">Gibt an, dass es sich bei diesem neuen Element um ein Verzeichnis und nicht um eine Datei handelt.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-127">Indicates that this new item is a directory and not a file.</span></span>

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

### <span data-ttu-id="b1fb9-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="b1fb9-128">-FileSystem</span></span>
<span data-ttu-id="b1fb9-129">FileSystem name</span><span class="sxs-lookup"><span data-stu-id="b1fb9-129">FileSystem name</span></span>

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

### <span data-ttu-id="b1fb9-130">-Force</span><span class="sxs-lookup"><span data-stu-id="b1fb9-130">-Force</span></span>
<span data-ttu-id="b1fb9-131">Wenn übergeben, wird ein neues Element ohne Eingabeaufforderung erstellt.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-131">If passed then new item is created without any prompt</span></span>

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

### <span data-ttu-id="b1fb9-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b1fb9-132">-Metadata</span></span>
<span data-ttu-id="b1fb9-133">Gibt Metadaten für das erstellte Verzeichnis oder die erstellte Datei an.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-133">Specifies metadata for the created directory or file.</span></span>

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

### <span data-ttu-id="b1fb9-134">-Path</span><span class="sxs-lookup"><span data-stu-id="b1fb9-134">-Path</span></span>
<span data-ttu-id="b1fb9-135">Der Pfad im angegebenen Dateisystem, der erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-135">The path in the specified Filesystem that should be create.</span></span>
<span data-ttu-id="b1fb9-136">Kann eine Datei oder ein Verzeichnis im Format "Verzeichnis/file.txt" oder "Verzeichnis1/Verzeichnis2/" sein.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-136">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="b1fb9-137">-Permission</span><span class="sxs-lookup"><span data-stu-id="b1fb9-137">-Permission</span></span>
<span data-ttu-id="b1fb9-138">Legt die ZUGRIFFSBERECHTIGUNGEN von POSIX für den Dateibesitzer, die Gruppe, die die Datei besitzt, und andere Personen fest.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-138">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="b1fb9-139">Jeder Klasse können Lese-, Schreib- oder Ausführungsberechtigungen erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-139">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="b1fb9-140">Symbolisches (rwxrw-rw-) wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-140">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="b1fb9-141">-Property</span><span class="sxs-lookup"><span data-stu-id="b1fb9-141">-Property</span></span>
<span data-ttu-id="b1fb9-142">Gibt Eigenschaften für das erstellte Verzeichnis oder die erstellte Datei an.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-142">Specifies properties for the created directory or file.</span></span> <span data-ttu-id="b1fb9-143">Die unterstützten Eigenschaften für die Datei sind: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-143">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="b1fb9-144">Die unterstützten Eigenschaften für das Verzeichnis sind: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-144">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="b1fb9-145">-Source</span><span class="sxs-lookup"><span data-stu-id="b1fb9-145">-Source</span></span>
<span data-ttu-id="b1fb9-146">Geben Sie den lokalen Quelldateipfad an, der in eine Datalake Gen2-Datei hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-146">Specify the local source file path which will be upload to a Datalake Gen2 file.</span></span>

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

### <span data-ttu-id="b1fb9-147">-Umask</span><span class="sxs-lookup"><span data-stu-id="b1fb9-147">-Umask</span></span>
<span data-ttu-id="b1fb9-148">Wenn "Neues Element" erstellt wird und das übergeordnete Verzeichnis keine Standard-ACL hat, schränkt der Umask die Berechtigungen der zu erstellenden Datei oder des Verzeichnisses ein.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-148">When creating New Item and the parent directory does not have a default ACL, the umask restricts the permissions of the file or directory to be created.</span></span>
<span data-ttu-id="b1fb9-149">Die resultierende Berechtigung wird durch P & ^u erteilt, wobei p die Berechtigung ist und Sie die Umask sind.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-149">The resulting permission is given by p & ^u, where p is the permission and u is the umask.</span></span>
<span data-ttu-id="b1fb9-150">Symbolisches (rwxrw-rw-) wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-150">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="b1fb9-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1fb9-151">-Confirm</span></span>
<span data-ttu-id="b1fb9-152">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1fb9-153">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b1fb9-153">-WhatIf</span></span>
<span data-ttu-id="b1fb9-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1fb9-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1fb9-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1fb9-156">CommonParameters</span></span>
<span data-ttu-id="b1fb9-157">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1fb9-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1fb9-158">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1fb9-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1fb9-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b1fb9-159">INPUTS</span></span>

### <span data-ttu-id="b1fb9-160">System.String</span><span class="sxs-lookup"><span data-stu-id="b1fb9-160">System.String</span></span>

### <span data-ttu-id="b1fb9-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b1fb9-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b1fb9-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b1fb9-162">OUTPUTS</span></span>

### <span data-ttu-id="b1fb9-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="b1fb9-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="b1fb9-164">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b1fb9-164">NOTES</span></span>

## <span data-ttu-id="b1fb9-165">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b1fb9-165">RELATED LINKS</span></span>
