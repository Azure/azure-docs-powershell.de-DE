---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: a4a40f67eef901cd1e93ac004fa01a3224ab222e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841320"
---
# <span data-ttu-id="aad00-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="aad00-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="aad00-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aad00-102">SYNOPSIS</span></span>
<span data-ttu-id="aad00-103">Erstellt eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="aad00-103">Creates a network interface.</span></span>

## <span data-ttu-id="aad00-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aad00-104">SYNTAX</span></span>

### <span data-ttu-id="aad00-105">SetByIpConfigurationResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="aad00-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aad00-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="aad00-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-NetworkSecurityGroupId <String>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aad00-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="aad00-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aad00-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="aad00-108">SetByResource</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aad00-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aad00-109">DESCRIPTION</span></span>
<span data-ttu-id="aad00-110">Das Cmdlet **New-AzNetworkInterface** erstellt eine Azure-Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="aad00-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="aad00-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aad00-111">EXAMPLES</span></span>

### <span data-ttu-id="aad00-112">Beispiel 1: Erstellen einer Azure-Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="aad00-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="aad00-113">Dieser Befehl erstellt eine Netzwerkschnittstelle mit dem Namen NetworkInterface001 mit einer dynamisch zugewiesenen privaten IP-Adresse aus Subnet1 im virtuellen Netzwerk mit dem Namen VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="aad00-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="aad00-114">Der Befehl weist auch zwei DNS-Server der Netzwerkschnittstelle zu.</span><span class="sxs-lookup"><span data-stu-id="aad00-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="aad00-115">Die IPKonfigurationsdateiAddress-untergeordnete Ressource wird automatisch mit dem Namen IPConfiguration1 erstellt.</span><span class="sxs-lookup"><span data-stu-id="aad00-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="aad00-116">Beispiel 2: Erstellen einer Azure-Netzwerkschnittstelle mithilfe eines IP-Konfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="aad00-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="aad00-117">In diesem Beispiel wird eine neue Netzwerkschnittstelle mit einem IP-Konfigurationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="aad00-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="aad00-118">Das IP-Konfigurationsobjekt gibt eine statische private IPv4-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="aad00-118">The IP configuration object specifies a static private IPv4 address.</span></span>

<span data-ttu-id="aad00-119">Der erste Befehl erstellt eine Netzwerkschnittstellen-IP-Konfiguration mit dem Namen IPConfig1 und speichert die Konfiguration in der Variablen mit dem Namen $ipconfig.</span><span class="sxs-lookup"><span data-stu-id="aad00-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>

<span data-ttu-id="aad00-120">Der zweite Befehl erstellt eine Netzwerkschnittstelle mit dem Namen NetworkInterface1, die die in der Variablen mit dem Namen $ipconfig gespeicherte Netzwerkschnittstellen-IP-Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="aad00-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="aad00-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="aad00-121">PARAMETERS</span></span>

### <span data-ttu-id="aad00-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="aad00-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="aad00-123">Gibt ein **ApplicationGatewayBackendAddressPool** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="aad00-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="aad00-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="aad00-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="aad00-125">Gibt die ID eines **ApplicationGatewayBackendAddressPool** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="aad00-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="aad00-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aad00-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="aad00-127">Gibt eine Sammlung von Anwendungs Sicherheitsgruppen-verweisen an, zu denen die IP-Konfiguration der Netzwerkschnittstelle gehören soll.</span><span class="sxs-lookup"><span data-stu-id="aad00-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="aad00-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="aad00-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="aad00-129">Gibt eine Sammlung von Anwendungs Sicherheitsgruppen-verweisen an, zu denen die IP-Konfiguration der Netzwerkschnittstelle gehören soll.</span><span class="sxs-lookup"><span data-stu-id="aad00-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="aad00-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aad00-130">-AsJob</span></span>
<span data-ttu-id="aad00-131">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="aad00-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aad00-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aad00-132">-DefaultProfile</span></span>
<span data-ttu-id="aad00-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aad00-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aad00-134">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="aad00-134">-DnsServer</span></span>
<span data-ttu-id="aad00-135">Gibt den DNS-Server für die Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="aad00-135">Specifies the DNS server for the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-136">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="aad00-136">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="aad00-137">Ermöglicht beschleunigtes Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="aad00-137">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="aad00-138">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="aad00-138">-EnableIPForwarding</span></span>
<span data-ttu-id="aad00-139">Gibt an, dass dieses Cmdlet die IP-Weiterleitung für die Netzwerkschnittstelle aktiviert.</span><span class="sxs-lookup"><span data-stu-id="aad00-139">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="aad00-140">IP-Weiterleitung ermöglicht einem virtuellen Computer den Empfang von Datenverkehr, der an andere Zielorte adressiert ist.</span><span class="sxs-lookup"><span data-stu-id="aad00-140">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="aad00-141">-Force</span><span class="sxs-lookup"><span data-stu-id="aad00-141">-Force</span></span>
<span data-ttu-id="aad00-142">Erzwingt die Erstellung der Netzwerkschnittstelle, selbst wenn bereits eine Netzwerkschnittstelle mit dem gleichen Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="aad00-142">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="aad00-143">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="aad00-143">-InternalDnsNameLabel</span></span>
<span data-ttu-id="aad00-144">Gibt die interne DNS-Namensbezeichnung für die neue Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="aad00-144">Specifies the internal DNS name label for the new network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-145">-IPKonfigurationsdateiAddress</span><span class="sxs-lookup"><span data-stu-id="aad00-145">-IpConfiguration</span></span>
<span data-ttu-id="aad00-146">Gibt die IP-Konfiguration an, die dieses Cmdlet für die Netzwerkschnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="aad00-146">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]
Parameter Sets: SetByIpConfigurationResource, SetByIpConfigurationResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-147">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="aad00-147">-IpConfigurationName</span></span>
<span data-ttu-id="aad00-148">Gibt den Namen einer IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="aad00-148">Specifies the name of an IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-149">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="aad00-149">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="aad00-150">Gibt ein **BackendAddressPool** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="aad00-150">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="aad00-151">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="aad00-151">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="aad00-152">Gibt die ID eines **BackendAddressPool** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="aad00-152">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="aad00-153">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="aad00-153">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="aad00-154">Gibt eine eingehende NAT-Regelkonfiguration für ein Load Balancer an.</span><span class="sxs-lookup"><span data-stu-id="aad00-154">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="aad00-155">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="aad00-155">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="aad00-156">Gibt die ID einer eingehenden NAT-Regelkonfiguration für ein Lastenausgleichsmodul an.</span><span class="sxs-lookup"><span data-stu-id="aad00-156">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="aad00-157">-Standort</span><span class="sxs-lookup"><span data-stu-id="aad00-157">-Location</span></span>
<span data-ttu-id="aad00-158">Gibt den Bereich für eine Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="aad00-158">Specifies the region for a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-159">-Name</span><span class="sxs-lookup"><span data-stu-id="aad00-159">-Name</span></span>
<span data-ttu-id="aad00-160">Gibt den Namen der zu erstellende Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="aad00-160">Specifies the name of the network interface to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-161">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aad00-161">-NetworkSecurityGroup</span></span>
<span data-ttu-id="aad00-162">Gibt ein **NetworkSecurityGroup** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="aad00-162">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: SetByIpConfigurationResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-163">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="aad00-163">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="aad00-164">Gibt die ID einer Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="aad00-164">Specifies the ID of a network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByIpConfigurationResourceId, SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-165">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="aad00-165">-PrivateIpAddress</span></span>
<span data-ttu-id="aad00-166">Gibt eine statische IPv4-IP-Adresse an, die dieser Netzwerkschnittstelle zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="aad00-166">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-167">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="aad00-167">-PublicIpAddress</span></span>
<span data-ttu-id="aad00-168">Gibt ein **PublicIPAddress** -Objekt an, das einer Netzwerkschnittstelle zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="aad00-168">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-169">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="aad00-169">-PublicIpAddressId</span></span>
<span data-ttu-id="aad00-170">Gibt die ID eines **PublicIPAddress** -Objekts an, das einer Netzwerkschnittstelle zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="aad00-170">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aad00-171">-ResourceGroupName</span></span>
<span data-ttu-id="aad00-172">Gibt den Namen einer Ressourcengruppe an, zu der die Netzwerkschnittstelle gehört.</span><span class="sxs-lookup"><span data-stu-id="aad00-172">Specifies the name of a resource group that the network interface belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-173">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="aad00-173">-Subnet</span></span>
<span data-ttu-id="aad00-174">Gibt ein **Subnetz** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="aad00-174">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="aad00-175">Dieses Cmdlet erstellt eine Netzwerkschnittstelle für das Subnetz, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="aad00-175">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-176">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="aad00-176">-SubnetId</span></span>
<span data-ttu-id="aad00-177">Gibt die ID des Subnets an, für das eine Netzwerkschnittstelle erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="aad00-177">Specifies the ID of the subnet for which to create a network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-178">-Tag</span><span class="sxs-lookup"><span data-stu-id="aad00-178">-Tag</span></span>
<span data-ttu-id="aad00-179">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="aad00-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="aad00-180">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="aad00-180">For example:</span></span>

<span data-ttu-id="aad00-181">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="aad00-181">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-182">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aad00-182">-Confirm</span></span>
<span data-ttu-id="aad00-183">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aad00-183">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aad00-184">-WhatIf</span></span>
<span data-ttu-id="aad00-185">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aad00-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aad00-186">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aad00-186">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aad00-187">CommonParameters</span></span>
<span data-ttu-id="aad00-188">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aad00-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aad00-189">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aad00-189">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aad00-190">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aad00-190">INPUTS</span></span>

## <span data-ttu-id="aad00-191">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aad00-191">OUTPUTS</span></span>

### <span data-ttu-id="aad00-192">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="aad00-192">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="aad00-193">Notizen</span><span class="sxs-lookup"><span data-stu-id="aad00-193">NOTES</span></span>

## <span data-ttu-id="aad00-194">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aad00-194">RELATED LINKS</span></span>

[<span data-ttu-id="aad00-195">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="aad00-195">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="aad00-196">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="aad00-196">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="aad00-197">Satz-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="aad00-197">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
