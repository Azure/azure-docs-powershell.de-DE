---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: a2aacf68d20e495856ffd6d5e868b82bed8d34ef
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849128"
---
# <span data-ttu-id="9fb1c-101">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9fb1c-101">New-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="9fb1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9fb1c-102">SYNOPSIS</span></span>
<span data-ttu-id="9fb1c-103">Erstellt ein virtuelles Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="9fb1c-103">Creates a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fb1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fb1c-104">SYNTAX</span></span>

### <span data-ttu-id="9fb1c-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="9fb1c-105">Default (Default)</span></span>
```
New-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fb1c-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fb1c-106">RadiusServerConfiguration</span></span>
```
New-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9fb1c-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9fb1c-107">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGateway
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fb1c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9fb1c-108">DESCRIPTION</span></span>
<span data-ttu-id="9fb1c-109">Das virtuelle Netzwerkgateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="9fb1c-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="9fb1c-110">Das Cmdlet **New-AzureRmVirtualNetworkGateway** erstellt das Objekt Ihres Gateways in Azure basierend auf dem Namen, dem Namen der Ressourcengruppe, dem Speicherort und der IP-Konfiguration sowie dem Gatewayserver und dem VPN-Typ.</span><span class="sxs-lookup"><span data-stu-id="9fb1c-110">The **New-AzureRmVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="9fb1c-111">Sie können auch die Gateway-SKU benennen.</span><span class="sxs-lookup"><span data-stu-id="9fb1c-111">You can also name the Gateway SKU.</span></span>

<span data-ttu-id="9fb1c-112">Wenn dieses Gateway für Punkt-zu-Standort-Verbindungen verwendet wird, müssen Sie auch den VPN-Client Adress Pool einbeziehen, aus dem die Adressen verbunden werden sollen, und das VPN-Client-Stammzertifikat, das zum Authentifizieren von VPN-Clients verwendet wird, die eine Verbindung mit dem Gateway herstellen.</span><span class="sxs-lookup"><span data-stu-id="9fb1c-112">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>

<span data-ttu-id="9fb1c-113">Sie können auch andere Features wie "BGP" und "Active-Active" hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9fb1c-113">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="9fb1c-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9fb1c-114">EXAMPLES</span></span>

### <span data-ttu-id="9fb1c-115">1: Erstellen eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="9fb1c-115">1: Create a Virtual Network Gateway</span></span>
```
New-AzureRmResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzureRMVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzureRMPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzureRmVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzureRMVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzureRmVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic"
```

<span data-ttu-id="9fb1c-116">Das obige wird eine Ressourcengruppe erstellen, eine öffentliche IP-Adresse anfordern, ein virtuelles Netzwerk und ein Subnetz erstellen und ein virtuelles Netzwerk Gateway in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="9fb1c-116">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="9fb1c-117">Das Gateway wird innerhalb der Ressourcengruppe "vnet-Gateway" in der Position "UK West" als "myNGW" bezeichnet, wobei die zuvor erstellten IP-Konfigurationen in der Variablen "ngwIPConfig", dem Gatewaytyp "VPN", dem VPN-Typ "RouteBased" und der SKU "Basic" gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="9fb1c-117">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="9fb1c-118">2: Erstellen eines virtuellen Netzwerkgateways mit externer RADIUS-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="9fb1c-118">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzureRmResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzureRMVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzureRMPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzureRmVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzureRMVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzureRmVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="9fb1c-119">Das obige wird eine Ressourcengruppe erstellen, eine öffentliche IP-Adresse anfordern, ein virtuelles Netzwerk und ein Subnetz erstellen und ein virtuelles Netzwerk Gateway in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="9fb1c-119">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="9fb1c-120">Das Gateway wird innerhalb der Ressourcengruppe "vnet-Gateway" in der Position "UK West" als "myNGW" bezeichnet, wobei die zuvor erstellten IP-Konfigurationen in der Variablen "ngwIPConfig", dem Gatewaytyp "VPN", dem VPN-Typ "RouteBased" und der SKU "Basic" gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="9fb1c-120">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="9fb1c-121">Außerdem wird ein externer RADIUS-Server mit der Adresse "TestRadiusServer" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9fb1c-121">It also adds an external radius server with address "TestRadiusServer"</span></span>

## <span data-ttu-id="9fb1c-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fb1c-122">PARAMETERS</span></span>

### <span data-ttu-id="9fb1c-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9fb1c-123">-AsJob</span></span>
<span data-ttu-id="9fb1c-124">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9fb1c-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9fb1c-125">-ASN</span><span class="sxs-lookup"><span data-stu-id="9fb1c-125">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb1c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fb1c-126">-DefaultProfile</span></span>
<span data-ttu-id="9fb1c-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9fb1c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="9fb1c-128">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="9fb1c-128">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="9fb1c-129">Aktiviert das Active-Active-Feature.</span><span class="sxs-lookup"><span data-stu-id="9fb1c-129">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="9fb1c-130">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="9fb1c-130">-EnableBgp</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb1c-131">-Force</span><span class="sxs-lookup"><span data-stu-id="9fb1c-131">-Force</span></span>
<span data-ttu-id="9fb1c-132">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9fb1c-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9fb1c-133">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="9fb1c-133">-GatewayDefaultSite</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb1c-134">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="9fb1c-134">-GatewaySku</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb1c-135">-Gatewaytype</span><span class="sxs-lookup"><span data-stu-id="9fb1c-135">-GatewayType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Vpn, ExpressRoute

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb1c-136">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="9fb1c-136">-IpConfigurations</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb1c-137">-Standort</span><span class="sxs-lookup"><span data-stu-id="9fb1c-137">-Location</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb1c-138">-Name</span><span class="sxs-lookup"><span data-stu-id="9fb1c-138">-Name</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb1c-139">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="9fb1c-139">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb1c-140">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="9fb1c-140">-RadiusServerAddress</span></span>
<span data-ttu-id="9fb1c-141">P2S-externe RADIUS-Serveradresse.</span><span class="sxs-lookup"><span data-stu-id="9fb1c-141">P2S External Radius server address.</span></span>
```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb1c-142">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="9fb1c-142">-RadiusServerSecret</span></span>
<span data-ttu-id="9fb1c-143">P2S externer RADIUS-Server-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="9fb1c-143">P2S External Radius server secret.</span></span>
```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb1c-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fb1c-144">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb1c-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="9fb1c-145">-Tag</span></span>
<span data-ttu-id="9fb1c-146">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="9fb1c-146">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9fb1c-147">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9fb1c-147">For example:</span></span>

<span data-ttu-id="9fb1c-148">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="9fb1c-148">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9fb1c-149">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="9fb1c-149">-VpnClientAddressPool</span></span>
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

### <span data-ttu-id="9fb1c-150">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="9fb1c-150">-VpnClientProtocol</span></span>
<span data-ttu-id="9fb1c-151">Liste der P2S-VPN-Client Tunneling-Protokolle</span><span class="sxs-lookup"><span data-stu-id="9fb1c-151">The list of P2S VPN client tunneling protocols</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: SSTP, IkeV2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb1c-152">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="9fb1c-152">-VpnClientRevokedCertificates</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb1c-153">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="9fb1c-153">-VpnClientRootCertificates</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb1c-154">-VpnType</span><span class="sxs-lookup"><span data-stu-id="9fb1c-154">-VpnType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PolicyBased, RouteBased

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb1c-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9fb1c-155">-Confirm</span></span>
<span data-ttu-id="9fb1c-156">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9fb1c-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fb1c-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fb1c-157">-WhatIf</span></span>
<span data-ttu-id="9fb1c-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9fb1c-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fb1c-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9fb1c-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fb1c-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fb1c-160">CommonParameters</span></span>
<span data-ttu-id="9fb1c-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fb1c-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fb1c-162">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fb1c-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fb1c-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9fb1c-163">INPUTS</span></span>

## <span data-ttu-id="9fb1c-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9fb1c-164">OUTPUTS</span></span>

### <span data-ttu-id="9fb1c-165">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9fb1c-165">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="9fb1c-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="9fb1c-166">NOTES</span></span>

## <span data-ttu-id="9fb1c-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9fb1c-167">RELATED LINKS</span></span>

[<span data-ttu-id="9fb1c-168">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9fb1c-168">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="9fb1c-169">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9fb1c-169">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="9fb1c-170">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9fb1c-170">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="9fb1c-171">Größe ändern – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9fb1c-171">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="9fb1c-172">Satz-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9fb1c-172">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)
