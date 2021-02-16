---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: e8e90b6cca2808bbf2caee69ebef5582ed0f8c5b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161876"
---
# <span data-ttu-id="29506-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="29506-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="29506-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29506-102">SYNOPSIS</span></span>
<span data-ttu-id="29506-103">Verschiebt eine Datei oder einen Ordner in Data Lake Store oder benennt sie um.</span><span class="sxs-lookup"><span data-stu-id="29506-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="29506-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29506-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29506-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29506-105">DESCRIPTION</span></span>
<span data-ttu-id="29506-106">Das **Cmdlet "Move-AzDataLakeStoreItem"** verschiebt oder benennt eine Datei oder einen Ordner im Data Lake Store um.</span><span class="sxs-lookup"><span data-stu-id="29506-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="29506-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="29506-107">EXAMPLES</span></span>

### <span data-ttu-id="29506-108">Beispiel 1: Verschieben und Umbenennen eines Elements</span><span class="sxs-lookup"><span data-stu-id="29506-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="29506-109">Mit diesem Befehl wird das Element File.txt in RenamedFile.txt in einen anderen Ordner verschoben.</span><span class="sxs-lookup"><span data-stu-id="29506-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="29506-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29506-110">PARAMETERS</span></span>

### <span data-ttu-id="29506-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="29506-111">-Account</span></span>
<span data-ttu-id="29506-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="29506-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="29506-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29506-113">-DefaultProfile</span></span>
<span data-ttu-id="29506-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29506-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29506-115">-Destination</span><span class="sxs-lookup"><span data-stu-id="29506-115">-Destination</span></span>
<span data-ttu-id="29506-116">Gibt den Data Lake Store-Pfad an, in den das Element zu verschieben ist, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="29506-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="29506-117">-Force</span><span class="sxs-lookup"><span data-stu-id="29506-117">-Force</span></span>
<span data-ttu-id="29506-118">Gibt an, dass die Zieldatei durch diesen Vorgang überschrieben werden kann, wenn sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="29506-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="29506-119">-Path</span><span class="sxs-lookup"><span data-stu-id="29506-119">-Path</span></span>
<span data-ttu-id="29506-120">Gibt den Data Lake Store-Pfad des zu verschiebenden oder umzubenennen Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="29506-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="29506-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29506-121">-Confirm</span></span>
<span data-ttu-id="29506-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29506-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29506-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="29506-123">-WhatIf</span></span>
<span data-ttu-id="29506-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29506-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29506-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29506-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29506-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29506-126">CommonParameters</span></span>
<span data-ttu-id="29506-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29506-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29506-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29506-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29506-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="29506-129">INPUTS</span></span>

### <span data-ttu-id="29506-130">System.String</span><span class="sxs-lookup"><span data-stu-id="29506-130">System.String</span></span>

### <span data-ttu-id="29506-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="29506-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="29506-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="29506-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="29506-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="29506-133">OUTPUTS</span></span>

### <span data-ttu-id="29506-134">System.String</span><span class="sxs-lookup"><span data-stu-id="29506-134">System.String</span></span>

## <span data-ttu-id="29506-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="29506-135">NOTES</span></span>

## <span data-ttu-id="29506-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="29506-136">RELATED LINKS</span></span>

[<span data-ttu-id="29506-137">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="29506-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="29506-138">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="29506-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="29506-139">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="29506-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="29506-140">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="29506-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="29506-141">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="29506-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="29506-142">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="29506-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


