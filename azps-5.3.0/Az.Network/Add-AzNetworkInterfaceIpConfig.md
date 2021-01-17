---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 9fef4a3cfe57b75ad992d4f4068bb0d51bbdcd90
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467452"
---
# <span data-ttu-id="0f5be-101">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0f5be-101">Add-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="0f5be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f5be-102">SYNOPSIS</span></span>
<span data-ttu-id="0f5be-103">Fügt einer Netzwerkschnittstelle eine Netzwerkschnittstellen-IP-Konfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="0f5be-103">Adds a network interface IP configuration to a network interface.</span></span>

## <span data-ttu-id="0f5be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f5be-104">SYNTAX</span></span>

### <span data-ttu-id="0f5be-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="0f5be-105">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f5be-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0f5be-106">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f5be-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f5be-107">DESCRIPTION</span></span>
<span data-ttu-id="0f5be-108">Das **Cmdlet "Add-AzNetworkInterfaceIpConfig"** fügt einer Azure-Netzwerkschnittstelle eine Netzwerkschnittstellen-IP-Konfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="0f5be-108">The **Add-AzNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="0f5be-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0f5be-109">EXAMPLES</span></span>

### <span data-ttu-id="0f5be-110">Beispiel 1: Hinzufügen einer neuen IP-Konfiguration mit einer Anwendungssicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="0f5be-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzVirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US" -Subnet $vnet.Subnets[0]

$asg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface

$nic | Add-AzNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface
```

<span data-ttu-id="0f5be-111">In diesem Beispiel erstellen wir eine neue Netzwerkschnittstelle "MyNetworkInterface", die zu einem Subnetz im neuen virtuellen Netzwerk MyVNET gehört.</span><span class="sxs-lookup"><span data-stu-id="0f5be-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="0f5be-112">Außerdem wird eine leere Anwendungssicherheitsgruppe "MyASG" erstellt, die den IP-Konfigurationen in der Netzwerkschnittstelle zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="0f5be-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="0f5be-113">Sobald beide Objekte erstellt wurden, verknüpfen wir die Standard-IP-Konfiguration mit dem MyASG-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0f5be-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="0f5be-114">Schließlich erstellen wir eine neue IP-Konfiguration in der Netzwerkschnittstelle, die ebenfalls mit dem Anwendungssicherheitsgruppenobjekt verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="0f5be-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="0f5be-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f5be-115">PARAMETERS</span></span>

### <span data-ttu-id="0f5be-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0f5be-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="0f5be-117">Gibt eine Sammlung von Verweisen auf den Back-End-Adresspool des Anwendungsgateways an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="0f5be-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f5be-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="0f5be-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="0f5be-119">Gibt eine Sammlung von Verweisen auf den Back-End-Adresspool des Anwendungsgateways an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="0f5be-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f5be-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0f5be-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="0f5be-121">Gibt eine Sammlung von Anwendungssicherheitsgruppeverweisen an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="0f5be-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f5be-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="0f5be-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="0f5be-123">Gibt eine Sammlung von Anwendungssicherheitsgruppeverweisen an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="0f5be-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f5be-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f5be-124">-DefaultProfile</span></span>
<span data-ttu-id="0f5be-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0f5be-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f5be-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0f5be-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="0f5be-127">Gibt eine Sammlung von Verweisen auf den Load Balancer-Back-End-Adresspool an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="0f5be-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f5be-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="0f5be-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="0f5be-129">Gibt eine Sammlung von Verweisen auf den Load Balancer-Back-End-Adresspool an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="0f5be-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f5be-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="0f5be-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="0f5be-131">Gibt eine Sammlung von Bezügen zur eingehenden Netzwerkadressenübersetzung (Network Address Translation, NAT) an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="0f5be-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f5be-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="0f5be-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="0f5be-133">Gibt eine Sammlung von eingehenden NAT-Regelverweisen für den Lastenausgleich an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="0f5be-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f5be-134">-Name</span><span class="sxs-lookup"><span data-stu-id="0f5be-134">-Name</span></span>
<span data-ttu-id="0f5be-135">Gibt den Namen der Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="0f5be-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="0f5be-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0f5be-136">-NetworkInterface</span></span>
<span data-ttu-id="0f5be-137">Gibt ein **"NetworkInterface"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="0f5be-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="0f5be-138">Dieses Cmdlet fügt dem von diesem Parameter angegebenen Objekt eine Netzwerkschnittstellen-IP-Konfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="0f5be-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f5be-139">-Primary</span><span class="sxs-lookup"><span data-stu-id="0f5be-139">-Primary</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f5be-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="0f5be-140">-PrivateIpAddress</span></span>
<span data-ttu-id="0f5be-141">Gibt die statische IP-Adresse der Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="0f5be-141">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="0f5be-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="0f5be-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="0f5be-143">Gibt die IP-Adressversion einer Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="0f5be-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="0f5be-144">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="0f5be-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0f5be-145">IPv4</span><span class="sxs-lookup"><span data-stu-id="0f5be-145">IPv4</span></span>
- <span data-ttu-id="0f5be-146">IPv6</span><span class="sxs-lookup"><span data-stu-id="0f5be-146">IPv6</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f5be-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0f5be-147">-PublicIpAddress</span></span>
<span data-ttu-id="0f5be-148">Gibt ein **PublicIPAddress-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="0f5be-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="0f5be-149">Dieses Cmdlet erstellt einen Verweis auf eine öffentliche IP-Adresse, die dieser Netzwerkschnittstellen-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0f5be-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="0f5be-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="0f5be-150">-PublicIpAddressId</span></span>
<span data-ttu-id="0f5be-151">Dieses Cmdlet erstellt einen Verweis auf eine öffentliche IP-Adresse, die dieser Netzwerkschnittstellen-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0f5be-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="0f5be-152">-Subnet</span><span class="sxs-lookup"><span data-stu-id="0f5be-152">-Subnet</span></span>
<span data-ttu-id="0f5be-153">Gibt ein **Subnetzobjekt** an.</span><span class="sxs-lookup"><span data-stu-id="0f5be-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="0f5be-154">Dieses Cmdlet erstellt einen Verweis auf ein Subnetz, in dem diese Konfiguration der Netzwerkschnittstelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0f5be-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="0f5be-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0f5be-155">-SubnetId</span></span>
<span data-ttu-id="0f5be-156">Dieses Cmdlet erstellt einen Verweis auf ein Subnetz, in dem diese Konfiguration der Netzwerkschnittstelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0f5be-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="0f5be-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f5be-157">CommonParameters</span></span>
<span data-ttu-id="0f5be-158">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f5be-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f5be-159">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f5be-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f5be-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0f5be-160">INPUTS</span></span>

### <span data-ttu-id="0f5be-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0f5be-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="0f5be-162">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0f5be-162">System.String[]</span></span>

### <span data-ttu-id="0f5be-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="0f5be-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="0f5be-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="0f5be-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="0f5be-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="0f5be-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="0f5be-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="0f5be-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="0f5be-167">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0f5be-167">OUTPUTS</span></span>

### <span data-ttu-id="0f5be-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0f5be-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="0f5be-169">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0f5be-169">NOTES</span></span>
* <span data-ttu-id="0f5be-170">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="0f5be-170">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="0f5be-171">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0f5be-171">RELATED LINKS</span></span>

[<span data-ttu-id="0f5be-172">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0f5be-172">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="0f5be-173">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0f5be-173">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="0f5be-174">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0f5be-174">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="0f5be-175">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0f5be-175">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
