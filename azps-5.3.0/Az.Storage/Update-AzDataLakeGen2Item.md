---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
ms.openlocfilehash: 6af68da41e1d5ea212d23d0cbc2296a68a6fa7e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375975"
---
# <span data-ttu-id="46d83-101">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="46d83-101">Update-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="46d83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46d83-102">SYNOPSIS</span></span>
<span data-ttu-id="46d83-103">Aktualisieren sie eine Datei oder ein Verzeichnis für Eigenschaften, Metadaten, Berechtigungen, ACL und Besitzer.</span><span class="sxs-lookup"><span data-stu-id="46d83-103">Update a file or directory on properties, metadata, permission, ACL, and owner.</span></span>

## <span data-ttu-id="46d83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46d83-104">SYNTAX</span></span>

### <span data-ttu-id="46d83-105">ReceiveManual (Standard)</span><span class="sxs-lookup"><span data-stu-id="46d83-105">ReceiveManual (Default)</span></span>
```
Update-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46d83-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="46d83-106">ItemPipeline</span></span>
```
Update-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46d83-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46d83-107">DESCRIPTION</span></span>
<span data-ttu-id="46d83-108">Das **Cmdlet "Update-AzDataLakeGen2Item"** aktualisiert eine Datei oder ein Verzeichnis zu Eigenschaften, Metadaten, Berechtigungen, ACL und Besitzer.</span><span class="sxs-lookup"><span data-stu-id="46d83-108">The **Update-AzDataLakeGen2Item** cmdlet updates a file or directory on properties, metadata, permission, ACL, and owner.</span></span>
<span data-ttu-id="46d83-109">Dieses Cmdlet funktioniert nur, wenn der hierarchische Namespace für das Konto "Storage" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="46d83-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="46d83-110">Diese Art von Konto kann durch Ausführen des Cmdlets "New-AzStorageAccount" mit "-EnableHierarchicalNamespace $true" erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="46d83-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="46d83-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="46d83-111">EXAMPLES</span></span>

### <span data-ttu-id="46d83-112">Beispiel 1: Erstellen eines ACL-Objekts mit 3 ACL-Einträgen und rekursives Aktualisieren der ACL für alle Elemente in einem Filesystem</span><span class="sxs-lookup"><span data-stu-id="46d83-112">Example 1: Create an ACL object with 3 ACL entry, and update ACL to all items in a Filesystem recursively</span></span>
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

<span data-ttu-id="46d83-113">Dieser Befehl erstellt zuerst ein ACL-Objekt mit 3 acl-Eintrag (verwenden Sie den Parameter "-InputObject", um einem vorhandenen acl-Objekt einen Eintrag hinzuzufügen), dann alle Elemente in einem Dateisystem abzurufen und die Cl für die Elemente zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="46d83-113">This command first creates an ACL object with 3 acl entry (use -InputObject parameter to add acl entry to existing acl object), then get all items in a filesystem and update acl on the items.</span></span>

### <span data-ttu-id="46d83-114">Beispiel 2: Aktualisieren aller Eigenschaften einer Datei und Anzeigen dieser Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="46d83-114">Example 2: Update all properties on a file, and show them</span></span>
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

<span data-ttu-id="46d83-115">Dieser Befehl aktualisiert alle Eigenschaften einer Datei (ACL, Berechtigung, Besitzer, Gruppe, Metadaten, Eigenschaft kann mit beliebigen Konbinationen aktualisiert werden) und zeigt sie in der Powershell-Konsole an.</span><span class="sxs-lookup"><span data-stu-id="46d83-115">This command updates all properties on a file (ACL, permission,owner, group, metadata, property can be updated with any conbination), and show them in Powershell console.</span></span>

### <span data-ttu-id="46d83-116">Beispiel 3: Hinzufügen eines Eintrags "ACL" zu einem Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="46d83-116">Example 3: Add an ACL entry to a directory</span></span>
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

<span data-ttu-id="46d83-117">Dieser Befehl ruft eine ACL aus einem Verzeichnis ab, aktualisiert/fügt einen Eintrag für die ACL hinzu und legt die Synchronisierung auf das Verzeichnis zurück.</span><span class="sxs-lookup"><span data-stu-id="46d83-117">This command gets ACL from a directory, updates/adds an ACL entry, and sets back to the directory.</span></span>
<span data-ttu-id="46d83-118">Wenn der Eintrag "ACL" mit demselben AccessControlType/EntityId/DefaultScope nicht vorhanden ist, wird ein neuer "ACL"-Eintrag hinzugefügt, ansonsten wird die Berechtigung eines vorhandenen Eintrags für den Zugriffssteuerungszugriff (ACL) aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="46d83-118">If ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="46d83-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46d83-119">PARAMETERS</span></span>

### <span data-ttu-id="46d83-120">-Acl</span><span class="sxs-lookup"><span data-stu-id="46d83-120">-Acl</span></span>
<span data-ttu-id="46d83-121">Legt die Zugriffsrechte für POSIX für Dateien und Verzeichnisse fest.</span><span class="sxs-lookup"><span data-stu-id="46d83-121">Sets POSIX access control rights on files and directories.</span></span>
<span data-ttu-id="46d83-122">Erstellen Sie dieses Objekt mit "New-AzDataLakeGen2ItemAclObject".</span><span class="sxs-lookup"><span data-stu-id="46d83-122">Create this object with New-AzDataLakeGen2ItemAclObject.</span></span>

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

### <span data-ttu-id="46d83-123">-Context</span><span class="sxs-lookup"><span data-stu-id="46d83-123">-Context</span></span>
<span data-ttu-id="46d83-124">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="46d83-124">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="46d83-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d83-125">-DefaultProfile</span></span>
<span data-ttu-id="46d83-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46d83-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46d83-127">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="46d83-127">-FileSystem</span></span>
<span data-ttu-id="46d83-128">FileSystem name</span><span class="sxs-lookup"><span data-stu-id="46d83-128">FileSystem name</span></span>

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

### <span data-ttu-id="46d83-129">-Group</span><span class="sxs-lookup"><span data-stu-id="46d83-129">-Group</span></span>
<span data-ttu-id="46d83-130">Legt die besitzende Gruppe des BLOB fest.</span><span class="sxs-lookup"><span data-stu-id="46d83-130">Sets the owning group of the blob.</span></span>

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

### <span data-ttu-id="46d83-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46d83-131">-InputObject</span></span>
<span data-ttu-id="46d83-132">Zu aktualisierende Azure Datalake Gen2-Elementobjekt</span><span class="sxs-lookup"><span data-stu-id="46d83-132">Azure Datalake Gen2 Item Object to update</span></span>

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

### <span data-ttu-id="46d83-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="46d83-133">-Metadata</span></span>
<span data-ttu-id="46d83-134">Gibt die Metadaten für das Verzeichnis oder die Datei an.</span><span class="sxs-lookup"><span data-stu-id="46d83-134">Specifies metadata for the directory or file.</span></span>

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

### <span data-ttu-id="46d83-135">-Owner</span><span class="sxs-lookup"><span data-stu-id="46d83-135">-Owner</span></span>
<span data-ttu-id="46d83-136">Legt den Besitzer des BLOB fest.</span><span class="sxs-lookup"><span data-stu-id="46d83-136">Sets the owner of the blob.</span></span>

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

### <span data-ttu-id="46d83-137">-Path</span><span class="sxs-lookup"><span data-stu-id="46d83-137">-Path</span></span>
<span data-ttu-id="46d83-138">Der Pfad im angegebenen Dateisystem, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="46d83-138">The path in the specified Filesystem that should be updated.</span></span>
<span data-ttu-id="46d83-139">Kann eine Datei oder ein Verzeichnis im Format "Verzeichnis/file.txt" oder "Verzeichnis1/Verzeichnis2/" sein.</span><span class="sxs-lookup"><span data-stu-id="46d83-139">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="46d83-140">Wenn Sie diesen Parameter nicht angeben, wird das Stammverzeichnis des Filesystem aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="46d83-140">Not specify this parameter will update the root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="46d83-141">-Permission</span><span class="sxs-lookup"><span data-stu-id="46d83-141">-Permission</span></span>
<span data-ttu-id="46d83-142">Legt die POSIX-Zugriffsberechtigungen für den Dateibesitzer, die Gruppe, die besitzer der Datei ist, und andere Fest.</span><span class="sxs-lookup"><span data-stu-id="46d83-142">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="46d83-143">Jeder Klasse können Lese-, Schreib- oder Ausführungsberechtigungen erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="46d83-143">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="46d83-144">Symbolisches (rwxrw-rw-) wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="46d83-144">Symbolic (rwxrw-rw-) is supported.</span></span>
<span data-ttu-id="46d83-145">Ungültig in Verbindung mit "Acl"</span><span class="sxs-lookup"><span data-stu-id="46d83-145">Invalid in conjunction with Acl.</span></span>

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

### <span data-ttu-id="46d83-146">-Property</span><span class="sxs-lookup"><span data-stu-id="46d83-146">-Property</span></span>
<span data-ttu-id="46d83-147">Gibt Eigenschaften für das Verzeichnis oder die Datei an.</span><span class="sxs-lookup"><span data-stu-id="46d83-147">Specifies properties for the directory or file.</span></span> <span data-ttu-id="46d83-148">Die unterstützten Eigenschaften für die Datei sind: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="46d83-148">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="46d83-149">Die unterstützten Eigenschaften für das Verzeichnis sind: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="46d83-149">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="46d83-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46d83-150">-Confirm</span></span>
<span data-ttu-id="46d83-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46d83-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46d83-152">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="46d83-152">-WhatIf</span></span>
<span data-ttu-id="46d83-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46d83-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46d83-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46d83-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46d83-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d83-155">CommonParameters</span></span>
<span data-ttu-id="46d83-156">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46d83-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d83-157">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46d83-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d83-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="46d83-158">INPUTS</span></span>

### <span data-ttu-id="46d83-159">System.String</span><span class="sxs-lookup"><span data-stu-id="46d83-159">System.String</span></span>

### <span data-ttu-id="46d83-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="46d83-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="46d83-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="46d83-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="46d83-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="46d83-162">OUTPUTS</span></span>

### <span data-ttu-id="46d83-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="46d83-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="46d83-164">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="46d83-164">NOTES</span></span>

## <span data-ttu-id="46d83-165">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="46d83-165">RELATED LINKS</span></span>
