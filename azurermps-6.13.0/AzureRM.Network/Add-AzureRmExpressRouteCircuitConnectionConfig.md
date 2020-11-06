---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: aab4e78cd01e814ed8eb81b820e20bd3da4c03f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503573"
---
# <span data-ttu-id="39546-101">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="39546-101">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="39546-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="39546-102">SYNOPSIS</span></span>
<span data-ttu-id="39546-103">Fügt eine Schaltungs Verbindungskonfiguration zum privaten Peering eines Express-Route-Schaltkreises hinzu.</span><span class="sxs-lookup"><span data-stu-id="39546-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39546-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="39546-104">SYNTAX</span></span>

### <span data-ttu-id="39546-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="39546-105">SetByResource (Default)</span></span>
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39546-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="39546-106">SetByResourceId</span></span>
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39546-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39546-107">DESCRIPTION</span></span>
<span data-ttu-id="39546-108">Das Cmdlet " **Add-AzureRmExpressRouteCircuitConnectionConfig** " fügt eine Verbindungskonfiguration für private Peering für einen Express Route-Schaltkreis hinzu.</span><span class="sxs-lookup"><span data-stu-id="39546-108">The **Add-AzureRmExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="39546-109">So können Sie zwei Express-Route-Schaltkreise über Regionen oder Abonnements hinweg Peering. Beachten Sie, dass Sie nach dem Ausführen von **Add-AzureRmExpressRouteCircuitPeeringConfig** das Set-AzureRmExpressRouteCircuit-Cmdlet aufrufen müssen, um die Konfiguration zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="39546-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzureRmExpressRouteCircuitPeeringConfig** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="39546-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39546-110">EXAMPLES</span></span>

### <span data-ttu-id="39546-111">Beispiel 1: Hinzufügen einer Leitungs Verbindungsressource zu einem vorhandenen Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="39546-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="39546-112">Beispiel 2: Hinzufügen einer Leitungs Verbindungskonfiguration mithilfe von Rohrleitungen zu einem vorhandenen Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="39546-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="39546-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="39546-113">PARAMETERS</span></span>

### <span data-ttu-id="39546-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="39546-114">-AddressPrefix</span></span>
<span data-ttu-id="39546-115">Ein minimaler/29 Kunden Adressraum zum Erstellen von VxLan-Tunneln zwischen Express-Route-Schaltkreisen</span><span class="sxs-lookup"><span data-stu-id="39546-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

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

### <span data-ttu-id="39546-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="39546-116">-AuthorizationKey</span></span>
<span data-ttu-id="39546-117">Autorisierungsschlüssel für Peer-Express-Route-Schaltkreis in einem anderen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="39546-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="39546-118">Die Autorisierung auf einem Peer-Schaltkreis kann mithilfe vorhandener Befehle erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="39546-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="39546-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39546-119">-DefaultProfile</span></span>
<span data-ttu-id="39546-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="39546-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39546-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="39546-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="39546-122">Der Express Route-Schaltkreis wird geändert.</span><span class="sxs-lookup"><span data-stu-id="39546-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="39546-123">Hierbei handelt es sich um ein Azure-Objekt, das vom Cmdlet **Get-AzureRmExpressRouteCircuit** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="39546-123">This is Azure object returned by the **Get-AzureRmExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="39546-124">-Name</span><span class="sxs-lookup"><span data-stu-id="39546-124">-Name</span></span>
<span data-ttu-id="39546-125">Der Name der hinzuzufügenden Schaltkreis Verbindungsressource.</span><span class="sxs-lookup"><span data-stu-id="39546-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="39546-126">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="39546-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="39546-127">Ressourcen-ID für privates Peering des Remote-Schaltkreises, der mit dem aktuellen Schaltkreis Peering wird.</span><span class="sxs-lookup"><span data-stu-id="39546-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="39546-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="39546-128">-Confirm</span></span>
<span data-ttu-id="39546-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39546-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39546-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39546-130">-WhatIf</span></span>
<span data-ttu-id="39546-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39546-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39546-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39546-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39546-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39546-133">CommonParameters</span></span>
<span data-ttu-id="39546-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39546-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39546-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39546-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39546-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="39546-136">INPUTS</span></span>

### <span data-ttu-id="39546-137">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="39546-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="39546-138">Parameter: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="39546-138">Parameters: ExpressRouteCircuit (ByValue)</span></span>

### <span data-ttu-id="39546-139">System. String</span><span class="sxs-lookup"><span data-stu-id="39546-139">System.String</span></span>

## <span data-ttu-id="39546-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39546-140">OUTPUTS</span></span>

### <span data-ttu-id="39546-141">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="39546-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="39546-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="39546-142">NOTES</span></span>

## <span data-ttu-id="39546-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="39546-143">RELATED LINKS</span></span>

[<span data-ttu-id="39546-144">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="39546-144">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="39546-145">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="39546-145">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Get-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="39546-146">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="39546-146">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="39546-147">Satz-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="39546-147">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="39546-148">Neu – AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="39546-148">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="39546-149">Satz-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="39546-149">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="39546-150">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="39546-150">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)
