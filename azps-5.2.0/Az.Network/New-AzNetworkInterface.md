---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: 23d0b2eacb5e4053cbed2c08101e225d861311de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298328"
---
# <span data-ttu-id="e17bc-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e17bc-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="e17bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e17bc-102">SYNOPSIS</span></span>
<span data-ttu-id="e17bc-103">Erstellt eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e17bc-103">Creates a network interface.</span></span>

## <span data-ttu-id="e17bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e17bc-104">SYNTAX</span></span>

### <span data-ttu-id="e17bc-105">SetByIpConfigurationResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="e17bc-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e17bc-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="e17bc-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e17bc-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e17bc-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e17bc-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e17bc-108">SetByResource</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>] [-EnableIPForwarding]
 [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e17bc-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e17bc-109">DESCRIPTION</span></span>
<span data-ttu-id="e17bc-110">Das **Cmdlet "New-AzNetworkInterface"** erstellt eine Azure-Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e17bc-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="e17bc-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e17bc-111">EXAMPLES</span></span>

### <span data-ttu-id="e17bc-112">Beispiel 1: Erstellen einer Azure-Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="e17bc-112">Example 1: Create an Azure network interface</span></span>
```powershell
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="e17bc-113">Mit diesem Befehl wird eine Netzwerkschnittstelle namens "NetworkInterface001" mit einer dynamisch zugewiesenen privaten IP-Adresse aus Subnetz1 im virtuellen Netzwerk namens "VirtualNetwork1" erstellt.</span><span class="sxs-lookup"><span data-stu-id="e17bc-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="e17bc-114">Der Befehl weist der Netzwerkschnittstelle außerdem zwei DNS-Server zu.</span><span class="sxs-lookup"><span data-stu-id="e17bc-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="e17bc-115">Die untergeordnete Ressource "IPConfiguration" wird automatisch unter dem Namen "IPConfiguration1" erstellt.</span><span class="sxs-lookup"><span data-stu-id="e17bc-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="e17bc-116">Beispiel 2: Erstellen einer Azure-Netzwerkschnittstelle mit einem IP-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="e17bc-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```powershell
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="e17bc-117">In diesem Beispiel wird mithilfe eines IP-Konfigurationsobjekts eine neue Netzwerkschnittstelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="e17bc-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="e17bc-118">Das IP-Konfigurationsobjekt gibt eine statische private IPv4-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="e17bc-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="e17bc-119">Der erste Befehl ruft ein vorhandenes angegebenes virtuelles Netzwerk ab, das zum Zuweisen des Subnetzes im zweiten Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e17bc-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="e17bc-120">Der zweite Befehl erstellt eine Netzwerkschnittstellen-IP-Konfiguration namens IPConfig1 und speichert die Konfiguration in der Variablen namens $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="e17bc-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="e17bc-121">Der dritte Befehl erstellt eine Netzwerkschnittstelle namens "NetworkInterface1", die die in der Variablen namens "netzwerkinterface1" gespeicherte Netzwerkschnittstellen-IP-Konfiguration $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="e17bc-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

### <span data-ttu-id="e17bc-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e17bc-122">Example 3</span></span>

<span data-ttu-id="e17bc-123">Erstellt eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e17bc-123">Creates a network interface.</span></span> <span data-ttu-id="e17bc-124">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="e17bc-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzNetworkInterface -Location 'West US' -Name 'NetworkInterface1' -PrivateIpAddress '10.0.1.10' -ResourceGroupName 'ResourceGroup1' -SubnetId '/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1'
```

## <span data-ttu-id="e17bc-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e17bc-125">PARAMETERS</span></span>

### <span data-ttu-id="e17bc-126">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e17bc-126">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="e17bc-127">Gibt ein **ApplicationGatewayBackendAddressPool-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="e17bc-127">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="e17bc-128">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e17bc-128">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="e17bc-129">Gibt die ID eines **ApplicationGatewayBackendAddressPool-Objekts** an.</span><span class="sxs-lookup"><span data-stu-id="e17bc-129">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="e17bc-130">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e17bc-130">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="e17bc-131">Gibt eine Sammlung von Anwendungssicherheitsgruppeverweisen an, zu denen die Netzwerkschnittstellen-IP-Konfiguration gehören soll.</span><span class="sxs-lookup"><span data-stu-id="e17bc-131">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="e17bc-132">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e17bc-132">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="e17bc-133">Gibt eine Sammlung von Anwendungssicherheitsgruppeverweisen an, zu denen die Netzwerkschnittstellen-IP-Konfiguration gehören soll.</span><span class="sxs-lookup"><span data-stu-id="e17bc-133">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="e17bc-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e17bc-134">-AsJob</span></span>
<span data-ttu-id="e17bc-135">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e17bc-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e17bc-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e17bc-136">-DefaultProfile</span></span>
<span data-ttu-id="e17bc-137">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e17bc-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e17bc-138">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="e17bc-138">-DnsServer</span></span>
<span data-ttu-id="e17bc-139">Gibt den DNS-Server für die Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="e17bc-139">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="e17bc-140">-EnableAcce 2010Networking</span><span class="sxs-lookup"><span data-stu-id="e17bc-140">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="e17bc-141">Ermöglicht eine beschleunigte Netzwerkverbindung.</span><span class="sxs-lookup"><span data-stu-id="e17bc-141">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="e17bc-142">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="e17bc-142">-EnableIPForwarding</span></span>
<span data-ttu-id="e17bc-143">Gibt an, dass dieses Cmdlet die IP-Weiterleitung für die Netzwerkschnittstelle aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e17bc-143">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="e17bc-144">Die IP-Weiterleitung ermöglicht es einem virtuellen Computer, Datenverkehr zu empfangen, der an andere Ziele adressiert ist.</span><span class="sxs-lookup"><span data-stu-id="e17bc-144">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="e17bc-145">-Force</span><span class="sxs-lookup"><span data-stu-id="e17bc-145">-Force</span></span>
<span data-ttu-id="e17bc-146">Erzwingt die Erstellung der Netzwerkschnittstelle auch dann, wenn bereits eine Netzwerkschnittstelle mit demselben Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e17bc-146">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="e17bc-147">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="e17bc-147">-InternalDnsNameLabel</span></span>
<span data-ttu-id="e17bc-148">Gibt die interne Namenbezeichnung des DNS für die neue Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="e17bc-148">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="e17bc-149">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e17bc-149">-IpConfiguration</span></span>
<span data-ttu-id="e17bc-150">Gibt die IP-Konfiguration an, die dieses Cmdlet für die Netzwerkschnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="e17bc-150">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]
Parameter Sets: SetByIpConfigurationResource, SetByIpConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17bc-151">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e17bc-151">-IpConfigurationName</span></span>
<span data-ttu-id="e17bc-152">Gibt den Namen einer IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="e17bc-152">Specifies the name of an IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17bc-153">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e17bc-153">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="e17bc-154">Gibt ein **Back-End-AddressPool-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="e17bc-154">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="e17bc-155">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e17bc-155">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="e17bc-156">Gibt die ID eines **Back-End-AddressPool-Objekts** an.</span><span class="sxs-lookup"><span data-stu-id="e17bc-156">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="e17bc-157">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="e17bc-157">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="e17bc-158">Gibt die Konfiguration einer eingehenden NAT-Regel für einen Lastenausgleich an.</span><span class="sxs-lookup"><span data-stu-id="e17bc-158">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="e17bc-159">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="e17bc-159">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="e17bc-160">Gibt die ID einer eingehenden NAT-Regelkonfiguration für einen Lastenausgleich an.</span><span class="sxs-lookup"><span data-stu-id="e17bc-160">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="e17bc-161">-Location</span><span class="sxs-lookup"><span data-stu-id="e17bc-161">-Location</span></span>
<span data-ttu-id="e17bc-162">Gibt die Region für eine Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="e17bc-162">Specifies the region for a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17bc-163">-Name</span><span class="sxs-lookup"><span data-stu-id="e17bc-163">-Name</span></span>
<span data-ttu-id="e17bc-164">Gibt den Namen der zu erstellenden Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="e17bc-164">Specifies the name of the network interface to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17bc-165">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e17bc-165">-NetworkSecurityGroup</span></span>
<span data-ttu-id="e17bc-166">Gibt ein **NetworkSecurityGroup-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="e17bc-166">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByIpConfigurationResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17bc-167">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e17bc-167">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="e17bc-168">Gibt die ID einer Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="e17bc-168">Specifies the ID of a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIpConfigurationResourceId, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17bc-169">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="e17bc-169">-PrivateIpAddress</span></span>
<span data-ttu-id="e17bc-170">Gibt eine statische IPv4-IP-Adresse an, die dieser Netzwerkschnittstelle zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e17bc-170">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17bc-171">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e17bc-171">-PublicIpAddress</span></span>
<span data-ttu-id="e17bc-172">Gibt ein **PublicIPAddress-Objekt** an, das einer Netzwerkschnittstelle zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e17bc-172">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17bc-173">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="e17bc-173">-PublicIpAddressId</span></span>
<span data-ttu-id="e17bc-174">Gibt die ID eines **PublicIPAddress-Objekts** an, das einer Netzwerkschnittstelle zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e17bc-174">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="e17bc-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e17bc-175">-ResourceGroupName</span></span>
<span data-ttu-id="e17bc-176">Gibt den Namen einer Ressourcengruppe an, zu der die Netzwerkschnittstelle gehört.</span><span class="sxs-lookup"><span data-stu-id="e17bc-176">Specifies the name of a resource group that the network interface belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17bc-177">-Subnet</span><span class="sxs-lookup"><span data-stu-id="e17bc-177">-Subnet</span></span>
<span data-ttu-id="e17bc-178">Gibt ein **Subnetzobjekt** an.</span><span class="sxs-lookup"><span data-stu-id="e17bc-178">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="e17bc-179">Dieses Cmdlet erstellt eine Netzwerkschnittstelle für das Subnetz, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e17bc-179">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17bc-180">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e17bc-180">-SubnetId</span></span>
<span data-ttu-id="e17bc-181">Gibt die ID des Subnetzes an, für das eine Netzwerkschnittstelle erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e17bc-181">Specifies the ID of the subnet for which to create a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17bc-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="e17bc-182">-Tag</span></span>
<span data-ttu-id="e17bc-183">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e17bc-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e17bc-184">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="e17bc-184">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17bc-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e17bc-185">-Confirm</span></span>
<span data-ttu-id="e17bc-186">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e17bc-186">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e17bc-187">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e17bc-187">-WhatIf</span></span>
<span data-ttu-id="e17bc-188">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e17bc-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e17bc-189">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e17bc-189">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e17bc-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e17bc-190">CommonParameters</span></span>
<span data-ttu-id="e17bc-191">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e17bc-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e17bc-192">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e17bc-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e17bc-193">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e17bc-193">INPUTS</span></span>

### <span data-ttu-id="e17bc-194">System.String</span><span class="sxs-lookup"><span data-stu-id="e17bc-194">System.String</span></span>

### <span data-ttu-id="e17bc-195">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="e17bc-195">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="e17bc-196">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="e17bc-196">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="e17bc-197">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e17bc-197">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="e17bc-198">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e17bc-198">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="e17bc-199">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e17bc-199">System.String[]</span></span>

### <span data-ttu-id="e17bc-200">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="e17bc-200">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="e17bc-201">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="e17bc-201">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="e17bc-202">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="e17bc-202">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="e17bc-203">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="e17bc-203">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="e17bc-204">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e17bc-204">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e17bc-205">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e17bc-205">OUTPUTS</span></span>

### <span data-ttu-id="e17bc-206">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e17bc-206">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="e17bc-207">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e17bc-207">NOTES</span></span>

## <span data-ttu-id="e17bc-208">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e17bc-208">RELATED LINKS</span></span>

[<span data-ttu-id="e17bc-209">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e17bc-209">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="e17bc-210">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e17bc-210">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="e17bc-211">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e17bc-211">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
