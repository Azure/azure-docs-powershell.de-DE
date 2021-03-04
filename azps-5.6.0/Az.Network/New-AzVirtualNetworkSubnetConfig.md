---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 5a874bac2a546a07b2946ec8315065035cabba72
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931747"
---
# <span data-ttu-id="87a5b-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="87a5b-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="87a5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87a5b-102">SYNOPSIS</span></span>
<span data-ttu-id="87a5b-103">Erstellt eine Subnetzkonfiguration für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="87a5b-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="87a5b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87a5b-104">SYNTAX</span></span>

### <span data-ttu-id="87a5b-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="87a5b-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87a5b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="87a5b-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ResourceId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-PrivateEndpointNetworkPoliciesFlag <String>] [-PrivateLinkServiceNetworkPoliciesFlag <String>]
 [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87a5b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87a5b-107">DESCRIPTION</span></span>
<span data-ttu-id="87a5b-108">**Das Cmdlet New-AzVirtualNetworkSubnetConfig** erstellt eine Subnetzkonfiguration für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="87a5b-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="87a5b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="87a5b-109">EXAMPLES</span></span>

### <span data-ttu-id="87a5b-110">Beispiel 1: Erstellen eines virtuellen Netzwerks mit zwei Subnetzen und einer Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="87a5b-110">Example 1: Create a virtual network with two subnets and a network security group</span></span>
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

<span data-ttu-id="87a5b-111">In diesem Beispiel werden zwei neue Subnetzkonfigurationen mithilfe des cmdlets New-AzVirtualSubnetConfig erstellt und dann zum Erstellen eines virtuellen Netzwerks verwendet.</span><span class="sxs-lookup"><span data-stu-id="87a5b-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="87a5b-112">Die New-AzVirtualSubnetConfig erstellt nur eine Speicherdarstellung des Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="87a5b-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="87a5b-113">In diesem Beispiel verfügt das frontendSubnet über CIDR 10.0.1.0/24 und verweist auf eine Netzwerksicherheitsgruppe, die rdP-Zugriff ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="87a5b-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="87a5b-114">Das back-EndSubnet verfügt über CIDR 10.0.2.0/24 und verweist auf dieselbe Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="87a5b-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="87a5b-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="87a5b-115">PARAMETERS</span></span>

### <span data-ttu-id="87a5b-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="87a5b-116">-AddressPrefix</span></span>
<span data-ttu-id="87a5b-117">Gibt einen Bereich von IP-Adressen für eine Subnetzkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="87a5b-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="87a5b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87a5b-118">-DefaultProfile</span></span>
<span data-ttu-id="87a5b-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87a5b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87a5b-120">-Delegierung</span><span class="sxs-lookup"><span data-stu-id="87a5b-120">-Delegation</span></span>
<span data-ttu-id="87a5b-121">Liste der Dienste, die über die Berechtigung zum Ausführen von Vorgängen in diesem Subnetz verfügen.</span><span class="sxs-lookup"><span data-stu-id="87a5b-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="87a5b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87a5b-122">-InputObject</span></span>
<span data-ttu-id="87a5b-123">Gibt das nat-Gateway an, das der Subnetzkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="87a5b-123">Specifies the nat gateway associated with the subnet configuration</span></span>

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

### <span data-ttu-id="87a5b-124">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="87a5b-124">-IpAllocation</span></span>
<span data-ttu-id="87a5b-125">Gibt IpAllocations für ein Subnetz an.</span><span class="sxs-lookup"><span data-stu-id="87a5b-125">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="87a5b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="87a5b-126">-Name</span></span>
<span data-ttu-id="87a5b-127">Gibt den Namen der zu erstellenden Subnetzkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="87a5b-127">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="87a5b-128">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="87a5b-128">-NetworkSecurityGroup</span></span>
<span data-ttu-id="87a5b-129">Gibt ein NetworkSecurityGroup-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="87a5b-129">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="87a5b-130">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="87a5b-130">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="87a5b-131">Gibt die ID einer Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="87a5b-131">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="87a5b-132">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="87a5b-132">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="87a5b-133">Konfigurieren, um das Anwenden von Netzwerkrichtlinien auf privaten Endpunkt im Subnetz zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="87a5b-133">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="87a5b-134">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="87a5b-134">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="87a5b-135">Konfigurieren, um die Anwendung von Netzwerkrichtlinien für den privaten Linkdienst im Subnetz zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="87a5b-135">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="87a5b-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87a5b-136">-ResourceId</span></span>
<span data-ttu-id="87a5b-137">Gibt die ID der NAT-Gateway-Ressource an, die der Subnetzkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="87a5b-137">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="87a5b-138">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="87a5b-138">-RouteTable</span></span>
<span data-ttu-id="87a5b-139">Gibt die der Subnetzkonfiguration zugeordnete Routentabelle an.</span><span class="sxs-lookup"><span data-stu-id="87a5b-139">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="87a5b-140">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="87a5b-140">-RouteTableId</span></span>
<span data-ttu-id="87a5b-141">Gibt die ID der Der Subnetzkonfiguration zugeordneten Routentabelle an.</span><span class="sxs-lookup"><span data-stu-id="87a5b-141">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="87a5b-142">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="87a5b-142">-ServiceEndpoint</span></span>
<span data-ttu-id="87a5b-143">Wert des Dienstendpunkts</span><span class="sxs-lookup"><span data-stu-id="87a5b-143">Service Endpoint Value</span></span>

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

### <span data-ttu-id="87a5b-144">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="87a5b-144">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="87a5b-145">Richtlinien für Dienstendpunkt</span><span class="sxs-lookup"><span data-stu-id="87a5b-145">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="87a5b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a5b-146">CommonParameters</span></span>
<span data-ttu-id="87a5b-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87a5b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a5b-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87a5b-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a5b-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="87a5b-149">INPUTS</span></span>

### <span data-ttu-id="87a5b-150">System.String</span><span class="sxs-lookup"><span data-stu-id="87a5b-150">System.String</span></span>

### <span data-ttu-id="87a5b-151">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="87a5b-151">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="87a5b-152">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="87a5b-152">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="87a5b-153">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="87a5b-153">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="87a5b-154">System.String[]</span><span class="sxs-lookup"><span data-stu-id="87a5b-154">System.String[]</span></span>

### <span data-ttu-id="87a5b-155">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="87a5b-155">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="87a5b-156">Microsoft.Azure.Commands.Network.Models.PSD-Elegation[]</span><span class="sxs-lookup"><span data-stu-id="87a5b-156">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="87a5b-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="87a5b-157">OUTPUTS</span></span>

### <span data-ttu-id="87a5b-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="87a5b-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="87a5b-159">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="87a5b-159">NOTES</span></span>

## <span data-ttu-id="87a5b-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="87a5b-160">RELATED LINKS</span></span>

[<span data-ttu-id="87a5b-161">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="87a5b-161">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="87a5b-162">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="87a5b-162">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="87a5b-163">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="87a5b-163">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="87a5b-164">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="87a5b-164">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
