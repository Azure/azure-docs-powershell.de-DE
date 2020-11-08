---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: 3c30f7a341615b7e12843f3cd745cd691fa205aa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003439"
---
# <span data-ttu-id="f46a1-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f46a1-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="f46a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f46a1-102">SYNOPSIS</span></span>
<span data-ttu-id="f46a1-103">Erstellt ein virtuelles Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="f46a1-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="f46a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f46a1-104">SYNTAX</span></span>

### <span data-ttu-id="f46a1-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="f46a1-105">Default (Default)</span></span>
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

### <span data-ttu-id="f46a1-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f46a1-106">RadiusServerConfiguration</span></span>
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

### <span data-ttu-id="f46a1-107">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="f46a1-107">AadAuthenticationConfiguration</span></span>
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

## <span data-ttu-id="f46a1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f46a1-108">DESCRIPTION</span></span>
<span data-ttu-id="f46a1-109">Das virtuelle Netzwerkgateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="f46a1-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="f46a1-110">Das Cmdlet **New-AzVirtualNetworkGateway** erstellt das Objekt Ihres Gateways in Azure basierend auf dem Namen, dem Namen der Ressourcengruppe, dem Speicherort und der IP-Konfiguration sowie dem Gatewayserver und dem VPN-Typ.</span><span class="sxs-lookup"><span data-stu-id="f46a1-110">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="f46a1-111">Sie können auch die Gateway-SKU benennen.</span><span class="sxs-lookup"><span data-stu-id="f46a1-111">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="f46a1-112">Wenn dieses Gateway für Punkt-zu-Standort-Verbindungen verwendet wird, müssen Sie auch den VPN-Client Adress Pool einbeziehen, aus dem die Adressen verbunden werden sollen, und das VPN-Client-Stammzertifikat, das zum Authentifizieren von VPN-Clients verwendet wird, die eine Verbindung mit dem Gateway herstellen.</span><span class="sxs-lookup"><span data-stu-id="f46a1-112">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="f46a1-113">Sie können auch andere Features wie "BGP" und "Active-Active" hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f46a1-113">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="f46a1-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f46a1-114">EXAMPLES</span></span>

### <span data-ttu-id="f46a1-115">1: Erstellen eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="f46a1-115">1: Create a Virtual Network Gateway</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="f46a1-116">Das obige wird eine Ressourcengruppe erstellen, eine öffentliche IP-Adresse anfordern, ein virtuelles Netzwerk und ein Subnetz erstellen und ein virtuelles Netzwerk Gateway in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="f46a1-116">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f46a1-117">Das Gateway wird innerhalb der Ressourcengruppe "vnet-Gateway" in der Position "UK West" als "myNGW" bezeichnet, wobei die zuvor erstellten IP-Konfigurationen in der Variablen "ngwIPConfig", dem Gatewaytyp "VPN", dem VPN-Typ "RouteBased" und der SKU "Basic" gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="f46a1-117">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="f46a1-118">2: Erstellen eines virtuellen Netzwerkgateways mit externer RADIUS-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="f46a1-118">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="f46a1-119">Das obige wird eine Ressourcengruppe erstellen, eine öffentliche IP-Adresse anfordern, ein virtuelles Netzwerk und ein Subnetz erstellen und ein virtuelles Netzwerk Gateway in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="f46a1-119">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f46a1-120">Das Gateway wird innerhalb der Ressourcengruppe "vnet-Gateway" in der Position "UK West" als "myNGW" bezeichnet, wobei die zuvor erstellten IP-Konfigurationen in der Variablen "ngwIPConfig", dem Gatewaytyp "VPN", dem VPN-Typ "RouteBased" und der SKU "Basic" gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="f46a1-120">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="f46a1-121">Außerdem wird ein externer RADIUS-Server mit der Adresse "TestRadiusServer" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f46a1-121">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="f46a1-122">Außerdem werden benutzerdefinierte Routen festgelegt, die von Kunden auf dem Gateway angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f46a1-122">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="f46a1-123">3: Erstellen eines virtuellen Netzwerkgateways mit P2S-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="f46a1-123">3: Create a Virtual Network Gateway with P2S settings</span></span>
```
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

<span data-ttu-id="f46a1-124">Im obigen Beispiel wird eine Ressourcengruppe erstellt, eine öffentliche IP-Adresse angefordert, ein virtuelles Netzwerk und Subnetz erstellt und ein virtuelles Netzwerk Gateway mit P2S-Einstellungen wie VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy usw. in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="f46a1-124">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="f46a1-125">Das Gateway wird innerhalb der Ressourcengruppe "vnet-Gateway" in der Position "UK West" als "myNGW" bezeichnet, wobei die zuvor erstellten IP-Konfigurationen in der Variablen "ngwIPConfig", dem Gatewaytyp "VPN", dem VPN-Typ "RouteBased" und der SKU "VpnGw1" gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="f46a1-125">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="f46a1-126">VPN-Einstellungen werden auf dem Gateway wie VpnProtocol-Satz als Ikev2, VpnClientAddressPool als "201.169.0.0/16", VpnClientRootCertificate, wie übergeben: clientRootCertName und benutzerdefinierte VPN-IPSec-Richtlinie, die in Object übergeben wurde: $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="f46a1-126">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="f46a1-127">Außerdem werden benutzerdefinierte Routen festgelegt, die von Kunden auf dem Gateway angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f46a1-127">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="f46a1-128">4: Erstellen eines virtuellen Netzwerkgateways mit Aad-Authentifizierungskonfiguration für VpnClient des virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="f46a1-128">4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol OpenVPN   -VpnClientAddressPool 201.169.0.0/16 -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"
```

<span data-ttu-id="f46a1-129">Das obige wird eine Ressourcengruppe erstellen, eine öffentliche IP-Adresse anfordern, ein virtuelles Netzwerk und ein Subnetz erstellen und ein virtuelles Netzwerk Gateway in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="f46a1-129">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f46a1-130">Das Gateway wird innerhalb der Ressourcengruppe "vnet-Gateway" in der Position "UK West" als "myNGW" bezeichnet, wobei die zuvor erstellten IP-Konfigurationen in der Variablen "ngwIPConfig", dem Gatewaytyp "VPN", dem VPN-Typ "RouteBased" und der SKU "Basic" gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="f46a1-130">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="f46a1-131">Außerdem werden Aad-Authentifizierungs Konfigurationen konfiguriert: AadTenantUri, AadIssuerUri und AadAudienceId für VpnClient des virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="f46a1-131">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="f46a1-132">5: Erstellen eines virtuellen Netzwerkgateways mit VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="f46a1-132">5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="f46a1-133">Das obige wird eine Ressourcengruppe erstellen, eine öffentliche IP-Adresse anfordern, ein virtuelles Netzwerk und ein Subnetz erstellen und ein virtuelles Netzwerk Gateway in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="f46a1-133">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f46a1-134">Das Gateway wird "myNGW" innerhalb der Ressourcengruppe "vnet-Gateway" in der Position "UK West" mit den zuvor erstellten IP-Konfigurationen, die in der Variablen "ngwIPConfig" gespeichert sind, dem Gatewaytyp "VPN", dem VPN-Typ "RouteBased", der SKU "VpnGw4" und VpnGatewayGeneration Generation2 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f46a1-134">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="f46a1-135">6: Erstellen eines virtuellen Netzwerkgateways mit IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="f46a1-135">6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
```
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

<span data-ttu-id="f46a1-136">Das obige wird eine Ressourcengruppe erstellen, eine öffentliche IP-Adresse anfordern, ein virtuelles Netzwerk und ein Subnetz erstellen und ein virtuelles Netzwerk Gateway in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="f46a1-136">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f46a1-137">ipconfigurationId1 des Gateway-IPKonfigurationsdateiAddress, das soeben in ngwipconfig erstellt und gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="f46a1-137">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="f46a1-138">Das Gateway wird "gateway1" innerhalb der Ressourcengruppe "resourcegroup1resourcegroup1" am Standort "UK West" mit der zuvor erstellten IP-Konfiguration Bgppeering Adresse, die in der Variablen "gw1ipconfBgp1" gespeichert ist, dem Gatewaytyp "VPN", dem VPN-Typ "RouteBased", dem Typ "VpnGw4" und der VpnGatewayGeneration-Generation2 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f46a1-138">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="f46a1-139">Parameter</span><span class="sxs-lookup"><span data-stu-id="f46a1-139">PARAMETERS</span></span>

### <span data-ttu-id="f46a1-140">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="f46a1-140">-AadAudienceId</span></span>
<span data-ttu-id="f46a1-141">P2S Aad-Authentifizierungsoption: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="f46a1-141">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="f46a1-142">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="f46a1-142">-AadIssuerUri</span></span>
<span data-ttu-id="f46a1-143">P2S Aad-Authentifizierungsoption: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="f46a1-143">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="f46a1-144">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="f46a1-144">-AadTenantUri</span></span>
<span data-ttu-id="f46a1-145">P2S Aad-Authentifizierungsoption: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="f46a1-145">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="f46a1-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f46a1-146">-AsJob</span></span>
<span data-ttu-id="f46a1-147">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f46a1-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f46a1-148">-ASN</span><span class="sxs-lookup"><span data-stu-id="f46a1-148">-Asn</span></span>
<span data-ttu-id="f46a1-149">ASN für BGP des virtuellen Netzwerkgateways über VPN</span><span class="sxs-lookup"><span data-stu-id="f46a1-149">The virtual network gateway's ASN for BGP over VPN</span></span>

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

### <span data-ttu-id="f46a1-150">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="f46a1-150">-CustomRoute</span></span>
<span data-ttu-id="f46a1-151">Vom Kunden angegebene benutzerdefinierte Routen AddressPool</span><span class="sxs-lookup"><span data-stu-id="f46a1-151">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="f46a1-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f46a1-152">-DefaultProfile</span></span>
<span data-ttu-id="f46a1-153">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f46a1-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f46a1-154">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="f46a1-154">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="f46a1-155">Flag zum Aktivieren des aktiven aktiven Features auf dem virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="f46a1-155">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="f46a1-156">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="f46a1-156">-EnableBgp</span></span>
<span data-ttu-id="f46a1-157">EnableBgp-Flag</span><span class="sxs-lookup"><span data-stu-id="f46a1-157">EnableBgp Flag</span></span>

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

### <span data-ttu-id="f46a1-158">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f46a1-158">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="f46a1-159">Flag zum Aktivieren von privater IPAddress auf dem virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="f46a1-159">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="f46a1-160">-Force</span><span class="sxs-lookup"><span data-stu-id="f46a1-160">-Force</span></span>
<span data-ttu-id="f46a1-161">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="f46a1-161">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f46a1-162">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="f46a1-162">-GatewayDefaultSite</span></span>
<span data-ttu-id="f46a1-163">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="f46a1-163">GatewayDefaultSite</span></span>

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

### <span data-ttu-id="f46a1-164">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="f46a1-164">-GatewaySku</span></span>
<span data-ttu-id="f46a1-165">Die Gateway-SKU-Ebene</span><span class="sxs-lookup"><span data-stu-id="f46a1-165">The Gateway Sku Tier</span></span>

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

### <span data-ttu-id="f46a1-166">-Gatewaytype</span><span class="sxs-lookup"><span data-stu-id="f46a1-166">-GatewayType</span></span>
<span data-ttu-id="f46a1-167">Der Typ dieses virtuellen Netzwerkgateways: VPN, ExoressRoute</span><span class="sxs-lookup"><span data-stu-id="f46a1-167">The type of this virtual network gateway: Vpn, ExoressRoute</span></span>

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

### <span data-ttu-id="f46a1-168">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="f46a1-168">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="f46a1-169">Das BgpPeeringAddresses für virtuelles Netzwerkgateway-bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="f46a1-169">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="f46a1-170">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="f46a1-170">-IpConfigurations</span></span>
<span data-ttu-id="f46a1-171">Das IpConfigurations für virtuelles Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="f46a1-171">The IpConfigurations for Virtual network gateway.</span></span>

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

### <span data-ttu-id="f46a1-172">-Standort</span><span class="sxs-lookup"><span data-stu-id="f46a1-172">-Location</span></span>
<span data-ttu-id="f46a1-173">Lage.</span><span class="sxs-lookup"><span data-stu-id="f46a1-173">location.</span></span>

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

### <span data-ttu-id="f46a1-174">-Name</span><span class="sxs-lookup"><span data-stu-id="f46a1-174">-Name</span></span>
<span data-ttu-id="f46a1-175">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="f46a1-175">The resource name.</span></span>

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

### <span data-ttu-id="f46a1-176">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="f46a1-176">-PeerWeight</span></span>
<span data-ttu-id="f46a1-177">Das Gewicht, das den Routen über BGP von diesem virtuellen Netzwerkgateway hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="f46a1-177">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="f46a1-178">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="f46a1-178">-RadiusServerAddress</span></span>
<span data-ttu-id="f46a1-179">P2S-externe RADIUS-Serveradresse.</span><span class="sxs-lookup"><span data-stu-id="f46a1-179">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="f46a1-180">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="f46a1-180">-RadiusServerSecret</span></span>
<span data-ttu-id="f46a1-181">P2S externer RADIUS-Server-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="f46a1-181">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="f46a1-182">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f46a1-182">-ResourceGroupName</span></span>
<span data-ttu-id="f46a1-183">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f46a1-183">The resource group name.</span></span>

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

### <span data-ttu-id="f46a1-184">-Tag</span><span class="sxs-lookup"><span data-stu-id="f46a1-184">-Tag</span></span>
<span data-ttu-id="f46a1-185">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="f46a1-185">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f46a1-186">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="f46a1-186">-VpnClientAddressPool</span></span>
<span data-ttu-id="f46a1-187">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="f46a1-187">P2S VpnClient AddressPool</span></span>

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

### <span data-ttu-id="f46a1-188">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="f46a1-188">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="f46a1-189">Eine Liste der IPSec-Richtlinien für P2S-VPN-Client Tunneling-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="f46a1-189">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="f46a1-190">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="f46a1-190">-VpnClientProtocol</span></span>
<span data-ttu-id="f46a1-191">Liste der P2S-VPN-Client Tunneling-Protokolle</span><span class="sxs-lookup"><span data-stu-id="f46a1-191">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="f46a1-192">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="f46a1-192">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="f46a1-193">Die Liste der VpnClientCertificates, die gesperrt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f46a1-193">The list of VpnClientCertificates to be revoked.</span></span>

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

### <span data-ttu-id="f46a1-194">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="f46a1-194">-VpnClientRootCertificates</span></span>
<span data-ttu-id="f46a1-195">Die Liste der VpnClientRootCertificates, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f46a1-195">The list of VpnClientRootCertificates to be added.</span></span>

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

### <span data-ttu-id="f46a1-196">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="f46a1-196">-VpnGatewayGeneration</span></span>
<span data-ttu-id="f46a1-197">Die Generierung für dieses VirtualNetwork-VPN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="f46a1-197">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="f46a1-198">Muss None sein, wenn gatewaytype kein VPN ist.</span><span class="sxs-lookup"><span data-stu-id="f46a1-198">Must be None if GatewayType is not VPN.</span></span>

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

### <span data-ttu-id="f46a1-199">-VpnType</span><span class="sxs-lookup"><span data-stu-id="f46a1-199">-VpnType</span></span>
<span data-ttu-id="f46a1-200">Der Typ des VPNs: PolicyBased/RouteBased</span><span class="sxs-lookup"><span data-stu-id="f46a1-200">The type of the Vpn:PolicyBased/RouteBased</span></span>

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

### <span data-ttu-id="f46a1-201">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f46a1-201">-Confirm</span></span>
<span data-ttu-id="f46a1-202">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f46a1-202">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f46a1-203">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f46a1-203">-WhatIf</span></span>
<span data-ttu-id="f46a1-204">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f46a1-204">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f46a1-205">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f46a1-205">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f46a1-206">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f46a1-206">CommonParameters</span></span>
<span data-ttu-id="f46a1-207">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f46a1-207">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f46a1-208">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f46a1-208">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f46a1-209">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f46a1-209">INPUTS</span></span>

### <span data-ttu-id="f46a1-210">System. String</span><span class="sxs-lookup"><span data-stu-id="f46a1-210">System.String</span></span>

### <span data-ttu-id="f46a1-211">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="f46a1-211">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="f46a1-212">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f46a1-212">System.Boolean</span></span>

### <span data-ttu-id="f46a1-213">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f46a1-213">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="f46a1-214">System. String []</span><span class="sxs-lookup"><span data-stu-id="f46a1-214">System.String[]</span></span>

### <span data-ttu-id="f46a1-215">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="f46a1-215">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="f46a1-216">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="f46a1-216">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="f46a1-217">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="f46a1-217">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="f46a1-218">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="f46a1-218">System.UInt32</span></span>

### <span data-ttu-id="f46a1-219">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f46a1-219">System.Int32</span></span>

### <span data-ttu-id="f46a1-220">Microsoft. Azure. Commands. Network. Models. PSIpConfigurationBgpPeeringAddress []</span><span class="sxs-lookup"><span data-stu-id="f46a1-220">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="f46a1-221">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f46a1-221">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f46a1-222">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="f46a1-222">System.Security.SecureString</span></span>

## <span data-ttu-id="f46a1-223">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f46a1-223">OUTPUTS</span></span>

### <span data-ttu-id="f46a1-224">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f46a1-224">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f46a1-225">Notizen</span><span class="sxs-lookup"><span data-stu-id="f46a1-225">NOTES</span></span>

## <span data-ttu-id="f46a1-226">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f46a1-226">RELATED LINKS</span></span>
