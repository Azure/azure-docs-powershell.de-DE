---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2itemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
ms.openlocfilehash: 9721305494ffd9b1d6a6f260008f050c9600437a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010393"
---
# <span data-ttu-id="87369-101">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="87369-101">Get-AzDataLakeGen2ItemContent</span></span>

## <span data-ttu-id="87369-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="87369-102">SYNOPSIS</span></span>
<span data-ttu-id="87369-103">Laden Sie eine Datei herunter.</span><span class="sxs-lookup"><span data-stu-id="87369-103">Download a file.</span></span>

## <span data-ttu-id="87369-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="87369-104">SYNTAX</span></span>

### <span data-ttu-id="87369-105">ReceiveManual (Standard)</span><span class="sxs-lookup"><span data-stu-id="87369-105">ReceiveManual (Default)</span></span>
```
Get-AzDataLakeGen2ItemContent [-FileSystem] <String> [-Path] <String> [-Destination <String>] [-CheckMd5]
 [-Force] [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87369-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="87369-106">ItemPipeline</span></span>
```
Get-AzDataLakeGen2ItemContent -InputObject <AzureDataLakeGen2Item> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87369-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87369-107">DESCRIPTION</span></span>
<span data-ttu-id="87369-108">Mit dem Cmdlet **Get-AzDataLakeGen2ItemContent können Sie** eine Datei in einem Dateisystem in einem Azure-Speicherkonto herunterladen.</span><span class="sxs-lookup"><span data-stu-id="87369-108">The **Get-AzDataLakeGen2ItemContent** cmdlet download a file in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="87369-109">Dieses Cmdlet funktioniert nur, wenn der Hierarchical-Namespace für das Speicherkonto aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="87369-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="87369-110">Diese Art von Konto kann erstellt werden, indem Sie das Cmdlet "New-AzStorageAccount" mit "-EnableHierarchicalNamespace $true" ausführen.</span><span class="sxs-lookup"><span data-stu-id="87369-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="87369-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87369-111">EXAMPLES</span></span>

### <span data-ttu-id="87369-112">Beispiel 1: Herunterladen einer Datei ohne Aufforderung</span><span class="sxs-lookup"><span data-stu-id="87369-112">Example 1: Download a file without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2ItemContent -FileSystem "filesystem1" -Path "dir1/file1" -Destination $localDestFile -Force

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="87369-113">Mit diesem Befehl wird eine Datei ohne Aufforderung in eine lokale Datei heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="87369-113">This command downloads a file to a local file without prompt.</span></span>

### <span data-ttu-id="87369-114">Beispiel 2: Abrufen einer Datei und anschließende Pipeline zum Herunterladen der Datei in eine lokale Datei</span><span class="sxs-lookup"><span data-stu-id="87369-114">Example 2: Get a file, then pipeline to download the file to a local file</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" |  Get-AzDataLakeGen2ItemContent -Destination $localDestFile 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="87369-115">Dieser Befehl ruft zuerst eine Datei und dann Pipeline ab, um die Datei in eine lokale Datei herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="87369-115">This command first gets a file, then pipeline to download the file to a local file.</span></span>

## <span data-ttu-id="87369-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="87369-116">PARAMETERS</span></span>

### <span data-ttu-id="87369-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87369-117">-AsJob</span></span>
<span data-ttu-id="87369-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="87369-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="87369-119">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="87369-119">-CheckMd5</span></span>
<span data-ttu-id="87369-120">Überprüfen der md5sum</span><span class="sxs-lookup"><span data-stu-id="87369-120">check the md5sum</span></span>

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

### <span data-ttu-id="87369-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="87369-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="87369-122">Der Gesamtumfang der gleichzeitigen asynchronen Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="87369-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="87369-123">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="87369-123">The default value is 10.</span></span>

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

### <span data-ttu-id="87369-124">-Context</span><span class="sxs-lookup"><span data-stu-id="87369-124">-Context</span></span>
<span data-ttu-id="87369-125">Azure-Speicherkontext Objekt</span><span class="sxs-lookup"><span data-stu-id="87369-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="87369-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87369-126">-DefaultProfile</span></span>
<span data-ttu-id="87369-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="87369-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87369-128">-Ziel</span><span class="sxs-lookup"><span data-stu-id="87369-128">-Destination</span></span>
<span data-ttu-id="87369-129">Ziel lokaler Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="87369-129">Destination local file path.</span></span>

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

### <span data-ttu-id="87369-130">-Dateisystem</span><span class="sxs-lookup"><span data-stu-id="87369-130">-FileSystem</span></span>
<span data-ttu-id="87369-131">Dateisystemname</span><span class="sxs-lookup"><span data-stu-id="87369-131">FileSystem name</span></span>

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

### <span data-ttu-id="87369-132">-Force</span><span class="sxs-lookup"><span data-stu-id="87369-132">-Force</span></span>
<span data-ttu-id="87369-133">Erzwingen, dass das vorhandene BLOB oder die vorhandene Datei überschrieben wird</span><span class="sxs-lookup"><span data-stu-id="87369-133">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="87369-134">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="87369-134">-InputObject</span></span>
<span data-ttu-id="87369-135">Azure datalake Gen2-Element Objekt, das heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="87369-135">Azure Datalake Gen2 Item Object to download.</span></span>

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

### <span data-ttu-id="87369-136">-Path</span><span class="sxs-lookup"><span data-stu-id="87369-136">-Path</span></span>
<span data-ttu-id="87369-137">Der Pfad im angegebenen Dateisystem, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="87369-137">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="87369-138">Kann eine Datei oder ein Verzeichnis im Format "Verzeichnis/file.txt" oder "Verzeichnis1/directory2/" sein.</span><span class="sxs-lookup"><span data-stu-id="87369-138">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87369-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="87369-139">-Confirm</span></span>
<span data-ttu-id="87369-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="87369-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87369-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87369-141">-WhatIf</span></span>
<span data-ttu-id="87369-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87369-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87369-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87369-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87369-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87369-144">CommonParameters</span></span>
<span data-ttu-id="87369-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87369-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87369-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87369-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87369-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="87369-147">INPUTS</span></span>

### <span data-ttu-id="87369-148">System. String</span><span class="sxs-lookup"><span data-stu-id="87369-148">System.String</span></span>

### <span data-ttu-id="87369-149">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="87369-149">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="87369-150">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="87369-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="87369-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="87369-151">OUTPUTS</span></span>

### <span data-ttu-id="87369-152">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="87369-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="87369-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="87369-153">NOTES</span></span>

## <span data-ttu-id="87369-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="87369-154">RELATED LINKS</span></span>
