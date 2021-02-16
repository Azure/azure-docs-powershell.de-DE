---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: b14d7f0ac4f70268175948b41abaa1fee564a383
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157161"
---
# <span data-ttu-id="fe6f1-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fe6f1-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="fe6f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe6f1-102">SYNOPSIS</span></span> 
<span data-ttu-id="fe6f1-103">Trennen Sie die Verbindung von verbundenen VPN-Clientverbindungen mit einem bestimmten virtuellen Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="fe6f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe6f1-104">SYNTAX</span></span>
### <span data-ttu-id="fe6f1-105">ByVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fe6f1-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="fe6f1-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="fe6f1-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="fe6f1-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="fe6f1-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="fe6f1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe6f1-108">DESCRIPTION</span></span>
<span data-ttu-id="fe6f1-109">Mit **dem Cmdlet "Disconnect-AzVirtualNetworkGatewayVpnConnection"** können Sie die Verbindung zu einer verbundenen VPN-Clientverbindung trennen.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="fe6f1-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fe6f1-110">EXAMPLES</span></span>

### <span data-ttu-id="fe6f1-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fe6f1-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="fe6f1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe6f1-112">PARAMETERS</span></span>

### <span data-ttu-id="fe6f1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe6f1-113">-ResourceGroupName</span></span>
<span data-ttu-id="fe6f1-114">Name der Ressourcengruppe des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="fe6f1-114">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="fe6f1-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="fe6f1-115">-ResourceName</span></span>
<span data-ttu-id="fe6f1-116">Name des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="fe6f1-116">Virtual network gateway name</span></span>

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

### <span data-ttu-id="fe6f1-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe6f1-117">-ResourceId</span></span>
<span data-ttu-id="fe6f1-118">Ressourcen-ID des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="fe6f1-118">Virtual network gateway resource Id</span></span>

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

### <span data-ttu-id="fe6f1-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="fe6f1-119">-VpnConnectionId</span></span>
<span data-ttu-id="fe6f1-120">VPN-Verbindungs-IDs</span><span class="sxs-lookup"><span data-stu-id="fe6f1-120">Vpn Connection Ids</span></span>

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

### <span data-ttu-id="fe6f1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe6f1-121">-InputObject</span></span>
<span data-ttu-id="fe6f1-122">Objekt des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="fe6f1-122">Virtual network gateway object</span></span>

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

### <span data-ttu-id="fe6f1-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe6f1-123">-AsJob</span></span>
<span data-ttu-id="fe6f1-124">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fe6f1-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe6f1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe6f1-125">CommonParameters</span></span>
<span data-ttu-id="fe6f1-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe6f1-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe6f1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe6f1-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fe6f1-128">INPUTS</span></span>

### <span data-ttu-id="fe6f1-129">System.String</span><span class="sxs-lookup"><span data-stu-id="fe6f1-129">System.String</span></span>

## <span data-ttu-id="fe6f1-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fe6f1-130">OUTPUTS</span></span>

### <span data-ttu-id="fe6f1-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fe6f1-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="fe6f1-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fe6f1-132">NOTES</span></span>

## <span data-ttu-id="fe6f1-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fe6f1-133">RELATED LINKS</span></span>
