---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/join-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
ms.openlocfilehash: 1d361149109b654cf3e7fa45e133b9daff84c21c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155820"
---
# <span data-ttu-id="1dbdd-101">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1dbdd-101">Join-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="1dbdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dbdd-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbdd-103">Joins one or more files to create one file in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-103">Joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="1dbdd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1dbdd-104">SYNTAX</span></span>

```
Join-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dbdd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1dbdd-105">DESCRIPTION</span></span>
<span data-ttu-id="1dbdd-106">Das **Cmdlet "Join-AzDataLakeStoreItem"** joint eine oder mehrere Dateien, um eine Datei im Data Lake Store zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-106">The **Join-AzDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="1dbdd-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1dbdd-107">EXAMPLES</span></span>

### <span data-ttu-id="1dbdd-108">Beispiel 1: Verbinden von zwei Elementen</span><span class="sxs-lookup"><span data-stu-id="1dbdd-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="1dbdd-109">Mit diesem Befehl werden File01.txt und File02.txt zum Erstellen der Datei CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="1dbdd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dbdd-110">PARAMETERS</span></span>

### <span data-ttu-id="1dbdd-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="1dbdd-111">-Account</span></span>
<span data-ttu-id="1dbdd-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1dbdd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbdd-113">-DefaultProfile</span></span>
<span data-ttu-id="1dbdd-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dbdd-115">-Destination</span><span class="sxs-lookup"><span data-stu-id="1dbdd-115">-Destination</span></span>
<span data-ttu-id="1dbdd-116">Gibt den Data Lake Store-Pfad für das angeschlossene Element an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="1dbdd-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="1dbdd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1dbdd-117">-Force</span></span>
<span data-ttu-id="1dbdd-118">Gibt an, dass die Zieldatei durch diesen Vorgang überschrieben werden kann, wenn sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="1dbdd-119">-Paths</span><span class="sxs-lookup"><span data-stu-id="1dbdd-119">-Paths</span></span>
<span data-ttu-id="1dbdd-120">Gibt ein Array von Data Lake Store-Pfaden der zu kombinierenden Dateien an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="1dbdd-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dbdd-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1dbdd-121">-Confirm</span></span>
<span data-ttu-id="1dbdd-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dbdd-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1dbdd-123">-WhatIf</span></span>
<span data-ttu-id="1dbdd-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dbdd-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dbdd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbdd-126">CommonParameters</span></span>
<span data-ttu-id="1dbdd-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbdd-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dbdd-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbdd-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1dbdd-129">INPUTS</span></span>

### <span data-ttu-id="1dbdd-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1dbdd-130">System.String</span></span>

### <span data-ttu-id="1dbdd-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span><span class="sxs-lookup"><span data-stu-id="1dbdd-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="1dbdd-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="1dbdd-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="1dbdd-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1dbdd-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1dbdd-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1dbdd-134">OUTPUTS</span></span>

### <span data-ttu-id="1dbdd-135">System.String</span><span class="sxs-lookup"><span data-stu-id="1dbdd-135">System.String</span></span>

## <span data-ttu-id="1dbdd-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1dbdd-136">NOTES</span></span>

## <span data-ttu-id="1dbdd-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1dbdd-137">RELATED LINKS</span></span>

[<span data-ttu-id="1dbdd-138">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1dbdd-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="1dbdd-139">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1dbdd-139">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="1dbdd-140">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1dbdd-140">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="1dbdd-141">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1dbdd-141">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="1dbdd-142">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1dbdd-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="1dbdd-143">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1dbdd-143">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


