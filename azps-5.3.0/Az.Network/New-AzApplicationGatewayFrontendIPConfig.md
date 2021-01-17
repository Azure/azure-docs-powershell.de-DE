---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: c1c2f9fc3cbe528687f0a276c1b5feed3bbdb4b9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385565"
---
# New-AzApplicationGatewayFrontendIPConfig

## SYNOPSIS
Erstellt eine Front-End-IP-Konfiguration für ein Anwendungsgateway.

## SYNTAX

### SetByResourceId
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-PrivateLinkConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzApplicationGatewayFrontendIPConfig"** erstellt eine Front-End-IP-Konfiguration für ein Azure-Anwendungsgateway.
Ein Anwendungsgateway unterstützt zwei Arten von Front-End-IP-Konfigurationen: 
- Öffentliche IP-Adressen – Private IP-Adressen mit internem Lastenausgleich (ILB).
 Ein Anwendungsgateway kann mindestens eine öffentliche und eine private IP-Adresse haben.
Die öffentliche und die private IP-Adresse sollten separat als Front-End-IP-Adressen hinzugefügt werden.

## BEISPIELE

### Beispiel 1: Erstellen einer Front-End-IP-Konfiguration mit einem öffentlichen IP-Ressourcenobjekt
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

Der erste Befehl erstellt ein öffentliches IP-Ressourcenobjekt und speichert es in der $PublicIP Variable.
Der zweite Befehl verwendet $PublicIP zum Erstellen einer neuen Front-End-IP-Konfiguration namens FrontEndIP01 und speichert sie in der $FrontEnd Variable.

### Beispiel 2: Erstellen einer statischen privaten IP als Front-End-IP-Adresse
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

Der erste Befehl ruft ein virtuelles Netzwerk namens VNet01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $VNet Variable.
Der zweite Befehl ruft eine Subnetzkonfiguration namens Subnetz01 mit $VNet des ersten Befehls ab und speichert ihn in der $Subnet Variable.
Der dritte Befehl erstellt eine Front-End-IP-Konfiguration namens FrontEndIP02 mithilfe von $Subnet aus dem zweiten Befehl und der privaten IP-Adresse 10.0.1.1 und speichert sie dann in der $FrontEnd-Variable.

### Beispiel 3: Erstellen einer dynamischen privaten IP als Front-End-IP-Adresse
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

Der erste Befehl ruft ein virtuelles Netzwerk namens VNet01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $VNet Variable.
Der zweite Befehl ruft eine Subnetzkonfiguration namens Subnetz01 mit $VNet des ersten Befehls ab und speichert ihn in der $Subnet Variable.
Der dritte Befehl erstellt mithilfe von $Subnet des zweiten Befehls eine Front-End-IP-Konfiguration namens FrontEndIP03 und speichert sie in der $FrontEnd Variable.

## PARAMETERS

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Front-End-IP-Konfiguration an, die von diesem Cmdlet erstellt wird.

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

### -PrivateIPAddress
Gibt die private IP-Adresse an, die dieses Cmdlet der Front-End-IP-Adresse des Anwendungsgateways zugibt.
Dies kann nur angegeben werden, wenn ein Subnetz angegeben ist.
Diese IP wird statisch aus dem Subnetz zugewiesen.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateLinkConfiguration
PrivateLinkConfiguration

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateLinkConfigurationId
PrivateLinkConfigurationId

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

### -PublicIPAddress
Gibt das öffentliche IP-Adressobjekt an, das dieses Cmdlet der Front-End-IP-Adresse des Anwendungsgateways zugibt.

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddressId
Gibt die öffentliche IP-Adress-ID an, die dieses Cmdlet der Front-End-IP des Anwendungsgateways zugibt.

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

### -Subnet
Gibt das Subnetzobjekt an, das dieses Cmdlet der Front-End-IP-Adresse des Anwendungsgateways zugibt.
Wenn Sie diesen Parameter angeben, bedeutet dies, dass das Gateway eine private IP-Adresse verwendet.
Wenn der *Parameter "PrivateIPAddress"* angegeben wird, sollte er zu dem subnetz gehören, das durch diesen Parameter angegeben ist.
Wenn *"PrivateIPAddress"* nicht angegeben wird, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungsgateways aufgenommen.

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetId
Gibt die Subnetz-ID an, die dieses Cmdlet der Front-End-IP-Konfiguration des Anwendungsgateways zugibt.
Wenn Sie den Parameter *"Subnet"* angeben, bedeutet dies, dass das Gateway eine private IP-Adresse verwendet.
Wenn der *Parameter "PrivateIPAddress"* angegeben ist, sollte er zu dem Subnetz gehören, das durch Subnetz *angegeben ist.*
Wenn *"PrivateIPAddress"* nicht angegeben wird, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungsgateways aufgenommen.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Add-AzApplicationGatewayFrontendIPConfig](./Add-AzApplicationGatewayFrontendIPConfig.md)

[Get-AzApplicationGatewayFrontendIPConfig](./Get-AzApplicationGatewayFrontendIPConfig.md)

[Remove-AzApplicationGatewayFrontendIPConfig](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[Set-AzApplicationGatewayFrontendIPConfig](./Set-AzApplicationGatewayFrontendIPConfig.md)


