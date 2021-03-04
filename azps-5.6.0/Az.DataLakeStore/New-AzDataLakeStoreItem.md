---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: 46495d5a057de6c7cff21cdc09fe68d80e0c4da7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938832"
---
# <span data-ttu-id="82989-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82989-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="82989-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82989-102">SYNOPSIS</span></span>
<span data-ttu-id="82989-103">Erstellt eine neue Datei oder einen neuen Ordner im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="82989-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="82989-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82989-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82989-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82989-105">DESCRIPTION</span></span>
<span data-ttu-id="82989-106">Das **Cmdlet New-AzDataLakeStoreItem** erstellt eine neue Datei oder einen neuen Ordner im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="82989-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="82989-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="82989-107">EXAMPLES</span></span>

### <span data-ttu-id="82989-108">Beispiel 1: Erstellen einer neuen Datei und eines neuen Ordners</span><span class="sxs-lookup"><span data-stu-id="82989-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="82989-109">Mit dem ersten Befehl wird die Datei NewFile.txt für das angegebene Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="82989-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="82989-110">Mit dem zweiten Befehl wird der Ordner NewFolder im Stammordner erstellt.</span><span class="sxs-lookup"><span data-stu-id="82989-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="82989-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="82989-111">PARAMETERS</span></span>

### <span data-ttu-id="82989-112">-Konto</span><span class="sxs-lookup"><span data-stu-id="82989-112">-Account</span></span>
<span data-ttu-id="82989-113">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="82989-113">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82989-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82989-114">-DefaultProfile</span></span>
<span data-ttu-id="82989-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82989-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82989-116">-Encoding</span><span class="sxs-lookup"><span data-stu-id="82989-116">-Encoding</span></span>
<span data-ttu-id="82989-117">Gibt die Codierung für das zu erstellende Element an.</span><span class="sxs-lookup"><span data-stu-id="82989-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="82989-118">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="82989-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="82989-119">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="82989-119">Unknown</span></span>
- <span data-ttu-id="82989-120">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="82989-120">String</span></span>
- <span data-ttu-id="82989-121">Unicode</span><span class="sxs-lookup"><span data-stu-id="82989-121">Unicode</span></span>
- <span data-ttu-id="82989-122">Byte</span><span class="sxs-lookup"><span data-stu-id="82989-122">Byte</span></span>
- <span data-ttu-id="82989-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="82989-123">BigEndianUnicode</span></span>
- <span data-ttu-id="82989-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="82989-124">UTF8</span></span>
- <span data-ttu-id="82989-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="82989-125">UTF7</span></span>
- <span data-ttu-id="82989-126">Ascii</span><span class="sxs-lookup"><span data-stu-id="82989-126">Ascii</span></span>
- <span data-ttu-id="82989-127">Standard</span><span class="sxs-lookup"><span data-stu-id="82989-127">Default</span></span>
- <span data-ttu-id="82989-128">Oem</span><span class="sxs-lookup"><span data-stu-id="82989-128">Oem</span></span>
- <span data-ttu-id="82989-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="82989-129">BigEndianUTF32</span></span>

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82989-130">-Folder</span><span class="sxs-lookup"><span data-stu-id="82989-130">-Folder</span></span>
<span data-ttu-id="82989-131">Gibt an, dass mit diesem Vorgang ein Ordner erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="82989-131">Indicates that this operation creates a folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82989-132">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="82989-132">-Force</span></span>
<span data-ttu-id="82989-133">Gibt an, dass durch diesen Vorgang das Zielelement überschrieben werden kann, wenn es bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="82989-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82989-134">-Path</span><span class="sxs-lookup"><span data-stu-id="82989-134">-Path</span></span>
<span data-ttu-id="82989-135">Gibt den Data Lake Store-Pfad des zu erstellenden Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="82989-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82989-136">-Wert</span><span class="sxs-lookup"><span data-stu-id="82989-136">-Value</span></span>
<span data-ttu-id="82989-137">Gibt den Inhalt an, der dem von Ihnen erstellten Element hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="82989-137">Specifies the content to add to the item you create.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82989-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="82989-138">-Confirm</span></span>
<span data-ttu-id="82989-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="82989-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82989-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82989-140">-WhatIf</span></span>
<span data-ttu-id="82989-141">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="82989-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82989-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="82989-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82989-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82989-143">CommonParameters</span></span>
<span data-ttu-id="82989-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82989-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82989-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82989-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82989-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="82989-146">INPUTS</span></span>

### <span data-ttu-id="82989-147">System.String</span><span class="sxs-lookup"><span data-stu-id="82989-147">System.String</span></span>

### <span data-ttu-id="82989-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="82989-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="82989-149">System.Object</span><span class="sxs-lookup"><span data-stu-id="82989-149">System.Object</span></span>

### <span data-ttu-id="82989-150">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="82989-150">System.Text.Encoding</span></span>

### <span data-ttu-id="82989-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="82989-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="82989-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="82989-152">OUTPUTS</span></span>

### <span data-ttu-id="82989-153">System.String</span><span class="sxs-lookup"><span data-stu-id="82989-153">System.String</span></span>

## <span data-ttu-id="82989-154">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="82989-154">NOTES</span></span>

## <span data-ttu-id="82989-155">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="82989-155">RELATED LINKS</span></span>

[<span data-ttu-id="82989-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82989-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="82989-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82989-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="82989-158">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82989-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="82989-159">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82989-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="82989-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82989-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="82989-161">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82989-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


