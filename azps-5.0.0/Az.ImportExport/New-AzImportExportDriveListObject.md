---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 54252b82ecb32d26cf44b3b6f745856b755d60d9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177576"
---
# <span data-ttu-id="e6527-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="e6527-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="e6527-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e6527-102">SYNOPSIS</span></span>
<span data-ttu-id="e6527-103">Erstellen Sie ein driverlist-Objekt für DataObjects.</span><span class="sxs-lookup"><span data-stu-id="e6527-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="e6527-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6527-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="e6527-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6527-105">DESCRIPTION</span></span>
<span data-ttu-id="e6527-106">Erstellen Sie ein driverlist-Objekt für DataObjects.</span><span class="sxs-lookup"><span data-stu-id="e6527-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="e6527-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6527-107">EXAMPLES</span></span>

### <span data-ttu-id="e6527-108">Beispiel 1: Erstellen einer neuen Laufwerkliste für DataObjects-Auftrag</span><span class="sxs-lookup"><span data-stu-id="e6527-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="e6527-109">Diese Cmdlets erstellen eine neue drivelist für DataObjects-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="e6527-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="e6527-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6527-110">PARAMETERS</span></span>

### <span data-ttu-id="e6527-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="e6527-111">-BitLockerKey</span></span>
<span data-ttu-id="e6527-112">Der BitLocker-Schlüssel, der zum Verschlüsseln des Laufwerks verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e6527-112">The BitLocker key used to encrypt the drive.</span></span>

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

### <span data-ttu-id="e6527-113">-BytesSucceeded</span><span class="sxs-lookup"><span data-stu-id="e6527-113">-BytesSucceeded</span></span>
<span data-ttu-id="e6527-114">Bytes, die für das Laufwerk erfolgreich übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="e6527-114">Bytes successfully transferred for the drive.</span></span>

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

### <span data-ttu-id="e6527-115">-CopyStatus</span><span class="sxs-lookup"><span data-stu-id="e6527-115">-CopyStatus</span></span>
<span data-ttu-id="e6527-116">Der detaillierte Status des Daten Übertragungsprozesses.</span><span class="sxs-lookup"><span data-stu-id="e6527-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="e6527-117">Dieses Feld wird in der Antwort erst zurückgegeben, wenn sich das Laufwerk im Status "übertragen" befindet.</span><span class="sxs-lookup"><span data-stu-id="e6527-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

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

### <span data-ttu-id="e6527-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="e6527-118">-DriveHeaderHash</span></span>
<span data-ttu-id="e6527-119">Der Hashwert des Laufwerk Headers.</span><span class="sxs-lookup"><span data-stu-id="e6527-119">The drive header hash value.</span></span>

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

### <span data-ttu-id="e6527-120">-Laufwerks-Nr</span><span class="sxs-lookup"><span data-stu-id="e6527-120">-DriveId</span></span>
<span data-ttu-id="e6527-121">Die Hardware-Seriennummer des Laufwerks ohne Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="e6527-121">The drive's hardware serial number, without spaces.</span></span>

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

### <span data-ttu-id="e6527-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="e6527-122">-ErrorLogUri</span></span>
<span data-ttu-id="e6527-123">Ein URI, der auf das BLOB verweist, das das Fehlerprotokoll für den Daten Übertragungsvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="e6527-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

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

### <span data-ttu-id="e6527-124">-Manifestdatei</span><span class="sxs-lookup"><span data-stu-id="e6527-124">-ManifestFile</span></span>
<span data-ttu-id="e6527-125">Der relative Pfad der Manifestdatei auf dem Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="e6527-125">The relative path of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="e6527-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="e6527-126">-ManifestHash</span></span>
<span data-ttu-id="e6527-127">Der Base16-codierte MD5-Hash der Manifestdatei auf dem Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="e6527-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="e6527-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="e6527-128">-ManifestUri</span></span>
<span data-ttu-id="e6527-129">Ein URI, der auf das BLOB verweist, das die Laufwerk Manifestdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="e6527-129">A URI that points to the blob containing the drive manifest file.</span></span>

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

### <span data-ttu-id="e6527-130">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="e6527-130">-PercentComplete</span></span>
<span data-ttu-id="e6527-131">Prozentsatz für das Laufwerk abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="e6527-131">Percentage completed for the drive.</span></span>

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

### <span data-ttu-id="e6527-132">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="e6527-132">-State</span></span>
<span data-ttu-id="e6527-133">Der aktuelle Zustand des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="e6527-133">The drive's current state.</span></span>

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

### <span data-ttu-id="e6527-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="e6527-134">-VerboseLogUri</span></span>
<span data-ttu-id="e6527-135">Ein URI, der auf das BLOB verweist, das das ausführliche Protokoll für den Daten Übertragungsvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="e6527-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

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

### <span data-ttu-id="e6527-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6527-136">CommonParameters</span></span>
<span data-ttu-id="e6527-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6527-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6527-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6527-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6527-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e6527-139">INPUTS</span></span>

## <span data-ttu-id="e6527-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e6527-140">OUTPUTS</span></span>

### <span data-ttu-id="e6527-141">Microsoft. Azure. PowerShell. Cmdlets. DataObjects. Models. Api20161101. IDriveStatus</span><span class="sxs-lookup"><span data-stu-id="e6527-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="e6527-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="e6527-142">NOTES</span></span>

<span data-ttu-id="e6527-143">Aliase</span><span class="sxs-lookup"><span data-stu-id="e6527-143">ALIASES</span></span>

## <span data-ttu-id="e6527-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e6527-144">RELATED LINKS</span></span>

