---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 4ce79044793bbecc76d72fab015166ccc3d8fba6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479266"
---
# <span data-ttu-id="d5119-101">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="d5119-101">Add-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="d5119-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d5119-102">SYNOPSIS</span></span>
<span data-ttu-id="d5119-103">Fügt Inhalt zu einem Element in einem Data Lake Store hinzu.</span><span class="sxs-lookup"><span data-stu-id="d5119-103">Adds content to an item in a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5119-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5119-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5119-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5119-105">DESCRIPTION</span></span>
<span data-ttu-id="d5119-106">Das Cmdlet **Add-AzureRmDataLakeStoreItemContent** fügt Inhalt zu einem Element in einem Azure Data Lake Store hinzu.</span><span class="sxs-lookup"><span data-stu-id="d5119-106">The **Add-AzureRmDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="d5119-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5119-107">EXAMPLES</span></span>

### <span data-ttu-id="d5119-108">Beispiel 1: Hinzufügen von Inhalt zu einer Datei</span><span class="sxs-lookup"><span data-stu-id="d5119-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzureRmDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="d5119-109">Dieser Befehl fügt der Datei myFile.txt Inhalt hinzu.</span><span class="sxs-lookup"><span data-stu-id="d5119-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="d5119-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5119-110">PARAMETERS</span></span>

### <span data-ttu-id="d5119-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="d5119-111">-Account</span></span>
<span data-ttu-id="d5119-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="d5119-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d5119-113">-Encoding</span><span class="sxs-lookup"><span data-stu-id="d5119-113">-Encoding</span></span>
<span data-ttu-id="d5119-114">Gibt die Codierung für das zu erstellende Element an.</span><span class="sxs-lookup"><span data-stu-id="d5119-114">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="d5119-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d5119-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d5119-116">Unbekannten</span><span class="sxs-lookup"><span data-stu-id="d5119-116">Unknown</span></span>
- <span data-ttu-id="d5119-117">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d5119-117">String</span></span>
- <span data-ttu-id="d5119-118">Unicode</span><span class="sxs-lookup"><span data-stu-id="d5119-118">Unicode</span></span>
- <span data-ttu-id="d5119-119">Byte</span><span class="sxs-lookup"><span data-stu-id="d5119-119">Byte</span></span>
- <span data-ttu-id="d5119-120">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="d5119-120">BigEndianUnicode</span></span>
- <span data-ttu-id="d5119-121">UTF8</span><span class="sxs-lookup"><span data-stu-id="d5119-121">UTF8</span></span>
- <span data-ttu-id="d5119-122">UTF7</span><span class="sxs-lookup"><span data-stu-id="d5119-122">UTF7</span></span>
- <span data-ttu-id="d5119-123">ASCII</span><span class="sxs-lookup"><span data-stu-id="d5119-123">Ascii</span></span>
- <span data-ttu-id="d5119-124">Standard</span><span class="sxs-lookup"><span data-stu-id="d5119-124">Default</span></span>
- <span data-ttu-id="d5119-125">OEM</span><span class="sxs-lookup"><span data-stu-id="d5119-125">Oem</span></span>
- <span data-ttu-id="d5119-126">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="d5119-126">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.PowerShell.Commands.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5119-127">-Path</span><span class="sxs-lookup"><span data-stu-id="d5119-127">-Path</span></span>
<span data-ttu-id="d5119-128">Gibt den Daten See-Speicherpfad des zu ändernden Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="d5119-128">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d5119-129">-Wert</span><span class="sxs-lookup"><span data-stu-id="d5119-129">-Value</span></span>
<span data-ttu-id="d5119-130">Gibt den Inhalt an, der dem Element hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5119-130">Specifies the content to add to the item.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5119-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5119-131">-DefaultProfile</span></span>
<span data-ttu-id="d5119-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d5119-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5119-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5119-133">CommonParameters</span></span>
<span data-ttu-id="d5119-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5119-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5119-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5119-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5119-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d5119-136">INPUTS</span></span>

### <span data-ttu-id="d5119-137">Objekt</span><span class="sxs-lookup"><span data-stu-id="d5119-137">Object</span></span>
<span data-ttu-id="d5119-138">Der Parameter "Wert" akzeptiert den Wert vom Typ "Object" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d5119-138">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="d5119-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d5119-139">OUTPUTS</span></span>

### <span data-ttu-id="d5119-140">bool</span><span class="sxs-lookup"><span data-stu-id="d5119-140">bool</span></span>
<span data-ttu-id="d5119-141">Gibt beim Erfolg TRUE zurück.</span><span class="sxs-lookup"><span data-stu-id="d5119-141">Returns true on success.</span></span>

## <span data-ttu-id="d5119-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="d5119-142">NOTES</span></span>

## <span data-ttu-id="d5119-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d5119-143">RELATED LINKS</span></span>

[<span data-ttu-id="d5119-144">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="d5119-144">Get-AzureRmDataLakeStoreItemContent</span></span>](./Get-AzureRmDataLakeStoreItemContent.md)


