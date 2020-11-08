---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
ms.openlocfilehash: dc3cde19bde2da95fd2ffc731223783c1963d1f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174276"
---
# <span data-ttu-id="bf843-101">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="bf843-101">Set-AzExpressRouteConnection</span></span>

## <span data-ttu-id="bf843-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf843-102">SYNOPSIS</span></span>
<span data-ttu-id="bf843-103">Aktualisiert eine Express-Route-Verbindung, die zwischen einem Express-Route-Gateway und einem lokalen Express-Route Circuit-Peering erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="bf843-103">Updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="bf843-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf843-104">SYNTAX</span></span>

### <span data-ttu-id="bf843-105">ByExpressRouteConnectionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="bf843-105">ByExpressRouteConnectionName (Default)</span></span>
```
Set-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf843-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="bf843-106">ByExpressRouteConnectionResourceId</span></span>
```
Set-AzExpressRouteConnection -ResourceId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf843-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="bf843-107">ByExpressRouteConnectionObject</span></span>
```
Set-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-AuthorizationKey <String>]
 [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf843-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf843-108">DESCRIPTION</span></span>
<span data-ttu-id="bf843-109">Das Cmdlet " **Satz-AzExpressRouteConnection** " aktualisiert eine Express Route-Verbindung, die zwischen einem Express-Route-Gateway und einem lokalen Express-Route-Circuit-Peering erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="bf843-109">The **Set-AzExpressRouteConnection** cmdlet updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="bf843-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf843-110">EXAMPLES</span></span>

### <span data-ttu-id="bf843-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bf843-111">Example 1</span></span>

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
PS C:\> Set-AzExpressRouteConnection -InputObject $ExpressRouteConnection -RoutingWeight 30

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 30
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
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

<span data-ttu-id="bf843-112">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuellen Hub und einen ExpressRouteSite in West US in "testRG"-Ressourcengruppe in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="bf843-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="bf843-113">Anschließend wird ein Express Route-Gateway im virtuellen Hub mit zwei Skaleneinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="bf843-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="bf843-114">Nachdem das Gateway erstellt wurde, wird es mit dem Express Route-Schaltkreis-Peering mit dem Befehl "New-AzExpressRouteConnection" verbunden.</span><span class="sxs-lookup"><span data-stu-id="bf843-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit peering using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="bf843-115">Die Verbindung wird dann mit dem Befehl Set-AzExpressRouteConnection auf einen anderen RoutingWeight aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bf843-115">The connection is then updated to have a different RoutingWeight by using the Set-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="bf843-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf843-116">PARAMETERS</span></span>

### <span data-ttu-id="bf843-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf843-117">-AsJob</span></span>
<span data-ttu-id="bf843-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="bf843-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf843-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="bf843-119">-AuthorizationKey</span></span>
<span data-ttu-id="bf843-120">Der Autorisierungsschlüssel, der zum Erstellen der Express Route-Gatewayverbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf843-120">The authorization key to be used to create the ExpressRoute gateway connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf843-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf843-121">-DefaultProfile</span></span>
<span data-ttu-id="bf843-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bf843-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf843-123">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="bf843-123">-EnableInternetSecurity</span></span>
<span data-ttu-id="bf843-124">Aktivieren der Internetsicherheit für diese Express Route-Gateway-Verbindung</span><span class="sxs-lookup"><span data-stu-id="bf843-124">Enable internet security for this ExpressRoute Gateway connection</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf843-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="bf843-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="bf843-126">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="bf843-126">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf843-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bf843-127">-InputObject</span></span>
<span data-ttu-id="bf843-128">Das zu Aktualisier ExpressRouteConnection-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bf843-128">The ExpressRouteConnection object to update.</span></span>

```yaml
Type: PSExpressRouteConnection
Parameter Sets: ByExpressRouteConnectionObject
Aliases: ExpressRouteConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf843-129">-Name</span><span class="sxs-lookup"><span data-stu-id="bf843-129">-Name</span></span>
<span data-ttu-id="bf843-130">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="bf843-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf843-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf843-131">-ResourceGroupName</span></span>
<span data-ttu-id="bf843-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bf843-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf843-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="bf843-133">-ResourceId</span></span>
<span data-ttu-id="bf843-134">Die Ressourcen-ID des zu löschenden ExpressRouteConnection-Objekts.</span><span class="sxs-lookup"><span data-stu-id="bf843-134">The resource id of the ExpressRouteConnection object to delete.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionResourceId
Aliases: ExpressRouteConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf843-135">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf843-135">-RoutingConfiguration</span></span>
<span data-ttu-id="bf843-136">Routing Konfiguration für diese Verbindung</span><span class="sxs-lookup"><span data-stu-id="bf843-136">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf843-137">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="bf843-137">-RoutingWeight</span></span>
<span data-ttu-id="bf843-138">Die Gewichtung, die dieser Verbindung für das Paketrouting zugewiesen werden muss.</span><span class="sxs-lookup"><span data-stu-id="bf843-138">The weight that needs to be assigned to this connection for packet routing.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf843-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bf843-139">-Confirm</span></span>
<span data-ttu-id="bf843-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf843-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf843-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf843-141">-WhatIf</span></span>
<span data-ttu-id="bf843-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf843-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf843-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf843-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf843-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf843-144">CommonParameters</span></span>
<span data-ttu-id="bf843-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf843-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf843-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf843-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf843-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf843-147">INPUTS</span></span>

### <span data-ttu-id="bf843-148">System. String</span><span class="sxs-lookup"><span data-stu-id="bf843-148">System.String</span></span>

### <span data-ttu-id="bf843-149">Microsoft. Azure. Commands. Network. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="bf843-149">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="bf843-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf843-150">OUTPUTS</span></span>

### <span data-ttu-id="bf843-151">Microsoft. Azure. Commands. Network. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="bf843-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="bf843-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf843-152">NOTES</span></span>

## <span data-ttu-id="bf843-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf843-153">RELATED LINKS</span></span>

[<span data-ttu-id="bf843-154">Neu – AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf843-154">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
