---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 80ffb0adf7703553d22cf991ad84a1af3b8e229c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173210"
---
# <span data-ttu-id="33d07-101">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="33d07-101">New-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="33d07-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="33d07-102">SYNOPSIS</span></span>
<span data-ttu-id="33d07-103">Erstellt eine Netzwerkschnittstellen-IP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="33d07-103">Creates a network interface IP configuration.</span></span>

## <span data-ttu-id="33d07-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="33d07-104">SYNTAX</span></span>

### <span data-ttu-id="33d07-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="33d07-105">SetByResource (Default)</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="33d07-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="33d07-106">SetByResourceId</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33d07-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="33d07-107">DESCRIPTION</span></span>
<span data-ttu-id="33d07-108">Das Cmdlet **New-AzNetworkInterfaceIpConfig** erstellt eine Azure-Netzwerkschnittstellen-IP-Konfiguration für eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="33d07-108">The **New-AzNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="33d07-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33d07-109">EXAMPLES</span></span>

### <span data-ttu-id="33d07-110">1: Erstellen einer IP-Konfiguration mit einer öffentlichen IP-Adresse für eine Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="33d07-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="33d07-111">Die ersten beiden Befehle erhalten ein virtuelles Netzwerk namens myvnet und ein Subnetz mit dem Namen "mysubnet", das zuvor erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="33d07-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="33d07-112">Diese werden in $vnet und $Subnet gespeichert.</span><span class="sxs-lookup"><span data-stu-id="33d07-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="33d07-113">Der dritte Befehl ruft eine zuvor erstellte öffentliche IP-Adresse mit dem Namen PIP1 ab.</span><span class="sxs-lookup"><span data-stu-id="33d07-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="33d07-114">Der Befehl Forth erstellt eine neue IP-Konfiguration mit dem Namen "ipconfig-1" als primäre IP-Konfiguration mit einer zugehörigen öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="33d07-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="33d07-115">Der letzte Befehl erstellt dann mithilfe dieser IP-Konfiguration eine Netzwerkschnittstelle namens mynic1.</span><span class="sxs-lookup"><span data-stu-id="33d07-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="33d07-116">2: Erstellen einer IP-Konfiguration mit einer privaten IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="33d07-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="33d07-117">Die ersten beiden Befehle erhalten ein virtuelles Netzwerk namens myvnet und ein Subnetz mit dem Namen "mysubnet", das zuvor erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="33d07-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="33d07-118">Diese werden in $vnet und $Subnet gespeichert.</span><span class="sxs-lookup"><span data-stu-id="33d07-118">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="33d07-119">Der dritte Befehl erstellt eine neue IP-Konfiguration mit dem Namen "ipconfig-2" mit einer privaten IP-Adresse, die 10.0.0.5 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="33d07-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="33d07-120">Der letzte Befehl erstellt dann mithilfe dieser IP-Konfiguration eine Netzwerkschnittstelle namens mynic1.</span><span class="sxs-lookup"><span data-stu-id="33d07-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="33d07-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="33d07-121">PARAMETERS</span></span>

### <span data-ttu-id="33d07-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="33d07-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="33d07-123">Gibt eine Sammlung von Anwendungsgateway-Back-End-Adresspool verweisen an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="33d07-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="33d07-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="33d07-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="33d07-125">Gibt eine Sammlung von Anwendungsgateway-Back-End-Adresspool verweisen an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="33d07-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="33d07-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="33d07-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="33d07-127">Gibt eine Sammlung von Anwendungs Sicherheitsgruppen verweisen an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="33d07-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="33d07-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="33d07-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="33d07-129">Gibt eine Sammlung von Anwendungs Sicherheitsgruppen verweisen an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="33d07-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="33d07-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d07-130">-DefaultProfile</span></span>
<span data-ttu-id="33d07-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="33d07-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33d07-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="33d07-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="33d07-133">Gibt eine Sammlung von Quellen des Load Balancer-Back-End-Adresspools an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="33d07-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="33d07-134">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="33d07-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="33d07-135">Gibt eine Sammlung von Quellen des Load Balancer-Back-End-Adresspools an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="33d07-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="33d07-136">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="33d07-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="33d07-137">Gibt eine Sammlung von eingehenden NAT-Regel Bezügen für das Load Balancer an, zu denen diese Netzwerkschnittstellen-IPKonfigurationsdateiAddress gehört.</span><span class="sxs-lookup"><span data-stu-id="33d07-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

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

### <span data-ttu-id="33d07-138">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="33d07-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="33d07-139">Gibt eine Sammlung von NAT-Regel Bezügen (eingehende Netzwerkadressübersetzung) für den Lastenausgleich an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="33d07-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="33d07-140">-Name</span><span class="sxs-lookup"><span data-stu-id="33d07-140">-Name</span></span>
<span data-ttu-id="33d07-141">Gibt den Namen der Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="33d07-141">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="33d07-142">– Primär</span><span class="sxs-lookup"><span data-stu-id="33d07-142">-Primary</span></span>
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

### <span data-ttu-id="33d07-143">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="33d07-143">-PrivateIpAddress</span></span>
<span data-ttu-id="33d07-144">Gibt die statische IP-Adresse der Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="33d07-144">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="33d07-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="33d07-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="33d07-146">Gibt die IP-Adressenversion einer Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="33d07-146">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="33d07-147">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="33d07-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="33d07-148">IPv4</span><span class="sxs-lookup"><span data-stu-id="33d07-148">IPv4</span></span>
- <span data-ttu-id="33d07-149">IPv6</span><span class="sxs-lookup"><span data-stu-id="33d07-149">IPv6</span></span>

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

### <span data-ttu-id="33d07-150">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="33d07-150">-PublicIpAddress</span></span>
<span data-ttu-id="33d07-151">Gibt ein **PublicIPAddress** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="33d07-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="33d07-152">Dieses Cmdlet erstellt einen Verweis auf eine öffentliche IP-Adresse, die dieser Netzwerkschnittstellen-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="33d07-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="33d07-153">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="33d07-153">-PublicIpAddressId</span></span>
<span data-ttu-id="33d07-154">Dieses Cmdlet erstellt einen Verweis auf eine öffentliche IP-Adresse, die dieser Netzwerkschnittstellen-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="33d07-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="33d07-155">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="33d07-155">-Subnet</span></span>
<span data-ttu-id="33d07-156">Gibt ein **Subnetz** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="33d07-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="33d07-157">Dieses Cmdlet erstellt einen Verweis auf ein Subnetz, in dem diese Netzwerkschnittstellen-IP-Konfiguration erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="33d07-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="33d07-158">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="33d07-158">-SubnetId</span></span>
<span data-ttu-id="33d07-159">Gibt einen Verweis auf ein Subnetz an, in dem diese Netzwerkschnittstellen-IP-Konfiguration erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="33d07-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="33d07-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d07-160">CommonParameters</span></span>
<span data-ttu-id="33d07-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33d07-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d07-162">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33d07-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d07-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="33d07-163">INPUTS</span></span>

### <span data-ttu-id="33d07-164">System. String []</span><span class="sxs-lookup"><span data-stu-id="33d07-164">System.String[]</span></span>

### <span data-ttu-id="33d07-165">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="33d07-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="33d07-166">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="33d07-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="33d07-167">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="33d07-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="33d07-168">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="33d07-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="33d07-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="33d07-169">OUTPUTS</span></span>

### <span data-ttu-id="33d07-170">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="33d07-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="33d07-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="33d07-171">NOTES</span></span>
* <span data-ttu-id="33d07-172">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="33d07-172">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="33d07-173">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="33d07-173">RELATED LINKS</span></span>

[<span data-ttu-id="33d07-174">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="33d07-174">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="33d07-175">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="33d07-175">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="33d07-176">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="33d07-176">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="33d07-177">Satz-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="33d07-177">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
