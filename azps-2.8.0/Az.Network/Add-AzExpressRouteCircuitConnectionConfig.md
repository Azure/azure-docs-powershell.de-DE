---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: bc08305d7aa604dd9c7540573ffb5a199e85b287
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409765"
---
# <span data-ttu-id="5e9c6-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5e9c6-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="5e9c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e9c6-102">SYNOPSIS</span></span>
<span data-ttu-id="5e9c6-103">Fügt dem privaten Peering eines Expressroutenkreises eine Verbindungskonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="5e9c6-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="5e9c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e9c6-104">SYNTAX</span></span>

### <span data-ttu-id="5e9c6-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e9c6-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e9c6-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5e9c6-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e9c6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e9c6-107">DESCRIPTION</span></span>
<span data-ttu-id="5e9c6-108">Das **Cmdlet "Add-AzExpressRouteCircuitConnectionConfig"** fügt dem privaten Peering für einen "ExpressRoute"-Schaltkreis eine Verbindungskonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="5e9c6-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="5e9c6-109">Dies ermöglicht das Peering von zwei Expressrouten über Regionen oder Abonnements hinweg. Beachten Sie, dass Sie nach der Ausführung von **"Add-AzExpressRouteCircuitPeeringConfig"** das cmdlet Set-AzExpressRouteCircuit aufrufen müssen, um die Konfiguration zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5e9c6-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="5e9c6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5e9c6-110">EXAMPLES</span></span>

### <span data-ttu-id="5e9c6-111">Beispiel 1: Hinzufügen einer Schaltkreisverbindungsressource zu einem vorhandenen</span><span class="sxs-lookup"><span data-stu-id="5e9c6-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="5e9c6-112">Beispiel 2: Hinzufügen einer Verbindungskonfiguration mit einer Leitung zu einem vorhandenen "ExpressRoute-Schaltkreis"</span><span class="sxs-lookup"><span data-stu-id="5e9c6-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="5e9c6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e9c6-113">PARAMETERS</span></span>

### <span data-ttu-id="5e9c6-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5e9c6-114">-AddressPrefix</span></span>
<span data-ttu-id="5e9c6-115">Mindestens /29 Kundenad address space to create VxLan tunnels between Express Route Circuits</span><span class="sxs-lookup"><span data-stu-id="5e9c6-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

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

### <span data-ttu-id="5e9c6-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="5e9c6-116">-AuthorizationKey</span></span>
<span data-ttu-id="5e9c6-117">Autorisierungsschlüssel für peer Express Route Circuit in einem anderen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e9c6-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="5e9c6-118">Autorisierung für Peerkreise kann mit vorhandenen Befehlen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5e9c6-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="5e9c6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e9c6-119">-DefaultProfile</span></span>
<span data-ttu-id="5e9c6-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e9c6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e9c6-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e9c6-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="5e9c6-122">Der zu ändernde ExpressRoute-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="5e9c6-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="5e9c6-123">Dies ist das Azure-Objekt, das vom **Cmdlet "Get-AzExpressRouteCircuit"** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5e9c6-123">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="5e9c6-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5e9c6-124">-Name</span></span>
<span data-ttu-id="5e9c6-125">Der Name der Verbindungsressource, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e9c6-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="5e9c6-126">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="5e9c6-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="5e9c6-127">Ressourcen-ID für privates Peering eines Remotekreises, das mit dem aktuellen Schaltkreis peered wird.</span><span class="sxs-lookup"><span data-stu-id="5e9c6-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="5e9c6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e9c6-128">-Confirm</span></span>
<span data-ttu-id="5e9c6-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e9c6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e9c6-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5e9c6-130">-WhatIf</span></span>
<span data-ttu-id="5e9c6-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e9c6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e9c6-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e9c6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e9c6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e9c6-133">CommonParameters</span></span>
<span data-ttu-id="5e9c6-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e9c6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e9c6-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e9c6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e9c6-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5e9c6-136">INPUTS</span></span>

### <span data-ttu-id="5e9c6-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e9c6-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="5e9c6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5e9c6-138">System.String</span></span>

## <span data-ttu-id="5e9c6-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5e9c6-139">OUTPUTS</span></span>

### <span data-ttu-id="5e9c6-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e9c6-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="5e9c6-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5e9c6-141">NOTES</span></span>

## <span data-ttu-id="5e9c6-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5e9c6-142">RELATED LINKS</span></span>

[<span data-ttu-id="5e9c6-143">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e9c6-143">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="5e9c6-144">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5e9c6-144">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="5e9c6-145">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5e9c6-145">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)





[<span data-ttu-id="5e9c6-146">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e9c6-146">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="5e9c6-147">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e9c6-147">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
