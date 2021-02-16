---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 3e67452a5d5e11fa4aa96d1b38b80a4284c21f00
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155577"
---
# <span data-ttu-id="326b8-101">New-AzImageBuilderCustomizerObject</span><span class="sxs-lookup"><span data-stu-id="326b8-101">New-AzImageBuilderCustomizerObject</span></span>

## <span data-ttu-id="326b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="326b8-102">SYNOPSIS</span></span>
<span data-ttu-id="326b8-103">Beschreibt eine Einheit der Bildanpassung</span><span class="sxs-lookup"><span data-stu-id="326b8-103">Describes a unit of image customization</span></span>

## <span data-ttu-id="326b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="326b8-104">SYNTAX</span></span>

### <span data-ttu-id="326b8-105">ShellCustomizer (Standard)</span><span class="sxs-lookup"><span data-stu-id="326b8-105">ShellCustomizer (Default)</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### <span data-ttu-id="326b8-106">FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="326b8-106">FileCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### <span data-ttu-id="326b8-107">PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="326b8-107">PowerShellCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### <span data-ttu-id="326b8-108">RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="326b8-108">RestartCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### <span data-ttu-id="326b8-109">WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="326b8-109">WindowsUpdateCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="326b8-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="326b8-110">DESCRIPTION</span></span>
<span data-ttu-id="326b8-111">Beschreibt eine Einheit der Bildanpassung</span><span class="sxs-lookup"><span data-stu-id="326b8-111">Describes a unit of image customization</span></span>

## <span data-ttu-id="326b8-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="326b8-112">EXAMPLES</span></span>

### <span data-ttu-id="326b8-113">Beispiel 1: Erstellen eines Windows Update Customizers</span><span class="sxs-lookup"><span data-stu-id="326b8-113">Example 1: Create a windows update customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

<span data-ttu-id="326b8-114">Mit diesem Befehl wird ein Windows Update Customizer erstellt.</span><span class="sxs-lookup"><span data-stu-id="326b8-114">This command creates a windows update customizer.</span></span>

### <span data-ttu-id="326b8-115">Beispiel 2: Erstellen eines Datei-Customizers</span><span class="sxs-lookup"><span data-stu-id="326b8-115">Example 2: Create a file customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

<span data-ttu-id="326b8-116">Mit diesem Befehl wird eine Datei anpasst.</span><span class="sxs-lookup"><span data-stu-id="326b8-116">This command creates a file customizer.</span></span>

### <span data-ttu-id="326b8-117">Beispiel 3: Erstellen eines Powershell-Customizers</span><span class="sxs-lookup"><span data-stu-id="326b8-117">Example 3: Create a powershell customizer</span></span>
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

<span data-ttu-id="326b8-118">Dieser Befehl erstellt einen Powershell-Customizer.</span><span class="sxs-lookup"><span data-stu-id="326b8-118">This command creates a powershell customizer.</span></span>

### <span data-ttu-id="326b8-119">Beispiel 4: Erstellen eines Neustart-Customizers</span><span class="sxs-lookup"><span data-stu-id="326b8-119">Example 4: Create a restart customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

<span data-ttu-id="326b8-120">Dieser Befehl erstellt einen Neustart-Customizer.</span><span class="sxs-lookup"><span data-stu-id="326b8-120">This command creates a restart customizer.</span></span>

### <span data-ttu-id="326b8-121">Beispiel 5: Erstellen eines Shell-Customizers</span><span class="sxs-lookup"><span data-stu-id="326b8-121">Example 5: Create a shell customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

<span data-ttu-id="326b8-122">Dieser Befehl erstellt einen Shell-Customizer.</span><span class="sxs-lookup"><span data-stu-id="326b8-122">This command creates a shell customizer.</span></span>

## <span data-ttu-id="326b8-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="326b8-123">PARAMETERS</span></span>

### <span data-ttu-id="326b8-124">-CustomizerName</span><span class="sxs-lookup"><span data-stu-id="326b8-124">-CustomizerName</span></span>
<span data-ttu-id="326b8-125">Anzeigename, der Kontext zu den Durchschritten dieses Anpassungsschritts bietet.</span><span class="sxs-lookup"><span data-stu-id="326b8-125">Friendly Name to provide context on what this customization step does.</span></span>

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

### <span data-ttu-id="326b8-126">-Destination</span><span class="sxs-lookup"><span data-stu-id="326b8-126">-Destination</span></span>
<span data-ttu-id="326b8-127">Der absolute Pfad zu einer Datei (mit bereits erstellten geschachtelten Verzeichnisstrukturen), in die die Datei (from sourceUri) auf die VM hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="326b8-127">The absolute path to a file (with nested directory structures already created) where the file (from sourceUri) will be uploaded to in the VM.</span></span>

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

### <span data-ttu-id="326b8-128">-FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="326b8-128">-FileCustomizer</span></span>
<span data-ttu-id="326b8-129">Lädt Dateien in VMs (Linux, Windows) hoch.</span><span class="sxs-lookup"><span data-stu-id="326b8-129">Uploads files to VMs (Linux, Windows).</span></span>
<span data-ttu-id="326b8-130">Entspricht der Packer-Dateibereitstellung.</span><span class="sxs-lookup"><span data-stu-id="326b8-130">Corresponds to Packer file provisioner.</span></span>

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

### <span data-ttu-id="326b8-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="326b8-131">-Filter</span></span>
<span data-ttu-id="326b8-132">Array von Filtern zum Auswählen anzuwendener Updates.</span><span class="sxs-lookup"><span data-stu-id="326b8-132">Array of filters to select updates to apply.</span></span>
<span data-ttu-id="326b8-133">Lassen Sie ein leeres Array weg, oder geben Sie es an, um den Standardwert zu verwenden (kein Filter).</span><span class="sxs-lookup"><span data-stu-id="326b8-133">Omit or specify empty array to use the default (no filter).</span></span>
<span data-ttu-id="326b8-134">Beispiele und eine detaillierte Beschreibung dieses Felds finden Sie oben unter dem Link.</span><span class="sxs-lookup"><span data-stu-id="326b8-134">Refer to above link for examples and detailed description of this field.</span></span>

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

### <span data-ttu-id="326b8-135">-Inline</span><span class="sxs-lookup"><span data-stu-id="326b8-135">-Inline</span></span>
<span data-ttu-id="326b8-136">Array der auszuführende Shellbefehle.</span><span class="sxs-lookup"><span data-stu-id="326b8-136">Array of shell commands to execute.</span></span>

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

### <span data-ttu-id="326b8-137">-PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="326b8-137">-PowerShellCustomizer</span></span>
<span data-ttu-id="326b8-138">Führt die angegebene PowerShell auf der VM (Windows) aus.</span><span class="sxs-lookup"><span data-stu-id="326b8-138">Runs the specified PowerShell on the VM (Windows).</span></span>
<span data-ttu-id="326b8-139">Entspricht dem Packer Powershell-Provisioner.</span><span class="sxs-lookup"><span data-stu-id="326b8-139">Corresponds to Packer powershell provisioner.</span></span>
<span data-ttu-id="326b8-140">Es kann genau ein "scriptUri"- oder "inline"-Wert angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="326b8-140">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

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

### <span data-ttu-id="326b8-141">-RestartCheckCommand</span><span class="sxs-lookup"><span data-stu-id="326b8-141">-RestartCheckCommand</span></span>
<span data-ttu-id="326b8-142">Befehl zum Überprüfen, ob der Neustart erfolgreich war [Standard: ''].</span><span class="sxs-lookup"><span data-stu-id="326b8-142">Command to check if restart succeeded [Default: ''].</span></span>

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

### <span data-ttu-id="326b8-143">-RestartCommand</span><span class="sxs-lookup"><span data-stu-id="326b8-143">-RestartCommand</span></span>
<span data-ttu-id="326b8-144">Befehl zum Ausführen des Neustarts [Standard: 'shutdown /r /f /t 0 /c packer restart']</span><span class="sxs-lookup"><span data-stu-id="326b8-144">Command to execute the restart [Default: 'shutdown /r /f /t 0 /c packer restart']</span></span>

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

### <span data-ttu-id="326b8-145">-RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="326b8-145">-RestartCustomizer</span></span>
<span data-ttu-id="326b8-146">Startet eine VM neu und wartet darauf, dass sie wieder online ist (Windows).</span><span class="sxs-lookup"><span data-stu-id="326b8-146">Reboots a VM and waits for it to come back online (Windows).</span></span>
<span data-ttu-id="326b8-147">Entspricht dem Packer-Windows-Neustart-Provisioner.</span><span class="sxs-lookup"><span data-stu-id="326b8-147">Corresponds to Packer windows-restart provisioner.</span></span>

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

### <span data-ttu-id="326b8-148">-RestartTimeout</span><span class="sxs-lookup"><span data-stu-id="326b8-148">-RestartTimeout</span></span>
<span data-ttu-id="326b8-149">Neustarttimeout, das als Zeichenfolge mit Größe und Einheit angegeben ist, z. B. '5m' (5 Minuten) oder '2 Std. (2 Stunden) [Standard: '5m'].</span><span class="sxs-lookup"><span data-stu-id="326b8-149">Restart timeout specified as a string of magnitude and unit, e.g. '5m' (5 minutes) or '2h' (2 hours) [Default: '5m'].</span></span>

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

### <span data-ttu-id="326b8-150">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="326b8-150">-RunElevated</span></span>
<span data-ttu-id="326b8-151">Falls angegeben, wird das PowerShell-Skript mit erhöhten Rechten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="326b8-151">If specified, the PowerShell script will be run with elevated privileges.</span></span>

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

### <span data-ttu-id="326b8-152">-ScriptUri</span><span class="sxs-lookup"><span data-stu-id="326b8-152">-ScriptUri</span></span>
<span data-ttu-id="326b8-153">URI des Shellskripts, das zum Anpassen ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="326b8-153">URI of the shell script to be run for customizing.</span></span>
<span data-ttu-id="326b8-154">Es kann sich um einen Github-Link, einen SAS-URI für Azure Storage usw.</span><span class="sxs-lookup"><span data-stu-id="326b8-154">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

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

### <span data-ttu-id="326b8-155">-SearchCrikritischen</span><span class="sxs-lookup"><span data-stu-id="326b8-155">-SearchCriterion</span></span>
<span data-ttu-id="326b8-156">Kriterien für die Suche nach Updates.</span><span class="sxs-lookup"><span data-stu-id="326b8-156">Criteria to search updates.</span></span>
<span data-ttu-id="326b8-157">Lassen Sie eine leere Zeichenfolge weg, oder geben Sie sie an, um die Standardzeichenfolge zu verwenden (alle durchsuchen).</span><span class="sxs-lookup"><span data-stu-id="326b8-157">Omit or specify empty string to use the default (search all).</span></span>
<span data-ttu-id="326b8-158">Beispiele und eine detaillierte Beschreibung dieses Felds finden Sie oben unter dem Link.</span><span class="sxs-lookup"><span data-stu-id="326b8-158">Refer to above link for examples and detailed description of this field.</span></span>

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

### <span data-ttu-id="326b8-159">-Sha256Checksum</span><span class="sxs-lookup"><span data-stu-id="326b8-159">-Sha256Checksum</span></span>
<span data-ttu-id="326b8-160">SHA256-Prüfsumme des Shellskripts, das im Feld "scriptUri" bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="326b8-160">SHA256 checksum of the shell script provided in the scriptUri field.</span></span>

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

### <span data-ttu-id="326b8-161">-ShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="326b8-161">-ShellCustomizer</span></span>
<span data-ttu-id="326b8-162">Führt während der Anpassungsphase (Linux) ein Shellskript aus.</span><span class="sxs-lookup"><span data-stu-id="326b8-162">Runs a shell script during the customization phase (Linux).</span></span>
<span data-ttu-id="326b8-163">Entspricht der Packer-Shellbereitstellung.</span><span class="sxs-lookup"><span data-stu-id="326b8-163">Corresponds to Packer shell provisioner.</span></span>
<span data-ttu-id="326b8-164">Es kann genau ein "scriptUri"- oder "inline"-Wert angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="326b8-164">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

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

### <span data-ttu-id="326b8-165">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="326b8-165">-SourceUri</span></span>
<span data-ttu-id="326b8-166">Der URI der Datei, die hochgeladen werden soll, um die VM anpassen zu können.</span><span class="sxs-lookup"><span data-stu-id="326b8-166">The URI of the file to be uploaded for customizing the VM.</span></span>
<span data-ttu-id="326b8-167">Es kann sich um einen Github-Link, einen SAS-URI für Azure Storage usw.</span><span class="sxs-lookup"><span data-stu-id="326b8-167">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

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

### <span data-ttu-id="326b8-168">-UpdateLimit</span><span class="sxs-lookup"><span data-stu-id="326b8-168">-UpdateLimit</span></span>
<span data-ttu-id="326b8-169">Die maximale Anzahl von Updates, die gleichzeitig angewendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="326b8-169">Maximum number of updates to apply at a time.</span></span>
<span data-ttu-id="326b8-170">Geben Sie "0" aus, um den Standardwert (1000) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="326b8-170">Omit or specify 0 to use the default (1000).</span></span>

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

### <span data-ttu-id="326b8-171">-ValidExitCode</span><span class="sxs-lookup"><span data-stu-id="326b8-171">-ValidExitCode</span></span>
<span data-ttu-id="326b8-172">Gültige Exitcodes für das PowerShell-Skript.</span><span class="sxs-lookup"><span data-stu-id="326b8-172">Valid exit codes for the PowerShell script.</span></span>
<span data-ttu-id="326b8-173">[Standard: 0].</span><span class="sxs-lookup"><span data-stu-id="326b8-173">[Default: 0].</span></span>

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

### <span data-ttu-id="326b8-174">-WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="326b8-174">-WindowsUpdateCustomizer</span></span>
<span data-ttu-id="326b8-175">Windows Updates wird installiert.</span><span class="sxs-lookup"><span data-stu-id="326b8-175">Installs Windows Updates.</span></span>
<span data-ttu-id="326b8-176">Entspricht dem Packer Windows Update Provisioner ( https://github.com/rgl/packer-provisioner-windows-update) .</span><span class="sxs-lookup"><span data-stu-id="326b8-176">Corresponds to Packer Windows Update Provisioner (https://github.com/rgl/packer-provisioner-windows-update).</span></span>

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

### <span data-ttu-id="326b8-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="326b8-177">CommonParameters</span></span>
<span data-ttu-id="326b8-178">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="326b8-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="326b8-179">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="326b8-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="326b8-180">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="326b8-180">INPUTS</span></span>

## <span data-ttu-id="326b8-181">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="326b8-181">OUTPUTS</span></span>

### <span data-ttu-id="326b8-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span><span class="sxs-lookup"><span data-stu-id="326b8-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span></span>

## <span data-ttu-id="326b8-183">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="326b8-183">NOTES</span></span>

<span data-ttu-id="326b8-184">ALIASE</span><span class="sxs-lookup"><span data-stu-id="326b8-184">ALIASES</span></span>

## <span data-ttu-id="326b8-185">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="326b8-185">RELATED LINKS</span></span>

