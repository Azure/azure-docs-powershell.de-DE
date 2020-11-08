---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003337"
---
# <span data-ttu-id="60282-101">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="60282-101">Invoke-AzStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="60282-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60282-102">SYNOPSIS</span></span>
<span data-ttu-id="60282-103">Überprüft mögliche Kompatibilitätsprobleme zwischen der System-und Azure-Dateisynchronisierung.</span><span class="sxs-lookup"><span data-stu-id="60282-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

## <span data-ttu-id="60282-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60282-104">SYNTAX</span></span>

### <span data-ttu-id="60282-105">PathBased (Standard)</span><span class="sxs-lookup"><span data-stu-id="60282-105">PathBased (Default)</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### <span data-ttu-id="60282-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="60282-106">ComputerNameBased</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## <span data-ttu-id="60282-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60282-107">DESCRIPTION</span></span>
<span data-ttu-id="60282-108">Das Cmdlet **Invoke-AzStorageSyncCompatibilityCheck** überprüft potenzielle Kompatibilitätsprobleme zwischen der System-und Azure-Dateisynchronisierung. Bei einem lokalen oder Remotepfad wird eine Reihe von Validierungen für den System-und Datei Namespace durchgeführt und dann alle gefundenen Kompatibilitätsprobleme zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="60282-108">The **Invoke-AzStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="60282-109">System Prüfungen:</span><span class="sxs-lookup"><span data-stu-id="60282-109">System checks:</span></span>
- <span data-ttu-id="60282-110">System Kompatibilitätsdatei-Namespace überprüft:</span><span class="sxs-lookup"><span data-stu-id="60282-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="60282-111">Nicht unterstützte Zeichen</span><span class="sxs-lookup"><span data-stu-id="60282-111">Unsupported characters</span></span>
- <span data-ttu-id="60282-112">Maximale Dateigröße</span><span class="sxs-lookup"><span data-stu-id="60282-112">Maximum file size</span></span>
- <span data-ttu-id="60282-113">Maximale Länge des Pfads</span><span class="sxs-lookup"><span data-stu-id="60282-113">Maximum path length</span></span>
- <span data-ttu-id="60282-114">Maximale Dateilänge</span><span class="sxs-lookup"><span data-stu-id="60282-114">Maximum file length</span></span>
- <span data-ttu-id="60282-115">Maximale Datensatzgröße</span><span class="sxs-lookup"><span data-stu-id="60282-115">Maximum dataset size</span></span>
- <span data-ttu-id="60282-116">Maximale Verzeichnistiefe</span><span class="sxs-lookup"><span data-stu-id="60282-116">Maximum directory depth</span></span>

## <span data-ttu-id="60282-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60282-117">EXAMPLES</span></span>

### <span data-ttu-id="60282-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="60282-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="60282-119">Dieser Befehl überprüft die Kompatibilität des Systems und auch von Dateien und Ordnern in C:\data.</span><span class="sxs-lookup"><span data-stu-id="60282-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="60282-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="60282-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="60282-121">Dieser Befehl überprüft die Kompatibilität von Dateien und Ordnern in C:\data, führt jedoch keine System Kompatibilitätsüberprüfung durch.</span><span class="sxs-lookup"><span data-stu-id="60282-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="60282-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="60282-122">Example 3</span></span>
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

<span data-ttu-id="60282-123">Dieser Befehl überprüft die Kompatibilität des Systems und auch von Dateien und Ordnern in C:\data und exportiert die Ergebnisse dann als CSV-Datei in C:\results.</span><span class="sxs-lookup"><span data-stu-id="60282-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="60282-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="60282-124">PARAMETERS</span></span>

### <span data-ttu-id="60282-125">-Computername</span><span class="sxs-lookup"><span data-stu-id="60282-125">-ComputerName</span></span>
<span data-ttu-id="60282-126">Der Computer, auf dem Sie diese Prüfung durchführen.</span><span class="sxs-lookup"><span data-stu-id="60282-126">The computer you are performing this check on.</span></span>

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

### <span data-ttu-id="60282-127">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="60282-127">-Credential</span></span>
<span data-ttu-id="60282-128">Ihre Anmeldeinformationen für die Freigabe, die Sie überprüfen.</span><span class="sxs-lookup"><span data-stu-id="60282-128">Your credentials for the share you are validating.</span></span>

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

### <span data-ttu-id="60282-129">-Path</span><span class="sxs-lookup"><span data-stu-id="60282-129">-Path</span></span>
<span data-ttu-id="60282-130">Der UNC-Pfad der Freigabe, die Sie überprüfen.</span><span class="sxs-lookup"><span data-stu-id="60282-130">The UNC path of the share you are validating.</span></span>

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

### <span data-ttu-id="60282-131">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="60282-131">-SkipNamespaceChecks</span></span>
<span data-ttu-id="60282-132">Setzen Sie dieses Flag, um Datei Namespace-Validierungen zu überspringen und nur System Validierungen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="60282-132">Set this flag to skip file namespace validations and only perform system validations.</span></span>

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

### <span data-ttu-id="60282-133">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="60282-133">-SkipSystemChecks</span></span>
<span data-ttu-id="60282-134">Legen Sie dieses Flag so ein, dass System Validierungen übersprungen werden und nur Datei Namespace-Validierungen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="60282-134">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="60282-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60282-135">CommonParameters</span></span>
<span data-ttu-id="60282-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60282-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60282-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60282-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60282-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60282-138">INPUTS</span></span>

### <span data-ttu-id="60282-139">Keine</span><span class="sxs-lookup"><span data-stu-id="60282-139">None</span></span>

## <span data-ttu-id="60282-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60282-140">OUTPUTS</span></span>

### <span data-ttu-id="60282-141">Microsoft. Azure. Commands. StorageSync. Evaluation. Models. PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="60282-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="60282-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="60282-142">NOTES</span></span>
* <span data-ttu-id="60282-143">Schlüsselwörter: Azure, AZ, arm, Resource, Verwaltung, storagesync, FileSync</span><span class="sxs-lookup"><span data-stu-id="60282-143">Keywords: azure, Az, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="60282-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60282-144">RELATED LINKS</span></span>
