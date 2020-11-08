---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176238"
---
# Get-AzPolicyMetadata

## Synopsis
Ruft Ressourcen für die Richtlinien Metadaten ab

## Syntax

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzPolicyRemediation** " ruft alle Richtlinien Metadaten-Ressourcen oder eine bestimmte Richtlinien Metadaten-Ressource ab.

## Beispiele

### Beispiel 1: Abrufen aller Ressourcen für die Richtlinien Metadaten
```powershell
PS C:\> Get-AzPolicyMetadata
```

Dieser Befehl ruft alle Richtlinien Metadaten-Ressourcen ab.

### Beispiel 2: Abrufen einer Sammlung von 10 Richtlinien Metadaten-Ressourcen
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

Dieser Befehl ruft eine Sammlung von 10 Richtlinien Metadaten-Ressourcen ab.

### Beispiel 3: Abrufen einer einzelnen Richtlinien Metadaten-Ressource mit dem Namen "ACF1348"
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

Dieser Befehl ruft eine einzelne Richtlinien Metadaten-Ressource mit dem Namen "ACF1348" ab.

## Parameter

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

### -Name
Ressourcenname

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
Die maximale Anzahl der zurückzugebenden Richtlinien Metadaten-Ressourcen.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. PolicyInsights. Models. PSPolicyMetadata

## Notizen

## Verwandte Links
