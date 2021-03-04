---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: 13a81733ac748d2593df967268021f10d60de50b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924760"
---
# <span data-ttu-id="83c3b-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="83c3b-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="83c3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="83c3b-103">Liste der von einem virtuellen Azure-Netzwerkgateway angekündigten Routen</span><span class="sxs-lookup"><span data-stu-id="83c3b-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

## <span data-ttu-id="83c3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83c3b-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83c3b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="83c3b-105">DESCRIPTION</span></span>
<span data-ttu-id="83c3b-106">Angesichts der IP eines BGP-Peers werden routen aufgezählt, die für den Peer vom angegebenen virtuellen Azure-Netzwerkgateway angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="83c3b-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="83c3b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="83c3b-107">EXAMPLES</span></span>

### <span data-ttu-id="83c3b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="83c3b-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="83c3b-109">Ruft für das Azure-Gateway mit dem Namen gatewayName in resource group resourceGroupName eine Liste der Routen ab, die für den BGP-Peer mit IP 10.0.0.254 angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="83c3b-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="83c3b-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="83c3b-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="83c3b-111">Ruft für das Azure-Gateway mit dem Namen gatewayName in resource group resourceGroupName Routen ab, die für den ersten BGP-Peer in der Liste der BGP-Peers des Gateways angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="83c3b-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="83c3b-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="83c3b-112">PARAMETERS</span></span>

### <span data-ttu-id="83c3b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83c3b-113">-AsJob</span></span>
<span data-ttu-id="83c3b-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="83c3b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="83c3b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83c3b-115">-DefaultProfile</span></span>
<span data-ttu-id="83c3b-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83c3b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83c3b-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="83c3b-117">-Peer</span></span>
<span data-ttu-id="83c3b-118">die IP-Adresse des BGP-Peers.</span><span class="sxs-lookup"><span data-stu-id="83c3b-118">BGP peer's IP address.</span></span> <span data-ttu-id="83c3b-119">Dies sollte eine IP innerhalb des Adressbereichs sein, auf den innerhalb des virtuellen Azure-Netzwerks zugegriffen werden kann, in dem das Gateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="83c3b-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="83c3b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83c3b-120">-ResourceGroupName</span></span>
<span data-ttu-id="83c3b-121">Name der Ressourcengruppe "Virtuelles Netzwerkgateway"</span><span class="sxs-lookup"><span data-stu-id="83c3b-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="83c3b-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="83c3b-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="83c3b-123">Name des Virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="83c3b-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="83c3b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83c3b-124">CommonParameters</span></span>
<span data-ttu-id="83c3b-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83c3b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83c3b-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83c3b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83c3b-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="83c3b-127">INPUTS</span></span>

### <span data-ttu-id="83c3b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="83c3b-128">System.String</span></span>

## <span data-ttu-id="83c3b-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="83c3b-129">OUTPUTS</span></span>

### <span data-ttu-id="83c3b-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="83c3b-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="83c3b-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="83c3b-131">NOTES</span></span>
<span data-ttu-id="83c3b-132">Dieser Befehl gilt nur für Azure Virtual Network Gateways mit BGP-aktivierten Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="83c3b-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="83c3b-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="83c3b-133">RELATED LINKS</span></span>
