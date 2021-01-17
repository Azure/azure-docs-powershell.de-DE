---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: ab752ec2201c9b64a9656153f29a947b7a722819
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458067"
---
# <span data-ttu-id="0ea21-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0ea21-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="0ea21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ea21-102">SYNOPSIS</span></span>
<span data-ttu-id="0ea21-103">Erstellt eine neue Datei oder einen neuen Ordner im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0ea21-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0ea21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ea21-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ea21-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ea21-105">DESCRIPTION</span></span>
<span data-ttu-id="0ea21-106">Das **Cmdlet "New-AzDataLakeStoreItem"** erstellt eine neue Datei oder einen neuen Ordner im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0ea21-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0ea21-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0ea21-107">EXAMPLES</span></span>

### <span data-ttu-id="0ea21-108">Beispiel 1: Erstellen einer neuen Datei und eines neuen Ordners</span><span class="sxs-lookup"><span data-stu-id="0ea21-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="0ea21-109">Der erste Befehl erstellt die NewFile.txt für das angegebene Konto.</span><span class="sxs-lookup"><span data-stu-id="0ea21-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="0ea21-110">Der zweite Befehl erstellt den Ordner "NewFolder" im Stammordner.</span><span class="sxs-lookup"><span data-stu-id="0ea21-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="0ea21-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ea21-111">PARAMETERS</span></span>

### <span data-ttu-id="0ea21-112">-Konto</span><span class="sxs-lookup"><span data-stu-id="0ea21-112">-Account</span></span>
<span data-ttu-id="0ea21-113">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="0ea21-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="0ea21-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ea21-114">-DefaultProfile</span></span>
<span data-ttu-id="0ea21-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ea21-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ea21-116">-Encoding</span><span class="sxs-lookup"><span data-stu-id="0ea21-116">-Encoding</span></span>
<span data-ttu-id="0ea21-117">Gibt die Codierung für das zu erstellende Element an.</span><span class="sxs-lookup"><span data-stu-id="0ea21-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="0ea21-118">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="0ea21-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0ea21-119">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="0ea21-119">Unknown</span></span>
- <span data-ttu-id="0ea21-120">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0ea21-120">String</span></span>
- <span data-ttu-id="0ea21-121">Unicode</span><span class="sxs-lookup"><span data-stu-id="0ea21-121">Unicode</span></span>
- <span data-ttu-id="0ea21-122">Byte</span><span class="sxs-lookup"><span data-stu-id="0ea21-122">Byte</span></span>
- <span data-ttu-id="0ea21-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="0ea21-123">BigEndianUnicode</span></span>
- <span data-ttu-id="0ea21-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="0ea21-124">UTF8</span></span>
- <span data-ttu-id="0ea21-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="0ea21-125">UTF7</span></span>
- <span data-ttu-id="0ea21-126">Ascii</span><span class="sxs-lookup"><span data-stu-id="0ea21-126">Ascii</span></span>
- <span data-ttu-id="0ea21-127">Standard</span><span class="sxs-lookup"><span data-stu-id="0ea21-127">Default</span></span>
- <span data-ttu-id="0ea21-128">Oem</span><span class="sxs-lookup"><span data-stu-id="0ea21-128">Oem</span></span>
- <span data-ttu-id="0ea21-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="0ea21-129">BigEndianUTF32</span></span>

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

### <span data-ttu-id="0ea21-130">-Folder</span><span class="sxs-lookup"><span data-stu-id="0ea21-130">-Folder</span></span>
<span data-ttu-id="0ea21-131">Gibt an, dass mit diesem Vorgang ein Ordner erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0ea21-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="0ea21-132">-Force</span><span class="sxs-lookup"><span data-stu-id="0ea21-132">-Force</span></span>
<span data-ttu-id="0ea21-133">Gibt an, dass das Zielelement durch diesen Vorgang überschrieben werden kann, wenn es bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0ea21-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="0ea21-134">-Path</span><span class="sxs-lookup"><span data-stu-id="0ea21-134">-Path</span></span>
<span data-ttu-id="0ea21-135">Gibt den Data Lake Store-Pfad des zu erstellenden Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="0ea21-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="0ea21-136">-Value</span><span class="sxs-lookup"><span data-stu-id="0ea21-136">-Value</span></span>
<span data-ttu-id="0ea21-137">Gibt den Inhalt an, der dem von Ihnen erstellten Element hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0ea21-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="0ea21-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ea21-138">-Confirm</span></span>
<span data-ttu-id="0ea21-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0ea21-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ea21-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0ea21-140">-WhatIf</span></span>
<span data-ttu-id="0ea21-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ea21-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ea21-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ea21-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ea21-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ea21-143">CommonParameters</span></span>
<span data-ttu-id="0ea21-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ea21-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ea21-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ea21-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ea21-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0ea21-146">INPUTS</span></span>

### <span data-ttu-id="0ea21-147">System.String</span><span class="sxs-lookup"><span data-stu-id="0ea21-147">System.String</span></span>

### <span data-ttu-id="0ea21-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="0ea21-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="0ea21-149">System.Object</span><span class="sxs-lookup"><span data-stu-id="0ea21-149">System.Object</span></span>

### <span data-ttu-id="0ea21-150">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="0ea21-150">System.Text.Encoding</span></span>

### <span data-ttu-id="0ea21-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0ea21-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0ea21-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0ea21-152">OUTPUTS</span></span>

### <span data-ttu-id="0ea21-153">System.String</span><span class="sxs-lookup"><span data-stu-id="0ea21-153">System.String</span></span>

## <span data-ttu-id="0ea21-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0ea21-154">NOTES</span></span>

## <span data-ttu-id="0ea21-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0ea21-155">RELATED LINKS</span></span>

[<span data-ttu-id="0ea21-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0ea21-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="0ea21-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0ea21-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="0ea21-158">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0ea21-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="0ea21-159">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0ea21-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="0ea21-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0ea21-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="0ea21-161">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0ea21-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


