---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 2e50135762826661e82f499f2aec48c67d00c648
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476118"
---
# <span data-ttu-id="83c19-101">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83c19-101">New-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="83c19-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83c19-102">SYNOPSIS</span></span>
<span data-ttu-id="83c19-103">Erstellt eine neue Datei oder einen neuen Ordner im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="83c19-103">Creates a new file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83c19-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83c19-104">SYNTAX</span></span>

```
New-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83c19-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83c19-105">DESCRIPTION</span></span>
<span data-ttu-id="83c19-106">Das Cmdlet **New-AzureRmDataLakeStoreItem** erstellt eine neue Datei oder einen neuen Ordner im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="83c19-106">The **New-AzureRmDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="83c19-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83c19-107">EXAMPLES</span></span>

### <span data-ttu-id="83c19-108">Beispiel 1: Erstellen einer neuen Datei und eines neuen Ordners</span><span class="sxs-lookup"><span data-stu-id="83c19-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="83c19-109">Mit dem ersten Befehl wird die Datei NewFile.txt für das angegebene Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="83c19-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="83c19-110">Mit dem zweiten Befehl wird der Ordner "Ordner" im Stammordner erstellt.</span><span class="sxs-lookup"><span data-stu-id="83c19-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="83c19-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="83c19-111">PARAMETERS</span></span>

### <span data-ttu-id="83c19-112">-Konto</span><span class="sxs-lookup"><span data-stu-id="83c19-112">-Account</span></span>
<span data-ttu-id="83c19-113">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="83c19-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="83c19-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83c19-114">-DefaultProfile</span></span>
<span data-ttu-id="83c19-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="83c19-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83c19-116">-Encoding</span><span class="sxs-lookup"><span data-stu-id="83c19-116">-Encoding</span></span>
<span data-ttu-id="83c19-117">Gibt die Codierung für das zu erstellende Element an.</span><span class="sxs-lookup"><span data-stu-id="83c19-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="83c19-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="83c19-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="83c19-119">Unbekannten</span><span class="sxs-lookup"><span data-stu-id="83c19-119">Unknown</span></span>
- <span data-ttu-id="83c19-120">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="83c19-120">String</span></span>
- <span data-ttu-id="83c19-121">Unicode</span><span class="sxs-lookup"><span data-stu-id="83c19-121">Unicode</span></span>
- <span data-ttu-id="83c19-122">Byte</span><span class="sxs-lookup"><span data-stu-id="83c19-122">Byte</span></span>
- <span data-ttu-id="83c19-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="83c19-123">BigEndianUnicode</span></span>
- <span data-ttu-id="83c19-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="83c19-124">UTF8</span></span>
- <span data-ttu-id="83c19-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="83c19-125">UTF7</span></span>
- <span data-ttu-id="83c19-126">ASCII</span><span class="sxs-lookup"><span data-stu-id="83c19-126">Ascii</span></span>
- <span data-ttu-id="83c19-127">Standard</span><span class="sxs-lookup"><span data-stu-id="83c19-127">Default</span></span>
- <span data-ttu-id="83c19-128">OEM</span><span class="sxs-lookup"><span data-stu-id="83c19-128">Oem</span></span>
- <span data-ttu-id="83c19-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="83c19-129">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83c19-130">-Folder</span><span class="sxs-lookup"><span data-stu-id="83c19-130">-Folder</span></span>
<span data-ttu-id="83c19-131">Gibt an, dass dieser Vorgang einen Ordner erstellt.</span><span class="sxs-lookup"><span data-stu-id="83c19-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="83c19-132">-Force</span><span class="sxs-lookup"><span data-stu-id="83c19-132">-Force</span></span>
<span data-ttu-id="83c19-133">Gibt an, dass dieser Vorgang das Zielelement überschreiben kann, wenn es bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="83c19-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="83c19-134">-Path</span><span class="sxs-lookup"><span data-stu-id="83c19-134">-Path</span></span>
<span data-ttu-id="83c19-135">Gibt den Daten See-Speicherpfad des zu erstellenden Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="83c19-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="83c19-136">-Wert</span><span class="sxs-lookup"><span data-stu-id="83c19-136">-Value</span></span>
<span data-ttu-id="83c19-137">Gibt den Inhalt an, der dem erstellten Element hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="83c19-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="83c19-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="83c19-138">-Confirm</span></span>
<span data-ttu-id="83c19-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="83c19-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83c19-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83c19-140">-WhatIf</span></span>
<span data-ttu-id="83c19-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83c19-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83c19-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="83c19-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83c19-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83c19-143">CommonParameters</span></span>
<span data-ttu-id="83c19-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83c19-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83c19-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83c19-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83c19-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83c19-146">INPUTS</span></span>

### <span data-ttu-id="83c19-147">System. String</span><span class="sxs-lookup"><span data-stu-id="83c19-147">System.String</span></span>

### <span data-ttu-id="83c19-148">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="83c19-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="83c19-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="83c19-149">System.Object</span></span>

### <span data-ttu-id="83c19-150">Microsoft. Azure. Commands. DataLakeStore. Models. FileSystemCmdletProviderEncoding</span><span class="sxs-lookup"><span data-stu-id="83c19-150">Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding</span></span>

### <span data-ttu-id="83c19-151">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="83c19-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="83c19-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83c19-152">OUTPUTS</span></span>

### <span data-ttu-id="83c19-153">System. String</span><span class="sxs-lookup"><span data-stu-id="83c19-153">System.String</span></span>
<span data-ttu-id="83c19-154">Der vollständige Pfad zu der erstellten Datei oder dem erstellten Ordner.</span><span class="sxs-lookup"><span data-stu-id="83c19-154">The full path to the created file or folder.</span></span>

## <span data-ttu-id="83c19-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="83c19-155">NOTES</span></span>

## <span data-ttu-id="83c19-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83c19-156">RELATED LINKS</span></span>

[<span data-ttu-id="83c19-157">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83c19-157">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="83c19-158">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83c19-158">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="83c19-159">Importieren-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83c19-159">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="83c19-160">Neu – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83c19-160">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="83c19-161">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83c19-161">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="83c19-162">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83c19-162">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


