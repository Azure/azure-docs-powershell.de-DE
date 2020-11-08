---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: e8e90b6cca2808bbf2caee69ebef5582ed0f8c5b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165826"
---
# <span data-ttu-id="de764-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="de764-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="de764-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="de764-102">SYNOPSIS</span></span>
<span data-ttu-id="de764-103">Verschiebt oder benennt eine Datei oder einen Ordner im Data Lake Store um.</span><span class="sxs-lookup"><span data-stu-id="de764-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="de764-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="de764-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de764-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de764-105">DESCRIPTION</span></span>
<span data-ttu-id="de764-106">Das Cmdlet **Move-AzDataLakeStoreItem** verschiebt oder benennt eine Datei oder einen Ordner im Data Lake Store um.</span><span class="sxs-lookup"><span data-stu-id="de764-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="de764-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de764-107">EXAMPLES</span></span>

### <span data-ttu-id="de764-108">Beispiel 1: Verschieben und Umbenennen eines Elements</span><span class="sxs-lookup"><span data-stu-id="de764-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="de764-109">Mit diesem Befehl wird das Element File.txt in RenamedFile.txt umbenennen und in einen anderen Ordner verschoben.</span><span class="sxs-lookup"><span data-stu-id="de764-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="de764-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="de764-110">PARAMETERS</span></span>

### <span data-ttu-id="de764-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="de764-111">-Account</span></span>
<span data-ttu-id="de764-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="de764-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="de764-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de764-113">-DefaultProfile</span></span>
<span data-ttu-id="de764-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="de764-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de764-115">-Ziel</span><span class="sxs-lookup"><span data-stu-id="de764-115">-Destination</span></span>
<span data-ttu-id="de764-116">Gibt den Daten See-Speicherpfad an, in den das Element verschoben werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="de764-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="de764-117">-Force</span><span class="sxs-lookup"><span data-stu-id="de764-117">-Force</span></span>
<span data-ttu-id="de764-118">Gibt an, dass dieser Vorgang die Zieldatei überschreiben kann, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="de764-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="de764-119">-Path</span><span class="sxs-lookup"><span data-stu-id="de764-119">-Path</span></span>
<span data-ttu-id="de764-120">Gibt den Daten See-Speicherpfad des Elements an, das verschoben oder umbenannt werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="de764-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="de764-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="de764-121">-Confirm</span></span>
<span data-ttu-id="de764-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="de764-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de764-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de764-123">-WhatIf</span></span>
<span data-ttu-id="de764-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="de764-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de764-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="de764-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de764-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de764-126">CommonParameters</span></span>
<span data-ttu-id="de764-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de764-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de764-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de764-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de764-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="de764-129">INPUTS</span></span>

### <span data-ttu-id="de764-130">System. String</span><span class="sxs-lookup"><span data-stu-id="de764-130">System.String</span></span>

### <span data-ttu-id="de764-131">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="de764-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="de764-132">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="de764-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="de764-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="de764-133">OUTPUTS</span></span>

### <span data-ttu-id="de764-134">System. String</span><span class="sxs-lookup"><span data-stu-id="de764-134">System.String</span></span>

## <span data-ttu-id="de764-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="de764-135">NOTES</span></span>

## <span data-ttu-id="de764-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="de764-136">RELATED LINKS</span></span>

[<span data-ttu-id="de764-137">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="de764-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="de764-138">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="de764-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="de764-139">Importieren-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="de764-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="de764-140">Neu – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="de764-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="de764-141">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="de764-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="de764-142">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="de764-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


