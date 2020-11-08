---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: 7cb3f6d015f95ba6a72066714647eb7a0551398b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009712"
---
# Get-AzApplicationGatewayAvailableWafRuleSet

## Synopsis
Ruft alle verfügbaren Webanwendungs-Firewallregel-Regelsätze ab.

## Syntax

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzApplicationGatewayAvailableWafRuleSet** " ruft alle verfügbaren Firewall-Regelsätze für Webanwendungen ab.

## Beispiele

### Beispiel 1
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

Diese Befehle gibt alle verfügbaren Firewall-Regelsätze für Webanwendungen zurück.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult

## Notizen
**List-AzApplicationGatewayAvailableWafRuleSets** ist ein Alias für das Cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** .

## Verwandte Links
