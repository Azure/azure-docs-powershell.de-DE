---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 214f408a5120982a903ed0d0d934c44073c32df8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936168"
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
Das **Cmdlet New-AzApplicationGatewayFrontendIPConfig** erstellt eine Front-End-IP-Konfiguration für ein Azure-Anwendungsgateway.
Ein Anwendungsgateway unterstützt zwei Arten von Front-End-IP-Konfigurationen: 
- Öffentliche IP-Adressen – Private IP-Adressen mit internem Lastenausgleich (ILB).
 Ein Anwendungsgateway kann mindestens eine öffentliche IP-Adresse und eine private IP-Adresse haben.
Die öffentliche IP-Adresse und private IP-Adresse sollten separat als Front-End-IP-Adressen hinzugefügt werden.

## BEISPIELE

### Beispiel 1: Erstellen einer Front-End-IP-Konfiguration mit einem öffentlichen IP-Ressourcenobjekt
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

Mit dem ersten Befehl wird ein öffentliches IP-Ressourcenobjekt erstellt und in der $PublicIP gespeichert.
Der zweite Befehl verwendet $PublicIP zum Erstellen einer neuen Front-End-IP-Konfiguration namens FrontEndIP01 und speichert sie in der $FrontEnd Variablen.

### Beispiel 2: Erstellen einer statischen privaten IP als Front-End-IP-Adresse
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

Der erste Befehl ruft ein virtuelles Netzwerk namens VNet01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $VNet Variablen.
Der zweite Befehl ruft eine Subnetzkonfiguration namens Subnetz01 mit $VNet ersten Befehl ab und speichert sie in der $Subnet Variable.
Mit dem dritten Befehl wird eine Front-End-IP-Konfiguration namens FrontEndIP02 mithilfe von $Subnet aus dem zweiten Befehl und der privaten IP-Adresse 10.0.1.1 erstellt und dann in der variablen $FrontEnd gespeichert.

### Beispiel 3: Erstellen einer dynamischen privaten IP als Front-End-IP-Adresse
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

Der erste Befehl ruft ein virtuelles Netzwerk namens VNet01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $VNet Variablen.
Der zweite Befehl ruft eine Subnetzkonfiguration namens Subnetz01 mit $VNet ersten Befehl ab und speichert sie in der $Subnet Variable.
Der dritte Befehl erstellt eine Front-End-IP-Konfiguration mit dem Namen FrontEndIP03 mit $Subnet aus dem zweiten Befehl und speichert sie in der $FrontEnd Variable.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Gibt die private IP-Adresse an, die dieses Cmdlet der Front-End-IP-Adresse des Anwendungsgateways zurät.
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
Gibt das öffentliche IP-Adressobjekt an, das dieses Cmdlet mit der Front-End-IP-Adresse des Anwendungsgateways verknüpft.

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
Gibt die öffentliche IP-Adress-ID an, die dieses Cmdlet mit der Front-End-IP des Anwendungsgateways verknüpft.

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

### -Subnetz
Gibt das Subnetzobjekt an, das dieses Cmdlet mit der Front-End-IP-Adresse des Anwendungsgateways verknüpft.
Wenn Sie diesen Parameter angeben, bedeutet dies, dass das Gateway eine private IP-Adresse verwendet.
Wenn der *Parameter PrivateIPAddress* angegeben ist, sollte er zum Subnetz gehören, das durch diesen Parameter angegeben ist.
Wenn *PrivateIPAddress* nicht angegeben ist, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungsgateways erfasst.

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
Gibt die Subnetz-ID an, die dieses Cmdlet der Front-End-IP-Konfiguration des Anwendungsgateways zurät.
Wenn Sie den *Parameter Subnetz* angeben, bedeutet dies, dass das Gateway eine private IP-Adresse verwendet.
Wenn der *Parameter PrivateIPAddress* angegeben ist, sollte er zum Subnetz gehören, das von Subnetz *angegeben ist.*
Wenn *PrivateIPAddress* nicht angegeben ist, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungsgateways erfasst.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration

## NOTIZEN

## VERWANDTE LINKS

[Add-AzApplicationGatewayFrontendIPConfig](./Add-AzApplicationGatewayFrontendIPConfig.md)

[Get-AzApplicationGatewayFrontendIPConfig](./Get-AzApplicationGatewayFrontendIPConfig.md)

[Remove-AzApplicationGatewayFrontendIPConfig](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[Set-AzApplicationGatewayFrontendIPConfig](./Set-AzApplicationGatewayFrontendIPConfig.md)


