---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8b4a8c9f-874c-4a27-b87e-c8ad7e73188d
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 432af4d97f2ddf085d23db33cc0f2604c1fc7aa5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472178"
---
# <span data-ttu-id="ed208-101">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ed208-101">Set-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="ed208-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed208-102">SYNOPSIS</span></span>
<span data-ttu-id="ed208-103">Aktualisiert eine Verbindungskonfiguration eines Schaltkreises, die in privaten Peerings für einen Expressroutenkreis erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ed208-103">Updates a circuit connection configuration created in Private Peerings for an Express Route Circuit.</span></span> 

## <span data-ttu-id="ed208-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed208-104">SYNTAX</span></span>

### <span data-ttu-id="ed208-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed208-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed208-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ed208-106">SetByResourceId</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed208-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed208-107">DESCRIPTION</span></span>
<span data-ttu-id="ed208-108">Das **Cmdlet Set-AzExpressRouteCircuitConnectionConfig** aktualisiert eine Schaltkreisverbindungskonfiguration, die in privatem Peering für einen ExpressRoute-Schaltkreis erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ed208-108">The **Set-AzExpressRouteCircuitConnectionConfig** cmdlet updates a circuit connection configuration created in private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="ed208-109">Dies ermöglicht das Peering von zwei Expressrouten über Regionen oder Abonnements hinweg.</span><span class="sxs-lookup"><span data-stu-id="ed208-109">This allows peering two Express Route Circuits across regions or subscriptions.</span></span>
<span data-ttu-id="ed208-110">Beachten Sie, dass Sie vor dem Ausführen von **Set-AzExpressRouteCircuitConnectionConfig** die Verbindungsverbindung mithilfe von **Add-AzExpressRouteCircuitConnectionConfig hinzufügen müssen.**</span><span class="sxs-lookup"><span data-stu-id="ed208-110">Note that, before running **Set-AzExpressRouteCircuitConnectionConfig** you must add the circuit connection using **Add-AzExpressRouteCircuitConnectionConfig**.</span></span> <span data-ttu-id="ed208-111">Außerdem müssen Sie nach der Ausführung von **Set-AzExpressRouteCircuitPeeringConfig** das cmdlet Set-AzExpressRouteCircuit aufrufen, um die Konfiguration zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ed208-111">Also, after running **Set-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>


## <span data-ttu-id="ed208-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ed208-112">EXAMPLES</span></span>

### <span data-ttu-id="ed208-113">Beispiel 1: Aktualisieren einer Schaltkreisverbindungsressource für einen vorhandenen ExpressRoute-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="ed208-113">Example 1: Update a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = 'aa:bb::0/125'
$addressPrefixType = 'IPv6'
Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="ed208-114">Beispiel 2: Festlegen einer Verbindungskonfiguration für eine Schaltkreisverbindung mithilfe der Piping zu einem vorhandenen ExpressRoute-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="ed208-114">Example 2: Set a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="ed208-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed208-115">PARAMETERS</span></span>

### <span data-ttu-id="ed208-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ed208-116">-AddressPrefix</span></span>
<span data-ttu-id="ed208-117">Mindestens /29 Kundenad address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span><span class="sxs-lookup"><span data-stu-id="ed208-117">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="ed208-118">oder mindestens /125 Kundenad address space zum Erstellen von VxLan-Tunneln zwischen Express Route Circuits für IPv6-Tunnel.</span><span class="sxs-lookup"><span data-stu-id="ed208-118">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="ed208-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="ed208-119">-AddressPrefixType</span></span>
<span data-ttu-id="ed208-120">Gibt die Adressfamilie an, zu der das Adresspräfix gehört.</span><span class="sxs-lookup"><span data-stu-id="ed208-120">Specifies the address family that address prefix belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: IPv4
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed208-121">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="ed208-121">-AuthorizationKey</span></span>
<span data-ttu-id="ed208-122">Autorisierungsschlüssel für peer Express Route Circuit in einem anderen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed208-122">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="ed208-123">Autorisierung für Peerkreise kann mit vorhandenen Befehlen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ed208-123">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="ed208-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed208-124">-DefaultProfile</span></span>
<span data-ttu-id="ed208-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed208-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed208-126">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ed208-126">-ExpressRouteCircuit</span></span>
<span data-ttu-id="ed208-127">Der zu ändernde ExpressRoute-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="ed208-127">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="ed208-128">Dies ist das Azure-Objekt, das vom **Cmdlet "Get-AzExpressRouteCircuit"** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ed208-128">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed208-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ed208-129">-Name</span></span>
<span data-ttu-id="ed208-130">Der Name der Verbindungsressource, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed208-130">The name of the circuit connection resource to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed208-131">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="ed208-131">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="ed208-132">Ressourcen-ID für privates Peering eines Remotekreises, das mit dem aktuellen Schaltkreis peered wird.</span><span class="sxs-lookup"><span data-stu-id="ed208-132">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed208-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed208-133">-Confirm</span></span>
<span data-ttu-id="ed208-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed208-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed208-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ed208-135">-WhatIf</span></span>
<span data-ttu-id="ed208-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed208-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed208-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed208-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed208-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed208-138">CommonParameters</span></span>
<span data-ttu-id="ed208-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed208-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed208-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed208-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed208-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ed208-141">INPUTS</span></span>

### <span data-ttu-id="ed208-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ed208-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="ed208-143">System.String</span><span class="sxs-lookup"><span data-stu-id="ed208-143">System.String</span></span>

## <span data-ttu-id="ed208-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ed208-144">OUTPUTS</span></span>

### <span data-ttu-id="ed208-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ed208-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ed208-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ed208-146">NOTES</span></span>

## <span data-ttu-id="ed208-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ed208-147">RELATED LINKS</span></span>

[<span data-ttu-id="ed208-148">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ed208-148">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="ed208-149">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ed208-149">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="ed208-150">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ed208-150">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="ed208-151">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ed208-151">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="ed208-152">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ed208-152">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
