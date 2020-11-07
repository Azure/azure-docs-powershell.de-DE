---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: df3b8df85cd53931de5da7dc710e4558aedcdd48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823796"
---
# <span data-ttu-id="3b52a-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3b52a-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="3b52a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3b52a-102">SYNOPSIS</span></span>
<span data-ttu-id="3b52a-103">Aktualisiert ein virtuelles Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="3b52a-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="3b52a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b52a-104">SYNTAX</span></span>

### <span data-ttu-id="3b52a-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="3b52a-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b52a-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b52a-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b52a-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="3b52a-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b52a-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b52a-108">AadAuthenticationConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -AadTenantUri <String> -AadAudienceId <String> -AadIssuerUri <String> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b52a-109">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="3b52a-109">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b52a-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b52a-110">DESCRIPTION</span></span>
<span data-ttu-id="3b52a-111">Das Cmdlet " **Satz-AzVirtualNetworkGateway** " aktualisiert ein virtuelles Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="3b52a-111">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="3b52a-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b52a-112">EXAMPLES</span></span>

### <span data-ttu-id="3b52a-113">Beispiel 1: Aktualisieren des ASN eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="3b52a-113">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="3b52a-114">Der erste Befehl ruft ein virtuelles Netzwerkgateway mit dem Namen Gateway01 ab, das zu Ressourcengruppen-ResourceGroup001 gehört, und speichert es in der Variablen mit dem Namen $Gateway der zweite Befehl das virtuelle Netzwerkgateway aktualisiert, das in Variablen $Gateway gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="3b52a-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="3b52a-115">Der Befehl legt auch die ASN auf 1337 fest.</span><span class="sxs-lookup"><span data-stu-id="3b52a-115">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="3b52a-116">Beispiel 2: Hinzufügen einer IPSec-Richtlinie zu einem virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="3b52a-116">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="3b52a-117">Der erste Befehl ruft ein virtuelles Netzwerkgateway mit dem Namen Gateway01 ab, das zu Ressourcengruppen-ResourceGroup001 gehört, und speichert es in der Variablen mit dem Namen $Gateway der zweite Befehl das VPN-IPSec-Richtlinienobjekt als pro angegebene IPSec-Parameter erstellt.</span><span class="sxs-lookup"><span data-stu-id="3b52a-117">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="3b52a-118">Der dritte Befehl aktualisiert das virtuelle Netzwerkgateway, das in Variablen $Gateway gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="3b52a-118">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="3b52a-119">Der Befehl legt auch die benutzerdefinierte VPN-IPSec-Richtlinie fest, die im $vpnclientipsecpolicy-Objekt auf dem virtuellen Netzwerkgateway angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3b52a-119">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="3b52a-120">Beispiel 3: Hinzufügen/Aktualisieren von Tags zu einem vorhandenen virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="3b52a-120">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
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

<span data-ttu-id="3b52a-121">Der erste Befehl ruft ein virtuelles Netzwerkgateway mit dem Namen Gateway01 ab, das zu Ressourcengruppen-ResourceGroup001 gehört, und speichert es in der Variablen mit dem Namen $Gateway der zweite Befehl den virtuellen Netzwerkgateway-Gateway01 mit den Tags @ {testtagKey = "SomeTagKey"; testtagValue = "SomeKeyValue"} aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3b52a-121">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="3b52a-122">Beispiel 4: Hinzufügen/Aktualisieren der Aad-Authentifizierungskonfiguration für VpnClient eines vorhandenen virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="3b52a-122">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
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

<span data-ttu-id="3b52a-123">Der erste Befehl ruft ein virtuelles Netzwerkgateway mit dem Namen Gateway01 ab, das zu Ressourcengruppen-ResourceGroup001 gehört, und speichert es in der Variablen mit dem Namen $Gateway der zweite Befehl den virtuellen Netzwerkgateway-Gateway01 mit den Aad-Authentifizierungs Konfigurationen params: aadTenantUri, aadAudienceId, aadIssuerUri für VpnClient.</span><span class="sxs-lookup"><span data-stu-id="3b52a-123">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="3b52a-124">Der dritte Befehl entfernt die Aad-Authentifizierungskonfiguration aus VpnClient des virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="3b52a-124">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

## <span data-ttu-id="3b52a-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b52a-125">PARAMETERS</span></span>

### <span data-ttu-id="3b52a-126">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="3b52a-126">-AadAudienceId</span></span>
<span data-ttu-id="3b52a-127">P2S Aad-Authentifizierungsoption: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="3b52a-127">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="3b52a-128">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="3b52a-128">-AadIssuerUri</span></span>
<span data-ttu-id="3b52a-129">P2S Aad-Authentifizierungsoption: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="3b52a-129">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="3b52a-130">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="3b52a-130">-AadTenantUri</span></span>
<span data-ttu-id="3b52a-131">P2S Aad-Authentifizierungsoption: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="3b52a-131">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="3b52a-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b52a-132">-AsJob</span></span>
<span data-ttu-id="3b52a-133">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3b52a-133">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3b52a-134">-ASN</span><span class="sxs-lookup"><span data-stu-id="3b52a-134">-Asn</span></span>
<span data-ttu-id="3b52a-135">Gibt den virtuellen Netzwerkgateway (autonome System Nummer) an, der zum Einrichten von BGP-Sitzungen (Border Gateway Protocol) innerhalb von IPSec-Tunneln verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3b52a-135">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="3b52a-136">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="3b52a-136">-CustomRoute</span></span>
<span data-ttu-id="3b52a-137">Vom Kunden angegebene benutzerdefinierte Routen AddressPool</span><span class="sxs-lookup"><span data-stu-id="3b52a-137">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="3b52a-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b52a-138">-DefaultProfile</span></span>
<span data-ttu-id="3b52a-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3b52a-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b52a-140">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="3b52a-140">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="3b52a-141">Deaktiviert das Active-Active-Feature.</span><span class="sxs-lookup"><span data-stu-id="3b52a-141">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="3b52a-142">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="3b52a-142">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="3b52a-143">Aktiviert das Active-Active-Feature.</span><span class="sxs-lookup"><span data-stu-id="3b52a-143">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="3b52a-144">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="3b52a-144">-GatewayDefaultSite</span></span>
<span data-ttu-id="3b52a-145">Gibt die Standardwebsite an, die für das Erzwingen des Tunnelns verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3b52a-145">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="3b52a-146">Wenn eine Standardwebsite angegeben wird, wird der gesamte Internetdatenverkehr vom VPN (virtuelles privates Netzwerk) des Gateways an diese Website weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="3b52a-146">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="3b52a-147">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="3b52a-147">-GatewaySku</span></span>
<span data-ttu-id="3b52a-148">Gibt die Lagerhaltungs Einheit (SKU) des virtuellen Netzwerkgateways an.</span><span class="sxs-lookup"><span data-stu-id="3b52a-148">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="3b52a-149">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3b52a-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3b52a-150">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="3b52a-150">Basic</span></span>
- <span data-ttu-id="3b52a-151">Standard</span><span class="sxs-lookup"><span data-stu-id="3b52a-151">Standard</span></span>
- <span data-ttu-id="3b52a-152">Hochleistungs</span><span class="sxs-lookup"><span data-stu-id="3b52a-152">HighPerformance</span></span>
- <span data-ttu-id="3b52a-153">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="3b52a-153">VpnGw1</span></span>
- <span data-ttu-id="3b52a-154">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="3b52a-154">VpnGw2</span></span>
- <span data-ttu-id="3b52a-155">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="3b52a-155">VpnGw3</span></span>
- <span data-ttu-id="3b52a-156">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="3b52a-156">VpnGw1AZ</span></span>
- <span data-ttu-id="3b52a-157">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="3b52a-157">VpnGw2AZ</span></span>
- <span data-ttu-id="3b52a-158">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="3b52a-158">VpnGw3AZ</span></span>
- <span data-ttu-id="3b52a-159">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="3b52a-159">ErGw1AZ</span></span>
- <span data-ttu-id="3b52a-160">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="3b52a-160">ErGw2AZ</span></span>
- <span data-ttu-id="3b52a-161">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="3b52a-161">ErGw3AZ</span></span>

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

### <span data-ttu-id="3b52a-162">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="3b52a-162">-PeerWeight</span></span>
<span data-ttu-id="3b52a-163">Gibt die Gewichtung von Routen an, die über BGP von diesem virtuellen Netzwerkgateway gelernt wurden.</span><span class="sxs-lookup"><span data-stu-id="3b52a-163">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="3b52a-164">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="3b52a-164">-RadiusServerAddress</span></span>
<span data-ttu-id="3b52a-165">P2S-externe RADIUS-Serveradresse.</span><span class="sxs-lookup"><span data-stu-id="3b52a-165">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="3b52a-166">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="3b52a-166">-RadiusServerSecret</span></span>
<span data-ttu-id="3b52a-167">P2S externer RADIUS-Server-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="3b52a-167">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="3b52a-168">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="3b52a-168">-RemoveAadAuthentication</span></span>
<span data-ttu-id="3b52a-169">Flag, um die Aad-Authentifizierung für den P2S-Client vom virtuellen Netzwerkgateway zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="3b52a-169">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="3b52a-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="3b52a-170">-Tag</span></span>
<span data-ttu-id="3b52a-171">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="3b52a-171">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="3b52a-172">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3b52a-172">-VirtualNetworkGateway</span></span>
<span data-ttu-id="3b52a-173">Gibt das virtuelles Netzwerkgateway-Objekt an, auf dem Änderungen basieren sollen.</span><span class="sxs-lookup"><span data-stu-id="3b52a-173">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="3b52a-174">Sie können das Get-AzVirtualNetworkGateway-Cmdlet verwenden, um das Virtual Network Gateway-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3b52a-174">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="3b52a-175">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="3b52a-175">-VpnClientAddressPool</span></span>
<span data-ttu-id="3b52a-176">Gibt den Adressraum an, von dem dieses Cmdlet für die Zuweisung von VPN-Client-IP-Adressen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3b52a-176">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="3b52a-177">Dies sollte sich nicht mit virtuellen Netzwerken oder lokalen Bereichen überlappen.</span><span class="sxs-lookup"><span data-stu-id="3b52a-177">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="3b52a-178">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="3b52a-178">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="3b52a-179">Eine Liste der IPSec-Richtlinien für P2S-VPN-Client Tunneling-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="3b52a-179">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="3b52a-180">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="3b52a-180">-VpnClientProtocol</span></span>
<span data-ttu-id="3b52a-181">Eine Liste der P2S-VPN-Client Tunneling-Protokolle</span><span class="sxs-lookup"><span data-stu-id="3b52a-181">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="3b52a-182">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="3b52a-182">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="3b52a-183">Gibt eine Liste der gesperrten VPN-Clientzertifikate an.</span><span class="sxs-lookup"><span data-stu-id="3b52a-183">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="3b52a-184">Ein VPN-Client mit einem Zertifikat, das einem dieser Zertifikate entspricht, wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="3b52a-184">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="3b52a-185">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="3b52a-185">-VpnClientRootCertificates</span></span>
<span data-ttu-id="3b52a-186">Gibt eine Liste der VPN-Client Stammzertifikate an, die für die VPN-Clientauthentifizierung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3b52a-186">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="3b52a-187">Beim Verbinden von VPN-Clients müssen Zertifikate vorhanden sein, die aus einem dieser Stammzertifikate generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="3b52a-187">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="3b52a-188">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3b52a-188">-Confirm</span></span>
<span data-ttu-id="3b52a-189">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b52a-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b52a-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b52a-190">-WhatIf</span></span>
<span data-ttu-id="3b52a-191">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b52a-191">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b52a-192">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b52a-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b52a-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b52a-193">CommonParameters</span></span>
<span data-ttu-id="3b52a-194">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b52a-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b52a-195">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b52a-195">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b52a-196">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3b52a-196">INPUTS</span></span>

### <span data-ttu-id="3b52a-197">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3b52a-197">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="3b52a-198">System. String</span><span class="sxs-lookup"><span data-stu-id="3b52a-198">System.String</span></span>

### <span data-ttu-id="3b52a-199">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3b52a-199">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="3b52a-200">System. String []</span><span class="sxs-lookup"><span data-stu-id="3b52a-200">System.String[]</span></span>

### <span data-ttu-id="3b52a-201">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="3b52a-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="3b52a-202">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="3b52a-202">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="3b52a-203">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="3b52a-203">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="3b52a-204">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="3b52a-204">System.UInt32</span></span>

### <span data-ttu-id="3b52a-205">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3b52a-205">System.Int32</span></span>

### <span data-ttu-id="3b52a-206">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="3b52a-206">System.Security.SecureString</span></span>

## <span data-ttu-id="3b52a-207">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3b52a-207">OUTPUTS</span></span>

### <span data-ttu-id="3b52a-208">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3b52a-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="3b52a-209">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b52a-209">NOTES</span></span>
* <span data-ttu-id="3b52a-210">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="3b52a-210">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3b52a-211">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3b52a-211">RELATED LINKS</span></span>

[<span data-ttu-id="3b52a-212">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3b52a-212">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="3b52a-213">Neu – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3b52a-213">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="3b52a-214">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3b52a-214">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="3b52a-215">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3b52a-215">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="3b52a-216">Größe ändern – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3b52a-216">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)
