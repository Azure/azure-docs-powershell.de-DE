---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: 9b8ee02cbe28784ff1fd5789881dd62add62d674
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660467"
---
# <span data-ttu-id="2625c-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2625c-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="2625c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2625c-102">SYNOPSIS</span></span>
<span data-ttu-id="2625c-103">Erstellt ein virtuelles Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="2625c-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="2625c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2625c-104">SYNTAX</span></span>

### <span data-ttu-id="2625c-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="2625c-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2625c-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="2625c-106">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2625c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2625c-107">DESCRIPTION</span></span>
<span data-ttu-id="2625c-108">Das virtuelle Netzwerkgateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="2625c-108">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="2625c-109">Das Cmdlet **New-AzVirtualNetworkGateway** erstellt das Objekt Ihres Gateways in Azure basierend auf dem Namen, dem Namen der Ressourcengruppe, dem Speicherort und der IP-Konfiguration sowie dem Gatewayserver und dem VPN-Typ.</span><span class="sxs-lookup"><span data-stu-id="2625c-109">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="2625c-110">Sie können auch die Gateway-SKU benennen.</span><span class="sxs-lookup"><span data-stu-id="2625c-110">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="2625c-111">Wenn dieses Gateway für Punkt-zu-Standort-Verbindungen verwendet wird, müssen Sie auch den VPN-Client Adress Pool einbeziehen, aus dem die Adressen verbunden werden sollen, und das VPN-Client-Stammzertifikat, das zum Authentifizieren von VPN-Clients verwendet wird, die eine Verbindung mit dem Gateway herstellen.</span><span class="sxs-lookup"><span data-stu-id="2625c-111">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="2625c-112">Sie können auch andere Features wie "BGP" und "Active-Active" hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2625c-112">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="2625c-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2625c-113">EXAMPLES</span></span>

### <span data-ttu-id="2625c-114">1: Erstellen eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="2625c-114">1: Create a Virtual Network Gateway</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic"
```

<span data-ttu-id="2625c-115">Das obige wird eine Ressourcengruppe erstellen, eine öffentliche IP-Adresse anfordern, ein virtuelles Netzwerk und ein Subnetz erstellen und ein virtuelles Netzwerk Gateway in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="2625c-115">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="2625c-116">Das Gateway wird innerhalb der Ressourcengruppe "vnet-Gateway" in der Position "UK West" als "myNGW" bezeichnet, wobei die zuvor erstellten IP-Konfigurationen in der Variablen "ngwIPConfig", dem Gatewaytyp "VPN", dem VPN-Typ "RouteBased" und der SKU "Basic" gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="2625c-116">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="2625c-117">2: Erstellen eines virtuellen Netzwerkgateways mit externer RADIUS-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="2625c-117">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="2625c-118">Das obige wird eine Ressourcengruppe erstellen, eine öffentliche IP-Adresse anfordern, ein virtuelles Netzwerk und ein Subnetz erstellen und ein virtuelles Netzwerk Gateway in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="2625c-118">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="2625c-119">Das Gateway wird innerhalb der Ressourcengruppe "vnet-Gateway" in der Position "UK West" als "myNGW" bezeichnet, wobei die zuvor erstellten IP-Konfigurationen in der Variablen "ngwIPConfig", dem Gatewaytyp "VPN", dem VPN-Typ "RouteBased" und der SKU "Basic" gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="2625c-119">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="2625c-120">Außerdem wird ein externer RADIUS-Server mit der Adresse "TestRadiusServer" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2625c-120">It also adds an external radius server with address "TestRadiusServer"</span></span>

### <span data-ttu-id="2625c-121">1: Erstellen eines virtuellen Netzwerkgateways mit P2S-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="2625c-121">1: Create a Virtual Network Gateway with P2S settings</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$rootCert = New-AzVpnClientRootCertificate -Name $clientRootCertName -PublicCertData $samplePublicCertData
$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86471 -SADataSizeKilobytes 429496 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol IkeV2 -VpnClientAddressPool 201.169.0.0/16 -VpnClientRootCertificates $rootCert -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="2625c-122">Im obigen Beispiel wird eine Ressourcengruppe erstellt, eine öffentliche IP-Adresse angefordert, ein virtuelles Netzwerk und Subnetz erstellt und ein virtuelles Netzwerk Gateway mit P2S-Einstellungen wie VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy usw. in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="2625c-122">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="2625c-123">Das Gateway wird innerhalb der Ressourcengruppe "vnet-Gateway" in der Position "UK West" als "myNGW" bezeichnet, wobei die zuvor erstellten IP-Konfigurationen in der Variablen "ngwIPConfig", dem Gatewaytyp "VPN", dem VPN-Typ "RouteBased" und der SKU "VpnGw1" gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="2625c-123">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="2625c-124">VPN-Einstellungen werden auf dem Gateway wie VpnProtocol-Satz als Ikev2, VpnClientAddressPool als "201.169.0.0/16", VpnClientRootCertificate, wie übergeben: clientRootCertName und benutzerdefinierte VPN-IPSec-Richtlinie, die in Object übergeben wurde: $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="2625c-124">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  

## <span data-ttu-id="2625c-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="2625c-125">PARAMETERS</span></span>

### <span data-ttu-id="2625c-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2625c-126">-AsJob</span></span>
<span data-ttu-id="2625c-127">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2625c-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2625c-128">-ASN</span><span class="sxs-lookup"><span data-stu-id="2625c-128">-Asn</span></span>

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

### <span data-ttu-id="2625c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2625c-129">-DefaultProfile</span></span>
<span data-ttu-id="2625c-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2625c-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2625c-131">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="2625c-131">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="2625c-132">Aktiviert das Active-Active-Feature.</span><span class="sxs-lookup"><span data-stu-id="2625c-132">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="2625c-133">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="2625c-133">-EnableBgp</span></span>

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

### <span data-ttu-id="2625c-134">-Force</span><span class="sxs-lookup"><span data-stu-id="2625c-134">-Force</span></span>
<span data-ttu-id="2625c-135">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="2625c-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2625c-136">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="2625c-136">-GatewayDefaultSite</span></span>

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

### <span data-ttu-id="2625c-137">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="2625c-137">-GatewaySku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2625c-138">-Gatewaytype</span><span class="sxs-lookup"><span data-stu-id="2625c-138">-GatewayType</span></span>

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

### <span data-ttu-id="2625c-139">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="2625c-139">-IpConfigurations</span></span>

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

### <span data-ttu-id="2625c-140">-Standort</span><span class="sxs-lookup"><span data-stu-id="2625c-140">-Location</span></span>

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

### <span data-ttu-id="2625c-141">-Name</span><span class="sxs-lookup"><span data-stu-id="2625c-141">-Name</span></span>

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

### <span data-ttu-id="2625c-142">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="2625c-142">-PeerWeight</span></span>

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

### <span data-ttu-id="2625c-143">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="2625c-143">-RadiusServerAddress</span></span>
<span data-ttu-id="2625c-144">P2S-externe RADIUS-Serveradresse.</span><span class="sxs-lookup"><span data-stu-id="2625c-144">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="2625c-145">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="2625c-145">-RadiusServerSecret</span></span>
<span data-ttu-id="2625c-146">P2S externer RADIUS-Server-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="2625c-146">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="2625c-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2625c-147">-ResourceGroupName</span></span>

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

### <span data-ttu-id="2625c-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="2625c-148">-Tag</span></span>
<span data-ttu-id="2625c-149">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="2625c-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2625c-150">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="2625c-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2625c-151">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="2625c-151">-VpnClientAddressPool</span></span>

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

### <span data-ttu-id="2625c-152">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="2625c-152">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="2625c-153">Eine Liste der IPSec-Richtlinien für P2S-VPN-Client Tunneling-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="2625c-153">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="2625c-154">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="2625c-154">-VpnClientProtocol</span></span>
<span data-ttu-id="2625c-155">Liste der P2S-VPN-Client Tunneling-Protokolle</span><span class="sxs-lookup"><span data-stu-id="2625c-155">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="2625c-156">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="2625c-156">-VpnClientRevokedCertificates</span></span>

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

### <span data-ttu-id="2625c-157">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="2625c-157">-VpnClientRootCertificates</span></span>

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

### <span data-ttu-id="2625c-158">-VpnType</span><span class="sxs-lookup"><span data-stu-id="2625c-158">-VpnType</span></span>

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

### <span data-ttu-id="2625c-159">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2625c-159">-Confirm</span></span>
<span data-ttu-id="2625c-160">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2625c-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2625c-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2625c-161">-WhatIf</span></span>
<span data-ttu-id="2625c-162">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2625c-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2625c-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2625c-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2625c-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2625c-164">CommonParameters</span></span>
<span data-ttu-id="2625c-165">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2625c-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2625c-166">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2625c-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2625c-167">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2625c-167">INPUTS</span></span>

### <span data-ttu-id="2625c-168">System. String</span><span class="sxs-lookup"><span data-stu-id="2625c-168">System.String</span></span>

### <span data-ttu-id="2625c-169">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="2625c-169">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="2625c-170">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2625c-170">System.Boolean</span></span>

### <span data-ttu-id="2625c-171">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2625c-171">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="2625c-172">System. String []</span><span class="sxs-lookup"><span data-stu-id="2625c-172">System.String[]</span></span>

### <span data-ttu-id="2625c-173">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="2625c-173">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="2625c-174">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="2625c-174">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="2625c-175">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="2625c-175">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="2625c-176">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="2625c-176">System.UInt32</span></span>

### <span data-ttu-id="2625c-177">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2625c-177">System.Int32</span></span>

### <span data-ttu-id="2625c-178">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2625c-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2625c-179">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="2625c-179">System.Security.SecureString</span></span>

## <span data-ttu-id="2625c-180">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2625c-180">OUTPUTS</span></span>

### <span data-ttu-id="2625c-181">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2625c-181">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="2625c-182">Notizen</span><span class="sxs-lookup"><span data-stu-id="2625c-182">NOTES</span></span>

## <span data-ttu-id="2625c-183">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2625c-183">RELATED LINKS</span></span>

[<span data-ttu-id="2625c-184">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2625c-184">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="2625c-185">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2625c-185">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="2625c-186">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2625c-186">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="2625c-187">Größe ändern – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2625c-187">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="2625c-188">Satz-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2625c-188">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
