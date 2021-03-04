---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 19ceeb045c3a7cc86dd9152ee08d12078d858240
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921144"
---
# <span data-ttu-id="f4521-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f4521-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="f4521-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4521-102">SYNOPSIS</span></span>
<span data-ttu-id="f4521-103">Fügt dem privaten Peering eines ExpressRoute Circuit eine Verbindungskonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="f4521-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="f4521-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4521-104">SYNTAX</span></span>

### <span data-ttu-id="f4521-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4521-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4521-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f4521-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4521-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4521-107">DESCRIPTION</span></span>
<span data-ttu-id="f4521-108">Das **Add-AzExpressRouteCircuitConnectionConfig-Cmdlet** fügt dem privaten Peering für einen ExpressRoute-Schaltkreis eine Verbindungskonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="f4521-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="f4521-109">Dies ermöglicht das Peering von zwei ExpressRoute Circuits über Regionen oder Abonnements hinweg. Beachten Sie, dass Sie nach dem Ausführen von **Add-AzExpressRouteCircuitConnectionConfig** das cmdlet Set-AzExpressRouteCircuit aufrufen müssen, um die Konfiguration zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f4521-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitConnectionConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="f4521-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f4521-110">EXAMPLES</span></span>

### <span data-ttu-id="f4521-111">Beispiel 1: Hinzufügen einer Verbindungsressource zu einem vorhandenen ExpressRoute-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="f4521-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
$addressPrefixType = 'IPv4'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="f4521-112">Beispiel 2: Hinzufügen einer Verbindungskonfiguration mit Piping zu einem vorhandenen ExpressRoute-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="f4521-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="f4521-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f4521-113">PARAMETERS</span></span>

### <span data-ttu-id="f4521-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f4521-114">-AddressPrefix</span></span>
<span data-ttu-id="f4521-115">Mindestens /29 Kundenadressenplatz zum Erstellen von VxLan-Tunneln zwischen Expressroutenkreisläufen für IPv4-Tunnel.</span><span class="sxs-lookup"><span data-stu-id="f4521-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="f4521-116">oder mindestens /125 Kundenadressenplatz zum Erstellen von VxLan-Tunneln zwischen ExpressRoute Circuits für IPv6-Tunnel.</span><span class="sxs-lookup"><span data-stu-id="f4521-116">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="f4521-117">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="f4521-117">-AddressPrefixType</span></span>
<span data-ttu-id="f4521-118">Dadurch wird die Adressfamilie angegeben, zu der das Adresspräfix gehört.</span><span class="sxs-lookup"><span data-stu-id="f4521-118">This specifies the Address Family that address prefix belongs to.</span></span>

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

### <span data-ttu-id="f4521-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="f4521-119">-AuthorizationKey</span></span>
<span data-ttu-id="f4521-120">Autorisierungsschlüssel für peer Express Route Circuit in einem anderen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f4521-120">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="f4521-121">Die Autorisierung für Peerschaltungen kann mit vorhandenen Befehlen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f4521-121">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="f4521-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4521-122">-DefaultProfile</span></span>
<span data-ttu-id="f4521-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f4521-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4521-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f4521-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="f4521-125">Der geänderte ExpressRoute-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="f4521-125">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="f4521-126">Dies ist das vom **Get-AzExpressRouteCircuit-Cmdlet** zurückgegebene Azure-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f4521-126">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="f4521-127">-Name</span><span class="sxs-lookup"><span data-stu-id="f4521-127">-Name</span></span>
<span data-ttu-id="f4521-128">Der Name der zu hinzufügende Schaltkreisverbindungsressource.</span><span class="sxs-lookup"><span data-stu-id="f4521-128">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="f4521-129">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="f4521-129">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="f4521-130">Ressourcen-ID für privates Peering von Remoteschaltungen, die mit dem aktuellen Schaltkreis ge peeret werden.</span><span class="sxs-lookup"><span data-stu-id="f4521-130">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="f4521-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f4521-131">-Confirm</span></span>
<span data-ttu-id="f4521-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4521-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4521-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4521-133">-WhatIf</span></span>
<span data-ttu-id="f4521-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4521-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4521-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4521-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4521-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4521-136">CommonParameters</span></span>
<span data-ttu-id="f4521-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4521-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4521-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4521-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4521-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f4521-139">INPUTS</span></span>

### <span data-ttu-id="f4521-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f4521-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="f4521-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f4521-141">System.String</span></span>

## <span data-ttu-id="f4521-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f4521-142">OUTPUTS</span></span>

### <span data-ttu-id="f4521-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f4521-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f4521-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f4521-144">NOTES</span></span>

## <span data-ttu-id="f4521-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f4521-145">RELATED LINKS</span></span>

[<span data-ttu-id="f4521-146">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f4521-146">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f4521-147">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f4521-147">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f4521-148">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f4521-148">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f4521-149">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f4521-149">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="f4521-150">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f4521-150">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)