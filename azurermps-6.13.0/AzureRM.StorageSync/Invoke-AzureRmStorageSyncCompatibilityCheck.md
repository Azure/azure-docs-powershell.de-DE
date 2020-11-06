---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: AzureRM.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storagesync/invoke-azurermstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 73e0f00fe184a5462141b060717ca64567d4a67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498126"
---
# <span data-ttu-id="d98bd-101">Invoke-AzureRmStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="d98bd-101">Invoke-AzureRmStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="d98bd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d98bd-102">SYNOPSIS</span></span>
<span data-ttu-id="d98bd-103">Überprüft mögliche Kompatibilitätsprobleme zwischen der System-und Azure-Dateisynchronisierung.</span><span class="sxs-lookup"><span data-stu-id="d98bd-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d98bd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d98bd-104">SYNTAX</span></span>

### <span data-ttu-id="d98bd-105">PathBased (Standard)</span><span class="sxs-lookup"><span data-stu-id="d98bd-105">PathBased (Default)</span></span>
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [-Quiet] [<CommonParameters>]
```

### <span data-ttu-id="d98bd-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="d98bd-106">ComputerNameBased</span></span>
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [-Quiet] [<CommonParameters>]
```

## <span data-ttu-id="d98bd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d98bd-107">DESCRIPTION</span></span>
<span data-ttu-id="d98bd-108">Das Cmdlet **Invoke-AzureRmStorageSyncCompatibilityCheck** überprüft potenzielle Kompatibilitätsprobleme zwischen der System-und Azure-Dateisynchronisierung. Bei einem lokalen oder Remotepfad wird eine Reihe von Validierungen für den System-und Datei Namespace durchgeführt und dann alle gefundenen Kompatibilitätsprobleme zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d98bd-108">The **Invoke-AzureRmStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="d98bd-109">System Prüfungen:</span><span class="sxs-lookup"><span data-stu-id="d98bd-109">System checks:</span></span>
- <span data-ttu-id="d98bd-110">System Kompatibilitätsdatei-Namespace überprüft:</span><span class="sxs-lookup"><span data-stu-id="d98bd-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="d98bd-111">Nicht unterstützte Zeichen</span><span class="sxs-lookup"><span data-stu-id="d98bd-111">Unsupported characters</span></span>
- <span data-ttu-id="d98bd-112">Maximale Dateigröße</span><span class="sxs-lookup"><span data-stu-id="d98bd-112">Maximum file size</span></span>
- <span data-ttu-id="d98bd-113">Maximale Länge des Pfads</span><span class="sxs-lookup"><span data-stu-id="d98bd-113">Maximum path length</span></span>
- <span data-ttu-id="d98bd-114">Maximale Dateilänge</span><span class="sxs-lookup"><span data-stu-id="d98bd-114">Maximum file length</span></span>
- <span data-ttu-id="d98bd-115">Maximale Datensatzgröße</span><span class="sxs-lookup"><span data-stu-id="d98bd-115">Maximum dataset size</span></span>
- <span data-ttu-id="d98bd-116">Maximale Verzeichnistiefe</span><span class="sxs-lookup"><span data-stu-id="d98bd-116">Maximum directory depth</span></span>

## <span data-ttu-id="d98bd-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d98bd-117">EXAMPLES</span></span>

### <span data-ttu-id="d98bd-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d98bd-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="d98bd-119">Dieser Befehl überprüft die Kompatibilität des Systems und auch von Dateien und Ordnern in C:\data.</span><span class="sxs-lookup"><span data-stu-id="d98bd-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="d98bd-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d98bd-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="d98bd-121">Dieser Befehl überprüft die Kompatibilität von Dateien und Ordnern in C:\data, führt jedoch keine System Kompatibilitätsüberprüfung durch.</span><span class="sxs-lookup"><span data-stu-id="d98bd-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="d98bd-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d98bd-122">Example 3</span></span>
```powershell
PS C:\> $errors = Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
PS C:\> $errors | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results
```

<span data-ttu-id="d98bd-123">Dieser Befehl überprüft die Kompatibilität des Systems und auch von Dateien und Ordnern in C:\data und exportiert die Ergebnisse dann als CSV-Datei in C:\results.</span><span class="sxs-lookup"><span data-stu-id="d98bd-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="d98bd-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="d98bd-124">PARAMETERS</span></span>

### <span data-ttu-id="d98bd-125">-Computername</span><span class="sxs-lookup"><span data-stu-id="d98bd-125">-ComputerName</span></span>
<span data-ttu-id="d98bd-126">Der Computer, auf dem Sie diese Prüfung durchführen.</span><span class="sxs-lookup"><span data-stu-id="d98bd-126">The computer you are performing this check on.</span></span>

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

### <span data-ttu-id="d98bd-127">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="d98bd-127">-Credential</span></span>
<span data-ttu-id="d98bd-128">Ihre Anmeldeinformationen für die Freigabe, die Sie überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d98bd-128">Your credentials for the share you are validating.</span></span>

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

### <span data-ttu-id="d98bd-129">-Path</span><span class="sxs-lookup"><span data-stu-id="d98bd-129">-Path</span></span>
<span data-ttu-id="d98bd-130">Der UNC-Pfad der Freigabe, die Sie überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d98bd-130">The UNC path of the share you are validating.</span></span>

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

### <span data-ttu-id="d98bd-131">– Ruhig</span><span class="sxs-lookup"><span data-stu-id="d98bd-131">-Quiet</span></span>
<span data-ttu-id="d98bd-132">Unterdrückt das Schreiben des Ausgabe Berichts an die Konsole.</span><span class="sxs-lookup"><span data-stu-id="d98bd-132">Suppresses writing output report to console.</span></span>

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

### <span data-ttu-id="d98bd-133">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="d98bd-133">-SkipNamespaceChecks</span></span>
<span data-ttu-id="d98bd-134">Setzen Sie dieses Flag, um Datei Namespace-Validierungen zu überspringen und nur System Validierungen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="d98bd-134">Set this flag to skip file namespace validations and only perform system validations.</span></span>

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

### <span data-ttu-id="d98bd-135">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="d98bd-135">-SkipSystemChecks</span></span>
<span data-ttu-id="d98bd-136">Legen Sie dieses Flag so ein, dass System Validierungen übersprungen werden und nur Datei Namespace-Validierungen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d98bd-136">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="d98bd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d98bd-137">CommonParameters</span></span>
<span data-ttu-id="d98bd-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d98bd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d98bd-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d98bd-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d98bd-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d98bd-140">INPUTS</span></span>

### <span data-ttu-id="d98bd-141">Keine</span><span class="sxs-lookup"><span data-stu-id="d98bd-141">None</span></span>

## <span data-ttu-id="d98bd-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d98bd-142">OUTPUTS</span></span>

### <span data-ttu-id="d98bd-143">Microsoft. Azure. Commands. StorageSync. Evaluation. Models. PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="d98bd-143">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="d98bd-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="d98bd-144">NOTES</span></span>
* <span data-ttu-id="d98bd-145">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, storagesync, FileSync</span><span class="sxs-lookup"><span data-stu-id="d98bd-145">Keywords: azure, azurerm, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="d98bd-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d98bd-146">RELATED LINKS</span></span>
