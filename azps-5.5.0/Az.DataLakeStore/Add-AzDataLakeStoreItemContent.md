---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 3cf411e75e2a3ec430f13354015d5b6e271c840c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161924"
---
# <span data-ttu-id="dcc98-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="dcc98-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="dcc98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcc98-102">SYNOPSIS</span></span>
<span data-ttu-id="dcc98-103">Fügt einem Element in einem Data Lake Store Inhalte hinzu.</span><span class="sxs-lookup"><span data-stu-id="dcc98-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="dcc98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dcc98-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcc98-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dcc98-105">DESCRIPTION</span></span>
<span data-ttu-id="dcc98-106">Das **Cmdlet "Add-AzDataLakeStoreItemContent"** fügt einem Element in einem Azure Data Lake Store Inhalte hinzu.</span><span class="sxs-lookup"><span data-stu-id="dcc98-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="dcc98-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dcc98-107">EXAMPLES</span></span>

### <span data-ttu-id="dcc98-108">Beispiel 1: Hinzufügen von Inhalt zu einer Datei</span><span class="sxs-lookup"><span data-stu-id="dcc98-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="dcc98-109">Mit diesem Befehl wird dem Dateiinhalt Inhalt myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="dcc98-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="dcc98-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcc98-110">PARAMETERS</span></span>

### <span data-ttu-id="dcc98-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="dcc98-111">-Account</span></span>
<span data-ttu-id="dcc98-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="dcc98-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="dcc98-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcc98-113">-DefaultProfile</span></span>
<span data-ttu-id="dcc98-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="dcc98-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcc98-115">-Encoding</span><span class="sxs-lookup"><span data-stu-id="dcc98-115">-Encoding</span></span>
<span data-ttu-id="dcc98-116">Gibt die Codierung für das zu erstellende Element an.</span><span class="sxs-lookup"><span data-stu-id="dcc98-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="dcc98-117">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="dcc98-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dcc98-118">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="dcc98-118">Unknown</span></span>
- <span data-ttu-id="dcc98-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="dcc98-119">String</span></span>
- <span data-ttu-id="dcc98-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="dcc98-120">Unicode</span></span>
- <span data-ttu-id="dcc98-121">Byte</span><span class="sxs-lookup"><span data-stu-id="dcc98-121">Byte</span></span>
- <span data-ttu-id="dcc98-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="dcc98-122">BigEndianUnicode</span></span>
- <span data-ttu-id="dcc98-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="dcc98-123">UTF8</span></span>
- <span data-ttu-id="dcc98-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="dcc98-124">UTF7</span></span>
- <span data-ttu-id="dcc98-125">Ascii</span><span class="sxs-lookup"><span data-stu-id="dcc98-125">Ascii</span></span>
- <span data-ttu-id="dcc98-126">Standard</span><span class="sxs-lookup"><span data-stu-id="dcc98-126">Default</span></span>
- <span data-ttu-id="dcc98-127">Oem</span><span class="sxs-lookup"><span data-stu-id="dcc98-127">Oem</span></span>
- <span data-ttu-id="dcc98-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="dcc98-128">BigEndianUTF32</span></span>

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

### <span data-ttu-id="dcc98-129">-Path</span><span class="sxs-lookup"><span data-stu-id="dcc98-129">-Path</span></span>
<span data-ttu-id="dcc98-130">Gibt den Data Lake Store-Pfad des zu ändernden Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="dcc98-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="dcc98-131">-Value</span><span class="sxs-lookup"><span data-stu-id="dcc98-131">-Value</span></span>
<span data-ttu-id="dcc98-132">Gibt den Inhalt an, der dem Element hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dcc98-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="dcc98-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcc98-133">CommonParameters</span></span>
<span data-ttu-id="dcc98-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcc98-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcc98-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcc98-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcc98-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dcc98-136">INPUTS</span></span>

### <span data-ttu-id="dcc98-137">System.String</span><span class="sxs-lookup"><span data-stu-id="dcc98-137">System.String</span></span>

### <span data-ttu-id="dcc98-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="dcc98-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="dcc98-139">System.Object</span><span class="sxs-lookup"><span data-stu-id="dcc98-139">System.Object</span></span>

### <span data-ttu-id="dcc98-140">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="dcc98-140">System.Text.Encoding</span></span>

## <span data-ttu-id="dcc98-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dcc98-141">OUTPUTS</span></span>

### <span data-ttu-id="dcc98-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dcc98-142">System.Boolean</span></span>

## <span data-ttu-id="dcc98-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dcc98-143">NOTES</span></span>

## <span data-ttu-id="dcc98-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dcc98-144">RELATED LINKS</span></span>

[<span data-ttu-id="dcc98-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="dcc98-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


