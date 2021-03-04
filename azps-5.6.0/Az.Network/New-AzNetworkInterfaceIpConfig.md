---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 72d2439e66245e8469e440cb5e501cd9e9379fa6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919584"
---
# <span data-ttu-id="8027b-101">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8027b-101">New-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="8027b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8027b-102">SYNOPSIS</span></span>
<span data-ttu-id="8027b-103">Erstellt eine IP-Konfiguration der Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8027b-103">Creates a network interface IP configuration.</span></span>

## <span data-ttu-id="8027b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8027b-104">SYNTAX</span></span>

### <span data-ttu-id="8027b-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="8027b-105">SetByResource (Default)</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8027b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8027b-106">SetByResourceId</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8027b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8027b-107">DESCRIPTION</span></span>
<span data-ttu-id="8027b-108">Das **Cmdlet New-AzNetworkInterfaceIpConfig** erstellt eine Azure-Netzwerkschnittstellen-IP-Konfiguration für eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8027b-108">The **New-AzNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="8027b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8027b-109">EXAMPLES</span></span>

### <span data-ttu-id="8027b-110">1: Erstellen einer IP-Konfiguration mit einer öffentlichen IP-Adresse für eine Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="8027b-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="8027b-111">Die ersten beiden Befehle erhalten ein virtuelles Netzwerk namens "myvnet" und ein Subnetz namens "mysubnet", das zuvor erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8027b-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="8027b-112">Diese werden in $vnet bzw. $Subnet gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8027b-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="8027b-113">Der dritte Befehl ruft eine zuvor erstellte öffentliche IP-Adresse namens PIP1 ab.</span><span class="sxs-lookup"><span data-stu-id="8027b-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="8027b-114">Der vierte Befehl erstellt eine neue IP-Konfiguration namens "IPConfig-1" als primäre IP-Konfiguration mit einer zugehörigen öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="8027b-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="8027b-115">Mit dem letzten Befehl wird dann mithilfe dieser IP-Konfiguration eine Netzwerkschnittstelle namens mynic1 erstellt.</span><span class="sxs-lookup"><span data-stu-id="8027b-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="8027b-116">2: Erstellen einer IP-Konfiguration mit einer privaten IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="8027b-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="8027b-117">Die ersten beiden Befehle erhalten ein virtuelles Netzwerk namens "myvnet" und ein Subnetz namens "mysubnet", das zuvor erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8027b-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="8027b-118">Diese werden in $vnet bzw. $Subnet gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8027b-118">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="8027b-119">Mit dem dritten Befehl wird eine neue IP-Konfiguration namens "IPConfig-2" erstellt, der eine private IP-Adresse 10.0.0.5 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8027b-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="8027b-120">Mit dem letzten Befehl wird dann mithilfe dieser IP-Konfiguration eine Netzwerkschnittstelle namens mynic1 erstellt.</span><span class="sxs-lookup"><span data-stu-id="8027b-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="8027b-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8027b-121">PARAMETERS</span></span>

### <span data-ttu-id="8027b-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8027b-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="8027b-123">Gibt eine Sammlung von Anwendungsgateway-Back-End-Adresspoolverweisen an, zu denen diese NETZWERKSCHNITTSTELLEN-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="8027b-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="8027b-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8027b-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="8027b-125">Gibt eine Sammlung von Anwendungsgateway-Back-End-Adresspoolverweisen an, zu denen diese NETZWERKSCHNITTSTELLEN-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="8027b-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="8027b-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8027b-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="8027b-127">Gibt eine Sammlung von Anwendungssicherheitsgruppeverweisen an, zu denen diese IP-Konfiguration der Netzwerkschnittstelle gehört.</span><span class="sxs-lookup"><span data-stu-id="8027b-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="8027b-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="8027b-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="8027b-129">Gibt eine Sammlung von Anwendungssicherheitsgruppeverweisen an, zu denen diese IP-Konfiguration der Netzwerkschnittstelle gehört.</span><span class="sxs-lookup"><span data-stu-id="8027b-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="8027b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8027b-130">-DefaultProfile</span></span>
<span data-ttu-id="8027b-131">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8027b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8027b-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8027b-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="8027b-133">Gibt eine Sammlung von Load Balancer-Back-End-Adresspoolverweisen an, zu denen diese IP-Konfiguration der Netzwerkschnittstelle gehört.</span><span class="sxs-lookup"><span data-stu-id="8027b-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="8027b-134">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8027b-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="8027b-135">Gibt eine Sammlung von Load Balancer-Back-End-Adresspoolverweisen an, zu denen diese IP-Konfiguration der Netzwerkschnittstelle gehört.</span><span class="sxs-lookup"><span data-stu-id="8027b-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="8027b-136">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="8027b-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="8027b-137">Gibt eine Sammlung von eingehenden Nat Rule-Bezügen für den Lastenausgleich an, zu denen die IPConfiguration der Netzwerkschnittstelle gehört.</span><span class="sxs-lookup"><span data-stu-id="8027b-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

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

### <span data-ttu-id="8027b-138">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="8027b-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="8027b-139">Gibt eine Sammlung von NAT-Regelverweisen (Load Balancer Inbound Network Address Translation) an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="8027b-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="8027b-140">-Name</span><span class="sxs-lookup"><span data-stu-id="8027b-140">-Name</span></span>
<span data-ttu-id="8027b-141">Gibt den Namen der IP-Konfiguration der Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="8027b-141">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="8027b-142">-Primär</span><span class="sxs-lookup"><span data-stu-id="8027b-142">-Primary</span></span>
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

### <span data-ttu-id="8027b-143">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="8027b-143">-PrivateIpAddress</span></span>
<span data-ttu-id="8027b-144">Gibt die statische IP-Adresse der Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="8027b-144">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="8027b-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="8027b-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="8027b-146">Gibt die IP-Adressversion einer Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="8027b-146">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="8027b-147">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="8027b-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8027b-148">IPv4</span><span class="sxs-lookup"><span data-stu-id="8027b-148">IPv4</span></span>
- <span data-ttu-id="8027b-149">IPv6</span><span class="sxs-lookup"><span data-stu-id="8027b-149">IPv6</span></span>

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

### <span data-ttu-id="8027b-150">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8027b-150">-PublicIpAddress</span></span>
<span data-ttu-id="8027b-151">Gibt ein **PublicIPAddress-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="8027b-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="8027b-152">Dieses Cmdlet erstellt einen Verweis auf eine öffentliche IP-Adresse, die dieser IP-Konfiguration der Netzwerkschnittstelle zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8027b-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="8027b-153">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="8027b-153">-PublicIpAddressId</span></span>
<span data-ttu-id="8027b-154">Dieses Cmdlet erstellt einen Verweis auf eine öffentliche IP-Adresse, die dieser IP-Konfiguration der Netzwerkschnittstelle zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8027b-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="8027b-155">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="8027b-155">-Subnet</span></span>
<span data-ttu-id="8027b-156">Gibt ein **Subnetzobjekt** an.</span><span class="sxs-lookup"><span data-stu-id="8027b-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="8027b-157">Dieses Cmdlet erstellt einen Verweis auf ein Subnetz, in dem diese IP-Konfiguration der Netzwerkschnittstelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8027b-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="8027b-158">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8027b-158">-SubnetId</span></span>
<span data-ttu-id="8027b-159">Gibt einen Verweis auf ein Subnetz an, in dem diese IP-Konfiguration der Netzwerkschnittstelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8027b-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="8027b-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8027b-160">CommonParameters</span></span>
<span data-ttu-id="8027b-161">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8027b-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8027b-162">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8027b-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8027b-163">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8027b-163">INPUTS</span></span>

### <span data-ttu-id="8027b-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="8027b-164">System.String[]</span></span>

### <span data-ttu-id="8027b-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="8027b-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="8027b-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="8027b-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="8027b-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="8027b-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="8027b-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="8027b-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="8027b-169">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8027b-169">OUTPUTS</span></span>

### <span data-ttu-id="8027b-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8027b-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="8027b-171">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8027b-171">NOTES</span></span>
* <span data-ttu-id="8027b-172">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="8027b-172">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8027b-173">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8027b-173">RELATED LINKS</span></span>

[<span data-ttu-id="8027b-174">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8027b-174">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="8027b-175">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8027b-175">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="8027b-176">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8027b-176">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="8027b-177">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8027b-177">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
