---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: aa2fe76f221ce412c0e47f7a43b1dba551131f45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940528"
---
# <span data-ttu-id="aea62-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="aea62-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="aea62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aea62-102">SYNOPSIS</span></span>
<span data-ttu-id="aea62-103">Fügt einem Element in einem Data Lake Store Inhalt hinzu.</span><span class="sxs-lookup"><span data-stu-id="aea62-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="aea62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aea62-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aea62-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aea62-105">DESCRIPTION</span></span>
<span data-ttu-id="aea62-106">Das **Add-AzDataLakeStoreItemContent-Cmdlet** fügt einem Element in einem Azure Data Lake Store Inhalt hinzu.</span><span class="sxs-lookup"><span data-stu-id="aea62-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="aea62-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aea62-107">EXAMPLES</span></span>

### <span data-ttu-id="aea62-108">Beispiel 1: Hinzufügen von Inhalt zu einer Datei</span><span class="sxs-lookup"><span data-stu-id="aea62-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="aea62-109">Mit diesem Befehl werden Dem Dateiinhalt myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="aea62-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="aea62-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="aea62-110">PARAMETERS</span></span>

### <span data-ttu-id="aea62-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="aea62-111">-Account</span></span>
<span data-ttu-id="aea62-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="aea62-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="aea62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea62-113">-DefaultProfile</span></span>
<span data-ttu-id="aea62-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="aea62-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aea62-115">-Encoding</span><span class="sxs-lookup"><span data-stu-id="aea62-115">-Encoding</span></span>
<span data-ttu-id="aea62-116">Gibt die Codierung für das zu erstellende Element an.</span><span class="sxs-lookup"><span data-stu-id="aea62-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="aea62-117">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="aea62-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aea62-118">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="aea62-118">Unknown</span></span>
- <span data-ttu-id="aea62-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="aea62-119">String</span></span>
- <span data-ttu-id="aea62-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="aea62-120">Unicode</span></span>
- <span data-ttu-id="aea62-121">Byte</span><span class="sxs-lookup"><span data-stu-id="aea62-121">Byte</span></span>
- <span data-ttu-id="aea62-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="aea62-122">BigEndianUnicode</span></span>
- <span data-ttu-id="aea62-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="aea62-123">UTF8</span></span>
- <span data-ttu-id="aea62-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="aea62-124">UTF7</span></span>
- <span data-ttu-id="aea62-125">Ascii</span><span class="sxs-lookup"><span data-stu-id="aea62-125">Ascii</span></span>
- <span data-ttu-id="aea62-126">Standard</span><span class="sxs-lookup"><span data-stu-id="aea62-126">Default</span></span>
- <span data-ttu-id="aea62-127">Oem</span><span class="sxs-lookup"><span data-stu-id="aea62-127">Oem</span></span>
- <span data-ttu-id="aea62-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="aea62-128">BigEndianUTF32</span></span>

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

### <span data-ttu-id="aea62-129">-Path</span><span class="sxs-lookup"><span data-stu-id="aea62-129">-Path</span></span>
<span data-ttu-id="aea62-130">Gibt den Data Lake Store-Pfad des zu ändernden Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="aea62-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="aea62-131">-Wert</span><span class="sxs-lookup"><span data-stu-id="aea62-131">-Value</span></span>
<span data-ttu-id="aea62-132">Gibt den Inhalt an, der dem Element hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="aea62-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="aea62-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea62-133">CommonParameters</span></span>
<span data-ttu-id="aea62-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aea62-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea62-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aea62-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea62-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aea62-136">INPUTS</span></span>

### <span data-ttu-id="aea62-137">System.String</span><span class="sxs-lookup"><span data-stu-id="aea62-137">System.String</span></span>

### <span data-ttu-id="aea62-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="aea62-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="aea62-139">System.Object</span><span class="sxs-lookup"><span data-stu-id="aea62-139">System.Object</span></span>

### <span data-ttu-id="aea62-140">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="aea62-140">System.Text.Encoding</span></span>

## <span data-ttu-id="aea62-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aea62-141">OUTPUTS</span></span>

### <span data-ttu-id="aea62-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aea62-142">System.Boolean</span></span>

## <span data-ttu-id="aea62-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="aea62-143">NOTES</span></span>

## <span data-ttu-id="aea62-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="aea62-144">RELATED LINKS</span></span>

[<span data-ttu-id="aea62-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="aea62-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


