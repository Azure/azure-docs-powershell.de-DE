---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: b6052172ecca2821b1373d93a8de870969a6b4f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944416"
---
# Invoke-AzStorageSyncCompatibilityCheck

## SYNOPSIS
Sucht nach möglichen Kompatibilitätsproblemen zwischen Ihrem System und Azure File Sync.

## SYNTAX

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

## BESCHREIBUNG
Das **Cmdlet Invoke-AzStorageSyncCompatibilityCheck** sucht nach möglichen Kompatibilitätsproblemen zwischen Ihrem System und Azure File Sync. Bei einem lokalen oder Remotepfad führt er eine Reihe von Überprüfungen für das System und den Dateinamen aus und gibt dann alle gefundenen Kompatibilitätsprobleme zurück.
Systemüberprüfungen:
- Betriebssystemkompatibilität Dateinamespace überprüft:
- Nicht unterstützte Zeichen
- Maximale Dateigröße
- Maximale Pfadlänge
- Maximale Dateilänge
- Maximale Datasetgröße
- Maximale Verzeichnistiefe

## BEISPIELE

### Beispiel 1
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

Mit diesem Befehl wird die Kompatibilität des Systems sowie von Dateien und Ordnern in C:\DATA überprüft.

### Beispiel 2
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

Dieser Befehl überprüft die Kompatibilität von Dateien und Ordnern in C:\DATA, führt jedoch keine Systemkompatibilitätsprüfung durch.

### Beispiel 3
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

Mit diesem Befehl wird die Kompatibilität des Systems sowie von Dateien und Ordnern in C:\DATA überprüft und die Ergebnisse dann als #A0 in C:\results exportiert.

## PARAMETER

### -ComputerName
Der Computer, auf dem Sie diese Überprüfung durchführen.

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

### -Anmeldeinformationen
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
Legen Sie dieses Flag so ein, dass Dateinamespaceüberprüfungen übersprungen und nur Systemüberprüfungen durchzuführen sind.

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
Legen Sie dieses Kennzeichen so ein, dass Systemüberprüfungen übersprungen und nur Dateinamespaceüberprüfungen ausführen.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult

## NOTIZEN
* Schlüsselwörter: azure, Az, arm, resource, management, storagesync, filesync

## VERWANDTE LINKS
