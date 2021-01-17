---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: e8691d31956e1ee59f692cc3d37fa1e2d5598efa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98308547"
---
# <span data-ttu-id="3251d-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3251d-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="3251d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3251d-102">SYNOPSIS</span></span>
<span data-ttu-id="3251d-103">Fügt dem privaten Peering eines Expressroutenkreises eine Verbindungskonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="3251d-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="3251d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3251d-104">SYNTAX</span></span>

### <span data-ttu-id="3251d-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="3251d-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3251d-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3251d-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3251d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3251d-107">DESCRIPTION</span></span>
<span data-ttu-id="3251d-108">Das **Cmdlet "Add-AzExpressRouteCircuitConnectionConfig"** fügt dem privaten Peering für einen "ExpressRoute"-Schaltkreis eine Verbindungskonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="3251d-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="3251d-109">Dies ermöglicht das Peering von zwei ExpressRoute-Schaltkreisen über Regionen oder Abonnements hinweg. Beachten Sie, dass Sie nach der Ausführung von **"Add-AzExpressRouteCircuitConnectionConfig"** das cmdlet Set-AzExpressRouteCircuit aufrufen müssen, um die Konfiguration zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3251d-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitConnectionConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="3251d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3251d-110">EXAMPLES</span></span>

### <span data-ttu-id="3251d-111">Beispiel 1: Hinzufügen einer Schaltkreisverbindungsressource zu einem vorhandenen</span><span class="sxs-lookup"><span data-stu-id="3251d-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
$addressPrefixType = 'IPv4'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="3251d-112">Beispiel 2: Hinzufügen einer Verbindungskonfiguration mit einer Leitung zu einem vorhandenen "ExpressRoute-Schaltkreis"</span><span class="sxs-lookup"><span data-stu-id="3251d-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="3251d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3251d-113">PARAMETERS</span></span>

### <span data-ttu-id="3251d-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3251d-114">-AddressPrefix</span></span>
<span data-ttu-id="3251d-115">Mindestens /29 Kundenad address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span><span class="sxs-lookup"><span data-stu-id="3251d-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="3251d-116">oder mindestens /125 Kundenad address space zum Erstellen von VxLan-Tunneln zwischen Express Route Circuits für IPv6-Tunnel.</span><span class="sxs-lookup"><span data-stu-id="3251d-116">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="3251d-117">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="3251d-117">-AddressPrefixType</span></span>
<span data-ttu-id="3251d-118">Damit wird die Adressfamilie angegeben, zu der das Adresspräfix gehört.</span><span class="sxs-lookup"><span data-stu-id="3251d-118">This specifies the Address Family that address prefix belongs to.</span></span>

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

### <span data-ttu-id="3251d-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="3251d-119">-AuthorizationKey</span></span>
<span data-ttu-id="3251d-120">Autorisierungsschlüssel für peer Express Route Circuit in einem anderen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3251d-120">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="3251d-121">Autorisierung für Peerkreise kann mit vorhandenen Befehlen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3251d-121">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="3251d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3251d-122">-DefaultProfile</span></span>
<span data-ttu-id="3251d-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3251d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3251d-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3251d-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="3251d-125">Der zu ändernde ExpressRoute-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="3251d-125">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="3251d-126">Dies ist das Azure-Objekt, das vom **Cmdlet "Get-AzExpressRouteCircuit"** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3251d-126">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="3251d-127">-Name</span><span class="sxs-lookup"><span data-stu-id="3251d-127">-Name</span></span>
<span data-ttu-id="3251d-128">Der Name der Verbindungsressource, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3251d-128">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="3251d-129">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="3251d-129">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="3251d-130">Ressourcen-ID für privates Peering eines Remotekreises, das mit dem aktuellen Schaltkreis peered wird.</span><span class="sxs-lookup"><span data-stu-id="3251d-130">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="3251d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3251d-131">-Confirm</span></span>
<span data-ttu-id="3251d-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3251d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3251d-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3251d-133">-WhatIf</span></span>
<span data-ttu-id="3251d-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3251d-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3251d-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3251d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3251d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3251d-136">CommonParameters</span></span>
<span data-ttu-id="3251d-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3251d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3251d-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3251d-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3251d-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3251d-139">INPUTS</span></span>

### <span data-ttu-id="3251d-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3251d-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="3251d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3251d-141">System.String</span></span>

## <span data-ttu-id="3251d-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3251d-142">OUTPUTS</span></span>

### <span data-ttu-id="3251d-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3251d-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3251d-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3251d-144">NOTES</span></span>

## <span data-ttu-id="3251d-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3251d-145">RELATED LINKS</span></span>

[<span data-ttu-id="3251d-146">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3251d-146">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="3251d-147">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3251d-147">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="3251d-148">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3251d-148">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="3251d-149">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3251d-149">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="3251d-150">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3251d-150">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)