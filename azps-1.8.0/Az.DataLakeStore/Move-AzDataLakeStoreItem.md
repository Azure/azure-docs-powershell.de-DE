---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: 8a8cc4d60bfba73b9cbcc9d323b063bff87f8a2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820171"
---
# <span data-ttu-id="88a6b-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="88a6b-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="88a6b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="88a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="88a6b-103">Verschiebt oder benennt eine Datei oder einen Ordner im Data Lake Store um.</span><span class="sxs-lookup"><span data-stu-id="88a6b-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="88a6b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="88a6b-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88a6b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88a6b-105">DESCRIPTION</span></span>
<span data-ttu-id="88a6b-106">Das Cmdlet **Move-AzDataLakeStoreItem** verschiebt oder benennt eine Datei oder einen Ordner im Data Lake Store um.</span><span class="sxs-lookup"><span data-stu-id="88a6b-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="88a6b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88a6b-107">EXAMPLES</span></span>

### <span data-ttu-id="88a6b-108">Beispiel 1: Verschieben und Umbenennen eines Elements</span><span class="sxs-lookup"><span data-stu-id="88a6b-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="88a6b-109">Mit diesem Befehl wird das Element File.txt in RenamedFile.txt umbenennen und in einen anderen Ordner verschoben.</span><span class="sxs-lookup"><span data-stu-id="88a6b-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="88a6b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="88a6b-110">PARAMETERS</span></span>

### <span data-ttu-id="88a6b-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="88a6b-111">-Account</span></span>
<span data-ttu-id="88a6b-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="88a6b-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="88a6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88a6b-113">-DefaultProfile</span></span>
<span data-ttu-id="88a6b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="88a6b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88a6b-115">-Ziel</span><span class="sxs-lookup"><span data-stu-id="88a6b-115">-Destination</span></span>
<span data-ttu-id="88a6b-116">Gibt den Daten See-Speicherpfad an, in den das Element verschoben werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="88a6b-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88a6b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="88a6b-117">-Force</span></span>
<span data-ttu-id="88a6b-118">Gibt an, dass dieser Vorgang die Zieldatei überschreiben kann, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="88a6b-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="88a6b-119">-Path</span><span class="sxs-lookup"><span data-stu-id="88a6b-119">-Path</span></span>
<span data-ttu-id="88a6b-120">Gibt den Daten See-Speicherpfad des Elements an, das verschoben oder umbenannt werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="88a6b-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="88a6b-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="88a6b-121">-Confirm</span></span>
<span data-ttu-id="88a6b-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="88a6b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88a6b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88a6b-123">-WhatIf</span></span>
<span data-ttu-id="88a6b-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88a6b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88a6b-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88a6b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88a6b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88a6b-126">CommonParameters</span></span>
<span data-ttu-id="88a6b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88a6b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88a6b-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88a6b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88a6b-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="88a6b-129">INPUTS</span></span>

### <span data-ttu-id="88a6b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="88a6b-130">System.String</span></span>

### <span data-ttu-id="88a6b-131">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="88a6b-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="88a6b-132">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="88a6b-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="88a6b-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="88a6b-133">OUTPUTS</span></span>

### <span data-ttu-id="88a6b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="88a6b-134">System.String</span></span>

## <span data-ttu-id="88a6b-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="88a6b-135">NOTES</span></span>

## <span data-ttu-id="88a6b-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="88a6b-136">RELATED LINKS</span></span>

[<span data-ttu-id="88a6b-137">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="88a6b-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="88a6b-138">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="88a6b-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="88a6b-139">Importieren-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="88a6b-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="88a6b-140">Neu – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="88a6b-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="88a6b-141">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="88a6b-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="88a6b-142">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="88a6b-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


