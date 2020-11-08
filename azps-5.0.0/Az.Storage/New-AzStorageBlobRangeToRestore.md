---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177381"
---
# <span data-ttu-id="9cabb-101">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="9cabb-101">New-AzStorageBlobRangeToRestore</span></span>

## <span data-ttu-id="9cabb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9cabb-102">SYNOPSIS</span></span>
<span data-ttu-id="9cabb-103">Erstellt ein BLOB Range-Objekt, um ein Speicherkonto wieder zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9cabb-103">Creates a Blob Range object to restores a Storage account.</span></span>

## <span data-ttu-id="9cabb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cabb-104">SYNTAX</span></span>

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cabb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9cabb-105">DESCRIPTION</span></span>
<span data-ttu-id="9cabb-106">Das Cmdlet **New-AzStorageBlobRangeToRestore** erstellt ein BLOB Range-Objekt, das in Restore-AzStorageBlobRange verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9cabb-106">The **New-AzStorageBlobRangeToRestore** cmdlet creates a Blob range object, which can be used in Restore-AzStorageBlobRange.</span></span>

## <span data-ttu-id="9cabb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9cabb-107">EXAMPLES</span></span>

### <span data-ttu-id="9cabb-108">Beispiel 1: erstellt einen zu wiederherzustellenden BLOB-Bereich</span><span class="sxs-lookup"><span data-stu-id="9cabb-108">Example 1: Creates a blob range to restore</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

<span data-ttu-id="9cabb-109">Dieser Befehl erstellt einen zu wiederherzustellenden BLOB-Bereich, der bei Container1/blob1 (Include) beginnt und bei container2/blob2 (Exclude) endet.</span><span class="sxs-lookup"><span data-stu-id="9cabb-109">This command creates a blob range to restore, which starts at container1/blob1 (include), and ends at container2/blob2 (exclude).</span></span>

### <span data-ttu-id="9cabb-110">Beispiel 2: erstellt einen BLOB-Bereich, der aus dem ersten BLOB in alphabetischer Reihenfolge wiederhergestellt wird, bis zu einem bestimmten BLOB (ausschließen).</span><span class="sxs-lookup"><span data-stu-id="9cabb-110">Example 2: Creates a blob range which will restore from first blob in alphabetical order, to a specific blob (exclude)</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

<span data-ttu-id="9cabb-111">Dieser Befehl erstellt einen BLOB-Bereich, der aus dem ersten BLOB in alphabetischer Reihenfolge wiederhergestellt wird, bis zu einem bestimmten BLOB-container2/blob2 (ausschließen).</span><span class="sxs-lookup"><span data-stu-id="9cabb-111">This command creates a blob range which will restore from first blob of alphabetical order, to a specific blob container2/blob2 (exclude)</span></span>

### <span data-ttu-id="9cabb-112">Beispiel 3: erstellt einen BLOB-Bereich, der von einem bestimmten BLOB (Include) bis zum letzten BLOB in alphabetischer Reihenfolge wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9cabb-112">Example 3: Creates a blob range which will restore from a specific blob (include), to the last blob in alphabetical order</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

<span data-ttu-id="9cabb-113">Mit diesem Befehl wird ein BLOB-Bereich erstellt, der von einem bestimmten BLOB-Container1/blob1 (Include) zum letzten BLOB in alphabetischer Reihenfolge wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9cabb-113">This command creates a blob range which will restore from a specific blob container1/blob1 (include), to the last blob in alphabetical order.</span></span>

### <span data-ttu-id="9cabb-114">Beispiel 4: erstellt einen BLOB-Bereich, in dem alle Blobs wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9cabb-114">Example 4: Creates a blob range which will restore all blobs</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

<span data-ttu-id="9cabb-115">Mit diesem Befehl wird ein BLOB-Bereich erstellt, der alle Blobs wieder herstellt.</span><span class="sxs-lookup"><span data-stu-id="9cabb-115">This command creates a blob range which will restore all blobs.</span></span>

## <span data-ttu-id="9cabb-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cabb-116">PARAMETERS</span></span>

### <span data-ttu-id="9cabb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cabb-117">-DefaultProfile</span></span>
<span data-ttu-id="9cabb-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9cabb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cabb-119">-EndRange</span><span class="sxs-lookup"><span data-stu-id="9cabb-119">-EndRange</span></span>
<span data-ttu-id="9cabb-120">Geben Sie den Endbereich der BLOB-Wiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="9cabb-120">Specify the blob restore End range.</span></span>
<span data-ttu-id="9cabb-121">Der Endbereich wird in BLOB-wiederherstellen ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9cabb-121">End range will be excluded in restore blobs.</span></span>
<span data-ttu-id="9cabb-122">Legen Sie Sie als leere Strng-Datei zum Ende wieder her.</span><span class="sxs-lookup"><span data-stu-id="9cabb-122">Set it as empty strng to restore to the end.</span></span>

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

### <span data-ttu-id="9cabb-123">-StartRange</span><span class="sxs-lookup"><span data-stu-id="9cabb-123">-StartRange</span></span>
<span data-ttu-id="9cabb-124">Geben Sie den Startbereich für die BLOB-Wiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="9cabb-124">Specify the blob restore start range.</span></span>
<span data-ttu-id="9cabb-125">Der Start Bereich wird in die BLOB-Wiederherstellung aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="9cabb-125">Start range will be included in restore blobs.</span></span>
<span data-ttu-id="9cabb-126">Als leere Zeichenfolge zum Wiederherstellen von Anfang an.</span><span class="sxs-lookup"><span data-stu-id="9cabb-126">Set it as empty string to restore from begining.</span></span>

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

### <span data-ttu-id="9cabb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cabb-127">CommonParameters</span></span>
<span data-ttu-id="9cabb-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cabb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cabb-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cabb-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cabb-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9cabb-130">INPUTS</span></span>

### <span data-ttu-id="9cabb-131">Keine</span><span class="sxs-lookup"><span data-stu-id="9cabb-131">None</span></span>

## <span data-ttu-id="9cabb-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9cabb-132">OUTPUTS</span></span>

### <span data-ttu-id="9cabb-133">Microsoft. Azure. Commands. Management. Storage. Models. PSBlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="9cabb-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span></span>

## <span data-ttu-id="9cabb-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="9cabb-134">NOTES</span></span>

## <span data-ttu-id="9cabb-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9cabb-135">RELATED LINKS</span></span>
