---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: 7b8e770a37b7f196878d1650f20d08ee382f6008
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661501"
---
# Publish-AzVMDscConfiguration

## Synopsis
Lädt ein DSC-Skript in einen Azure BLOB-Speicher hoch.

## Syntax

### UploadArchive (Standard)
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Createarchiv
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **Publish-AzVMDscConfiguration** " wird ein gewünschtes Status-Konfigurations (DSC)-Skript in einen Azure BLOB-Speicher hochgeladen, das später auf Azure Virtual Machines mithilfe des Set-AzVMDscExtension-Cmdlets angewendet werden kann.

## Beispiele

### Beispiel 1: Erstellen eines ZIP-Pakets und Hochladen in den Azure-Speicher
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

Mit diesem Befehl wird ein ZIP-Paket für das angegebene Skript und alle abhängigen Ressourcenmodule erstellt und in den Azure-Speicher hochgeladen.

### Beispiel 2: Erstellen eines ZIP-Pakets und speichern in einer lokalen Datei
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

Mit diesem Befehl wird ein ZIP-Paket für das angegebene Skript und alle abhängigen Ressourcenmodule erstellt und in der lokalen Datei mit dem Namen .\MyConfiguration.ps1.zip gespeichert.

### Beispiel 3: Hinzufügen einer Konfiguration zum Archiv und anschließendes hochladen auf den Speicher
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

Dieser Befehl fügt dem Konfigurations Archiv die Konfiguration mit dem Namen Sample.ps1 hinzu, um auf Azure-Speicher hochzuladen und abhängige Ressourcenmodule zu überspringen.

### Beispiel 4: Hinzufügen von Konfigurations-und Konfigurationsdaten zum Archiv und anschließendes hochladen auf den Speicher
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

Dieser Befehl fügt dem Konfigurations Archiv Sample.ps1-und Konfigurationsdaten mit dem Namen SampleData.psd1 hinzu, um Sie in den Azure-Speicher hochzuladen.

### Beispiel 5: Hinzufügen von Konfiguration, Konfigurationsdaten und zusätzlichem Inhalt zum Archiv und anschließendes hochladen auf den Speicher
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

Mit diesem Befehl werden die Konfiguration Sample.ps1, Konfigurationsdaten SampleData.psd1 und zusätzlicher Inhalt zum Konfigurations Archiv hinzugefügt, um den Upload in den Azure-Speicher durch zustellen.

## Parameter

### -AdditionalPath
Gibt den Pfad einer Datei oder eines Verzeichnisses an, das in das Konfigurations Archiv aufgenommen werden soll.
Es wird zusammen mit der Konfiguration auf den virtuellen Computer heruntergeladen.

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
Gibt den Pfad einer psd1-Datei an, die die Daten für die Konfiguration angibt.
Dieser wird dem Konfigurations Archiv hinzugefügt und dann an die Konfigurationsfunktion übergeben.
Sie wird durch den Konfigurationsdaten Pfad überschrieben, der über das Set-AzVMDscExtension-Cmdlet bereitgestellt wird.

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
Bei der Datei kann es sich um eine Windows PowerShell-Skriptdatei (. ps1) oder um eine Windows PowerShell-Moduldatei (psm1) handeln.

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

### -Containername
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
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

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
Gibt den Pfad einer lokalen ZIP-Datei an, in die das Konfigurations Archiv geschrieben werden soll.
Wenn dieser Parameter verwendet wird, wird das Konfigurationsskript nicht in den Azure BLOB-Speicher hochgeladen.

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
Gibt an, dass dieses Cmdlet DSC-Ressourcenabhängigkeiten vom Konfigurations Archiv ausschließt.

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
Gibt den Namen des Azure-speicherkontos an, das zum Hochladen des Konfigurationsskripts in den Container verwendet wird, der durch den *Container* Name-Parameter angegeben wird.

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
Gibt das Suffix für den Speicher Endpunkt an.

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
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### System. String []

## Ausgaben

### System. String

## Notizen

## Verwandte Links

[Get-AzVMDscExtension](./Get-AzVMDscExtension.md)

[Remove-AzVMDscExtension](./Remove-AzVMDscExtension.md)

[Satz-AzVMDscExtension](./Set-AzVMDscExtension.md)


