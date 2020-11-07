---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
ms.openlocfilehash: 72aa8af012addf4fa309adc7c63467ecaf667fff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821607"
---
# <span data-ttu-id="4b0a1-101">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="4b0a1-101">New-AzExpressRouteConnection</span></span>

## <span data-ttu-id="4b0a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4b0a1-102">SYNOPSIS</span></span>
<span data-ttu-id="4b0a1-103">Erstellt eine Express Route-Verbindung, die ein Express Route-Gateway mit einem lokalen Express Route-Schaltkreis verbindet.</span><span class="sxs-lookup"><span data-stu-id="4b0a1-103">Creates an ExpressRoute connection that connects an ExpressRoute gateway to an on premise ExpressRoute circuit</span></span>

## <span data-ttu-id="4b0a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b0a1-104">SYNTAX</span></span>

### <span data-ttu-id="4b0a1-105">ByExpressRouteGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4b0a1-105">ByExpressRouteGatewayName (Default)</span></span>
```
New-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b0a1-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="4b0a1-106">ByExpressRouteGatewayObject</span></span>
```
New-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b0a1-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="4b0a1-107">ByExpressRouteGatewayResourceId</span></span>
```
New-AzExpressRouteConnection -ParentResourceId <String> -Name <String> -ExpressRouteCircuitPeeringId <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b0a1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b0a1-108">DESCRIPTION</span></span>
<span data-ttu-id="4b0a1-109">Erstellt eine Express Route-Verbindung zwischen einer lokalen Express Route Circuit-BGP, die mit dem Express Route-Gateway innerhalb eines virtuellen Hubs späht.</span><span class="sxs-lookup"><span data-stu-id="4b0a1-109">Creates an ExpressRoute connection between an on-premise ExpressRoute circuit BGP peering to the ExpressRoute gateway inside a Virtual hub.</span></span>

## <span data-ttu-id="4b0a1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b0a1-110">EXAMPLES</span></span>

### <span data-ttu-id="4b0a1-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4b0a1-111">Example 1</span></span>

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
ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
```

<span data-ttu-id="4b0a1-112">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuelles Drehkreuz, Express-Routen-Gateway und einen Express Route-Circuit mit Private Peering in West Central US in der "testRG"-Ressourcengruppe in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="4b0a1-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub, Express Route gateway and an ExpressRoute circuit with private peering in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="4b0a1-113">Nachdem das Gateway erstellt wurde, wird es mit dem Express Route-Schaltungs Peering mit dem Befehl New-AzExpressRouteConnection verbunden.</span><span class="sxs-lookup"><span data-stu-id="4b0a1-113">Once the gateway has been created, it is connected to the ExpressRoute Circuit Peering using the New-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="4b0a1-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b0a1-114">PARAMETERS</span></span>

### <span data-ttu-id="4b0a1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b0a1-115">-AsJob</span></span>
<span data-ttu-id="4b0a1-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4b0a1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b0a1-117">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="4b0a1-117">-AuthorizationKey</span></span>
<span data-ttu-id="4b0a1-118">Ein vom Express Route-Schaltkreis Besitzer abgerufener Schlüssel, um eine Verbindung mit einem Gateway in einem anderen Abonnement erstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="4b0a1-118">A key obtained from the ExpressRoute circuit owner to be able to create a connection with a gateway in a different subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b0a1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b0a1-119">-DefaultProfile</span></span>
<span data-ttu-id="4b0a1-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4b0a1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b0a1-121">-ExpressRouteCircuitPeeringId</span><span class="sxs-lookup"><span data-stu-id="4b0a1-121">-ExpressRouteCircuitPeeringId</span></span>
<span data-ttu-id="4b0a1-122">Die Ressourcen-ID des Express Route Circuit-Peers, zu dem diese Express-Route-Gateway-Verbindung erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b0a1-122">The resource id of the Express Route Circuit Peering to which this Express Route gateway connection is to be created to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b0a1-123">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="4b0a1-123">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="4b0a1-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4b0a1-124">The resource group name.</span></span>

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

### <span data-ttu-id="4b0a1-125">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="4b0a1-125">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="4b0a1-126">Der übergeordnete ExpressRouteGateway für diese Verbindung.</span><span class="sxs-lookup"><span data-stu-id="4b0a1-126">The parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="4b0a1-127">-Name</span><span class="sxs-lookup"><span data-stu-id="4b0a1-127">-Name</span></span>
<span data-ttu-id="4b0a1-128">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="4b0a1-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b0a1-129">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4b0a1-129">-ParentResourceId</span></span>
<span data-ttu-id="4b0a1-130">Die Ressourcen-ID des übergeordneten ExpressRouteGateway für diese Verbindung.</span><span class="sxs-lookup"><span data-stu-id="4b0a1-130">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="4b0a1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b0a1-131">-ResourceGroupName</span></span>
<span data-ttu-id="4b0a1-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4b0a1-132">The resource group name.</span></span>

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

### <span data-ttu-id="4b0a1-133">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="4b0a1-133">-RoutingWeight</span></span>
<span data-ttu-id="4b0a1-134">Die Gewichtung für das Paketrouting, das dieser Verbindung zugewiesen werden muss.</span><span class="sxs-lookup"><span data-stu-id="4b0a1-134">The weight for packet routing that needs to be assigned to this connection.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b0a1-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4b0a1-135">-Confirm</span></span>
<span data-ttu-id="4b0a1-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b0a1-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b0a1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b0a1-137">-WhatIf</span></span>
<span data-ttu-id="4b0a1-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4b0a1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b0a1-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b0a1-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b0a1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b0a1-140">CommonParameters</span></span>
<span data-ttu-id="4b0a1-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b0a1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b0a1-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b0a1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b0a1-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b0a1-143">INPUTS</span></span>

### <span data-ttu-id="4b0a1-144">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="4b0a1-144">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="4b0a1-145">System. String</span><span class="sxs-lookup"><span data-stu-id="4b0a1-145">System.String</span></span>

## <span data-ttu-id="4b0a1-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4b0a1-146">OUTPUTS</span></span>

### <span data-ttu-id="4b0a1-147">Microsoft. Azure. Commands. Network. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="4b0a1-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="4b0a1-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b0a1-148">NOTES</span></span>

## <span data-ttu-id="4b0a1-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4b0a1-149">RELATED LINKS</span></span>
