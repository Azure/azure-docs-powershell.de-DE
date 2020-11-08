---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 3e67452a5d5e11fa4aa96d1b38b80a4284c21f00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008293"
---
# <span data-ttu-id="39c23-101">New-AzImageBuilderCustomizerObject</span><span class="sxs-lookup"><span data-stu-id="39c23-101">New-AzImageBuilderCustomizerObject</span></span>

## <span data-ttu-id="39c23-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="39c23-102">SYNOPSIS</span></span>
<span data-ttu-id="39c23-103">Beschreibt eine Einheit der Bildanpassung</span><span class="sxs-lookup"><span data-stu-id="39c23-103">Describes a unit of image customization</span></span>

## <span data-ttu-id="39c23-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="39c23-104">SYNTAX</span></span>

### <span data-ttu-id="39c23-105">ShellCustomizer (Standard)</span><span class="sxs-lookup"><span data-stu-id="39c23-105">ShellCustomizer (Default)</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### <span data-ttu-id="39c23-106">Filecustomizer</span><span class="sxs-lookup"><span data-stu-id="39c23-106">FileCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### <span data-ttu-id="39c23-107">PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="39c23-107">PowerShellCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### <span data-ttu-id="39c23-108">RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="39c23-108">RestartCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### <span data-ttu-id="39c23-109">WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="39c23-109">WindowsUpdateCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="39c23-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39c23-110">DESCRIPTION</span></span>
<span data-ttu-id="39c23-111">Beschreibt eine Einheit der Bildanpassung</span><span class="sxs-lookup"><span data-stu-id="39c23-111">Describes a unit of image customization</span></span>

## <span data-ttu-id="39c23-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39c23-112">EXAMPLES</span></span>

### <span data-ttu-id="39c23-113">Beispiel 1: Erstellen eines Windows Update-Customizers</span><span class="sxs-lookup"><span data-stu-id="39c23-113">Example 1: Create a windows update customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

<span data-ttu-id="39c23-114">Mit diesem Befehl wird ein Windows Update-Customizer erstellt.</span><span class="sxs-lookup"><span data-stu-id="39c23-114">This command creates a windows update customizer.</span></span>

### <span data-ttu-id="39c23-115">Beispiel 2: Erstellen einer Datei Anpassung</span><span class="sxs-lookup"><span data-stu-id="39c23-115">Example 2: Create a file customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

<span data-ttu-id="39c23-116">Mit diesem Befehl wird ein Datei-Customizer erstellt.</span><span class="sxs-lookup"><span data-stu-id="39c23-116">This command creates a file customizer.</span></span>

### <span data-ttu-id="39c23-117">Beispiel 3: Erstellen eines PowerShell-Customizers</span><span class="sxs-lookup"><span data-stu-id="39c23-117">Example 3: Create a powershell customizer</span></span>
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

<span data-ttu-id="39c23-118">Mit diesem Befehl wird ein PowerShell-Customizer erstellt.</span><span class="sxs-lookup"><span data-stu-id="39c23-118">This command creates a powershell customizer.</span></span>

### <span data-ttu-id="39c23-119">Beispiel 4: Erstellen eines Neustart-Customizers</span><span class="sxs-lookup"><span data-stu-id="39c23-119">Example 4: Create a restart customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

<span data-ttu-id="39c23-120">Mit diesem Befehl wird ein Neustart-Customizer erstellt.</span><span class="sxs-lookup"><span data-stu-id="39c23-120">This command creates a restart customizer.</span></span>

### <span data-ttu-id="39c23-121">Beispiel 5: Erstellen eines Shell-Customizers</span><span class="sxs-lookup"><span data-stu-id="39c23-121">Example 5: Create a shell customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

<span data-ttu-id="39c23-122">Mit diesem Befehl wird ein Shell-Customizer erstellt.</span><span class="sxs-lookup"><span data-stu-id="39c23-122">This command creates a shell customizer.</span></span>

## <span data-ttu-id="39c23-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="39c23-123">PARAMETERS</span></span>

### <span data-ttu-id="39c23-124">-CustomizerName</span><span class="sxs-lookup"><span data-stu-id="39c23-124">-CustomizerName</span></span>
<span data-ttu-id="39c23-125">Anzeige Name, um einen Kontext zu dem zu liefern, was dieser Anpassungs Schritt macht.</span><span class="sxs-lookup"><span data-stu-id="39c23-125">Friendly Name to provide context on what this customization step does.</span></span>

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

### <span data-ttu-id="39c23-126">-Ziel</span><span class="sxs-lookup"><span data-stu-id="39c23-126">-Destination</span></span>
<span data-ttu-id="39c23-127">Der absolute Pfad zu einer Datei (mit bereits erstellten geschachtelten Verzeichnisstrukturen), in der die Datei (von SourceUri) in den virtuellen Computer hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="39c23-127">The absolute path to a file (with nested directory structures already created) where the file (from sourceUri) will be uploaded to in the VM.</span></span>

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

### <span data-ttu-id="39c23-128">-Filecustomizer</span><span class="sxs-lookup"><span data-stu-id="39c23-128">-FileCustomizer</span></span>
<span data-ttu-id="39c23-129">Lädt Dateien auf VMS (Linux, Windows) hoch.</span><span class="sxs-lookup"><span data-stu-id="39c23-129">Uploads files to VMs (Linux, Windows).</span></span>
<span data-ttu-id="39c23-130">Entspricht dem Packer-Datei Provisioner.</span><span class="sxs-lookup"><span data-stu-id="39c23-130">Corresponds to Packer file provisioner.</span></span>

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

### <span data-ttu-id="39c23-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="39c23-131">-Filter</span></span>
<span data-ttu-id="39c23-132">Array von Filtern, um Updates auszuwählen, die angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="39c23-132">Array of filters to select updates to apply.</span></span>
<span data-ttu-id="39c23-133">Geben Sie das leere Array aus, um den Standardwert (kein Filter) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="39c23-133">Omit or specify empty array to use the default (no filter).</span></span>
<span data-ttu-id="39c23-134">Beispiele und eine detaillierte Beschreibung dieses Felds finden Sie im obigen Link.</span><span class="sxs-lookup"><span data-stu-id="39c23-134">Refer to above link for examples and detailed description of this field.</span></span>

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

### <span data-ttu-id="39c23-135">-Inline</span><span class="sxs-lookup"><span data-stu-id="39c23-135">-Inline</span></span>
<span data-ttu-id="39c23-136">Array von Shell-Befehlen, die ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="39c23-136">Array of shell commands to execute.</span></span>

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

### <span data-ttu-id="39c23-137">-PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="39c23-137">-PowerShellCustomizer</span></span>
<span data-ttu-id="39c23-138">Führt die angegebene PowerShell auf dem virtuellen Computer (Windows) aus.</span><span class="sxs-lookup"><span data-stu-id="39c23-138">Runs the specified PowerShell on the VM (Windows).</span></span>
<span data-ttu-id="39c23-139">Entspricht Packer PowerShell Provisioner.</span><span class="sxs-lookup"><span data-stu-id="39c23-139">Corresponds to Packer powershell provisioner.</span></span>
<span data-ttu-id="39c23-140">Genau eine von "scriptUri" oder "Inline" kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="39c23-140">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

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

### <span data-ttu-id="39c23-141">-RestartCheckCommand</span><span class="sxs-lookup"><span data-stu-id="39c23-141">-RestartCheckCommand</span></span>
<span data-ttu-id="39c23-142">Befehl zum Überprüfen, ob Restart erfolgreich war [Standard: ' '].</span><span class="sxs-lookup"><span data-stu-id="39c23-142">Command to check if restart succeeded [Default: ''].</span></span>

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

### <span data-ttu-id="39c23-143">-RestartCommand</span><span class="sxs-lookup"><span data-stu-id="39c23-143">-RestartCommand</span></span>
<span data-ttu-id="39c23-144">Befehl zum Ausführen des Neustarts [Standard: ' Shutdown/r/f/t 0/c Packer restart ']</span><span class="sxs-lookup"><span data-stu-id="39c23-144">Command to execute the restart [Default: 'shutdown /r /f /t 0 /c packer restart']</span></span>

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

### <span data-ttu-id="39c23-145">-RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="39c23-145">-RestartCustomizer</span></span>
<span data-ttu-id="39c23-146">Startet einen virtuellen Computer neu und wartet darauf, dass er wieder online geschaltet wird (Windows).</span><span class="sxs-lookup"><span data-stu-id="39c23-146">Reboots a VM and waits for it to come back online (Windows).</span></span>
<span data-ttu-id="39c23-147">Entspricht Packer Windows – starten Sie Provisioner erneut.</span><span class="sxs-lookup"><span data-stu-id="39c23-147">Corresponds to Packer windows-restart provisioner.</span></span>

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

### <span data-ttu-id="39c23-148">-RestartTimeout</span><span class="sxs-lookup"><span data-stu-id="39c23-148">-RestartTimeout</span></span>
<span data-ttu-id="39c23-149">Neustart-Timeout, angegeben als eine Zeichenfolge von Größe und Einheit, beispielsweise "5M" (5 Minuten) oder "2H" (2 Stunden) [Standard: ' 5M '].</span><span class="sxs-lookup"><span data-stu-id="39c23-149">Restart timeout specified as a string of magnitude and unit, e.g. '5m' (5 minutes) or '2h' (2 hours) [Default: '5m'].</span></span>

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

### <span data-ttu-id="39c23-150">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="39c23-150">-RunElevated</span></span>
<span data-ttu-id="39c23-151">Wenn angegeben, wird das PowerShell-Skript mit erhöhten Rechten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39c23-151">If specified, the PowerShell script will be run with elevated privileges.</span></span>

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

### <span data-ttu-id="39c23-152">-ScriptUri</span><span class="sxs-lookup"><span data-stu-id="39c23-152">-ScriptUri</span></span>
<span data-ttu-id="39c23-153">Der URI des Shell-Skripts, das für das Customizing ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="39c23-153">URI of the shell script to be run for customizing.</span></span>
<span data-ttu-id="39c23-154">Hierbei kann es sich um einen GitHub-Link, SAS-URI für Azure-Speicher usw. handeln.</span><span class="sxs-lookup"><span data-stu-id="39c23-154">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

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

### <span data-ttu-id="39c23-155">-SearchCriterion</span><span class="sxs-lookup"><span data-stu-id="39c23-155">-SearchCriterion</span></span>
<span data-ttu-id="39c23-156">Kriterien zum Durchsuchen von Updates</span><span class="sxs-lookup"><span data-stu-id="39c23-156">Criteria to search updates.</span></span>
<span data-ttu-id="39c23-157">Geben Sie eine leere Zeichenfolge aus, um den Standardwert (alle durchsuchen) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="39c23-157">Omit or specify empty string to use the default (search all).</span></span>
<span data-ttu-id="39c23-158">Beispiele und eine detaillierte Beschreibung dieses Felds finden Sie im obigen Link.</span><span class="sxs-lookup"><span data-stu-id="39c23-158">Refer to above link for examples and detailed description of this field.</span></span>

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

### <span data-ttu-id="39c23-159">-Sha256Checksum</span><span class="sxs-lookup"><span data-stu-id="39c23-159">-Sha256Checksum</span></span>
<span data-ttu-id="39c23-160">SHA256-Prüfsumme des Shell-Skripts, das im Feld scriptUri bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="39c23-160">SHA256 checksum of the shell script provided in the scriptUri field.</span></span>

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

### <span data-ttu-id="39c23-161">-ShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="39c23-161">-ShellCustomizer</span></span>
<span data-ttu-id="39c23-162">Führt ein Shell-Skript während der Anpassungsphase (Linux) aus.</span><span class="sxs-lookup"><span data-stu-id="39c23-162">Runs a shell script during the customization phase (Linux).</span></span>
<span data-ttu-id="39c23-163">Entspricht Packer Shell Provisioner.</span><span class="sxs-lookup"><span data-stu-id="39c23-163">Corresponds to Packer shell provisioner.</span></span>
<span data-ttu-id="39c23-164">Genau eine von "scriptUri" oder "Inline" kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="39c23-164">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

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

### <span data-ttu-id="39c23-165">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="39c23-165">-SourceUri</span></span>
<span data-ttu-id="39c23-166">Der URI der Datei, die zum Anpassen des VM hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="39c23-166">The URI of the file to be uploaded for customizing the VM.</span></span>
<span data-ttu-id="39c23-167">Hierbei kann es sich um einen GitHub-Link, SAS-URI für Azure-Speicher usw. handeln.</span><span class="sxs-lookup"><span data-stu-id="39c23-167">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

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

### <span data-ttu-id="39c23-168">-UpdateLimit</span><span class="sxs-lookup"><span data-stu-id="39c23-168">-UpdateLimit</span></span>
<span data-ttu-id="39c23-169">Die maximale Anzahl von Updates, die gleichzeitig angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="39c23-169">Maximum number of updates to apply at a time.</span></span>
<span data-ttu-id="39c23-170">Geben Sie "0" aus, um den Standardwert (1000) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="39c23-170">Omit or specify 0 to use the default (1000).</span></span>

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

### <span data-ttu-id="39c23-171">-ValidExitCode</span><span class="sxs-lookup"><span data-stu-id="39c23-171">-ValidExitCode</span></span>
<span data-ttu-id="39c23-172">Gültige Exit-Codes für das PowerShell-Skript.</span><span class="sxs-lookup"><span data-stu-id="39c23-172">Valid exit codes for the PowerShell script.</span></span>
<span data-ttu-id="39c23-173">[Standard: 0].</span><span class="sxs-lookup"><span data-stu-id="39c23-173">[Default: 0].</span></span>

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

### <span data-ttu-id="39c23-174">-WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="39c23-174">-WindowsUpdateCustomizer</span></span>
<span data-ttu-id="39c23-175">Installiert Windows-Updates.</span><span class="sxs-lookup"><span data-stu-id="39c23-175">Installs Windows Updates.</span></span>
<span data-ttu-id="39c23-176">Entspricht Packer Windows Update Provisioner ( https://github.com/rgl/packer-provisioner-windows-update) .</span><span class="sxs-lookup"><span data-stu-id="39c23-176">Corresponds to Packer Windows Update Provisioner (https://github.com/rgl/packer-provisioner-windows-update).</span></span>

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

### <span data-ttu-id="39c23-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c23-177">CommonParameters</span></span>
<span data-ttu-id="39c23-178">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39c23-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c23-179">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39c23-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c23-180">Eingaben</span><span class="sxs-lookup"><span data-stu-id="39c23-180">INPUTS</span></span>

## <span data-ttu-id="39c23-181">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39c23-181">OUTPUTS</span></span>

### <span data-ttu-id="39c23-182">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. Api20200214. IImageTemplateCustomizer</span><span class="sxs-lookup"><span data-stu-id="39c23-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span></span>

## <span data-ttu-id="39c23-183">Notizen</span><span class="sxs-lookup"><span data-stu-id="39c23-183">NOTES</span></span>

<span data-ttu-id="39c23-184">Aliase</span><span class="sxs-lookup"><span data-stu-id="39c23-184">ALIASES</span></span>

## <span data-ttu-id="39c23-185">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="39c23-185">RELATED LINKS</span></span>

