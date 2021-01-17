---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459791"
---
# Get-AzPolicyMetadata

## SYNOPSIS
Ruft Richtlinienmetadatenressourcen ab

## SYNTAX

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzPolicyRemediation"** ruft alle Metadatenressourcen für Richtlinien oder eine bestimmte Metadatenressource für Richtlinien ab.

## BEISPIELE

### Beispiel 1: Alle Metadatenressourcen für Richtlinien erhalten
```powershell
PS C:\> Get-AzPolicyMetadata
```

Dieser Befehl ruft alle Metadatenressourcen für Richtlinien ab.

### Beispiel 2: Erhalten einer Sammlung von 10 Ressourcen für Richtlinienmetadaten
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

Dieser Befehl ruft eine Sammlung von 10 Ressourcen für Richtlinienmetadaten ab.

### Beispiel 3: Erhalten einer einzelnen Metadatenressource für Richtlinien mit dem Namen 'ACF1348'
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

Dieser Befehl ruft eine einzelne Metadatenressource für Richtlinien mit dem Namen 'ACF1348' ab.

## PARAMETERS

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -Name
Ressourcenname.

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

### -Top
Maximale Anzahl von Zurücksendungsressourcen für Richtlinienmetadaten.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
