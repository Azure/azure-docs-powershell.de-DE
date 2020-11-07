---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: b3c6b69b628c7461616a42ecbaaf37d017e06b46
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826919"
---
# Invoke-AzStorageSyncCompatibilityCheck

## Synopsis
Überprüft mögliche Kompatibilitätsprobleme zwischen der System-und Azure-Dateisynchronisierung.

## Syntax

### PathBased (Standard)
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### ComputerNameBased
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Invoke-AzStorageSyncCompatibilityCheck** überprüft potenzielle Kompatibilitätsprobleme zwischen der System-und Azure-Dateisynchronisierung. Bei einem lokalen oder Remotepfad wird eine Reihe von Validierungen für den System-und Datei Namespace durchgeführt und dann alle gefundenen Kompatibilitätsprobleme zurückgegeben.
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
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

Dieser Befehl überprüft die Kompatibilität des Systems und auch von Dateien und Ordnern in C:\data.

### Beispiel 2
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

Dieser Befehl überprüft die Kompatibilität von Dateien und Ordnern in C:\data, führt jedoch keine System Kompatibilitätsüberprüfung durch.

### Beispiel 3
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
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
* Schlüsselwörter: Azure, AZ, arm, Resource, Verwaltung, storagesync, FileSync

## Verwandte Links
