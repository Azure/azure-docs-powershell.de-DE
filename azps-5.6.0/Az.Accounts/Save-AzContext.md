---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: f73ca19ffa2c68599a5244d41b39d90ebbd2835a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930443"
---
# Save-AzContext

## SYNOPSIS
Speichert die aktuellen Authentifizierungsinformationen für die Verwendung in anderen PowerShell-Sitzungen.

## SYNTAX

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das Save-AzContext-Cmdlet speichert die aktuellen Authentifizierungsinformationen für die Verwendung in anderen PowerShell-Sitzungen.

## BEISPIELE

### Beispiel 1: Speichern des Kontexts der aktuellen Sitzung
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

In diesem Beispiel wird der Azure-Kontext der aktuellen Sitzung in der bereitgestellten JSON-Datei gespeichert.

### Beispiel 2: Speichern eines bestimmten Kontexts
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

In diesem Beispiel wird der Azure-Kontext gespeichert, der an das Cmdlet an die bereitgestellte JSON-Datei übergeben wird.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Überschreiben der angegebenen Datei, wenn sie vorhanden ist

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
Gibt den Pfad der Datei an, in der Authentifizierungsinformationen gespeichert werden.

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
Gibt den Azure-Kontext an, aus dem dieses Cmdlet gelesen wird.
Wenn Sie keinen Kontext angeben, liest dieses Cmdlet aus dem lokalen Standardkontext vor.

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
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile

## AUSGABEN

### Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile

## NOTIZEN

## VERWANDTE LINKS
