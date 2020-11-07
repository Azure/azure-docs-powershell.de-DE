---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 1727c0960d90a8566d2247e8d8e091f6ce66f9b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661286"
---
# <span data-ttu-id="515b2-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="515b2-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="515b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="515b2-102">SYNOPSIS</span></span>
<span data-ttu-id="515b2-103">Fügt Inhalt zu einem Element in einem Data Lake Store hinzu.</span><span class="sxs-lookup"><span data-stu-id="515b2-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="515b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="515b2-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="515b2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="515b2-105">DESCRIPTION</span></span>
<span data-ttu-id="515b2-106">Das Cmdlet **Add-AzDataLakeStoreItemContent** fügt Inhalt zu einem Element in einem Azure Data Lake Store hinzu.</span><span class="sxs-lookup"><span data-stu-id="515b2-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="515b2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="515b2-107">EXAMPLES</span></span>

### <span data-ttu-id="515b2-108">Beispiel 1: Hinzufügen von Inhalt zu einer Datei</span><span class="sxs-lookup"><span data-stu-id="515b2-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="515b2-109">Dieser Befehl fügt der Datei myFile.txt Inhalt hinzu.</span><span class="sxs-lookup"><span data-stu-id="515b2-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="515b2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="515b2-110">PARAMETERS</span></span>

### <span data-ttu-id="515b2-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="515b2-111">-Account</span></span>
<span data-ttu-id="515b2-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="515b2-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="515b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="515b2-113">-DefaultProfile</span></span>
<span data-ttu-id="515b2-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="515b2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="515b2-115">-Encoding</span><span class="sxs-lookup"><span data-stu-id="515b2-115">-Encoding</span></span>
<span data-ttu-id="515b2-116">Gibt die Codierung für das zu erstellende Element an.</span><span class="sxs-lookup"><span data-stu-id="515b2-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="515b2-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="515b2-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="515b2-118">Unbekannten</span><span class="sxs-lookup"><span data-stu-id="515b2-118">Unknown</span></span>
- <span data-ttu-id="515b2-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="515b2-119">String</span></span>
- <span data-ttu-id="515b2-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="515b2-120">Unicode</span></span>
- <span data-ttu-id="515b2-121">Byte</span><span class="sxs-lookup"><span data-stu-id="515b2-121">Byte</span></span>
- <span data-ttu-id="515b2-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="515b2-122">BigEndianUnicode</span></span>
- <span data-ttu-id="515b2-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="515b2-123">UTF8</span></span>
- <span data-ttu-id="515b2-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="515b2-124">UTF7</span></span>
- <span data-ttu-id="515b2-125">ASCII</span><span class="sxs-lookup"><span data-stu-id="515b2-125">Ascii</span></span>
- <span data-ttu-id="515b2-126">Standard</span><span class="sxs-lookup"><span data-stu-id="515b2-126">Default</span></span>
- <span data-ttu-id="515b2-127">OEM</span><span class="sxs-lookup"><span data-stu-id="515b2-127">Oem</span></span>
- <span data-ttu-id="515b2-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="515b2-128">BigEndianUTF32</span></span>

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

### <span data-ttu-id="515b2-129">-Path</span><span class="sxs-lookup"><span data-stu-id="515b2-129">-Path</span></span>
<span data-ttu-id="515b2-130">Gibt den Daten See-Speicherpfad des zu ändernden Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="515b2-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="515b2-131">-Wert</span><span class="sxs-lookup"><span data-stu-id="515b2-131">-Value</span></span>
<span data-ttu-id="515b2-132">Gibt den Inhalt an, der dem Element hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="515b2-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="515b2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="515b2-133">CommonParameters</span></span>
<span data-ttu-id="515b2-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="515b2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="515b2-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="515b2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="515b2-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="515b2-136">INPUTS</span></span>

### <span data-ttu-id="515b2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="515b2-137">System.String</span></span>

### <span data-ttu-id="515b2-138">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="515b2-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="515b2-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="515b2-139">System.Object</span></span>

### <span data-ttu-id="515b2-140">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="515b2-140">System.Text.Encoding</span></span>

## <span data-ttu-id="515b2-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="515b2-141">OUTPUTS</span></span>

### <span data-ttu-id="515b2-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="515b2-142">System.Boolean</span></span>

## <span data-ttu-id="515b2-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="515b2-143">NOTES</span></span>

## <span data-ttu-id="515b2-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="515b2-144">RELATED LINKS</span></span>

[<span data-ttu-id="515b2-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="515b2-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


