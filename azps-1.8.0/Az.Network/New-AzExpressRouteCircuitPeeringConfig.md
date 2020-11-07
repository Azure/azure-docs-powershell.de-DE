---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: a1bb490d81d2c4df92299c18eeb0e1a05a6760f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660560"
---
# <span data-ttu-id="addc9-101">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="addc9-101">New-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="addc9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="addc9-102">SYNOPSIS</span></span>
<span data-ttu-id="addc9-103">Erstellt eine neue Peering-Konfiguration, die einem Express Route-Schaltkreis hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="addc9-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="addc9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="addc9-104">SYNTAX</span></span>

### <span data-ttu-id="addc9-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="addc9-105">SetByResource (Default)</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="addc9-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="addc9-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="addc9-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="addc9-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="addc9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="addc9-108">DESCRIPTION</span></span>
<span data-ttu-id="addc9-109">Mit dem Cmdlet **New-AzExpressRouteCircuitPeeringConfig** wird eine Peering-Konfiguration zu einem Express Route-Schaltkreis hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="addc9-109">The **New-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="addc9-110">Express Route-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem Sie einen Verbindungsanbieter anstelle des öffentlichen Internets verwenden.</span><span class="sxs-lookup"><span data-stu-id="addc9-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="addc9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="addc9-111">EXAMPLES</span></span>

### <span data-ttu-id="addc9-112">Beispiel 1: Erstellen eines neuen Express Route-Schaltkreises mit einer Peering-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="addc9-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
```
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
$PeerConfig = New-AzExpressRouteCircuitPeeringConfig @parameters

$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ServiceProviderName='Equinix'
    Peering=$PeerConfig
    PeeringLocation='Silicon Valley'
    BandwidthInMbps=200
}
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="addc9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="addc9-113">PARAMETERS</span></span>

### <span data-ttu-id="addc9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="addc9-114">-DefaultProfile</span></span>
<span data-ttu-id="addc9-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="addc9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="addc9-116">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="addc9-116">-LegacyMode</span></span>
<span data-ttu-id="addc9-117">Der Legacy Modus des Peering</span><span class="sxs-lookup"><span data-stu-id="addc9-117">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="addc9-118">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="addc9-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="addc9-119">Für eine PeeringType von MicrosoftPeering müssen Sie eine Liste aller Präfixe angeben, die Sie für die BGP-Sitzung ankündigen möchten.</span><span class="sxs-lookup"><span data-stu-id="addc9-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="addc9-120">Es werden nur die Präfixe öffentlicher IP-Adressen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="addc9-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="addc9-121">Sie können eine durch trennzeichengetrennte Liste senden, wenn Sie eine Reihe von Präfixen senden möchten.</span><span class="sxs-lookup"><span data-stu-id="addc9-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="addc9-122">Diese Präfixe müssen in einem Routing Registrierungsnamen (RIR/IRR) für Sie registriert sein.</span><span class="sxs-lookup"><span data-stu-id="addc9-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="addc9-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="addc9-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="addc9-124">Wenn Sie Präfixe anzeigen, die nicht für die Peering-Nummer registriert sind, können Sie die als Zahl angeben, in der Sie registriert sind.</span><span class="sxs-lookup"><span data-stu-id="addc9-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="addc9-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="addc9-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="addc9-126">Der Routing Registrierungs Name (RIR/IRR), in dem die AS-Nummer und die Präfixe registriert sind.</span><span class="sxs-lookup"><span data-stu-id="addc9-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="addc9-127">-Name</span><span class="sxs-lookup"><span data-stu-id="addc9-127">-Name</span></span>
<span data-ttu-id="addc9-128">Der Name der zu erstellende Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="addc9-128">The name of the peering configuration to be created.</span></span>

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

### <span data-ttu-id="addc9-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="addc9-129">-PeerAddressType</span></span>
<span data-ttu-id="addc9-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="addc9-130">PeerAddressType</span></span>

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

### <span data-ttu-id="addc9-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="addc9-131">-PeerASN</span></span>
<span data-ttu-id="addc9-132">Die AS-Nummer Ihres Express Route-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="addc9-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="addc9-133">Dies muss ein öffentlicher ASN sein, wenn PeeringType AzurePublicPeering ist.</span><span class="sxs-lookup"><span data-stu-id="addc9-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="addc9-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="addc9-134">-PeeringType</span></span>
<span data-ttu-id="addc9-135">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="addc9-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="addc9-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="addc9-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="addc9-137">Dies ist der IP-Adressbereich für den primären Routingpfad dieser Peering-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="addc9-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="addc9-138">Dies muss ein/30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="addc9-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="addc9-139">Die erste ungerade nummerierte Adresse in diesem Subnetz sollte Ihrer Router-Schnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="addc9-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="addc9-140">Azure konfiguriert die nächste gerade nummerierte Adresse für die Azure-Router-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="addc9-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="addc9-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="addc9-141">-RouteFilter</span></span>
<span data-ttu-id="addc9-142">Hierbei handelt es sich um ein vorhandenes RouteFilter-Objekt.</span><span class="sxs-lookup"><span data-stu-id="addc9-142">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="addc9-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="addc9-143">-RouteFilterId</span></span>
<span data-ttu-id="addc9-144">Dies ist die Ressourcen-ID eines vorhandenen RouteFilter-Objekts.</span><span class="sxs-lookup"><span data-stu-id="addc9-144">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="addc9-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="addc9-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="addc9-146">Hierbei handelt es sich um den IP-Adressbereich für den sekundären Routingpfad dieser Peering-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="addc9-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="addc9-147">Dies muss ein/30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="addc9-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="addc9-148">Die erste ungerade nummerierte Adresse in diesem Subnetz sollte Ihrer Router-Schnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="addc9-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="addc9-149">Azure konfiguriert die nächste gerade nummerierte Adresse für die Azure-Router-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="addc9-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="addc9-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="addc9-150">-SharedKey</span></span>
<span data-ttu-id="addc9-151">Hierbei handelt es sich um einen optionalen MD5-Hash, der als vorab freigegebener Schlüssel für die Peering-Konfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="addc9-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="addc9-152">-VLAN-Nr</span><span class="sxs-lookup"><span data-stu-id="addc9-152">-VlanId</span></span>
<span data-ttu-id="addc9-153">Dies ist die ID-Nummer des VLAN, das diesem Peering zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="addc9-153">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="addc9-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="addc9-154">CommonParameters</span></span>
<span data-ttu-id="addc9-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="addc9-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="addc9-156">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="addc9-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="addc9-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="addc9-157">INPUTS</span></span>

### <span data-ttu-id="addc9-158">System. String</span><span class="sxs-lookup"><span data-stu-id="addc9-158">System.String</span></span>

### <span data-ttu-id="addc9-159">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="addc9-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="addc9-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="addc9-160">System.Boolean</span></span>

## <span data-ttu-id="addc9-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="addc9-161">OUTPUTS</span></span>

### <span data-ttu-id="addc9-162">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="addc9-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="addc9-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="addc9-163">NOTES</span></span>

## <span data-ttu-id="addc9-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="addc9-164">RELATED LINKS</span></span>

[<span data-ttu-id="addc9-165">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="addc9-165">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="addc9-166">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="addc9-166">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="addc9-167">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="addc9-167">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="addc9-168">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="addc9-168">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
