---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 7afedb15ea5e7b5e2968dbb425a662f7de7e2ac1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362703"
---
# <span data-ttu-id="91102-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="91102-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="91102-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91102-102">SYNOPSIS</span></span>
<span data-ttu-id="91102-103">Erstellt eine Subnetzkonfiguration für ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="91102-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="91102-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91102-104">SYNTAX</span></span>

### <span data-ttu-id="91102-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="91102-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91102-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="91102-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ResourceId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-PrivateEndpointNetworkPoliciesFlag <String>] [-PrivateLinkServiceNetworkPoliciesFlag <String>]
 [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91102-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91102-107">DESCRIPTION</span></span>
<span data-ttu-id="91102-108">**Das Cmdlet "New-AzVirtualNetworkSubnetConfig"** erstellt eine Subnetzkonfiguration für ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="91102-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="91102-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="91102-109">EXAMPLES</span></span>

### <span data-ttu-id="91102-110">Beispiel 1: Erstellen eines virtuellen Netzwerks mit zwei Subnetzen und einer Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="91102-110">Example 1: Create a virtual network with two subnets and a network security group</span></span>
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

<span data-ttu-id="91102-111">In diesem Beispiel werden zwei neue Subnetzkonfigurationen mit dem cmdlet New-AzVirtualSubnetConfig erstellt, die dann zum Erstellen eines virtuellen Netzwerks verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="91102-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="91102-112">Mit New-AzVirtualSubnetConfig Vorlage wird nur eine speicherinte Darstellung des Subnetzes erstellt.</span><span class="sxs-lookup"><span data-stu-id="91102-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="91102-113">In diesem Beispiel hat das frontendSubnet CIDR 10.0.1.0/24 und verweist auf eine Netzwerksicherheitsgruppe, die RDP-Zugriff zulässt.</span><span class="sxs-lookup"><span data-stu-id="91102-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="91102-114">Das Back-EndSubnet verfügt über CIDR 10.0.2.0/24 und verweist auf dieselbe Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="91102-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="91102-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91102-115">PARAMETERS</span></span>

### <span data-ttu-id="91102-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="91102-116">-AddressPrefix</span></span>
<span data-ttu-id="91102-117">Gibt einen Bereich von IP-Adressen für eine Subnetzkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="91102-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="91102-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91102-118">-DefaultProfile</span></span>
<span data-ttu-id="91102-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="91102-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91102-120">-Delegierung</span><span class="sxs-lookup"><span data-stu-id="91102-120">-Delegation</span></span>
<span data-ttu-id="91102-121">Liste der Dienste, die über die Berechtigung zum Ausführen von Vorgängen in diesem Subnetz verfügen.</span><span class="sxs-lookup"><span data-stu-id="91102-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="91102-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91102-122">-InputObject</span></span>
<span data-ttu-id="91102-123">Gibt das nat-Gateway an, das der Subnetzkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="91102-123">Specifies the nat gateway associated with the subnet configuration</span></span>

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

### <span data-ttu-id="91102-124">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="91102-124">-IpAllocation</span></span>
<span data-ttu-id="91102-125">Gibt "IpAllocations" für ein Subnetz an.</span><span class="sxs-lookup"><span data-stu-id="91102-125">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="91102-126">-Name</span><span class="sxs-lookup"><span data-stu-id="91102-126">-Name</span></span>
<span data-ttu-id="91102-127">Gibt den Namen der zu erstellenden Subnetzkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="91102-127">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="91102-128">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="91102-128">-NetworkSecurityGroup</span></span>
<span data-ttu-id="91102-129">Gibt ein NetworkSecurityGroup-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="91102-129">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="91102-130">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="91102-130">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="91102-131">Gibt die ID einer Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="91102-131">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="91102-132">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="91102-132">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="91102-133">Konfigurieren Sie die Aktivierung oder Deaktivierung der Anwendung von Netzwerkrichtlinien auf privaten Endpunkten im Subnetz.</span><span class="sxs-lookup"><span data-stu-id="91102-133">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="91102-134">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="91102-134">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="91102-135">Konfigurieren Sie die Aktivierung oder Deaktivierung der Anwendung von Netzwerkrichtlinien auf den Dienst für private Verknüpfungen im Subnetz.</span><span class="sxs-lookup"><span data-stu-id="91102-135">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="91102-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91102-136">-ResourceId</span></span>
<span data-ttu-id="91102-137">Gibt die ID der NAT-Gateway-Ressource an, die der Subnetzkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="91102-137">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="91102-138">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="91102-138">-RouteTable</span></span>
<span data-ttu-id="91102-139">Gibt die Routentabelle an, die der Subnetzkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="91102-139">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="91102-140">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="91102-140">-RouteTableId</span></span>
<span data-ttu-id="91102-141">Gibt die ID der Routentabelle an, die der Subnetzkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="91102-141">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="91102-142">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="91102-142">-ServiceEndpoint</span></span>
<span data-ttu-id="91102-143">Dienstendpunktwert</span><span class="sxs-lookup"><span data-stu-id="91102-143">Service Endpoint Value</span></span>

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

### <span data-ttu-id="91102-144">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="91102-144">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="91102-145">Richtlinien für Dienstendpunkt</span><span class="sxs-lookup"><span data-stu-id="91102-145">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="91102-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91102-146">CommonParameters</span></span>
<span data-ttu-id="91102-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91102-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91102-148">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91102-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91102-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="91102-149">INPUTS</span></span>

### <span data-ttu-id="91102-150">System.String</span><span class="sxs-lookup"><span data-stu-id="91102-150">System.String</span></span>

### <span data-ttu-id="91102-151">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="91102-151">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="91102-152">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="91102-152">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="91102-153">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="91102-153">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="91102-154">System.String[]</span><span class="sxs-lookup"><span data-stu-id="91102-154">System.String[]</span></span>

### <span data-ttu-id="91102-155">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="91102-155">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="91102-156">Microsoft.Azure.Commands.Network.Models.PSD-Elegation[]</span><span class="sxs-lookup"><span data-stu-id="91102-156">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="91102-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="91102-157">OUTPUTS</span></span>

### <span data-ttu-id="91102-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="91102-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="91102-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="91102-159">NOTES</span></span>

## <span data-ttu-id="91102-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="91102-160">RELATED LINKS</span></span>

[<span data-ttu-id="91102-161">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="91102-161">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="91102-162">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="91102-162">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="91102-163">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="91102-163">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="91102-164">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="91102-164">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
