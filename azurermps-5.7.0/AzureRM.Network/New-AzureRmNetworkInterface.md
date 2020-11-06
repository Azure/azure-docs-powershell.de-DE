---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
ms.openlocfilehash: 111723b2f0271583d43bd1c845eebe9800190a59
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93506029"
---
# <span data-ttu-id="18926-101">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="18926-101">New-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="18926-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="18926-102">SYNOPSIS</span></span>
<span data-ttu-id="18926-103">Erstellt eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="18926-103">Creates a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18926-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="18926-104">SYNTAX</span></span>

### <span data-ttu-id="18926-105">SetByIpConfigurationResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="18926-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18926-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="18926-106">SetByIpConfigurationResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-NetworkSecurityGroupId <String>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18926-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="18926-107">SetByResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18926-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="18926-108">SetByResource</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
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

## <span data-ttu-id="18926-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18926-109">DESCRIPTION</span></span>
<span data-ttu-id="18926-110">Das Cmdlet **New-AzureRmNetworkInterface** erstellt eine Azure-Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="18926-110">The **New-AzureRmNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="18926-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18926-111">EXAMPLES</span></span>

### <span data-ttu-id="18926-112">Beispiel 1: Erstellen einer Azure-Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="18926-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="18926-113">Dieser Befehl erstellt eine Netzwerkschnittstelle mit dem Namen NetworkInterface001 mit einer dynamisch zugewiesenen privaten IP-Adresse aus Subnet1 im virtuellen Netzwerk mit dem Namen VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="18926-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="18926-114">Der Befehl weist auch zwei DNS-Server der Netzwerkschnittstelle zu.</span><span class="sxs-lookup"><span data-stu-id="18926-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="18926-115">Die IPKonfigurationsdateiAddress-untergeordnete Ressource wird automatisch mit dem Namen IPConfiguration1 erstellt.</span><span class="sxs-lookup"><span data-stu-id="18926-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="18926-116">Beispiel 2: Erstellen einer Azure-Netzwerkschnittstelle mithilfe eines IP-Konfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="18926-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzureRmNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="18926-117">In diesem Beispiel wird eine neue Netzwerkschnittstelle mit einem IP-Konfigurationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="18926-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="18926-118">Das IP-Konfigurationsobjekt gibt eine statische private IPv4-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="18926-118">The IP configuration object specifies a static private IPv4 address.</span></span>

<span data-ttu-id="18926-119">Der erste Befehl erstellt eine Netzwerkschnittstellen-IP-Konfiguration mit dem Namen IPConfig1 und speichert die Konfiguration in der Variablen mit dem Namen $ipconfig.</span><span class="sxs-lookup"><span data-stu-id="18926-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>

<span data-ttu-id="18926-120">Der zweite Befehl erstellt eine Netzwerkschnittstelle mit dem Namen NetworkInterface1, die die in der Variablen mit dem Namen $ipconfig gespeicherte Netzwerkschnittstellen-IP-Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="18926-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="18926-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="18926-121">PARAMETERS</span></span>

### <span data-ttu-id="18926-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="18926-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="18926-123">Gibt ein **ApplicationGatewayBackendAddressPool** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="18926-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="18926-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="18926-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="18926-125">Gibt die ID eines **ApplicationGatewayBackendAddressPool** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="18926-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="18926-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="18926-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="18926-127">Gibt eine Sammlung von Anwendungs Sicherheitsgruppen-verweisen an, zu denen die IP-Konfiguration der Netzwerkschnittstelle gehören soll.</span><span class="sxs-lookup"><span data-stu-id="18926-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="18926-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="18926-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="18926-129">Gibt eine Sammlung von Anwendungs Sicherheitsgruppen-verweisen an, zu denen die IP-Konfiguration der Netzwerkschnittstelle gehören soll.</span><span class="sxs-lookup"><span data-stu-id="18926-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="18926-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18926-130">-AsJob</span></span>
<span data-ttu-id="18926-131">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="18926-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18926-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18926-132">-DefaultProfile</span></span>
<span data-ttu-id="18926-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="18926-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18926-134">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="18926-134">-DnsServer</span></span>
<span data-ttu-id="18926-135">Gibt den DNS-Server für die Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="18926-135">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="18926-136">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="18926-136">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="18926-137">Ermöglicht beschleunigtes Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="18926-137">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="18926-138">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="18926-138">-EnableIPForwarding</span></span>
<span data-ttu-id="18926-139">Gibt an, dass dieses Cmdlet die IP-Weiterleitung für die Netzwerkschnittstelle aktiviert.</span><span class="sxs-lookup"><span data-stu-id="18926-139">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="18926-140">IP-Weiterleitung ermöglicht einem virtuellen Computer den Empfang von Datenverkehr, der an andere Zielorte adressiert ist.</span><span class="sxs-lookup"><span data-stu-id="18926-140">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="18926-141">-Force</span><span class="sxs-lookup"><span data-stu-id="18926-141">-Force</span></span>
<span data-ttu-id="18926-142">Erzwingt die Erstellung der Netzwerkschnittstelle, selbst wenn bereits eine Netzwerkschnittstelle mit dem gleichen Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="18926-142">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="18926-143">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="18926-143">-InternalDnsNameLabel</span></span>
<span data-ttu-id="18926-144">Gibt die interne DNS-Namensbezeichnung für die neue Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="18926-144">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="18926-145">-IPKonfigurationsdateiAddress</span><span class="sxs-lookup"><span data-stu-id="18926-145">-IpConfiguration</span></span>
<span data-ttu-id="18926-146">Gibt die IP-Konfiguration an, die dieses Cmdlet für die Netzwerkschnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="18926-146">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="18926-147">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="18926-147">-IpConfigurationName</span></span>
<span data-ttu-id="18926-148">Gibt den Namen einer IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="18926-148">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="18926-149">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="18926-149">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="18926-150">Gibt ein **BackendAddressPool** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="18926-150">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="18926-151">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="18926-151">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="18926-152">Gibt die ID eines **BackendAddressPool** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="18926-152">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="18926-153">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="18926-153">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="18926-154">Gibt eine eingehende NAT-Regelkonfiguration für ein Load Balancer an.</span><span class="sxs-lookup"><span data-stu-id="18926-154">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="18926-155">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="18926-155">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="18926-156">Gibt die ID einer eingehenden NAT-Regelkonfiguration für ein Lastenausgleichsmodul an.</span><span class="sxs-lookup"><span data-stu-id="18926-156">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="18926-157">-Standort</span><span class="sxs-lookup"><span data-stu-id="18926-157">-Location</span></span>
<span data-ttu-id="18926-158">Gibt den Bereich für eine Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="18926-158">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="18926-159">-Name</span><span class="sxs-lookup"><span data-stu-id="18926-159">-Name</span></span>
<span data-ttu-id="18926-160">Gibt den Namen der zu erstellende Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="18926-160">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="18926-161">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="18926-161">-NetworkSecurityGroup</span></span>
<span data-ttu-id="18926-162">Gibt ein **NetworkSecurityGroup** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="18926-162">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="18926-163">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="18926-163">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="18926-164">Gibt die ID einer Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="18926-164">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="18926-165">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="18926-165">-PrivateIpAddress</span></span>
<span data-ttu-id="18926-166">Gibt eine statische IPv4-IP-Adresse an, die dieser Netzwerkschnittstelle zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="18926-166">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="18926-167">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="18926-167">-PublicIpAddress</span></span>
<span data-ttu-id="18926-168">Gibt ein **PublicIPAddress** -Objekt an, das einer Netzwerkschnittstelle zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="18926-168">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="18926-169">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="18926-169">-PublicIpAddressId</span></span>
<span data-ttu-id="18926-170">Gibt die ID eines **PublicIPAddress** -Objekts an, das einer Netzwerkschnittstelle zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="18926-170">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="18926-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18926-171">-ResourceGroupName</span></span>
<span data-ttu-id="18926-172">Gibt den Namen einer Ressourcengruppe an, zu der die Netzwerkschnittstelle gehört.</span><span class="sxs-lookup"><span data-stu-id="18926-172">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="18926-173">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="18926-173">-Subnet</span></span>
<span data-ttu-id="18926-174">Gibt ein **Subnetz** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="18926-174">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="18926-175">Dieses Cmdlet erstellt eine Netzwerkschnittstelle für das Subnetz, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="18926-175">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="18926-176">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="18926-176">-SubnetId</span></span>
<span data-ttu-id="18926-177">Gibt die ID des Subnets an, für das eine Netzwerkschnittstelle erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="18926-177">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="18926-178">-Tag</span><span class="sxs-lookup"><span data-stu-id="18926-178">-Tag</span></span>
<span data-ttu-id="18926-179">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="18926-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="18926-180">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="18926-180">For example:</span></span>

<span data-ttu-id="18926-181">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="18926-181">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="18926-182">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="18926-182">-Confirm</span></span>
<span data-ttu-id="18926-183">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="18926-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18926-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18926-184">-WhatIf</span></span>
<span data-ttu-id="18926-185">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="18926-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18926-186">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="18926-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18926-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18926-187">CommonParameters</span></span>
<span data-ttu-id="18926-188">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18926-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18926-189">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18926-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18926-190">Eingaben</span><span class="sxs-lookup"><span data-stu-id="18926-190">INPUTS</span></span>

### <span data-ttu-id="18926-191">Keine</span><span class="sxs-lookup"><span data-stu-id="18926-191">None</span></span>
<span data-ttu-id="18926-192">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="18926-192">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="18926-193">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="18926-193">OUTPUTS</span></span>

### <span data-ttu-id="18926-194">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="18926-194">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="18926-195">Notizen</span><span class="sxs-lookup"><span data-stu-id="18926-195">NOTES</span></span>

## <span data-ttu-id="18926-196">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="18926-196">RELATED LINKS</span></span>

[<span data-ttu-id="18926-197">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="18926-197">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="18926-198">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="18926-198">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="18926-199">Satz-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="18926-199">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)
