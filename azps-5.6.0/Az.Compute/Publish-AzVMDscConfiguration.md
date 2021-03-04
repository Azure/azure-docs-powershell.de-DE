---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: a57ed6bb12a1357ebd8d9b4f090bd1d551f3c554
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937099"
---
# Publish-AzVMDscConfiguration

## SYNOPSIS
Lädt ein DSC-Skript in den Azure-Blobspeicher hoch.

## SYNTAX

### UploadArchive (Standard)
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateArchive
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Publish-AzVMDscConfiguration** lädt ein Dsc-Skript (Desired State Configuration) in azure blob storage hoch, das später mithilfe des Set-AzVMDscExtension-Cmdlets auf virtuelle Azure-Computer angewendet werden kann.

## BEISPIELE

### Beispiel 1: Erstellen eines ZIP-Pakets, um es in den Azure-Speicher hochzuladen
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

Mit diesem Befehl wird ein ZIP-Paket für das angegebene Skript und alle abhängigen Ressourcenmodule erstellt und in den Azure-Speicher hochgeladen.

### Beispiel 2: Erstellen eines ZIP-Pakets und Speichern in einer lokalen Datei
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

Mit diesem Befehl wird ein ZIP-Paket für das angegebene Skript und alle abhängigen Ressourcenmodule erstellt und in der lokalen Datei mit dem Namen .\MyConfiguration.ps1.zip.

### Beispiel 3: Hinzufügen einer Konfiguration zum Archiv und Hochladen in den Speicher
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

Mit diesem Befehl wird die Konfiguration Sample.ps1 dem Konfigurationsarchiv zum Hochladen in den Azure-Speicher und abhängige Ressourcenmodule übersprungen.

### Beispiel 4: Hinzufügen von Konfigurations- und Konfigurationsdaten zum Archiv und anschließendes Hochladen in den Speicher
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

Mit diesem Befehl werden dem Konfigurationsarchiv Sample.ps1 Konfigurationsdaten SampleData.psd1 zum Hochladen in den Azure-Speicher hinzufügt.

### Beispiel 5: Hinzufügen von Konfigurations-, Konfigurationsdaten und zusätzlichen Inhalten zum Archiv und anschließendes Hochladen in den Speicher
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

Mit diesem Befehl werden konfiguration namens Sample.ps1, Konfigurationsdaten SampleData.psd1 und zusätzliche Inhalte zum Konfigurationsarchiv zum Hochladen in den Azure-Speicher addiert.

## PARAMETER

### -AdditionalPath
Gibt den Pfad einer Datei oder eines Verzeichnisses an, der in das Konfigurationsarchiv ein-/ausg.
Sie wird zusammen mit der Konfiguration auf den virtuellen Computer heruntergeladen.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationDataPath
Gibt den Pfad einer PSD1-Datei an, der die Daten für die Konfiguration angibt.
Dies wird dem Konfigurationsarchiv hinzugefügt und dann an die Konfigurationsfunktion übergeben.
Sie wird vom Konfigurationsdatenpfad überschrieben, der über das cmdlet Set-AzVMDscExtension wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationPath
Gibt den Pfad einer Datei an, die eine oder mehrere Konfigurationen enthält.
Bei der Datei kann es sich Windows PowerShell -Skriptdatei (PS1) oder Windows PowerShell -Moduldatei (PSM1) um eine datei.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ContainerName
Gibt den Namen des Azure-Speichercontainers an, in den die Konfiguration hochgeladen wird.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Erzwingen
Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.

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

### -OutputArchivePath
Gibt den Pfad einer lokalen ZIP-Datei an, in die das Konfigurationsarchiv geschrieben werden soll.
Wenn dieser Parameter verwendet wird, wird das Konfigurationsskript nicht in den Azure-Blobspeicher hochgeladen.

```yaml
Type: System.String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipDependencyDetection
Gibt an, dass dieses Cmdlet DSC-Ressourcenabhängigkeiten aus dem Konfigurationsarchiv ausschließt.

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

### -StorageAccountName
Gibt den Namen des Azure-Speicherkontos an, der zum Hochladen des Konfigurationsskripts in den Container verwendet wird, der vom *Parameter ContainerName angegeben* wird.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEndpointSuffix
Gibt das Suffix für den Speicherendpunkt an.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

### System.String[]

## AUSGABEN

### System.String

## NOTIZEN

## VERWANDTE LINKS

[Get-AzVMDscExtension](./Get-AzVMDscExtension.md)

[Remove-AzVMDscExtension](./Remove-AzVMDscExtension.md)

[Set-AzVMDscExtension](./Set-AzVMDscExtension.md)


