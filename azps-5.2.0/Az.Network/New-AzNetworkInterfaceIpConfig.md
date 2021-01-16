---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 80ffb0adf7703553d22cf991ad84a1af3b8e229c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298320"
---
# <span data-ttu-id="0e5fa-101">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e5fa-101">New-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="0e5fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e5fa-102">SYNOPSIS</span></span>
<span data-ttu-id="0e5fa-103">Erstellt eine IP-Konfiguration der Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-103">Creates a network interface IP configuration.</span></span>

## <span data-ttu-id="0e5fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e5fa-104">SYNTAX</span></span>

### <span data-ttu-id="0e5fa-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="0e5fa-105">SetByResource (Default)</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e5fa-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0e5fa-106">SetByResourceId</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e5fa-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e5fa-107">DESCRIPTION</span></span>
<span data-ttu-id="0e5fa-108">Das **Cmdlet "New-AzNetworkInterfaceIpConfig"** erstellt eine IP-Konfiguration der Azure-Netzwerkschnittstelle für eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-108">The **New-AzNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="0e5fa-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0e5fa-109">EXAMPLES</span></span>

### <span data-ttu-id="0e5fa-110">1: Erstellen einer IP-Konfiguration mit einer öffentlichen IP-Adresse für eine Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="0e5fa-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="0e5fa-111">Die ersten beiden Befehle erhalten ein virtuelles Netzwerk namens "myvnet" bzw. ein Subnetz namens "mysubnet", das zuvor erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="0e5fa-112">Diese werden in $vnet bzw. $Subnet gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="0e5fa-113">Der dritte Befehl ruft eine zuvor erstellte öffentliche IP-Adresse namens PIP1 ab.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="0e5fa-114">Der vierte Befehl erstellt eine neue IP-Konfiguration namens "IPConfig-1" als primäre IP-Konfiguration mit einer ihm zugeordneten öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="0e5fa-115">Der letzte Befehl erstellt dann mithilfe dieser IP-Konfiguration eine Netzwerkschnittstelle namens Mynic1.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="0e5fa-116">2: Erstellen einer IP-Konfiguration mit einer privaten IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="0e5fa-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="0e5fa-117">Die ersten beiden Befehle erhalten ein virtuelles Netzwerk namens "myvnet" bzw. ein Subnetz namens "mysubnet", das zuvor erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="0e5fa-118">Diese werden in $vnet bzw. $Subnet gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-118">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="0e5fa-119">Mit dem dritten Befehl wird eine neue IP-Konfiguration namens "IPConfig-2" erstellt, der eine private IP-Adresse 10.0.0.5 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="0e5fa-120">Der letzte Befehl erstellt dann mithilfe dieser IP-Konfiguration eine Netzwerkschnittstelle namens Mynic1.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="0e5fa-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e5fa-121">PARAMETERS</span></span>

### <span data-ttu-id="0e5fa-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0e5fa-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="0e5fa-123">Gibt eine Sammlung von Verweisen auf den Back-End-Adresspool des Anwendungsgateways an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="0e5fa-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="0e5fa-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="0e5fa-125">Gibt eine Sammlung von Verweisen auf den Back-End-Adresspool des Anwendungsgateways an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="0e5fa-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0e5fa-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="0e5fa-127">Gibt eine Sammlung von Anwendungssicherheitsgruppeverweisen an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="0e5fa-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="0e5fa-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="0e5fa-129">Gibt eine Sammlung von Anwendungssicherheitsgruppeverweisen an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="0e5fa-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e5fa-130">-DefaultProfile</span></span>
<span data-ttu-id="0e5fa-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e5fa-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0e5fa-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="0e5fa-133">Gibt eine Sammlung von Verweisen auf den Load Balancer-Back-End-Adresspool an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="0e5fa-134">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="0e5fa-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="0e5fa-135">Gibt eine Sammlung von Verweisen auf den Load Balancer-Back-End-Adresspool an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="0e5fa-136">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="0e5fa-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="0e5fa-137">Gibt eine Sammlung von eingehenden Nat-Regel-Bezügen für den Lastenausgleich an, zu denen die IPConfiguration der Netzwerkschnittstelle gehört.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

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

### <span data-ttu-id="0e5fa-138">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="0e5fa-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="0e5fa-139">Gibt eine Sammlung von Bezügen zur eingehenden Netzwerkadressenübersetzung (Network Address Translation, NAT) an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="0e5fa-140">-Name</span><span class="sxs-lookup"><span data-stu-id="0e5fa-140">-Name</span></span>
<span data-ttu-id="0e5fa-141">Gibt den Namen der Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-141">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="0e5fa-142">-Primary</span><span class="sxs-lookup"><span data-stu-id="0e5fa-142">-Primary</span></span>
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

### <span data-ttu-id="0e5fa-143">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="0e5fa-143">-PrivateIpAddress</span></span>
<span data-ttu-id="0e5fa-144">Gibt die statische IP-Adresse der Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-144">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="0e5fa-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="0e5fa-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="0e5fa-146">Gibt die IP-Adressversion einer Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-146">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="0e5fa-147">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="0e5fa-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0e5fa-148">IPv4</span><span class="sxs-lookup"><span data-stu-id="0e5fa-148">IPv4</span></span>
- <span data-ttu-id="0e5fa-149">IPv6</span><span class="sxs-lookup"><span data-stu-id="0e5fa-149">IPv6</span></span>

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

### <span data-ttu-id="0e5fa-150">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0e5fa-150">-PublicIpAddress</span></span>
<span data-ttu-id="0e5fa-151">Gibt ein **PublicIPAddress-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="0e5fa-152">Dieses Cmdlet erstellt einen Verweis auf eine öffentliche IP-Adresse, die dieser Netzwerkschnittstellen-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="0e5fa-153">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="0e5fa-153">-PublicIpAddressId</span></span>
<span data-ttu-id="0e5fa-154">Dieses Cmdlet erstellt einen Verweis auf eine öffentliche IP-Adresse, die dieser Netzwerkschnittstellen-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="0e5fa-155">-Subnet</span><span class="sxs-lookup"><span data-stu-id="0e5fa-155">-Subnet</span></span>
<span data-ttu-id="0e5fa-156">Gibt ein **Subnetzobjekt** an.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="0e5fa-157">Dieses Cmdlet erstellt einen Verweis auf ein Subnetz, in dem diese Netzwerkschnittstellen-IP-Konfiguration erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="0e5fa-158">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0e5fa-158">-SubnetId</span></span>
<span data-ttu-id="0e5fa-159">Gibt einen Verweis auf ein Subnetz an, in dem diese Netzwerkschnittstellen-IP-Konfiguration erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="0e5fa-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e5fa-160">CommonParameters</span></span>
<span data-ttu-id="0e5fa-161">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e5fa-162">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e5fa-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e5fa-163">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0e5fa-163">INPUTS</span></span>

### <span data-ttu-id="0e5fa-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0e5fa-164">System.String[]</span></span>

### <span data-ttu-id="0e5fa-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="0e5fa-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="0e5fa-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="0e5fa-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="0e5fa-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="0e5fa-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="0e5fa-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="0e5fa-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="0e5fa-169">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0e5fa-169">OUTPUTS</span></span>

### <span data-ttu-id="0e5fa-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e5fa-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="0e5fa-171">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0e5fa-171">NOTES</span></span>
* <span data-ttu-id="0e5fa-172">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="0e5fa-172">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="0e5fa-173">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0e5fa-173">RELATED LINKS</span></span>

[<span data-ttu-id="0e5fa-174">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e5fa-174">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="0e5fa-175">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e5fa-175">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="0e5fa-176">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e5fa-176">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="0e5fa-177">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e5fa-177">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
