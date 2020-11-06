---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: aef46264bc13b7136f9f999b2a97b3dd0951fbe8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496454"
---
# <span data-ttu-id="57f17-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="57f17-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="57f17-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="57f17-102">SYNOPSIS</span></span>
<span data-ttu-id="57f17-103">Fügt eine Peering-Konfiguration zu einem Express Route-Schaltkreis hinzu.</span><span class="sxs-lookup"><span data-stu-id="57f17-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57f17-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="57f17-104">SYNTAX</span></span>

### <span data-ttu-id="57f17-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="57f17-105">SetByResource (Default)</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57f17-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="57f17-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57f17-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="57f17-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57f17-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57f17-108">DESCRIPTION</span></span>
<span data-ttu-id="57f17-109">Mit dem Cmdlet **Add-AzureRmExpressRouteCircuitPeeringConfig** wird eine Peering-Konfiguration zu einem Express Route-Schaltkreis hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="57f17-109">The **Add-AzureRmExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="57f17-110">Express Route-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem Sie einen Verbindungsanbieter anstelle des öffentlichen Internets verwenden.</span><span class="sxs-lookup"><span data-stu-id="57f17-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="57f17-111">Beachten Sie, dass Sie nach dem Ausführen von **Add-AzureRmExpressRouteCircuitPeeringConfig** das Set-AzureRmExpressRouteCircuit-Cmdlet aufrufen müssen, um die Konfiguration zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="57f17-111">Note that, after running **Add-AzureRmExpressRouteCircuitPeeringConfig** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="57f17-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57f17-112">EXAMPLES</span></span>

### <span data-ttu-id="57f17-113">Beispiel 1: Hinzufügen eines Peers zu einem vorhandenen Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="57f17-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
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

## <span data-ttu-id="57f17-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="57f17-114">PARAMETERS</span></span>

### <span data-ttu-id="57f17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57f17-115">-DefaultProfile</span></span>
<span data-ttu-id="57f17-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="57f17-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f17-117">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="57f17-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="57f17-118">Der Express Route-Schaltkreis wird geändert.</span><span class="sxs-lookup"><span data-stu-id="57f17-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="57f17-119">Hierbei handelt es sich um ein Azure-Objekt, das vom Cmdlet **Get-AzureRmExpressRouteCircuit** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="57f17-119">This is Azure object returned by the **Get-AzureRmExpressRouteCircuit** cmdlet.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57f17-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="57f17-120">-LegacyMode</span></span>
<span data-ttu-id="57f17-121">Der Legacy Modus des Peering</span><span class="sxs-lookup"><span data-stu-id="57f17-121">The legacy mode of the Peering</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f17-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="57f17-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="57f17-123">Für eine PeeringType von MicrosoftPeering müssen Sie eine Liste aller Präfixe angeben, die Sie für die BGP-Sitzung ankündigen möchten.</span><span class="sxs-lookup"><span data-stu-id="57f17-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="57f17-124">Es werden nur die Präfixe öffentlicher IP-Adressen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="57f17-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="57f17-125">Sie können eine durch trennzeichengetrennte Liste senden, wenn Sie eine Reihe von Präfixen senden möchten.</span><span class="sxs-lookup"><span data-stu-id="57f17-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="57f17-126">Diese Präfixe müssen in einem Routing Registrierungsnamen (RIR/IRR) für Sie registriert sein.</span><span class="sxs-lookup"><span data-stu-id="57f17-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="57f17-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="57f17-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="57f17-128">Wenn Sie Präfixe anzeigen, die nicht für die Peering-Nummer registriert sind, können Sie die als Zahl angeben, in der Sie registriert sind.</span><span class="sxs-lookup"><span data-stu-id="57f17-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f17-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="57f17-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="57f17-130">Der Routing Registrierungs Name (RIR/IRR), in dem die AS-Nummer und die Präfixe registriert sind.</span><span class="sxs-lookup"><span data-stu-id="57f17-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f17-131">-Name</span><span class="sxs-lookup"><span data-stu-id="57f17-131">-Name</span></span>
<span data-ttu-id="57f17-132">Der Name der Peering-Beziehung, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="57f17-132">The name of the peering relationship to be added.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f17-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="57f17-133">-PeerAddressType</span></span>
<span data-ttu-id="57f17-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="57f17-134">PeerAddressType</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f17-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="57f17-135">-PeerASN</span></span>
<span data-ttu-id="57f17-136">Die AS-Nummer Ihres Express Route-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="57f17-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="57f17-137">Dies muss ein öffentlicher ASN sein, wenn PeeringType AzurePublicPeering ist.</span><span class="sxs-lookup"><span data-stu-id="57f17-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f17-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="57f17-138">-PeeringType</span></span>
<span data-ttu-id="57f17-139">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="57f17-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f17-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="57f17-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="57f17-141">Dies ist der IP-Adressbereich für den primären Routingpfad dieser Peering-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="57f17-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="57f17-142">Dies muss ein/30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="57f17-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="57f17-143">Die erste ungerade nummerierte Adresse in diesem Subnetz sollte Ihrer Router-Schnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="57f17-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="57f17-144">Azure konfiguriert die nächste gerade nummerierte Adresse für die Azure-Router-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="57f17-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f17-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="57f17-145">-RouteFilter</span></span>
<span data-ttu-id="57f17-146">Hierbei handelt es sich um ein vorhandenes RouteFilter-Objekt.</span><span class="sxs-lookup"><span data-stu-id="57f17-146">This is an existing RouteFilter object.</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: MicrosoftPeeringConfigRoutFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f17-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="57f17-147">-RouteFilterId</span></span>
<span data-ttu-id="57f17-148">Dies ist die Ressourcen-ID eines vorhandenen RouteFilter-Objekts.</span><span class="sxs-lookup"><span data-stu-id="57f17-148">This is the resource Id of an existing RouteFilter object.</span></span>

```yaml
Type: String
Parameter Sets: MicrosoftPeeringConfigRoutFilterId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f17-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="57f17-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="57f17-150">Hierbei handelt es sich um den IP-Adressbereich für den sekundären Routingpfad dieser Peering-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="57f17-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="57f17-151">Dies muss ein/30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="57f17-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="57f17-152">Die erste ungerade nummerierte Adresse in diesem Subnetz sollte Ihrer Router-Schnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="57f17-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="57f17-153">Azure konfiguriert die nächste gerade nummerierte Adresse für die Azure-Router-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="57f17-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f17-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="57f17-154">-SharedKey</span></span>
<span data-ttu-id="57f17-155">Hierbei handelt es sich um einen optionalen MD5-Hash, der als vorab freigegebener Schlüssel für die Peering-Konfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="57f17-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f17-156">-VLAN-Nr</span><span class="sxs-lookup"><span data-stu-id="57f17-156">-VlanId</span></span>
<span data-ttu-id="57f17-157">Dies ist die ID-Nummer des VLAN, das diesem Peering zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="57f17-157">This is the Id number of the VLAN assigned for this peering.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f17-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f17-158">CommonParameters</span></span>
<span data-ttu-id="57f17-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57f17-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f17-160">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57f17-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f17-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="57f17-161">INPUTS</span></span>

### <span data-ttu-id="57f17-162">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="57f17-162">PSExpressRouteCircuit</span></span>
<span data-ttu-id="57f17-163">Der Parameter "ExpressRouteCircuit" akzeptiert den Wert vom Typ "PSExpressRouteCircuit" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="57f17-163">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="57f17-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57f17-164">OUTPUTS</span></span>

### <span data-ttu-id="57f17-165">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="57f17-165">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="57f17-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="57f17-166">NOTES</span></span>

## <span data-ttu-id="57f17-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="57f17-167">RELATED LINKS</span></span>

[<span data-ttu-id="57f17-168">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="57f17-168">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="57f17-169">Neu – AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="57f17-169">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="57f17-170">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="57f17-170">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="57f17-171">Satz-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="57f17-171">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
