---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
ms.openlocfilehash: e5aaff4f915143e2e7695c9f650aed6fb01ba389
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458081"
---
# <span data-ttu-id="79868-101">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="79868-101">Get-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="79868-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79868-102">SYNOPSIS</span></span>
<span data-ttu-id="79868-103">Ruft den Inhalt einer Datei im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="79868-103">Gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="79868-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79868-104">SYNTAX</span></span>

### <span data-ttu-id="79868-105">PreviewFileContent (Standard)</span><span class="sxs-lookup"><span data-stu-id="79868-105">PreviewFileContent (Default)</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <Encoding>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79868-106">PreviewFileRowsFromHead</span><span class="sxs-lookup"><span data-stu-id="79868-106">PreviewFileRowsFromHead</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79868-107">PreviewFileRowsFromTail</span><span class="sxs-lookup"><span data-stu-id="79868-107">PreviewFileRowsFromTail</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79868-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79868-108">DESCRIPTION</span></span>
<span data-ttu-id="79868-109">Das **Cmdlet "Get-AzDataLakeStoreItemContent"** ruft den Inhalt einer Datei im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="79868-109">The **Get-AzDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="79868-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="79868-110">EXAMPLES</span></span>

### <span data-ttu-id="79868-111">Beispiel 1: Herunterladen des Inhalts einer Datei</span><span class="sxs-lookup"><span data-stu-id="79868-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="79868-112">Mit diesem Befehl wird der Inhalt der Datei MyFile.txt contosoADL-Konto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="79868-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="79868-113">Beispiel 2: Erstellen der ersten beiden Zeilen einer Datei</span><span class="sxs-lookup"><span data-stu-id="79868-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="79868-114">Mit diesem Befehl werden die ersten beiden zeilenweise getrennten Zeilen in der Datei MyFile.txt ContosoADL-Konto.</span><span class="sxs-lookup"><span data-stu-id="79868-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="79868-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79868-115">PARAMETERS</span></span>

### <span data-ttu-id="79868-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="79868-116">-Account</span></span>
<span data-ttu-id="79868-117">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="79868-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="79868-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79868-118">-DefaultProfile</span></span>
<span data-ttu-id="79868-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79868-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79868-120">-Encoding</span><span class="sxs-lookup"><span data-stu-id="79868-120">-Encoding</span></span>
<span data-ttu-id="79868-121">Gibt die Codierung für das zu erstellende Element an.</span><span class="sxs-lookup"><span data-stu-id="79868-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="79868-122">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="79868-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="79868-123">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="79868-123">Unknown</span></span>
- <span data-ttu-id="79868-124">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="79868-124">String</span></span>
- <span data-ttu-id="79868-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="79868-125">Unicode</span></span>
- <span data-ttu-id="79868-126">Byte</span><span class="sxs-lookup"><span data-stu-id="79868-126">Byte</span></span>
- <span data-ttu-id="79868-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="79868-127">BigEndianUnicode</span></span>
- <span data-ttu-id="79868-128">UTF8</span><span class="sxs-lookup"><span data-stu-id="79868-128">UTF8</span></span>
- <span data-ttu-id="79868-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="79868-129">UTF7</span></span>
- <span data-ttu-id="79868-130">Ascii</span><span class="sxs-lookup"><span data-stu-id="79868-130">Ascii</span></span>
- <span data-ttu-id="79868-131">Standard</span><span class="sxs-lookup"><span data-stu-id="79868-131">Default</span></span>
- <span data-ttu-id="79868-132">Oem</span><span class="sxs-lookup"><span data-stu-id="79868-132">Oem</span></span>
- <span data-ttu-id="79868-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="79868-133">BigEndianUTF32</span></span>

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

### <span data-ttu-id="79868-134">-Force</span><span class="sxs-lookup"><span data-stu-id="79868-134">-Force</span></span>
<span data-ttu-id="79868-135">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="79868-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="79868-136">-Head</span><span class="sxs-lookup"><span data-stu-id="79868-136">-Head</span></span>
<span data-ttu-id="79868-137">Die Anzahl der Zeilen (durch Trennzeichen in neuer Zeile) vom Anfang der Datei bis zur Vorschau.</span><span class="sxs-lookup"><span data-stu-id="79868-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="79868-138">Wenn in den ersten 4 MB daten keine neue Zeile gefunden wird, werden nur diese Daten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="79868-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

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

### <span data-ttu-id="79868-139">-Length</span><span class="sxs-lookup"><span data-stu-id="79868-139">-Length</span></span>
<span data-ttu-id="79868-140">Gibt die Länge (in Bytes) des zu erhaltenden Inhalts an.</span><span class="sxs-lookup"><span data-stu-id="79868-140">Specifies the length, in bytes, of the content to get.</span></span>

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

### <span data-ttu-id="79868-141">-Offset</span><span class="sxs-lookup"><span data-stu-id="79868-141">-Offset</span></span>
<span data-ttu-id="79868-142">Gibt die Anzahl der Bytes an, die in einer Datei vor dem Abrufen von Inhalten übersprungen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="79868-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

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

### <span data-ttu-id="79868-143">-Path</span><span class="sxs-lookup"><span data-stu-id="79868-143">-Path</span></span>
<span data-ttu-id="79868-144">Gibt den Data Lake Store-Pfad einer Datei an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="79868-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="79868-145">-Tail</span><span class="sxs-lookup"><span data-stu-id="79868-145">-Tail</span></span>
<span data-ttu-id="79868-146">Die Anzahl der Zeilen (durch Trennzeichen für neue Zeile) vom Ende der Datei bis zur Vorschau.</span><span class="sxs-lookup"><span data-stu-id="79868-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="79868-147">Wenn in den ersten 4 MB daten keine neue Zeile gefunden wird, werden nur diese Daten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="79868-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

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

### <span data-ttu-id="79868-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79868-148">-Confirm</span></span>
<span data-ttu-id="79868-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="79868-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79868-150">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="79868-150">-WhatIf</span></span>
<span data-ttu-id="79868-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="79868-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79868-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79868-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79868-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79868-153">CommonParameters</span></span>
<span data-ttu-id="79868-154">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79868-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79868-155">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79868-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79868-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="79868-156">INPUTS</span></span>

### <span data-ttu-id="79868-157">System.String</span><span class="sxs-lookup"><span data-stu-id="79868-157">System.String</span></span>

### <span data-ttu-id="79868-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="79868-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="79868-159">System.Int32</span><span class="sxs-lookup"><span data-stu-id="79868-159">System.Int32</span></span>

### <span data-ttu-id="79868-160">System.Int64</span><span class="sxs-lookup"><span data-stu-id="79868-160">System.Int64</span></span>

### <span data-ttu-id="79868-161">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="79868-161">System.Text.Encoding</span></span>

### <span data-ttu-id="79868-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="79868-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="79868-163">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="79868-163">OUTPUTS</span></span>

### <span data-ttu-id="79868-164">System.Byte</span><span class="sxs-lookup"><span data-stu-id="79868-164">System.Byte</span></span>

### <span data-ttu-id="79868-165">System.String</span><span class="sxs-lookup"><span data-stu-id="79868-165">System.String</span></span>

## <span data-ttu-id="79868-166">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="79868-166">NOTES</span></span>

## <span data-ttu-id="79868-167">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="79868-167">RELATED LINKS</span></span>
