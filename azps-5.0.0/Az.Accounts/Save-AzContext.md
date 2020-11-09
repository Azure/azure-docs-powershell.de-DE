---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 2d3506fcf0968e58a71d81fbabe56f08428af761
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300027"
---
# Save-AzContext

## Synopsis
Speichert die aktuellen Authentifizierungsinformationen zur Verwendung in anderen PowerShell-Sitzungen.

## Syntax

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Save-AzContext-Cmdlet speichert die aktuellen Authentifizierungsinformationen zur Verwendung in anderen PowerShell-Sitzungen.

## Beispiele

### Beispiel 1: Speichern des Kontexts der aktuellen Sitzung
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

In diesem Beispiel wird der Azure-Kontext der aktuellen Sitzung in der angegebenen JSON-Datei gespeichert.

### Beispiel 2: Speichern eines bestimmten Kontexts
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

In diesem Beispiel wird der Azure-Kontext, der an das Cmdlet übergeben wird, in die angegebene JSON-Datei gespeichert.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements.

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
Überschreiben der angegebenen Datei, sofern vorhanden

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

### -Path
Gibt den Pfad der Datei an, in der Authentifizierungsinformationen gespeichert werden sollen.

```yaml
Type: System.String
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
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Common. Authentication. Models. AzureRmProfile

## Ausgaben

### Microsoft. Azure. Commands. profile. Models. Core. PSAzureProfile

## Notizen

## Verwandte Links
