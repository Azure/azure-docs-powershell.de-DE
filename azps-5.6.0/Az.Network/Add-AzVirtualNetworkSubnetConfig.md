---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 4c206bfe4681bfdc1cb622ec90170776e5528ebe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932480"
---
# <span data-ttu-id="5fc07-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5fc07-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="5fc07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fc07-102">SYNOPSIS</span></span>
<span data-ttu-id="5fc07-103">Fügt einem virtuellen Netzwerk eine Subnetzkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="5fc07-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="5fc07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5fc07-104">SYNTAX</span></span>

### <span data-ttu-id="5fc07-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="5fc07-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5fc07-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5fc07-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5fc07-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fc07-107">DESCRIPTION</span></span>
<span data-ttu-id="5fc07-108">Das **Add-AzVirtualNetworkSubnetConfig-Cmdlet** fügt einem vorhandenen virtuellen Azure-Netzwerk eine Subnetzkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="5fc07-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="5fc07-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5fc07-109">EXAMPLES</span></span>

### <span data-ttu-id="5fc07-110">Beispiel 1: Hinzufügen eines Subnetzes zu einem vorhandenen virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="5fc07-110">Example 1: Add a subnet to an existing virtual network</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="5fc07-111">In diesem Beispiel wird zuerst eine Ressourcengruppe als Container der zu erstellende Ressourcen erstellt.</span><span class="sxs-lookup"><span data-stu-id="5fc07-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="5fc07-112">Anschließend wird eine Subnetzkonfiguration erstellt und zum Erstellen eines virtuellen Netzwerks verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fc07-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="5fc07-113">Die Add-AzVirtualNetworkSubnetConfig wird dann verwendet, um der Arbeitsspeicherdarstellung des virtuellen Netzwerks ein Subnetz hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5fc07-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="5fc07-114">Der Set-AzVirtualNetwork aktualisiert das vorhandene virtuelle Netzwerk mit dem neuen Subnetz.</span><span class="sxs-lookup"><span data-stu-id="5fc07-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="5fc07-115">Beispiel 2: Hinzufügen einer Delegierung zu einem Subnetz, das einem vorhandenen virtuellen Netzwerk hinzugefügt wird</span><span class="sxs-lookup"><span data-stu-id="5fc07-115">Example 2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="5fc07-116">Dieses Beispiel ruft zuerst ein vorhandenes vnet ab.</span><span class="sxs-lookup"><span data-stu-id="5fc07-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="5fc07-117">Anschließend wird ein Delegierungsobjekt im Arbeitsspeicher erstellt.</span><span class="sxs-lookup"><span data-stu-id="5fc07-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="5fc07-118">Schließlich wird ein neues Subnetz mit dieser Delegierung erstellt, das dem vnet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="5fc07-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="5fc07-119">Die geänderte Konfiguration wird dann an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="5fc07-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="5fc07-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5fc07-120">PARAMETERS</span></span>

### <span data-ttu-id="5fc07-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5fc07-121">-AddressPrefix</span></span>
<span data-ttu-id="5fc07-122">Gibt einen Bereich von IP-Adressen für eine Subnetzkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="5fc07-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="5fc07-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fc07-123">-DefaultProfile</span></span>
<span data-ttu-id="5fc07-124">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5fc07-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fc07-125">-Delegierung</span><span class="sxs-lookup"><span data-stu-id="5fc07-125">-Delegation</span></span>
<span data-ttu-id="5fc07-126">Liste der Dienste, die über die Berechtigung zum Ausführen von Vorgängen in diesem Subnetz verfügen.</span><span class="sxs-lookup"><span data-stu-id="5fc07-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="5fc07-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fc07-127">-InputObject</span></span>
<span data-ttu-id="5fc07-128">Gibt das nat-Gateway an, das der Subnetzkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5fc07-128">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="5fc07-129">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="5fc07-129">-IpAllocation</span></span>
<span data-ttu-id="5fc07-130">Gibt IpAllocations für ein Subnetz an.</span><span class="sxs-lookup"><span data-stu-id="5fc07-130">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="5fc07-131">-Name</span><span class="sxs-lookup"><span data-stu-id="5fc07-131">-Name</span></span>
<span data-ttu-id="5fc07-132">Gibt den Namen der hinzuzufügenden Subnetzkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="5fc07-132">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="5fc07-133">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5fc07-133">-NetworkSecurityGroup</span></span>
<span data-ttu-id="5fc07-134">Gibt ein **NetworkSecurityGroup-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="5fc07-134">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="5fc07-135">Dieses Cmdlet fügt dem von diesem Parameter angegebenen Objekt eine Subnetzkonfiguration für virtuelle Netzwerke hinzu.</span><span class="sxs-lookup"><span data-stu-id="5fc07-135">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="5fc07-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="5fc07-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="5fc07-137">Gibt die ID einer Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="5fc07-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="5fc07-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="5fc07-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="5fc07-139">Konfigurieren, um das Anwenden von Netzwerkrichtlinien auf privaten Endpunkt im Subnetz zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="5fc07-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="5fc07-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="5fc07-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="5fc07-141">Konfigurieren, um die Anwendung von Netzwerkrichtlinien für den privaten Linkdienst im Subnetz zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="5fc07-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="5fc07-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fc07-142">-ResourceId</span></span>
<span data-ttu-id="5fc07-143">Gibt die ID der NAT-Gateway-Ressource an, die der Subnetzkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5fc07-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="5fc07-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="5fc07-144">-RouteTable</span></span>
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

### <span data-ttu-id="5fc07-145">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="5fc07-145">-RouteTableId</span></span>
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

### <span data-ttu-id="5fc07-146">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="5fc07-146">-ServiceEndpoint</span></span>
<span data-ttu-id="5fc07-147">Wert des Dienstendpunkts</span><span class="sxs-lookup"><span data-stu-id="5fc07-147">Service Endpoint Value</span></span>

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

### <span data-ttu-id="5fc07-148">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5fc07-148">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="5fc07-149">Richtlinien für Dienstendpunkt</span><span class="sxs-lookup"><span data-stu-id="5fc07-149">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="5fc07-150">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5fc07-150">-VirtualNetwork</span></span>
<span data-ttu-id="5fc07-151">Gibt das **VirtualNetwork-Objekt** an, in dem eine Subnetzkonfiguration hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5fc07-151">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="5fc07-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fc07-152">CommonParameters</span></span>
<span data-ttu-id="5fc07-153">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fc07-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fc07-154">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5fc07-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fc07-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5fc07-155">INPUTS</span></span>

### <span data-ttu-id="5fc07-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5fc07-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="5fc07-157">System.String</span><span class="sxs-lookup"><span data-stu-id="5fc07-157">System.String</span></span>

### <span data-ttu-id="5fc07-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5fc07-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="5fc07-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="5fc07-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="5fc07-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="5fc07-160">System.String[]</span></span>

### <span data-ttu-id="5fc07-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="5fc07-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="5fc07-162">Microsoft.Azure.Commands.Network.Models.PSD-Elegation[]</span><span class="sxs-lookup"><span data-stu-id="5fc07-162">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="5fc07-163">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5fc07-163">OUTPUTS</span></span>

### <span data-ttu-id="5fc07-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5fc07-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="5fc07-165">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5fc07-165">NOTES</span></span>

## <span data-ttu-id="5fc07-166">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5fc07-166">RELATED LINKS</span></span>

[<span data-ttu-id="5fc07-167">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5fc07-167">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5fc07-168">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5fc07-168">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5fc07-169">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5fc07-169">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5fc07-170">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5fc07-170">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
