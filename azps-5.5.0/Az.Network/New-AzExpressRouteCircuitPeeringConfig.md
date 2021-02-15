---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 6561faf00104bf0892747ac97c09b5d8fc2c6f2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159113"
---
# <span data-ttu-id="61c9d-101">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="61c9d-101">New-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="61c9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61c9d-102">SYNOPSIS</span></span>
<span data-ttu-id="61c9d-103">Erstellt eine neue Peeringkonfiguration, die einem "ExpressRoute"-Schaltkreis hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="61c9d-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="61c9d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61c9d-104">SYNTAX</span></span>

### <span data-ttu-id="61c9d-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="61c9d-105">SetByResource (Default)</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61c9d-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="61c9d-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61c9d-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="61c9d-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61c9d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61c9d-108">DESCRIPTION</span></span>
<span data-ttu-id="61c9d-109">Das **Cmdlet "New-AzExpressRouteCircuitPeeringConfig"** fügt einem "ExpressRoute"-Schaltkreis eine Peeringkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="61c9d-109">The **New-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="61c9d-110">ExpressRoute-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem anstelle des öffentlichen Internets ein Konnektivitätsanbieter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="61c9d-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="61c9d-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="61c9d-111">EXAMPLES</span></span>

### <span data-ttu-id="61c9d-112">Beispiel 1: Erstellen eines neuen "ExpressRoute"-Schaltkreises mit einer Peeringkonfiguration</span><span class="sxs-lookup"><span data-stu-id="61c9d-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
```powershell
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

## <span data-ttu-id="61c9d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61c9d-113">PARAMETERS</span></span>

### <span data-ttu-id="61c9d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61c9d-114">-DefaultProfile</span></span>
<span data-ttu-id="61c9d-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61c9d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61c9d-116">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="61c9d-116">-LegacyMode</span></span>
<span data-ttu-id="61c9d-117">Der legacy-Modus des Peerings</span><span class="sxs-lookup"><span data-stu-id="61c9d-117">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="61c9d-118">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="61c9d-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="61c9d-119">Für einen PeeringType von MicrosoftPeering müssen Sie eine Liste aller Präfixe bereitstellen, die Über die BGP-Sitzung angekündigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="61c9d-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="61c9d-120">Es werden nur Öffentliche IP-Adresspräfixe akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="61c9d-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="61c9d-121">Sie können eine durch Kommas getrennte Liste senden, wenn Sie eine Gruppe von Präfixen senden möchten.</span><span class="sxs-lookup"><span data-stu-id="61c9d-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="61c9d-122">Diese Präfixe müssen bei Ihnen unter einem Routingregistrierungsnamen (ROUTING Registry Name, RIR/IRR) registriert sein.</span><span class="sxs-lookup"><span data-stu-id="61c9d-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="61c9d-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="61c9d-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="61c9d-124">Wenn Sie Präfixe anzeigen, die nicht für die Peering -AS-Nummer registriert sind, können Sie die AS-Nummer angeben, mit der sie registriert sind.</span><span class="sxs-lookup"><span data-stu-id="61c9d-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="61c9d-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="61c9d-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="61c9d-126">Der Routingregistrierungsname (ROUTING Registry Name, RIR/IRR), für den die AS-Nummer und -Präfixe registriert sind.</span><span class="sxs-lookup"><span data-stu-id="61c9d-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="61c9d-127">-Name</span><span class="sxs-lookup"><span data-stu-id="61c9d-127">-Name</span></span>
<span data-ttu-id="61c9d-128">Der Name der zu erstellenden Peeringkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="61c9d-128">The name of the peering configuration to be created.</span></span>

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

### <span data-ttu-id="61c9d-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="61c9d-129">-PeerAddressType</span></span>
<span data-ttu-id="61c9d-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="61c9d-130">PeerAddressType</span></span>

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

### <span data-ttu-id="61c9d-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="61c9d-131">-PeerASN</span></span>
<span data-ttu-id="61c9d-132">Die AS-Nummer Ihres ExpressRoute-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="61c9d-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="61c9d-133">Dies muss ein öffentlicher ASN sein, wenn "PeeringType" "AzurePublicPeering" ist.</span><span class="sxs-lookup"><span data-stu-id="61c9d-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="61c9d-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="61c9d-134">-PeeringType</span></span>
<span data-ttu-id="61c9d-135">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` `AzurePublicPeering` , und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="61c9d-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="61c9d-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="61c9d-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="61c9d-137">Dies ist der IP-Adressbereich für den primären Routingpfad dieser Peeringbeziehung.</span><span class="sxs-lookup"><span data-stu-id="61c9d-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="61c9d-138">Dies muss ein /30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="61c9d-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="61c9d-139">Die erste Adresse mit ungerader Nummer in diesem Subnetz sollte Ihrer Routerschnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="61c9d-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="61c9d-140">Azure konfiguriert die nächste adresse mit gleichmäßiger Nummer für die Azure-Routerschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="61c9d-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="61c9d-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="61c9d-141">-RouteFilter</span></span>
<span data-ttu-id="61c9d-142">Dies ist ein vorhandenes RouteFilter-Objekt.</span><span class="sxs-lookup"><span data-stu-id="61c9d-142">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="61c9d-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="61c9d-143">-RouteFilterId</span></span>
<span data-ttu-id="61c9d-144">Dies ist die Ressourcen-ID eines vorhandenen RouteFilter-Objekts.</span><span class="sxs-lookup"><span data-stu-id="61c9d-144">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="61c9d-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="61c9d-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="61c9d-146">Dies ist der IP-Adressbereich für den sekundären Routingpfad dieser Peeringbeziehung.</span><span class="sxs-lookup"><span data-stu-id="61c9d-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="61c9d-147">Dies muss ein /30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="61c9d-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="61c9d-148">Die erste Adresse mit ungerader Nummer in diesem Subnetz sollte Ihrer Routerschnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="61c9d-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="61c9d-149">Azure konfiguriert die nächste adresse mit gleichmäßiger Nummer für die Azure-Routerschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="61c9d-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="61c9d-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="61c9d-150">-SharedKey</span></span>
<span data-ttu-id="61c9d-151">Dies ist ein optionaler MD5-Hash, der als vorab freigegebener Schlüssel für die Peeringkonfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="61c9d-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="61c9d-152">-YrnId</span><span class="sxs-lookup"><span data-stu-id="61c9d-152">-VlanId</span></span>
<span data-ttu-id="61c9d-153">Dies ist die ID-Nummer des FÜR DIESES Peering zugewiesenen ODEREINNs.</span><span class="sxs-lookup"><span data-stu-id="61c9d-153">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="61c9d-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61c9d-154">CommonParameters</span></span>
<span data-ttu-id="61c9d-155">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61c9d-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61c9d-156">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61c9d-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61c9d-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="61c9d-157">INPUTS</span></span>

### <span data-ttu-id="61c9d-158">System.String</span><span class="sxs-lookup"><span data-stu-id="61c9d-158">System.String</span></span>

### <span data-ttu-id="61c9d-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="61c9d-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="61c9d-160">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="61c9d-160">System.Boolean</span></span>

## <span data-ttu-id="61c9d-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="61c9d-161">OUTPUTS</span></span>

### <span data-ttu-id="61c9d-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="61c9d-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="61c9d-163">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="61c9d-163">NOTES</span></span>

## <span data-ttu-id="61c9d-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="61c9d-164">RELATED LINKS</span></span>

[<span data-ttu-id="61c9d-165">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="61c9d-165">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="61c9d-166">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="61c9d-166">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="61c9d-167">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="61c9d-167">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="61c9d-168">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="61c9d-168">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
