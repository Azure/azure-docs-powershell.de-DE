---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azureatalakestorechilditemsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItemSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItemSummary.md
ms.openlocfilehash: 83fb8b3ea5fdf9ad63983d2a3a3d23d402fbb5a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502961"
---
# <span data-ttu-id="a0530-101">Get-AzureRmDataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="a0530-101">Get-AzureRmDataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="a0530-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0530-102">SYNOPSIS</span></span>
<span data-ttu-id="a0530-103">Ruft die Zusammenfassung der Gesamtgröße, Dateien und Verzeichnisse ab, die in dem angegebenen Pfad enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a0530-103">Gets the summary of total size, files and directories contained in the path specified</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0530-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0530-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreChildItemSummary [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0530-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0530-105">DESCRIPTION</span></span>
<span data-ttu-id="a0530-106">Der **Get-AzureRmDataLakeStoreChildItemSummary** Ruft die Inhaltszusammenfassung für einen angegebenen Pfad ab.</span><span class="sxs-lookup"><span data-stu-id="a0530-106">The **Get-AzureRmDataLakeStoreChildItemSummary** retrieves the content summary for a given path.</span></span> <span data-ttu-id="a0530-107">Die Gesamtzahl der Dateien, Verzeichnisse und die Gesamtgröße aller Dateien unter dem angegebenen Pfad werden rekursiv berechnet.</span><span class="sxs-lookup"><span data-stu-id="a0530-107">It recursively computes total number of files, directories and total size of all the files under the given path.</span></span>

## <span data-ttu-id="a0530-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0530-108">EXAMPLES</span></span>

### <span data-ttu-id="a0530-109">Beispiel 1: Abrufen der Inhaltszusammenfassung eines Ordners</span><span class="sxs-lookup"><span data-stu-id="a0530-109">Example 1: Get the content summary of a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreChildItemSummary -Account ContosoADL -Path /a -Concurrency 128
```

<span data-ttu-id="a0530-110">In dieser Liste sind die Gesamtzahl der Verzeichnisse, Dateien und deren Größe unter/a aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0530-110">It lists number of total directories, files and their size contained under /a.</span></span>

## <span data-ttu-id="a0530-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0530-111">PARAMETERS</span></span>

### <span data-ttu-id="a0530-112">-Konto</span><span class="sxs-lookup"><span data-stu-id="a0530-112">-Account</span></span>
<span data-ttu-id="a0530-113">Das Data Lake Store-Konto zum Ausführen des Dateisystem Vorgangs in</span><span class="sxs-lookup"><span data-stu-id="a0530-113">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="a0530-114">-Parallelität</span><span class="sxs-lookup"><span data-stu-id="a0530-114">-Concurrency</span></span>
<span data-ttu-id="a0530-115">Gibt an, wie viele Dateien/Verzeichnisse parallel verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a0530-115">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="a0530-116">Der Standardwert wird basierend auf der Systemspezifikation als optimaler Aufwand berechnet.</span><span class="sxs-lookup"><span data-stu-id="a0530-116">Default will be computed as a best effort based on system specification.</span></span>

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

### <span data-ttu-id="a0530-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0530-117">-DefaultProfile</span></span>
<span data-ttu-id="a0530-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a0530-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0530-119">-Path</span><span class="sxs-lookup"><span data-stu-id="a0530-119">-Path</span></span>
<span data-ttu-id="a0530-120">Der Pfad im angegebenen Data Lake-Konto, das abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0530-120">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="a0530-121">Kann eine Datei oder ein Ordner im Format "/Folder/file.txt" sein, wobei der erste "/" nach dem DNS den Stamm des Dateisystems angibt.</span><span class="sxs-lookup"><span data-stu-id="a0530-121">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

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

### <span data-ttu-id="a0530-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a0530-122">-Confirm</span></span>
<span data-ttu-id="a0530-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0530-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0530-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0530-124">-WhatIf</span></span>
<span data-ttu-id="a0530-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0530-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0530-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0530-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0530-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0530-127">CommonParameters</span></span>
<span data-ttu-id="a0530-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0530-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0530-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0530-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0530-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0530-130">INPUTS</span></span>

### <span data-ttu-id="a0530-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a0530-131">System.String</span></span>

### <span data-ttu-id="a0530-132">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="a0530-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="a0530-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a0530-133">System.Int32</span></span>

## <span data-ttu-id="a0530-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0530-134">OUTPUTS</span></span>

### <span data-ttu-id="a0530-135">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="a0530-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="a0530-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0530-136">NOTES</span></span>

## <span data-ttu-id="a0530-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0530-137">RELATED LINKS</span></span>
