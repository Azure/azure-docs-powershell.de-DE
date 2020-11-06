---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: 209986a25882415a68df86611d10559612a8ec04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500506"
---
# New-AzureRmApplicationGatewayPathRuleConfig

## Synopsis
Erstellt eine Anwendungsgateway-Pfadregel.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### SetByResourceId
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmApplicationGatewayPathRuleConfig** erstellt eine Pfadregel für das Anwendungsgateway.
Von diesem Cmdlet erstellte Regeln können einer Sammlung von URL-Pfad Zuordnungs Konfigurationseinstellungen hinzugefügt und dann einem Gateway zugewiesen werden.

Konfigurationseinstellungen für Pfad Zuordnungen werden im Lastenausgleich des Anwendungs Gateways verwendet.

## Beispiele

### Beispiel 1
```
PS C:\>$Gateway = Get-AzureRmApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzureRmApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

Mit diesen Befehlen wird eine neue Anwendungsgateway-Pfadregel erstellt, und dann wird das Cmdlet **Add-AzureRmApplicationGatewayUrlPathMapConfig** verwendet, um die Regel einem Anwendungsgateway zuzuweisen.
Dazu erstellt der erste Befehl einen Objektverweis auf das Gateway-ContosoApplicationGateway.
Dieser Objektverweis wird in einer Variablen mit dem Namen $Gateway gespeichert.

Mit den nächsten beiden Befehlen wird ein Back-End-Adresspool und ein Back-End-HTTP-Einstellungsobjekt erstellt. Diese Objekte (in den Variablen $AddressPool und $HttpSettings gespeichert) werden benötigt, um ein Pfadregel-Objekt zu erstellen.

Der vierte Befehl erstellt das Pfadregel-Objekt und wird in einer Variablen mit dem Namen $PathRuleConfig gespeichert.

Der fünfte Befehl verwendet **Add-AzureRmApplicationGatewayUrlPathMapConfig** , um die Konfigurationseinstellungen und die neue Pfadregel, die in diesen Einstellungen enthalten ist, ContosoApplicationGateway hinzuzufügen.

## Parameter

### -BackendAddressPool
Gibt einen Objektverweis auf eine Sammlung von Einstellungen des Back-End-Adresspools an, die den Konfigurationseinstellungen für Gateway-Pfadregeln hinzugefügt werden sollen.
Sie können diesen Objektverweis mithilfe des New-AzureRmApplicationGatewayBackendAddressPool-Cmdlets und der Syntax wie folgt erstellen:

`$AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

Der vorhergehende Befehl fügt dem Adresspool zwei IP-Adressen (192.16.1.1 und 192.168.1.2) hinzu.
Beachten Sie, dass die IP-Adresse in Anführungszeichen eingeschlossen und durch Kommas getrennt wird.

Die resultierende Variable $AddressPool kann dann als Parameterwert für den *DefaultBackendAddressPool* -Parameter verwendet werden.

Der Back-End-Adresspool stellt die IP-Adressen auf den Back-End-Servern dar.
Diese IP-Adressen sollten entweder zum Subnetz des virtuellen Netzwerks gehören oder öffentliche IP-Adressen sein.
Wenn Sie diesen Parameter verwenden, können Sie den *DefaultBackendAddressPoolId* -Parameter nicht im gleichen Befehl verwenden.

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendAddressPoolId
Gibt die ID eines vorhandenen Back-End-Adresspools an, der den Konfigurationseinstellungen für Gateway-Pfad Regel hinzugefügt werden kann.
Adresspool-IDs können mithilfe des Get-AzureRmApplicationGatewayBackendAddressPool-Cmdlets zurückgegeben werden.
Nachdem Sie die ID haben, können Sie den *DefaultBackendAddressPoolId* -Parameter anstelle des *DefaultBackendAddressPool* -Parameters verwenden.
Zum Beispiel:

-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"

Der Back-End-Adresspool stellt die IP-Adressen auf den Back-End-Servern dar.
Diese IP-Adressen sollten entweder zum Subnetz des virtuellen Netzwerks gehören oder öffentliche IP-Adressen sein.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendHttpSettings
Gibt einen Objektverweis auf eine Sammlung von Back-End-HTTP-Einstellungen an, die den Konfigurationseinstellungen für Gateway-Pfad Regel hinzugefügt werden sollen.
Sie können diesen Objektverweis mithilfe des New-AzureRmApplicationGatewayBackendHttpSettings-Cmdlets und der Syntax wie folgt erstellen:

$HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings-Name "ContosoHttpSetings"-Port 80-Protokoll "http"-CookieBasedAffinity "deaktiviert"

Die resultierende Variable $HttpSettings kann dann als Parameterwert für den *DefaultBackendAddressPool* -Parameter verwendet werden:

-DefaultBackendHttpSettings $HttpSettings

Die HTTP-Back-End-Einstellungen konfigurieren Eigenschaften wie Port-, Protokoll-und Cookie-basierter Affinität für einen Back-End-Pool.
Wenn Sie diesen Parameter verwenden, können Sie den *DefaultBackendHttpSettingsId* -Parameter nicht im gleichen Befehl verwenden.

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendHttpSettingsId
Gibt die ID einer vorhandenen Back-End-HTTP-Einstellungs Sammlung an, die den Konfigurationseinstellungen für Gateway-Pfad Regel hinzugefügt werden kann.
HTTP-Einstellungs-IDs können mithilfe des Get-AzureRmApplicationGatewayBackendHttpSettings-Cmdlets zurückgegeben werden.
Nachdem Sie die ID haben, können Sie den *DefaultBackendHttpSettingsId* -Parameter anstelle des *DefaultBackendHttpSettings* -Parameters verwenden.
Zum Beispiel:

-DefaultBackendSettings-ID "/Subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-RG/Providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"

Die HTTP-Back-End-Einstellungen konfigurieren Eigenschaften wie Port-, Protokoll-und Cookie-basierter Affinität für einen Back-End-Pool.
Wenn Sie diesen Parameter verwenden, können Sie den *DefaultBackendHttpSettings* -Parameter nicht im gleichen Befehl verwenden.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen der vom Cmdlet erstellten Pfad Regelkonfiguration an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pfade
Gibt mindestens eine Application Gateway Path-Regel an.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfiguration
Application Gateway RedirectConfiguration

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfigurationId
ID des Application Gateway RedirectConfiguration

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

###  
**New-AzureRmApplicationGatewayPathRuleConfig** akzeptiert keine Pipeline-Eingabe.

## Ausgaben

###  
**New-AzureRmApplicationGatewayPathRuleConfig** erstellt neue Instanzen des **Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPathRule** -Objekts.

## Notizen

## Verwandte Links

[Add-AzureRmApplicationGatewayUrlPathMapConfig](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[Get-AzureRmApplicationGateway](./Get-AzureRmApplicationGateway.md)

[Get-AzureRmApplicationGatewayUrlPathMapConfig](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[Neu – AzureRmApplicationGatewayBackendAddressPool](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[Neu – AzureRmApplicationGatewayBackendHttpSettings](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[Neu – AzureRmApplicationGatewayPathRuleConfig](./New-AzureRmApplicationGatewayPathRuleConfig.md)

[Neu – AzureRmApplicationGatewayUrlPathMapConfig](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[Remove-AzureRmApplicationGatewayUrlPathMapConfig](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[Satz-AzureRmApplicationGatewayUrlPathMapConfig](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


