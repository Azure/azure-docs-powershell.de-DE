---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06a78584437021df570bc5ff2b6ec19e332bffd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475205"
---
# Save-AzureRmProfile

## Synopsis
Speichert die aktuellen Authentifizierungsinformationen zur Verwendung in anderen PowerShell-Sitzungen.

## Syntax

```
Save-AzureRmProfile [[-Profile] <AzureRMProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Save-AzureRmProfile-Cmdlet speichert die aktuellen Authentifizierungsinformationen zur Verwendung in anderen PowerShell-Sitzungen.

## Beispiele

### Beispiel 1: Speichern des Profils der aktuellen Sitzung
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmProfile -Path C:\test.json
```

In diesem Beispiel wird das Azure-Profil der aktuellen Sitzung in der angegebenen JSON-Datei gespeichert.

### Beispiel 2: Speichern eines angegebenen Profils
```
PS C:\> Save-AzureRmProfile -Profile (Add-AzureRmAccount) -Path C:\test.json
```

In diesem Beispiel wird das Azure-Profil, das an das Cmdlet übergeben wird, in die angegebene JSON-Datei gespeichert.

## Parameter

### -Force
Überschreiben der angegebenen Datei, sofern vorhanden

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Gibt den Pfad der Datei an, in der Authentifizierungsinformationen gespeichert werden sollen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureRMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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

## Ausgaben

### PSAzureProfile

## Notizen

## Verwandte Links

[SELECT-AzureRMProfile]()

