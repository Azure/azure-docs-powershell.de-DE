---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: c36cb832034535f13cbcb49805531c64ee906c60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172772"
---
# New-AzApplicationGatewayPathRuleConfig

## SYNOPSIS
Erstellt eine Anwendungsgatewaypfadregel.

## SYNTAX

### SetByResourceId
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzApplicationGatewayPathRuleConfig"** erstellt eine Anwendungsgatewaypfadregel.
Von diesem Cmdlet erstellte Regeln können einer Sammlung von Konfigurationseinstellungen für die URL-Pfadzuordnung hinzugefügt und dann einem Gateway zugewiesen werden.
Die Konfigurationseinstellungen der Pfadzuordnung werden beim Lastenausgleich des Anwendungsgateways verwendet.

## BEISPIELE

### Beispiel 1
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

Diese Befehle erstellen eine neue Regel für den Anwendungsgatewaypfad und verwenden dann das **Cmdlet "Add-AzApplicationGatewayUrlPathMapConfig",** um die Regel einem Anwendungsgateway zuzuordnen.
Dazu erstellt der erste Befehl einen Objektverweis auf das Gateway "ContosoApplicationGateway".
Dieser Objektverweis wird in einer Variablen mit dem Namen $Gateway.
Mit den nächsten beiden Befehlen werden ein Back-End-Adresspool und ein #A0 für #A1 erstellt. diese Objekte (in den Variablen $AddressPool und $HttpSettings gespeichert) benötigt, um ein Pfadregelobjekt zu erstellen.
Der vierte Befehl erstellt das Pfadregelobjekt und wird in einer Variablen namens "$PathRuleConfig.
Der fünfte Befehl verwendet **"Add-AzApplicationGatewayUrlPathMapConfig",** um die Konfigurationseinstellungen und die neue Pfadregel, die in diesen Einstellungen enthalten sind, zu "ContosoApplicationGateway" hinzuzufügen.

### Beispiel 2
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

Dieser Befehl erstellt eine Pfadregel mit dem Namen als "basis", Pfaden als "/base", Back-EndAddressPool als $AddressPool, Back-EndHttpSettings als $HttpSettings und FirewallPolicy als $firewallPolicy.ngs und der neuen Pfadregel, die in diesen Einstellungen zu ContosoApplicationGateway enthalten ist.

## PARAMETERS

### -BackendAddressPool
Gibt einen Objektverweis auf eine Sammlung von Einstellungen für den Back-End-Adresspool an, die den Konfigurationseinstellungen für Gatewaypfadregeln hinzugefügt werden sollen.
Sie können diesen Objektverweis mithilfe des #New-AzApplicationGatewayBackendAddressPool und einer ähnlichen Syntax erstellen: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`
Der vorherige Befehl fügt dem Adresspool zwei IP-Adressen (192.16.1.1 und 192.168.1.2) hinzu.
Beachten Sie, dass die IP-Adresse in Anführungszeichen eingeschlossen und durch Kommas getrennt ist.
Die resultierende Variable ($AddressPool) kann dann als Parameterwert für den Parameter *"DefaultBackendAddressPool" verwendet* werden.
Der Back-End-Adresspool stellt die IP-Adressen auf den Back-End-Servern dar.
Diese IP-Adressen sollten entweder zum Subnetz des virtuellen Netzwerks gehören oder öffentliche IP-Adressen sein.
Wenn Sie diesen Parameter verwenden, können Sie den Parameter *"DefaultBackendAddressPoolId"* nicht im gleichen Befehl verwenden.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Back-EndAddressPoolId
Gibt die ID eines vorhandenen Back-End-Adresspools an, der den Konfigurationseinstellungen der Gatewaypfadregel hinzugefügt werden kann.
Adresspool-IDs können mit dem cmdlet Get-AzApplicationGatewayBackendAddressPool zurückgegeben werden.
Nachdem Sie über die ID verfügen, können Sie den Parameter *"DefaultBackendAddressPoolId"* anstelle des Parameters *"DefaultBackendAddressPool"* verwenden.
Beispiel: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" Der Back-End-Adresspool stellt die IP-Adressen auf den Back-End-Servern dar.
Diese IP-Adressen sollten entweder zum Subnetz des virtuellen Netzwerks gehören oder öffentliche IP-Adressen sein.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Back-EndHttpSettings
Gibt einen Objektverweis auf eine Sammlung von HTTP-Back-End-Einstellungen an, die den Konfigurationseinstellungen der Gatewaypfadregel hinzugefügt werden sollen.
Sie können diesen Objektverweis mithilfe des Cmdlets New-AzApplicationGatewayBackendHttpSettings und einer ähnlichen Syntax erstellen: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" Die resultierende Variable, $HttpSettings kann dann als Parameterwert für den *Parameter "DefaultBackendAddressPool"* verwendet werden: -DefaultBackendHttpSettings $HttpSettings Die Back-End-HTTP-Einstellungen konfigurieren Eigenschaften wie Port, Protokoll und cookiebasierte Affinität für einen Back-End-Pool.
Wenn Sie diesen Parameter verwenden, können Sie den Parameter *"DefaultBackendHttpSettingsId"* nicht im gleichen Befehl verwenden.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Back-EndHttpSettingsId
Gibt die ID einer vorhandenen HTTP-Back-End-Einstellungssammlung an, die den Konfigurationseinstellungen der Gatewaypfadregel hinzugefügt werden kann.
HTTP-Einstellungs-IDs können mit dem cmdlet Get-AzApplicationGatewayBackendHttpSettings zurückgegeben werden.
Nachdem Sie über die ID verfügen, können Sie den Parameter *"DefaultBackendHttpSettingsId"* anstelle des Parameters *"DefaultBackendHttpSettings"* verwenden.
Beispiel: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backHttpSettingsCollection/ContosoHttpSettings" Die Back-End-HTTP-Einstellungen konfigurieren Eigenschaften wie Port, und cookiebasierte Affinität für einen Back-End-Pool.
Wenn Sie diesen Parameter verwenden, können Sie den Parameter *"DefaultBackendHttpSettings"* nicht im gleichen Befehl verwenden.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallPolicy
Gibt den Objektverweis auf eine Firewallrichtlinie der obersten Ebene an. Der Objektverweis kann mithilfe eines cmdlets New-AzApplicationGatewayWebApplicationFirewallPolicy werden.
$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" Auf eine Firewallrichtlinie, die mit dem obigen Befehlslet erstellt wurde, kann auf Pfadregelebene verwiesen werden. Der oben aufgeführte Befehl würde standardmäßige Richtlinieneinstellungen und verwaltete Regeln erstellen.
Statt der Standardwerte können Benutzer "PolicySettings", "ManagedRules" New-AzApplicationGatewayFirewallPolicySettings und New-AzApplicationGatewayFirewallPolicyManagedRules angeben.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallPolicyId
Gibt die ID einer vorhandenen Webanwendungsfirewallressource der obersten Ebene an.
Firewallrichtlinien-IDs können mit dem cmdlet Get-AzApplicationGatewayWebApplicationFirewallPolicy zurückgegeben werden. Nachdem wir die ID haben, können Sie den Parameter *"FirewallPolicyId"* anstelle des Parameters *"FirewallPolicy"* verwenden.
Beispiel: -FirewallPolicyId "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Gibt den Namen der Pfadregelkonfiguration an, die von diesem Cmdlet erstellt wird.

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

### -Paths
Gibt eine oder mehrere Regeln für den Anwendungsgatewaypfad an.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfiguration
Anwendungsgateway RedirectConfiguration

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfigurationId
ID des Anwendungsgateways RedirectConfiguration

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RewriteRuleSet
Application gateway RewriteRuleSet

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RewriteRuleSetId
ID des Anwendungsgateways "RewriteRuleSet"

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Add-AzApplicationGatewayUrlPathMapConfig](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[Get-AzApplicationGateway](./Get-AzApplicationGateway.md)

[Get-AzApplicationGatewayUrlPathMapConfig](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[New-AzApplicationGatewayBackendAddressPool](./New-AzApplicationGatewayBackendAddressPool.md)

[New-AzApplicationGatewayBackendHttpSetting](./New-AzApplicationGatewayBackendHttpSetting.md)

[New-AzApplicationGatewayPathRuleConfig](./New-AzApplicationGatewayPathRuleConfig.md)

[New-AzApplicationGatewayUrlPathMapConfig](./New-AzApplicationGatewayUrlPathMapConfig.md)

[Remove-AzApplicationGatewayUrlPathMapConfig](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[Set-AzApplicationGatewayUrlPathMapConfig](./Set-AzApplicationGatewayUrlPathMapConfig.md)


