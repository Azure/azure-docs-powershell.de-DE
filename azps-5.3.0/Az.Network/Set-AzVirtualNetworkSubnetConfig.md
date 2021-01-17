---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: fe6c67c39ef3d14ec1b1e4200b4fad09aa7d2a24
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473358"
---
# <span data-ttu-id="9d670-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9d670-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="9d670-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d670-102">SYNOPSIS</span></span>
<span data-ttu-id="9d670-103">Aktualisiert eine Subnetzkonfiguration für ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="9d670-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="9d670-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d670-104">SYNTAX</span></span>

### <span data-ttu-id="9d670-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="9d670-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d670-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9d670-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d670-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d670-107">DESCRIPTION</span></span>
<span data-ttu-id="9d670-108">Das **Cmdlet Set-AzVirtualNetworkSubnetConfig** aktualisiert eine Subnetzkonfiguration für ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="9d670-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="9d670-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9d670-109">EXAMPLES</span></span>

### <span data-ttu-id="9d670-110">1: Ändern des Adresspräfixs eines Subnetzes</span><span class="sxs-lookup"><span data-stu-id="9d670-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="9d670-111">In diesem Beispiel wird ein virtuelles Netzwerk mit einem Subnetz erstellt.</span><span class="sxs-lookup"><span data-stu-id="9d670-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="9d670-112">Anschließend werden Aufrufe Set-AzVirtualNetworkSubnetConfig, um das AddressPrefix des Subnetzes zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9d670-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="9d670-113">Dies betrifft nur die Speicherdarstellung des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="9d670-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="9d670-114">Set-AzVirtualNetwork wird dann aufgerufen, um das virtuelle Netzwerk in Azure zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9d670-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="9d670-115">2: Hinzufügen einer Netzwerksicherheitsgruppe zu einem Subnetz</span><span class="sxs-lookup"><span data-stu-id="9d670-115">2: Add a network security group to a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="9d670-116">In diesem Beispiel wird eine Ressourcengruppe mit einem virtuellen Netzwerk erstellt, das nur ein Subnetz enthält.</span><span class="sxs-lookup"><span data-stu-id="9d670-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="9d670-117">Anschließend erstellt sie eine Netzwerksicherheitsgruppe mit einer "Allow"-Regel für RDP-Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="9d670-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="9d670-118">Das Set-AzVirtualNetworkSubnetConfig cmdlet wird verwendet, um die speicherinte Darstellung des frontend-Subnetzes so zu ändern, dass es auf die neu erstellte Netzwerksicherheitsgruppe verweist.</span><span class="sxs-lookup"><span data-stu-id="9d670-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="9d670-119">Das Set-AzVirtualNetwork cmdlet wird dann aufgerufen, um den geänderten Zustand wieder in den Dienst zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="9d670-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

### <span data-ttu-id="9d670-120">3: Anfügen eines Nat-Gateways an ein Subnetz</span><span class="sxs-lookup"><span data-stu-id="9d670-120">3: Attach a Nat Gateway to a subnet</span></span>
```
$pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" `
   -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"

$natGateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" `
   -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" 

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -InputObject $natGateway 

$virtualNetwork | Set-AzVirtualNetwork
```

## <span data-ttu-id="9d670-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d670-121">PARAMETERS</span></span>

### <span data-ttu-id="9d670-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9d670-122">-AddressPrefix</span></span>
<span data-ttu-id="9d670-123">Gibt einen Bereich von IP-Adressen für eine Subnetzkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="9d670-123">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="9d670-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d670-124">-DefaultProfile</span></span>
<span data-ttu-id="9d670-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d670-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d670-126">-Delegierung</span><span class="sxs-lookup"><span data-stu-id="9d670-126">-Delegation</span></span>
<span data-ttu-id="9d670-127">Liste der Dienste, die über die Berechtigung zum Ausführen von Vorgängen in diesem Subnetz verfügen.</span><span class="sxs-lookup"><span data-stu-id="9d670-127">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="9d670-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d670-128">-InputObject</span></span>
<span data-ttu-id="9d670-129">Gibt das nat-Gateway an, das der Subnetzkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9d670-129">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="9d670-130">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="9d670-130">-IpAllocation</span></span>
<span data-ttu-id="9d670-131">Gibt "IpAllocations" für ein Subnetz an.</span><span class="sxs-lookup"><span data-stu-id="9d670-131">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="9d670-132">-Name</span><span class="sxs-lookup"><span data-stu-id="9d670-132">-Name</span></span>
<span data-ttu-id="9d670-133">Gibt den Namen einer Subnetzkonfiguration an, die von diesem Cmdlet konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="9d670-133">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="9d670-134">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9d670-134">-NetworkSecurityGroup</span></span>
<span data-ttu-id="9d670-135">Gibt ein **NetworkSecurityGroup-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="9d670-135">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="9d670-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="9d670-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="9d670-137">Gibt die ID einer Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="9d670-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="9d670-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="9d670-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="9d670-139">Konfigurieren Sie die Aktivierung oder Deaktivierung der Anwendung von Netzwerkrichtlinien auf privaten Endpunkten im Subnetz.</span><span class="sxs-lookup"><span data-stu-id="9d670-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="9d670-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="9d670-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="9d670-141">Konfigurieren Sie die Aktivierung oder Deaktivierung der Anwendung von Netzwerkrichtlinien auf den Dienst für private Verknüpfungen im Subnetz.</span><span class="sxs-lookup"><span data-stu-id="9d670-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="9d670-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d670-142">-ResourceId</span></span>
<span data-ttu-id="9d670-143">Gibt die ID der NAT-Gateway-Ressource an, die der Subnetzkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9d670-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="9d670-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="9d670-144">-RouteTable</span></span>
<span data-ttu-id="9d670-145">Gibt das Routentabellesobjekt an, das der Netzwerksicherheitsgruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9d670-145">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="9d670-146">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="9d670-146">-RouteTableId</span></span>
<span data-ttu-id="9d670-147">Gibt die ID des Tabellenobjekts für die Route an, das der Netzwerksicherheitsgruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9d670-147">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="9d670-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="9d670-148">-ServiceEndpoint</span></span>
<span data-ttu-id="9d670-149">Dienstendpunktwert</span><span class="sxs-lookup"><span data-stu-id="9d670-149">Service Endpoint Value</span></span>

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

### <span data-ttu-id="9d670-150">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="9d670-150">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="9d670-151">Richtlinien für Dienstendpunkt</span><span class="sxs-lookup"><span data-stu-id="9d670-151">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="9d670-152">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9d670-152">-VirtualNetwork</span></span>
<span data-ttu-id="9d670-153">Gibt das **VirtualNetwork-Objekt** an, das die Subnetzkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="9d670-153">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="9d670-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d670-154">CommonParameters</span></span>
<span data-ttu-id="9d670-155">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d670-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d670-156">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d670-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d670-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9d670-157">INPUTS</span></span>

### <span data-ttu-id="9d670-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9d670-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="9d670-159">System.String</span><span class="sxs-lookup"><span data-stu-id="9d670-159">System.String</span></span>

### <span data-ttu-id="9d670-160">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9d670-160">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="9d670-161">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="9d670-161">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="9d670-162">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9d670-162">System.String[]</span></span>

### <span data-ttu-id="9d670-163">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="9d670-163">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="9d670-164">Microsoft.Azure.Commands.Network.Models.PSD-Elegation[]</span><span class="sxs-lookup"><span data-stu-id="9d670-164">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="9d670-165">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9d670-165">OUTPUTS</span></span>

### <span data-ttu-id="9d670-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9d670-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="9d670-167">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9d670-167">NOTES</span></span>

## <span data-ttu-id="9d670-168">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9d670-168">RELATED LINKS</span></span>

[<span data-ttu-id="9d670-169">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9d670-169">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9d670-170">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9d670-170">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9d670-171">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9d670-171">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9d670-172">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9d670-172">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)
