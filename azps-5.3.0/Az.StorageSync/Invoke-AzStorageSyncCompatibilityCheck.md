---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460127"
---
# <span data-ttu-id="dedd3-101">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="dedd3-101">Invoke-AzStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="dedd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dedd3-102">SYNOPSIS</span></span>
<span data-ttu-id="dedd3-103">Sucht nach potenziellen Kompatibilitätsproblemen zwischen Ihrem System und der Azure File Sync.</span><span class="sxs-lookup"><span data-stu-id="dedd3-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

## <span data-ttu-id="dedd3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dedd3-104">SYNTAX</span></span>

### <span data-ttu-id="dedd3-105">PathBased (Standard)</span><span class="sxs-lookup"><span data-stu-id="dedd3-105">PathBased (Default)</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### <span data-ttu-id="dedd3-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="dedd3-106">ComputerNameBased</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## <span data-ttu-id="dedd3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dedd3-107">DESCRIPTION</span></span>
<span data-ttu-id="dedd3-108">Das **Cmdlet Invoke-AzStorageSyncCompatibilityCheck** sucht nach potenziellen Kompatibilitätsproblemen zwischen Ihrem System und der Azure File Sync. Bei einem lokalen Pfad oder Remotepfad führt er eine Reihe von Überprüfungen für den System- und Dateinamespace aus und gibt dann alle gefundenen Kompatibilitätsprobleme zurück.</span><span class="sxs-lookup"><span data-stu-id="dedd3-108">The **Invoke-AzStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="dedd3-109">Systemprüfungen:</span><span class="sxs-lookup"><span data-stu-id="dedd3-109">System checks:</span></span>
- <span data-ttu-id="dedd3-110">Betriebssystemkompatibilität: Dateinamespaceprüfungen:</span><span class="sxs-lookup"><span data-stu-id="dedd3-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="dedd3-111">Nicht unterstützte Zeichen</span><span class="sxs-lookup"><span data-stu-id="dedd3-111">Unsupported characters</span></span>
- <span data-ttu-id="dedd3-112">Maximale Dateigröße</span><span class="sxs-lookup"><span data-stu-id="dedd3-112">Maximum file size</span></span>
- <span data-ttu-id="dedd3-113">Maximale Pfadlänge</span><span class="sxs-lookup"><span data-stu-id="dedd3-113">Maximum path length</span></span>
- <span data-ttu-id="dedd3-114">Maximale Dateilänge</span><span class="sxs-lookup"><span data-stu-id="dedd3-114">Maximum file length</span></span>
- <span data-ttu-id="dedd3-115">Maximale Datasetgröße</span><span class="sxs-lookup"><span data-stu-id="dedd3-115">Maximum dataset size</span></span>
- <span data-ttu-id="dedd3-116">Maximale Verzeichnistiefe</span><span class="sxs-lookup"><span data-stu-id="dedd3-116">Maximum directory depth</span></span>

## <span data-ttu-id="dedd3-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dedd3-117">EXAMPLES</span></span>

### <span data-ttu-id="dedd3-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dedd3-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="dedd3-119">Dieser Befehl überprüft die Kompatibilität des Systems sowie von Dateien und Ordnern in "C:\DATA".</span><span class="sxs-lookup"><span data-stu-id="dedd3-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="dedd3-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="dedd3-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="dedd3-121">Dieser Befehl überprüft die Kompatibilität von Dateien und Ordnern in "C:\DATA", führt aber keine Systemkompatibilitätsprüfung aus.</span><span class="sxs-lookup"><span data-stu-id="dedd3-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="dedd3-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="dedd3-122">Example 3</span></span>
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

<span data-ttu-id="dedd3-123">Mit diesem Befehl wird die Kompatibilität des Systems sowie von Dateien und Ordnern in "C:\DATA" überprüft und die Ergebnisse dann als #A0 in "C:\results" exportiert.</span><span class="sxs-lookup"><span data-stu-id="dedd3-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="dedd3-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dedd3-124">PARAMETERS</span></span>

### <span data-ttu-id="dedd3-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="dedd3-125">-ComputerName</span></span>
<span data-ttu-id="dedd3-126">Der Computer, auf dem Sie diese Überprüfung durchführen.</span><span class="sxs-lookup"><span data-stu-id="dedd3-126">The computer you are performing this check on.</span></span>

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

### <span data-ttu-id="dedd3-127">-Credential</span><span class="sxs-lookup"><span data-stu-id="dedd3-127">-Credential</span></span>
<span data-ttu-id="dedd3-128">Ihre Anmeldeinformationen für die Freigabe, die Sie überprüfen.</span><span class="sxs-lookup"><span data-stu-id="dedd3-128">Your credentials for the share you are validating.</span></span>

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

### <span data-ttu-id="dedd3-129">-Path</span><span class="sxs-lookup"><span data-stu-id="dedd3-129">-Path</span></span>
<span data-ttu-id="dedd3-130">Der UNC-Pfad der Freigabe, die Sie überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="dedd3-130">The UNC path of the share you are validating.</span></span>

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

### <span data-ttu-id="dedd3-131">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="dedd3-131">-SkipNamespaceChecks</span></span>
<span data-ttu-id="dedd3-132">Legen Sie dieses Kennzeichen so ein, dass Dateinamespaceüberprüfungen übersprungen und nur Systemüberprüfungen durchzuführen sind.</span><span class="sxs-lookup"><span data-stu-id="dedd3-132">Set this flag to skip file namespace validations and only perform system validations.</span></span>

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

### <span data-ttu-id="dedd3-133">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="dedd3-133">-SkipSystemChecks</span></span>
<span data-ttu-id="dedd3-134">Legen Sie dieses Kennzeichen so ein, dass Systemüberprüfungen übersprungen und nur Dateinamespaceüberprüfungen durchzuführen sind.</span><span class="sxs-lookup"><span data-stu-id="dedd3-134">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="dedd3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dedd3-135">CommonParameters</span></span>
<span data-ttu-id="dedd3-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dedd3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dedd3-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dedd3-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dedd3-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dedd3-138">INPUTS</span></span>

### <span data-ttu-id="dedd3-139">Keine</span><span class="sxs-lookup"><span data-stu-id="dedd3-139">None</span></span>

## <span data-ttu-id="dedd3-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dedd3-140">OUTPUTS</span></span>

### <span data-ttu-id="dedd3-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="dedd3-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="dedd3-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dedd3-142">NOTES</span></span>
* <span data-ttu-id="dedd3-143">Schlüsselwörter: azure, Az, arm, resource, management, storagesync, filesync</span><span class="sxs-lookup"><span data-stu-id="dedd3-143">Keywords: azure, Az, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="dedd3-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dedd3-144">RELATED LINKS</span></span>
