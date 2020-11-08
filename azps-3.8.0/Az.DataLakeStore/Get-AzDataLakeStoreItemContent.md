---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
ms.openlocfilehash: e5aaff4f915143e2e7695c9f650aed6fb01ba389
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995192"
---
# <span data-ttu-id="d2727-101">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="d2727-101">Get-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="d2727-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2727-102">SYNOPSIS</span></span>
<span data-ttu-id="d2727-103">Ruft den Inhalt einer Datei im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="d2727-103">Gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="d2727-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2727-104">SYNTAX</span></span>

### <span data-ttu-id="d2727-105">PreviewFileContent (Standard)</span><span class="sxs-lookup"><span data-stu-id="d2727-105">PreviewFileContent (Default)</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <Encoding>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2727-106">PreviewFileRowsFromHead</span><span class="sxs-lookup"><span data-stu-id="d2727-106">PreviewFileRowsFromHead</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2727-107">PreviewFileRowsFromTail</span><span class="sxs-lookup"><span data-stu-id="d2727-107">PreviewFileRowsFromTail</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2727-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2727-108">DESCRIPTION</span></span>
<span data-ttu-id="d2727-109">Das Cmdlet " **Get-AzDataLakeStoreItemContent** " Ruft den Inhalt einer Datei im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="d2727-109">The **Get-AzDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="d2727-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2727-110">EXAMPLES</span></span>

### <span data-ttu-id="d2727-111">Beispiel 1: Abrufen des Inhalts einer Datei</span><span class="sxs-lookup"><span data-stu-id="d2727-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="d2727-112">Dieser Befehl ruft den Inhalt der Datei MyFile.txt im ContosoADL-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="d2727-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="d2727-113">Beispiel 2: Abrufen der ersten beiden Zeilen einer Datei</span><span class="sxs-lookup"><span data-stu-id="d2727-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="d2727-114">Dieser Befehl ruft die ersten beiden Zeilen in der Datei MyFile.txt im ContosoADL-Konto getrennt ab.</span><span class="sxs-lookup"><span data-stu-id="d2727-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="d2727-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2727-115">PARAMETERS</span></span>

### <span data-ttu-id="d2727-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="d2727-116">-Account</span></span>
<span data-ttu-id="d2727-117">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="d2727-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d2727-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2727-118">-DefaultProfile</span></span>
<span data-ttu-id="d2727-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d2727-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2727-120">-Encoding</span><span class="sxs-lookup"><span data-stu-id="d2727-120">-Encoding</span></span>
<span data-ttu-id="d2727-121">Gibt die Codierung für das zu erstellende Element an.</span><span class="sxs-lookup"><span data-stu-id="d2727-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="d2727-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d2727-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d2727-123">Unbekannten</span><span class="sxs-lookup"><span data-stu-id="d2727-123">Unknown</span></span>
- <span data-ttu-id="d2727-124">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d2727-124">String</span></span>
- <span data-ttu-id="d2727-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2727-125">Unicode</span></span>
- <span data-ttu-id="d2727-126">Byte</span><span class="sxs-lookup"><span data-stu-id="d2727-126">Byte</span></span>
- <span data-ttu-id="d2727-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="d2727-127">BigEndianUnicode</span></span>
- <span data-ttu-id="d2727-128">UTF8</span><span class="sxs-lookup"><span data-stu-id="d2727-128">UTF8</span></span>
- <span data-ttu-id="d2727-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="d2727-129">UTF7</span></span>
- <span data-ttu-id="d2727-130">ASCII</span><span class="sxs-lookup"><span data-stu-id="d2727-130">Ascii</span></span>
- <span data-ttu-id="d2727-131">Standard</span><span class="sxs-lookup"><span data-stu-id="d2727-131">Default</span></span>
- <span data-ttu-id="d2727-132">OEM</span><span class="sxs-lookup"><span data-stu-id="d2727-132">Oem</span></span>
- <span data-ttu-id="d2727-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="d2727-133">BigEndianUTF32</span></span>

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2727-134">-Force</span><span class="sxs-lookup"><span data-stu-id="d2727-134">-Force</span></span>
<span data-ttu-id="d2727-135">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d2727-135">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2727-136">-Head</span><span class="sxs-lookup"><span data-stu-id="d2727-136">-Head</span></span>
<span data-ttu-id="d2727-137">Die Anzahl der Zeilen (neue Zeile getrennt) vom Anfang der Datei bis zur Vorschau.</span><span class="sxs-lookup"><span data-stu-id="d2727-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="d2727-138">Wenn in den ersten 4MB-Daten keine neue Zeile gefunden wird, werden nur die Daten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d2727-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: PreviewFileRowsFromHead
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2727-139">-Length</span><span class="sxs-lookup"><span data-stu-id="d2727-139">-Length</span></span>
<span data-ttu-id="d2727-140">Gibt die Länge des abzurufenden Inhalts in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="d2727-140">Specifies the length, in bytes, of the content to get.</span></span>

```yaml
Type: System.Int64
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2727-141">-Offset</span><span class="sxs-lookup"><span data-stu-id="d2727-141">-Offset</span></span>
<span data-ttu-id="d2727-142">Gibt die Anzahl der Bytes an, die vor dem Abrufen von Inhalten in einer Datei übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d2727-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

```yaml
Type: System.Int64
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2727-143">-Path</span><span class="sxs-lookup"><span data-stu-id="d2727-143">-Path</span></span>
<span data-ttu-id="d2727-144">Gibt den Daten See-Speicherpfad einer Datei an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="d2727-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d2727-145">-Tail</span><span class="sxs-lookup"><span data-stu-id="d2727-145">-Tail</span></span>
<span data-ttu-id="d2727-146">Die Anzahl der Zeilen (neue Zeile getrennt) vom Ende der Datei bis zur Vorschau.</span><span class="sxs-lookup"><span data-stu-id="d2727-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="d2727-147">Wenn in den ersten 4MB-Daten keine neue Zeile gefunden wird, werden nur die Daten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d2727-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: PreviewFileRowsFromTail
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2727-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d2727-148">-Confirm</span></span>
<span data-ttu-id="d2727-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d2727-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2727-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2727-150">-WhatIf</span></span>
<span data-ttu-id="d2727-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2727-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2727-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2727-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2727-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2727-153">CommonParameters</span></span>
<span data-ttu-id="d2727-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2727-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2727-155">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2727-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2727-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2727-156">INPUTS</span></span>

### <span data-ttu-id="d2727-157">System. String</span><span class="sxs-lookup"><span data-stu-id="d2727-157">System.String</span></span>

### <span data-ttu-id="d2727-158">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d2727-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d2727-159">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d2727-159">System.Int32</span></span>

### <span data-ttu-id="d2727-160">System. Int64</span><span class="sxs-lookup"><span data-stu-id="d2727-160">System.Int64</span></span>

### <span data-ttu-id="d2727-161">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="d2727-161">System.Text.Encoding</span></span>

### <span data-ttu-id="d2727-162">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="d2727-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d2727-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2727-163">OUTPUTS</span></span>

### <span data-ttu-id="d2727-164">System. Byte</span><span class="sxs-lookup"><span data-stu-id="d2727-164">System.Byte</span></span>

### <span data-ttu-id="d2727-165">System. String</span><span class="sxs-lookup"><span data-stu-id="d2727-165">System.String</span></span>

## <span data-ttu-id="d2727-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2727-166">NOTES</span></span>

## <span data-ttu-id="d2727-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2727-167">RELATED LINKS</span></span>
