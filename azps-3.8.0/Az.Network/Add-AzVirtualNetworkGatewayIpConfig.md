---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: f8de9ce0aab60aad729d990c233acfaf75ae50b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997240"
---
# <span data-ttu-id="a2d57-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="a2d57-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="a2d57-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2d57-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d57-103">Fügt eine IP-Konfiguration zu einem virtuellen Netzwerkgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="a2d57-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="a2d57-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2d57-104">SYNTAX</span></span>

### <span data-ttu-id="a2d57-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a2d57-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2d57-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a2d57-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2d57-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2d57-107">DESCRIPTION</span></span>
<span data-ttu-id="a2d57-108">Das Cmdlet **Add-AzVirtualNetworkGatewayIpConfig** fügt eine IP-Konfiguration zu einem virtuellen Netzwerkgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="a2d57-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="a2d57-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2d57-109">EXAMPLES</span></span>

### <span data-ttu-id="a2d57-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a2d57-110">Example 1</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gw -Name GWIPConfig2 -Subnet $subnet -PublicIpAddress $gwpip2


Name                   : VNet7GW
ResourceGroupName      : VPNGatewayV3
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworkGateways/VNet7GW
Etag                   : W/"d27a784f-3c3f-4150-863d-764649b6e8e7"
ResourceGuid           : 3c2478a7-d5d4-4e80-8532-7ea2ad577598
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworks/Vnet7/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/publicIPAddresses/VNet7GW_IP"
                             },
                             "Name": "default",
                             "Etag": "W/\"d27a784f-3c3f-4150-863d-764649b6e8e7\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworkGateways/VNet7GW/ipConfigurations/default"
                           },
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/publicIPAddresses/delIPConfig"
                             },
                             "Name": "GWIPConfig2",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupNotSet/providers/Microsoft.Network/virtualNetworkGateways/VirtualNetworkGatewayNameNotSet/virtualNetworkGatewayIpConfiguration/GWIPConfig2"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : True
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65534,
                           "BgpPeeringAddress": "10.7.255.254",
                           "PeerWeight": 0
                         }
```

## <span data-ttu-id="a2d57-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2d57-111">PARAMETERS</span></span>

### <span data-ttu-id="a2d57-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d57-112">-DefaultProfile</span></span>
<span data-ttu-id="a2d57-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a2d57-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2d57-114">-Name</span><span class="sxs-lookup"><span data-stu-id="a2d57-114">-Name</span></span>
<span data-ttu-id="a2d57-115">Gibt den Namen der IP-Gateway-Konfiguration an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2d57-115">Specifies the name of the gateway IP configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d57-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="a2d57-116">-PrivateIpAddress</span></span>
<span data-ttu-id="a2d57-117">Gibt die private IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="a2d57-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="a2d57-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a2d57-118">-PublicIpAddress</span></span>
<span data-ttu-id="a2d57-119">Gibt die öffentliche IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="a2d57-119">Specifies the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d57-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="a2d57-120">-PublicIpAddressId</span></span>
<span data-ttu-id="a2d57-121">Gibt die ID der öffentlichen IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="a2d57-121">Specifies the ID of the public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d57-122">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="a2d57-122">-Subnet</span></span>
<span data-ttu-id="a2d57-123">Gibt ein **PSSubnet** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a2d57-123">Specifies a **PSSubnet** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d57-124">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="a2d57-124">-SubnetId</span></span>
<span data-ttu-id="a2d57-125">Gibt die ID des Subnets an.</span><span class="sxs-lookup"><span data-stu-id="a2d57-125">Specifies the ID of the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d57-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a2d57-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="a2d57-127">Gibt ein **PSVirtualNetworkGateway** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a2d57-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="a2d57-128">Dieses Cmdlet ändert das von Ihnen angegebene **PSVirtualNetworkGateway** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a2d57-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="a2d57-129">Sie können das Get-AzVirtualNetworkGateway-Cmdlet verwenden, um ein **PSVirtualNetworkGateway** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a2d57-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="a2d57-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a2d57-130">-Confirm</span></span>
<span data-ttu-id="a2d57-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2d57-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2d57-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2d57-132">-WhatIf</span></span>
<span data-ttu-id="a2d57-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2d57-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2d57-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2d57-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2d57-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d57-135">CommonParameters</span></span>
<span data-ttu-id="a2d57-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2d57-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d57-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2d57-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d57-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2d57-138">INPUTS</span></span>

### <span data-ttu-id="a2d57-139">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a2d57-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="a2d57-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2d57-140">OUTPUTS</span></span>

### <span data-ttu-id="a2d57-141">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a2d57-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="a2d57-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2d57-142">NOTES</span></span>

## <span data-ttu-id="a2d57-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2d57-143">RELATED LINKS</span></span>

[<span data-ttu-id="a2d57-144">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a2d57-144">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a2d57-145">Neu – AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="a2d57-145">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="a2d57-146">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="a2d57-146">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
