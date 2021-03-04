---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/disconnect-azp2svpngatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2SVpnGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2SVpnGatewayVpnConnection.md
ms.openlocfilehash: 493927a21b4154065777109341b437d75f934ee3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931816"
---
# <span data-ttu-id="c343f-101">Disconnect-AzP2sVpnGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="c343f-101">Disconnect-AzP2sVpnGatewayVpnConnection</span></span>

## <span data-ttu-id="c343f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c343f-102">SYNOPSIS</span></span>
<span data-ttu-id="c343f-103">Trennen von verbundenen Vpn-Clientverbindungen mit einem bestimmten p2s-VPN-Gateway</span><span class="sxs-lookup"><span data-stu-id="c343f-103">Disconnect given connected vpn client connections with a given p2s vpn gateway</span></span>

## <span data-ttu-id="c343f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c343f-104">SYNTAX</span></span>

### <span data-ttu-id="c343f-105">ByP2SVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c343f-105">ByP2SVpnGatewayName (Default)</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -Name <String> -ResourceGroupName <String>
 -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="c343f-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="c343f-106">ByP2SVpnGatewayObject</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="c343f-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="c343f-107">ByP2SVpnGatewayResourceId</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="c343f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c343f-108">DESCRIPTION</span></span>
<span data-ttu-id="c343f-109">Mit **dem Cmdlet Disconnect-AzP2sVpnGatewayVpnConnection** können Sie die Verbindung zu einer aktuellen Punkt-zu-Website-Verbindung von P2SVpnGateway trennen.</span><span class="sxs-lookup"><span data-stu-id="c343f-109">The **Disconnect-AzP2sVpnGatewayVpnConnection** cmdlet enables you to disconnect given current point to site connection from P2SVpnGateway.</span></span>

## <span data-ttu-id="c343f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c343f-110">EXAMPLES</span></span>

### <span data-ttu-id="c343f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c343f-111">Example 1</span></span>
```powershell
PS C:\> Disconnect-AzP2sVpnGatewayVpnConnection -ResourceName 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

## <span data-ttu-id="c343f-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c343f-112">PARAMETERS</span></span>

### <span data-ttu-id="c343f-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c343f-113">-InputObject</span></span>
<span data-ttu-id="c343f-114">Das zu ändernde p2s-Vpn-Gatewayobjekt</span><span class="sxs-lookup"><span data-stu-id="c343f-114">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c343f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c343f-115">-Name</span></span>
<span data-ttu-id="c343f-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="c343f-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c343f-117">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="c343f-117">-VpnConnectionId</span></span>
<span data-ttu-id="c343f-118">Vpn Connection Ida</span><span class="sxs-lookup"><span data-stu-id="c343f-118">Vpn Connection Ida</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c343f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c343f-119">-ResourceGroupName</span></span>
<span data-ttu-id="c343f-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c343f-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c343f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c343f-121">-ResourceId</span></span>
<span data-ttu-id="c343f-122">P2s Virtual network gateway resource Id</span><span class="sxs-lookup"><span data-stu-id="c343f-122">P2s Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c343f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c343f-123">CommonParameters</span></span>
<span data-ttu-id="c343f-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c343f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c343f-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c343f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c343f-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c343f-126">INPUTS</span></span>

### <span data-ttu-id="c343f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="c343f-127">System.String</span></span>

## <span data-ttu-id="c343f-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c343f-128">OUTPUTS</span></span>

### <span data-ttu-id="c343f-129">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c343f-129">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="c343f-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c343f-130">NOTES</span></span>

## <span data-ttu-id="c343f-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c343f-131">RELATED LINKS</span></span>
