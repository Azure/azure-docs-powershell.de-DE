---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 857f91cd8847e97dadf90c063ffc7b0e0366dab9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820187"
---
# <span data-ttu-id="5faeb-101">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="5faeb-101">Get-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="5faeb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5faeb-102">SYNOPSIS</span></span>
<span data-ttu-id="5faeb-103">Ruft den Inhalt einer Datei im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="5faeb-103">Gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="5faeb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5faeb-104">SYNTAX</span></span>

### <span data-ttu-id="5faeb-105">PreviewFileContent (Standard)</span><span class="sxs-lookup"><span data-stu-id="5faeb-105">PreviewFileContent (Default)</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <Encoding>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5faeb-106">PreviewFileRowsFromHead</span><span class="sxs-lookup"><span data-stu-id="5faeb-106">PreviewFileRowsFromHead</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5faeb-107">PreviewFileRowsFromTail</span><span class="sxs-lookup"><span data-stu-id="5faeb-107">PreviewFileRowsFromTail</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5faeb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5faeb-108">DESCRIPTION</span></span>
<span data-ttu-id="5faeb-109">Das Cmdlet " **Get-AzDataLakeStoreItemContent** " Ruft den Inhalt einer Datei im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="5faeb-109">The **Get-AzDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="5faeb-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5faeb-110">EXAMPLES</span></span>

### <span data-ttu-id="5faeb-111">Beispiel 1: Abrufen des Inhalts einer Datei</span><span class="sxs-lookup"><span data-stu-id="5faeb-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="5faeb-112">Dieser Befehl ruft den Inhalt der Datei MyFile.txt im ContosoADL-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="5faeb-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="5faeb-113">Beispiel 2: Abrufen der ersten beiden Zeilen einer Datei</span><span class="sxs-lookup"><span data-stu-id="5faeb-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="5faeb-114">Dieser Befehl ruft die ersten beiden Zeilen in der Datei MyFile.txt im ContosoADL-Konto getrennt ab.</span><span class="sxs-lookup"><span data-stu-id="5faeb-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="5faeb-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5faeb-115">PARAMETERS</span></span>

### <span data-ttu-id="5faeb-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="5faeb-116">-Account</span></span>
<span data-ttu-id="5faeb-117">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="5faeb-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5faeb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5faeb-118">-DefaultProfile</span></span>
<span data-ttu-id="5faeb-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5faeb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5faeb-120">-Encoding</span><span class="sxs-lookup"><span data-stu-id="5faeb-120">-Encoding</span></span>
<span data-ttu-id="5faeb-121">Gibt die Codierung für das zu erstellende Element an.</span><span class="sxs-lookup"><span data-stu-id="5faeb-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="5faeb-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5faeb-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5faeb-123">Unbekannten</span><span class="sxs-lookup"><span data-stu-id="5faeb-123">Unknown</span></span>
- <span data-ttu-id="5faeb-124">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5faeb-124">String</span></span>
- <span data-ttu-id="5faeb-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="5faeb-125">Unicode</span></span>
- <span data-ttu-id="5faeb-126">Byte</span><span class="sxs-lookup"><span data-stu-id="5faeb-126">Byte</span></span>
- <span data-ttu-id="5faeb-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="5faeb-127">BigEndianUnicode</span></span>
- <span data-ttu-id="5faeb-128">UTF8</span><span class="sxs-lookup"><span data-stu-id="5faeb-128">UTF8</span></span>
- <span data-ttu-id="5faeb-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="5faeb-129">UTF7</span></span>
- <span data-ttu-id="5faeb-130">ASCII</span><span class="sxs-lookup"><span data-stu-id="5faeb-130">Ascii</span></span>
- <span data-ttu-id="5faeb-131">Standard</span><span class="sxs-lookup"><span data-stu-id="5faeb-131">Default</span></span>
- <span data-ttu-id="5faeb-132">OEM</span><span class="sxs-lookup"><span data-stu-id="5faeb-132">Oem</span></span>
- <span data-ttu-id="5faeb-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="5faeb-133">BigEndianUTF32</span></span>

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

### <span data-ttu-id="5faeb-134">-Force</span><span class="sxs-lookup"><span data-stu-id="5faeb-134">-Force</span></span>
<span data-ttu-id="5faeb-135">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="5faeb-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5faeb-136">-Head</span><span class="sxs-lookup"><span data-stu-id="5faeb-136">-Head</span></span>
<span data-ttu-id="5faeb-137">Die Anzahl der Zeilen (neue Zeile getrennt) vom Anfang der Datei bis zur Vorschau.</span><span class="sxs-lookup"><span data-stu-id="5faeb-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="5faeb-138">Wenn in den ersten 4MB-Daten keine neue Zeile gefunden wird, werden nur die Daten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5faeb-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

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

### <span data-ttu-id="5faeb-139">-Length</span><span class="sxs-lookup"><span data-stu-id="5faeb-139">-Length</span></span>
<span data-ttu-id="5faeb-140">Gibt die Länge des abzurufenden Inhalts in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="5faeb-140">Specifies the length, in bytes, of the content to get.</span></span>

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

### <span data-ttu-id="5faeb-141">-Offset</span><span class="sxs-lookup"><span data-stu-id="5faeb-141">-Offset</span></span>
<span data-ttu-id="5faeb-142">Gibt die Anzahl der Bytes an, die vor dem Abrufen von Inhalten in einer Datei übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5faeb-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

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

### <span data-ttu-id="5faeb-143">-Path</span><span class="sxs-lookup"><span data-stu-id="5faeb-143">-Path</span></span>
<span data-ttu-id="5faeb-144">Gibt den Daten See-Speicherpfad einer Datei an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="5faeb-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="5faeb-145">-Tail</span><span class="sxs-lookup"><span data-stu-id="5faeb-145">-Tail</span></span>
<span data-ttu-id="5faeb-146">Die Anzahl der Zeilen (neue Zeile getrennt) vom Ende der Datei bis zur Vorschau.</span><span class="sxs-lookup"><span data-stu-id="5faeb-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="5faeb-147">Wenn in den ersten 4MB-Daten keine neue Zeile gefunden wird, werden nur die Daten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5faeb-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

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

### <span data-ttu-id="5faeb-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5faeb-148">-Confirm</span></span>
<span data-ttu-id="5faeb-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5faeb-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5faeb-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5faeb-150">-WhatIf</span></span>
<span data-ttu-id="5faeb-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5faeb-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5faeb-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5faeb-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5faeb-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5faeb-153">CommonParameters</span></span>
<span data-ttu-id="5faeb-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5faeb-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5faeb-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5faeb-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5faeb-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5faeb-156">INPUTS</span></span>

### <span data-ttu-id="5faeb-157">System. String</span><span class="sxs-lookup"><span data-stu-id="5faeb-157">System.String</span></span>

### <span data-ttu-id="5faeb-158">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="5faeb-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="5faeb-159">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5faeb-159">System.Int32</span></span>

### <span data-ttu-id="5faeb-160">System. Int64</span><span class="sxs-lookup"><span data-stu-id="5faeb-160">System.Int64</span></span>

### <span data-ttu-id="5faeb-161">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="5faeb-161">System.Text.Encoding</span></span>

### <span data-ttu-id="5faeb-162">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="5faeb-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5faeb-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5faeb-163">OUTPUTS</span></span>

### <span data-ttu-id="5faeb-164">System. Byte</span><span class="sxs-lookup"><span data-stu-id="5faeb-164">System.Byte</span></span>

### <span data-ttu-id="5faeb-165">System. String</span><span class="sxs-lookup"><span data-stu-id="5faeb-165">System.String</span></span>

## <span data-ttu-id="5faeb-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="5faeb-166">NOTES</span></span>

## <span data-ttu-id="5faeb-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5faeb-167">RELATED LINKS</span></span>
