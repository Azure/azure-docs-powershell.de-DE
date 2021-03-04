---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorechilditemsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
ms.openlocfilehash: d83e07e207c2b0e3a03c745abc874814378e5ee4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921259"
---
# <span data-ttu-id="4373b-101">Get-AzDataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="4373b-101">Get-AzDataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="4373b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4373b-102">SYNOPSIS</span></span>
<span data-ttu-id="4373b-103">Ruft die Zusammenfassung der Gesamtgröße, der Dateien und Verzeichnisse ab, die im angegebenen Pfad enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="4373b-103">Gets the summary of total size, files and directories contained in the path specified</span></span>

## <span data-ttu-id="4373b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4373b-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItemSummary [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4373b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4373b-105">DESCRIPTION</span></span>
<span data-ttu-id="4373b-106">Die **Get-AzDataLakeStoreChildItemSummary** ruft die Inhaltszusammenfassung für einen bestimmten Pfad ab.</span><span class="sxs-lookup"><span data-stu-id="4373b-106">The **Get-AzDataLakeStoreChildItemSummary** retrieves the content summary for a given path.</span></span> <span data-ttu-id="4373b-107">Es berechnet rekursiv die Gesamtanzahl der Dateien, Verzeichnisse und die Gesamtgröße aller Dateien unter dem angegebenen Pfad.</span><span class="sxs-lookup"><span data-stu-id="4373b-107">It recursively computes total number of files, directories and total size of all the files under the given path.</span></span>

## <span data-ttu-id="4373b-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4373b-108">EXAMPLES</span></span>

### <span data-ttu-id="4373b-109">Beispiel 1: Anzeigen der Inhaltszusammenfassung eines Ordners</span><span class="sxs-lookup"><span data-stu-id="4373b-109">Example 1: Get the content summary of a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreChildItemSummary -Account ContosoADL -Path /a -Concurrency 128
```

<span data-ttu-id="4373b-110">Es listet die Anzahl der Gesamtverzeichnissen, Dateien und deren Größe auf, die unter /a enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="4373b-110">It lists number of total directories, files and their size contained under /a.</span></span>

## <span data-ttu-id="4373b-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4373b-111">PARAMETERS</span></span>

### <span data-ttu-id="4373b-112">-Konto</span><span class="sxs-lookup"><span data-stu-id="4373b-112">-Account</span></span>
<span data-ttu-id="4373b-113">Das Data Lake Store-Konto zum Ausführen des Dateisystemvorgangs in</span><span class="sxs-lookup"><span data-stu-id="4373b-113">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="4373b-114">-Parallelität</span><span class="sxs-lookup"><span data-stu-id="4373b-114">-Concurrency</span></span>
<span data-ttu-id="4373b-115">Gibt die Anzahl der parallel verarbeiteten Dateien/Verzeichnisse an.</span><span class="sxs-lookup"><span data-stu-id="4373b-115">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="4373b-116">Der Standardwert wird als optimaler Aufwand basierend auf der Systemspezifikation berechnet.</span><span class="sxs-lookup"><span data-stu-id="4373b-116">Default will be computed as a best effort based on system specification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4373b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4373b-117">-DefaultProfile</span></span>
<span data-ttu-id="4373b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4373b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4373b-119">-Path</span><span class="sxs-lookup"><span data-stu-id="4373b-119">-Path</span></span>
<span data-ttu-id="4373b-120">Der Pfad im angegebenen Data Lake-Konto, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4373b-120">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="4373b-121">Kann eine Datei oder ein Ordner im Format "/folder/file.txt" sein, wobei das erste "/" nach dem DNS den Stamm des Dateisystems angibt.</span><span class="sxs-lookup"><span data-stu-id="4373b-121">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4373b-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4373b-122">-Confirm</span></span>
<span data-ttu-id="4373b-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4373b-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4373b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4373b-124">-WhatIf</span></span>
<span data-ttu-id="4373b-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4373b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4373b-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4373b-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4373b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4373b-127">CommonParameters</span></span>
<span data-ttu-id="4373b-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4373b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4373b-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4373b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4373b-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4373b-130">INPUTS</span></span>

### <span data-ttu-id="4373b-131">System.String</span><span class="sxs-lookup"><span data-stu-id="4373b-131">System.String</span></span>

### <span data-ttu-id="4373b-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="4373b-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="4373b-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="4373b-133">System.Int32</span></span>

## <span data-ttu-id="4373b-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4373b-134">OUTPUTS</span></span>

### <span data-ttu-id="4373b-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="4373b-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="4373b-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4373b-136">NOTES</span></span>

## <span data-ttu-id="4373b-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4373b-137">RELATED LINKS</span></span>
