---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 9cd5a4417f3fd8d6d40cfdf70e6c76f1910ce7c3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470183"
---
# <span data-ttu-id="99032-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="99032-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="99032-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99032-102">SYNOPSIS</span></span>
<span data-ttu-id="99032-103">Erstellt ein VHubRoute-Objekt, das als Parameter an den Befehl "New-AzVHubRouteTable übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="99032-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="99032-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99032-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99032-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99032-105">DESCRIPTION</span></span>

<span data-ttu-id="99032-106">Erstellt ein VHubRoute-Objekt.</span><span class="sxs-lookup"><span data-stu-id="99032-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="99032-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="99032-107">EXAMPLES</span></span>

### <span data-ttu-id="99032-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="99032-108">Example 1</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $firewallName = "testFirewall"
PS C:\> $firewall = Get-AzFirewall -Name $firewallName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall
```

<span data-ttu-id="99032-109">Mit dem oben angegebenen Befehl wird ein VHubRoute-Objekt mit "nextHop" als angegebener Firewall erstellt, das dann einer "VHubRouteTable"-Ressource hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="99032-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="99032-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="99032-110">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $hubName = "testHub"
PS C:\> $hubVnetConnName = "testHubVnetConn"
PS C:\> $hubVnetConnection = Get-AzVirtualHubVnetConnection -Name $hubVnetConnName -ParentResourceName $hubName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "nva-traffic" -Destination @("10.20.0.0/16", "10.50.0.0/16") -DestinationType "CIDR" -NextHop $hubVnetConnection.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubVirtualNetworkConnections/testHubVnetConn
```

<span data-ttu-id="99032-111">Mit dem oben angegebenen Befehl wird ein VHubRoute-Objekt mit "nextHop" als angegebener hubVnetConnection erstellt, das dann einer "VHubRouteTable"-Ressource hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="99032-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>


### <span data-ttu-id="99032-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="99032-112">Example 3</span></span>
```powershell
PS C:\> $hub = Get-AzVirtualHub -ResourceGroupName {rgname} -Name {virtual-hub-name}
PS C:\> $hubVnetConn = Get-AzVirtualHubVnetConnection -ParentObject $hub -Name {connection-name}
PS C:\> $hubVnetConn
Name                   : conn_2
Id                     : /subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubVirtualNetworkConnections/conn_2
RemoteVirtualNetwork   : /subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualNetworks/rVnet_2
EnableInternetSecurity : True
ProvisioningState      : Succeeded
RoutingConfiguration   : {
                           "AssociatedRouteTable": {
                             "Id": "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubRouteTables/defaultRouteTable"
                           },
                           "PropagatedRouteTables": {
                             "Labels": [
                               "default"
                             ],
                             "Ids": [
                               {
                                 "Id":
                         "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubRouteTables/defaultRouteTable"
                               }
                             ]
                           },
                           "VnetRoutes": {
                             "StaticRoutes": []
                           }
                         }
                         
PS C:\> $staticRoute1 = New-AzStaticRoute -Name "static_route1" -AddressPrefix @("10.2.1.0/24", "10.2.3.0/24") -NextHopIpAddress "10.2.0.5"
PS C:\> $routingConfig = $hubVnetConn.RoutingConfiguration
PS C:\> $routingConfig.VnetRoutes.StaticRoutes = @($staticRoute1)
PS C:\> $routingConfig
AssociatedRouteTable  : Microsoft.Azure.Commands.Network.Models.PSResourceId
PropagatedRouteTables : {
                          "Labels": [
                            "default"
                          ],
                          "Ids": [
                            {
                              "Id":
                        "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/rTestHub1/hubRouteTables/defaultRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "static_route1",
                              "AddressPrefixes": [
                                "10.2.1.0/24",
                                "10.2.3.0/24"
                              ],
                              "NextHopIpAddress": "10.2.0.5"
                            }
                          ]
                        }

PS C:\> Update-AzVirtualHubVnetConnection -InputObject $hubVnetConn -RoutingConfiguration $routingConfig
```
<span data-ttu-id="99032-113">Die oben aufgeführten Befehle erhalten die RoutingConfiguration eines bereits vorhandenen AzVHubRoute und fügen dann eine statische Route für die Verbindung hinzu.</span><span class="sxs-lookup"><span data-stu-id="99032-113">The above commands will get the RoutingConfiguration of an already existing AzVHubRoute and then add a static route on the connection.</span></span> <span data-ttu-id="99032-114">Wenn Sie aber hoffen, eine neue Verbindung mit der statischen Route zu erstellen, lesen Sie hier Beispiel [1.](New-AzRoutingConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="99032-114">Alternatively, if you hope to create a new connection with the static route within it, please see Example 1 [here.](New-AzRoutingConfiguration.md)</span></span>
## <span data-ttu-id="99032-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99032-115">PARAMETERS</span></span>

### <span data-ttu-id="99032-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99032-116">-DefaultProfile</span></span>
<span data-ttu-id="99032-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99032-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99032-118">-Destination</span><span class="sxs-lookup"><span data-stu-id="99032-118">-Destination</span></span>
<span data-ttu-id="99032-119">Liste der Ziele.</span><span class="sxs-lookup"><span data-stu-id="99032-119">List of Destinations.</span></span>

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

### <span data-ttu-id="99032-120">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="99032-120">-DestinationType</span></span>
<span data-ttu-id="99032-121">Typ der Ziele.</span><span class="sxs-lookup"><span data-stu-id="99032-121">Type of Destinations.</span></span>

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

### <span data-ttu-id="99032-122">-Name</span><span class="sxs-lookup"><span data-stu-id="99032-122">-Name</span></span>
<span data-ttu-id="99032-123">Der Routenname.</span><span class="sxs-lookup"><span data-stu-id="99032-123">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99032-124">-NextHop</span><span class="sxs-lookup"><span data-stu-id="99032-124">-NextHop</span></span>
<span data-ttu-id="99032-125">Der nächste Hop.</span><span class="sxs-lookup"><span data-stu-id="99032-125">The next hop.</span></span>

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

### <span data-ttu-id="99032-126">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="99032-126">-NextHopType</span></span>
<span data-ttu-id="99032-127">Der Nächste Hop-Typ.</span><span class="sxs-lookup"><span data-stu-id="99032-127">The Next Hop type.</span></span>

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

### <span data-ttu-id="99032-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99032-128">CommonParameters</span></span>
<span data-ttu-id="99032-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99032-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99032-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99032-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99032-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="99032-131">INPUTS</span></span>

### <span data-ttu-id="99032-132">System.String</span><span class="sxs-lookup"><span data-stu-id="99032-132">System.String</span></span>

## <span data-ttu-id="99032-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="99032-133">OUTPUTS</span></span>

### <span data-ttu-id="99032-134">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span><span class="sxs-lookup"><span data-stu-id="99032-134">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="99032-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="99032-135">NOTES</span></span>

## <span data-ttu-id="99032-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="99032-136">RELATED LINKS</span></span>

[<span data-ttu-id="99032-137">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="99032-137">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="99032-138">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="99032-138">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="99032-139">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="99032-139">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="99032-140">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="99032-140">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)