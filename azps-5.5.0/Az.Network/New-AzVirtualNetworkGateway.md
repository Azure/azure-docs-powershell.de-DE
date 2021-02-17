---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: c6c3e7826b7b9c8aa80e362ad579c1875d53bbce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169799"
---
# <span data-ttu-id="d0cce-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d0cce-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="d0cce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0cce-102">SYNOPSIS</span></span>
<span data-ttu-id="d0cce-103">Erstellt ein virtuelles Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="d0cce-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="d0cce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0cce-104">SYNTAX</span></span>

### <span data-ttu-id="d0cce-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="d0cce-105">Default (Default)</span></span>
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

### <span data-ttu-id="d0cce-106">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0cce-106">MultipleRadiusServersConfiguration</span></span>
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

### <span data-ttu-id="d0cce-107">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0cce-107">RadiusServerConfiguration</span></span>
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

### <span data-ttu-id="d0cce-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0cce-108">AadAuthenticationConfiguration</span></span>
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

## <span data-ttu-id="d0cce-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0cce-109">DESCRIPTION</span></span>
<span data-ttu-id="d0cce-110">Das virtuelle Netzwerkgateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="d0cce-110">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="d0cce-111">Das **Cmdlet "New-AzVirtualNetworkGateway"** erstellt das Objekt Ihres Gateways in Azure basierend auf dem Namen, dem Ressourcengruppennamen, dem Standort und der IP-Konfiguration sowie dem Gatewaytyp und, falls VPN, dem VPN-Typ.</span><span class="sxs-lookup"><span data-stu-id="d0cce-111">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="d0cce-112">Sie können die Gateway-SKU auch benennen.</span><span class="sxs-lookup"><span data-stu-id="d0cce-112">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="d0cce-113">Wenn dieses Gateway für Punkt-zu-Website-Verbindungen verwendet wird, müssen Sie auch den VPN-Clientadressenpool, aus dem Verbindungsclients Adressen zugewiesen werden sollen, sowie das VPN-Clientstammzertifikat, das zum Authentifizieren von VPN-Clients verwendet wird, die eine Verbindung mit dem Gateway herstellen.</span><span class="sxs-lookup"><span data-stu-id="d0cce-113">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="d0cce-114">Sie können auch andere Features wie BGP und Active-Active verwenden.</span><span class="sxs-lookup"><span data-stu-id="d0cce-114">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="d0cce-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d0cce-115">EXAMPLES</span></span>

### <span data-ttu-id="d0cce-116">Beispiel 1: Erstellen eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="d0cce-116">Example 1: Create a Virtual Network Gateway</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="d0cce-117">Im vorstehenden Beispiel wird eine Ressourcengruppe erstellt, eine öffentliche IP-Adresse, ein virtuelles Netzwerk und ein Subnetz sowie ein virtuelles Netzwerkgateway in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="d0cce-117">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="d0cce-118">Das Gateway wird in der Ressourcengruppe "vnet-gateway" am Standort "UK West" mit den zuvor erstellten IP-Konfigurationen, die in der Variablen "ngwIPConfig", dem Gatewaytyp "VPN", dem Vpntyp "RouteBased" und der SKU "Basic" gespeichert wurden, als "myNGW" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d0cce-118">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="d0cce-119">Beispiel 2: Erstellen eines virtuellen Netzwerkgateways mit einer Konfiguration mit externem Radius</span><span class="sxs-lookup"><span data-stu-id="d0cce-119">Example 2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
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

<span data-ttu-id="d0cce-120">Im vorstehenden Beispiel wird eine Ressourcengruppe erstellt, eine öffentliche IP-Adresse, ein virtuelles Netzwerk und ein Subnetz sowie ein virtuelles Netzwerkgateway in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="d0cce-120">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="d0cce-121">Das Gateway wird in der Ressourcengruppe "vnet-gateway" am Standort "UK West" mit den zuvor erstellten IP-Konfigurationen, die in der Variablen "ngwIPConfig", dem Gatewaytyp "VPN", dem Vpntyp "RouteBased" und der SKU "Basic" gespeichert wurden, als "myNGW" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d0cce-121">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="d0cce-122">Außerdem wird ein externer Radiusserver mit der Adresse "TestRadiusServer" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d0cce-122">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="d0cce-123">Außerdem werden benutzerdefinierte Routen festgelegt, die von Kunden auf dem Gateway angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d0cce-123">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="d0cce-124">Beispiel 3: Erstellen eines virtuellen Netzwerkgateways mit P2S-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d0cce-124">Example 3: Create a Virtual Network Gateway with P2S settings</span></span>
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

<span data-ttu-id="d0cce-125">Im vorstehenden Beispiel wird eine Ressourcengruppe erstellt, eine öffentliche IP-Adresse, ein virtuelles Netzwerk und ein Subnetz sowie ein virtuelles Netzwerkgateway mit P2S-Einstellungen erstellt, z. B. "VpnProtocol", "VpnClientAddressPool", "VpnClientRootCertificates", "VpnClientIpsecPolicy" usw. in Azure.</span><span class="sxs-lookup"><span data-stu-id="d0cce-125">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="d0cce-126">Das Gateway wird in der Ressourcengruppe "vnet-gateway" am Standort "UK West" mit den zuvor erstellten IP-Konfigurationen, die in der Variablen "ngwIPConfig", dem Gatewaytyp "VPN", dem Vpntyp "RouteBased" und der SKU "VpnGw1" gespeichert wurden, als "myNGW" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d0cce-126">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="d0cce-127">Vpn-Einstellungen werden auf dem Gateway festgelegt, z. B. "VpnProtocol" als "Ikev2", "VpnClientAddressPool" als "201.169.0.0/16", "VpnClientRootCertificate" als "passed One" festgelegt: "clientRootCertName" und "custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="d0cce-127">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="d0cce-128">Außerdem werden benutzerdefinierte Routen festgelegt, die von Kunden auf dem Gateway angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d0cce-128">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="d0cce-129">Beispiel 4: Erstellen eines virtuellen Netzwerkgateways mit einer AAD-Authentifizierungskonfiguration für VpnClient des virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="d0cce-129">Example 4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
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

<span data-ttu-id="d0cce-130">Im vorstehenden Beispiel wird eine Ressourcengruppe erstellt, eine öffentliche IP-Adresse, ein virtuelles Netzwerk und ein Subnetz sowie ein virtuelles Netzwerkgateway in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="d0cce-130">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="d0cce-131">Das Gateway wird in der Ressourcengruppe "vnet-gateway" am Standort "UK West" mit den zuvor erstellten IP-Konfigurationen, die in der Variablen "ngwIPConfig", dem Gatewaytyp "VPN", dem Vpntyp "RouteBased" und der SKU "Basic" gespeichert wurden, als "myNGW" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d0cce-131">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="d0cce-132">Außerdem werden AAD-Authentifizierungskonfigurationen konfiguriert: AadTenantUri, AadIssuerUri und AadAudienceId für VpnClient des virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="d0cce-132">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="d0cce-133">Beispiel 5: Erstellen eines virtuellen Netzwerkgateways mit VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="d0cce-133">Example 5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="d0cce-134">Im vorstehenden Beispiel wird eine Ressourcengruppe erstellt, eine öffentliche IP-Adresse, ein virtuelles Netzwerk und ein Subnetz sowie ein virtuelles Netzwerkgateway in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="d0cce-134">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="d0cce-135">Das Gateway wird in der Ressourcengruppe "vnet-gateway" am Standort "UK West" mit den zuvor erstellten IP-Konfigurationen, die in der Variablen "ngwIPConfig", dem Gatewaytyp "VPN", dem vpn-Typ "RouteBased", der SKU "VpnGw4" und der aktivierten VpnGatewayGeneration Generation2 gespeichert sind, als "myNGW" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d0cce-135">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="d0cce-136">Beispiel 6: Erstellen eines virtuellen Netzwerkgateways mit IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="d0cce-136">Example 6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
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

<span data-ttu-id="d0cce-137">Im vorstehenden Beispiel wird eine Ressourcengruppe erstellt, eine öffentliche IP-Adresse, ein virtuelles Netzwerk und ein Subnetz sowie ein virtuelles Netzwerkgateway in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="d0cce-137">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="d0cce-138">ipconfigurationId1 der gerade erstellten und in ngwipconfig gespeicherten Gateway-Ipkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="d0cce-138">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="d0cce-139">Das Gateway wird in der Ressourcengruppe "resourcegroup1resourcegroup1" am Standort "UK West" mit den zuvor erstellten IP-Konfigurationen "Bgppeering-Adresse" in der Ressourcengruppe "gw1ipconfBgp1", dem Gatewaytyp von "VPN", dem VPN-Typ "RouteBased", der SKU "VpnGw4" und aktivierter "VpnGatewayGeneration Generation2" als "Gateway1" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d0cce-139">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="d0cce-140">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0cce-140">PARAMETERS</span></span>

### <span data-ttu-id="d0cce-141">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="d0cce-141">-AadAudienceId</span></span>
<span data-ttu-id="d0cce-142">P2S AAD-Authentifizierungsoption:AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="d0cce-142">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="d0cce-143">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="d0cce-143">-AadIssuerUri</span></span>
<span data-ttu-id="d0cce-144">P2S AAD-Authentifizierungsoption:AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="d0cce-144">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="d0cce-145">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="d0cce-145">-AadTenantUri</span></span>
<span data-ttu-id="d0cce-146">P2S AAD-Authentifizierungsoption:AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="d0cce-146">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="d0cce-147">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0cce-147">-AsJob</span></span>
<span data-ttu-id="d0cce-148">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d0cce-148">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0cce-149">-Asn</span><span class="sxs-lookup"><span data-stu-id="d0cce-149">-Asn</span></span>
<span data-ttu-id="d0cce-150">ASN des virtuellen Netzwerkgateways für BGP über VPN</span><span class="sxs-lookup"><span data-stu-id="d0cce-150">The virtual network gateway's ASN for BGP over VPN</span></span>

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

### <span data-ttu-id="d0cce-151">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="d0cce-151">-CustomRoute</span></span>
<span data-ttu-id="d0cce-152">Vom Kunden angegebene benutzerdefinierte Routen "AddressPool"</span><span class="sxs-lookup"><span data-stu-id="d0cce-152">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="d0cce-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0cce-153">-DefaultProfile</span></span>
<span data-ttu-id="d0cce-154">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0cce-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0cce-155">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="d0cce-155">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="d0cce-156">Kennzeichnung zum Aktivieren des Active Active -Features auf einem virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="d0cce-156">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="d0cce-157">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="d0cce-157">-EnableBgp</span></span>
<span data-ttu-id="d0cce-158">EnableBgp Flag</span><span class="sxs-lookup"><span data-stu-id="d0cce-158">EnableBgp Flag</span></span>

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

### <span data-ttu-id="d0cce-159">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="d0cce-159">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="d0cce-160">Flag zum Aktivieren der privaten "IPAddress" auf einem virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="d0cce-160">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="d0cce-161">-Force</span><span class="sxs-lookup"><span data-stu-id="d0cce-161">-Force</span></span>
<span data-ttu-id="d0cce-162">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="d0cce-162">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d0cce-163">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="d0cce-163">-GatewayDefaultSite</span></span>
<span data-ttu-id="d0cce-164">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="d0cce-164">GatewayDefaultSite</span></span>

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

### <span data-ttu-id="d0cce-165">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="d0cce-165">-GatewaySku</span></span>
<span data-ttu-id="d0cce-166">Die Gateway-SKU-Stufe</span><span class="sxs-lookup"><span data-stu-id="d0cce-166">The Gateway Sku Tier</span></span>

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

### <span data-ttu-id="d0cce-167">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="d0cce-167">-GatewayType</span></span>
<span data-ttu-id="d0cce-168">Der Typ dieses virtuellen Netzwerkgateways: Vpn, ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="d0cce-168">The type of this virtual network gateway: Vpn, ExpressRoute</span></span>

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

### <span data-ttu-id="d0cce-169">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="d0cce-169">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="d0cce-170">Die BgpPeeringAddresses für virtual network gateway bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="d0cce-170">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="d0cce-171">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="d0cce-171">-IpConfigurations</span></span>
<span data-ttu-id="d0cce-172">Die IpConfigurations für das virtuelle Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="d0cce-172">The IpConfigurations for Virtual network gateway.</span></span>

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

### <span data-ttu-id="d0cce-173">-Location</span><span class="sxs-lookup"><span data-stu-id="d0cce-173">-Location</span></span>
<span data-ttu-id="d0cce-174">aus.</span><span class="sxs-lookup"><span data-stu-id="d0cce-174">location.</span></span>

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

### <span data-ttu-id="d0cce-175">-Name</span><span class="sxs-lookup"><span data-stu-id="d0cce-175">-Name</span></span>
<span data-ttu-id="d0cce-176">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="d0cce-176">The resource name.</span></span>

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

### <span data-ttu-id="d0cce-177">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="d0cce-177">-PeerWeight</span></span>
<span data-ttu-id="d0cce-178">Die Gewichtung, die den über BGP über dieses virtuellen Netzwerkgateway erlernten Routen hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="d0cce-178">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="d0cce-179">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="d0cce-179">-RadiusServerAddress</span></span>
<span data-ttu-id="d0cce-180">Serveradresse des externen Radius von P2S.</span><span class="sxs-lookup"><span data-stu-id="d0cce-180">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="d0cce-181">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="d0cce-181">-RadiusServerList</span></span>
<span data-ttu-id="d0cce-182">P2S für mehrere externe Radiusserver.</span><span class="sxs-lookup"><span data-stu-id="d0cce-182">P2S multiple external Radius server servers.</span></span>

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

### <span data-ttu-id="d0cce-183">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="d0cce-183">-RadiusServerSecret</span></span>
<span data-ttu-id="d0cce-184">Geheimer Servergeheimnis des externen P2S-Radius.</span><span class="sxs-lookup"><span data-stu-id="d0cce-184">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="d0cce-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0cce-185">-ResourceGroupName</span></span>
<span data-ttu-id="d0cce-186">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d0cce-186">The resource group name.</span></span>

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

### <span data-ttu-id="d0cce-187">-Tag</span><span class="sxs-lookup"><span data-stu-id="d0cce-187">-Tag</span></span>
<span data-ttu-id="d0cce-188">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="d0cce-188">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d0cce-189">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="d0cce-189">-VpnClientAddressPool</span></span>
<span data-ttu-id="d0cce-190">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="d0cce-190">P2S VpnClient AddressPool</span></span>

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

### <span data-ttu-id="d0cce-191">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="d0cce-191">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="d0cce-192">Eine Liste der IPSec-Richtlinien für das Tunneln von P2S-VPN-Client-Protokollen.</span><span class="sxs-lookup"><span data-stu-id="d0cce-192">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="d0cce-193">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="d0cce-193">-VpnClientProtocol</span></span>
<span data-ttu-id="d0cce-194">Liste der Protokolle zum Tunneln von P2S-VPN-Clients</span><span class="sxs-lookup"><span data-stu-id="d0cce-194">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="d0cce-195">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="d0cce-195">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="d0cce-196">Die Liste der vpnClientCertificates, die widerrufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d0cce-196">The list of VpnClientCertificates to be revoked.</span></span>

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

### <span data-ttu-id="d0cce-197">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="d0cce-197">-VpnClientRootCertificates</span></span>
<span data-ttu-id="d0cce-198">Die Liste der hinzuzufügenden VpnClientRootCertificates.</span><span class="sxs-lookup"><span data-stu-id="d0cce-198">The list of VpnClientRootCertificates to be added.</span></span>

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

### <span data-ttu-id="d0cce-199">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="d0cce-199">-VpnGatewayGeneration</span></span>
<span data-ttu-id="d0cce-200">Die Generation für dieses VirtualNetwork VPN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="d0cce-200">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="d0cce-201">Muss "None" sein, wenn GatewayType kein VPN ist.</span><span class="sxs-lookup"><span data-stu-id="d0cce-201">Must be None if GatewayType is not VPN.</span></span>

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

### <span data-ttu-id="d0cce-202">-VpnType</span><span class="sxs-lookup"><span data-stu-id="d0cce-202">-VpnType</span></span>
<span data-ttu-id="d0cce-203">Der Typ von "Vpn:PolicyBased/RouteBased"</span><span class="sxs-lookup"><span data-stu-id="d0cce-203">The type of the Vpn:PolicyBased/RouteBased</span></span>

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

### <span data-ttu-id="d0cce-204">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0cce-204">-Confirm</span></span>
<span data-ttu-id="d0cce-205">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d0cce-205">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0cce-206">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d0cce-206">-WhatIf</span></span>
<span data-ttu-id="d0cce-207">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d0cce-207">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0cce-208">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d0cce-208">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0cce-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0cce-209">CommonParameters</span></span>
<span data-ttu-id="d0cce-210">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0cce-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0cce-211">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0cce-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0cce-212">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d0cce-212">INPUTS</span></span>

### <span data-ttu-id="d0cce-213">System.String</span><span class="sxs-lookup"><span data-stu-id="d0cce-213">System.String</span></span>

### <span data-ttu-id="d0cce-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="d0cce-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="d0cce-215">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d0cce-215">System.Boolean</span></span>

### <span data-ttu-id="d0cce-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d0cce-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="d0cce-217">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d0cce-217">System.String[]</span></span>

### <span data-ttu-id="d0cce-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="d0cce-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="d0cce-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span><span class="sxs-lookup"><span data-stu-id="d0cce-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="d0cce-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="d0cce-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="d0cce-221">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="d0cce-221">System.UInt32</span></span>

### <span data-ttu-id="d0cce-222">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d0cce-222">System.Int32</span></span>

### <span data-ttu-id="d0cce-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span><span class="sxs-lookup"><span data-stu-id="d0cce-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="d0cce-224">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d0cce-224">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d0cce-225">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="d0cce-225">System.Security.SecureString</span></span>

## <span data-ttu-id="d0cce-226">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d0cce-226">OUTPUTS</span></span>

### <span data-ttu-id="d0cce-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d0cce-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d0cce-228">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d0cce-228">NOTES</span></span>

## <span data-ttu-id="d0cce-229">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d0cce-229">RELATED LINKS</span></span>
