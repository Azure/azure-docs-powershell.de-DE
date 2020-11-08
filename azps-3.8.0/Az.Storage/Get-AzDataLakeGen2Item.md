---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
ms.openlocfilehash: ffbfad973e881c3ae88e961517d097d7c8d6cedd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997007"
---
# <span data-ttu-id="4c825-101">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="4c825-101">Get-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="4c825-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4c825-102">SYNOPSIS</span></span>
<span data-ttu-id="4c825-103">Ruft die Details einer Datei oder eines Verzeichnisses in einem Dateisystem ab.</span><span class="sxs-lookup"><span data-stu-id="4c825-103">Gets the details of a file or directory in a filesystem.</span></span>

## <span data-ttu-id="4c825-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c825-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c825-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c825-105">DESCRIPTION</span></span>
<span data-ttu-id="4c825-106">Das Cmdlet " **Get-AzDataLakeGen2Item** " Ruft die Details einer Datei oder eines Verzeichnisses in einem Dateisystem in einem Azure Storage-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="4c825-106">The **Get-AzDataLakeGen2Item** cmdlet gets the details of a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="4c825-107">Dieses Cmdlet funktioniert nur, wenn der Hierarchical-Namespace für das Speicherkonto aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4c825-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="4c825-108">Diese Art von Konto kann erstellt werden, indem Sie das Cmdlet "New-AzStorageAccount" mit "-EnableHierarchicalNamespace $true" ausführen.</span><span class="sxs-lookup"><span data-stu-id="4c825-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="4c825-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c825-109">EXAMPLES</span></span>

### <span data-ttu-id="4c825-110">Beispiel 1: Abrufen eines Verzeichnisses aus einem Dateisystem und Anzeigen der Details</span><span class="sxs-lookup"><span data-stu-id="4c825-110">Example 1: Get a directory from a Filesystem, and show the details</span></span>
```
PS C:\> $dir1 = Get-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
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

<span data-ttu-id="4c825-111">Dieser Befehl ruft ein Verzeichnis aus einem Dateisystem ab und zeigt die Details an.</span><span class="sxs-lookup"><span data-stu-id="4c825-111">This command gets a directory from a Filesystem, and show the details.</span></span>

### <span data-ttu-id="4c825-112">Beispiel 2: Abrufen einer Datei aus einem Dateisystem</span><span class="sxs-lookup"><span data-stu-id="4c825-112">Example 2: Get a file from a Filesystem</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:20:37Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="4c825-113">Mit diesem Befehl werden die Details einer Datei aus einem Dateisystem abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4c825-113">This command gets the details of a file from a Filesystem.</span></span> 

## <span data-ttu-id="4c825-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c825-114">PARAMETERS</span></span>

### <span data-ttu-id="4c825-115">-Context</span><span class="sxs-lookup"><span data-stu-id="4c825-115">-Context</span></span>
<span data-ttu-id="4c825-116">Azure-Speicherkontext Objekt</span><span class="sxs-lookup"><span data-stu-id="4c825-116">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="4c825-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c825-117">-DefaultProfile</span></span>
<span data-ttu-id="4c825-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4c825-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c825-119">-Dateisystem</span><span class="sxs-lookup"><span data-stu-id="4c825-119">-FileSystem</span></span>
<span data-ttu-id="4c825-120">Dateisystemname</span><span class="sxs-lookup"><span data-stu-id="4c825-120">FileSystem name</span></span>

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

### <span data-ttu-id="4c825-121">-Path</span><span class="sxs-lookup"><span data-stu-id="4c825-121">-Path</span></span>
<span data-ttu-id="4c825-122">Der Pfad im angegebenen Dateisystem, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c825-122">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="4c825-123">Kann eine Datei oder ein Verzeichnis im Format "Verzeichnis/file.txt" oder "Verzeichnis1/directory2/" sein.</span><span class="sxs-lookup"><span data-stu-id="4c825-123">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="4c825-124">Geben Sie diesen Parameter nicht an, um das Stammverzeichnis des Dateisystems abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4c825-124">Not specify this parameter to get the root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="4c825-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c825-125">CommonParameters</span></span>
<span data-ttu-id="4c825-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c825-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c825-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c825-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c825-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4c825-128">INPUTS</span></span>

### <span data-ttu-id="4c825-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4c825-129">System.String</span></span>

### <span data-ttu-id="4c825-130">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4c825-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4c825-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4c825-131">OUTPUTS</span></span>

### <span data-ttu-id="4c825-132">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="4c825-132">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="4c825-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="4c825-133">NOTES</span></span>

## <span data-ttu-id="4c825-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4c825-134">RELATED LINKS</span></span>
