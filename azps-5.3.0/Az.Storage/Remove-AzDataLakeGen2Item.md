---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
ms.openlocfilehash: 06bb30dd98c491267675893192f61d4eb61529bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471704"
---
# <span data-ttu-id="822aa-101">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="822aa-101">Remove-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="822aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="822aa-102">SYNOPSIS</span></span>
<span data-ttu-id="822aa-103">Entfernen einer Datei oder eines Verzeichnisses</span><span class="sxs-lookup"><span data-stu-id="822aa-103">Remove a file or directory.</span></span>

## <span data-ttu-id="822aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="822aa-104">SYNTAX</span></span>

### <span data-ttu-id="822aa-105">ReceiveManual (Standard)</span><span class="sxs-lookup"><span data-stu-id="822aa-105">ReceiveManual (Default)</span></span>
```
Remove-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="822aa-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="822aa-106">ItemPipeline</span></span>
```
Remove-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="822aa-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="822aa-107">DESCRIPTION</span></span>
<span data-ttu-id="822aa-108">Das **Cmdlet "Remove-AzDataLakeGen2Item"** entfernt eine Datei oder ein Verzeichnis aus einem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="822aa-108">The **Remove-AzDataLakeGen2Item** cmdlet removes a file or directory from a Storage account.</span></span>
<span data-ttu-id="822aa-109">Dieses Cmdlet funktioniert nur, wenn der hierarchische Namespace für das Konto "Storage" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="822aa-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="822aa-110">Diese Art von Konto kann durch Ausführen des Cmdlets "New-AzStorageAccount" mit "-EnableHierarchicalNamespace $true" erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="822aa-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="822aa-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="822aa-111">EXAMPLES</span></span>

### <span data-ttu-id="822aa-112">Beispiel 1: Entfernen eines Verzeichnisses</span><span class="sxs-lookup"><span data-stu-id="822aa-112">Example 1: Removes a directory</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
```

<span data-ttu-id="822aa-113">Mit diesem Befehl wird ein Verzeichnis aus einem Dateisystem entfernt.</span><span class="sxs-lookup"><span data-stu-id="822aa-113">This command removes a directory from a Filesystem.</span></span>

### <span data-ttu-id="822aa-114">Beispiel 2: Entfernt eine Datei ohne Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="822aa-114">Example 2: Removes a file without prompt</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/file1" -Force
```

<span data-ttu-id="822aa-115">Mit diesem Befehl wird ein Verzeichnis ohne Eingabeaufforderung aus einem Dateisystem entfernt.</span><span class="sxs-lookup"><span data-stu-id="822aa-115">This command removes a directory from a Filesystem, without prompt.</span></span>

### <span data-ttu-id="822aa-116">Beispiel 3: Entfernen aller Elemente in einem Dateisystem mit Pipeline</span><span class="sxs-lookup"><span data-stu-id="822aa-116">Example 3: Remove all items in a Filesystem with pipeline</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" | Remove-AzDataLakeGen2Item -Force
```

<span data-ttu-id="822aa-117">Mit diesem Befehl werden alle Elemente in einem Dateisystem mit Pipeline entfernt.</span><span class="sxs-lookup"><span data-stu-id="822aa-117">This command removes all items in a Filesystem with pipeline.</span></span>

## <span data-ttu-id="822aa-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="822aa-118">PARAMETERS</span></span>

### <span data-ttu-id="822aa-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="822aa-119">-AsJob</span></span>
<span data-ttu-id="822aa-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="822aa-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="822aa-121">-Context</span><span class="sxs-lookup"><span data-stu-id="822aa-121">-Context</span></span>
<span data-ttu-id="822aa-122">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="822aa-122">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="822aa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="822aa-123">-DefaultProfile</span></span>
<span data-ttu-id="822aa-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="822aa-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="822aa-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="822aa-125">-FileSystem</span></span>
<span data-ttu-id="822aa-126">FileSystem name</span><span class="sxs-lookup"><span data-stu-id="822aa-126">FileSystem name</span></span>

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

### <span data-ttu-id="822aa-127">-Force</span><span class="sxs-lookup"><span data-stu-id="822aa-127">-Force</span></span>
<span data-ttu-id="822aa-128">Erzwingen, dass das Filesystem und alle Inhalte entfernt werden</span><span class="sxs-lookup"><span data-stu-id="822aa-128">Force to remove the Filesystem and all content in it</span></span>

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

### <span data-ttu-id="822aa-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="822aa-129">-InputObject</span></span>
<span data-ttu-id="822aa-130">Zu entfernende Azure Datalake Gen2-Elementobjekt.</span><span class="sxs-lookup"><span data-stu-id="822aa-130">Azure Datalake Gen2 Item Object to remove.</span></span>

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

### <span data-ttu-id="822aa-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="822aa-131">-PassThru</span></span>
<span data-ttu-id="822aa-132">Zurückgeben, ob das angegebene Dateisystem erfolgreich entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="822aa-132">Return whether the specified Filesystem is successfully removed</span></span>

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

### <span data-ttu-id="822aa-133">-Path</span><span class="sxs-lookup"><span data-stu-id="822aa-133">-Path</span></span>
<span data-ttu-id="822aa-134">Der Pfad im angegebenen Dateisystem, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="822aa-134">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="822aa-135">Kann eine Datei oder ein Verzeichnis im Format "Verzeichnis/file.txt" oder "Verzeichnis1/Verzeichnis2/" sein.</span><span class="sxs-lookup"><span data-stu-id="822aa-135">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="822aa-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="822aa-136">-Confirm</span></span>
<span data-ttu-id="822aa-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="822aa-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="822aa-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="822aa-138">-WhatIf</span></span>
<span data-ttu-id="822aa-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="822aa-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="822aa-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="822aa-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="822aa-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="822aa-141">CommonParameters</span></span>
<span data-ttu-id="822aa-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="822aa-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="822aa-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="822aa-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="822aa-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="822aa-144">INPUTS</span></span>

### <span data-ttu-id="822aa-145">System.String</span><span class="sxs-lookup"><span data-stu-id="822aa-145">System.String</span></span>

### <span data-ttu-id="822aa-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="822aa-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="822aa-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="822aa-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="822aa-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="822aa-148">OUTPUTS</span></span>

### <span data-ttu-id="822aa-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="822aa-149">System.Boolean</span></span>

## <span data-ttu-id="822aa-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="822aa-150">NOTES</span></span>

## <span data-ttu-id="822aa-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="822aa-151">RELATED LINKS</span></span>
