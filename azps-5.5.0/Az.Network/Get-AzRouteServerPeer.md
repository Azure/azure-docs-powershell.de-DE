---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
ms.openlocfilehash: d36a919adfbf1a7a2e2b7a10313433e820cc478a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151900"
---
# <span data-ttu-id="97703-101">Get-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="97703-101">Get-AzRouteServerPeer</span></span>

## <span data-ttu-id="97703-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97703-102">SYNOPSIS</span></span>
<span data-ttu-id="97703-103">Ruft einen RouteServer-Peer in einem Azure RouteServer ab.</span><span class="sxs-lookup"><span data-stu-id="97703-103">Gets a RouteServer peer in an Azure RouteServer</span></span>

## <span data-ttu-id="97703-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97703-104">SYNTAX</span></span>

### <span data-ttu-id="97703-105">RouteServerNPeerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="97703-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Get-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97703-106">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="97703-106">RouteServerNPeerResourceIdParameterSet</span></span>
```
Get-AzRouteServerPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97703-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97703-107">DESCRIPTION</span></span>
<span data-ttu-id="97703-108">Das **Cmdlet "Get-AzRouteServerPeer"** ruft einen Peer in einem Azure RouteServer ab.</span><span class="sxs-lookup"><span data-stu-id="97703-108">The **Get-AzRouteServerPeer** cmdlet gets a Peer in an Azure RouteServer</span></span>

## <span data-ttu-id="97703-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="97703-109">EXAMPLES</span></span>

### <span data-ttu-id="97703-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="97703-110">Example 1</span></span>
```powershell
Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
```

### <span data-ttu-id="97703-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="97703-111">Example 2</span></span>
```powershell
$routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Get-AzRouteServerPeer -ResourceId $routeServerPeerId
```

## <span data-ttu-id="97703-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97703-112">PARAMETERS</span></span>

### <span data-ttu-id="97703-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97703-113">-DefaultProfile</span></span>
<span data-ttu-id="97703-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97703-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97703-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="97703-115">-PeerName</span></span>
<span data-ttu-id="97703-116">Der Name des Routenserver-Peers.</span><span class="sxs-lookup"><span data-stu-id="97703-116">The name of the route server peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97703-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97703-117">-ResourceGroupName</span></span>
<span data-ttu-id="97703-118">Der Ressourcengruppenname des Routeservers.</span><span class="sxs-lookup"><span data-stu-id="97703-118">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97703-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97703-119">-ResourceId</span></span>
<span data-ttu-id="97703-120">ResourceId des Routenserver-Peers.</span><span class="sxs-lookup"><span data-stu-id="97703-120">ResourceId of the route server peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97703-121">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="97703-121">-RouteServerName</span></span>
<span data-ttu-id="97703-122">Der Name des Routeservers.</span><span class="sxs-lookup"><span data-stu-id="97703-122">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97703-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97703-123">CommonParameters</span></span>
<span data-ttu-id="97703-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97703-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97703-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97703-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97703-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="97703-126">INPUTS</span></span>

### <span data-ttu-id="97703-127">System.String</span><span class="sxs-lookup"><span data-stu-id="97703-127">System.String</span></span>

## <span data-ttu-id="97703-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="97703-128">OUTPUTS</span></span>

### <span data-ttu-id="97703-129">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="97703-129">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="97703-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="97703-130">NOTES</span></span>

## <span data-ttu-id="97703-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="97703-131">RELATED LINKS</span></span>
