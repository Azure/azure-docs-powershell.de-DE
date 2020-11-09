---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 3e67452a5d5e11fa4aa96d1b38b80a4284c21f00
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296277"
---
# New-AzImageBuilderCustomizerObject

## Synopsis
Beschreibt eine Einheit der Bildanpassung

## Syntax

### ShellCustomizer (Standard)
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### Filecustomizer
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### PowerShellCustomizer
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### RestartCustomizer
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### WindowsUpdateCustomizer
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## Beschreibung
Beschreibt eine Einheit der Bildanpassung

## Beispiele

### Beispiel 1: Erstellen eines Windows Update-Customizers
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

Mit diesem Befehl wird ein Windows Update-Customizer erstellt.

### Beispiel 2: Erstellen einer Datei Anpassung
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

Mit diesem Befehl wird ein Datei-Customizer erstellt.

### Beispiel 3: Erstellen eines PowerShell-Customizers
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

Mit diesem Befehl wird ein PowerShell-Customizer erstellt.

### Beispiel 4: Erstellen eines Neustart-Customizers
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

Mit diesem Befehl wird ein Neustart-Customizer erstellt.

### Beispiel 5: Erstellen eines Shell-Customizers
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

Mit diesem Befehl wird ein Shell-Customizer erstellt.

## Parameter

### -CustomizerName
Anzeige Name, um einen Kontext zu dem zu liefern, was dieser Anpassungs Schritt macht.

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

### -Ziel
Der absolute Pfad zu einer Datei (mit bereits erstellten geschachtelten Verzeichnisstrukturen), in der die Datei (von SourceUri) in den virtuellen Computer hochgeladen wird.

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

### -Filecustomizer
Lädt Dateien auf VMS (Linux, Windows) hoch.
Entspricht dem Packer-Datei Provisioner.

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

### -Filter
Array von Filtern, um Updates auszuwählen, die angewendet werden sollen.
Geben Sie das leere Array aus, um den Standardwert (kein Filter) zu verwenden.
Beispiele und eine detaillierte Beschreibung dieses Felds finden Sie im obigen Link.

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

### -Inline
Array von Shell-Befehlen, die ausgeführt werden sollen.

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

### -PowerShellCustomizer
Führt die angegebene PowerShell auf dem virtuellen Computer (Windows) aus.
Entspricht Packer PowerShell Provisioner.
Genau eine von "scriptUri" oder "Inline" kann angegeben werden.

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

### -RestartCheckCommand
Befehl zum Überprüfen, ob Restart erfolgreich war [Standard: ' '].

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

### -RestartCommand
Befehl zum Ausführen des Neustarts [Standard: ' Shutdown/r/f/t 0/c Packer restart ']

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

### -RestartCustomizer
Startet einen virtuellen Computer neu und wartet darauf, dass er wieder online geschaltet wird (Windows).
Entspricht Packer Windows – starten Sie Provisioner erneut.

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

### -RestartTimeout
Neustart-Timeout, angegeben als eine Zeichenfolge von Größe und Einheit, beispielsweise "5M" (5 Minuten) oder "2H" (2 Stunden) [Standard: ' 5M '].

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

### -RunElevated
Wenn angegeben, wird das PowerShell-Skript mit erhöhten Rechten ausgeführt.

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

### -ScriptUri
Der URI des Shell-Skripts, das für das Customizing ausgeführt werden soll.
Hierbei kann es sich um einen GitHub-Link, SAS-URI für Azure-Speicher usw. handeln.

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

### -SearchCriterion
Kriterien zum Durchsuchen von Updates
Geben Sie eine leere Zeichenfolge aus, um den Standardwert (alle durchsuchen) zu verwenden.
Beispiele und eine detaillierte Beschreibung dieses Felds finden Sie im obigen Link.

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

### -Sha256Checksum
SHA256-Prüfsumme des Shell-Skripts, das im Feld scriptUri bereitgestellt wird.

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

### -ShellCustomizer
Führt ein Shell-Skript während der Anpassungsphase (Linux) aus.
Entspricht Packer Shell Provisioner.
Genau eine von "scriptUri" oder "Inline" kann angegeben werden.

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

### -SourceUri
Der URI der Datei, die zum Anpassen des VM hochgeladen werden soll.
Hierbei kann es sich um einen GitHub-Link, SAS-URI für Azure-Speicher usw. handeln.

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

### -UpdateLimit
Die maximale Anzahl von Updates, die gleichzeitig angewendet werden sollen.
Geben Sie "0" aus, um den Standardwert (1000) zu verwenden.

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

### -ValidExitCode
Gültige Exit-Codes für das PowerShell-Skript.
[Standard: 0].

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

### -WindowsUpdateCustomizer
Installiert Windows-Updates.
Entspricht Packer Windows Update Provisioner ( https://github.com/rgl/packer-provisioner-windows-update) .

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. Api20200214. IImageTemplateCustomizer

## Notizen

Aliase

## Verwandte Links

