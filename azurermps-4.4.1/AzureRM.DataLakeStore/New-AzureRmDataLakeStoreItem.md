---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a087c2f7cfd4358e137550aa2e916fa2200d2a2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501893"
---
# <span data-ttu-id="86d75-101">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="86d75-101">New-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="86d75-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="86d75-102">SYNOPSIS</span></span>
<span data-ttu-id="86d75-103">Erstellt eine neue Datei oder einen neuen Ordner im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="86d75-103">Creates a new file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86d75-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="86d75-104">SYNTAX</span></span>

```
New-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86d75-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86d75-105">DESCRIPTION</span></span>
<span data-ttu-id="86d75-106">Das Cmdlet **New-AzureRmDataLakeStoreItem** erstellt eine neue Datei oder einen neuen Ordner im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="86d75-106">The **New-AzureRmDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="86d75-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86d75-107">EXAMPLES</span></span>

### <span data-ttu-id="86d75-108">Beispiel 1: Erstellen einer neuen Datei und eines neuen Ordners</span><span class="sxs-lookup"><span data-stu-id="86d75-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="86d75-109">Mit dem ersten Befehl wird die Datei NewFile.txt für das angegebene Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="86d75-109">The first command creates the file NewFile.txt for the specified account.</span></span>

<span data-ttu-id="86d75-110">Mit dem zweiten Befehl wird der Ordner "Ordner" im Stammordner erstellt.</span><span class="sxs-lookup"><span data-stu-id="86d75-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="86d75-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="86d75-111">PARAMETERS</span></span>

### <span data-ttu-id="86d75-112">-Konto</span><span class="sxs-lookup"><span data-stu-id="86d75-112">-Account</span></span>
<span data-ttu-id="86d75-113">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="86d75-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="86d75-114">-Encoding</span><span class="sxs-lookup"><span data-stu-id="86d75-114">-Encoding</span></span>
<span data-ttu-id="86d75-115">Gibt die Codierung für das zu erstellende Element an.</span><span class="sxs-lookup"><span data-stu-id="86d75-115">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="86d75-116">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="86d75-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="86d75-117">Unbekannten</span><span class="sxs-lookup"><span data-stu-id="86d75-117">Unknown</span></span>
- <span data-ttu-id="86d75-118">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="86d75-118">String</span></span>
- <span data-ttu-id="86d75-119">Unicode</span><span class="sxs-lookup"><span data-stu-id="86d75-119">Unicode</span></span>
- <span data-ttu-id="86d75-120">Byte</span><span class="sxs-lookup"><span data-stu-id="86d75-120">Byte</span></span>
- <span data-ttu-id="86d75-121">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="86d75-121">BigEndianUnicode</span></span>
- <span data-ttu-id="86d75-122">UTF8</span><span class="sxs-lookup"><span data-stu-id="86d75-122">UTF8</span></span>
- <span data-ttu-id="86d75-123">UTF7</span><span class="sxs-lookup"><span data-stu-id="86d75-123">UTF7</span></span>
- <span data-ttu-id="86d75-124">ASCII</span><span class="sxs-lookup"><span data-stu-id="86d75-124">Ascii</span></span>
- <span data-ttu-id="86d75-125">Standard</span><span class="sxs-lookup"><span data-stu-id="86d75-125">Default</span></span>
- <span data-ttu-id="86d75-126">OEM</span><span class="sxs-lookup"><span data-stu-id="86d75-126">Oem</span></span>
- <span data-ttu-id="86d75-127">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="86d75-127">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.PowerShell.Commands.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86d75-128">-Folder</span><span class="sxs-lookup"><span data-stu-id="86d75-128">-Folder</span></span>
<span data-ttu-id="86d75-129">Gibt an, dass dieser Vorgang einen Ordner erstellt.</span><span class="sxs-lookup"><span data-stu-id="86d75-129">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="86d75-130">-Force</span><span class="sxs-lookup"><span data-stu-id="86d75-130">-Force</span></span>
<span data-ttu-id="86d75-131">Gibt an, dass dieser Vorgang das Zielelement überschreiben kann, wenn es bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="86d75-131">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="86d75-132">-Path</span><span class="sxs-lookup"><span data-stu-id="86d75-132">-Path</span></span>
<span data-ttu-id="86d75-133">Gibt den Daten See-Speicherpfad des zu erstellenden Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="86d75-133">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="86d75-134">-Wert</span><span class="sxs-lookup"><span data-stu-id="86d75-134">-Value</span></span>
<span data-ttu-id="86d75-135">Gibt den Inhalt an, der dem erstellten Element hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="86d75-135">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="86d75-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="86d75-136">-Confirm</span></span>
<span data-ttu-id="86d75-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="86d75-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86d75-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86d75-138">-WhatIf</span></span>
<span data-ttu-id="86d75-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="86d75-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86d75-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="86d75-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86d75-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86d75-141">-DefaultProfile</span></span>
<span data-ttu-id="86d75-142">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="86d75-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d75-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d75-143">CommonParameters</span></span>
<span data-ttu-id="86d75-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86d75-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86d75-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86d75-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d75-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="86d75-146">INPUTS</span></span>

### <span data-ttu-id="86d75-147">Objekt</span><span class="sxs-lookup"><span data-stu-id="86d75-147">Object</span></span>
<span data-ttu-id="86d75-148">Der Parameter "Wert" akzeptiert den Wert vom Typ "Object" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="86d75-148">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="86d75-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="86d75-149">OUTPUTS</span></span>

### <span data-ttu-id="86d75-150">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="86d75-150">string</span></span>
<span data-ttu-id="86d75-151">Der vollständige Pfad zu der erstellten Datei oder dem erstellten Ordner.</span><span class="sxs-lookup"><span data-stu-id="86d75-151">The full path to the created file or folder.</span></span>

## <span data-ttu-id="86d75-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="86d75-152">NOTES</span></span>

## <span data-ttu-id="86d75-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="86d75-153">RELATED LINKS</span></span>

[<span data-ttu-id="86d75-154">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="86d75-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="86d75-155">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="86d75-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="86d75-156">Importieren-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="86d75-156">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="86d75-157">Neu – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="86d75-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="86d75-158">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="86d75-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="86d75-159">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="86d75-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


