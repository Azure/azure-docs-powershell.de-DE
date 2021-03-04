---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: 0f74ad9b146a0c5d2f2c65b7109fb57f56902834
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944560"
---
# <span data-ttu-id="18eb1-101">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="18eb1-101">New-AzStorageBlobRangeToRestore</span></span>

## <span data-ttu-id="18eb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="18eb1-103">Erstellt ein Blob Range-Objekt, um ein Speicherkonto wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="18eb1-103">Creates a Blob Range object to restores a Storage account.</span></span>

## <span data-ttu-id="18eb1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18eb1-104">SYNTAX</span></span>

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18eb1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18eb1-105">DESCRIPTION</span></span>
<span data-ttu-id="18eb1-106">Das **Cmdlet New-AzStorageBlobRangeToRestore** erstellt ein Blobbereichsobjekt, das in Restore-AzStorageBlobRange verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="18eb1-106">The **New-AzStorageBlobRangeToRestore** cmdlet creates a Blob range object, which can be used in Restore-AzStorageBlobRange.</span></span>

## <span data-ttu-id="18eb1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="18eb1-107">EXAMPLES</span></span>

### <span data-ttu-id="18eb1-108">Beispiel 1: Erstellt einen Blobbereich, der wiederhergestellt werden soll</span><span class="sxs-lookup"><span data-stu-id="18eb1-108">Example 1: Creates a blob range to restore</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

<span data-ttu-id="18eb1-109">Mit diesem Befehl wird ein wiederherstellende Blobbereich erstellt, der bei container1/blob1 (include) beginnt und bei container2/blob2 (exclude) endet.</span><span class="sxs-lookup"><span data-stu-id="18eb1-109">This command creates a blob range to restore, which starts at container1/blob1 (include), and ends at container2/blob2 (exclude).</span></span>

### <span data-ttu-id="18eb1-110">Beispiel 2: Erstellt einen Blobbereich, der vom ersten Blob in alphabetischer Reihenfolge in einem bestimmten Blob wiederhergestellt wird (ausschließen)</span><span class="sxs-lookup"><span data-stu-id="18eb1-110">Example 2: Creates a blob range which will restore from first blob in alphabetical order, to a specific blob (exclude)</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

<span data-ttu-id="18eb1-111">Mit diesem Befehl wird ein Blobbereich erstellt, der aus dem ersten Blob alphabetischer Reihenfolge in einen bestimmten Blobcontainer2/Blob2 (ausschluss) wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="18eb1-111">This command creates a blob range which will restore from first blob of alphabetical order, to a specific blob container2/blob2 (exclude)</span></span>

### <span data-ttu-id="18eb1-112">Beispiel 3: Erstellt einen Blobbereich, der von einem bestimmten Blob (include) zum letzten Blob in alphabetischer Reihenfolge wiederhergestellt wird</span><span class="sxs-lookup"><span data-stu-id="18eb1-112">Example 3: Creates a blob range which will restore from a specific blob (include), to the last blob in alphabetical order</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

<span data-ttu-id="18eb1-113">Mit diesem Befehl wird ein Blobbereich erstellt, der aus einem bestimmten Blobcontainer1/Blob1 (include) bis zum letzten Blob in alphabetischer Reihenfolge wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="18eb1-113">This command creates a blob range which will restore from a specific blob container1/blob1 (include), to the last blob in alphabetical order.</span></span>

### <span data-ttu-id="18eb1-114">Beispiel 4: Erstellt einen Blobbereich, der alle Blobs wiederherstellen wird</span><span class="sxs-lookup"><span data-stu-id="18eb1-114">Example 4: Creates a blob range which will restore all blobs</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

<span data-ttu-id="18eb1-115">Mit diesem Befehl wird ein Blobbereich erstellt, der alle Blobs wiederherstellen wird.</span><span class="sxs-lookup"><span data-stu-id="18eb1-115">This command creates a blob range which will restore all blobs.</span></span>

## <span data-ttu-id="18eb1-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="18eb1-116">PARAMETERS</span></span>

### <span data-ttu-id="18eb1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18eb1-117">-DefaultProfile</span></span>
<span data-ttu-id="18eb1-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18eb1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18eb1-119">-EndRange</span><span class="sxs-lookup"><span data-stu-id="18eb1-119">-EndRange</span></span>
<span data-ttu-id="18eb1-120">Geben Sie den Endbereich für die Blobwiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="18eb1-120">Specify the blob restore End range.</span></span>
<span data-ttu-id="18eb1-121">Der Endbereich wird in Wiederherstellenblobs ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="18eb1-121">End range will be excluded in restore blobs.</span></span>
<span data-ttu-id="18eb1-122">Legen Sie sie als leere Strg-Strg-Wiederherstellen bis zum Ende des Wiederherstellens ein.</span><span class="sxs-lookup"><span data-stu-id="18eb1-122">Set it as empty strng to restore to the end.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18eb1-123">-StartRange</span><span class="sxs-lookup"><span data-stu-id="18eb1-123">-StartRange</span></span>
<span data-ttu-id="18eb1-124">Geben Sie den Startbereich für die Blobwiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="18eb1-124">Specify the blob restore start range.</span></span>
<span data-ttu-id="18eb1-125">Der Startbereich wird in Wiederherstellen-Blobs einbezogen.</span><span class="sxs-lookup"><span data-stu-id="18eb1-125">Start range will be included in restore blobs.</span></span>
<span data-ttu-id="18eb1-126">Legen Sie die Zeichenfolge als leere Zeichenfolge für die Wiederherstellung von Anfang an ein.</span><span class="sxs-lookup"><span data-stu-id="18eb1-126">Set it as empty string to restore from begining.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18eb1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18eb1-127">CommonParameters</span></span>
<span data-ttu-id="18eb1-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18eb1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18eb1-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18eb1-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18eb1-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="18eb1-130">INPUTS</span></span>

### <span data-ttu-id="18eb1-131">Keine</span><span class="sxs-lookup"><span data-stu-id="18eb1-131">None</span></span>

## <span data-ttu-id="18eb1-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="18eb1-132">OUTPUTS</span></span>

### <span data-ttu-id="18eb1-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="18eb1-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span></span>

## <span data-ttu-id="18eb1-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="18eb1-134">NOTES</span></span>

## <span data-ttu-id="18eb1-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="18eb1-135">RELATED LINKS</span></span>
