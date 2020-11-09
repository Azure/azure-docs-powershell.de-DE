---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 9cd5a4417f3fd8d6d40cfdf70e6c76f1910ce7c3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301858"
---
# <span data-ttu-id="b3d41-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="b3d41-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="b3d41-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b3d41-102">SYNOPSIS</span></span>
<span data-ttu-id="b3d41-103">Erstellt ein VHubRoute-Objekt, das als Parameter an den Befehl New-AzVHubRouteTable übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="b3d41-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="b3d41-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3d41-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3d41-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3d41-105">DESCRIPTION</span></span>

<span data-ttu-id="b3d41-106">Erstellt ein VHubRoute-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b3d41-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="b3d41-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b3d41-107">EXAMPLES</span></span>

### <span data-ttu-id="b3d41-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b3d41-108">Example 1</span></span>

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

<span data-ttu-id="b3d41-109">Mit dem obigen Befehl wird ein VHubRoute-Objekt mit nextHop als angegebenen Firewall erstellt, das dann einer VHubRouteTable-Ressource hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b3d41-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="b3d41-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b3d41-110">Example 2</span></span>

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

<span data-ttu-id="b3d41-111">Der obige Befehl erstellt ein VHubRoute-Objekt mit nextHop als angegebenen hubVnetConnection, das dann einer VHubRouteTable-Ressource hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b3d41-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>


### <span data-ttu-id="b3d41-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b3d41-112">Example 3</span></span>
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
<span data-ttu-id="b3d41-113">Mit den obigen Befehlen wird die RoutingConfiguration einer bereits vorhandenen AzVHubRoute abgerufen und dann eine statische Route für die Verbindung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b3d41-113">The above commands will get the RoutingConfiguration of an already existing AzVHubRoute and then add a static route on the connection.</span></span> <span data-ttu-id="b3d41-114">Wenn Sie eine neue Verbindung mit der statischen Route darin erstellen möchten, lesen Sie hier Beispiel 1 [.](New-AzRoutingConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b3d41-114">Alternatively, if you hope to create a new connection with the static route within it, please see Example 1 [here.](New-AzRoutingConfiguration.md)</span></span>
## <span data-ttu-id="b3d41-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3d41-115">PARAMETERS</span></span>

### <span data-ttu-id="b3d41-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3d41-116">-DefaultProfile</span></span>
<span data-ttu-id="b3d41-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b3d41-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3d41-118">-Ziel</span><span class="sxs-lookup"><span data-stu-id="b3d41-118">-Destination</span></span>
<span data-ttu-id="b3d41-119">Liste der Ziele.</span><span class="sxs-lookup"><span data-stu-id="b3d41-119">List of Destinations.</span></span>

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

### <span data-ttu-id="b3d41-120">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="b3d41-120">-DestinationType</span></span>
<span data-ttu-id="b3d41-121">Art der Ziele.</span><span class="sxs-lookup"><span data-stu-id="b3d41-121">Type of Destinations.</span></span>

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

### <span data-ttu-id="b3d41-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b3d41-122">-Name</span></span>
<span data-ttu-id="b3d41-123">Der Name der Route.</span><span class="sxs-lookup"><span data-stu-id="b3d41-123">The route name.</span></span>

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

### <span data-ttu-id="b3d41-124">-NextHop</span><span class="sxs-lookup"><span data-stu-id="b3d41-124">-NextHop</span></span>
<span data-ttu-id="b3d41-125">Nächster Hop.</span><span class="sxs-lookup"><span data-stu-id="b3d41-125">The next hop.</span></span>

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

### <span data-ttu-id="b3d41-126">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="b3d41-126">-NextHopType</span></span>
<span data-ttu-id="b3d41-127">Der nächste Hop-Typ.</span><span class="sxs-lookup"><span data-stu-id="b3d41-127">The Next Hop type.</span></span>

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

### <span data-ttu-id="b3d41-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3d41-128">CommonParameters</span></span>
<span data-ttu-id="b3d41-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3d41-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3d41-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3d41-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3d41-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b3d41-131">INPUTS</span></span>

### <span data-ttu-id="b3d41-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b3d41-132">System.String</span></span>

## <span data-ttu-id="b3d41-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b3d41-133">OUTPUTS</span></span>

### <span data-ttu-id="b3d41-134">Microsoft. Azure. Commands. Network. Models. PSVHubRoute</span><span class="sxs-lookup"><span data-stu-id="b3d41-134">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="b3d41-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="b3d41-135">NOTES</span></span>

## <span data-ttu-id="b3d41-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b3d41-136">RELATED LINKS</span></span>

[<span data-ttu-id="b3d41-137">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b3d41-137">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="b3d41-138">Neu – AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b3d41-138">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="b3d41-139">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b3d41-139">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="b3d41-140">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b3d41-140">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)