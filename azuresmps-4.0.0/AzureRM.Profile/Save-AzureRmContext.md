---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: f3afbd9b96de51f754dd87dfa42ed6f71e5b3577
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93474337"
---
# Save-AzureRmContext

## Synopsis
Speichert die aktuellen Authentifizierungsinformationen zur Verwendung in anderen PowerShell-Sitzungen.

## Syntax

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
```

## Beschreibung
Das Save-AzureRmContext-Cmdlet speichert die aktuellen Authentifizierungsinformationen zur Verwendung in anderen PowerShell-Sitzungen.

## Beispiele

### Beispiel 1: Speichern des Kontexts der aktuellen Sitzung
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

In diesem Beispiel wird der Azure-Kontext der aktuellen Sitzung in der angegebenen JSON-Datei gespeichert.

### Beispiel 2: Speichern eines bestimmten Kontexts
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

In diesem Beispiel wird der Azure-Kontext, der an das Cmdlet übergeben wird, in die angegebene JSON-Datei gespeichert.

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
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Gibt den Azure-Kontext an, aus dem dieses Cmdlet liest.
Wenn Sie keinen Kontext angeben, liest dieses Cmdlet aus dem lokalen Standardkontext.

```yaml
Type: AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
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

## Eingaben

### Microsoft. Azure. Commands. Common. Authentication. Models. AzureRMProfile

## Ausgaben

### Microsoft. Azure. Commands. profile. Models. PSAzureProfile

## Notizen

## Verwandte Links

