---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azroutingconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
ms.openlocfilehash: b67b37f66e9b13c692b10dbdca54230bc1b0a529
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919555"
---
# <span data-ttu-id="0e7cb-101">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e7cb-101">New-AzRoutingConfiguration</span></span>

## <span data-ttu-id="0e7cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e7cb-102">SYNOPSIS</span></span>
<span data-ttu-id="0e7cb-103">Erstellt ein RoutingConfiguration-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0e7cb-103">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="0e7cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e7cb-104">SYNTAX</span></span>

```powershell
New-AzRoutingConfiguration -AssociatedRouteTable <String> -Label <String[]> -Id <String[]> [-StaticRoute <PSStaticRoute[]>]  [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e7cb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e7cb-105">DESCRIPTION</span></span>
<span data-ttu-id="0e7cb-106">Erstellt ein RoutingConfiguration-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0e7cb-106">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="0e7cb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0e7cb-107">EXAMPLES</span></span>

### <span data-ttu-id="0e7cb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0e7cb-108">Example 1</span></span>
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

<span data-ttu-id="0e7cb-109">Mit dem obigen Befehl wird ein RoutingConfiguration-Objekt erstellt, das dann einer Verbindungsressource hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0e7cb-109">The above command will create a RoutingConfiguration object which can then be added to a connection resource.</span></span> <span data-ttu-id="0e7cb-110">Statische Routen sind nur mit einem HubVirtualNetworkConnection-Objekt zulässig.</span><span class="sxs-lookup"><span data-stu-id="0e7cb-110">Static routes are only allowed with a HubVirtualNetworkConnection object.</span></span> 

## <span data-ttu-id="0e7cb-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0e7cb-111">PARAMETERS</span></span>

### <span data-ttu-id="0e7cb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e7cb-112">-DefaultProfile</span></span>
<span data-ttu-id="0e7cb-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0e7cb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e7cb-114">-AssociatedRouteTable</span><span class="sxs-lookup"><span data-stu-id="0e7cb-114">-AssociatedRouteTable</span></span>
<span data-ttu-id="0e7cb-115">Die Hubroutentabelle, die dieser Routingkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0e7cb-115">The hub route table associated with this routing configuration.</span></span>

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

### <span data-ttu-id="0e7cb-116">-ID</span><span class="sxs-lookup"><span data-stu-id="0e7cb-116">-Id</span></span>
<span data-ttu-id="0e7cb-117">Die Liste der Ressourcen-IDs aller Hubroutentabellen, an die die Routen für die PropagatedRouteTables-Eigenschaft angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="0e7cb-117">The list of resource ids of all the hub route tables to advertise the routes to for the PropagatedRouteTables property.</span></span>

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

### <span data-ttu-id="0e7cb-118">-Label</span><span class="sxs-lookup"><span data-stu-id="0e7cb-118">-Label</span></span>
<span data-ttu-id="0e7cb-119">Die Liste der Bezeichnungen für die PropagatedRouteTables-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0e7cb-119">The list of labels for the PropagatedRouteTables property.</span></span>

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

### <span data-ttu-id="0e7cb-120">-StaticRoute</span><span class="sxs-lookup"><span data-stu-id="0e7cb-120">-StaticRoute</span></span>
<span data-ttu-id="0e7cb-121">Liste der Routen, die das Routing von VirtualHub in eine virtuelle Netzwerkverbindung steuern.</span><span class="sxs-lookup"><span data-stu-id="0e7cb-121">List of routes that control routing from VirtualHub into a virtual network connection.</span></span>

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

### <span data-ttu-id="0e7cb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e7cb-122">CommonParameters</span></span>
<span data-ttu-id="0e7cb-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e7cb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e7cb-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e7cb-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e7cb-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0e7cb-125">INPUTS</span></span>

### <span data-ttu-id="0e7cb-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0e7cb-126">System.String</span></span>

### <span data-ttu-id="0e7cb-127">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="0e7cb-127">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="0e7cb-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0e7cb-128">OUTPUTS</span></span>

### <span data-ttu-id="0e7cb-129">Microsoft.Azure.Commands.Network.Models.PSRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e7cb-129">Microsoft.Azure.Commands.Network.Models.PSRoutingConfiguration</span></span>

## <span data-ttu-id="0e7cb-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0e7cb-130">NOTES</span></span>

## <span data-ttu-id="0e7cb-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0e7cb-131">RELATED LINKS</span></span>

[<span data-ttu-id="0e7cb-132">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="0e7cb-132">New-AzStaticRoute</span></span>](./New-AzStaticRoute.md)

[<span data-ttu-id="0e7cb-133">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="0e7cb-133">New-AzExpressRouteConnection</span></span>](./New-AzExpressRouteConnection.md)

[<span data-ttu-id="0e7cb-134">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="0e7cb-134">Set-AzExpressRouteConnection</span></span>](./Set-AzExpressRouteConnection.md)

[<span data-ttu-id="0e7cb-135">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="0e7cb-135">New-AzVirtualHubVnetConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="0e7cb-136">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="0e7cb-136">Update-AzVirtualHubVnetConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="0e7cb-137">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0e7cb-137">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="0e7cb-138">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0e7cb-138">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)

[<span data-ttu-id="0e7cb-139">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="0e7cb-139">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="0e7cb-140">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="0e7cb-140">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)