---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
ms.openlocfilehash: 4665e67b64baa87273c365137cc2247e86efd2c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938603"
---
# <span data-ttu-id="a5366-101">Get-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="a5366-101">Get-AzExpressRouteConnection</span></span>

## <span data-ttu-id="a5366-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5366-102">SYNOPSIS</span></span>
<span data-ttu-id="a5366-103">Ruft eine ExpressRoute-Verbindung nach Name ab oder listet alle mit einem ExpressRouteGateway verbundenen ExpressRoute-Verbindungen auf.</span><span class="sxs-lookup"><span data-stu-id="a5366-103">Gets a ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="a5366-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5366-104">SYNTAX</span></span>

### <span data-ttu-id="a5366-105">ByExpressRouteGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5366-105">ByExpressRouteGatewayName (Default)</span></span>
```
Get-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5366-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="a5366-106">ByExpressRouteGatewayObject</span></span>
```
Get-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5366-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="a5366-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5366-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5366-108">DESCRIPTION</span></span>
<span data-ttu-id="a5366-109">Ruft eine ExpressRoute-Verbindung nach Name ab oder listet alle mit einem ExpressRouteGateway verbundenen ExpressRoute-Verbindungen auf.</span><span class="sxs-lookup"><span data-stu-id="a5366-109">Gets an ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="a5366-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a5366-110">EXAMPLES</span></span>

### <span data-ttu-id="a5366-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a5366-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection"

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
EnableInternetSecurity             : False
RoutingConfiguration               : {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                       },
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                             "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                           }
                                         ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     }
```

<span data-ttu-id="a5366-112">Mit den vorstehenden Beispielen werden eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub und eine ExpressRouteSite in West USA in der Ressourcengruppe "testRG" in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="a5366-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="a5366-113">Anschließend wird im virtuellen Hub ein ExpressRoute-Gateway mit zwei Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="a5366-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="a5366-114">Nachdem das Gateway erstellt wurde, wird es über den Befehl New-AzExpressRouteConnection mit dem lokalen ExpressRoute-Schaltkreis verbunden.</span><span class="sxs-lookup"><span data-stu-id="a5366-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="a5366-115">Anschließend ruft sie die Verbindung unter dem Verbindungsnamen ab.</span><span class="sxs-lookup"><span data-stu-id="a5366-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="a5366-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a5366-116">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName ps9361 -ParentResourceName testExpressRoutegw -Name test*

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection1
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection1
EnableInternetSecurity             : False
RoutingConfiguration               : {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                       },
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                             "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                           }
                                         ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     }

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection2
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection2
EnableInternetSecurity             : False
RoutingConfiguration               : {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                       },
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                             "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                           }
                                         ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     }
```

<span data-ttu-id="a5366-117">Dieser Befehl zeigt alle Verbindungen in ExpressRoute "testExpressRoutegw" an, die mit "test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="a5366-117">This command will get all Connections in ExpressRoute "testExpressRoutegw" that start with "test"</span></span>

## <span data-ttu-id="a5366-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a5366-118">PARAMETERS</span></span>

### <span data-ttu-id="a5366-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5366-119">-DefaultProfile</span></span>
<span data-ttu-id="a5366-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5366-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5366-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="a5366-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="a5366-122">Der übergeordnete Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="a5366-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5366-123">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="a5366-123">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="a5366-124">Das übergeordnete ExpressRouteGateway für diese Verbindung.</span><span class="sxs-lookup"><span data-stu-id="a5366-124">The parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5366-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a5366-125">-Name</span></span>
<span data-ttu-id="a5366-126">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="a5366-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="a5366-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a5366-127">-ParentResourceId</span></span>
<span data-ttu-id="a5366-128">Die Ressourcen-ID des übergeordneten ExpressRouteGateway für diese Verbindung.</span><span class="sxs-lookup"><span data-stu-id="a5366-128">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: ExpressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5366-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5366-129">-ResourceGroupName</span></span>
<span data-ttu-id="a5366-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a5366-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5366-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5366-131">CommonParameters</span></span>
<span data-ttu-id="a5366-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5366-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5366-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5366-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5366-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a5366-134">INPUTS</span></span>

### <span data-ttu-id="a5366-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a5366-135">System.String</span></span>

## <span data-ttu-id="a5366-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a5366-136">OUTPUTS</span></span>

### <span data-ttu-id="a5366-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="a5366-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="a5366-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a5366-138">NOTES</span></span>

## <span data-ttu-id="a5366-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a5366-139">RELATED LINKS</span></span>
