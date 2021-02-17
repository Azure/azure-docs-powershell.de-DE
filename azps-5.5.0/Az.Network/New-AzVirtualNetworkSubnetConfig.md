---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 7afedb15ea5e7b5e2968dbb425a662f7de7e2ac1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169776"
---
# New-AzVirtualNetworkSubnetConfig

## SYNOPSIS
Erstellt eine Subnetzkonfiguration für ein virtuelles Netzwerk.

## SYNTAX

### SetByResource (Standard)
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SetByResourceId
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ResourceId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-PrivateEndpointNetworkPoliciesFlag <String>] [-PrivateLinkServiceNetworkPoliciesFlag <String>]
 [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
**Das Cmdlet "New-AzVirtualNetworkSubnetConfig"** erstellt eine Subnetzkonfiguration für ein virtuelles Netzwerk.

## BEISPIELE

### Beispiel 1: Erstellen eines virtuellen Netzwerks mit zwei Subnetzen und einer Netzwerksicherheitsgruppe
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

$pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" `
   -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"

$natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" `
   -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip

$natGatewaySubnet = New-AzVirtualNetworkSubnetConfig -Name natGatewaySubnet `
   -AddressPrefix "10.0.3.0/24" -InputObject $natGateway

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet,$natGatewaySubnet
```

In diesem Beispiel werden zwei neue Subnetzkonfigurationen mit dem cmdlet New-AzVirtualSubnetConfig erstellt, die dann zum Erstellen eines virtuellen Netzwerks verwendet werden. Mit New-AzVirtualSubnetConfig Vorlage wird nur eine speicherinte Darstellung des Subnetzes erstellt. In diesem Beispiel hat das frontendSubnet CIDR 10.0.1.0/24 und verweist auf eine Netzwerksicherheitsgruppe, die RDP-Zugriff zulässt. Das Back-EndSubnet verfügt über CIDR 10.0.2.0/24 und verweist auf dieselbe Netzwerksicherheitsgruppe.

## PARAMETERS

### -AddressPrefix
Gibt einen Bereich von IP-Adressen für eine Subnetzkonfiguration an.

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

### -Delegierung
Liste der Dienste, die über die Berechtigung zum Ausführen von Vorgängen in diesem Subnetz verfügen.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSDelegation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
Gibt das nat-Gateway an, das der Subnetzkonfiguration zugeordnet ist.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByResource
Aliases: NatGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpAllocation
Gibt "IpAllocations" für ein Subnetz an.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der zu erstellenden Subnetzkonfiguration an.

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

### -NetworkSecurityGroup
Gibt ein NetworkSecurityGroup-Objekt an.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkSecurityGroupId
Gibt die ID einer Netzwerksicherheitsgruppe an.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrivateEndpointNetworkPoliciesFlag
Konfigurieren Sie die Aktivierung oder Deaktivierung der Anwendung von Netzwerkrichtlinien auf privaten Endpunkten im Subnetz.

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

### -PrivateLinkServiceNetworkPoliciesFlag
Konfigurieren Sie die Aktivierung oder Deaktivierung der Anwendung von Netzwerkrichtlinien auf den Dienst für private Verknüpfungen im Subnetz.

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

### -ResourceId
Gibt die ID der NAT-Gateway-Ressource an, die der Subnetzkonfiguration zugeordnet ist.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: NatGatewayId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RouteTable
Gibt die Routentabelle an, die der Subnetzkonfiguration zugeordnet ist.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RouteTableId
Gibt die ID der Routentabelle an, die der Subnetzkonfiguration zugeordnet ist.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceEndpoint
Dienstendpunktwert

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceEndpointPolicy
Richtlinien für Dienstendpunkt

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup

### Microsoft.Azure.Commands.Network.Models.PSRouteTable

### Microsoft.Azure.Commands.Network.Models.PSNatGateway

### System.String[]

### Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]

### Microsoft.Azure.Commands.Network.Models.PSDElegation[]

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSSubnet

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Add-AzVirtualNetworkSubnetConfig](./Add-AzVirtualNetworkSubnetConfig.md)

[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)

[Remove-AzVirtualNetworkSubnetConfig](./Remove-AzVirtualNetworkSubnetConfig.md)

[Set-AzVirtualNetworkSubnetConfig](./Set-AzVirtualNetworkSubnetConfig.md)
