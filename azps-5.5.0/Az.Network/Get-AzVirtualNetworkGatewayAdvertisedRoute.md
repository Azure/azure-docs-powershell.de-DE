---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: d41e71afc27129d2b2de40df97f12b0bb8f07ae5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147060"
---
# <span data-ttu-id="85431-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="85431-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="85431-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85431-102">SYNOPSIS</span></span>
<span data-ttu-id="85431-103">Listet Routen auf, die von einem virtuellen Azure-Netzwerkgateway angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="85431-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

## <span data-ttu-id="85431-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85431-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85431-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85431-105">DESCRIPTION</span></span>
<span data-ttu-id="85431-106">Angesichts der IP eines BGP-Peers werden die Routen aufgezählt, die vom angegebenen virtuellen Azure-Netzwerkgateway an den Peer angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="85431-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="85431-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="85431-107">EXAMPLES</span></span>

### <span data-ttu-id="85431-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="85431-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="85431-109">Ruft für das Azure-Gateway mit dem Namen "gatewayName" in der Ressourcengruppe "ResourceGroupName" eine Liste der Routen ab, die für den BGP-Peer mit IP 10.0.0.254 angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="85431-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="85431-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="85431-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="85431-111">Ruft für das Azure-Gateway mit dem Namen "gatewayName" in der Ressourcengruppe "ResourceGroupName" routen ab, die an den ersten BGP-Peer in der Liste der BGP-Peers des Gateways angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="85431-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="85431-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85431-112">PARAMETERS</span></span>

### <span data-ttu-id="85431-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85431-113">-AsJob</span></span>
<span data-ttu-id="85431-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="85431-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85431-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85431-115">-DefaultProfile</span></span>
<span data-ttu-id="85431-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85431-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85431-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="85431-117">-Peer</span></span>
<span data-ttu-id="85431-118">Die IP-Adresse des BGP-Peers.</span><span class="sxs-lookup"><span data-stu-id="85431-118">BGP peer's IP address.</span></span> <span data-ttu-id="85431-119">Dabei sollte es sich um eine IP innerhalb des Adressbereichs handelt, auf den innerhalb des virtuellen Azure-Netzwerks zugegriffen werden kann, in dem das Gateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="85431-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="85431-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85431-120">-ResourceGroupName</span></span>
<span data-ttu-id="85431-121">Name der Ressourcengruppe des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="85431-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="85431-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="85431-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="85431-123">Name des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="85431-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="85431-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85431-124">CommonParameters</span></span>
<span data-ttu-id="85431-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85431-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85431-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85431-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85431-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="85431-127">INPUTS</span></span>

### <span data-ttu-id="85431-128">System.String</span><span class="sxs-lookup"><span data-stu-id="85431-128">System.String</span></span>

## <span data-ttu-id="85431-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="85431-129">OUTPUTS</span></span>

### <span data-ttu-id="85431-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="85431-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="85431-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="85431-131">NOTES</span></span>
<span data-ttu-id="85431-132">Dieser Befehl gilt nur für virtuelle Azure-Netzwerkgateways mit BGP-fähigen Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="85431-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="85431-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="85431-133">RELATED LINKS</span></span>
