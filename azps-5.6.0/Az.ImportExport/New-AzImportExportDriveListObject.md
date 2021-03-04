---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 4b3907e71dd8d457b1ab38ecd5cdc82b38d7b772
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928027"
---
# <span data-ttu-id="3864e-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="3864e-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="3864e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3864e-102">SYNOPSIS</span></span>
<span data-ttu-id="3864e-103">Erstellen Sie ein DriverList-Objekt für ImportExport.</span><span class="sxs-lookup"><span data-stu-id="3864e-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="3864e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3864e-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="3864e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3864e-105">DESCRIPTION</span></span>
<span data-ttu-id="3864e-106">Erstellen Sie ein DriverList-Objekt für ImportExport.</span><span class="sxs-lookup"><span data-stu-id="3864e-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="3864e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3864e-107">EXAMPLES</span></span>

### <span data-ttu-id="3864e-108">Beispiel 1: Erstellen eines neuen DriveList for ImportExport-Auftrags</span><span class="sxs-lookup"><span data-stu-id="3864e-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="3864e-109">Diese Cmdlets erstellen einen neuen DriveList for ImportExport-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="3864e-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="3864e-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3864e-110">PARAMETERS</span></span>

### <span data-ttu-id="3864e-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="3864e-111">-BitLockerKey</span></span>
<span data-ttu-id="3864e-112">Der Zum Verschlüsseln des Laufwerks verwendete BitLocker-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="3864e-112">The BitLocker key used to encrypt the drive.</span></span>

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

### <span data-ttu-id="3864e-113">-BytesSucceeded</span><span class="sxs-lookup"><span data-stu-id="3864e-113">-BytesSucceeded</span></span>
<span data-ttu-id="3864e-114">Bytes, die erfolgreich für das Laufwerk übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="3864e-114">Bytes successfully transferred for the drive.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3864e-115">-CopyStatus</span><span class="sxs-lookup"><span data-stu-id="3864e-115">-CopyStatus</span></span>
<span data-ttu-id="3864e-116">Detaillierter Status zum Datenübertragungsprozess.</span><span class="sxs-lookup"><span data-stu-id="3864e-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="3864e-117">Dieses Feld wird in der Antwort erst zurückgegeben, wenn sich das Laufwerk im Übertragungszustand befindet.</span><span class="sxs-lookup"><span data-stu-id="3864e-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

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

### <span data-ttu-id="3864e-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="3864e-118">-DriveHeaderHash</span></span>
<span data-ttu-id="3864e-119">Der Hashwert der Laufwerkkopfzeile.</span><span class="sxs-lookup"><span data-stu-id="3864e-119">The drive header hash value.</span></span>

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

### <span data-ttu-id="3864e-120">-DriveId</span><span class="sxs-lookup"><span data-stu-id="3864e-120">-DriveId</span></span>
<span data-ttu-id="3864e-121">Die Seriennummer der Hardware des Laufwerks ohne Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="3864e-121">The drive's hardware serial number, without spaces.</span></span>

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

### <span data-ttu-id="3864e-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="3864e-122">-ErrorLogUri</span></span>
<span data-ttu-id="3864e-123">Ein URI, der auf den Blob verweist, der das Fehlerprotokoll für den Datenübertragungsvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="3864e-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

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

### <span data-ttu-id="3864e-124">-ManifestFile</span><span class="sxs-lookup"><span data-stu-id="3864e-124">-ManifestFile</span></span>
<span data-ttu-id="3864e-125">Der relative Pfad der Manifestdatei auf dem Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="3864e-125">The relative path of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="3864e-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="3864e-126">-ManifestHash</span></span>
<span data-ttu-id="3864e-127">Der base16-codierte #A0 der Manifestdatei auf dem Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="3864e-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="3864e-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="3864e-128">-ManifestUri</span></span>
<span data-ttu-id="3864e-129">Ein URI, der auf den Blob verweist, der die Laufwerkmanifestdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="3864e-129">A URI that points to the blob containing the drive manifest file.</span></span>

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

### <span data-ttu-id="3864e-130">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="3864e-130">-PercentComplete</span></span>
<span data-ttu-id="3864e-131">Prozentsatz, der für das Laufwerk abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="3864e-131">Percentage completed for the drive.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3864e-132">-State</span><span class="sxs-lookup"><span data-stu-id="3864e-132">-State</span></span>
<span data-ttu-id="3864e-133">Der aktuelle Zustand des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="3864e-133">The drive's current state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Support.DriveState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3864e-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="3864e-134">-VerboseLogUri</span></span>
<span data-ttu-id="3864e-135">Ein URI, der auf den Blob verweist, der das ausführliche Protokoll für den Datenübertragungsvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="3864e-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

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

### <span data-ttu-id="3864e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3864e-136">CommonParameters</span></span>
<span data-ttu-id="3864e-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3864e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3864e-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3864e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3864e-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3864e-139">INPUTS</span></span>

## <span data-ttu-id="3864e-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3864e-140">OUTPUTS</span></span>

### <span data-ttu-id="3864e-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span><span class="sxs-lookup"><span data-stu-id="3864e-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="3864e-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3864e-142">NOTES</span></span>

<span data-ttu-id="3864e-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="3864e-143">ALIASES</span></span>

## <span data-ttu-id="3864e-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3864e-144">RELATED LINKS</span></span>

