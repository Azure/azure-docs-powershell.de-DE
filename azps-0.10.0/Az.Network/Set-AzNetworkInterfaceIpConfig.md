---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 0e74aa06d2966ed4e907de7428ddc1f4d3a6f2cb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843608"
---
# <span data-ttu-id="ace18-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ace18-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="ace18-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ace18-102">SYNOPSIS</span></span>
<span data-ttu-id="ace18-103">Legt den Zielstatus für eine Azure-Netzwerkschnittstellen-IP-Konfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="ace18-103">Sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="ace18-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ace18-104">SYNTAX</span></span>

### <span data-ttu-id="ace18-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="ace18-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ace18-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ace18-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ace18-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ace18-107">DESCRIPTION</span></span>
<span data-ttu-id="ace18-108">Das Cmdlet " **Set-AzNetworkInterfaceIpConfig** " legt den Zielstatus für eine Azure-Netzwerkschnittstellen-IP-Konfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="ace18-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="ace18-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ace18-109">EXAMPLES</span></span>

### <span data-ttu-id="ace18-110">1: Ändern der IP-Adresse einer IP-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="ace18-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="ace18-111">Die ersten beiden Befehle erhalten ein virtuelles Netzwerk namens myvnet und ein Subnetz namens mysubnet und speichern es in den Variablen $vnet und $Subnet.</span><span class="sxs-lookup"><span data-stu-id="ace18-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="ace18-112">Der dritte Befehl ruft die Netzwerkschnittstellen-NIC1 ab, die der IP-Konfiguration zugeordnet ist, die aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="ace18-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="ace18-113">Der dritte Befehl legt die private IP-Adresse der primären IP-Konfigurations ipconfig1 auf 10.0.0.11 fest.</span><span class="sxs-lookup"><span data-stu-id="ace18-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="ace18-114">Schließlich aktualisiert der letzte Befehl die Netzwerkschnittstelle, um sicherzustellen, dass die Änderungen erfolgreich durchgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="ace18-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="ace18-115">2: Zuordnen einer IP-Konfiguration zu einem Application Security groupp</span><span class="sxs-lookup"><span data-stu-id="ace18-115">2: Associating an IP configuration with an applicaiton security groupp</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="ace18-116">In diesem Beispiel enthält die Variable $ASG einen Verweis auf eine Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="ace18-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="ace18-117">Der vierte Befehl ruft die Netzwerkschnittstellen-NIC1 ab, die der IP-Konfiguration zugeordnet ist, die aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="ace18-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="ace18-118">Die Set-AzNetworkInterfaceIpConfig legt die private IP-Adresse des primären IP-Konfigurations ipconfig1 auf 10.0.0.11 fest und erstellt eine Zuordnung mit der abgerufenen Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="ace18-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="ace18-119">Schließlich aktualisiert der letzte Befehl die Netzwerkschnittstelle, um sicherzustellen, dass die Änderungen erfolgreich durchgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="ace18-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="ace18-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="ace18-120">PARAMETERS</span></span>

### <span data-ttu-id="ace18-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ace18-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="ace18-122">Gibt eine Sammlung von Anwendungsgateway-Back-End-Adresspool verweisen an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="ace18-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace18-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="ace18-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="ace18-124">Gibt eine Sammlung von Anwendungsgateway-Back-End-Adresspool verweisen an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="ace18-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace18-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ace18-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="ace18-126">Gibt eine Sammlung von Anwendungs Sicherheitsgruppen verweisen an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="ace18-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace18-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="ace18-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="ace18-128">Gibt eine Sammlung von Anwendungs Sicherheitsgruppen verweisen an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="ace18-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace18-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ace18-129">-DefaultProfile</span></span>
<span data-ttu-id="ace18-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ace18-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ace18-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ace18-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="ace18-132">Gibt eine Sammlung von Quellen des Load Balancer-Back-End-Adresspools an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="ace18-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace18-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="ace18-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="ace18-134">Gibt eine Sammlung von Quellen des Load Balancer-Back-End-Adresspools an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="ace18-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace18-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="ace18-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="ace18-136">Gibt eine Sammlung von NAT-Regel Bezügen (eingehende Netzwerkadressübersetzung) für den Lastenausgleich an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="ace18-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace18-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="ace18-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="ace18-138">Gibt eine Sammlung von eingehenden NAT-Regel Bezügen für das Load Balancer an, zu denen diese Netzwerkschnittstellen-IP-Konfiguration gehört.</span><span class="sxs-lookup"><span data-stu-id="ace18-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace18-139">-Name</span><span class="sxs-lookup"><span data-stu-id="ace18-139">-Name</span></span>
<span data-ttu-id="ace18-140">Gibt den Namen der Netzwerk-IP-Konfiguration an, für die dieses Cmdlet festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ace18-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ace18-141">-Network Interface</span><span class="sxs-lookup"><span data-stu-id="ace18-141">-NetworkInterface</span></span>
<span data-ttu-id="ace18-142">Gibt ein **Network Interface** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ace18-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="ace18-143">Mit diesem Cmdlet wird dem Objekt, das dieser Parameter angibt, eine Netzwerkschnittstellen-IP-Konfiguration hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ace18-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ace18-144">– Primär</span><span class="sxs-lookup"><span data-stu-id="ace18-144">-Primary</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ace18-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="ace18-145">-PrivateIpAddress</span></span>
<span data-ttu-id="ace18-146">Gibt die statische IP-Adresse der Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="ace18-146">Specifies the static IP address of the network interface IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ace18-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="ace18-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="ace18-148">Gibt die IP-Adressenversion einer Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="ace18-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="ace18-149">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ace18-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ace18-150">IPv4</span><span class="sxs-lookup"><span data-stu-id="ace18-150">IPv4</span></span>
- <span data-ttu-id="ace18-151">IPv6</span><span class="sxs-lookup"><span data-stu-id="ace18-151">IPv6</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ace18-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ace18-152">-PublicIpAddress</span></span>
<span data-ttu-id="ace18-153">Gibt ein **PublicIPAddress** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ace18-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="ace18-154">Dieses Cmdlet erstellt einen Verweis auf eine öffentliche IP-Adresse, die dieser Netzwerkschnittstellen-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ace18-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ace18-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="ace18-155">-PublicIpAddressId</span></span>
<span data-ttu-id="ace18-156">Dieses Cmdlet erstellt einen Verweis auf eine öffentliche IP-Adresse, die dieser Netzwerkschnittstellen-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ace18-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ace18-157">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="ace18-157">-Subnet</span></span>
<span data-ttu-id="ace18-158">Gibt ein **Subnetz** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ace18-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="ace18-159">Dieses Cmdlet erstellt einen Verweis auf ein Subnetz, in dem diese Netzwerkschnittstellen-IP-Konfiguration erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ace18-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ace18-160">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="ace18-160">-SubnetId</span></span>
<span data-ttu-id="ace18-161">Dieses Cmdlet erstellt einen Verweis auf ein Subnetz, in dem diese Netzwerkschnittstellen-IP-Konfiguration erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ace18-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ace18-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ace18-162">CommonParameters</span></span>
<span data-ttu-id="ace18-163">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ace18-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ace18-164">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ace18-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ace18-165">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ace18-165">INPUTS</span></span>

### <span data-ttu-id="ace18-166">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ace18-166">PSNetworkInterface</span></span>
<span data-ttu-id="ace18-167">Der Parameter "Network Interface" akzeptiert den Wert vom Typ "PSNetworkInterface" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ace18-167">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="ace18-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ace18-168">OUTPUTS</span></span>

### <span data-ttu-id="ace18-169">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ace18-169">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="ace18-170">Notizen</span><span class="sxs-lookup"><span data-stu-id="ace18-170">NOTES</span></span>
* <span data-ttu-id="ace18-171">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="ace18-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ace18-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ace18-172">RELATED LINKS</span></span>

[<span data-ttu-id="ace18-173">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ace18-173">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ace18-174">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ace18-174">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ace18-175">Neu – AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ace18-175">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ace18-176">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ace18-176">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)


