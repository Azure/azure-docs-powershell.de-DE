---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: c3d01639d428820578ffe8a319bddd591c007e00
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359678"
---
# Add-AzVirtualNetworkSubnetConfig

## SYNOPSIS
Fügt einem virtuellen Netzwerk eine Subnetzkonfiguration hinzu.

## SYNTAX

### SetByResource (Standard)
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SetByResourceId
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Add-AzVirtualNetworkSubnetConfig"** fügt einem vorhandenen virtuellen Azure-Netzwerk eine Subnetzkonfiguration hinzu.

## BEISPIELE

### Beispiel 1: Hinzufügen eines Subnetzes zu einem vorhandenen virtuellen Netzwerk
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  In diesem Beispiel wird zuerst eine Ressourcengruppe als Container der zu erstellende Ressourcen erstellt. Anschließend erstellt sie eine Subnetzkonfiguration und erstellt damit ein virtuelles Netzwerk. Die Add-AzVirtualNetworkSubnetConfig wird dann verwendet, um der Speicherdarstellung des virtuellen Netzwerks ein Subnetz hinzuzufügen. Der Set-AzVirtualNetwork aktualisiert das vorhandene virtuelle Netzwerk mit dem neuen Subnetz.

### Beispiel 2: Hinzufügen einer Delegierung zu einem Subnetz, das einem vorhandenen virtuellen Netzwerk hinzugefügt wird
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

In diesem Beispiel wird zuerst ein vorhandenes vnet ruft.
Anschließend wird ein Delegierungsobjekt im Arbeitsspeicher erstellt.
Schließlich wird ein neues Subnetz mit dieser Delegierung erstellt, das dem vnet hinzugefügt wird. Die geänderte Konfiguration wird dann an den Server gesendet.

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
Gibt den Namen der hinzuzufügenden Subnetzkonfiguration an.

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
Gibt ein **NetworkSecurityGroup-Objekt** an.
Dieses Cmdlet fügt dem von diesem Parameter angegebenen Objekt eine virtuelle Netzwerk-Subnetzkonfiguration hinzu.

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

### -VirtualNetwork
Gibt das **VirtualNetwork-Objekt** an, in dem eine Subnetzkonfiguration hinzugefügt werden soll.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork

### System.String

### Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup

### Microsoft.Azure.Commands.Network.Models.PSRouteTable

### System.String[]

### Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]

### Microsoft.Azure.Commands.Network.Models.PSD-Elegation[]

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)

[New-AzVirtualNetworkSubnetConfig](./New-AzVirtualNetworkSubnetConfig.md)

[Remove-AzVirtualNetworkSubnetConfig](./Remove-AzVirtualNetworkSubnetConfig.md)

[Set-AzVirtualNetworkSubnetConfig](./Set-AzVirtualNetworkSubnetConfig.md)
