---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 4d329b0521e5b0f4974c25382be53ff32267e51c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303165"
---
# <span data-ttu-id="2cc58-101">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="2cc58-101">Add-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="2cc58-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2cc58-102">SYNOPSIS</span></span>
<span data-ttu-id="2cc58-103">Fügt eine Peering-Konfiguration zu einem Express Route-Schaltkreis hinzu.</span><span class="sxs-lookup"><span data-stu-id="2cc58-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="2cc58-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cc58-104">SYNTAX</span></span>

### <span data-ttu-id="2cc58-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="2cc58-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cc58-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="2cc58-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cc58-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="2cc58-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cc58-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2cc58-108">DESCRIPTION</span></span>
<span data-ttu-id="2cc58-109">Mit dem Cmdlet **Add-AzExpressRouteCircuitPeeringConfig** wird eine Peering-Konfiguration zu einem Express Route-Schaltkreis hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2cc58-109">The **Add-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="2cc58-110">Express Route-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem Sie einen Verbindungsanbieter anstelle des öffentlichen Internets verwenden.</span><span class="sxs-lookup"><span data-stu-id="2cc58-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="2cc58-111">Beachten Sie, dass Sie nach dem Ausführen von **Add-AzExpressRouteCircuitPeeringConfig** das Set-AzExpressRouteCircuit-Cmdlet aufrufen müssen, um die Konfiguration zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2cc58-111">Note that, after running **Add-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="2cc58-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2cc58-112">EXAMPLES</span></span>

### <span data-ttu-id="2cc58-113">Beispiel 1: Hinzufügen eines Peers zu einem vorhandenen Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="2cc58-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCircuitPeeringConfig @parameters
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="2cc58-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cc58-114">PARAMETERS</span></span>

### <span data-ttu-id="2cc58-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cc58-115">-DefaultProfile</span></span>
<span data-ttu-id="2cc58-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2cc58-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cc58-117">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2cc58-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="2cc58-118">Der Express Route-Schaltkreis wird geändert.</span><span class="sxs-lookup"><span data-stu-id="2cc58-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="2cc58-119">Hierbei handelt es sich um ein Azure-Objekt, das vom Cmdlet **Get-AzExpressRouteCircuit** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2cc58-119">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cc58-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="2cc58-120">-LegacyMode</span></span>
<span data-ttu-id="2cc58-121">Der Legacy Modus des Peering</span><span class="sxs-lookup"><span data-stu-id="2cc58-121">The legacy mode of the Peering</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cc58-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="2cc58-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="2cc58-123">Für eine PeeringType von MicrosoftPeering müssen Sie eine Liste aller Präfixe angeben, die Sie für die BGP-Sitzung ankündigen möchten.</span><span class="sxs-lookup"><span data-stu-id="2cc58-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="2cc58-124">Es werden nur die Präfixe öffentlicher IP-Adressen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="2cc58-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="2cc58-125">Sie können eine durch trennzeichengetrennte Liste senden, wenn Sie eine Reihe von Präfixen senden möchten.</span><span class="sxs-lookup"><span data-stu-id="2cc58-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="2cc58-126">Diese Präfixe müssen in einem Routing Registrierungsnamen (RIR/IRR) für Sie registriert sein.</span><span class="sxs-lookup"><span data-stu-id="2cc58-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc58-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="2cc58-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="2cc58-128">Wenn Sie Präfixe anzeigen, die nicht für die Peering-Nummer registriert sind, können Sie die als Zahl angeben, in der Sie registriert sind.</span><span class="sxs-lookup"><span data-stu-id="2cc58-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc58-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="2cc58-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="2cc58-130">Der Routing Registrierungs Name (RIR/IRR), in dem die AS-Nummer und die Präfixe registriert sind.</span><span class="sxs-lookup"><span data-stu-id="2cc58-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="2cc58-131">-Name</span><span class="sxs-lookup"><span data-stu-id="2cc58-131">-Name</span></span>
<span data-ttu-id="2cc58-132">Der Name der Peering-Beziehung, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2cc58-132">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="2cc58-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="2cc58-133">-PeerAddressType</span></span>
<span data-ttu-id="2cc58-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="2cc58-134">PeerAddressType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cc58-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="2cc58-135">-PeerASN</span></span>
<span data-ttu-id="2cc58-136">Die AS-Nummer Ihres Express Route-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="2cc58-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="2cc58-137">Dies muss ein öffentlicher ASN sein, wenn PeeringType AzurePublicPeering ist.</span><span class="sxs-lookup"><span data-stu-id="2cc58-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc58-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="2cc58-138">-PeeringType</span></span>
<span data-ttu-id="2cc58-139">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="2cc58-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc58-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2cc58-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="2cc58-141">Dies ist der IP-Adressbereich für den primären Routingpfad dieser Peering-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="2cc58-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="2cc58-142">Dies muss ein/30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="2cc58-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="2cc58-143">Die erste ungerade nummerierte Adresse in diesem Subnetz sollte Ihrer Router-Schnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="2cc58-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="2cc58-144">Azure konfiguriert die nächste gerade nummerierte Adresse für die Azure-Router-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2cc58-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="2cc58-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="2cc58-145">-RouteFilter</span></span>
<span data-ttu-id="2cc58-146">Hierbei handelt es sich um ein vorhandenes RouteFilter-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2cc58-146">This is an existing RouteFilter object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: MicrosoftPeeringConfigRoutFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cc58-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="2cc58-147">-RouteFilterId</span></span>
<span data-ttu-id="2cc58-148">Dies ist die Ressourcen-ID eines vorhandenen RouteFilter-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2cc58-148">This is the resource Id of an existing RouteFilter object.</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftPeeringConfigRoutFilterId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cc58-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2cc58-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="2cc58-150">Hierbei handelt es sich um den IP-Adressbereich für den sekundären Routingpfad dieser Peering-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="2cc58-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="2cc58-151">Dies muss ein/30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="2cc58-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="2cc58-152">Die erste ungerade nummerierte Adresse in diesem Subnetz sollte Ihrer Router-Schnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="2cc58-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="2cc58-153">Azure konfiguriert die nächste gerade nummerierte Adresse für die Azure-Router-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2cc58-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="2cc58-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="2cc58-154">-SharedKey</span></span>
<span data-ttu-id="2cc58-155">Hierbei handelt es sich um einen optionalen MD5-Hash, der als vorab freigegebener Schlüssel für die Peering-Konfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2cc58-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="2cc58-156">-VLAN-Nr</span><span class="sxs-lookup"><span data-stu-id="2cc58-156">-VlanId</span></span>
<span data-ttu-id="2cc58-157">Dies ist die ID-Nummer des VLAN, das diesem Peering zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="2cc58-157">This is the Id number of the VLAN assigned for this peering.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc58-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cc58-158">CommonParameters</span></span>
<span data-ttu-id="2cc58-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cc58-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cc58-160">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cc58-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cc58-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2cc58-161">INPUTS</span></span>

### <span data-ttu-id="2cc58-162">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2cc58-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="2cc58-163">System. String</span><span class="sxs-lookup"><span data-stu-id="2cc58-163">System.String</span></span>

### <span data-ttu-id="2cc58-164">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2cc58-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="2cc58-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2cc58-165">System.Boolean</span></span>

## <span data-ttu-id="2cc58-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2cc58-166">OUTPUTS</span></span>

### <span data-ttu-id="2cc58-167">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2cc58-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="2cc58-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="2cc58-168">NOTES</span></span>

## <span data-ttu-id="2cc58-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2cc58-169">RELATED LINKS</span></span>

[<span data-ttu-id="2cc58-170">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2cc58-170">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="2cc58-171">Neu – AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="2cc58-171">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="2cc58-172">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="2cc58-172">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="2cc58-173">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2cc58-173">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
