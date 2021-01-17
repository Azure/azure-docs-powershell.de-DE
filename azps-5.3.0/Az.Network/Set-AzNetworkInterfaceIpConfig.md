---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 4c8dd4df4c3dd2d9aac8491b3d04e1755e6b4c38
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472158"
---
# <span data-ttu-id="104b9-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="104b9-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="104b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="104b9-102">SYNOPSIS</span></span>
<span data-ttu-id="104b9-103">Aktualisiert eine IP-Konfiguration für eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="104b9-103">Updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="104b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="104b9-104">SYNTAX</span></span>

### <span data-ttu-id="104b9-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="104b9-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="104b9-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="104b9-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="104b9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="104b9-107">DESCRIPTION</span></span>
<span data-ttu-id="104b9-108">Das **Cmdlet Set-AzNetworkInterfaceIpConfig** aktualisiert eine IP-Konfiguration für eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="104b9-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="104b9-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="104b9-109">EXAMPLES</span></span>

### <span data-ttu-id="104b9-110">1: Ändern der IP-Adresse einer IP-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="104b9-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="104b9-111">Die ersten beiden Befehle erhalten ein virtuelles Netzwerk namens myvnet und ein Subnetz namens mysubnet und speichern es in den Variablen $vnet und $subnet.</span><span class="sxs-lookup"><span data-stu-id="104b9-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="104b9-112">Der dritte Befehl ruft die Network Interface nic1 ab, die der IP-Konfiguration zugeordnet ist, die aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="104b9-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="104b9-113">Der dritte Befehl legt die private IP-Adresse der primären IP-Konfigurations-IPconfig1 auf 10.0.0.11 fest.</span><span class="sxs-lookup"><span data-stu-id="104b9-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="104b9-114">Schließlich aktualisiert der letzte Befehl die Netzwerkschnittstelle, um sicherzustellen, dass die Änderungen erfolgreich vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="104b9-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="104b9-115">2: Zuordnen einer IP-Konfiguration zu einer Anwendungssicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="104b9-115">2: Associating an IP configuration with an application security group</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="104b9-116">In diesem Beispiel enthält die variable $asg einen Verweis auf eine Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="104b9-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="104b9-117">Der vierte Befehl ruft die Netzwerkschnittstellen-nic1 ab, die der IP-Konfiguration zugeordnet ist, die aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="104b9-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="104b9-118">Die Set-AzNetworkInterfaceIpConfig legt die private IP-Adresse der primären IP-Konfigurations-Ipconfig1 auf 10.0.0.11 fest und erstellt eine Zuordnung zur abgerufenen Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="104b9-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="104b9-119">Schließlich aktualisiert der letzte Befehl die Netzwerkschnittstelle, um sicherzustellen, dass die Änderungen erfolgreich vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="104b9-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="104b9-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="104b9-120">PARAMETERS</span></span>

### <span data-ttu-id="104b9-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="104b9-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="104b9-122">Gibt eine Sammlung von Verweisen auf den Back-End-Adresspool des Anwendungsgateways an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="104b9-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="104b9-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="104b9-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="104b9-124">Gibt eine Sammlung von Verweisen auf den Back-End-Adresspool des Anwendungsgateways an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="104b9-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="104b9-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="104b9-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="104b9-126">Gibt eine Sammlung von Anwendungssicherheitsgruppeverweisen an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="104b9-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="104b9-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="104b9-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="104b9-128">Gibt eine Sammlung von Anwendungssicherheitsgruppeverweisen an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="104b9-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="104b9-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="104b9-129">-DefaultProfile</span></span>
<span data-ttu-id="104b9-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="104b9-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="104b9-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="104b9-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="104b9-132">Gibt eine Sammlung von Verweisen auf den Load Balancer-Back-End-Adresspool an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="104b9-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="104b9-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="104b9-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="104b9-134">Gibt eine Sammlung von Verweisen auf den Load Balancer-Back-End-Adresspool an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="104b9-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="104b9-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="104b9-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="104b9-136">Gibt eine Sammlung von Bezügen zur eingehenden Netzwerkadressenübersetzung (Network Address Translation, NAT) an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="104b9-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="104b9-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="104b9-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="104b9-138">Gibt eine Sammlung von eingehenden NAT-Regelverweisen für den Lastenausgleich an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="104b9-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="104b9-139">-Name</span><span class="sxs-lookup"><span data-stu-id="104b9-139">-Name</span></span>
<span data-ttu-id="104b9-140">Gibt den Namen der Netzwerk-IP-Konfiguration an, für die dieses Cmdlet festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="104b9-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="104b9-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="104b9-141">-NetworkInterface</span></span>
<span data-ttu-id="104b9-142">Gibt ein **"NetworkInterface"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="104b9-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="104b9-143">Dieses Cmdlet fügt dem von diesem Parameter angegebenen Objekt eine Netzwerkschnittstellen-IP-Konfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="104b9-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="104b9-144">-Primary</span><span class="sxs-lookup"><span data-stu-id="104b9-144">-Primary</span></span>
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

### <span data-ttu-id="104b9-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="104b9-145">-PrivateIpAddress</span></span>
<span data-ttu-id="104b9-146">Gibt die statische IP-Adresse der Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="104b9-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="104b9-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="104b9-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="104b9-148">Gibt die IP-Adressversion einer Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="104b9-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="104b9-149">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="104b9-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="104b9-150">IPv4</span><span class="sxs-lookup"><span data-stu-id="104b9-150">IPv4</span></span>
- <span data-ttu-id="104b9-151">IPv6</span><span class="sxs-lookup"><span data-stu-id="104b9-151">IPv6</span></span>

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

### <span data-ttu-id="104b9-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="104b9-152">-PublicIpAddress</span></span>
<span data-ttu-id="104b9-153">Gibt ein **PublicIPAddress-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="104b9-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="104b9-154">Dieses Cmdlet erstellt einen Verweis auf eine öffentliche IP-Adresse, die dieser Netzwerkschnittstellen-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="104b9-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="104b9-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="104b9-155">-PublicIpAddressId</span></span>
<span data-ttu-id="104b9-156">Dieses Cmdlet erstellt einen Verweis auf eine öffentliche IP-Adresse, die dieser Netzwerkschnittstellen-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="104b9-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="104b9-157">-Subnet</span><span class="sxs-lookup"><span data-stu-id="104b9-157">-Subnet</span></span>
<span data-ttu-id="104b9-158">Gibt ein **Subnetzobjekt** an.</span><span class="sxs-lookup"><span data-stu-id="104b9-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="104b9-159">Dieses Cmdlet erstellt einen Verweis auf ein Subnetz, in dem diese Netzwerkschnittstellen-IP-Konfiguration erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="104b9-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="104b9-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="104b9-160">-SubnetId</span></span>
<span data-ttu-id="104b9-161">Dieses Cmdlet erstellt einen Verweis auf ein Subnetz, in dem diese Netzwerkschnittstellen-IP-Konfiguration erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="104b9-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="104b9-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="104b9-162">CommonParameters</span></span>
<span data-ttu-id="104b9-163">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="104b9-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="104b9-164">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="104b9-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="104b9-165">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="104b9-165">INPUTS</span></span>

### <span data-ttu-id="104b9-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="104b9-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="104b9-167">System.String[]</span><span class="sxs-lookup"><span data-stu-id="104b9-167">System.String[]</span></span>

### <span data-ttu-id="104b9-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="104b9-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="104b9-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="104b9-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="104b9-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="104b9-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="104b9-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="104b9-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="104b9-172">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="104b9-172">OUTPUTS</span></span>

### <span data-ttu-id="104b9-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="104b9-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="104b9-174">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="104b9-174">NOTES</span></span>
* <span data-ttu-id="104b9-175">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="104b9-175">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="104b9-176">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="104b9-176">RELATED LINKS</span></span>

[<span data-ttu-id="104b9-177">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="104b9-177">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="104b9-178">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="104b9-178">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="104b9-179">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="104b9-179">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="104b9-180">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="104b9-180">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)
