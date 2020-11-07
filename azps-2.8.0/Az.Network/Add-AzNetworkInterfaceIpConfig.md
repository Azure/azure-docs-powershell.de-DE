---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 7aed72b3d219bf8a8c4f930d0b575fca4338ffc6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822500"
---
# <span data-ttu-id="db828-101">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="db828-101">Add-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="db828-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="db828-102">SYNOPSIS</span></span>
<span data-ttu-id="db828-103">Fügt eine Netzwerkschnittstelle-IP-Konfiguration zu einer Netzwerkschnittstelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="db828-103">Adds a network interface IP configuration to a network interface.</span></span>

## <span data-ttu-id="db828-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="db828-104">SYNTAX</span></span>

### <span data-ttu-id="db828-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="db828-105">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db828-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="db828-106">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db828-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="db828-107">DESCRIPTION</span></span>
<span data-ttu-id="db828-108">Mit dem Cmdlet **Add-AzNetworkInterfaceIpConfig** wird eine Netzwerkschnittstellen-IP-Konfiguration zu einer Azure-Netzwerkschnittstelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="db828-108">The **Add-AzNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="db828-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="db828-109">EXAMPLES</span></span>

### <span data-ttu-id="db828-110">Beispiel 1: Hinzufügen einer neuen IP-Konfiguration mit einer Anwendungs Sicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="db828-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzVirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US" -Subnet $vnet.Subnets[0]

$asg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface

$nic | Add-AzNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface
```

<span data-ttu-id="db828-111">In diesem Beispiel wird eine neue Netzwerkschnittstellen-MyNetworkInterface erstellt, die zu einem Subnetz im neuen virtuellen Netzwerk MyVNET gehört.</span><span class="sxs-lookup"><span data-stu-id="db828-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="db828-112">Darüber hinaus erstellen wir eine leere Anwendungs Sicherheitsgruppe MyASG, die mit den IP-Konfigurationen in der Netzwerkschnittstelle verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="db828-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="db828-113">Nachdem beide Objekte erstellt wurden, verknüpfen wir die standardmäßige IP-Konfiguration mit dem MyASG-Objekt.</span><span class="sxs-lookup"><span data-stu-id="db828-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="db828-114">Endlich erstellen wir eine neue IP-Konfiguration in der Netzwerkschnittstelle, die ebenfalls mit dem Application Security Group-Objekt verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="db828-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="db828-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="db828-115">PARAMETERS</span></span>

### <span data-ttu-id="db828-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="db828-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="db828-117">Gibt eine Sammlung von Anwendungsgateway-Back-End-Adresspool verweisen an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="db828-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="db828-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="db828-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="db828-119">Gibt eine Sammlung von Anwendungsgateway-Back-End-Adresspool verweisen an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="db828-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="db828-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="db828-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="db828-121">Gibt eine Sammlung von Anwendungs Sicherheitsgruppen verweisen an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="db828-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="db828-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="db828-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="db828-123">Gibt eine Sammlung von Anwendungs Sicherheitsgruppen verweisen an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="db828-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="db828-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db828-124">-DefaultProfile</span></span>
<span data-ttu-id="db828-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="db828-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db828-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="db828-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="db828-127">Gibt eine Sammlung von Quellen des Load Balancer-Back-End-Adresspools an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="db828-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="db828-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="db828-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="db828-129">Gibt eine Sammlung von Quellen des Load Balancer-Back-End-Adresspools an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="db828-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="db828-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="db828-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="db828-131">Gibt eine Sammlung von NAT-Regel Bezügen (eingehende Netzwerkadressübersetzung) für den Lastenausgleich an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="db828-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="db828-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="db828-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="db828-133">Gibt eine Sammlung von eingehenden NAT-Regel Bezügen für das Load Balancer an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="db828-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="db828-134">-Name</span><span class="sxs-lookup"><span data-stu-id="db828-134">-Name</span></span>
<span data-ttu-id="db828-135">Gibt den Namen der Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="db828-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="db828-136">-Network Interface</span><span class="sxs-lookup"><span data-stu-id="db828-136">-NetworkInterface</span></span>
<span data-ttu-id="db828-137">Gibt ein **Network Interface** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="db828-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="db828-138">Mit diesem Cmdlet wird dem Objekt, das dieser Parameter angibt, eine Netzwerkschnittstellen-IP-Konfiguration hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="db828-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="db828-139">– Primär</span><span class="sxs-lookup"><span data-stu-id="db828-139">-Primary</span></span>
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

### <span data-ttu-id="db828-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="db828-140">-PrivateIpAddress</span></span>
<span data-ttu-id="db828-141">Gibt die statische IP-Adresse der Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="db828-141">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="db828-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="db828-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="db828-143">Gibt die IP-Adressenversion einer Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="db828-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="db828-144">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="db828-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="db828-145">IPv4</span><span class="sxs-lookup"><span data-stu-id="db828-145">IPv4</span></span>
- <span data-ttu-id="db828-146">IPv6</span><span class="sxs-lookup"><span data-stu-id="db828-146">IPv6</span></span>

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

### <span data-ttu-id="db828-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="db828-147">-PublicIpAddress</span></span>
<span data-ttu-id="db828-148">Gibt ein **PublicIPAddress** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="db828-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="db828-149">Dieses Cmdlet erstellt einen Verweis auf eine öffentliche IP-Adresse, die dieser Netzwerkschnittstellen-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="db828-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="db828-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="db828-150">-PublicIpAddressId</span></span>
<span data-ttu-id="db828-151">Dieses Cmdlet erstellt einen Verweis auf eine öffentliche IP-Adresse, die dieser Netzwerkschnittstellen-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="db828-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="db828-152">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="db828-152">-Subnet</span></span>
<span data-ttu-id="db828-153">Gibt ein **Subnetz** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="db828-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="db828-154">Dieses Cmdlet erstellt einen Verweis auf ein Subnetz, in dem diese Netzwerkschnittstellen-IP-Konfiguration erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="db828-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="db828-155">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="db828-155">-SubnetId</span></span>
<span data-ttu-id="db828-156">Dieses Cmdlet erstellt einen Verweis auf ein Subnetz, in dem diese Netzwerkschnittstellen-IP-Konfiguration erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="db828-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="db828-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db828-157">CommonParameters</span></span>
<span data-ttu-id="db828-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db828-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db828-159">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db828-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db828-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="db828-160">INPUTS</span></span>

### <span data-ttu-id="db828-161">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="db828-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="db828-162">System. String []</span><span class="sxs-lookup"><span data-stu-id="db828-162">System.String[]</span></span>

### <span data-ttu-id="db828-163">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="db828-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="db828-164">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="db828-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="db828-165">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="db828-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="db828-166">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="db828-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="db828-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="db828-167">OUTPUTS</span></span>

### <span data-ttu-id="db828-168">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="db828-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="db828-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="db828-169">NOTES</span></span>
* <span data-ttu-id="db828-170">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="db828-170">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="db828-171">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="db828-171">RELATED LINKS</span></span>

[<span data-ttu-id="db828-172">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="db828-172">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="db828-173">Neu – AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="db828-173">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="db828-174">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="db828-174">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="db828-175">Satz-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="db828-175">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
