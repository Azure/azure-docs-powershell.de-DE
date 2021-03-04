---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
ms.openlocfilehash: c3ce4a8051867b535ba2aff4429b5bcfa0b9ab53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947928"
---
# <span data-ttu-id="e1f15-101">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e1f15-101">Remove-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="e1f15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1f15-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f15-103">Löscht eine Datei oder einen Ordner im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e1f15-103">Deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e1f15-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1f15-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1f15-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1f15-105">DESCRIPTION</span></span>
<span data-ttu-id="e1f15-106">Das **Cmdlet Remove-AzDataLakeStoreItem** löscht eine Datei oder einen Ordner im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e1f15-106">The **Remove-AzDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e1f15-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e1f15-107">EXAMPLES</span></span>

### <span data-ttu-id="e1f15-108">Beispiel 1: Entfernen mehrerer Elemente</span><span class="sxs-lookup"><span data-stu-id="e1f15-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="e1f15-109">Mit diesem Befehl werden die Dateien File01.txt und File.csv aus dem Data Lake Store entfernt.</span><span class="sxs-lookup"><span data-stu-id="e1f15-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="e1f15-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e1f15-110">PARAMETERS</span></span>

### <span data-ttu-id="e1f15-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="e1f15-111">-Account</span></span>
<span data-ttu-id="e1f15-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="e1f15-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="e1f15-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f15-113">-DefaultProfile</span></span>
<span data-ttu-id="e1f15-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1f15-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1f15-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="e1f15-115">-Force</span></span>
<span data-ttu-id="e1f15-116">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="e1f15-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e1f15-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1f15-117">-PassThru</span></span>
<span data-ttu-id="e1f15-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e1f15-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e1f15-119">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e1f15-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e1f15-120">-Paths</span><span class="sxs-lookup"><span data-stu-id="e1f15-120">-Paths</span></span>
<span data-ttu-id="e1f15-121">Gibt ein Array von Data Lake Store-Pfaden der zu entfernenden Dateien an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="e1f15-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="e1f15-122">-Rekursieren</span><span class="sxs-lookup"><span data-stu-id="e1f15-122">-Recurse</span></span>
<span data-ttu-id="e1f15-123">Gibt an, dass mit diesem Vorgang alle Elemente im Zielordner gelöscht werden, einschließlich Unterordner.</span><span class="sxs-lookup"><span data-stu-id="e1f15-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

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

### <span data-ttu-id="e1f15-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e1f15-124">-Confirm</span></span>
<span data-ttu-id="e1f15-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1f15-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1f15-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1f15-126">-WhatIf</span></span>
<span data-ttu-id="e1f15-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1f15-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1f15-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1f15-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1f15-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f15-129">CommonParameters</span></span>
<span data-ttu-id="e1f15-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1f15-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f15-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1f15-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f15-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e1f15-132">INPUTS</span></span>

### <span data-ttu-id="e1f15-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e1f15-133">System.String</span></span>

### <span data-ttu-id="e1f15-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span><span class="sxs-lookup"><span data-stu-id="e1f15-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="e1f15-135">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e1f15-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e1f15-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e1f15-136">OUTPUTS</span></span>

### <span data-ttu-id="e1f15-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e1f15-137">System.Boolean</span></span>

## <span data-ttu-id="e1f15-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e1f15-138">NOTES</span></span>

## <span data-ttu-id="e1f15-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e1f15-139">RELATED LINKS</span></span>

[<span data-ttu-id="e1f15-140">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e1f15-140">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="e1f15-141">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e1f15-141">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="e1f15-142">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e1f15-142">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="e1f15-143">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e1f15-143">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="e1f15-144">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e1f15-144">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="e1f15-145">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e1f15-145">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


