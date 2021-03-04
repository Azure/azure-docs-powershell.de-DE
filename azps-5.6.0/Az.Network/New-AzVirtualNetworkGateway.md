---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: c9729dd81dc5ff287ab032fdce6ad937c282e1c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931555"
---
# <span data-ttu-id="dad61-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dad61-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="dad61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dad61-102">SYNOPSIS</span></span>
<span data-ttu-id="dad61-103">Erstellt ein Virtuelles Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="dad61-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="dad61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dad61-104">SYNTAX</span></span>

### <span data-ttu-id="dad61-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="dad61-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad61-106">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="dad61-106">MultipleRadiusServersConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -RadiusServerList <PSRadiusServer[]> [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad61-107">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="dad61-107">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dad61-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="dad61-108">AadAuthenticationConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -AadTenantUri <String> -AadAudienceId <String> -AadIssuerUri <String> [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dad61-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dad61-109">DESCRIPTION</span></span>
<span data-ttu-id="dad61-110">Das Virtual Network Gateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="dad61-110">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="dad61-111">Das **Cmdlet New-AzVirtualNetworkGateway** erstellt das Objekt Ihres Gateways in Azure basierend auf der Konfiguration Name, Ressourcengruppe, Standort und IP sowie dem Gatewaytyp und, wenn VPN, dem VPN-Typ.</span><span class="sxs-lookup"><span data-stu-id="dad61-111">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="dad61-112">Sie können auch die Gateway-SKU benennen.</span><span class="sxs-lookup"><span data-stu-id="dad61-112">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="dad61-113">Wenn dieses Gateway für Punkt-zu-Website-Verbindungen verwendet wird, müssen Sie auch den VPN-Clientadressenpool angeben, über den Sie Verbindungsclients Adressen zuweisen können, und das VPN-Clientstammzertifikat, das zum Authentifizieren von VPN-Clients verwendet wird, die eine Verbindung mit dem Gateway herstellen.</span><span class="sxs-lookup"><span data-stu-id="dad61-113">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="dad61-114">Sie können auch andere Features wie BGP und Active-Active verwenden.</span><span class="sxs-lookup"><span data-stu-id="dad61-114">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="dad61-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dad61-115">EXAMPLES</span></span>

### <span data-ttu-id="dad61-116">Beispiel 1: Erstellen eines Virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="dad61-116">Example 1: Create a Virtual Network Gateway</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="dad61-117">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe erstellt, eine öffentliche IP-Adresse anfordern, ein virtuelles Netzwerk und ein Subnetz erstellt und ein Virtuelles Netzwerkgateway in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="dad61-117">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="dad61-118">Das Gateway wird innerhalb der Ressourcengruppe "vnet-gateway" im Speicherort "UK West" mit den zuvor erstellten IP-Konfigurationen in der Variablen "ngwIPConfig", dem Gatewaytyp "VPN", dem Vpntyp "RouteBased" und der Sku "Basic" als "myNGW" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="dad61-118">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="dad61-119">Beispiel 2: Erstellen eines virtuellen Netzwerkgateways mit Konfiguration für externen Radius</span><span class="sxs-lookup"><span data-stu-id="dad61-119">Example 2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="dad61-120">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe erstellt, eine öffentliche IP-Adresse anfordern, ein virtuelles Netzwerk und ein Subnetz erstellt und ein Virtuelles Netzwerkgateway in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="dad61-120">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="dad61-121">Das Gateway wird innerhalb der Ressourcengruppe "vnet-gateway" im Speicherort "UK West" mit den zuvor erstellten IP-Konfigurationen in der Variablen "ngwIPConfig", dem Gatewaytyp "VPN", dem Vpntyp "RouteBased" und der Sku "Basic" als "myNGW" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="dad61-121">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="dad61-122">Außerdem wird ein externer Radiusserver mit der Adresse "TestRadiusServer" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="dad61-122">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="dad61-123">Außerdem werden benutzerdefinierte Routen festgelegt, die von Kunden im Gateway angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="dad61-123">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="dad61-124">Beispiel 3: Erstellen eines Virtuellen Netzwerkgateways mit P2S-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="dad61-124">Example 3: Create a Virtual Network Gateway with P2S settings</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$rootCert = New-AzVpnClientRootCertificate -Name $clientRootCertName -PublicCertData $samplePublicCertData
$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86471 -SADataSizeKilobytes 429496 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol IkeV2 -VpnClientAddressPool 201.169.0.0/16 -VpnClientRootCertificates $rootCert -VpnClientIpsecPolicy $vpnclientipsecpolicy -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="dad61-125">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe erstellt, eine öffentliche IP-Adresse anfordern, ein virtuelles Netzwerk und ein Subnetz sowie ein virtuelles Netzwerkgateway mit P2S-Einstellungen wie VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy usw. in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="dad61-125">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="dad61-126">Das Gateway wird innerhalb der Ressourcengruppe "vnet-gateway" im Speicherort "UK West" mit den zuvor erstellten IP-Konfigurationen in der Variablen "ngwIPConfig", dem Gatewaytyp "VPN", dem Vpntyp "RouteBased" und der Sku "VpnGw1" als "myNGW" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="dad61-126">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="dad61-127">Vpn-Einstellungen werden für Gateway festgelegt, z. B. VpnProtocol als Ikev2 festgelegt, VpnClientAddressPool als "201.169.0.0/16", VpnClientRootCertificate als übergeben festgelegt: clientRootCertName und benutzerdefinierte vpn ipsec-Richtlinie, die in object:$vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="dad61-127">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="dad61-128">Außerdem werden benutzerdefinierte Routen festgelegt, die von Kunden im Gateway angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="dad61-128">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="dad61-129">Beispiel 4: Erstellen eines Virtuellen Netzwerkgateways mit AAD-Authentifizierungskonfiguration für VpnClient des virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="dad61-129">Example 4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol OpenVPN   -VpnClientAddressPool 201.169.0.0/16 -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"
```

<span data-ttu-id="dad61-130">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe erstellt, eine öffentliche IP-Adresse anfordern, ein virtuelles Netzwerk und ein Subnetz erstellt und ein Virtuelles Netzwerkgateway in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="dad61-130">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="dad61-131">Das Gateway wird innerhalb der Ressourcengruppe "vnet-gateway" im Speicherort "UK West" mit den zuvor erstellten IP-Konfigurationen in der Variablen "ngwIPConfig", dem Gatewaytyp "VPN", dem Vpntyp "RouteBased" und der Sku "Basic" als "myNGW" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="dad61-131">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="dad61-132">Außerdem werden AAD-Authentifizierungskonfigurationen konfiguriert: AadTenantUri, AadIssuerUri und AadAudienceId für VpnClient des Virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="dad61-132">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="dad61-133">Beispiel 5: Erstellen eines Virtuellen Netzwerkgateways mit VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="dad61-133">Example 5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="dad61-134">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe erstellt, eine öffentliche IP-Adresse anfordern, ein virtuelles Netzwerk und ein Subnetz erstellt und ein Virtuelles Netzwerkgateway in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="dad61-134">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="dad61-135">Das Gateway wird innerhalb der Ressourcengruppe "vnet-gateway" im Speicherort "UK West" mit den zuvor erstellten IP-Konfigurationen in der Variablen "ngwIPConfig", dem Gatewaytyp von "VPN", dem Vpntyp "RouteBased", der Sku "VpnGw4" und aktivierter VpnGatewayGeneration Generation2 als "myNGW" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="dad61-135">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="dad61-136">Beispiel 6: Erstellen eines virtuellen Netzwerkgateways mit IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="dad61-136">Example 6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "resourcegroup1"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "resourcegroup1" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "resourcegroup1" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ipconfig1 -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

$ipconfigurationId1 = ngwipconfig.id
$addresslist1 = @('169.254.21.10')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1

New-AzVirtualNetworkGateway -Name gateway1 -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig -IpConfigurationBgpPeeringAddresses $gw1ipconfBgp1 -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="dad61-137">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe erstellt, eine öffentliche IP-Adresse anfordern, ein virtuelles Netzwerk und ein Subnetz erstellt und ein Virtuelles Netzwerkgateway in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="dad61-137">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="dad61-138">ipconfigurationId1 der gerade erstellten und in ngwipconfig gespeicherten Gateway-ipconfiguration.</span><span class="sxs-lookup"><span data-stu-id="dad61-138">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="dad61-139">Das Gateway wird innerhalb der Ressourcengruppe "resourcegroup1resourcegroup1" im Speicherort "UK West" mit den zuvor erstellten IP-Konfigurationen Bgppeering-Adresse, die in der Variablen "gw1ipconfBgp1", dem Gatewaytyp von "VPN", dem Vpntyp "RouteBased", der sku "VpnGw4" und aktivierten VpnGatewayGeneration Generation2 gespeichert ist, als "Gateway1" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="dad61-139">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="dad61-140">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dad61-140">PARAMETERS</span></span>

### <span data-ttu-id="dad61-141">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="dad61-141">-AadAudienceId</span></span>
<span data-ttu-id="dad61-142">P2S AAD-Authentifizierungsoption:AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="dad61-142">P2S AAD authentication option:AadAudienceId.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad61-143">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="dad61-143">-AadIssuerUri</span></span>
<span data-ttu-id="dad61-144">P2S AAD-Authentifizierungsoption:AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="dad61-144">P2S AAD authentication option:AadIssuerUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad61-145">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="dad61-145">-AadTenantUri</span></span>
<span data-ttu-id="dad61-146">P2S AAD-Authentifizierungsoption:AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="dad61-146">P2S AAD authentication option:AadTenantUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad61-147">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dad61-147">-AsJob</span></span>
<span data-ttu-id="dad61-148">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="dad61-148">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dad61-149">-Asn</span><span class="sxs-lookup"><span data-stu-id="dad61-149">-Asn</span></span>
<span data-ttu-id="dad61-150">ASN für BGP über VPN des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="dad61-150">The virtual network gateway's ASN for BGP over VPN</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad61-151">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="dad61-151">-CustomRoute</span></span>
<span data-ttu-id="dad61-152">Vom Kunden angegebene benutzerdefinierte Routen AddressPool</span><span class="sxs-lookup"><span data-stu-id="dad61-152">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="dad61-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad61-153">-DefaultProfile</span></span>
<span data-ttu-id="dad61-154">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dad61-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dad61-155">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="dad61-155">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="dad61-156">Kennzeichnen zum Aktivieren des Active Active-Features auf einem Gateway für virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="dad61-156">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="dad61-157">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="dad61-157">-EnableBgp</span></span>
<span data-ttu-id="dad61-158">EnableBgp Flag</span><span class="sxs-lookup"><span data-stu-id="dad61-158">EnableBgp Flag</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad61-159">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="dad61-159">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="dad61-160">Kennzeichnen zum Aktivieren von privater IPAddress auf einem Gateway für virtuelle Netzwerke</span><span class="sxs-lookup"><span data-stu-id="dad61-160">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="dad61-161">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="dad61-161">-Force</span></span>
<span data-ttu-id="dad61-162">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="dad61-162">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="dad61-163">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="dad61-163">-GatewayDefaultSite</span></span>
<span data-ttu-id="dad61-164">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="dad61-164">GatewayDefaultSite</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad61-165">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="dad61-165">-GatewaySku</span></span>
<span data-ttu-id="dad61-166">Die Gateway-Sku-Ebene</span><span class="sxs-lookup"><span data-stu-id="dad61-166">The Gateway Sku Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw4, VpnGw5, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, VpnGw4AZ, VpnGw5AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad61-167">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="dad61-167">-GatewayType</span></span>
<span data-ttu-id="dad61-168">Der Typ dieses virtuellen Netzwerkgateways: Vpn, ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="dad61-168">The type of this virtual network gateway: Vpn, ExpressRoute</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Vpn, ExpressRoute

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad61-169">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="dad61-169">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="dad61-170">Die BgpPeeringAddresses für Virtual Network Gateway bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="dad61-170">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad61-171">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="dad61-171">-IpConfigurations</span></span>
<span data-ttu-id="dad61-172">Das IpConfigurations für Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="dad61-172">The IpConfigurations for Virtual network gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad61-173">-Location</span><span class="sxs-lookup"><span data-stu-id="dad61-173">-Location</span></span>
<span data-ttu-id="dad61-174">speicherort.</span><span class="sxs-lookup"><span data-stu-id="dad61-174">location.</span></span>

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

### <span data-ttu-id="dad61-175">-Name</span><span class="sxs-lookup"><span data-stu-id="dad61-175">-Name</span></span>
<span data-ttu-id="dad61-176">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="dad61-176">The resource name.</span></span>

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

### <span data-ttu-id="dad61-177">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="dad61-177">-PeerWeight</span></span>
<span data-ttu-id="dad61-178">Die Gewichtung, die routen hinzugefügt wird, die über BGP von diesem virtuellen Netzwerkgateway gelernt wurden</span><span class="sxs-lookup"><span data-stu-id="dad61-178">The weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad61-179">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="dad61-179">-RadiusServerAddress</span></span>
<span data-ttu-id="dad61-180">P2S-Serveradresse für externen Radius.</span><span class="sxs-lookup"><span data-stu-id="dad61-180">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad61-181">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="dad61-181">-RadiusServerList</span></span>
<span data-ttu-id="dad61-182">P2S mehrere externe Radiusserverserver.</span><span class="sxs-lookup"><span data-stu-id="dad61-182">P2S multiple external Radius server servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: MultipleRadiusServersConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad61-183">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="dad61-183">-RadiusServerSecret</span></span>
<span data-ttu-id="dad61-184">P2S External Radius server secret.</span><span class="sxs-lookup"><span data-stu-id="dad61-184">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad61-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dad61-185">-ResourceGroupName</span></span>
<span data-ttu-id="dad61-186">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dad61-186">The resource group name.</span></span>

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

### <span data-ttu-id="dad61-187">-Tag</span><span class="sxs-lookup"><span data-stu-id="dad61-187">-Tag</span></span>
<span data-ttu-id="dad61-188">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="dad61-188">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="dad61-189">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="dad61-189">-VpnClientAddressPool</span></span>
<span data-ttu-id="dad61-190">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="dad61-190">P2S VpnClient AddressPool</span></span>

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

### <span data-ttu-id="dad61-191">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="dad61-191">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="dad61-192">Eine Liste der IPSec-Richtlinien für P2S-VPN-Client-Tunnelprotokolle.</span><span class="sxs-lookup"><span data-stu-id="dad61-192">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad61-193">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="dad61-193">-VpnClientProtocol</span></span>
<span data-ttu-id="dad61-194">Die Liste der P2S-VPN-Client-Tunnelprotokolle</span><span class="sxs-lookup"><span data-stu-id="dad61-194">The list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad61-195">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="dad61-195">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="dad61-196">Die Liste der VpnClientCertificates, die widerrufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dad61-196">The list of VpnClientCertificates to be revoked.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad61-197">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="dad61-197">-VpnClientRootCertificates</span></span>
<span data-ttu-id="dad61-198">Die Liste der vpnClientRootCertificates, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dad61-198">The list of VpnClientRootCertificates to be added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad61-199">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="dad61-199">-VpnGatewayGeneration</span></span>
<span data-ttu-id="dad61-200">Die Generation für dieses VirtualNetwork VPN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="dad61-200">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="dad61-201">Muss Keine sein, wenn GatewayType kein VPN ist.</span><span class="sxs-lookup"><span data-stu-id="dad61-201">Must be None if GatewayType is not VPN.</span></span>

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

### <span data-ttu-id="dad61-202">-VpnType</span><span class="sxs-lookup"><span data-stu-id="dad61-202">-VpnType</span></span>
<span data-ttu-id="dad61-203">Der Typ des Vpn:PolicyBased/RouteBased</span><span class="sxs-lookup"><span data-stu-id="dad61-203">The type of the Vpn:PolicyBased/RouteBased</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PolicyBased, RouteBased

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad61-204">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dad61-204">-Confirm</span></span>
<span data-ttu-id="dad61-205">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dad61-205">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad61-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dad61-206">-WhatIf</span></span>
<span data-ttu-id="dad61-207">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dad61-207">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dad61-208">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dad61-208">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad61-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad61-209">CommonParameters</span></span>
<span data-ttu-id="dad61-210">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dad61-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad61-211">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dad61-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad61-212">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dad61-212">INPUTS</span></span>

### <span data-ttu-id="dad61-213">System.String</span><span class="sxs-lookup"><span data-stu-id="dad61-213">System.String</span></span>

### <span data-ttu-id="dad61-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="dad61-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="dad61-215">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dad61-215">System.Boolean</span></span>

### <span data-ttu-id="dad61-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dad61-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="dad61-217">System.String[]</span><span class="sxs-lookup"><span data-stu-id="dad61-217">System.String[]</span></span>

### <span data-ttu-id="dad61-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="dad61-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="dad61-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span><span class="sxs-lookup"><span data-stu-id="dad61-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="dad61-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="dad61-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="dad61-221">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="dad61-221">System.UInt32</span></span>

### <span data-ttu-id="dad61-222">System.Int32</span><span class="sxs-lookup"><span data-stu-id="dad61-222">System.Int32</span></span>

### <span data-ttu-id="dad61-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span><span class="sxs-lookup"><span data-stu-id="dad61-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="dad61-224">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="dad61-224">System.Collections.Hashtable</span></span>

### <span data-ttu-id="dad61-225">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="dad61-225">System.Security.SecureString</span></span>

## <span data-ttu-id="dad61-226">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dad61-226">OUTPUTS</span></span>

### <span data-ttu-id="dad61-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dad61-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="dad61-228">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dad61-228">NOTES</span></span>

## <span data-ttu-id="dad61-229">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dad61-229">RELATED LINKS</span></span>
