---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 4c1205599f048e33534f0ce0aa844da7b428b076
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948579"
---
# <span data-ttu-id="c3d05-101">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c3d05-101">Add-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="c3d05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3d05-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d05-103">Fügt einer ExpressRoute-Schaltung eine Peeringkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="c3d05-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="c3d05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3d05-104">SYNTAX</span></span>

### <span data-ttu-id="c3d05-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3d05-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3d05-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="c3d05-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3d05-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="c3d05-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3d05-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c3d05-108">DESCRIPTION</span></span>
<span data-ttu-id="c3d05-109">Das **Add-AzExpressRouteCircuitPeeringConfig-Cmdlet** fügt einem ExpressRoute-Schaltkreis eine Peeringkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="c3d05-109">The **Add-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="c3d05-110">ExpressRoute-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem sie einen Konnektivitätsanbieter anstelle des öffentlichen Internets verwenden.</span><span class="sxs-lookup"><span data-stu-id="c3d05-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="c3d05-111">Beachten Sie, dass Sie nach dem Ausführen von **Add-AzExpressRouteCircuitPeeringConfig** das cmdlet Set-AzExpressRouteCircuit aufrufen müssen, um die Konfiguration zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c3d05-111">Note that, after running **Add-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="c3d05-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c3d05-112">EXAMPLES</span></span>

### <span data-ttu-id="c3d05-113">Beispiel 1: Hinzufügen eines Peers zu einem vorhandenen ExpressRoute-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="c3d05-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
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

## <span data-ttu-id="c3d05-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c3d05-114">PARAMETERS</span></span>

### <span data-ttu-id="c3d05-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d05-115">-DefaultProfile</span></span>
<span data-ttu-id="c3d05-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3d05-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3d05-117">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c3d05-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="c3d05-118">Der geänderte ExpressRoute-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="c3d05-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="c3d05-119">Dies ist das vom **Get-AzExpressRouteCircuit-Cmdlet** zurückgegebene Azure-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c3d05-119">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="c3d05-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="c3d05-120">-LegacyMode</span></span>
<span data-ttu-id="c3d05-121">Der ältere Modus des Peerings</span><span class="sxs-lookup"><span data-stu-id="c3d05-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="c3d05-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="c3d05-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="c3d05-123">Für einen PeeringType von MicrosoftPeering müssen Sie eine Liste aller Präfixe bereitstellen, die Sie über die BGP-Sitzung bewerben möchten.</span><span class="sxs-lookup"><span data-stu-id="c3d05-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="c3d05-124">Es werden nur präfixe für öffentliche IP-Adressen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="c3d05-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="c3d05-125">Sie können eine durch Kommas getrennte Liste senden, wenn Sie eine Reihe von Präfixen senden möchten.</span><span class="sxs-lookup"><span data-stu-id="c3d05-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="c3d05-126">Diese Präfixe müssen für Sie in einem Routingregistrierungsnamen (ROUTING Registry Name, RIR/IRR) registriert sein.</span><span class="sxs-lookup"><span data-stu-id="c3d05-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="c3d05-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="c3d05-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="c3d05-128">Wenn Sie Präfixe anzeigen, die nicht für die Peering-AS-Nummer registriert sind, können Sie die AS-Nummer angeben, für die sie registriert sind.</span><span class="sxs-lookup"><span data-stu-id="c3d05-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="c3d05-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="c3d05-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="c3d05-130">Der Routingregistrierungsname (RIR/IRR), für den die AS-Nummer und -Präfixe registriert sind.</span><span class="sxs-lookup"><span data-stu-id="c3d05-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="c3d05-131">-Name</span><span class="sxs-lookup"><span data-stu-id="c3d05-131">-Name</span></span>
<span data-ttu-id="c3d05-132">Der Name der peering-Beziehung, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3d05-132">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="c3d05-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="c3d05-133">-PeerAddressType</span></span>
<span data-ttu-id="c3d05-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="c3d05-134">PeerAddressType</span></span>

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

### <span data-ttu-id="c3d05-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="c3d05-135">-PeerASN</span></span>
<span data-ttu-id="c3d05-136">Die AS-Nummer Ihres ExpressRoute-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="c3d05-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="c3d05-137">Dies muss ein öffentlicher ASN sein, wenn der PeeringType AzurePublicPeering ist.</span><span class="sxs-lookup"><span data-stu-id="c3d05-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="c3d05-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="c3d05-138">-PeeringType</span></span>
<span data-ttu-id="c3d05-139">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` `AzurePublicPeering` , und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="c3d05-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="c3d05-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c3d05-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="c3d05-141">Dies ist der IP-Adressbereich für den primären Routingpfad dieser Peeringbeziehung.</span><span class="sxs-lookup"><span data-stu-id="c3d05-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="c3d05-142">Dies muss ein /30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="c3d05-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="c3d05-143">Die erste ungerade Nummerierte Adresse in diesem Subnetz sollte Ihrer Routerschnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="c3d05-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="c3d05-144">Azure konfiguriert die nächste gleichmäßig nummerierte Adresse für die Azure-Routerschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c3d05-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="c3d05-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c3d05-145">-RouteFilter</span></span>
<span data-ttu-id="c3d05-146">Dies ist ein vorhandenes RouteFilter-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c3d05-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="c3d05-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="c3d05-147">-RouteFilterId</span></span>
<span data-ttu-id="c3d05-148">Dies ist die Ressourcen-ID eines vorhandenen RouteFilter-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c3d05-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="c3d05-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c3d05-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="c3d05-150">Dies ist der IP-Adressbereich für den sekundären Routingpfad dieser Peeringbeziehung.</span><span class="sxs-lookup"><span data-stu-id="c3d05-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="c3d05-151">Dies muss ein /30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="c3d05-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="c3d05-152">Die erste ungerade Nummerierte Adresse in diesem Subnetz sollte Ihrer Routerschnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="c3d05-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="c3d05-153">Azure konfiguriert die nächste gleichmäßig nummerierte Adresse für die Azure-Routerschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c3d05-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="c3d05-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="c3d05-154">-SharedKey</span></span>
<span data-ttu-id="c3d05-155">Dies ist ein optionaler MD5-Hash, der als vorab freigegebener Schlüssel für die Peeringkonfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3d05-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="c3d05-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="c3d05-156">-VlanId</span></span>
<span data-ttu-id="c3d05-157">Dies ist die ID-Nummer des für dieses Peering zugewiesenen VLANs.</span><span class="sxs-lookup"><span data-stu-id="c3d05-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="c3d05-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d05-158">CommonParameters</span></span>
<span data-ttu-id="c3d05-159">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3d05-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d05-160">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3d05-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d05-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c3d05-161">INPUTS</span></span>

### <span data-ttu-id="c3d05-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c3d05-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="c3d05-163">System.String</span><span class="sxs-lookup"><span data-stu-id="c3d05-163">System.String</span></span>

### <span data-ttu-id="c3d05-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c3d05-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="c3d05-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c3d05-165">System.Boolean</span></span>

## <span data-ttu-id="c3d05-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c3d05-166">OUTPUTS</span></span>

### <span data-ttu-id="c3d05-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c3d05-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="c3d05-168">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c3d05-168">NOTES</span></span>

## <span data-ttu-id="c3d05-169">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c3d05-169">RELATED LINKS</span></span>

[<span data-ttu-id="c3d05-170">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c3d05-170">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="c3d05-171">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c3d05-171">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="c3d05-172">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c3d05-172">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="c3d05-173">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c3d05-173">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
