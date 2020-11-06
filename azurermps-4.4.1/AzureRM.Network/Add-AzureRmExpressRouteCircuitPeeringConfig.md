---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 5655fafa866fbc3702a1c6bf017caddd21df6fab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504873"
---
# <span data-ttu-id="d3f16-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="d3f16-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="d3f16-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d3f16-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f16-103">Fügt eine Peering-Konfiguration zu einem Express Route-Schaltkreis hinzu.</span><span class="sxs-lookup"><span data-stu-id="d3f16-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3f16-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3f16-104">SYNTAX</span></span>

### <span data-ttu-id="d3f16-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="d3f16-105">SetByResource (Default)</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3f16-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="d3f16-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3f16-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="d3f16-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3f16-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3f16-108">DESCRIPTION</span></span>
<span data-ttu-id="d3f16-109">Mit dem Cmdlet **Add-AzureRmExpressRouteCircuitPeeringConfig** wird eine Peering-Konfiguration zu einem Express Route-Schaltkreis hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d3f16-109">The **Add-AzureRmExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="d3f16-110">Express Route-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem Sie einen Verbindungsanbieter anstelle des öffentlichen Internets verwenden.</span><span class="sxs-lookup"><span data-stu-id="d3f16-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="d3f16-111">Beachten Sie, dass Sie nach dem Ausführen von **Add-AzureRmExpressRouteCircuitPeeringConfig** das Set-AzureRmExpressRouteCircuit-Cmdlet aufrufen müssen, um die Konfiguration zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d3f16-111">Note that, after running **Add-AzureRmExpressRouteCircuitPeeringConfig** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="d3f16-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3f16-112">EXAMPLES</span></span>

### <span data-ttu-id="d3f16-113">Beispiel 1: Hinzufügen eines Peers zu einem vorhandenen Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="d3f16-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzureRmExpressRouteCircuitPeeringConfig @parameters
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="d3f16-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3f16-114">PARAMETERS</span></span>

### <span data-ttu-id="d3f16-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d3f16-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="d3f16-116">Der Express Route-Schaltkreis wird geändert.</span><span class="sxs-lookup"><span data-stu-id="d3f16-116">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="d3f16-117">Hierbei handelt es sich um ein Azure-Objekt, das vom Cmdlet **Get-AzureRmExpressRouteCircuit** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d3f16-117">This is Azure object returned by the **Get-AzureRmExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="d3f16-118">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="d3f16-118">-LegacyMode</span></span>
<span data-ttu-id="d3f16-119">Der Legacy Modus des Peering</span><span class="sxs-lookup"><span data-stu-id="d3f16-119">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="d3f16-120">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="d3f16-120">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="d3f16-121">Für eine PeeringType von MicrosoftPeering müssen Sie eine Liste aller Präfixe angeben, die Sie für die BGP-Sitzung ankündigen möchten.</span><span class="sxs-lookup"><span data-stu-id="d3f16-121">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="d3f16-122">Es werden nur die Präfixe öffentlicher IP-Adressen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="d3f16-122">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="d3f16-123">Sie können eine durch trennzeichengetrennte Liste senden, wenn Sie eine Reihe von Präfixen senden möchten.</span><span class="sxs-lookup"><span data-stu-id="d3f16-123">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="d3f16-124">Diese Präfixe müssen in einem Routing Registrierungsnamen (RIR/IRR) für Sie registriert sein.</span><span class="sxs-lookup"><span data-stu-id="d3f16-124">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f16-125">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="d3f16-125">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="d3f16-126">Wenn Sie Präfixe anzeigen, die nicht für die Peering-Nummer registriert sind, können Sie die als Zahl angeben, in der Sie registriert sind.</span><span class="sxs-lookup"><span data-stu-id="d3f16-126">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="d3f16-127">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="d3f16-127">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="d3f16-128">Der Routing Registrierungs Name (RIR/IRR), in dem die AS-Nummer und die Präfixe registriert sind.</span><span class="sxs-lookup"><span data-stu-id="d3f16-128">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="d3f16-129">-Name</span><span class="sxs-lookup"><span data-stu-id="d3f16-129">-Name</span></span>
<span data-ttu-id="d3f16-130">Der Name der Peering-Beziehung, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3f16-130">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="d3f16-131">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="d3f16-131">-PeerAddressType</span></span>
<span data-ttu-id="d3f16-132">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="d3f16-132">PeerAddressType</span></span>

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

### <span data-ttu-id="d3f16-133">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="d3f16-133">-PeerASN</span></span>
<span data-ttu-id="d3f16-134">Die AS-Nummer Ihres Express Route-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="d3f16-134">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="d3f16-135">Dies muss ein öffentlicher ASN sein, wenn PeeringType AzurePublicPeering ist.</span><span class="sxs-lookup"><span data-stu-id="d3f16-135">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="d3f16-136">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="d3f16-136">-PeeringType</span></span>
<span data-ttu-id="d3f16-137">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="d3f16-137">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="d3f16-138">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d3f16-138">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="d3f16-139">Dies ist der IP-Adressbereich für den primären Routingpfad dieser Peering-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="d3f16-139">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="d3f16-140">Dies muss ein/30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="d3f16-140">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="d3f16-141">Die erste ungerade nummerierte Adresse in diesem Subnetz sollte Ihrer Router-Schnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="d3f16-141">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="d3f16-142">Azure konfiguriert die nächste gerade nummerierte Adresse für die Azure-Router-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d3f16-142">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="d3f16-143">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="d3f16-143">-RouteFilter</span></span>
<span data-ttu-id="d3f16-144">Hierbei handelt es sich um ein vorhandenes RouteFilter-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d3f16-144">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="d3f16-145">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="d3f16-145">-RouteFilterId</span></span>
<span data-ttu-id="d3f16-146">Dies ist die Ressourcen-ID eines vorhandenen RouteFilter-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d3f16-146">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="d3f16-147">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d3f16-147">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="d3f16-148">Hierbei handelt es sich um den IP-Adressbereich für den sekundären Routingpfad dieser Peering-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="d3f16-148">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="d3f16-149">Dies muss ein/30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="d3f16-149">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="d3f16-150">Die erste ungerade nummerierte Adresse in diesem Subnetz sollte Ihrer Router-Schnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="d3f16-150">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="d3f16-151">Azure konfiguriert die nächste gerade nummerierte Adresse für die Azure-Router-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d3f16-151">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="d3f16-152">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="d3f16-152">-SharedKey</span></span>
<span data-ttu-id="d3f16-153">Hierbei handelt es sich um einen optionalen MD5-Hash, der als vorab freigegebener Schlüssel für die Peering-Konfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3f16-153">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="d3f16-154">-VLAN-Nr</span><span class="sxs-lookup"><span data-stu-id="d3f16-154">-VlanId</span></span>
<span data-ttu-id="d3f16-155">Dies ist die ID-Nummer des VLAN, das diesem Peering zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d3f16-155">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="d3f16-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f16-156">-DefaultProfile</span></span>
<span data-ttu-id="d3f16-157">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d3f16-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3f16-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f16-158">CommonParameters</span></span>
<span data-ttu-id="d3f16-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3f16-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f16-160">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3f16-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f16-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d3f16-161">INPUTS</span></span>

### <span data-ttu-id="d3f16-162">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d3f16-162">PSExpressRouteCircuit</span></span>
<span data-ttu-id="d3f16-163">Der Parameter "ExpressRouteCircuit" akzeptiert den Wert vom Typ "PSExpressRouteCircuit" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d3f16-163">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="d3f16-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d3f16-164">OUTPUTS</span></span>

### <span data-ttu-id="d3f16-165">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d3f16-165">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="d3f16-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="d3f16-166">NOTES</span></span>

## <span data-ttu-id="d3f16-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d3f16-167">RELATED LINKS</span></span>

[<span data-ttu-id="d3f16-168">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d3f16-168">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d3f16-169">Neu – AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="d3f16-169">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="d3f16-170">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="d3f16-170">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="d3f16-171">Satz-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d3f16-171">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
