---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 6e45f0bc0eaab8316d0534e1f73a1543175e1144
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009161"
---
# Add-AzApplicationGatewayRewriteRuleSet

## Synopsis
Fügt einem Anwendungsgateway eine Regel Satz umschreiben hinzu.

## Syntax

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Add-AzApplicationGatewayRewriteRuleSet** " fügt einem Anwendungsgateway eine umschreibungs Regel hinzu.

## Beispiele

### Beispiel 1
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw-Variablen.
Mit dem zweiten Befehl wird die Regel für das erneute Schreiben zum Anwendungsgateway hinzugefügt.

## Parameter

### -ApplicationGateway
Die applicationGateway

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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
Der Name des RewriteRuleSet

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RewriteRule
Liste der Regeln zum Umschreiben

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## Notizen

## Verwandte Links

[Get-AzApplicationGatewayRewriteRuleSet](./Get-AzApplicationGatewayRewriteRuleSet.md)

[Neu – AzApplicationGatewayRewriteRuleSet](./New-AzApplicationGatewayRewriteRuleSet.md)

[Remove-AzApplicationGatewayRewriteRuleSet](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[Satz-AzApplicationGatewayRewriteRuleSet](./Set-AzApplicationGatewayRewriteRuleSet.md)

[Neu – AzApplicationGatewayRewriteRule](./New-AzApplicationGatewayRewriteRule.md)

[Neu – AzApplicationGatewayRewriteRuleActionSet](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[Neu – AzApplicationGatewayRewriteRuleHeaderConfiguration](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
