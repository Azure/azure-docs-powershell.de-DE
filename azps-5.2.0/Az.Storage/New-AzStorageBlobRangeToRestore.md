---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290495"
---
# <span data-ttu-id="f6fbd-101">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="f6fbd-101">New-AzStorageBlobRangeToRestore</span></span>

## <span data-ttu-id="f6fbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="f6fbd-103">Erstellt ein Blob Range-Objekt, um ein Speicherkonto wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="f6fbd-103">Creates a Blob Range object to restores a Storage account.</span></span>

## <span data-ttu-id="f6fbd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6fbd-104">SYNTAX</span></span>

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6fbd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6fbd-105">DESCRIPTION</span></span>
<span data-ttu-id="f6fbd-106">Das **Cmdlet "New-AzStorageBlobRangeToRestore"** erstellt ein Blob Range-Objekt, das in Restore-AzStorageBlobRange verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f6fbd-106">The **New-AzStorageBlobRangeToRestore** cmdlet creates a Blob range object, which can be used in Restore-AzStorageBlobRange.</span></span>

## <span data-ttu-id="f6fbd-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f6fbd-107">EXAMPLES</span></span>

### <span data-ttu-id="f6fbd-108">Beispiel 1: Erstellt einen blob-Bereich, der wiederhergestellt werden soll</span><span class="sxs-lookup"><span data-stu-id="f6fbd-108">Example 1: Creates a blob range to restore</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

<span data-ttu-id="f6fbd-109">Mit diesem Befehl wird ein blob-Bereich erstellt, der wiederhergestellt werden soll, der mit "container1/blob1" (include) beginnt und mit "container2/blob2" endet (Ausschluss).</span><span class="sxs-lookup"><span data-stu-id="f6fbd-109">This command creates a blob range to restore, which starts at container1/blob1 (include), and ends at container2/blob2 (exclude).</span></span>

### <span data-ttu-id="f6fbd-110">Beispiel 2: Erstellt einen BLOB-Bereich, der vom ersten BLOB in alphabetischer Reihenfolge zu einem bestimmten BLOB wiederhergestellt wird (ausschließen)</span><span class="sxs-lookup"><span data-stu-id="f6fbd-110">Example 2: Creates a blob range which will restore from first blob in alphabetical order, to a specific blob (exclude)</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

<span data-ttu-id="f6fbd-111">Dieser Befehl erstellt einen BLOB-Bereich, der vom ersten BLOB alphabetischer Reihenfolge bis zu einem bestimmten BLOB Container2/BLOB2 wiederhergestellt wird (ausschließen)</span><span class="sxs-lookup"><span data-stu-id="f6fbd-111">This command creates a blob range which will restore from first blob of alphabetical order, to a specific blob container2/blob2 (exclude)</span></span>

### <span data-ttu-id="f6fbd-112">Beispiel 3: Erstellt einen BLOB-Bereich, der von einem bestimmten BLOB (include) zum letzten BLOB in alphabetischer Reihenfolge wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f6fbd-112">Example 3: Creates a blob range which will restore from a specific blob (include), to the last blob in alphabetical order</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

<span data-ttu-id="f6fbd-113">Mit diesem Befehl wird ein BLOB-Bereich erstellt, der von einem bestimmten BLOB-Container1/BLOB1 (include) bis zum letzten BLOB in alphabetischer Reihenfolge wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f6fbd-113">This command creates a blob range which will restore from a specific blob container1/blob1 (include), to the last blob in alphabetical order.</span></span>

### <span data-ttu-id="f6fbd-114">Beispiel 4: Erstellt einen BLOB-Bereich, der alle Blobs wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="f6fbd-114">Example 4: Creates a blob range which will restore all blobs</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

<span data-ttu-id="f6fbd-115">Mit diesem Befehl wird ein BLOB-Bereich erstellt, mit dem alle BLOB wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f6fbd-115">This command creates a blob range which will restore all blobs.</span></span>

## <span data-ttu-id="f6fbd-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6fbd-116">PARAMETERS</span></span>

### <span data-ttu-id="f6fbd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6fbd-117">-DefaultProfile</span></span>
<span data-ttu-id="f6fbd-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6fbd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6fbd-119">-EndRange</span><span class="sxs-lookup"><span data-stu-id="f6fbd-119">-EndRange</span></span>
<span data-ttu-id="f6fbd-120">Geben Sie den Endbereich für die Blobwiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="f6fbd-120">Specify the blob restore End range.</span></span>
<span data-ttu-id="f6fbd-121">Der Endbereich wird in "Blobs wiederherstellen" ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f6fbd-121">End range will be excluded in restore blobs.</span></span>
<span data-ttu-id="f6fbd-122">Legen Sie es als leere Strng für die Wiederherstellung am Ende des Felds ein.</span><span class="sxs-lookup"><span data-stu-id="f6fbd-122">Set it as empty strng to restore to the end.</span></span>

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

### <span data-ttu-id="f6fbd-123">-StartRange</span><span class="sxs-lookup"><span data-stu-id="f6fbd-123">-StartRange</span></span>
<span data-ttu-id="f6fbd-124">Geben Sie den Startbereich für die Blobwiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="f6fbd-124">Specify the blob restore start range.</span></span>
<span data-ttu-id="f6fbd-125">Der Startbereich wird in "Blobs wiederherstellen" eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f6fbd-125">Start range will be included in restore blobs.</span></span>
<span data-ttu-id="f6fbd-126">Legen Sie die Zeichenfolge als leere Zeichenfolge so ein, dass sie von Anfang an wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f6fbd-126">Set it as empty string to restore from begining.</span></span>

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

### <span data-ttu-id="f6fbd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6fbd-127">CommonParameters</span></span>
<span data-ttu-id="f6fbd-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6fbd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6fbd-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6fbd-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6fbd-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f6fbd-130">INPUTS</span></span>

### <span data-ttu-id="f6fbd-131">Keine</span><span class="sxs-lookup"><span data-stu-id="f6fbd-131">None</span></span>

## <span data-ttu-id="f6fbd-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f6fbd-132">OUTPUTS</span></span>

### <span data-ttu-id="f6fbd-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="f6fbd-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span></span>

## <span data-ttu-id="f6fbd-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f6fbd-134">NOTES</span></span>

## <span data-ttu-id="f6fbd-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f6fbd-135">RELATED LINKS</span></span>
