---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 40477ad0635f1b832e7d95e459b27102dc68f8db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476793"
---
# <span data-ttu-id="5aab9-101">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5aab9-101">Remove-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="5aab9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5aab9-102">SYNOPSIS</span></span>
<span data-ttu-id="5aab9-103">Löscht eine Datei oder einen Ordner im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5aab9-103">Deletes a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5aab9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5aab9-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Clean]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5aab9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5aab9-105">DESCRIPTION</span></span>
<span data-ttu-id="5aab9-106">Das Cmdlet **Remove-AzureRmDataLakeStoreItem** löscht eine Datei oder einen Ordner im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5aab9-106">The **Remove-AzureRmDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5aab9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5aab9-107">EXAMPLES</span></span>

### <span data-ttu-id="5aab9-108">Beispiel 1: Entfernen mehrerer Elemente</span><span class="sxs-lookup"><span data-stu-id="5aab9-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="5aab9-109">Mit diesem Befehl werden die Dateien File01.txt und File.csv aus dem Data Lake Store entfernt.</span><span class="sxs-lookup"><span data-stu-id="5aab9-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="5aab9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5aab9-110">PARAMETERS</span></span>

### <span data-ttu-id="5aab9-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="5aab9-111">-Account</span></span>
<span data-ttu-id="5aab9-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="5aab9-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5aab9-113">-Clean</span><span class="sxs-lookup"><span data-stu-id="5aab9-113">-Clean</span></span>
<span data-ttu-id="5aab9-114">Gibt an, dass der Benutzer alle Inhalte des Ordners, aber nicht den Ordner selbst entfernen möchte.</span><span class="sxs-lookup"><span data-stu-id="5aab9-114">Indicates the user wants to remove all of the contents of the folder, but not the folder itself</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5aab9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aab9-115">-DefaultProfile</span></span>
<span data-ttu-id="5aab9-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5aab9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aab9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5aab9-117">-Force</span></span>
<span data-ttu-id="5aab9-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="5aab9-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5aab9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5aab9-119">-PassThru</span></span>
<span data-ttu-id="5aab9-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="5aab9-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5aab9-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="5aab9-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5aab9-122">-Pfade</span><span class="sxs-lookup"><span data-stu-id="5aab9-122">-Paths</span></span>
<span data-ttu-id="5aab9-123">Gibt ein Array von Data Lake Store-Pfaden der zu entfernenden Dateien an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="5aab9-123">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5aab9-124">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="5aab9-124">-Recurse</span></span>
<span data-ttu-id="5aab9-125">Gibt an, dass dieser Vorgang alle Elemente im Zielordner, einschließlich Unterordnern, löscht.</span><span class="sxs-lookup"><span data-stu-id="5aab9-125">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>
<span data-ttu-id="5aab9-126">Sofern Sie den Parameter *Clean* nicht angeben, wird der Zielordner ebenfalls gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5aab9-126">Unless you specify the *Clean* parameter, the target folder is also deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5aab9-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5aab9-127">-Confirm</span></span>
<span data-ttu-id="5aab9-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5aab9-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aab9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aab9-129">-WhatIf</span></span>
<span data-ttu-id="5aab9-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5aab9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5aab9-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5aab9-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aab9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aab9-132">CommonParameters</span></span>
<span data-ttu-id="5aab9-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5aab9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aab9-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5aab9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aab9-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5aab9-135">INPUTS</span></span>

### <span data-ttu-id="5aab9-136">Keine</span><span class="sxs-lookup"><span data-stu-id="5aab9-136">None</span></span>
<span data-ttu-id="5aab9-137">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="5aab9-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5aab9-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5aab9-138">OUTPUTS</span></span>

### <span data-ttu-id="5aab9-139">bool</span><span class="sxs-lookup"><span data-stu-id="5aab9-139">bool</span></span>
<span data-ttu-id="5aab9-140">Wenn passthru angegeben ist, wird das Ergebnis des Vorgangs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5aab9-140">If PassThru is specified, returns the result of the operation.</span></span>

## <span data-ttu-id="5aab9-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="5aab9-141">NOTES</span></span>

## <span data-ttu-id="5aab9-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5aab9-142">RELATED LINKS</span></span>

[<span data-ttu-id="5aab9-143">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5aab9-143">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5aab9-144">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5aab9-144">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5aab9-145">Importieren-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5aab9-145">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5aab9-146">Teilnehmen – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5aab9-146">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5aab9-147">Neu – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5aab9-147">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5aab9-148">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5aab9-148">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


