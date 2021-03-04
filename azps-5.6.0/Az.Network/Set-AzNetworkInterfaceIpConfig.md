---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 9427a79c607d56fcc9ce7a39fa24bfa3e301cfc8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944855"
---
# <span data-ttu-id="43668-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="43668-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="43668-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43668-102">SYNOPSIS</span></span>
<span data-ttu-id="43668-103">Aktualisiert eine IP-Konfiguration für eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="43668-103">Updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="43668-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43668-104">SYNTAX</span></span>

### <span data-ttu-id="43668-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="43668-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43668-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="43668-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43668-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43668-107">DESCRIPTION</span></span>
<span data-ttu-id="43668-108">Das **Cmdlet Set-AzNetworkInterfaceIpConfig** aktualisiert eine IP-Konfiguration für eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="43668-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="43668-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="43668-109">EXAMPLES</span></span>

### <span data-ttu-id="43668-110">1: Ändern der IP-Adresse einer IP-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="43668-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="43668-111">Die ersten beiden Befehle erhalten ein virtuelles Netzwerk namens myvnet und ein Subnetz namens mysubnet und speichern es in den Variablen $vnet und $subnet.</span><span class="sxs-lookup"><span data-stu-id="43668-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="43668-112">Der dritte Befehl ruft die Netzwerkschnittstelle nic1 ab, die der IP-Konfiguration zugeordnet ist, die aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="43668-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="43668-113">Der dritte Befehl legt die private IP-Adresse der primären IP-Konfiguration ipconfig1 auf 10.0.0.11 fest.</span><span class="sxs-lookup"><span data-stu-id="43668-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="43668-114">Schließlich aktualisiert der letzte Befehl die Netzwerkschnittstelle, um sicherzustellen, dass die Änderungen erfolgreich vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="43668-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="43668-115">2: Zuordnen einer IP-Konfiguration zu einer Anwendungssicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="43668-115">2: Associating an IP configuration with an application security group</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="43668-116">In diesem Beispiel enthält die Variable $asg einen Verweis auf eine Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="43668-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="43668-117">Der vierte Befehl ruft die Netzwerkschnittstelle nic1 ab, die der IP-Konfiguration zugeordnet ist, die aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="43668-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="43668-118">Die Set-AzNetworkInterfaceIpConfig legt die private IP-Adresse der primären IP-Konfiguration ipconfig1 auf 10.0.0.11 fest und erstellt eine Zuordnung mit der abgerufenen Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="43668-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="43668-119">Schließlich aktualisiert der letzte Befehl die Netzwerkschnittstelle, um sicherzustellen, dass die Änderungen erfolgreich vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="43668-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="43668-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="43668-120">PARAMETERS</span></span>

### <span data-ttu-id="43668-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="43668-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="43668-122">Gibt eine Sammlung von Anwendungsgateway-Back-End-Adresspoolverweisen an, zu denen diese NETZWERKSCHNITTSTELLEN-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="43668-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="43668-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="43668-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="43668-124">Gibt eine Sammlung von Anwendungsgateway-Back-End-Adresspoolverweisen an, zu denen diese NETZWERKSCHNITTSTELLEN-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="43668-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="43668-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="43668-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="43668-126">Gibt eine Sammlung von Anwendungssicherheitsgruppeverweisen an, zu denen diese IP-Konfiguration der Netzwerkschnittstelle gehört.</span><span class="sxs-lookup"><span data-stu-id="43668-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="43668-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="43668-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="43668-128">Gibt eine Sammlung von Anwendungssicherheitsgruppeverweisen an, zu denen diese IP-Konfiguration der Netzwerkschnittstelle gehört.</span><span class="sxs-lookup"><span data-stu-id="43668-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="43668-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43668-129">-DefaultProfile</span></span>
<span data-ttu-id="43668-130">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43668-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43668-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="43668-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="43668-132">Gibt eine Sammlung von Load Balancer-Back-End-Adresspoolverweisen an, zu denen diese IP-Konfiguration der Netzwerkschnittstelle gehört.</span><span class="sxs-lookup"><span data-stu-id="43668-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="43668-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="43668-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="43668-134">Gibt eine Sammlung von Load Balancer-Back-End-Adresspoolverweisen an, zu denen diese IP-Konfiguration der Netzwerkschnittstelle gehört.</span><span class="sxs-lookup"><span data-stu-id="43668-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="43668-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="43668-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="43668-136">Gibt eine Sammlung von NAT-Regelverweisen (Load Balancer Inbound Network Address Translation) an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="43668-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="43668-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="43668-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="43668-138">Gibt eine Sammlung von Bezügen der eingehenden NAT-Regel für den Lastenausgleich an, zu denen diese IP-Konfiguration der Netzwerkschnittstelle gehört.</span><span class="sxs-lookup"><span data-stu-id="43668-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="43668-139">-Name</span><span class="sxs-lookup"><span data-stu-id="43668-139">-Name</span></span>
<span data-ttu-id="43668-140">Gibt den Namen der Netzwerk-IP-Konfiguration an, für die dieses Cmdlet festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="43668-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="43668-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="43668-141">-NetworkInterface</span></span>
<span data-ttu-id="43668-142">Gibt ein **NetworkInterface-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="43668-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="43668-143">Dieses Cmdlet fügt dem von diesem Parameter angegebenen Objekt eine IP-Konfiguration der Netzwerkschnittstelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="43668-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="43668-144">-Primär</span><span class="sxs-lookup"><span data-stu-id="43668-144">-Primary</span></span>
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

### <span data-ttu-id="43668-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="43668-145">-PrivateIpAddress</span></span>
<span data-ttu-id="43668-146">Gibt die statische IP-Adresse der Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="43668-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="43668-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="43668-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="43668-148">Gibt die IP-Adressversion einer Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="43668-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="43668-149">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="43668-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="43668-150">IPv4</span><span class="sxs-lookup"><span data-stu-id="43668-150">IPv4</span></span>
- <span data-ttu-id="43668-151">IPv6</span><span class="sxs-lookup"><span data-stu-id="43668-151">IPv6</span></span>

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

### <span data-ttu-id="43668-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="43668-152">-PublicIpAddress</span></span>
<span data-ttu-id="43668-153">Gibt ein **PublicIPAddress-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="43668-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="43668-154">Dieses Cmdlet erstellt einen Verweis auf eine öffentliche IP-Adresse, die dieser IP-Konfiguration der Netzwerkschnittstelle zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43668-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="43668-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="43668-155">-PublicIpAddressId</span></span>
<span data-ttu-id="43668-156">Dieses Cmdlet erstellt einen Verweis auf eine öffentliche IP-Adresse, die dieser IP-Konfiguration der Netzwerkschnittstelle zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43668-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="43668-157">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="43668-157">-Subnet</span></span>
<span data-ttu-id="43668-158">Gibt ein **Subnetzobjekt** an.</span><span class="sxs-lookup"><span data-stu-id="43668-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="43668-159">Dieses Cmdlet erstellt einen Verweis auf ein Subnetz, in dem diese IP-Konfiguration der Netzwerkschnittstelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="43668-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="43668-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="43668-160">-SubnetId</span></span>
<span data-ttu-id="43668-161">Dieses Cmdlet erstellt einen Verweis auf ein Subnetz, in dem diese IP-Konfiguration der Netzwerkschnittstelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="43668-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="43668-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43668-162">CommonParameters</span></span>
<span data-ttu-id="43668-163">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43668-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43668-164">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43668-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43668-165">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="43668-165">INPUTS</span></span>

### <span data-ttu-id="43668-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="43668-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="43668-167">System.String[]</span><span class="sxs-lookup"><span data-stu-id="43668-167">System.String[]</span></span>

### <span data-ttu-id="43668-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="43668-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="43668-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="43668-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="43668-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="43668-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="43668-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="43668-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="43668-172">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="43668-172">OUTPUTS</span></span>

### <span data-ttu-id="43668-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="43668-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="43668-174">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="43668-174">NOTES</span></span>
* <span data-ttu-id="43668-175">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="43668-175">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="43668-176">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="43668-176">RELATED LINKS</span></span>

[<span data-ttu-id="43668-177">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="43668-177">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="43668-178">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="43668-178">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="43668-179">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="43668-179">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="43668-180">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="43668-180">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)
