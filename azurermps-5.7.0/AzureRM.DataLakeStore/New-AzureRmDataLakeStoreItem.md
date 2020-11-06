---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 2dc2d18fc0bc09fd7e9477115f4212aeb2452bbb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478497"
---
# <span data-ttu-id="5a10a-101">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5a10a-101">New-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="5a10a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a10a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a10a-103">Erstellt eine neue Datei oder einen neuen Ordner im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5a10a-103">Creates a new file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a10a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a10a-104">SYNTAX</span></span>

```
New-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a10a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a10a-105">DESCRIPTION</span></span>
<span data-ttu-id="5a10a-106">Das Cmdlet **New-AzureRmDataLakeStoreItem** erstellt eine neue Datei oder einen neuen Ordner im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5a10a-106">The **New-AzureRmDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5a10a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a10a-107">EXAMPLES</span></span>

### <span data-ttu-id="5a10a-108">Beispiel 1: Erstellen einer neuen Datei und eines neuen Ordners</span><span class="sxs-lookup"><span data-stu-id="5a10a-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="5a10a-109">Mit dem ersten Befehl wird die Datei NewFile.txt für das angegebene Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="5a10a-109">The first command creates the file NewFile.txt for the specified account.</span></span>

<span data-ttu-id="5a10a-110">Mit dem zweiten Befehl wird der Ordner "Ordner" im Stammordner erstellt.</span><span class="sxs-lookup"><span data-stu-id="5a10a-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="5a10a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a10a-111">PARAMETERS</span></span>

### <span data-ttu-id="5a10a-112">-Konto</span><span class="sxs-lookup"><span data-stu-id="5a10a-112">-Account</span></span>
<span data-ttu-id="5a10a-113">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="5a10a-113">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a10a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a10a-114">-DefaultProfile</span></span>
<span data-ttu-id="5a10a-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5a10a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a10a-116">-Encoding</span><span class="sxs-lookup"><span data-stu-id="5a10a-116">-Encoding</span></span>
<span data-ttu-id="5a10a-117">Gibt die Codierung für das zu erstellende Element an.</span><span class="sxs-lookup"><span data-stu-id="5a10a-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="5a10a-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5a10a-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5a10a-119">Unbekannten</span><span class="sxs-lookup"><span data-stu-id="5a10a-119">Unknown</span></span>
- <span data-ttu-id="5a10a-120">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5a10a-120">String</span></span>
- <span data-ttu-id="5a10a-121">Unicode</span><span class="sxs-lookup"><span data-stu-id="5a10a-121">Unicode</span></span>
- <span data-ttu-id="5a10a-122">Byte</span><span class="sxs-lookup"><span data-stu-id="5a10a-122">Byte</span></span>
- <span data-ttu-id="5a10a-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="5a10a-123">BigEndianUnicode</span></span>
- <span data-ttu-id="5a10a-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="5a10a-124">UTF8</span></span>
- <span data-ttu-id="5a10a-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="5a10a-125">UTF7</span></span>
- <span data-ttu-id="5a10a-126">ASCII</span><span class="sxs-lookup"><span data-stu-id="5a10a-126">Ascii</span></span>
- <span data-ttu-id="5a10a-127">Standard</span><span class="sxs-lookup"><span data-stu-id="5a10a-127">Default</span></span>
- <span data-ttu-id="5a10a-128">OEM</span><span class="sxs-lookup"><span data-stu-id="5a10a-128">Oem</span></span>
- <span data-ttu-id="5a10a-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="5a10a-129">BigEndianUTF32</span></span>

```yaml
Type: FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a10a-130">-Folder</span><span class="sxs-lookup"><span data-stu-id="5a10a-130">-Folder</span></span>
<span data-ttu-id="5a10a-131">Gibt an, dass dieser Vorgang einen Ordner erstellt.</span><span class="sxs-lookup"><span data-stu-id="5a10a-131">Indicates that this operation creates a folder.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a10a-132">-Force</span><span class="sxs-lookup"><span data-stu-id="5a10a-132">-Force</span></span>
<span data-ttu-id="5a10a-133">Gibt an, dass dieser Vorgang das Zielelement überschreiben kann, wenn es bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5a10a-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a10a-134">-Path</span><span class="sxs-lookup"><span data-stu-id="5a10a-134">-Path</span></span>
<span data-ttu-id="5a10a-135">Gibt den Daten See-Speicherpfad des zu erstellenden Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="5a10a-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a10a-136">-Wert</span><span class="sxs-lookup"><span data-stu-id="5a10a-136">-Value</span></span>
<span data-ttu-id="5a10a-137">Gibt den Inhalt an, der dem erstellten Element hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a10a-137">Specifies the content to add to the item you create.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a10a-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5a10a-138">-Confirm</span></span>
<span data-ttu-id="5a10a-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a10a-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a10a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a10a-140">-WhatIf</span></span>
<span data-ttu-id="5a10a-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a10a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a10a-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a10a-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a10a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a10a-143">CommonParameters</span></span>
<span data-ttu-id="5a10a-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a10a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a10a-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a10a-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a10a-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a10a-146">INPUTS</span></span>

### <span data-ttu-id="5a10a-147">Objekt</span><span class="sxs-lookup"><span data-stu-id="5a10a-147">Object</span></span>
<span data-ttu-id="5a10a-148">Der Parameter "Wert" akzeptiert den Wert vom Typ "Object" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5a10a-148">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="5a10a-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a10a-149">OUTPUTS</span></span>

### <span data-ttu-id="5a10a-150">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5a10a-150">string</span></span>
<span data-ttu-id="5a10a-151">Der vollständige Pfad zu der erstellten Datei oder dem erstellten Ordner.</span><span class="sxs-lookup"><span data-stu-id="5a10a-151">The full path to the created file or folder.</span></span>

## <span data-ttu-id="5a10a-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a10a-152">NOTES</span></span>

## <span data-ttu-id="5a10a-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a10a-153">RELATED LINKS</span></span>

[<span data-ttu-id="5a10a-154">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5a10a-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5a10a-155">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5a10a-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5a10a-156">Importieren-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5a10a-156">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5a10a-157">Neu – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5a10a-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5a10a-158">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5a10a-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5a10a-159">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5a10a-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


