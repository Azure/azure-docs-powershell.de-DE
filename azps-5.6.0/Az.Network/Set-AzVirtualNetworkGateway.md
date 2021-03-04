---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 17d9e024d13db1871bfab3b5b7230391fe22d192
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938008"
---
# <span data-ttu-id="63e0a-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="63e0a-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="63e0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63e0a-102">SYNOPSIS</span></span>
<span data-ttu-id="63e0a-103">Aktualisiert ein virtuelles Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="63e0a-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="63e0a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63e0a-104">SYNTAX</span></span>

### <span data-ttu-id="63e0a-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="63e0a-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63e0a-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="63e0a-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e0a-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="63e0a-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RemoveAadAuthentication] [-CustomRoute <String[]>] -Tag <Hashtable>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e0a-108">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="63e0a-108">MultipleRadiusServersConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerList <PSRadiusServer[]>
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e0a-109">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="63e0a-109">AadAuthenticationConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -AadTenantUri <String>
 -AadAudienceId <String> -AadIssuerUri <String> [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e0a-110">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="63e0a-110">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63e0a-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63e0a-111">DESCRIPTION</span></span>
<span data-ttu-id="63e0a-112">Das **Cmdlet Set-AzVirtualNetworkGateway** aktualisiert ein Gateway für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="63e0a-112">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="63e0a-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="63e0a-113">EXAMPLES</span></span>

### <span data-ttu-id="63e0a-114">Beispiel 1: Aktualisieren des ASN eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="63e0a-114">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="63e0a-115">Der erste Befehl ruft ein virtuelles Netzwerkgateway namens Gateway01 ab, das zur Ressourcengruppe ResourceGroup001 gehört, und speichert es in der Variablen $Gateway Mit dem zweiten Befehl wird das virtuelle Netzwerkgateway aktualisiert, das in variablen $Gateway.</span><span class="sxs-lookup"><span data-stu-id="63e0a-115">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="63e0a-116">Der Befehl legt außerdem den ASN auf 1337 fest.</span><span class="sxs-lookup"><span data-stu-id="63e0a-116">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="63e0a-117">Beispiel 2: Hinzufügen einer IPsec-Richtlinie zu einem Gateway für virtuelle Netzwerke</span><span class="sxs-lookup"><span data-stu-id="63e0a-117">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="63e0a-118">Der erste Befehl ruft ein virtuelles Netzwerkgateway namens Gateway01 ab, das zur Ressourcengruppe ResourceGroup001 gehört, und speichert es in der Variablen mit dem Namen $Gateway Der zweite Befehl erstellt das Vpn-ipsec-Richtlinienobjekt nach den angegebenen ipsec-Parametern.</span><span class="sxs-lookup"><span data-stu-id="63e0a-118">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="63e0a-119">Mit dem dritten Befehl wird das gateway für virtuelle Netzwerke aktualisiert, das in variablen $Gateway.</span><span class="sxs-lookup"><span data-stu-id="63e0a-119">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="63e0a-120">Der Befehl legt außerdem die benutzerdefinierte VPN-IPSec-Richtlinie fest, die im $vpnclientipsecpolicy -Objekt auf dem Gateway für virtuelle Netzwerke angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="63e0a-120">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="63e0a-121">Beispiel 3: Hinzufügen/Aktualisieren von Tags zu einem vorhandenen Gateway für virtuelle Netzwerke</span><span class="sxs-lookup"><span data-stu-id="63e0a-121">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Tag @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
                         Name          Value
                         ============  ============
                         testtagValue  SomeKeyValue
                         testtagKey    SomeTagKey

IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/MyVnet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/Gateway001Ip"
                             },
                             "Name": "vng1ipConfig",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/Gateway001IpConfig"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "1.2.3.4",
                           "PeerWeight": 0
                         }
```

<span data-ttu-id="63e0a-122">Der erste Befehl ruft ein virtuelles Netzwerkgateway namens Gateway01 ab, das zur Ressourcengruppe ResourceGroup001 gehört, und speichert es in der Variablen $Gateway Der zweite Befehl aktualisiert das gateway01 des virtuellen Netzwerks mit den Tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span><span class="sxs-lookup"><span data-stu-id="63e0a-122">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="63e0a-123">Beispiel 4: Hinzufügen/Aktualisieren der AAD-Authentifizierungskonfiguration für VpnClient eines vorhandenen Gateways für virtuelle Netzwerke</span><span class="sxs-lookup"><span data-stu-id="63e0a-123">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
                         Name          Value
                         ============  ============
                         testtagValue  SomeKeyValue
                         testtagKey    SomeTagKey

IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/MyVnet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/Gateway001Ip"
                             },
                             "Name": "vng1ipConfig",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/Gateway001IpConfig"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
vpnClientConfiguration : {
                    "vpnClientProtocols": [
                    "OpenVPN"
                    ],

                    "vpnClientAddressPool": {
                    "addressPrefixes": [
                        "101.10.0.0/16"
                    ]
                    },
                    "vpnClientRootCertificates": "",
                    "vpnClientRevokedCertificates": "",

                    "radiusServerAddress": "",
                    "radiusServerSecret": "",
                    "aadTenantUri": "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4\",
                    "aadAudienceId": "a21fce82-76af-45e6-8583-a08cb3b956g9\",
                    "aadIssuerUri": "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/\"
                },
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "1.2.3.4",
                           "PeerWeight": 0
                         }
                         
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientRootCertificates $rootCert -RemoveAadAuthentication
```

<span data-ttu-id="63e0a-124">Der erste Befehl ruft ein virtuelles Netzwerkgateway namens Gateway01 ab, das zur Ressourcengruppe ResourceGroup001 gehört, und speichert es in der Variablen $Gateway Mit dem zweiten Befehl wird das Gateway für virtuelles Netzwerk gateway01 mit den AAD-Authentifizierungskonfigurationen params:aadTenantUri, aadAudienceId, aadIssuerUri für VpnClient aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="63e0a-124">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="63e0a-125">Mit dem dritten Befehl wird die AAD-Authentifizierungskonfiguration aus VpnClient des Gateways für virtuelle Netzwerke entfernt.</span><span class="sxs-lookup"><span data-stu-id="63e0a-125">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="63e0a-126">Beispiel 5: Hinzufügen/Aktualisieren von IpConfigurationBgpPeeringAddresses zu einem vorhandenen Gateway für virtuelle Netzwerke</span><span class="sxs-lookup"><span data-stu-id="63e0a-126">Example 5: Add/Update IpConfigurationBgpPeeringAddresses to an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>$ipconfigurationId1 = '/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default'
PS C:\>$addresslist1 = @('169.254.21.25')
PS C:\>$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -IpConfigurationBgpPeeringAddresses $gw1ipconfBgp1

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westcentralus
Id                     : /subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"a08f13d3-6106-44e0-9127-e35e6f9793d5"
ResourceGuid           : 30993429-a1ed-42ca-9862-9156b013626e
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/newApipaNet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/newapipaip"
                             },
                             "Name": "default",
                             "Etag": "W/\"a08f13d3-6106-44e0-9127-e35e6f9793d5\"",
                             "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "10.1.255.30",
                           "PeerWeight": 0,
                           "BgpPeeringAddresses": [
                             {
                               "IpconfigurationId": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default",
                               "DefaultBgpIpAddresses": [
                                 "10.1.255.30"
                               ],
                               "CustomBgpIpAddresses": [
                                 "169.254.21.55"
                               ],
                               "TunnelIpAddresses": [
                                 "13.78.146.151"
                               ]
                             }
                           ]
                         }
```

<span data-ttu-id="63e0a-127">Der erste Befehl ruft ein virtuelles Netzwerkgateway namens Gateway01 ab, das zur Ressourcengruppe ResourceGroup001 gehört, und speichert es in der Variablen $Gateway Der zweite Befehl weist den Wert des Gateway01-IpConfiguration-Id für das virtuelle Netzwerkgateway in die Variable ipconfigurationId1 zu.</span><span class="sxs-lookup"><span data-stu-id="63e0a-127">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command assigns the value of virtual network gateway Gateway01 IpConfiguration Id into variable ipconfigurationId1.</span></span>
<span data-ttu-id="63e0a-128">Der dritte Befehl weist die Adressliste der Adressliste1 zu.</span><span class="sxs-lookup"><span data-stu-id="63e0a-128">The third command assigns the address list into addresslist1.</span></span>
<span data-ttu-id="63e0a-129">Mit dem vierten Befehl wurde ein PSIpConfigurationBgpPeeringAddress-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="63e0a-129">The fourth command created a PSIpConfigurationBgpPeeringAddress object.</span></span>
<span data-ttu-id="63e0a-130">Mit dem fünften Befehl wird dieser neu erstellte PSIpConfigurationBgpPeeringAddress auf IpConfigurationBgpPeeringAddresses festgelegt und das Gateway aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="63e0a-130">The fifth command set this new created PSIpConfigurationBgpPeeringAddress to IpConfigurationBgpPeeringAddresses and update the gateway.</span></span>

## <span data-ttu-id="63e0a-131">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="63e0a-131">PARAMETERS</span></span>

### <span data-ttu-id="63e0a-132">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="63e0a-132">-AadAudienceId</span></span>
<span data-ttu-id="63e0a-133">P2S AAD-Authentifizierungsoption:AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="63e0a-133">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="63e0a-134">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="63e0a-134">-AadIssuerUri</span></span>
<span data-ttu-id="63e0a-135">P2S AAD-Authentifizierungsoption:AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="63e0a-135">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="63e0a-136">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="63e0a-136">-AadTenantUri</span></span>
<span data-ttu-id="63e0a-137">P2S AAD-Authentifizierungsoption:AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="63e0a-137">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="63e0a-138">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63e0a-138">-AsJob</span></span>
<span data-ttu-id="63e0a-139">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="63e0a-139">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63e0a-140">-Asn</span><span class="sxs-lookup"><span data-stu-id="63e0a-140">-Asn</span></span>
<span data-ttu-id="63e0a-141">ASN des virtuellen Netzwerkgateways, das zum Einrichten von BGP-Sitzungen in IPsec-Tunneln verwendet wird</span><span class="sxs-lookup"><span data-stu-id="63e0a-141">The virtual network gateway's ASN, used to set up BGP sessions inside IPsec tunnels</span></span>

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

### <span data-ttu-id="63e0a-142">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="63e0a-142">-CustomRoute</span></span>
<span data-ttu-id="63e0a-143">Vom Kunden angegebene benutzerdefinierte Routen AddressPool</span><span class="sxs-lookup"><span data-stu-id="63e0a-143">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="63e0a-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e0a-144">-DefaultProfile</span></span>
<span data-ttu-id="63e0a-145">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63e0a-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63e0a-146">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="63e0a-146">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="63e0a-147">Kennzeichnen zum Deaktivieren des Active Active-Features auf einem Gateway für virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="63e0a-147">Flag to disable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="63e0a-148">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="63e0a-148">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="63e0a-149">Kennzeichnen zum Aktivieren des Active Active-Features auf einem Gateway für virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="63e0a-149">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="63e0a-150">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="63e0a-150">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="63e0a-151">Kennzeichnen zum Aktivieren des Active Active-Features auf einem Gateway für virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="63e0a-151">Flag to enable Active Active feature on virtual network gateway</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e0a-152">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="63e0a-152">-GatewayDefaultSite</span></span>
<span data-ttu-id="63e0a-153">Die Standardwebsite, die zum Erzwingen des Tunnelns verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="63e0a-153">The default site to use for force tunneling.</span></span>
<span data-ttu-id="63e0a-154">Wenn eine Standardwebsite angegeben ist, wird der ganze Internetdatenverkehr vom vnet des Gateways an diese Website geroutet.</span><span class="sxs-lookup"><span data-stu-id="63e0a-154">If a default site is specified, all internet traffic from the gateway's vnet is routed to that site.</span></span>

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

### <span data-ttu-id="63e0a-155">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="63e0a-155">-GatewaySku</span></span>
<span data-ttu-id="63e0a-156">SKU des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="63e0a-156">The virtual network gateway's SKU</span></span>

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

### <span data-ttu-id="63e0a-157">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="63e0a-157">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="63e0a-158">Die BgpPeeringAddresses für Virtual Network Gateway bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="63e0a-158">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="63e0a-159">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="63e0a-159">-PeerWeight</span></span>
<span data-ttu-id="63e0a-160">Die Gewichtung, die routen hinzugefügt wird, die über BGP von diesem virtuellen Netzwerkgateway gelernt wurden</span><span class="sxs-lookup"><span data-stu-id="63e0a-160">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="63e0a-161">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="63e0a-161">-RadiusServerAddress</span></span>
<span data-ttu-id="63e0a-162">P2S-Serveradresse für externen Radius.</span><span class="sxs-lookup"><span data-stu-id="63e0a-162">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration, RadiusServerConfigurationUpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63e0a-163">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="63e0a-163">-RadiusServerList</span></span>
<span data-ttu-id="63e0a-164">P2S mehrere externe Radiusserver.</span><span class="sxs-lookup"><span data-stu-id="63e0a-164">P2S multiple external Radius servers.</span></span>

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

### <span data-ttu-id="63e0a-165">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="63e0a-165">-RadiusServerSecret</span></span>
<span data-ttu-id="63e0a-166">P2S External Radius server secret.</span><span class="sxs-lookup"><span data-stu-id="63e0a-166">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration, RadiusServerConfigurationUpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63e0a-167">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="63e0a-167">-RemoveAadAuthentication</span></span>
<span data-ttu-id="63e0a-168">Kennzeichnen Sie, um die AAD-Authentifizierung für den P2S-Client aus dem Gateway des virtuellen Netzwerks zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="63e0a-168">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="63e0a-169">-Tag</span><span class="sxs-lookup"><span data-stu-id="63e0a-169">-Tag</span></span>
<span data-ttu-id="63e0a-170">P2S-Serveradresse für externen Radius.</span><span class="sxs-lookup"><span data-stu-id="63e0a-170">P2S External Radius server address.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: RadiusServerConfigurationUpdateResourceWithTags, UpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e0a-171">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="63e0a-171">-VirtualNetworkGateway</span></span>
<span data-ttu-id="63e0a-172">Das Objekt des virtuellen Netzwerkgateways, um Änderungen von zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="63e0a-172">The virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="63e0a-173">Dies kann mithilfe von Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="63e0a-173">This can be retrieved using Get-AzVirtualNetworkGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63e0a-174">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="63e0a-174">-VpnClientAddressPool</span></span>
<span data-ttu-id="63e0a-175">Der Adressbereich zum Zuweisen von VPN-Client-IP-Adressen aus.</span><span class="sxs-lookup"><span data-stu-id="63e0a-175">The address space to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="63e0a-176">Dies sollte sich nicht mit virtuellen Netzwerken oder lokalen Bereichen überschneiden.</span><span class="sxs-lookup"><span data-stu-id="63e0a-176">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="63e0a-177">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="63e0a-177">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="63e0a-178">Eine Liste der IPSec-Richtlinien für P2S-VPN-Client-Tunnelprotokolle.</span><span class="sxs-lookup"><span data-stu-id="63e0a-178">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="63e0a-179">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="63e0a-179">-VpnClientProtocol</span></span>
<span data-ttu-id="63e0a-180">Eine Liste der P2S-VPN-Client-Tunnelprotokolle</span><span class="sxs-lookup"><span data-stu-id="63e0a-180">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="63e0a-181">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="63e0a-181">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="63e0a-182">Eine Liste der widerrufenen VPN-Clientzertifikate.</span><span class="sxs-lookup"><span data-stu-id="63e0a-182">A list of revoked VPN client certificates.</span></span>
<span data-ttu-id="63e0a-183">Ein VPN-Client, der ein Zertifikat präsentiert, das einem dieser Zertifikate entspricht, wird mitgeteilt, dass er abgehen soll.</span><span class="sxs-lookup"><span data-stu-id="63e0a-183">A VPN client presenting a certificate that matches one of these will be told to go away.</span></span>

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

### <span data-ttu-id="63e0a-184">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="63e0a-184">-VpnClientRootCertificates</span></span>
<span data-ttu-id="63e0a-185">Eine Liste der VPN-Clientstammzertifikate, die für die VPN-Clientauthentifizierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63e0a-185">A list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="63e0a-186">Beim Verbinden von VPN-Clients müssen Zertifikate vorhanden sein, die aus einem dieser Stammzertifikate generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="63e0a-186">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="63e0a-187">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="63e0a-187">-Confirm</span></span>
<span data-ttu-id="63e0a-188">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="63e0a-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63e0a-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63e0a-189">-WhatIf</span></span>
<span data-ttu-id="63e0a-190">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="63e0a-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63e0a-191">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63e0a-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63e0a-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e0a-192">CommonParameters</span></span>
<span data-ttu-id="63e0a-193">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63e0a-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e0a-194">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63e0a-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e0a-195">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="63e0a-195">INPUTS</span></span>

### <span data-ttu-id="63e0a-196">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="63e0a-196">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="63e0a-197">System.String</span><span class="sxs-lookup"><span data-stu-id="63e0a-197">System.String</span></span>

### <span data-ttu-id="63e0a-198">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="63e0a-198">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="63e0a-199">System.String[]</span><span class="sxs-lookup"><span data-stu-id="63e0a-199">System.String[]</span></span>

### <span data-ttu-id="63e0a-200">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="63e0a-200">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="63e0a-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span><span class="sxs-lookup"><span data-stu-id="63e0a-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="63e0a-202">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="63e0a-202">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="63e0a-203">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="63e0a-203">System.UInt32</span></span>

### <span data-ttu-id="63e0a-204">System.Int32</span><span class="sxs-lookup"><span data-stu-id="63e0a-204">System.Int32</span></span>

### <span data-ttu-id="63e0a-205">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span><span class="sxs-lookup"><span data-stu-id="63e0a-205">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="63e0a-206">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="63e0a-206">System.Security.SecureString</span></span>

## <span data-ttu-id="63e0a-207">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="63e0a-207">OUTPUTS</span></span>

### <span data-ttu-id="63e0a-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="63e0a-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="63e0a-209">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="63e0a-209">NOTES</span></span>

## <span data-ttu-id="63e0a-210">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="63e0a-210">RELATED LINKS</span></span>
