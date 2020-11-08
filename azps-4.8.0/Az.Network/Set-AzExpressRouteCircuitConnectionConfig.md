---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8b4a8c9f-874c-4a27-b87e-c8ad7e73188d
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 432af4d97f2ddf085d23db33cc0f2604c1fc7aa5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165128"
---
# <span data-ttu-id="325c7-101">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="325c7-101">Set-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="325c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="325c7-102">SYNOPSIS</span></span>
<span data-ttu-id="325c7-103">Aktualisiert eine Schaltungs Verbindungskonfiguration, die in privaten Peerings für einen Express-Routen Schaltkreis erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="325c7-103">Updates a circuit connection configuration created in Private Peerings for an Express Route Circuit.</span></span> 

## <span data-ttu-id="325c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="325c7-104">SYNTAX</span></span>

### <span data-ttu-id="325c7-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="325c7-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="325c7-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="325c7-106">SetByResourceId</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="325c7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="325c7-107">DESCRIPTION</span></span>
<span data-ttu-id="325c7-108">Das Cmdlet " **Satz-AzExpressRouteCircuitConnectionConfig** " aktualisiert eine in private Peering erstellte Schaltkreis Verbindungskonfiguration für einen Express Route-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="325c7-108">The **Set-AzExpressRouteCircuitConnectionConfig** cmdlet updates a circuit connection configuration created in private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="325c7-109">So können Sie zwei Express-Route-Schaltkreise über Regionen oder Abonnements hinweg Peering.</span><span class="sxs-lookup"><span data-stu-id="325c7-109">This allows peering two Express Route Circuits across regions or subscriptions.</span></span>
<span data-ttu-id="325c7-110">Beachten Sie, dass Sie vor dem Ausführen von **AzExpressRouteCircuitConnectionConfig** die Schaltkreis Verbindung mithilfe von **Add-AzExpressRouteCircuitConnectionConfig** hinzufügen müssen.</span><span class="sxs-lookup"><span data-stu-id="325c7-110">Note that, before running **Set-AzExpressRouteCircuitConnectionConfig** you must add the circuit connection using **Add-AzExpressRouteCircuitConnectionConfig**.</span></span> <span data-ttu-id="325c7-111">Nachdem Sie " **AzExpressRouteCircuitPeeringConfig** " ausgeführt haben, müssen Sie auch das Set-AzExpressRouteCircuit-Cmdlet aufrufen, um die Konfiguration zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="325c7-111">Also, after running **Set-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>


## <span data-ttu-id="325c7-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="325c7-112">EXAMPLES</span></span>

### <span data-ttu-id="325c7-113">Beispiel 1: Aktualisieren einer Leitungs Verbindungsressource auf einen vorhandenen Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="325c7-113">Example 1: Update a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = 'aa:bb::0/125'
$addressPrefixType = 'IPv6'
Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="325c7-114">Beispiel 2: Einrichten einer Leitungs Verbindungskonfiguration mithilfe von Piping an einen vorhandenen Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="325c7-114">Example 2: Set a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="325c7-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="325c7-115">PARAMETERS</span></span>

### <span data-ttu-id="325c7-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="325c7-116">-AddressPrefix</span></span>
<span data-ttu-id="325c7-117">Ein minimaler/29 Kunden Adressraum zum Erstellen von VxLan-Tunneln zwischen Express-Route-Schaltkreisen für IPv4-Tunnels.</span><span class="sxs-lookup"><span data-stu-id="325c7-117">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="325c7-118">oder mindestens 125 Kunden Adressraum zum Erstellen von VxLan-Tunneln zwischen Express-Route-Schaltkreisen für IPv6-Tunnels.</span><span class="sxs-lookup"><span data-stu-id="325c7-118">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="325c7-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="325c7-119">-AddressPrefixType</span></span>
<span data-ttu-id="325c7-120">Gibt die Adressfamilie an, zu der das Adresspräfix gehört.</span><span class="sxs-lookup"><span data-stu-id="325c7-120">Specifies the address family that address prefix belongs to.</span></span>

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

### <span data-ttu-id="325c7-121">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="325c7-121">-AuthorizationKey</span></span>
<span data-ttu-id="325c7-122">Autorisierungsschlüssel für Peer-Express-Route-Schaltkreis in einem anderen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="325c7-122">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="325c7-123">Die Autorisierung auf einem Peer-Schaltkreis kann mithilfe vorhandener Befehle erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="325c7-123">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="325c7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="325c7-124">-DefaultProfile</span></span>
<span data-ttu-id="325c7-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="325c7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="325c7-126">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="325c7-126">-ExpressRouteCircuit</span></span>
<span data-ttu-id="325c7-127">Der Express Route-Schaltkreis wird geändert.</span><span class="sxs-lookup"><span data-stu-id="325c7-127">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="325c7-128">Hierbei handelt es sich um ein Azure-Objekt, das vom Cmdlet **Get-AzExpressRouteCircuit** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="325c7-128">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="325c7-129">-Name</span><span class="sxs-lookup"><span data-stu-id="325c7-129">-Name</span></span>
<span data-ttu-id="325c7-130">Der Name der hinzuzufügenden Schaltkreis Verbindungsressource.</span><span class="sxs-lookup"><span data-stu-id="325c7-130">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="325c7-131">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="325c7-131">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="325c7-132">Ressourcen-ID für privates Peering des Remote-Schaltkreises, der mit dem aktuellen Schaltkreis Peering wird.</span><span class="sxs-lookup"><span data-stu-id="325c7-132">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="325c7-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="325c7-133">-Confirm</span></span>
<span data-ttu-id="325c7-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="325c7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="325c7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="325c7-135">-WhatIf</span></span>
<span data-ttu-id="325c7-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="325c7-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="325c7-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="325c7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="325c7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="325c7-138">CommonParameters</span></span>
<span data-ttu-id="325c7-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="325c7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="325c7-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="325c7-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="325c7-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="325c7-141">INPUTS</span></span>

### <span data-ttu-id="325c7-142">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="325c7-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="325c7-143">System. String</span><span class="sxs-lookup"><span data-stu-id="325c7-143">System.String</span></span>

## <span data-ttu-id="325c7-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="325c7-144">OUTPUTS</span></span>

### <span data-ttu-id="325c7-145">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="325c7-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="325c7-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="325c7-146">NOTES</span></span>

## <span data-ttu-id="325c7-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="325c7-147">RELATED LINKS</span></span>

[<span data-ttu-id="325c7-148">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="325c7-148">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="325c7-149">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="325c7-149">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="325c7-150">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="325c7-150">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="325c7-151">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="325c7-151">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="325c7-152">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="325c7-152">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
