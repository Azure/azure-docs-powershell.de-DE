---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8b4a8c9f-874c-4a27-b87e-c8ad7e73188d
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 432af4d97f2ddf085d23db33cc0f2604c1fc7aa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918640"
---
# <span data-ttu-id="3a597-101">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3a597-101">Set-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="3a597-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a597-102">SYNOPSIS</span></span>
<span data-ttu-id="3a597-103">Aktualisiert eine in Private Peerings erstellte Verbindungskonfiguration für einen ExpressRoute Circuit.</span><span class="sxs-lookup"><span data-stu-id="3a597-103">Updates a circuit connection configuration created in Private Peerings for an Express Route Circuit.</span></span> 

## <span data-ttu-id="3a597-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a597-104">SYNTAX</span></span>

### <span data-ttu-id="3a597-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="3a597-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a597-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3a597-106">SetByResourceId</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a597-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a597-107">DESCRIPTION</span></span>
<span data-ttu-id="3a597-108">Das **Cmdlet Set-AzExpressRouteCircuitConnectionConfig** aktualisiert eine in privatem Peering erstellte Verbindungskonfiguration für einen ExpressRoute-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="3a597-108">The **Set-AzExpressRouteCircuitConnectionConfig** cmdlet updates a circuit connection configuration created in private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="3a597-109">Dies ermöglicht das Peering von zwei ExpressRoute Circuits über Regionen oder Abonnements hinweg.</span><span class="sxs-lookup"><span data-stu-id="3a597-109">This allows peering two Express Route Circuits across regions or subscriptions.</span></span>
<span data-ttu-id="3a597-110">Beachten Sie, dass Sie vor dem Ausführen von **Set-AzExpressRouteCircuitConnectionConfig** die Verbindung mit **Add-AzExpressRouteCircuitConnectionConfig hinzufügen müssen.**</span><span class="sxs-lookup"><span data-stu-id="3a597-110">Note that, before running **Set-AzExpressRouteCircuitConnectionConfig** you must add the circuit connection using **Add-AzExpressRouteCircuitConnectionConfig**.</span></span> <span data-ttu-id="3a597-111">Nachdem Sie **Set-AzExpressRouteCircuitPeeringConfig** ausgeführt haben, müssen Sie auch das cmdlet Set-AzExpressRouteCircuit aufrufen, um die Konfiguration zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3a597-111">Also, after running **Set-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>


## <span data-ttu-id="3a597-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3a597-112">EXAMPLES</span></span>

### <span data-ttu-id="3a597-113">Beispiel 1: Aktualisieren einer Verbindungsressource für einen vorhandenen ExpressRoute-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="3a597-113">Example 1: Update a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = 'aa:bb::0/125'
$addressPrefixType = 'IPv6'
Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="3a597-114">Beispiel 2: Festlegen einer Verbindungskonfiguration mithilfe von Piping auf einen vorhandenen ExpressRoute-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="3a597-114">Example 2: Set a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="3a597-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3a597-115">PARAMETERS</span></span>

### <span data-ttu-id="3a597-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3a597-116">-AddressPrefix</span></span>
<span data-ttu-id="3a597-117">Mindestens /29 Kundenadressenplatz zum Erstellen von VxLan-Tunneln zwischen Expressroutenkreisläufen für IPv4-Tunnel.</span><span class="sxs-lookup"><span data-stu-id="3a597-117">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="3a597-118">oder mindestens /125 Kundenadressenplatz zum Erstellen von VxLan-Tunneln zwischen ExpressRoute Circuits für IPv6-Tunnel.</span><span class="sxs-lookup"><span data-stu-id="3a597-118">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="3a597-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="3a597-119">-AddressPrefixType</span></span>
<span data-ttu-id="3a597-120">Gibt die Adressfamilie an, zu der das Adresspräfix gehört.</span><span class="sxs-lookup"><span data-stu-id="3a597-120">Specifies the address family that address prefix belongs to.</span></span>

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

### <span data-ttu-id="3a597-121">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="3a597-121">-AuthorizationKey</span></span>
<span data-ttu-id="3a597-122">Autorisierungsschlüssel für peer Express Route Circuit in einem anderen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3a597-122">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="3a597-123">Die Autorisierung für Peerschaltungen kann mit vorhandenen Befehlen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3a597-123">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="3a597-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a597-124">-DefaultProfile</span></span>
<span data-ttu-id="3a597-125">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a597-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a597-126">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3a597-126">-ExpressRouteCircuit</span></span>
<span data-ttu-id="3a597-127">Der geänderte ExpressRoute-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="3a597-127">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="3a597-128">Dies ist das vom **Get-AzExpressRouteCircuit-Cmdlet** zurückgegebene Azure-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3a597-128">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="3a597-129">-Name</span><span class="sxs-lookup"><span data-stu-id="3a597-129">-Name</span></span>
<span data-ttu-id="3a597-130">Der Name der zu hinzufügende Schaltkreisverbindungsressource.</span><span class="sxs-lookup"><span data-stu-id="3a597-130">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="3a597-131">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="3a597-131">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="3a597-132">Ressourcen-ID für privates Peering von Remoteschaltungen, die mit dem aktuellen Schaltkreis ge peeret werden.</span><span class="sxs-lookup"><span data-stu-id="3a597-132">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="3a597-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3a597-133">-Confirm</span></span>
<span data-ttu-id="3a597-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3a597-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a597-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a597-135">-WhatIf</span></span>
<span data-ttu-id="3a597-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a597-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a597-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a597-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a597-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a597-138">CommonParameters</span></span>
<span data-ttu-id="3a597-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a597-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a597-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a597-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a597-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3a597-141">INPUTS</span></span>

### <span data-ttu-id="3a597-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3a597-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="3a597-143">System.String</span><span class="sxs-lookup"><span data-stu-id="3a597-143">System.String</span></span>

## <span data-ttu-id="3a597-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3a597-144">OUTPUTS</span></span>

### <span data-ttu-id="3a597-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3a597-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3a597-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3a597-146">NOTES</span></span>

## <span data-ttu-id="3a597-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3a597-147">RELATED LINKS</span></span>

[<span data-ttu-id="3a597-148">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3a597-148">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="3a597-149">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3a597-149">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="3a597-150">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3a597-150">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="3a597-151">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3a597-151">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="3a597-152">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3a597-152">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
