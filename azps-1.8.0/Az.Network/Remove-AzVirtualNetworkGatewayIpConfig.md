---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 9c36025f6de4ef6e6168bf5578d09d577cc4f46b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660307"
---
# <span data-ttu-id="1f7d2-101">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="1f7d2-101">Remove-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="1f7d2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1f7d2-102">SYNOPSIS</span></span>
<span data-ttu-id="1f7d2-103">Entfernt eine IP-Konfiguration von einem virtuellen Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="1f7d2-103">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="1f7d2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f7d2-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f7d2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f7d2-105">DESCRIPTION</span></span>
<span data-ttu-id="1f7d2-106">Entfernt eine IP-Konfiguration von einem virtuellen Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="1f7d2-106">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="1f7d2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f7d2-107">EXAMPLES</span></span>

### <span data-ttu-id="1f7d2-108">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="1f7d2-108">Example 1:</span></span>
```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gateway -Name ActiveActive

Name                   : myGateway
ResourceGroupName      : myRG
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft
                         .Network/virtualNetworkGateways/VNet8GW
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/800000000-0000-0000-0000-000000000000/resourceGroups/myRG/provid
                         ers/Microsoft.Network/virtualNetworks/VNet8/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/provid
                         ers/Microsoft.Network/publicIPAddresses/VNet8GWIP"
                             },
                             "Name": "gwipconfig1",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/provider
                         s/Microsoft.Network/virtualNetworkGateways/VNet8GW/ipConfigurations/gwipconfig1"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : True
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "192.0.2.4,192.0.2.5",
                           "PeerWeight": 0
                         }
```

## <span data-ttu-id="1f7d2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f7d2-109">PARAMETERS</span></span>

### <span data-ttu-id="1f7d2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f7d2-110">-DefaultProfile</span></span>
<span data-ttu-id="1f7d2-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1f7d2-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f7d2-112">-Name</span><span class="sxs-lookup"><span data-stu-id="1f7d2-112">-Name</span></span>
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

### <span data-ttu-id="1f7d2-113">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1f7d2-113">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="1f7d2-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1f7d2-114">-Confirm</span></span>
<span data-ttu-id="1f7d2-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1f7d2-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f7d2-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f7d2-116">-WhatIf</span></span>
<span data-ttu-id="1f7d2-117">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1f7d2-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f7d2-118">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1f7d2-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f7d2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f7d2-119">CommonParameters</span></span>
<span data-ttu-id="1f7d2-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f7d2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f7d2-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f7d2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f7d2-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1f7d2-122">INPUTS</span></span>

### <span data-ttu-id="1f7d2-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1f7d2-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="1f7d2-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1f7d2-124">OUTPUTS</span></span>

### <span data-ttu-id="1f7d2-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1f7d2-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="1f7d2-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f7d2-126">NOTES</span></span>

## <span data-ttu-id="1f7d2-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1f7d2-127">RELATED LINKS</span></span>

[<span data-ttu-id="1f7d2-128">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="1f7d2-128">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="1f7d2-129">Neu – AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="1f7d2-129">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)
