---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/move-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 5e6fb437833db3f4278335f67693d084c2d6d95b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662856"
---
# <span data-ttu-id="1bb02-101">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1bb02-101">Move-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="1bb02-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1bb02-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb02-103">Verschiebt oder benennt eine Datei oder einen Ordner im Data Lake Store um.</span><span class="sxs-lookup"><span data-stu-id="1bb02-103">Moves or renames a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bb02-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bb02-104">SYNTAX</span></span>

```
Move-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bb02-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1bb02-105">DESCRIPTION</span></span>
<span data-ttu-id="1bb02-106">Das Cmdlet **Move-AzureRmDataLakeStoreItem** verschiebt oder benennt eine Datei oder einen Ordner im Data Lake Store um.</span><span class="sxs-lookup"><span data-stu-id="1bb02-106">The **Move-AzureRmDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1bb02-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1bb02-107">EXAMPLES</span></span>

### <span data-ttu-id="1bb02-108">Beispiel 1: Verschieben und Umbenennen eines Elements</span><span class="sxs-lookup"><span data-stu-id="1bb02-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="1bb02-109">Mit diesem Befehl wird das Element File.txt in RenamedFile.txt umbenennen und in einen anderen Ordner verschoben.</span><span class="sxs-lookup"><span data-stu-id="1bb02-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="1bb02-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bb02-110">PARAMETERS</span></span>

### <span data-ttu-id="1bb02-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="1bb02-111">-Account</span></span>
<span data-ttu-id="1bb02-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="1bb02-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1bb02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bb02-113">-DefaultProfile</span></span>
<span data-ttu-id="1bb02-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1bb02-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bb02-115">-Ziel</span><span class="sxs-lookup"><span data-stu-id="1bb02-115">-Destination</span></span>
<span data-ttu-id="1bb02-116">Gibt den Daten See-Speicherpfad an, in den das Element verschoben werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="1bb02-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb02-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1bb02-117">-Force</span></span>
<span data-ttu-id="1bb02-118">Gibt an, dass dieser Vorgang die Zieldatei überschreiben kann, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1bb02-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="1bb02-119">-Path</span><span class="sxs-lookup"><span data-stu-id="1bb02-119">-Path</span></span>
<span data-ttu-id="1bb02-120">Gibt den Daten See-Speicherpfad des Elements an, das verschoben oder umbenannt werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="1bb02-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb02-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1bb02-121">-Confirm</span></span>
<span data-ttu-id="1bb02-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1bb02-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bb02-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bb02-123">-WhatIf</span></span>
<span data-ttu-id="1bb02-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1bb02-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bb02-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1bb02-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bb02-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb02-126">CommonParameters</span></span>
<span data-ttu-id="1bb02-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bb02-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb02-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bb02-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb02-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1bb02-129">INPUTS</span></span>

### <span data-ttu-id="1bb02-130">Keine</span><span class="sxs-lookup"><span data-stu-id="1bb02-130">None</span></span>
<span data-ttu-id="1bb02-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="1bb02-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1bb02-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1bb02-132">OUTPUTS</span></span>

### <span data-ttu-id="1bb02-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1bb02-133">string</span></span>
<span data-ttu-id="1bb02-134">Der vollständige Pfad zu der verschobenen Datei oder dem Ordner.</span><span class="sxs-lookup"><span data-stu-id="1bb02-134">The full path to the moved file or folder.</span></span>

## <span data-ttu-id="1bb02-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="1bb02-135">NOTES</span></span>

## <span data-ttu-id="1bb02-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1bb02-136">RELATED LINKS</span></span>

[<span data-ttu-id="1bb02-137">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1bb02-137">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="1bb02-138">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1bb02-138">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="1bb02-139">Importieren-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1bb02-139">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="1bb02-140">Neu – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1bb02-140">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="1bb02-141">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1bb02-141">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="1bb02-142">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1bb02-142">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


