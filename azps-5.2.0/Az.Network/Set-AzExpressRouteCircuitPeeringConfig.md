---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: b41e7a0d6da67134cc1dd8842e0bd34c73128f58
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291454"
---
# <span data-ttu-id="720d3-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="720d3-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="720d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="720d3-102">SYNOPSIS</span></span>
<span data-ttu-id="720d3-103">Speichert eine geänderte ExpressRoute-Peeringkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="720d3-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="720d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="720d3-104">SYNTAX</span></span>

### <span data-ttu-id="720d3-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="720d3-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="720d3-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="720d3-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="720d3-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="720d3-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="720d3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="720d3-108">DESCRIPTION</span></span>
<span data-ttu-id="720d3-109">Mit **den Cmdlets "Set-AzExpressRouteCircuitPeeringConfig"** wird eine geänderte ExpressRoute-Peeringkonfiguration wieder in Azure gespeichert.</span><span class="sxs-lookup"><span data-stu-id="720d3-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="720d3-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="720d3-110">EXAMPLES</span></span>

### <span data-ttu-id="720d3-111">Beispiel 1: Ändern einer vorhandenen Peeringkonfiguration</span><span class="sxs-lookup"><span data-stu-id="720d3-111">Example 1: Change an existing peering configuration</span></span>
```powershell
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 201
}
Set-AzExpressRouteCircuitPeeringConfig @parameters
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

### <span data-ttu-id="720d3-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="720d3-112">Example 2</span></span>

<span data-ttu-id="720d3-113">Speichert eine geänderte ExpressRoute-Peeringkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="720d3-113">Saves a modified ExpressRoute peering configuration.</span></span> <span data-ttu-id="720d3-114">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="720d3-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzExpressRouteCircuitPeeringConfig -ExpressRouteCircuit <PSExpressRouteCircuit> -Name 'cert01' -PeerASN 100 -PeerAddressType IPv4 -PeeringType AzurePrivatePeering -PrimaryPeerAddressPrefix '123.0.0.0/30' -SecondaryPeerAddressPrefix '123.0.0.4/30' -VlanId 300
```

## <span data-ttu-id="720d3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="720d3-115">PARAMETERS</span></span>

### <span data-ttu-id="720d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="720d3-116">-DefaultProfile</span></span>
<span data-ttu-id="720d3-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="720d3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="720d3-118">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="720d3-118">-ExpressRouteCircuit</span></span>
<span data-ttu-id="720d3-119">Das ExpressRoute-Schaltkreisobjekt, das die zu ändernde Peeringkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="720d3-119">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="720d3-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="720d3-120">-LegacyMode</span></span>
<span data-ttu-id="720d3-121">Der legacy-Modus des Peerings</span><span class="sxs-lookup"><span data-stu-id="720d3-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="720d3-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="720d3-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="720d3-123">Für einen PeeringType von MicrosoftPeering müssen Sie eine Liste aller Präfixe bereitstellen, die Über die BGP-Sitzung angekündigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="720d3-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="720d3-124">Es werden nur Öffentliche IP-Adresspräfixe akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="720d3-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="720d3-125">Sie können eine durch Kommas getrennte Liste senden, wenn Sie eine Gruppe von Präfixen senden möchten.</span><span class="sxs-lookup"><span data-stu-id="720d3-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="720d3-126">Diese Präfixe müssen für Sie in einem RIR/IRR (Routing Registry Name) registriert werden.</span><span class="sxs-lookup"><span data-stu-id="720d3-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="720d3-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="720d3-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="720d3-128">Wenn Sie Präfixe anzeigen, die nicht für die Peering -AS-Nummer registriert sind, können Sie die AS-Nummer angeben, mit der sie registriert sind.</span><span class="sxs-lookup"><span data-stu-id="720d3-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="720d3-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="720d3-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="720d3-130">Der Routingregistrierungsname (ROUTING Registry Name, RIR/IRR), für den die AS-Nummer und die Präfixe registriert sind.</span><span class="sxs-lookup"><span data-stu-id="720d3-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="720d3-131">-Name</span><span class="sxs-lookup"><span data-stu-id="720d3-131">-Name</span></span>
<span data-ttu-id="720d3-132">Der Name der zu ändernden Peeringkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="720d3-132">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="720d3-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="720d3-133">-PeerAddressType</span></span>
<span data-ttu-id="720d3-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="720d3-134">PeerAddressType</span></span>

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

### <span data-ttu-id="720d3-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="720d3-135">-PeerASN</span></span>
<span data-ttu-id="720d3-136">Die AS-Nummer Ihres ExpressRoute-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="720d3-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="720d3-137">Dies muss ein öffentlicher ASN sein, wenn "PeeringType" "AzurePublicPeering" ist.</span><span class="sxs-lookup"><span data-stu-id="720d3-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="720d3-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="720d3-138">-PeeringType</span></span>
<span data-ttu-id="720d3-139">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` `AzurePublicPeering` , und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="720d3-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="720d3-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="720d3-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="720d3-141">Dies ist der IP-Adressbereich für den primären Routingpfad dieser Peeringbeziehung.</span><span class="sxs-lookup"><span data-stu-id="720d3-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="720d3-142">Dies muss ein /30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="720d3-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="720d3-143">Die erste Adresse mit ungerader Nummer in diesem Subnetz sollte Ihrer Routerschnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="720d3-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="720d3-144">Azure konfiguriert die nächste adresse mit gleichmäßiger Nummer für die Azure-Routerschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="720d3-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="720d3-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="720d3-145">-RouteFilter</span></span>
<span data-ttu-id="720d3-146">Dies ist ein vorhandenes RouteFilter-Objekt.</span><span class="sxs-lookup"><span data-stu-id="720d3-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="720d3-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="720d3-147">-RouteFilterId</span></span>
<span data-ttu-id="720d3-148">Dies ist die Ressourcen-ID eines vorhandenen RouteFilter-Objekts.</span><span class="sxs-lookup"><span data-stu-id="720d3-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="720d3-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="720d3-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="720d3-150">Dies ist der IP-Adressbereich für den sekundären Routingpfad dieser Peeringbeziehung.</span><span class="sxs-lookup"><span data-stu-id="720d3-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="720d3-151">Dies muss ein /30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="720d3-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="720d3-152">Die erste Adresse mit ungerader Nummer in diesem Subnetz sollte Ihrer Routerschnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="720d3-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="720d3-153">Azure konfiguriert die nächste adresse mit gleichmäßiger Nummer für die Azure-Routerschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="720d3-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="720d3-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="720d3-154">-SharedKey</span></span>
<span data-ttu-id="720d3-155">Dies ist ein optionaler MD5-Hash, der als vorab freigegebener Schlüssel für die Peeringkonfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="720d3-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="720d3-156">-YrnId</span><span class="sxs-lookup"><span data-stu-id="720d3-156">-VlanId</span></span>
<span data-ttu-id="720d3-157">Dies ist die ID-Nummer des FÜR DIESES Peering zugewiesenen ODEREINNs.</span><span class="sxs-lookup"><span data-stu-id="720d3-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="720d3-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="720d3-158">CommonParameters</span></span>
<span data-ttu-id="720d3-159">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="720d3-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="720d3-160">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="720d3-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="720d3-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="720d3-161">INPUTS</span></span>

### <span data-ttu-id="720d3-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="720d3-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="720d3-163">System.String</span><span class="sxs-lookup"><span data-stu-id="720d3-163">System.String</span></span>

### <span data-ttu-id="720d3-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="720d3-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="720d3-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="720d3-165">System.Boolean</span></span>

## <span data-ttu-id="720d3-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="720d3-166">OUTPUTS</span></span>

### <span data-ttu-id="720d3-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="720d3-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="720d3-168">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="720d3-168">NOTES</span></span>

## <span data-ttu-id="720d3-169">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="720d3-169">RELATED LINKS</span></span>

[<span data-ttu-id="720d3-170">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="720d3-170">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="720d3-171">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="720d3-171">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="720d3-172">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="720d3-172">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="720d3-173">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="720d3-173">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)
