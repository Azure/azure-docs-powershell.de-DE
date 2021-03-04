---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 97e59efcc20f8ce025b2e90285ef051edc8272dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949144"
---
# <span data-ttu-id="5c29b-101">New-AzImageBuilderCustomizerObject</span><span class="sxs-lookup"><span data-stu-id="5c29b-101">New-AzImageBuilderCustomizerObject</span></span>

## <span data-ttu-id="5c29b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c29b-102">SYNOPSIS</span></span>
<span data-ttu-id="5c29b-103">Beschreibt eine Einheit der Bildanpassung</span><span class="sxs-lookup"><span data-stu-id="5c29b-103">Describes a unit of image customization</span></span>

## <span data-ttu-id="5c29b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c29b-104">SYNTAX</span></span>

### <span data-ttu-id="5c29b-105">ShellCustomizer (Standard)</span><span class="sxs-lookup"><span data-stu-id="5c29b-105">ShellCustomizer (Default)</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### <span data-ttu-id="5c29b-106">FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="5c29b-106">FileCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### <span data-ttu-id="5c29b-107">PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="5c29b-107">PowerShellCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c29b-108">RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="5c29b-108">RestartCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### <span data-ttu-id="5c29b-109">WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="5c29b-109">WindowsUpdateCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="5c29b-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c29b-110">DESCRIPTION</span></span>
<span data-ttu-id="5c29b-111">Beschreibt eine Einheit der Bildanpassung</span><span class="sxs-lookup"><span data-stu-id="5c29b-111">Describes a unit of image customization</span></span>

## <span data-ttu-id="5c29b-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5c29b-112">EXAMPLES</span></span>

### <span data-ttu-id="5c29b-113">Beispiel 1: Erstellen eines Windows-Update-Customizers</span><span class="sxs-lookup"><span data-stu-id="5c29b-113">Example 1: Create a windows update customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

<span data-ttu-id="5c29b-114">Mit diesem Befehl wird ein Windows-Update-Customizer erstellt.</span><span class="sxs-lookup"><span data-stu-id="5c29b-114">This command creates a windows update customizer.</span></span>

### <span data-ttu-id="5c29b-115">Beispiel 2: Erstellen eines Datei-Customizers</span><span class="sxs-lookup"><span data-stu-id="5c29b-115">Example 2: Create a file customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

<span data-ttu-id="5c29b-116">Mit diesem Befehl wird ein Datei-Customizer erstellt.</span><span class="sxs-lookup"><span data-stu-id="5c29b-116">This command creates a file customizer.</span></span>

### <span data-ttu-id="5c29b-117">Beispiel 3: Erstellen eines Powershell-Customizers</span><span class="sxs-lookup"><span data-stu-id="5c29b-117">Example 3: Create a powershell customizer</span></span>
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

<span data-ttu-id="5c29b-118">Mit diesem Befehl wird ein Powershell-Customizer erstellt.</span><span class="sxs-lookup"><span data-stu-id="5c29b-118">This command creates a powershell customizer.</span></span>

### <span data-ttu-id="5c29b-119">Beispiel 4: Erstellen eines Neustartanpassers</span><span class="sxs-lookup"><span data-stu-id="5c29b-119">Example 4: Create a restart customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

<span data-ttu-id="5c29b-120">Mit diesem Befehl wird ein Neustartanpasser erstellt.</span><span class="sxs-lookup"><span data-stu-id="5c29b-120">This command creates a restart customizer.</span></span>

### <span data-ttu-id="5c29b-121">Beispiel 5: Erstellen eines Shell-Customizers</span><span class="sxs-lookup"><span data-stu-id="5c29b-121">Example 5: Create a shell customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

<span data-ttu-id="5c29b-122">Mit diesem Befehl wird ein Shell-Customizer erstellt.</span><span class="sxs-lookup"><span data-stu-id="5c29b-122">This command creates a shell customizer.</span></span>

## <span data-ttu-id="5c29b-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5c29b-123">PARAMETERS</span></span>

### <span data-ttu-id="5c29b-124">-CustomizerName</span><span class="sxs-lookup"><span data-stu-id="5c29b-124">-CustomizerName</span></span>
<span data-ttu-id="5c29b-125">Anzeigename, um Kontext zu den Dienstleistungen dieses Anpassungsschritts zu liefern.</span><span class="sxs-lookup"><span data-stu-id="5c29b-125">Friendly Name to provide context on what this customization step does.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c29b-126">-Ziel</span><span class="sxs-lookup"><span data-stu-id="5c29b-126">-Destination</span></span>
<span data-ttu-id="5c29b-127">Der absolute Pfad zu einer Datei (mit bereits erstellten geschachtelten Verzeichnisstrukturen), in die die Datei (von sourceUri) in die VM hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="5c29b-127">The absolute path to a file (with nested directory structures already created) where the file (from sourceUri) will be uploaded to in the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c29b-128">-FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="5c29b-128">-FileCustomizer</span></span>
<span data-ttu-id="5c29b-129">Lädt Dateien in VMs (Linux, Windows) hoch.</span><span class="sxs-lookup"><span data-stu-id="5c29b-129">Uploads files to VMs (Linux, Windows).</span></span>
<span data-ttu-id="5c29b-130">Entspricht packer file provisioner.</span><span class="sxs-lookup"><span data-stu-id="5c29b-130">Corresponds to Packer file provisioner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c29b-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="5c29b-131">-Filter</span></span>
<span data-ttu-id="5c29b-132">Array von Filtern zum Auswählen von Aktualisierungen, die angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c29b-132">Array of filters to select updates to apply.</span></span>
<span data-ttu-id="5c29b-133">Lassen Sie leere Matrix weg, oder geben Sie sie an, um den Standard zu verwenden (kein Filter).</span><span class="sxs-lookup"><span data-stu-id="5c29b-133">Omit or specify empty array to use the default (no filter).</span></span>
<span data-ttu-id="5c29b-134">Beispiele und eine detaillierte Beschreibung dieses Felds finden Sie oben unter Link oben.</span><span class="sxs-lookup"><span data-stu-id="5c29b-134">Refer to above link for examples and detailed description of this field.</span></span>

```yaml
Type: System.String[]
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c29b-135">-Inline</span><span class="sxs-lookup"><span data-stu-id="5c29b-135">-Inline</span></span>
<span data-ttu-id="5c29b-136">Array der auszuführende Shellbefehle.</span><span class="sxs-lookup"><span data-stu-id="5c29b-136">Array of shell commands to execute.</span></span>

```yaml
Type: System.String[]
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c29b-137">-PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="5c29b-137">-PowerShellCustomizer</span></span>
<span data-ttu-id="5c29b-138">Führt die angegebene PowerShell auf der VM (Windows) aus.</span><span class="sxs-lookup"><span data-stu-id="5c29b-138">Runs the specified PowerShell on the VM (Windows).</span></span>
<span data-ttu-id="5c29b-139">Entspricht packer powershell provisioner.</span><span class="sxs-lookup"><span data-stu-id="5c29b-139">Corresponds to Packer powershell provisioner.</span></span>
<span data-ttu-id="5c29b-140">Genau einer von "scriptUri" oder "inline" kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5c29b-140">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PowerShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c29b-141">-RestartCheckCommand</span><span class="sxs-lookup"><span data-stu-id="5c29b-141">-RestartCheckCommand</span></span>
<span data-ttu-id="5c29b-142">Befehl, um zu überprüfen, ob der Neustart erfolgreich war [Standard: ''].</span><span class="sxs-lookup"><span data-stu-id="5c29b-142">Command to check if restart succeeded [Default: ''].</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c29b-143">-RestartCommand</span><span class="sxs-lookup"><span data-stu-id="5c29b-143">-RestartCommand</span></span>
<span data-ttu-id="5c29b-144">Befehl zum Ausführen des Neustarts [Standard: 'shutdown /r /f /t 0 /c packer restart']</span><span class="sxs-lookup"><span data-stu-id="5c29b-144">Command to execute the restart [Default: 'shutdown /r /f /t 0 /c packer restart']</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c29b-145">-RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="5c29b-145">-RestartCustomizer</span></span>
<span data-ttu-id="5c29b-146">Startet einen virtuellen Computer neu und wartet, bis er wieder online ist (Windows).</span><span class="sxs-lookup"><span data-stu-id="5c29b-146">Reboots a VM and waits for it to come back online (Windows).</span></span>
<span data-ttu-id="5c29b-147">Entspricht dem Packer Windows-Restart-Provisioner.</span><span class="sxs-lookup"><span data-stu-id="5c29b-147">Corresponds to Packer windows-restart provisioner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestartCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c29b-148">-RestartTimeout</span><span class="sxs-lookup"><span data-stu-id="5c29b-148">-RestartTimeout</span></span>
<span data-ttu-id="5c29b-149">Neustarttimeout als Zeichenfolge der Größe und Einheit angegeben, z. B. "5m" (5 Minuten) oder "2 Stunden" (2 Stunden) [Standard: '5m'].</span><span class="sxs-lookup"><span data-stu-id="5c29b-149">Restart timeout specified as a string of magnitude and unit, e.g. '5m' (5 minutes) or '2h' (2 hours) [Default: '5m'].</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c29b-150">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="5c29b-150">-RunElevated</span></span>
<span data-ttu-id="5c29b-151">Wenn angegeben, wird das PowerShell-Skript mit erhöhten Rechten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5c29b-151">If specified, the PowerShell script will be run with elevated privileges.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c29b-152">-ScriptUri</span><span class="sxs-lookup"><span data-stu-id="5c29b-152">-ScriptUri</span></span>
<span data-ttu-id="5c29b-153">URI des Shellskripts, das zum Anpassen ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c29b-153">URI of the shell script to be run for customizing.</span></span>
<span data-ttu-id="5c29b-154">Dabei kann es sich um einen Githublink, SAS-URI für Azure Storage usw. geben.</span><span class="sxs-lookup"><span data-stu-id="5c29b-154">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c29b-155">-SearchCriterion</span><span class="sxs-lookup"><span data-stu-id="5c29b-155">-SearchCriterion</span></span>
<span data-ttu-id="5c29b-156">Kriterien zum Durchsuchen von Updates.</span><span class="sxs-lookup"><span data-stu-id="5c29b-156">Criteria to search updates.</span></span>
<span data-ttu-id="5c29b-157">Lassen Sie leere Zeichenfolge weg, oder geben Sie sie an, um die Standardzeichenfolge zu verwenden (alle durchsuchen).</span><span class="sxs-lookup"><span data-stu-id="5c29b-157">Omit or specify empty string to use the default (search all).</span></span>
<span data-ttu-id="5c29b-158">Beispiele und eine detaillierte Beschreibung dieses Felds finden Sie oben unter Link oben.</span><span class="sxs-lookup"><span data-stu-id="5c29b-158">Refer to above link for examples and detailed description of this field.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c29b-159">-Sha256Checksum</span><span class="sxs-lookup"><span data-stu-id="5c29b-159">-Sha256Checksum</span></span>
<span data-ttu-id="5c29b-160">SHA256-Prüfsumme des Shellskripts, das im Feld "scriptUri" bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5c29b-160">SHA256 checksum of the shell script provided in the scriptUri field.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer, PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c29b-161">-ShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="5c29b-161">-ShellCustomizer</span></span>
<span data-ttu-id="5c29b-162">Führt während der Anpassungsphase (Linux) ein Shellskript aus.</span><span class="sxs-lookup"><span data-stu-id="5c29b-162">Runs a shell script during the customization phase (Linux).</span></span>
<span data-ttu-id="5c29b-163">Entspricht dem Packer-Shell-Provisioner.</span><span class="sxs-lookup"><span data-stu-id="5c29b-163">Corresponds to Packer shell provisioner.</span></span>
<span data-ttu-id="5c29b-164">Genau einer von "scriptUri" oder "inline" kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5c29b-164">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c29b-165">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="5c29b-165">-SourceUri</span></span>
<span data-ttu-id="5c29b-166">Der URI der Datei, die zum Anpassen der VM hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c29b-166">The URI of the file to be uploaded for customizing the VM.</span></span>
<span data-ttu-id="5c29b-167">Dabei kann es sich um einen Githublink, SAS-URI für Azure Storage usw. geben.</span><span class="sxs-lookup"><span data-stu-id="5c29b-167">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c29b-168">-UpdateLimit</span><span class="sxs-lookup"><span data-stu-id="5c29b-168">-UpdateLimit</span></span>
<span data-ttu-id="5c29b-169">Maximale Anzahl von Updates, die gleichzeitig angewendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5c29b-169">Maximum number of updates to apply at a time.</span></span>
<span data-ttu-id="5c29b-170">Geben Sie 0 weg, um den Standardwert (1000) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c29b-170">Omit or specify 0 to use the default (1000).</span></span>

```yaml
Type: System.Int32
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c29b-171">-ValidExitCode</span><span class="sxs-lookup"><span data-stu-id="5c29b-171">-ValidExitCode</span></span>
<span data-ttu-id="5c29b-172">Gültige Ausgangscodes für das PowerShell-Skript.</span><span class="sxs-lookup"><span data-stu-id="5c29b-172">Valid exit codes for the PowerShell script.</span></span>
<span data-ttu-id="5c29b-173">[Standard: 0].</span><span class="sxs-lookup"><span data-stu-id="5c29b-173">[Default: 0].</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c29b-174">-WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="5c29b-174">-WindowsUpdateCustomizer</span></span>
<span data-ttu-id="5c29b-175">Installiert Windows-Updates.</span><span class="sxs-lookup"><span data-stu-id="5c29b-175">Installs Windows Updates.</span></span>
<span data-ttu-id="5c29b-176">Entspricht packer Windows Update Provisioner ( https://github.com/rgl/packer-provisioner-windows-update) .</span><span class="sxs-lookup"><span data-stu-id="5c29b-176">Corresponds to Packer Windows Update Provisioner (https://github.com/rgl/packer-provisioner-windows-update).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c29b-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c29b-177">CommonParameters</span></span>
<span data-ttu-id="5c29b-178">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c29b-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c29b-179">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c29b-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c29b-180">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5c29b-180">INPUTS</span></span>

## <span data-ttu-id="5c29b-181">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5c29b-181">OUTPUTS</span></span>

### <span data-ttu-id="5c29b-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span><span class="sxs-lookup"><span data-stu-id="5c29b-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span></span>

## <span data-ttu-id="5c29b-183">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5c29b-183">NOTES</span></span>

<span data-ttu-id="5c29b-184">ALIASE</span><span class="sxs-lookup"><span data-stu-id="5c29b-184">ALIASES</span></span>

## <span data-ttu-id="5c29b-185">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5c29b-185">RELATED LINKS</span></span>

