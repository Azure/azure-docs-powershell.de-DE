---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 6f5edd934e7239c8d4bb5083e5b4881fff79f489
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665014"
---
# New-AzureRmApplicationGatewayFrontendIPConfig

## Synopsis
Erstellt eine Front-End-IP-Konfiguration für ein Anwendungsgateway.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### SetByResourceId
```
New-AzureRmApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzureRmApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **New-AzureRmApplicationGatewayFrontendIPConfig** wird ein Front-End-IP-Konfigurations für ein Azure Application Gateway erstellt.
Ein Anwendungsgateway unterstützt zwei Arten der Front-End-IP-Konfiguration: 

- Öffentliche IP-Adressen – private IP-Adressen mit internem Lastenausgleich (ILB).

Ein Anwendungsgateway kann höchstens eine öffentliche IP-Adresse und eine private IP-Adresse aufweisen.
Die öffentliche IP-Adresse und die private IP-Adresse sollten separat als Front-End-IP-Adressen hinzugefügt werden.

## Beispiele

### Beispiel 1: Erstellen einer Front-End-IP-Konfiguration mithilfe eines öffentlichen IP-Ressourcenobjekts
```
PS C:\>$PublicIP = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

Der erste Befehl erstellt ein öffentliches IP-Ressourcenobjekt und speichert es in der $PublicIP-Variablen.
Der zweite Befehl verwendet $PublicIP, um eine neue Front-End-IP-Konfiguration mit dem Namen FrontEndIP01 zu erstellen, und speichert Sie in der $Frontend-Variablen.

### Beispiel 2: Erstellen einer statischen privaten IP als Front-End-IP-Adresse
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $VNet-Variablen.
Der zweite Befehl ruft eine Subnetz-Konfiguration mit dem Namen Subnet01 mit $VNet aus dem ersten Befehl ab und speichert Sie in der $Subnet-Variablen.
Der dritte Befehl erstellt eine Front-End-IP-Konfiguration mit dem Namen FrontEndIP02 mit $Subnet aus dem zweiten Befehl und der privaten IP-Adresse 10.0.1.1 und speichert Sie dann in der $Frontend-Variablen.

### Beispiel 3: Erstellen einer dynamischen privaten IP-Adresse als Front-End-IP-Adresse
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $VNet-Variablen.
Der zweite Befehl ruft eine Subnetz-Konfiguration mit dem Namen Subnet01 mit $VNet aus dem ersten Befehl ab und speichert Sie in der $Subnet-Variablen.
Der dritte Befehl erstellt eine Front-End-IP-Konfiguration mit dem Namen FrontEndIP03 mit $Subnet aus dem zweiten Befehl und speichert Sie in der $Frontend-Variablen.

## Parameter

### -Name
Gibt den Namen der Front-End-IP-Konfiguration an, die von diesem Cmdlet erstellt wird.

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

### -PrivateIPAddress
Gibt die private IP-Adresse an, die dieses Cmdlet der Front-End-IP-Adresse des Anwendungs Gateways zuordnet.
Dies kann nur angegeben werden, wenn ein Subnetz angegeben ist.
Diese IP-Adresse wird statisch aus dem Subnetz zugewiesen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddress
Gibt das öffentliche IP-Adressen Objekt an, das dieses Cmdlet der Front-End-IP-Adresse des Anwendungs Gateways zuordnet.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddressId
Gibt die öffentliche IP-Adresse an, die dieses Cmdlet der Front-End-IP des Anwendungs Gateways zuordnet.

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

### -Subnetz
Gibt das Subnet-Objekt an, das dieses Cmdlet der Front-End-IP-Adresse des Anwendungs Gateways zuordnet.
Wenn Sie diesen Parameter angeben, bedeutet dies, dass das Gateway eine private IP-Adresse verwendet.
Wenn der *PrivateIPAddresss* -Parameter angegeben wird, sollte er zu dem durch diesen Parameter angegebenen Subnetz gehören.
Wenn *PrivateIPAddress* nicht angegeben ist, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungs Gateways übernommen.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subnet-Nr
Gibt die Subnetz-ID an, die dieses Cmdlet der Front-End-IP-Konfiguration des Anwendungs Gateways zuordnet.
Wenn Sie den Parameter *Subnet* angeben, bedeutet dies, dass das Gateway eine private IP-Adresse verwendet.
Wenn der Parameter *PrivateIPAddress* angegeben wird, sollte er zu dem Subnetz gehören, das von *Subnetz* angegeben wird.
Wenn *PrivateIPAddress* nicht angegeben ist, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungs Gateways übernommen.

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

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration

## Notizen

## Verwandte Links

[Add-AzureRmApplicationGatewayFrontendIPConfig](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[Get-AzureRmApplicationGatewayFrontendIPConfig](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[Remove-AzureRmApplicationGatewayFrontendIPConfig](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[Satz-AzureRmApplicationGatewayFrontendIPConfig](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


