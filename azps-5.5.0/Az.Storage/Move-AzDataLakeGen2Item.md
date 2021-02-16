---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/move-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
ms.openlocfilehash: b8d46d85d00f00afdfa326b22a759f60af7b5bbe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163009"
---
# <span data-ttu-id="e654a-101">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="e654a-101">Move-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="e654a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e654a-102">SYNOPSIS</span></span>
<span data-ttu-id="e654a-103">Verschieben Sie eine Datei oder ein Verzeichnis in eine andere Datei oder ein Verzeichnis in demselben Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="e654a-103">Move a file or directory to another a file or directory in same Storage account.</span></span>

## <span data-ttu-id="e654a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e654a-104">SYNTAX</span></span>

### <span data-ttu-id="e654a-105">ReceiveManual (Standard)</span><span class="sxs-lookup"><span data-stu-id="e654a-105">ReceiveManual (Default)</span></span>
```
Move-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e654a-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="e654a-106">ItemPipeline</span></span>
```
Move-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e654a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e654a-107">DESCRIPTION</span></span>
<span data-ttu-id="e654a-108">Das **Cmdlet "Move-AzDataLakeGen2Item"** verschiebt eine Datei oder ein Verzeichnis in eine andere Datei oder ein Verzeichnis in demselben Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="e654a-108">The **Move-AzDataLakeGen2Item** cmdlet moves a a file or directory to another a file or directory in same Storage account.</span></span>
<span data-ttu-id="e654a-109">Dieses Cmdlet funktioniert nur, wenn der hierarchische Namespace für das Konto "Storage" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e654a-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="e654a-110">Diese Art von Konto kann durch Ausführen des Cmdlets "New-AzStorageAccount" mit "-EnableHierarchicalNamespace $true" erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e654a-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="e654a-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e654a-111">EXAMPLES</span></span>

### <span data-ttu-id="e654a-112">Beispiel 1: Verschieben einer Faltung im selben Dateisystem</span><span class="sxs-lookup"><span data-stu-id="e654a-112">Example 1: Move a fold in same Filesystem</span></span>
```
PS C:\> Move-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/" -DestFileSystem "filesystem1" -DestPath "dir3/"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir3                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="e654a-113">Mit diesem Befehl wird das Verzeichnis "dir1" in das Verzeichnis "dir3" im selben Dateisystem verschieben.</span><span class="sxs-lookup"><span data-stu-id="e654a-113">This command move directory 'dir1' to directory 'dir3' in the same Filesystem.</span></span>

### <span data-ttu-id="e654a-114">Beispiel 2: Verschieben einer Datei per Pipeline in ein anderes Dateisystem im gleichen Speicherkonto ohne Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="e654a-114">Example 2: Move a file by pipeline, to another Filesystem in the same Storage account without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" | Move-AzDataLakeGen2Item -DestFileSystem "filesystem2" -DestPath "dir2/file2" -Force

   FileSystem Name: filesystem2

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir2/file2           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="e654a-115">Mit diesem Befehl wird die Datei "dir1/file1" in "filesystem1" ohne Aufforderung in "dir2/file2" in "filesystem2" im selben Speicherkonto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e654a-115">This command move file 'dir1/file1' in 'filesystem1' to file 'dir2/file2' in 'filesystem2' in the same Storage account without prompt.</span></span>

## <span data-ttu-id="e654a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e654a-116">PARAMETERS</span></span>

### <span data-ttu-id="e654a-117">-Context</span><span class="sxs-lookup"><span data-stu-id="e654a-117">-Context</span></span>
<span data-ttu-id="e654a-118">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="e654a-118">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="e654a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e654a-119">-DefaultProfile</span></span>
<span data-ttu-id="e654a-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e654a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e654a-121">-DestFileSystem</span><span class="sxs-lookup"><span data-stu-id="e654a-121">-DestFileSystem</span></span>
<span data-ttu-id="e654a-122">Dest FileSystem name</span><span class="sxs-lookup"><span data-stu-id="e654a-122">Dest FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e654a-123">-DestPath</span><span class="sxs-lookup"><span data-stu-id="e654a-123">-DestPath</span></span>
<span data-ttu-id="e654a-124">Dest BLOB path</span><span class="sxs-lookup"><span data-stu-id="e654a-124">Dest Blob path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e654a-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="e654a-125">-FileSystem</span></span>
<span data-ttu-id="e654a-126">FileSystem name</span><span class="sxs-lookup"><span data-stu-id="e654a-126">FileSystem name</span></span>

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

### <span data-ttu-id="e654a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="e654a-127">-Force</span></span>
<span data-ttu-id="e654a-128">Erzwingen Sie das Überschreiben des Ziels.</span><span class="sxs-lookup"><span data-stu-id="e654a-128">Force to over write the destination.</span></span>

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

### <span data-ttu-id="e654a-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e654a-129">-InputObject</span></span>
<span data-ttu-id="e654a-130">Azure Datalake Gen2-Elementobjekt zum Verschieben.</span><span class="sxs-lookup"><span data-stu-id="e654a-130">Azure Datalake Gen2 Item Object to move from.</span></span>

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

### <span data-ttu-id="e654a-131">-Path</span><span class="sxs-lookup"><span data-stu-id="e654a-131">-Path</span></span>
<span data-ttu-id="e654a-132">Der Pfad im angegebenen Dateisystem, aus dem der Pfad entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e654a-132">The path in the specified Filesystem that should be move from.</span></span>
<span data-ttu-id="e654a-133">Kann eine Datei oder ein Verzeichnis im Format "Verzeichnis/file.txt" oder "Verzeichnis1/Verzeichnis2/" sein.</span><span class="sxs-lookup"><span data-stu-id="e654a-133">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="e654a-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e654a-134">-Confirm</span></span>
<span data-ttu-id="e654a-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e654a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e654a-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e654a-136">-WhatIf</span></span>
<span data-ttu-id="e654a-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e654a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e654a-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e654a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e654a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e654a-139">CommonParameters</span></span>
<span data-ttu-id="e654a-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e654a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e654a-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e654a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e654a-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e654a-142">INPUTS</span></span>

### <span data-ttu-id="e654a-143">System.String</span><span class="sxs-lookup"><span data-stu-id="e654a-143">System.String</span></span>

### <span data-ttu-id="e654a-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="e654a-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="e654a-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e654a-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e654a-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e654a-146">OUTPUTS</span></span>

### <span data-ttu-id="e654a-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="e654a-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="e654a-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e654a-148">NOTES</span></span>

## <span data-ttu-id="e654a-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e654a-149">RELATED LINKS</span></span>
