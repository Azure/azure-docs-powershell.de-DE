---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: ec568878c6ecd1d7f80caeb3a77c16c0838373a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662777"
---
# Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration

## Synopsis
Ruft die WAF-Konfiguration eines Anwendungs Gateways ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** " Ruft die WAF-Konfiguration (Web Application Firewall) eines Anwendungs Gateways ab.

## Beispiele

### Beispiel 1: Abrufen der Firewall-Konfiguration einer Application Gateway-Webanwendung
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es dann in der $AppGW-Variablen.

Der zweite Befehl ruft die Firewall-Konfiguration des Anwendungs Gateways in $AppGW ab und speichert Sie dann in $FirewallConfig.

## Parameter

### -ApplicationGateway
Gibt ein Application Gateway-Objekt an.
Sie können das Get-AzureRmApplicationGateway-Cmdlet verwenden, um ein Application Gateway-Objekt abzurufen.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### PSApplicationGateway
Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration

## Notizen

## Verwandte Links

[Get-AzureRmApplicationGateway](./Get-AzureRmApplicationGateway.md)

[Neu – AzureRmApplicationGatewayWebApplicationFirewallConfiguration](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[Satz-AzureRmApplicationGatewayWebApplicationFirewallConfiguration](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


