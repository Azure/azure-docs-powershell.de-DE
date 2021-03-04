---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
ms.openlocfilehash: 38e350f8dd4c6e8f37d75c8708387d5980e5cb84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935483"
---
# <span data-ttu-id="04721-101">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="04721-101">Get-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="04721-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04721-102">SYNOPSIS</span></span>
<span data-ttu-id="04721-103">Ruft die Details einer Datei oder eines Verzeichnisses in einem Dateisystem ab.</span><span class="sxs-lookup"><span data-stu-id="04721-103">Gets the details of a file or directory in a filesystem.</span></span>

## <span data-ttu-id="04721-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04721-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04721-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04721-105">DESCRIPTION</span></span>
<span data-ttu-id="04721-106">Das **Get-AzDataLakeGen2Item-Cmdlet** ruft die Details einer Datei oder eines Verzeichnisses in einem Dateisystem in einem Azure-Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="04721-106">The **Get-AzDataLakeGen2Item** cmdlet gets the details of a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="04721-107">Dieses Cmdlet funktioniert nur, wenn hierarchischer Namespace für das Speicherkonto aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="04721-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="04721-108">Diese Art von Konto kann durch Ausführen des Cmdlets "New-AzStorageAccount" mit "-EnableHierarchicalNamespace $true" erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="04721-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="04721-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="04721-109">EXAMPLES</span></span>

### <span data-ttu-id="04721-110">Beispiel 1: Herunterladen eines Verzeichnisses aus einem Dateisystem und Anzeigen der Details</span><span class="sxs-lookup"><span data-stu-id="04721-110">Example 1: Get a directory from a Filesystem, and show the details</span></span>
```
PS C:\> $dir1 = Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/"
PS C:\> $dir1

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser     
 
PS C:\WINDOWS\system32> $dir1.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      ---        
False        Other                      rwx      

PS C:\WINDOWS\system32> $dir1.Permissions

Owner        : Execute, Write, Read
Group        : None
Other        : Execute, Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\WINDOWS\system32> $dir1.Properties.Metadata

Key          Value 
---          ----- 
hdi_isfolder true  
tag1         value1
tag2         value2

PS C:\WINDOWS\system32> $dir1.Properties

LastModified          : 3/23/2020 9:15:56 AM +00:00
CreatedOn             : 3/23/2020 9:15:56 AM +00:00
Metadata              : {[hdi_isfolder, true], [tag1, value1], [tag2, value2]}
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
ContentLength         : 0
ContentType           : application/octet-stream
ETag                  : "0x8D7CF0ACBA35FA8"
ContentHash           : 
ContentEncoding       : UDF12
ContentDisposition    : 
ContentLanguage       : 
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

<span data-ttu-id="04721-111">Dieser Befehl ruft ein Verzeichnis aus einem Dateisystem ab und zeigt die Details an.</span><span class="sxs-lookup"><span data-stu-id="04721-111">This command gets a directory from a Filesystem, and show the details.</span></span>

### <span data-ttu-id="04721-112">Beispiel 2: Herunterladen einer Datei aus einem Dateisystem</span><span class="sxs-lookup"><span data-stu-id="04721-112">Example 2: Get a file from a Filesystem</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:20:37Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="04721-113">Dieser Befehl ruft die Details einer Datei aus einem Dateisystem ab.</span><span class="sxs-lookup"><span data-stu-id="04721-113">This command gets the details of a file from a Filesystem.</span></span> 

## <span data-ttu-id="04721-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="04721-114">PARAMETERS</span></span>

### <span data-ttu-id="04721-115">-Context</span><span class="sxs-lookup"><span data-stu-id="04721-115">-Context</span></span>
<span data-ttu-id="04721-116">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="04721-116">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="04721-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04721-117">-DefaultProfile</span></span>
<span data-ttu-id="04721-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="04721-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04721-119">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="04721-119">-FileSystem</span></span>
<span data-ttu-id="04721-120">Dateisystemname</span><span class="sxs-lookup"><span data-stu-id="04721-120">FileSystem name</span></span>

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

### <span data-ttu-id="04721-121">-Path</span><span class="sxs-lookup"><span data-stu-id="04721-121">-Path</span></span>
<span data-ttu-id="04721-122">Der Pfad im angegebenen Dateisystem, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="04721-122">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="04721-123">Kann eine Datei oder ein Verzeichnis im Format "verzeichnis/file.txt" oder "directory1/directory2/" sein.</span><span class="sxs-lookup"><span data-stu-id="04721-123">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="04721-124">Geben Sie diesen Parameter nicht an, um das Stammverzeichnis des Dateisystems zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="04721-124">Not specify this parameter to get the root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04721-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04721-125">CommonParameters</span></span>
<span data-ttu-id="04721-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04721-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04721-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04721-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04721-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="04721-128">INPUTS</span></span>

### <span data-ttu-id="04721-129">System.String</span><span class="sxs-lookup"><span data-stu-id="04721-129">System.String</span></span>

### <span data-ttu-id="04721-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="04721-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="04721-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="04721-131">OUTPUTS</span></span>

### <span data-ttu-id="04721-132">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="04721-132">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="04721-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="04721-133">NOTES</span></span>

## <span data-ttu-id="04721-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="04721-134">RELATED LINKS</span></span>
