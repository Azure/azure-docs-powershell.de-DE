---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
ms.openlocfilehash: 6af68da41e1d5ea212d23d0cbc2296a68a6fa7e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176822"
---
# <span data-ttu-id="dabdd-101">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="dabdd-101">Update-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="dabdd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dabdd-102">SYNOPSIS</span></span>
<span data-ttu-id="dabdd-103">Aktualisieren Sie eine Datei oder ein Verzeichnis auf Eigenschaften, Metadaten, Berechtigung, ACL und Besitzer.</span><span class="sxs-lookup"><span data-stu-id="dabdd-103">Update a file or directory on properties, metadata, permission, ACL, and owner.</span></span>

## <span data-ttu-id="dabdd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dabdd-104">SYNTAX</span></span>

### <span data-ttu-id="dabdd-105">ReceiveManual (Standard)</span><span class="sxs-lookup"><span data-stu-id="dabdd-105">ReceiveManual (Default)</span></span>
```
Update-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dabdd-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="dabdd-106">ItemPipeline</span></span>
```
Update-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dabdd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dabdd-107">DESCRIPTION</span></span>
<span data-ttu-id="dabdd-108">Das Cmdlet **Update-AzDataLakeGen2Item** aktualisiert eine Datei oder ein Verzeichnis auf Eigenschaften, Metadaten, Berechtigung, ACL und Besitzer.</span><span class="sxs-lookup"><span data-stu-id="dabdd-108">The **Update-AzDataLakeGen2Item** cmdlet updates a file or directory on properties, metadata, permission, ACL, and owner.</span></span>
<span data-ttu-id="dabdd-109">Dieses Cmdlet funktioniert nur, wenn der Hierarchical-Namespace für das Speicherkonto aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="dabdd-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="dabdd-110">Diese Art von Konto kann erstellt werden, indem Sie das Cmdlet "New-AzStorageAccount" mit "-EnableHierarchicalNamespace $true" ausführen.</span><span class="sxs-lookup"><span data-stu-id="dabdd-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="dabdd-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dabdd-111">EXAMPLES</span></span>

### <span data-ttu-id="dabdd-112">Beispiel 1: Erstellen eines ACL-Objekts mit 3 ACL-Einträgen und Aktualisieren der ACL für alle Elemente in einem Dateisystem rekursiv</span><span class="sxs-lookup"><span data-stu-id="dabdd-112">Example 1: Create an ACL object with 3 ACL entry, and update ACL to all items in a Filesystem recursively</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Recurse | Update-AzDataLakeGen2Item -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser           
dir1/file1           False        1024            2020-03-23 09:29:18Z rwxrw-rw-    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="dabdd-113">Mit diesem Befehl wird zunächst ein ACL-Objekt mit 3 ACL-Eintrag (Use-Inputobject-Parameter zum Hinzufügen eines ACL-Eintrags zu einem vorhandenen ACL-Objekt) erstellt, dann alle Elemente in einem Dateisystem abgerufen und ACL für die Elemente aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="dabdd-113">This command first creates an ACL object with 3 acl entry (use -InputObject parameter to add acl entry to existing acl object), then get all items in a filesystem and update acl on the items.</span></span>

### <span data-ttu-id="dabdd-114">Beispiel 2: alle Eigenschaften einer Datei aktualisieren und anzeigen</span><span class="sxs-lookup"><span data-stu-id="dabdd-114">Example 2: Update all properties on a file, and show them</span></span>
```
PS C:\> $file = Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" `
                 -Acl $acl `
                 -Property @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="; "ContentEncoding" = "UDF8"; "CacheControl" = "READ"; "ContentDisposition" = "True"; "ContentLanguage" = "EN-US"} `
                 -Metadata  @{"tag1" = "value1"; "tag2" = "value2" } `
                 -Permission rw-rw-rwx `
                 -Owner '$superuser' `
                 -Group '$superuser'

PS C:\> $file

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser          

PS C:\> $file.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      rw-        
False        Other                      rw-        

PS C:\> $file.Permissions

Owner        : Execute, Write, Read
Group        : Write, Read
Other        : Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\> $file.Properties.Metadata

Key  Value 
---  ----- 
tag2 value2
tag1 value1

PS C:\> $file.Properties


LastModified          : 3/23/2020 9:57:33 AM +00:00
CreatedOn             : 3/23/2020 9:29:18 AM +00:00
Metadata              : {[tag2, value2], [tag1, value1]}
CopyCompletedOn       : 1/1/0001 12:00:00 AM +00:00
CopyStatusDescription : 
CopyId                : 
CopyProgress          : 
CopySource            : 
CopyStatus            : Pending
IsIncrementalCopy     : False
LeaseDuration         : Infinite
LeaseState            : Available
LeaseStatus           : Unlocked
ContentLength         : 1024
ContentType           : image/jpeg
ETag                  : "0x8D7CF109B9878CC"
ContentHash           : {139, 189, 187, 176...}
ContentEncoding       : UDF8
ContentDisposition    : True
ContentLanguage       : EN-US
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

<span data-ttu-id="dabdd-115">Mit diesem Befehl werden alle Eigenschaften einer Datei aktualisiert (ACL, Berechtigung, Besitzer, Gruppe, Metadaten, Eigenschaft können mit jedem conbination aktualisiert werden) und in der PowerShell-Konsole angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="dabdd-115">This command updates all properties on a file (ACL, permission,owner, group, metadata, property can be updated with any conbination), and show them in Powershell console.</span></span>

### <span data-ttu-id="dabdd-116">Beispiel 3: Hinzufügen eines ACL-Eintrags zu einem Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="dabdd-116">Example 3: Add an ACL entry to a directory</span></span>
```
## Get the origin ACL
PS C:\> $acl = (Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/').ACL

# Update permission of a new ACL entry (if ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry)
PS C:\> $acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rw- -InputObject $acl  

# set the new acl to the directory
PS C:\> update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/' -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

<span data-ttu-id="dabdd-117">Mit diesem Befehl wird ACL aus einem Verzeichnis abgerufen, ein ACL-Eintrag aktualisiert/hinzugefügt und auf das Verzeichnis zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="dabdd-117">This command gets ACL from a directory, updates/adds an ACL entry, and sets back to the directory.</span></span>
<span data-ttu-id="dabdd-118">Wenn der ACL-Eintrag mit demselben AccessControlType/Entity-DefaultScope nicht vorhanden ist, wird ein neuer ACL-Eintrag hinzugefügt, ansonsten Update-Berechtigung für vorhandenen ACL-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="dabdd-118">If ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="dabdd-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="dabdd-119">PARAMETERS</span></span>

### <span data-ttu-id="dabdd-120">-ACL</span><span class="sxs-lookup"><span data-stu-id="dabdd-120">-Acl</span></span>
<span data-ttu-id="dabdd-121">Legt POSIX-Zugriffssteuerungsrechte für Dateien und Verzeichnisse fest.</span><span class="sxs-lookup"><span data-stu-id="dabdd-121">Sets POSIX access control rights on files and directories.</span></span>
<span data-ttu-id="dabdd-122">Erstellen Sie dieses Objekt mit New-AzDataLakeGen2ItemAclObject.</span><span class="sxs-lookup"><span data-stu-id="dabdd-122">Create this object with New-AzDataLakeGen2ItemAclObject.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabdd-123">-Context</span><span class="sxs-lookup"><span data-stu-id="dabdd-123">-Context</span></span>
<span data-ttu-id="dabdd-124">Azure-Speicherkontext Objekt</span><span class="sxs-lookup"><span data-stu-id="dabdd-124">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="dabdd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dabdd-125">-DefaultProfile</span></span>
<span data-ttu-id="dabdd-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dabdd-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dabdd-127">-Dateisystem</span><span class="sxs-lookup"><span data-stu-id="dabdd-127">-FileSystem</span></span>
<span data-ttu-id="dabdd-128">Dateisystemname</span><span class="sxs-lookup"><span data-stu-id="dabdd-128">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dabdd-129">-Gruppe</span><span class="sxs-lookup"><span data-stu-id="dabdd-129">-Group</span></span>
<span data-ttu-id="dabdd-130">Legt die besitzende Gruppe des BLOBs fest.</span><span class="sxs-lookup"><span data-stu-id="dabdd-130">Sets the owning group of the blob.</span></span>

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

### <span data-ttu-id="dabdd-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dabdd-131">-InputObject</span></span>
<span data-ttu-id="dabdd-132">Azure datalake Gen2 zu aktualisierendes Element Objekt</span><span class="sxs-lookup"><span data-stu-id="dabdd-132">Azure Datalake Gen2 Item Object to update</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item
Parameter Sets: ItemPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dabdd-133">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="dabdd-133">-Metadata</span></span>
<span data-ttu-id="dabdd-134">Gibt Metadaten für das Verzeichnis oder die Datei an.</span><span class="sxs-lookup"><span data-stu-id="dabdd-134">Specifies metadata for the directory or file.</span></span>

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

### <span data-ttu-id="dabdd-135">-Besitzer</span><span class="sxs-lookup"><span data-stu-id="dabdd-135">-Owner</span></span>
<span data-ttu-id="dabdd-136">Legt den Besitzer des BLOB fest.</span><span class="sxs-lookup"><span data-stu-id="dabdd-136">Sets the owner of the blob.</span></span>

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

### <span data-ttu-id="dabdd-137">-Path</span><span class="sxs-lookup"><span data-stu-id="dabdd-137">-Path</span></span>
<span data-ttu-id="dabdd-138">Der Pfad im angegebenen Dateisystem, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="dabdd-138">The path in the specified Filesystem that should be updated.</span></span>
<span data-ttu-id="dabdd-139">Kann eine Datei oder ein Verzeichnis im Format "Verzeichnis/file.txt" oder "Verzeichnis1/directory2/" sein.</span><span class="sxs-lookup"><span data-stu-id="dabdd-139">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="dabdd-140">Nicht angeben dieser Parameter wird das Stammverzeichnis des Dateisystems aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="dabdd-140">Not specify this parameter will update the root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dabdd-141">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="dabdd-141">-Permission</span></span>
<span data-ttu-id="dabdd-142">Legt POSIX-Zugriffsberechtigungen für den Dateibesitzer, die Datei mit der besitzenden Gruppe und andere fest.</span><span class="sxs-lookup"><span data-stu-id="dabdd-142">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="dabdd-143">Jeder Klasse kann eine Lese-, Schreib-oder Ausführungsberechtigung erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="dabdd-143">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="dabdd-144">Symbolic (rwxrw-RW-) wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dabdd-144">Symbolic (rwxrw-rw-) is supported.</span></span>
<span data-ttu-id="dabdd-145">In Verbindung mit ACL ungültig.</span><span class="sxs-lookup"><span data-stu-id="dabdd-145">Invalid in conjunction with Acl.</span></span>

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

### <span data-ttu-id="dabdd-146">-Property</span><span class="sxs-lookup"><span data-stu-id="dabdd-146">-Property</span></span>
<span data-ttu-id="dabdd-147">Gibt Eigenschaften für das Verzeichnis oder die Datei an.</span><span class="sxs-lookup"><span data-stu-id="dabdd-147">Specifies properties for the directory or file.</span></span> <span data-ttu-id="dabdd-148">Die unterstützten Eigenschaften für File sind: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="dabdd-148">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="dabdd-149">Die unterstützten Eigenschaften für Directory sind: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="dabdd-149">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="dabdd-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dabdd-150">-Confirm</span></span>
<span data-ttu-id="dabdd-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dabdd-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dabdd-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dabdd-152">-WhatIf</span></span>
<span data-ttu-id="dabdd-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dabdd-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dabdd-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dabdd-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dabdd-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dabdd-155">CommonParameters</span></span>
<span data-ttu-id="dabdd-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dabdd-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dabdd-157">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dabdd-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dabdd-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dabdd-158">INPUTS</span></span>

### <span data-ttu-id="dabdd-159">System. String</span><span class="sxs-lookup"><span data-stu-id="dabdd-159">System.String</span></span>

### <span data-ttu-id="dabdd-160">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="dabdd-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="dabdd-161">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dabdd-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dabdd-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dabdd-162">OUTPUTS</span></span>

### <span data-ttu-id="dabdd-163">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="dabdd-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="dabdd-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="dabdd-164">NOTES</span></span>

## <span data-ttu-id="dabdd-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dabdd-165">RELATED LINKS</span></span>
