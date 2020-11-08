---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: feefe02c5056556d360a54819ea429cd39b84b62
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996838"
---
# <span data-ttu-id="08877-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="08877-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="08877-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08877-102">SYNOPSIS</span></span>
<span data-ttu-id="08877-103">Erstellt eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="08877-103">Creates a network interface.</span></span>

## <span data-ttu-id="08877-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08877-104">SYNTAX</span></span>

### <span data-ttu-id="08877-105">SetByIpConfigurationResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="08877-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08877-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="08877-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08877-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="08877-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08877-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="08877-108">SetByResource</span></span>
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

## <span data-ttu-id="08877-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08877-109">DESCRIPTION</span></span>
<span data-ttu-id="08877-110">Das Cmdlet **New-AzNetworkInterface** erstellt eine Azure-Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="08877-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="08877-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08877-111">EXAMPLES</span></span>

### <span data-ttu-id="08877-112">Beispiel 1: Erstellen einer Azure-Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="08877-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="08877-113">Dieser Befehl erstellt eine Netzwerkschnittstelle mit dem Namen NetworkInterface001 mit einer dynamisch zugewiesenen privaten IP-Adresse aus Subnet1 im virtuellen Netzwerk mit dem Namen VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="08877-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="08877-114">Der Befehl weist auch zwei DNS-Server der Netzwerkschnittstelle zu.</span><span class="sxs-lookup"><span data-stu-id="08877-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="08877-115">Die IPKonfigurationsdateiAddress-untergeordnete Ressource wird automatisch mit dem Namen IPConfiguration1 erstellt.</span><span class="sxs-lookup"><span data-stu-id="08877-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="08877-116">Beispiel 2: Erstellen einer Azure-Netzwerkschnittstelle mithilfe eines IP-Konfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="08877-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="08877-117">In diesem Beispiel wird eine neue Netzwerkschnittstelle mit einem IP-Konfigurationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="08877-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="08877-118">Das IP-Konfigurationsobjekt gibt eine statische private IPv4-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="08877-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="08877-119">Der erste Befehl ruft ein vorhandenes festgelegtes virtuelles Netzwerk ab, mit dem das Subnetz im zweiten Befehl zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="08877-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="08877-120">Der zweite Befehl erstellt eine Netzwerkschnittstellen-IP-Konfiguration mit dem Namen IPConfig1 und speichert die Konfiguration in der Variablen mit dem Namen $ipconfig.</span><span class="sxs-lookup"><span data-stu-id="08877-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="08877-121">Der dritte Befehl erstellt eine Netzwerkschnittstelle mit dem Namen NetworkInterface1, die die in der Variablen mit dem Namen $ipconfig gespeicherte Netzwerkschnittstellen-IP-Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="08877-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="08877-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="08877-122">PARAMETERS</span></span>

### <span data-ttu-id="08877-123">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="08877-123">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="08877-124">Gibt ein **ApplicationGatewayBackendAddressPool** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="08877-124">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="08877-125">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="08877-125">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="08877-126">Gibt die ID eines **ApplicationGatewayBackendAddressPool** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="08877-126">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="08877-127">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="08877-127">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="08877-128">Gibt eine Sammlung von Anwendungs Sicherheitsgruppen-verweisen an, zu denen die IP-Konfiguration der Netzwerkschnittstelle gehören soll.</span><span class="sxs-lookup"><span data-stu-id="08877-128">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="08877-129">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="08877-129">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="08877-130">Gibt eine Sammlung von Anwendungs Sicherheitsgruppen-verweisen an, zu denen die IP-Konfiguration der Netzwerkschnittstelle gehören soll.</span><span class="sxs-lookup"><span data-stu-id="08877-130">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="08877-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08877-131">-AsJob</span></span>
<span data-ttu-id="08877-132">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="08877-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="08877-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08877-133">-DefaultProfile</span></span>
<span data-ttu-id="08877-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="08877-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08877-135">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="08877-135">-DnsServer</span></span>
<span data-ttu-id="08877-136">Gibt den DNS-Server für die Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="08877-136">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="08877-137">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="08877-137">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="08877-138">Ermöglicht beschleunigtes Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="08877-138">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="08877-139">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="08877-139">-EnableIPForwarding</span></span>
<span data-ttu-id="08877-140">Gibt an, dass dieses Cmdlet die IP-Weiterleitung für die Netzwerkschnittstelle aktiviert.</span><span class="sxs-lookup"><span data-stu-id="08877-140">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="08877-141">IP-Weiterleitung ermöglicht einem virtuellen Computer den Empfang von Datenverkehr, der an andere Zielorte adressiert ist.</span><span class="sxs-lookup"><span data-stu-id="08877-141">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="08877-142">-Force</span><span class="sxs-lookup"><span data-stu-id="08877-142">-Force</span></span>
<span data-ttu-id="08877-143">Erzwingt die Erstellung der Netzwerkschnittstelle, selbst wenn bereits eine Netzwerkschnittstelle mit dem gleichen Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="08877-143">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="08877-144">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="08877-144">-InternalDnsNameLabel</span></span>
<span data-ttu-id="08877-145">Gibt die interne DNS-Namensbezeichnung für die neue Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="08877-145">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="08877-146">-IPKonfigurationsdateiAddress</span><span class="sxs-lookup"><span data-stu-id="08877-146">-IpConfiguration</span></span>
<span data-ttu-id="08877-147">Gibt die IP-Konfiguration an, die dieses Cmdlet für die Netzwerkschnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="08877-147">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="08877-148">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="08877-148">-IpConfigurationName</span></span>
<span data-ttu-id="08877-149">Gibt den Namen einer IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="08877-149">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="08877-150">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="08877-150">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="08877-151">Gibt ein **BackendAddressPool** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="08877-151">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="08877-152">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="08877-152">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="08877-153">Gibt die ID eines **BackendAddressPool** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="08877-153">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="08877-154">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="08877-154">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="08877-155">Gibt eine eingehende NAT-Regelkonfiguration für ein Load Balancer an.</span><span class="sxs-lookup"><span data-stu-id="08877-155">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="08877-156">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="08877-156">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="08877-157">Gibt die ID einer eingehenden NAT-Regelkonfiguration für ein Lastenausgleichsmodul an.</span><span class="sxs-lookup"><span data-stu-id="08877-157">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="08877-158">-Standort</span><span class="sxs-lookup"><span data-stu-id="08877-158">-Location</span></span>
<span data-ttu-id="08877-159">Gibt den Bereich für eine Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="08877-159">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="08877-160">-Name</span><span class="sxs-lookup"><span data-stu-id="08877-160">-Name</span></span>
<span data-ttu-id="08877-161">Gibt den Namen der zu erstellende Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="08877-161">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="08877-162">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="08877-162">-NetworkSecurityGroup</span></span>
<span data-ttu-id="08877-163">Gibt ein **NetworkSecurityGroup** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="08877-163">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="08877-164">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="08877-164">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="08877-165">Gibt die ID einer Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="08877-165">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="08877-166">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="08877-166">-PrivateIpAddress</span></span>
<span data-ttu-id="08877-167">Gibt eine statische IPv4-IP-Adresse an, die dieser Netzwerkschnittstelle zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="08877-167">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="08877-168">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="08877-168">-PublicIpAddress</span></span>
<span data-ttu-id="08877-169">Gibt ein **PublicIPAddress** -Objekt an, das einer Netzwerkschnittstelle zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="08877-169">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="08877-170">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="08877-170">-PublicIpAddressId</span></span>
<span data-ttu-id="08877-171">Gibt die ID eines **PublicIPAddress** -Objekts an, das einer Netzwerkschnittstelle zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="08877-171">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="08877-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08877-172">-ResourceGroupName</span></span>
<span data-ttu-id="08877-173">Gibt den Namen einer Ressourcengruppe an, zu der die Netzwerkschnittstelle gehört.</span><span class="sxs-lookup"><span data-stu-id="08877-173">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="08877-174">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="08877-174">-Subnet</span></span>
<span data-ttu-id="08877-175">Gibt ein **Subnetz** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="08877-175">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="08877-176">Dieses Cmdlet erstellt eine Netzwerkschnittstelle für das Subnetz, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="08877-176">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="08877-177">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="08877-177">-SubnetId</span></span>
<span data-ttu-id="08877-178">Gibt die ID des Subnets an, für das eine Netzwerkschnittstelle erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="08877-178">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="08877-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="08877-179">-Tag</span></span>
<span data-ttu-id="08877-180">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="08877-180">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="08877-181">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="08877-181">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="08877-182">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="08877-182">-Confirm</span></span>
<span data-ttu-id="08877-183">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08877-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08877-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08877-184">-WhatIf</span></span>
<span data-ttu-id="08877-185">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08877-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08877-186">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08877-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08877-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08877-187">CommonParameters</span></span>
<span data-ttu-id="08877-188">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08877-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08877-189">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08877-189">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08877-190">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08877-190">INPUTS</span></span>

### <span data-ttu-id="08877-191">System. String</span><span class="sxs-lookup"><span data-stu-id="08877-191">System.String</span></span>

### <span data-ttu-id="08877-192">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="08877-192">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="08877-193">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="08877-193">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="08877-194">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="08877-194">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="08877-195">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="08877-195">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="08877-196">System. String []</span><span class="sxs-lookup"><span data-stu-id="08877-196">System.String[]</span></span>

### <span data-ttu-id="08877-197">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="08877-197">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="08877-198">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="08877-198">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="08877-199">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="08877-199">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="08877-200">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="08877-200">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="08877-201">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="08877-201">System.Collections.Hashtable</span></span>

## <span data-ttu-id="08877-202">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08877-202">OUTPUTS</span></span>

### <span data-ttu-id="08877-203">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="08877-203">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="08877-204">Notizen</span><span class="sxs-lookup"><span data-stu-id="08877-204">NOTES</span></span>

## <span data-ttu-id="08877-205">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08877-205">RELATED LINKS</span></span>

[<span data-ttu-id="08877-206">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="08877-206">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="08877-207">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="08877-207">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="08877-208">Satz-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="08877-208">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
