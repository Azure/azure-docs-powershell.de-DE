---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/publish-azurermvmdscconfiguration
schema: 2.0.0
ms.openlocfilehash: c9a778638a0ca86198079227cfa0021a96ac138b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850103"
---
# Publish-AzureRmVMDscConfiguration

## Synopsis
Lädt ein DSC-Skript in einen Azure BLOB-Speicher hoch.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### UploadArchive (Standard)
```
Publish-AzureRmVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Createarchiv
```
Publish-AzureRmVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **Publish-AzureRmVMDscConfiguration** " wird ein gewünschtes Status-Konfigurations (DSC)-Skript in einen Azure BLOB-Speicher hochgeladen, das später auf Azure Virtual Machines mithilfe des Set-AzureRmVMDscExtension-Cmdlets angewendet werden kann.

## Beispiele

### Beispiel 1: Erstellen eines ZIP-Pakets und Hochladen in den Azure-Speicher
```
PS C:\> Publish-AzureRmVMDscConfiguration ".\MyConfiguration.ps1"
```

Mit diesem Befehl wird ein ZIP-Paket für das angegebene Skript und alle abhängigen Ressourcenmodule erstellt und in den Azure-Speicher hochgeladen.

### Beispiel 2: Erstellen eines ZIP-Pakets und speichern in einer lokalen Datei
```
PS C:\> Publish-AzureRmVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

Mit diesem Befehl wird ein ZIP-Paket für das angegebene Skript und alle abhängigen Ressourcenmodule erstellt und in der lokalen Datei mit dem Namen .\MyConfiguration.ps1.zip gespeichert.

### Beispiel 3: Hinzufügen einer Konfiguration zum Archiv und anschließendes hochladen auf den Speicher
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

Dieser Befehl fügt dem Konfigurations Archiv die Konfiguration mit dem Namen Sample.ps1 hinzu, um auf Azure-Speicher hochzuladen und abhängige Ressourcenmodule zu überspringen.

### Beispiel 4: Hinzufügen von Konfigurations-und Konfigurationsdaten zum Archiv und anschließendes hochladen auf den Speicher
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

Dieser Befehl fügt dem Konfigurations Archiv Sample.ps1-und Konfigurationsdaten mit dem Namen SampleData.psd1 hinzu, um Sie in den Azure-Speicher hochzuladen.

### Beispiel 5: Hinzufügen von Konfiguration, Konfigurationsdaten und zusätzlichem Inhalt zum Archiv und anschließendes hochladen auf den Speicher
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

Mit diesem Befehl werden die Konfiguration Sample.ps1, Konfigurationsdaten SampleData.psd1 und zusätzlicher Inhalt zum Konfigurations Archiv hinzugefügt, um den Upload in den Azure-Speicher durch zustellen.

## Parameter

### -AdditionalPath
Gibt den Pfad einer Datei oder eines Verzeichnisses an, das in das Konfigurations Archiv aufgenommen werden soll.
Es wird zusammen mit der Konfiguration auf den virtuellen Computer heruntergeladen.

```yaml
Type: String[]
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
Sie wird durch den Konfigurationsdaten Pfad überschrieben, der über das Set-AzureRmVMDscExtension-Cmdlet bereitgestellt wird.

```yaml
Type: String
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
Type: String
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
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

```yaml
Type: SwitchParameter
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
Type: String
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
Type: String
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
Type: SwitchParameter
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
Type: String
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
Type: String
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
Type: SwitchParameter
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
Type: SwitchParameter
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

### Zeichenfolge
Der Parameter "ConfigurationPath" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.

## Ausgaben

### System. String

## Notizen

## Verwandte Links

[Get-AzureRmVMDscExtension](./Get-AzureRmVMDscExtension.md)

[Remove-AzureRmVMDscExtension](./Remove-AzureRmVMDscExtension.md)

[Satz-AzureRmVMDscExtension](./Set-AzureRmVMDscExtension.md)


