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
# Invoke-AzureRmStorageSyncCompatibilityCheck

## Synopsis
Überprüft mögliche Kompatibilitätsprobleme zwischen der System-und Azure-Dateisynchronisierung.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### PathBased (Standard)
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [-Quiet] [<CommonParameters>]
```

### ComputerNameBased
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [-Quiet] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Invoke-AzureRmStorageSyncCompatibilityCheck** überprüft potenzielle Kompatibilitätsprobleme zwischen der System-und Azure-Dateisynchronisierung. Bei einem lokalen oder Remotepfad wird eine Reihe von Validierungen für den System-und Datei Namespace durchgeführt und dann alle gefundenen Kompatibilitätsprobleme zurückgegeben.
System Prüfungen:
- System Kompatibilitätsdatei-Namespace überprüft:
- Nicht unterstützte Zeichen
- Maximale Dateigröße
- Maximale Länge des Pfads
- Maximale Dateilänge
- Maximale Datensatzgröße
- Maximale Verzeichnistiefe

## Beispiele

### Beispiel 1
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
```

Dieser Befehl überprüft die Kompatibilität des Systems und auch von Dateien und Ordnern in C:\data.

### Beispiel 2
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

Dieser Befehl überprüft die Kompatibilität von Dateien und Ordnern in C:\data, führt jedoch keine System Kompatibilitätsüberprüfung durch.

### Beispiel 3
```powershell
PS C:\> $errors = Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
PS C:\> $errors | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results
```

Dieser Befehl überprüft die Kompatibilität des Systems und auch von Dateien und Ordnern in C:\data und exportiert die Ergebnisse dann als CSV-Datei in C:\results.

## Parameter

### -Computername
Der Computer, auf dem Sie diese Prüfung durchführen.

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

### – Anmeldeinformationen
Ihre Anmeldeinformationen für die Freigabe, die Sie überprüfen.

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

### -Path
Der UNC-Pfad der Freigabe, die Sie überprüfen.

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

### – Ruhig
Unterdrückt das Schreiben des Ausgabe Berichts an die Konsole.

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

### -SkipNamespaceChecks
Setzen Sie dieses Flag, um Datei Namespace-Validierungen zu überspringen und nur System Validierungen durchzuführen.

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

### -SkipSystemChecks
Legen Sie dieses Flag so ein, dass System Validierungen übersprungen werden und nur Datei Namespace-Validierungen durchgeführt werden.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. StorageSync. Evaluation. Models. PSValidationResult

## Notizen
* Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, storagesync, FileSync

## Verwandte Links
