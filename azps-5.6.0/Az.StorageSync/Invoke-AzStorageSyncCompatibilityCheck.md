---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: b6052172ecca2821b1373d93a8de870969a6b4f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944416"
---
# <span data-ttu-id="9787b-101">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="9787b-101">Invoke-AzStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="9787b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9787b-102">SYNOPSIS</span></span>
<span data-ttu-id="9787b-103">Sucht nach möglichen Kompatibilitätsproblemen zwischen Ihrem System und Azure File Sync.</span><span class="sxs-lookup"><span data-stu-id="9787b-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

## <span data-ttu-id="9787b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9787b-104">SYNTAX</span></span>

### <span data-ttu-id="9787b-105">PathBased (Standard)</span><span class="sxs-lookup"><span data-stu-id="9787b-105">PathBased (Default)</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### <span data-ttu-id="9787b-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="9787b-106">ComputerNameBased</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## <span data-ttu-id="9787b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9787b-107">DESCRIPTION</span></span>
<span data-ttu-id="9787b-108">Das **Cmdlet Invoke-AzStorageSyncCompatibilityCheck** sucht nach möglichen Kompatibilitätsproblemen zwischen Ihrem System und Azure File Sync. Bei einem lokalen oder Remotepfad führt er eine Reihe von Überprüfungen für das System und den Dateinamen aus und gibt dann alle gefundenen Kompatibilitätsprobleme zurück.</span><span class="sxs-lookup"><span data-stu-id="9787b-108">The **Invoke-AzStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="9787b-109">Systemüberprüfungen:</span><span class="sxs-lookup"><span data-stu-id="9787b-109">System checks:</span></span>
- <span data-ttu-id="9787b-110">Betriebssystemkompatibilität Dateinamespace überprüft:</span><span class="sxs-lookup"><span data-stu-id="9787b-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="9787b-111">Nicht unterstützte Zeichen</span><span class="sxs-lookup"><span data-stu-id="9787b-111">Unsupported characters</span></span>
- <span data-ttu-id="9787b-112">Maximale Dateigröße</span><span class="sxs-lookup"><span data-stu-id="9787b-112">Maximum file size</span></span>
- <span data-ttu-id="9787b-113">Maximale Pfadlänge</span><span class="sxs-lookup"><span data-stu-id="9787b-113">Maximum path length</span></span>
- <span data-ttu-id="9787b-114">Maximale Dateilänge</span><span class="sxs-lookup"><span data-stu-id="9787b-114">Maximum file length</span></span>
- <span data-ttu-id="9787b-115">Maximale Datasetgröße</span><span class="sxs-lookup"><span data-stu-id="9787b-115">Maximum dataset size</span></span>
- <span data-ttu-id="9787b-116">Maximale Verzeichnistiefe</span><span class="sxs-lookup"><span data-stu-id="9787b-116">Maximum directory depth</span></span>

## <span data-ttu-id="9787b-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9787b-117">EXAMPLES</span></span>

### <span data-ttu-id="9787b-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9787b-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="9787b-119">Mit diesem Befehl wird die Kompatibilität des Systems sowie von Dateien und Ordnern in C:\DATA überprüft.</span><span class="sxs-lookup"><span data-stu-id="9787b-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="9787b-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9787b-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="9787b-121">Dieser Befehl überprüft die Kompatibilität von Dateien und Ordnern in C:\DATA, führt jedoch keine Systemkompatibilitätsprüfung durch.</span><span class="sxs-lookup"><span data-stu-id="9787b-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="9787b-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="9787b-122">Example 3</span></span>
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

<span data-ttu-id="9787b-123">Mit diesem Befehl wird die Kompatibilität des Systems sowie von Dateien und Ordnern in C:\DATA überprüft und die Ergebnisse dann als #A0 in C:\results exportiert.</span><span class="sxs-lookup"><span data-stu-id="9787b-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="9787b-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9787b-124">PARAMETERS</span></span>

### <span data-ttu-id="9787b-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="9787b-125">-ComputerName</span></span>
<span data-ttu-id="9787b-126">Der Computer, auf dem Sie diese Überprüfung durchführen.</span><span class="sxs-lookup"><span data-stu-id="9787b-126">The computer you are performing this check on.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9787b-127">-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="9787b-127">-Credential</span></span>
<span data-ttu-id="9787b-128">Ihre Anmeldeinformationen für die Freigabe, die Sie überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9787b-128">Your credentials for the share you are validating.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9787b-129">-Path</span><span class="sxs-lookup"><span data-stu-id="9787b-129">-Path</span></span>
<span data-ttu-id="9787b-130">Der UNC-Pfad der Freigabe, die Sie überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9787b-130">The UNC path of the share you are validating.</span></span>

```yaml
Type: System.String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9787b-131">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="9787b-131">-SkipNamespaceChecks</span></span>
<span data-ttu-id="9787b-132">Legen Sie dieses Flag so ein, dass Dateinamespaceüberprüfungen übersprungen und nur Systemüberprüfungen durchzuführen sind.</span><span class="sxs-lookup"><span data-stu-id="9787b-132">Set this flag to skip file namespace validations and only perform system validations.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9787b-133">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="9787b-133">-SkipSystemChecks</span></span>
<span data-ttu-id="9787b-134">Legen Sie dieses Kennzeichen so ein, dass Systemüberprüfungen übersprungen und nur Dateinamespaceüberprüfungen ausführen.</span><span class="sxs-lookup"><span data-stu-id="9787b-134">Set this flag to skip system validations and only perform file namespace validations.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9787b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9787b-135">CommonParameters</span></span>
<span data-ttu-id="9787b-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9787b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9787b-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9787b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9787b-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9787b-138">INPUTS</span></span>

### <span data-ttu-id="9787b-139">Keine</span><span class="sxs-lookup"><span data-stu-id="9787b-139">None</span></span>

## <span data-ttu-id="9787b-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9787b-140">OUTPUTS</span></span>

### <span data-ttu-id="9787b-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="9787b-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="9787b-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9787b-142">NOTES</span></span>
* <span data-ttu-id="9787b-143">Schlüsselwörter: azure, Az, arm, resource, management, storagesync, filesync</span><span class="sxs-lookup"><span data-stu-id="9787b-143">Keywords: azure, Az, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="9787b-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9787b-144">RELATED LINKS</span></span>
