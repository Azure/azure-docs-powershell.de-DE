---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: 222df24f2d3db296ce116e49da8baeb3e22ec699
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651528"
---
# <span data-ttu-id="f0349-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f0349-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="f0349-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f0349-102">SYNOPSIS</span></span>
<span data-ttu-id="f0349-103">Erstellt eine neue Datei oder einen neuen Ordner im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f0349-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f0349-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0349-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0349-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0349-105">DESCRIPTION</span></span>
<span data-ttu-id="f0349-106">Das Cmdlet **New-AzDataLakeStoreItem** erstellt eine neue Datei oder einen neuen Ordner im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f0349-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f0349-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0349-107">EXAMPLES</span></span>

### <span data-ttu-id="f0349-108">Beispiel 1: Erstellen einer neuen Datei und eines neuen Ordners</span><span class="sxs-lookup"><span data-stu-id="f0349-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="f0349-109">Mit dem ersten Befehl wird die Datei NewFile.txt für das angegebene Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="f0349-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="f0349-110">Mit dem zweiten Befehl wird der Ordner "Ordner" im Stammordner erstellt.</span><span class="sxs-lookup"><span data-stu-id="f0349-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="f0349-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0349-111">PARAMETERS</span></span>

### <span data-ttu-id="f0349-112">-Konto</span><span class="sxs-lookup"><span data-stu-id="f0349-112">-Account</span></span>
<span data-ttu-id="f0349-113">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="f0349-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f0349-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0349-114">-DefaultProfile</span></span>
<span data-ttu-id="f0349-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f0349-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0349-116">-Encoding</span><span class="sxs-lookup"><span data-stu-id="f0349-116">-Encoding</span></span>
<span data-ttu-id="f0349-117">Gibt die Codierung für das zu erstellende Element an.</span><span class="sxs-lookup"><span data-stu-id="f0349-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="f0349-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f0349-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f0349-119">Unbekannten</span><span class="sxs-lookup"><span data-stu-id="f0349-119">Unknown</span></span>
- <span data-ttu-id="f0349-120">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f0349-120">String</span></span>
- <span data-ttu-id="f0349-121">Unicode</span><span class="sxs-lookup"><span data-stu-id="f0349-121">Unicode</span></span>
- <span data-ttu-id="f0349-122">Byte</span><span class="sxs-lookup"><span data-stu-id="f0349-122">Byte</span></span>
- <span data-ttu-id="f0349-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="f0349-123">BigEndianUnicode</span></span>
- <span data-ttu-id="f0349-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="f0349-124">UTF8</span></span>
- <span data-ttu-id="f0349-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="f0349-125">UTF7</span></span>
- <span data-ttu-id="f0349-126">ASCII</span><span class="sxs-lookup"><span data-stu-id="f0349-126">Ascii</span></span>
- <span data-ttu-id="f0349-127">Standard</span><span class="sxs-lookup"><span data-stu-id="f0349-127">Default</span></span>
- <span data-ttu-id="f0349-128">OEM</span><span class="sxs-lookup"><span data-stu-id="f0349-128">Oem</span></span>
- <span data-ttu-id="f0349-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="f0349-129">BigEndianUTF32</span></span>

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

### <span data-ttu-id="f0349-130">-Folder</span><span class="sxs-lookup"><span data-stu-id="f0349-130">-Folder</span></span>
<span data-ttu-id="f0349-131">Gibt an, dass dieser Vorgang einen Ordner erstellt.</span><span class="sxs-lookup"><span data-stu-id="f0349-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="f0349-132">-Force</span><span class="sxs-lookup"><span data-stu-id="f0349-132">-Force</span></span>
<span data-ttu-id="f0349-133">Gibt an, dass dieser Vorgang das Zielelement überschreiben kann, wenn es bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f0349-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="f0349-134">-Path</span><span class="sxs-lookup"><span data-stu-id="f0349-134">-Path</span></span>
<span data-ttu-id="f0349-135">Gibt den Daten See-Speicherpfad des zu erstellenden Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="f0349-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f0349-136">-Wert</span><span class="sxs-lookup"><span data-stu-id="f0349-136">-Value</span></span>
<span data-ttu-id="f0349-137">Gibt den Inhalt an, der dem erstellten Element hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0349-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="f0349-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f0349-138">-Confirm</span></span>
<span data-ttu-id="f0349-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0349-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0349-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0349-140">-WhatIf</span></span>
<span data-ttu-id="f0349-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0349-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0349-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0349-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0349-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0349-143">CommonParameters</span></span>
<span data-ttu-id="f0349-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0349-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0349-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0349-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0349-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f0349-146">INPUTS</span></span>

### <span data-ttu-id="f0349-147">System. String</span><span class="sxs-lookup"><span data-stu-id="f0349-147">System.String</span></span>

### <span data-ttu-id="f0349-148">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="f0349-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="f0349-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="f0349-149">System.Object</span></span>

### <span data-ttu-id="f0349-150">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="f0349-150">System.Text.Encoding</span></span>

### <span data-ttu-id="f0349-151">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="f0349-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f0349-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f0349-152">OUTPUTS</span></span>

### <span data-ttu-id="f0349-153">System. String</span><span class="sxs-lookup"><span data-stu-id="f0349-153">System.String</span></span>

## <span data-ttu-id="f0349-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="f0349-154">NOTES</span></span>

## <span data-ttu-id="f0349-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f0349-155">RELATED LINKS</span></span>

[<span data-ttu-id="f0349-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f0349-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="f0349-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f0349-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="f0349-158">Importieren-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f0349-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="f0349-159">Neu – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f0349-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="f0349-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f0349-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="f0349-161">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f0349-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


