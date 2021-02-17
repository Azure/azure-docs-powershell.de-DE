---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutingconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
ms.openlocfilehash: 31601c93a6979d09dfb3641cac079cba2757d043
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172604"
---
# <span data-ttu-id="bb157-101">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb157-101">New-AzRoutingConfiguration</span></span>

## <span data-ttu-id="bb157-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb157-102">SYNOPSIS</span></span>
<span data-ttu-id="bb157-103">Erstellt ein RoutingConfiguration-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bb157-103">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="bb157-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb157-104">SYNTAX</span></span>

```powershell
New-AzRoutingConfiguration -AssociatedRouteTable <String> -Label <String[]> -Id <String[]> [-StaticRoute <PSStaticRoute[]>]  [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb157-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb157-105">DESCRIPTION</span></span>
<span data-ttu-id="bb157-106">Erstellt ein RoutingConfiguration-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bb157-106">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="bb157-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bb157-107">EXAMPLES</span></span>

### <span data-ttu-id="bb157-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bb157-108">Example 1</span></span>
```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> $rt1 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "defaultRouteTable"
PS C:\> $rt2 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "noneRouteTable"
PS C:\> $route1 = New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16")-NextHopIpAddress "10.90.0.5"
PS C:\> New-AzRoutingConfiguration -AssociatedRouteTable $rt1.Id -Label @("testLabel") -Id @($rt2.Id) -StaticRoute @($route1)

AssociatedRouteTable  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable"
PropagatedRouteTables : {
                          "Labels": [
                            "testLabel"
                          ],
                          "Ids": [
                            {
                              "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "route1",
                              "AddressPrefixes": [
                                "10.20.0.0/16",
                                "10.30.0.0/16"
                              ],
                              "NextHopIpAddress": "10.90.0.5"
                            }
                          ]
                        }
```

<span data-ttu-id="bb157-109">Mit dem oben angegebenen Befehl wird ein RoutingConfiguration-Objekt erstellt, das dann einer Verbindungsressource hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="bb157-109">The above command will create a RoutingConfiguration object which can then be added to a connection resource.</span></span> <span data-ttu-id="bb157-110">Statische Routen sind nur bei einem HubVirtualNetworkConnection-Objekt zulässig.</span><span class="sxs-lookup"><span data-stu-id="bb157-110">Static routes are only allowed with a HubVirtualNetworkConnection object.</span></span> 

## <span data-ttu-id="bb157-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb157-111">PARAMETERS</span></span>

### <span data-ttu-id="bb157-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb157-112">-DefaultProfile</span></span>
<span data-ttu-id="bb157-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb157-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb157-114">-AssociatedRouteTable</span><span class="sxs-lookup"><span data-stu-id="bb157-114">-AssociatedRouteTable</span></span>
<span data-ttu-id="bb157-115">Die Hubroutentabelle, die dieser Routingkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bb157-115">The hub route table associated with this routing configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb157-116">-ID</span><span class="sxs-lookup"><span data-stu-id="bb157-116">-Id</span></span>
<span data-ttu-id="bb157-117">Die Liste der Ressourcen-IDs aller Hubroutentabellen, an die die Routen für die Eigenschaft "PropagatedRouteTables" angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="bb157-117">The list of resource ids of all the hub route tables to advertise the routes to for the PropagatedRouteTables property.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb157-118">-Label</span><span class="sxs-lookup"><span data-stu-id="bb157-118">-Label</span></span>
<span data-ttu-id="bb157-119">Die Liste der Bezeichnungen für die Eigenschaft "PropagatedRouteTables".</span><span class="sxs-lookup"><span data-stu-id="bb157-119">The list of labels for the PropagatedRouteTables property.</span></span>

```yaml
Type: String[]
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb157-120">-StaticRoute</span><span class="sxs-lookup"><span data-stu-id="bb157-120">-StaticRoute</span></span>
<span data-ttu-id="bb157-121">Liste der Routen, die das Routing von VirtualHub zu einer virtuellen Netzwerkverbindung steuern.</span><span class="sxs-lookup"><span data-stu-id="bb157-121">List of routes that control routing from VirtualHub into a virtual network connection.</span></span>

```yaml
Type: PSStaticRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb157-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb157-122">CommonParameters</span></span>
<span data-ttu-id="bb157-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb157-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb157-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb157-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb157-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bb157-125">INPUTS</span></span>

### <span data-ttu-id="bb157-126">System.String</span><span class="sxs-lookup"><span data-stu-id="bb157-126">System.String</span></span>

### <span data-ttu-id="bb157-127">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="bb157-127">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="bb157-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bb157-128">OUTPUTS</span></span>

### <span data-ttu-id="bb157-129">Microsoft.Azure.Commands.Network.Models.PSRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb157-129">Microsoft.Azure.Commands.Network.Models.PSRoutingConfiguration</span></span>

## <span data-ttu-id="bb157-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bb157-130">NOTES</span></span>

## <span data-ttu-id="bb157-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bb157-131">RELATED LINKS</span></span>

[<span data-ttu-id="bb157-132">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="bb157-132">New-AzStaticRoute</span></span>](./New-AzStaticRoute.md)

[<span data-ttu-id="bb157-133">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="bb157-133">New-AzExpressRouteConnection</span></span>](./New-AzExpressRouteConnection.md)

[<span data-ttu-id="bb157-134">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="bb157-134">Set-AzExpressRouteConnection</span></span>](./Set-AzExpressRouteConnection.md)

[<span data-ttu-id="bb157-135">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="bb157-135">New-AzVirtualHubVnetConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="bb157-136">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="bb157-136">Update-AzVirtualHubVnetConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="bb157-137">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="bb157-137">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="bb157-138">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="bb157-138">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)

[<span data-ttu-id="bb157-139">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="bb157-139">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="bb157-140">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="bb157-140">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)