---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: da26deb246fc90a1b83b63c47560dd5912616d62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502745"
---
# <span data-ttu-id="f3453-101">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f3453-101">Remove-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="f3453-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3453-102">SYNOPSIS</span></span>
<span data-ttu-id="f3453-103">Löscht eine Datei oder einen Ordner im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f3453-103">Deletes a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3453-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3453-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Clean]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3453-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3453-105">DESCRIPTION</span></span>
<span data-ttu-id="f3453-106">Das Cmdlet **Remove-AzureRmDataLakeStoreItem** löscht eine Datei oder einen Ordner im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f3453-106">The **Remove-AzureRmDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f3453-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3453-107">EXAMPLES</span></span>

### <span data-ttu-id="f3453-108">Beispiel 1: Entfernen mehrerer Elemente</span><span class="sxs-lookup"><span data-stu-id="f3453-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="f3453-109">Mit diesem Befehl werden die Dateien File01.txt und File.csv aus dem Data Lake Store entfernt.</span><span class="sxs-lookup"><span data-stu-id="f3453-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="f3453-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3453-110">PARAMETERS</span></span>

### <span data-ttu-id="f3453-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="f3453-111">-Account</span></span>
<span data-ttu-id="f3453-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="f3453-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f3453-113">-Clean</span><span class="sxs-lookup"><span data-stu-id="f3453-113">-Clean</span></span>
<span data-ttu-id="f3453-114">Gibt an, dass dieser Vorgang den gesamten Inhalt des Zielordners entfernt und den Ordner aufrecht erhält.</span><span class="sxs-lookup"><span data-stu-id="f3453-114">Indicates that this operation removes all of the contents of the target folder and retains the folder.</span></span>
<span data-ttu-id="f3453-115">Verwenden Sie diesen Parameter mit dem Parameter *recurse* .</span><span class="sxs-lookup"><span data-stu-id="f3453-115">Use this parameter with the *Recurse* parameter.</span></span>

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

### <span data-ttu-id="f3453-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f3453-116">-Force</span></span>
<span data-ttu-id="f3453-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f3453-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f3453-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3453-118">-PassThru</span></span>
<span data-ttu-id="f3453-119">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f3453-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f3453-120">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="f3453-120">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3453-121">-Pfade</span><span class="sxs-lookup"><span data-stu-id="f3453-121">-Paths</span></span>
<span data-ttu-id="f3453-122">Gibt ein Array von Data Lake Store-Pfaden der zu entfernenden Dateien an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="f3453-122">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3453-123">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="f3453-123">-Recurse</span></span>
<span data-ttu-id="f3453-124">Gibt an, dass dieser Vorgang alle Elemente im Zielordner, einschließlich Unterordnern, löscht.</span><span class="sxs-lookup"><span data-stu-id="f3453-124">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>
<span data-ttu-id="f3453-125">Sofern Sie den Parameter *Clean* nicht angeben, wird der Zielordner ebenfalls gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f3453-125">Unless you specify the *Clean* parameter, the target folder is also deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3453-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f3453-126">-Confirm</span></span>
<span data-ttu-id="f3453-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f3453-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3453-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3453-128">-WhatIf</span></span>
<span data-ttu-id="f3453-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f3453-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3453-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f3453-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3453-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3453-131">-DefaultProfile</span></span>
<span data-ttu-id="f3453-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3453-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3453-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3453-133">CommonParameters</span></span>
<span data-ttu-id="f3453-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3453-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3453-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3453-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3453-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3453-136">INPUTS</span></span>

## <span data-ttu-id="f3453-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3453-137">OUTPUTS</span></span>

### <span data-ttu-id="f3453-138">bool</span><span class="sxs-lookup"><span data-stu-id="f3453-138">bool</span></span>
<span data-ttu-id="f3453-139">Wenn passthru angegeben ist, wird das Ergebnis des Vorgangs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f3453-139">If PassThru is specified, returns the result of the operation.</span></span>

## <span data-ttu-id="f3453-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3453-140">NOTES</span></span>

## <span data-ttu-id="f3453-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3453-141">RELATED LINKS</span></span>

[<span data-ttu-id="f3453-142">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f3453-142">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f3453-143">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f3453-143">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f3453-144">Importieren-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f3453-144">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f3453-145">Teilnehmen – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f3453-145">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f3453-146">Neu – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f3453-146">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f3453-147">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f3453-147">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


