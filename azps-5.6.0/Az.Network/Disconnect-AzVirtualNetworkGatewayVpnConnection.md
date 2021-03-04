---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: 1cbbfcbc87ed1d9be869066f8ec6dd288ba3d4d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944975"
---
# <span data-ttu-id="14469-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="14469-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="14469-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14469-102">SYNOPSIS</span></span> 
<span data-ttu-id="14469-103">Trennen Sie die Verbindung zu verbundenen Vpn-Clientverbindungen mit einem bestimmten Gateway für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="14469-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="14469-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14469-104">SYNTAX</span></span>
### <span data-ttu-id="14469-105">ByVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="14469-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="14469-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="14469-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="14469-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="14469-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="14469-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14469-108">DESCRIPTION</span></span>
<span data-ttu-id="14469-109">Das **Cmdlet Disconnect-AzVirtualNetworkGatewayVpnConnection** ermöglicht ihnen das Trennen einer verbundenen VPN-Clientverbindung.</span><span class="sxs-lookup"><span data-stu-id="14469-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="14469-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="14469-110">EXAMPLES</span></span>

### <span data-ttu-id="14469-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="14469-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="14469-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="14469-112">PARAMETERS</span></span>

### <span data-ttu-id="14469-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14469-113">-ResourceGroupName</span></span>
<span data-ttu-id="14469-114">Name der Ressourcengruppe "Virtuelles Netzwerkgateway"</span><span class="sxs-lookup"><span data-stu-id="14469-114">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14469-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="14469-115">-ResourceName</span></span>
<span data-ttu-id="14469-116">Name des Virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="14469-116">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: VirtualNetworkGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14469-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14469-117">-ResourceId</span></span>
<span data-ttu-id="14469-118">Ressourcen-ID des Virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="14469-118">Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14469-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="14469-119">-VpnConnectionId</span></span>
<span data-ttu-id="14469-120">Vpn-Verbindungs-ID</span><span class="sxs-lookup"><span data-stu-id="14469-120">Vpn Connection Ids</span></span>

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

### <span data-ttu-id="14469-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14469-121">-InputObject</span></span>
<span data-ttu-id="14469-122">Virtuelles Netzwerkgatewayobjekt</span><span class="sxs-lookup"><span data-stu-id="14469-122">Virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VirtualNetworkGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14469-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14469-123">-AsJob</span></span>
<span data-ttu-id="14469-124">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="14469-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14469-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14469-125">CommonParameters</span></span>
<span data-ttu-id="14469-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14469-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14469-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14469-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14469-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="14469-128">INPUTS</span></span>

### <span data-ttu-id="14469-129">System.String</span><span class="sxs-lookup"><span data-stu-id="14469-129">System.String</span></span>

## <span data-ttu-id="14469-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="14469-130">OUTPUTS</span></span>

### <span data-ttu-id="14469-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="14469-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="14469-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="14469-132">NOTES</span></span>

## <span data-ttu-id="14469-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="14469-133">RELATED LINKS</span></span>
