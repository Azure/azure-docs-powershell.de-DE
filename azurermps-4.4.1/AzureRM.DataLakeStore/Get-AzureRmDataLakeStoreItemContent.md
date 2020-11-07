---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 3da97a14049671f8fff8bc03f7f32609f9b86984
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663960"
---
# <span data-ttu-id="4ae42-101">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="4ae42-101">Get-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="4ae42-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ae42-102">SYNOPSIS</span></span>
<span data-ttu-id="4ae42-103">Ruft den Inhalt einer Datei im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="4ae42-103">Gets the contents of a file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ae42-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ae42-104">SYNTAX</span></span>

### <span data-ttu-id="4ae42-105">Vorschau des Dateiinhalts (Standard)</span><span class="sxs-lookup"><span data-stu-id="4ae42-105">Preview file content (Default)</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ae42-106">Vorschau der Datei Zeilen vom Anfang der Datei</span><span class="sxs-lookup"><span data-stu-id="4ae42-106">Preview file rows from the head of the file</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ae42-107">Vorschau der Datei Zeilen vom Ende der Datei</span><span class="sxs-lookup"><span data-stu-id="4ae42-107">Preview file rows from the tail of the file</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ae42-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ae42-108">DESCRIPTION</span></span>
<span data-ttu-id="4ae42-109">Das Cmdlet " **Get-AzureRmDataLakeStoreItemContent** " Ruft den Inhalt einer Datei im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="4ae42-109">The **Get-AzureRmDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="4ae42-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ae42-110">EXAMPLES</span></span>

### <span data-ttu-id="4ae42-111">Beispiel 1: Abrufen des Inhalts einer Datei</span><span class="sxs-lookup"><span data-stu-id="4ae42-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="4ae42-112">Dieser Befehl ruft den Inhalt der Datei MyFile.txt im ContosoADL-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="4ae42-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="4ae42-113">Beispiel 2: Abrufen der ersten beiden Zeilen einer Datei</span><span class="sxs-lookup"><span data-stu-id="4ae42-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="4ae42-114">Dieser Befehl ruft die ersten beiden Zeilen in der Datei MyFile.txt im ContosoADL-Konto getrennt ab.</span><span class="sxs-lookup"><span data-stu-id="4ae42-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="4ae42-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ae42-115">PARAMETERS</span></span>

### <span data-ttu-id="4ae42-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="4ae42-116">-Account</span></span>
<span data-ttu-id="4ae42-117">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="4ae42-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="4ae42-118">-Encoding</span><span class="sxs-lookup"><span data-stu-id="4ae42-118">-Encoding</span></span>
<span data-ttu-id="4ae42-119">Gibt die Codierung für das zu erstellende Element an.</span><span class="sxs-lookup"><span data-stu-id="4ae42-119">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="4ae42-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4ae42-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4ae42-121">Unbekannten</span><span class="sxs-lookup"><span data-stu-id="4ae42-121">Unknown</span></span>
- <span data-ttu-id="4ae42-122">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4ae42-122">String</span></span>
- <span data-ttu-id="4ae42-123">Unicode</span><span class="sxs-lookup"><span data-stu-id="4ae42-123">Unicode</span></span>
- <span data-ttu-id="4ae42-124">Byte</span><span class="sxs-lookup"><span data-stu-id="4ae42-124">Byte</span></span>
- <span data-ttu-id="4ae42-125">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="4ae42-125">BigEndianUnicode</span></span>
- <span data-ttu-id="4ae42-126">UTF8</span><span class="sxs-lookup"><span data-stu-id="4ae42-126">UTF8</span></span>
- <span data-ttu-id="4ae42-127">UTF7</span><span class="sxs-lookup"><span data-stu-id="4ae42-127">UTF7</span></span>
- <span data-ttu-id="4ae42-128">ASCII</span><span class="sxs-lookup"><span data-stu-id="4ae42-128">Ascii</span></span>
- <span data-ttu-id="4ae42-129">Standard</span><span class="sxs-lookup"><span data-stu-id="4ae42-129">Default</span></span>
- <span data-ttu-id="4ae42-130">OEM</span><span class="sxs-lookup"><span data-stu-id="4ae42-130">Oem</span></span>
- <span data-ttu-id="4ae42-131">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="4ae42-131">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.PowerShell.Commands.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae42-132">-Force</span><span class="sxs-lookup"><span data-stu-id="4ae42-132">-Force</span></span>
<span data-ttu-id="4ae42-133">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="4ae42-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae42-134">-Head</span><span class="sxs-lookup"><span data-stu-id="4ae42-134">-Head</span></span>
<span data-ttu-id="4ae42-135">Die Anzahl der Zeilen (neue Zeile getrennt) vom Anfang der Datei bis zur Vorschau.</span><span class="sxs-lookup"><span data-stu-id="4ae42-135">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="4ae42-136">Wenn in den ersten 4MB-Daten keine neue Zeile gefunden wird, werden nur die Daten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4ae42-136">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Preview file rows from the head of the file
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae42-137">-Length</span><span class="sxs-lookup"><span data-stu-id="4ae42-137">-Length</span></span>
<span data-ttu-id="4ae42-138">Gibt die Länge des abzurufenden Inhalts in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="4ae42-138">Specifies the length, in bytes, of the content to get.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae42-139">-Offset</span><span class="sxs-lookup"><span data-stu-id="4ae42-139">-Offset</span></span>
<span data-ttu-id="4ae42-140">Gibt die Anzahl der Bytes an, die vor dem Abrufen von Inhalten in einer Datei übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4ae42-140">Specifies the number of bytes to skip in a file before getting content.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae42-141">-Path</span><span class="sxs-lookup"><span data-stu-id="4ae42-141">-Path</span></span>
<span data-ttu-id="4ae42-142">Gibt den Daten See-Speicherpfad einer Datei an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="4ae42-142">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="4ae42-143">-Tail</span><span class="sxs-lookup"><span data-stu-id="4ae42-143">-Tail</span></span>
<span data-ttu-id="4ae42-144">Die Anzahl der Zeilen (neue Zeile getrennt) vom Ende der Datei bis zur Vorschau.</span><span class="sxs-lookup"><span data-stu-id="4ae42-144">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="4ae42-145">Wenn in den ersten 4MB-Daten keine neue Zeile gefunden wird, werden nur die Daten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4ae42-145">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Preview file rows from the tail of the file
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae42-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4ae42-146">-Confirm</span></span>
<span data-ttu-id="4ae42-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ae42-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ae42-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ae42-148">-WhatIf</span></span>
<span data-ttu-id="4ae42-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ae42-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ae42-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ae42-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ae42-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ae42-151">-DefaultProfile</span></span>
<span data-ttu-id="4ae42-152">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ae42-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ae42-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ae42-153">CommonParameters</span></span>
<span data-ttu-id="4ae42-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ae42-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ae42-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ae42-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ae42-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ae42-156">INPUTS</span></span>

## <span data-ttu-id="4ae42-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ae42-157">OUTPUTS</span></span>

### <span data-ttu-id="4ae42-158">Byte []</span><span class="sxs-lookup"><span data-stu-id="4ae42-158">byte[]</span></span>
<span data-ttu-id="4ae42-159">Die Bytedatenstrom Darstellung des abgerufenen Dateiinhalts.</span><span class="sxs-lookup"><span data-stu-id="4ae42-159">The byte stream representation of the file contents retrieved.</span></span>

### <span data-ttu-id="4ae42-160">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4ae42-160">string</span></span>
<span data-ttu-id="4ae42-161">Die Zeichenfolgendarstellung (in der angegebenen Codierung) des abgerufenen Dateiinhalts.</span><span class="sxs-lookup"><span data-stu-id="4ae42-161">The string representation (in the specified encoding) of the file contents retrieved.</span></span>

## <span data-ttu-id="4ae42-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ae42-162">NOTES</span></span>

## <span data-ttu-id="4ae42-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ae42-163">RELATED LINKS</span></span>

