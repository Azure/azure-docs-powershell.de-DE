---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 22877a91c3b6939d35e2eae8d359dc9056425447
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503566"
---
# <span data-ttu-id="309fc-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="309fc-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="309fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="309fc-102">SYNOPSIS</span></span>
<span data-ttu-id="309fc-103">Fügt eine IP-Konfiguration zu einem virtuellen Netzwerkgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="309fc-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="309fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="309fc-104">SYNTAX</span></span>

### <span data-ttu-id="309fc-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="309fc-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="309fc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="309fc-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="309fc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="309fc-107">DESCRIPTION</span></span>
<span data-ttu-id="309fc-108">Das Cmdlet **Add-AzureRmVirtualNetworkGatewayIpConfig** fügt eine IP-Konfiguration zu einem virtuellen Netzwerkgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="309fc-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="309fc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="309fc-109">EXAMPLES</span></span>

### <span data-ttu-id="309fc-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="309fc-110">Example 1</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gw -Name GWIPConfig2 -Subnet $subnet -PublicIpAddress $gwpip2


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

## <span data-ttu-id="309fc-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="309fc-111">PARAMETERS</span></span>

### <span data-ttu-id="309fc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="309fc-112">-DefaultProfile</span></span>
<span data-ttu-id="309fc-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="309fc-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="309fc-114">-Name</span><span class="sxs-lookup"><span data-stu-id="309fc-114">-Name</span></span>
<span data-ttu-id="309fc-115">Gibt den Namen der IP-Gateway-Konfiguration an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="309fc-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="309fc-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="309fc-116">-PrivateIpAddress</span></span>
<span data-ttu-id="309fc-117">Gibt die private IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="309fc-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="309fc-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="309fc-118">-PublicIpAddress</span></span>
<span data-ttu-id="309fc-119">Gibt die öffentliche IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="309fc-119">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="309fc-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="309fc-120">-PublicIpAddressId</span></span>
<span data-ttu-id="309fc-121">Gibt die ID der öffentlichen IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="309fc-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="309fc-122">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="309fc-122">-Subnet</span></span>
<span data-ttu-id="309fc-123">Gibt ein **PSSubnet** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="309fc-123">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="309fc-124">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="309fc-124">-SubnetId</span></span>
<span data-ttu-id="309fc-125">Gibt die ID des Subnets an.</span><span class="sxs-lookup"><span data-stu-id="309fc-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="309fc-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="309fc-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="309fc-127">Gibt ein **PSVirtualNetworkGateway** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="309fc-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="309fc-128">Dieses Cmdlet ändert das von Ihnen angegebene **PSVirtualNetworkGateway** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="309fc-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="309fc-129">Sie können das Get-AzureRmVirtualNetworkGateway-Cmdlet verwenden, um ein **PSVirtualNetworkGateway** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="309fc-129">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="309fc-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="309fc-130">-Confirm</span></span>
<span data-ttu-id="309fc-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="309fc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="309fc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="309fc-132">-WhatIf</span></span>
<span data-ttu-id="309fc-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="309fc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="309fc-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="309fc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="309fc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="309fc-135">CommonParameters</span></span>
<span data-ttu-id="309fc-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="309fc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="309fc-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="309fc-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="309fc-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="309fc-138">INPUTS</span></span>

### <span data-ttu-id="309fc-139">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="309fc-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="309fc-140">Parameter: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="309fc-140">Parameters: VirtualNetworkGateway (ByValue)</span></span>

## <span data-ttu-id="309fc-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="309fc-141">OUTPUTS</span></span>

### <span data-ttu-id="309fc-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="309fc-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="309fc-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="309fc-143">NOTES</span></span>

## <span data-ttu-id="309fc-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="309fc-144">RELATED LINKS</span></span>

[<span data-ttu-id="309fc-145">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="309fc-145">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="309fc-146">Neu – AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="309fc-146">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="309fc-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="309fc-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


