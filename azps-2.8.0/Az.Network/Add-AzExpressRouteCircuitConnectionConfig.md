---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: a3b5b20eac34076dd6a5490a5d9cf1a5e2c49684
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822536"
---
# <span data-ttu-id="a6e30-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a6e30-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="a6e30-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a6e30-102">SYNOPSIS</span></span>
<span data-ttu-id="a6e30-103">Fügt eine Schaltungs Verbindungskonfiguration zum privaten Peering eines Express-Route-Schaltkreises hinzu.</span><span class="sxs-lookup"><span data-stu-id="a6e30-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="a6e30-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6e30-104">SYNTAX</span></span>

### <span data-ttu-id="a6e30-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="a6e30-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6e30-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a6e30-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6e30-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6e30-107">DESCRIPTION</span></span>
<span data-ttu-id="a6e30-108">Das Cmdlet " **Add-AzExpressRouteCircuitConnectionConfig** " fügt eine Verbindungskonfiguration für private Peering für einen Express Route-Schaltkreis hinzu.</span><span class="sxs-lookup"><span data-stu-id="a6e30-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="a6e30-109">So können Sie zwei Express-Route-Schaltkreise über Regionen oder Abonnements hinweg Peering. Beachten Sie, dass Sie nach dem Ausführen von **Add-AzExpressRouteCircuitPeeringConfig** das Set-AzExpressRouteCircuit-Cmdlet aufrufen müssen, um die Konfiguration zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6e30-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="a6e30-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6e30-110">EXAMPLES</span></span>

### <span data-ttu-id="a6e30-111">Beispiel 1: Hinzufügen einer Leitungs Verbindungsressource zu einem vorhandenen Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="a6e30-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="a6e30-112">Beispiel 2: Hinzufügen einer Leitungs Verbindungskonfiguration mithilfe von Rohrleitungen zu einem vorhandenen Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="a6e30-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="a6e30-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6e30-113">PARAMETERS</span></span>

### <span data-ttu-id="a6e30-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a6e30-114">-AddressPrefix</span></span>
<span data-ttu-id="a6e30-115">Ein minimaler/29 Kunden Adressraum zum Erstellen von VxLan-Tunneln zwischen Express-Route-Schaltkreisen</span><span class="sxs-lookup"><span data-stu-id="a6e30-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

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

### <span data-ttu-id="a6e30-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="a6e30-116">-AuthorizationKey</span></span>
<span data-ttu-id="a6e30-117">Autorisierungsschlüssel für Peer-Express-Route-Schaltkreis in einem anderen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a6e30-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="a6e30-118">Die Autorisierung auf einem Peer-Schaltkreis kann mithilfe vorhandener Befehle erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a6e30-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="a6e30-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6e30-119">-DefaultProfile</span></span>
<span data-ttu-id="a6e30-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a6e30-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6e30-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a6e30-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="a6e30-122">Der Express Route-Schaltkreis wird geändert.</span><span class="sxs-lookup"><span data-stu-id="a6e30-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="a6e30-123">Hierbei handelt es sich um ein Azure-Objekt, das vom Cmdlet **Get-AzExpressRouteCircuit** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a6e30-123">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="a6e30-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a6e30-124">-Name</span></span>
<span data-ttu-id="a6e30-125">Der Name der hinzuzufügenden Schaltkreis Verbindungsressource.</span><span class="sxs-lookup"><span data-stu-id="a6e30-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="a6e30-126">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="a6e30-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="a6e30-127">Ressourcen-ID für privates Peering des Remote-Schaltkreises, der mit dem aktuellen Schaltkreis Peering wird.</span><span class="sxs-lookup"><span data-stu-id="a6e30-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="a6e30-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a6e30-128">-Confirm</span></span>
<span data-ttu-id="a6e30-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a6e30-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6e30-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6e30-130">-WhatIf</span></span>
<span data-ttu-id="a6e30-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6e30-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6e30-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6e30-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6e30-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6e30-133">CommonParameters</span></span>
<span data-ttu-id="a6e30-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6e30-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6e30-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6e30-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6e30-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a6e30-136">INPUTS</span></span>

### <span data-ttu-id="a6e30-137">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a6e30-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="a6e30-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a6e30-138">System.String</span></span>

## <span data-ttu-id="a6e30-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a6e30-139">OUTPUTS</span></span>

### <span data-ttu-id="a6e30-140">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a6e30-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a6e30-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="a6e30-141">NOTES</span></span>

## <span data-ttu-id="a6e30-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a6e30-142">RELATED LINKS</span></span>

[<span data-ttu-id="a6e30-143">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a6e30-143">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a6e30-144">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a6e30-144">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="a6e30-145">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a6e30-145">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="a6e30-146">Satz-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a6e30-146">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="a6e30-147">Neu – AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a6e30-147">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="a6e30-148">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a6e30-148">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="a6e30-149">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a6e30-149">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)