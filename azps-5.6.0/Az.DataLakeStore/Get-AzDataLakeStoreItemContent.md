---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 8f128396982be5e461e450d320c0264dddb09fa8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923787"
---
# <span data-ttu-id="b019c-101">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="b019c-101">Get-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="b019c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b019c-102">SYNOPSIS</span></span>
<span data-ttu-id="b019c-103">Ruft den Inhalt einer Datei im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="b019c-103">Gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="b019c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b019c-104">SYNTAX</span></span>

### <span data-ttu-id="b019c-105">PreviewFileContent (Standard)</span><span class="sxs-lookup"><span data-stu-id="b019c-105">PreviewFileContent (Default)</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <Encoding>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b019c-106">PreviewFileRowsFromHead</span><span class="sxs-lookup"><span data-stu-id="b019c-106">PreviewFileRowsFromHead</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b019c-107">PreviewFileRowsFromTail</span><span class="sxs-lookup"><span data-stu-id="b019c-107">PreviewFileRowsFromTail</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b019c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b019c-108">DESCRIPTION</span></span>
<span data-ttu-id="b019c-109">Das **Cmdlet Get-AzDataLakeStoreItemContent** ruft den Inhalt einer Datei im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="b019c-109">The **Get-AzDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="b019c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b019c-110">EXAMPLES</span></span>

### <span data-ttu-id="b019c-111">Beispiel 1: Herunterladen des Inhalts einer Datei</span><span class="sxs-lookup"><span data-stu-id="b019c-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="b019c-112">Dieser Befehl ruft den Inhalt der Datei ab, die MyFile.txt ContosoADL-Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="b019c-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="b019c-113">Beispiel 2: Herunterladen der ersten beiden Zeilen einer Datei</span><span class="sxs-lookup"><span data-stu-id="b019c-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="b019c-114">Mit diesem Befehl werden die ersten beiden zeilen voneinander getrennten Zeilen in der Datei MyFile.txt contosoADL-Konto.</span><span class="sxs-lookup"><span data-stu-id="b019c-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="b019c-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b019c-115">PARAMETERS</span></span>

### <span data-ttu-id="b019c-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="b019c-116">-Account</span></span>
<span data-ttu-id="b019c-117">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="b019c-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b019c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b019c-118">-DefaultProfile</span></span>
<span data-ttu-id="b019c-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b019c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b019c-120">-Encoding</span><span class="sxs-lookup"><span data-stu-id="b019c-120">-Encoding</span></span>
<span data-ttu-id="b019c-121">Gibt die Codierung für das zu erstellende Element an.</span><span class="sxs-lookup"><span data-stu-id="b019c-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="b019c-122">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="b019c-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b019c-123">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="b019c-123">Unknown</span></span>
- <span data-ttu-id="b019c-124">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b019c-124">String</span></span>
- <span data-ttu-id="b019c-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="b019c-125">Unicode</span></span>
- <span data-ttu-id="b019c-126">Byte</span><span class="sxs-lookup"><span data-stu-id="b019c-126">Byte</span></span>
- <span data-ttu-id="b019c-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="b019c-127">BigEndianUnicode</span></span>
- <span data-ttu-id="b019c-128">UTF8</span><span class="sxs-lookup"><span data-stu-id="b019c-128">UTF8</span></span>
- <span data-ttu-id="b019c-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="b019c-129">UTF7</span></span>
- <span data-ttu-id="b019c-130">Ascii</span><span class="sxs-lookup"><span data-stu-id="b019c-130">Ascii</span></span>
- <span data-ttu-id="b019c-131">Standard</span><span class="sxs-lookup"><span data-stu-id="b019c-131">Default</span></span>
- <span data-ttu-id="b019c-132">Oem</span><span class="sxs-lookup"><span data-stu-id="b019c-132">Oem</span></span>
- <span data-ttu-id="b019c-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="b019c-133">BigEndianUTF32</span></span>

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

### <span data-ttu-id="b019c-134">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="b019c-134">-Force</span></span>
<span data-ttu-id="b019c-135">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="b019c-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b019c-136">-Head</span><span class="sxs-lookup"><span data-stu-id="b019c-136">-Head</span></span>
<span data-ttu-id="b019c-137">Die Anzahl der Zeilen (durch Trennzeichen für neue Zeile) vom Anfang der Datei bis zur Vorschau.</span><span class="sxs-lookup"><span data-stu-id="b019c-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="b019c-138">Wenn in den ersten 4 MB daten keine neue Zeile gefunden wird, werden nur diese Daten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b019c-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

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

### <span data-ttu-id="b019c-139">-Length</span><span class="sxs-lookup"><span data-stu-id="b019c-139">-Length</span></span>
<span data-ttu-id="b019c-140">Gibt die Länge (in Bytes) des zu erhaltenden Inhalts an.</span><span class="sxs-lookup"><span data-stu-id="b019c-140">Specifies the length, in bytes, of the content to get.</span></span>

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

### <span data-ttu-id="b019c-141">-Offset</span><span class="sxs-lookup"><span data-stu-id="b019c-141">-Offset</span></span>
<span data-ttu-id="b019c-142">Gibt die Anzahl der Bytes an, die in einer Datei vor dem Abrufen von Inhalten übersprungen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b019c-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

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

### <span data-ttu-id="b019c-143">-Path</span><span class="sxs-lookup"><span data-stu-id="b019c-143">-Path</span></span>
<span data-ttu-id="b019c-144">Gibt den Data Lake Store-Pfad einer Datei an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="b019c-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b019c-145">-Tail</span><span class="sxs-lookup"><span data-stu-id="b019c-145">-Tail</span></span>
<span data-ttu-id="b019c-146">Die Anzahl der Zeilen (durch Trennzeichen für neue Zeile) vom Ende der Datei bis zur Vorschau.</span><span class="sxs-lookup"><span data-stu-id="b019c-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="b019c-147">Wenn in den ersten 4 MB daten keine neue Zeile gefunden wird, werden nur diese Daten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b019c-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

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

### <span data-ttu-id="b019c-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b019c-148">-Confirm</span></span>
<span data-ttu-id="b019c-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b019c-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b019c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b019c-150">-WhatIf</span></span>
<span data-ttu-id="b019c-151">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b019c-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b019c-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b019c-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b019c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b019c-153">CommonParameters</span></span>
<span data-ttu-id="b019c-154">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b019c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b019c-155">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b019c-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b019c-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b019c-156">INPUTS</span></span>

### <span data-ttu-id="b019c-157">System.String</span><span class="sxs-lookup"><span data-stu-id="b019c-157">System.String</span></span>

### <span data-ttu-id="b019c-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="b019c-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="b019c-159">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b019c-159">System.Int32</span></span>

### <span data-ttu-id="b019c-160">System.Int64</span><span class="sxs-lookup"><span data-stu-id="b019c-160">System.Int64</span></span>

### <span data-ttu-id="b019c-161">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="b019c-161">System.Text.Encoding</span></span>

### <span data-ttu-id="b019c-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b019c-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b019c-163">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b019c-163">OUTPUTS</span></span>

### <span data-ttu-id="b019c-164">System.Byte</span><span class="sxs-lookup"><span data-stu-id="b019c-164">System.Byte</span></span>

### <span data-ttu-id="b019c-165">System.String</span><span class="sxs-lookup"><span data-stu-id="b019c-165">System.String</span></span>

## <span data-ttu-id="b019c-166">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b019c-166">NOTES</span></span>

## <span data-ttu-id="b019c-167">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b019c-167">RELATED LINKS</span></span>
