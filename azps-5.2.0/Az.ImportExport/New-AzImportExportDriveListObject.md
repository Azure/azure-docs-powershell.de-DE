---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 54252b82ecb32d26cf44b3b6f745856b755d60d9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364494"
---
# <span data-ttu-id="f0e88-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="f0e88-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="f0e88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0e88-102">SYNOPSIS</span></span>
<span data-ttu-id="f0e88-103">Erstellen Sie ein "DriverList"-Objekt für "ImportExport".</span><span class="sxs-lookup"><span data-stu-id="f0e88-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="f0e88-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0e88-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="f0e88-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0e88-105">DESCRIPTION</span></span>
<span data-ttu-id="f0e88-106">Erstellen Sie ein "DriverList"-Objekt für "ImportExport".</span><span class="sxs-lookup"><span data-stu-id="f0e88-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="f0e88-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f0e88-107">EXAMPLES</span></span>

### <span data-ttu-id="f0e88-108">Beispiel 1: Erstellen eines neuen "DriveList"-Auftrags für "ImportExport"</span><span class="sxs-lookup"><span data-stu-id="f0e88-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="f0e88-109">Diese Cmdlets erstellen einen neuen DriveList für ImportExport-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="f0e88-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="f0e88-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0e88-110">PARAMETERS</span></span>

### <span data-ttu-id="f0e88-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="f0e88-111">-BitLockerKey</span></span>
<span data-ttu-id="f0e88-112">Der Zum Verschlüsseln des Laufwerks verwendete BitLocker-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="f0e88-112">The BitLocker key used to encrypt the drive.</span></span>

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

### <span data-ttu-id="f0e88-113">-BytesSucceeded</span><span class="sxs-lookup"><span data-stu-id="f0e88-113">-BytesSucceeded</span></span>
<span data-ttu-id="f0e88-114">Bytes wurden erfolgreich für das Laufwerk übertragen.</span><span class="sxs-lookup"><span data-stu-id="f0e88-114">Bytes successfully transferred for the drive.</span></span>

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

### <span data-ttu-id="f0e88-115">-CopyStatus</span><span class="sxs-lookup"><span data-stu-id="f0e88-115">-CopyStatus</span></span>
<span data-ttu-id="f0e88-116">Detaillierter Status zum Datenübertragungsprozess.</span><span class="sxs-lookup"><span data-stu-id="f0e88-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="f0e88-117">Dieses Feld wird erst in der Antwort zurückgegeben, wenn sich das Laufwerk im Zustand "Übertragen" befindet.</span><span class="sxs-lookup"><span data-stu-id="f0e88-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

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

### <span data-ttu-id="f0e88-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="f0e88-118">-DriveHeaderHash</span></span>
<span data-ttu-id="f0e88-119">Der Hashwert für die Laufwerkkopfzeile.</span><span class="sxs-lookup"><span data-stu-id="f0e88-119">The drive header hash value.</span></span>

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

### <span data-ttu-id="f0e88-120">-DriveId</span><span class="sxs-lookup"><span data-stu-id="f0e88-120">-DriveId</span></span>
<span data-ttu-id="f0e88-121">Die Hardwareseriennummer des Laufwerks ohne Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="f0e88-121">The drive's hardware serial number, without spaces.</span></span>

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

### <span data-ttu-id="f0e88-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="f0e88-122">-ErrorLogUri</span></span>
<span data-ttu-id="f0e88-123">Ein URI, der auf das BLOB verweist, das das Fehlerprotokoll für den Datenübertragungsvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="f0e88-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

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

### <span data-ttu-id="f0e88-124">-ManifestFile</span><span class="sxs-lookup"><span data-stu-id="f0e88-124">-ManifestFile</span></span>
<span data-ttu-id="f0e88-125">Der relative Pfad der Manifestdatei auf dem Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="f0e88-125">The relative path of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="f0e88-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="f0e88-126">-ManifestHash</span></span>
<span data-ttu-id="f0e88-127">Der base16-codierte #A0 der Manifestdatei auf dem Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="f0e88-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="f0e88-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="f0e88-128">-ManifestUri</span></span>
<span data-ttu-id="f0e88-129">Ein URI, der auf das BLOB verweist, das die Laufwerkmanifestdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="f0e88-129">A URI that points to the blob containing the drive manifest file.</span></span>

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

### <span data-ttu-id="f0e88-130">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="f0e88-130">-PercentComplete</span></span>
<span data-ttu-id="f0e88-131">Prozentsatz der Fertigstellung für das Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="f0e88-131">Percentage completed for the drive.</span></span>

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

### <span data-ttu-id="f0e88-132">-State</span><span class="sxs-lookup"><span data-stu-id="f0e88-132">-State</span></span>
<span data-ttu-id="f0e88-133">Der aktuelle Zustand des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="f0e88-133">The drive's current state.</span></span>

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

### <span data-ttu-id="f0e88-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="f0e88-134">-VerboseLogUri</span></span>
<span data-ttu-id="f0e88-135">Ein URI, der auf das BLOB verweist, das das ausführliche Protokoll für den Datenübertragungsvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="f0e88-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

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

### <span data-ttu-id="f0e88-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0e88-136">CommonParameters</span></span>
<span data-ttu-id="f0e88-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0e88-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0e88-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0e88-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0e88-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f0e88-139">INPUTS</span></span>

## <span data-ttu-id="f0e88-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f0e88-140">OUTPUTS</span></span>

### <span data-ttu-id="f0e88-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span><span class="sxs-lookup"><span data-stu-id="f0e88-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="f0e88-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f0e88-142">NOTES</span></span>

<span data-ttu-id="f0e88-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f0e88-143">ALIASES</span></span>

## <span data-ttu-id="f0e88-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f0e88-144">RELATED LINKS</span></span>

