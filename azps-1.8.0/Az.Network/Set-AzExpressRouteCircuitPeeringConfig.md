---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: ecbd0d101db979d5982891bbfbd4ad1e3083ee8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660229"
---
# <span data-ttu-id="b2a77-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b2a77-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="b2a77-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2a77-102">SYNOPSIS</span></span>
<span data-ttu-id="b2a77-103">Speichert eine geänderte Express Route-Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b2a77-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="b2a77-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2a77-104">SYNTAX</span></span>

### <span data-ttu-id="b2a77-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="b2a77-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2a77-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="b2a77-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2a77-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="b2a77-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2a77-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2a77-108">DESCRIPTION</span></span>
<span data-ttu-id="b2a77-109">Die Cmdlets für "AzExpressRouteCircuitPeeringConfig" speichern eine geänderte Express Route **-** Peering-Konfiguration wieder in Azure.</span><span class="sxs-lookup"><span data-stu-id="b2a77-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="b2a77-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2a77-110">EXAMPLES</span></span>

### <span data-ttu-id="b2a77-111">Beispiel 1: Ändern einer vorhandenen Peering-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="b2a77-111">Example 1: Change an existing peering configuration</span></span>
```
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

## <span data-ttu-id="b2a77-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2a77-112">PARAMETERS</span></span>

### <span data-ttu-id="b2a77-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2a77-113">-DefaultProfile</span></span>
<span data-ttu-id="b2a77-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b2a77-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2a77-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b2a77-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="b2a77-116">Das Express Route-Schaltkreis Objekt, das die zu ändernde Peering-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="b2a77-116">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="b2a77-117">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="b2a77-117">-LegacyMode</span></span>
<span data-ttu-id="b2a77-118">Der Legacy Modus des Peering</span><span class="sxs-lookup"><span data-stu-id="b2a77-118">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="b2a77-119">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="b2a77-119">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="b2a77-120">Für eine PeeringType von MicrosoftPeering müssen Sie eine Liste aller Präfixe angeben, die Sie für die BGP-Sitzung ankündigen möchten.</span><span class="sxs-lookup"><span data-stu-id="b2a77-120">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="b2a77-121">Es werden nur die Präfixe öffentlicher IP-Adressen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="b2a77-121">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="b2a77-122">Sie können eine durch trennzeichengetrennte Liste senden, wenn Sie eine Reihe von Präfixen senden möchten.</span><span class="sxs-lookup"><span data-stu-id="b2a77-122">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="b2a77-123">Diese Präfixe müssen in einem Routing Registrierungsnamen (RIR/IRR) für Sie registriert sein.</span><span class="sxs-lookup"><span data-stu-id="b2a77-123">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="b2a77-124">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="b2a77-124">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="b2a77-125">Wenn Sie Präfixe anzeigen, die nicht für die Peering-Nummer registriert sind, können Sie die als Zahl angeben, in der Sie registriert sind.</span><span class="sxs-lookup"><span data-stu-id="b2a77-125">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="b2a77-126">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="b2a77-126">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="b2a77-127">Der Routing Registrierungs Name (RIR/IRR), in dem die AS-Nummer und die Präfixe registriert sind.</span><span class="sxs-lookup"><span data-stu-id="b2a77-127">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="b2a77-128">-Name</span><span class="sxs-lookup"><span data-stu-id="b2a77-128">-Name</span></span>
<span data-ttu-id="b2a77-129">Der Name der zu ändernden Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b2a77-129">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="b2a77-130">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="b2a77-130">-PeerAddressType</span></span>
<span data-ttu-id="b2a77-131">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="b2a77-131">PeerAddressType</span></span>

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

### <span data-ttu-id="b2a77-132">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="b2a77-132">-PeerASN</span></span>
<span data-ttu-id="b2a77-133">Die AS-Nummer Ihres Express Route-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="b2a77-133">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="b2a77-134">Dies muss ein öffentlicher ASN sein, wenn PeeringType AzurePublicPeering ist.</span><span class="sxs-lookup"><span data-stu-id="b2a77-134">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="b2a77-135">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="b2a77-135">-PeeringType</span></span>
<span data-ttu-id="b2a77-136">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="b2a77-136">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="b2a77-137">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b2a77-137">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="b2a77-138">Dies ist der IP-Adressbereich für den primären Routingpfad dieser Peering-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="b2a77-138">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="b2a77-139">Dies muss ein/30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="b2a77-139">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="b2a77-140">Die erste ungerade nummerierte Adresse in diesem Subnetz sollte Ihrer Router-Schnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="b2a77-140">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="b2a77-141">Azure konfiguriert die nächste gerade nummerierte Adresse für die Azure-Router-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b2a77-141">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="b2a77-142">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b2a77-142">-RouteFilter</span></span>
<span data-ttu-id="b2a77-143">Hierbei handelt es sich um ein vorhandenes RouteFilter-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b2a77-143">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="b2a77-144">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="b2a77-144">-RouteFilterId</span></span>
<span data-ttu-id="b2a77-145">Dies ist die Ressourcen-ID eines vorhandenen RouteFilter-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b2a77-145">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="b2a77-146">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b2a77-146">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="b2a77-147">Hierbei handelt es sich um den IP-Adressbereich für den sekundären Routingpfad dieser Peering-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="b2a77-147">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="b2a77-148">Dies muss ein/30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="b2a77-148">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="b2a77-149">Die erste ungerade nummerierte Adresse in diesem Subnetz sollte Ihrer Router-Schnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="b2a77-149">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="b2a77-150">Azure konfiguriert die nächste gerade nummerierte Adresse für die Azure-Router-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b2a77-150">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="b2a77-151">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="b2a77-151">-SharedKey</span></span>
<span data-ttu-id="b2a77-152">Hierbei handelt es sich um einen optionalen MD5-Hash, der als vorab freigegebener Schlüssel für die Peering-Konfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2a77-152">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="b2a77-153">-VLAN-Nr</span><span class="sxs-lookup"><span data-stu-id="b2a77-153">-VlanId</span></span>
<span data-ttu-id="b2a77-154">Dies ist die ID-Nummer des VLAN, das diesem Peering zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="b2a77-154">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="b2a77-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2a77-155">CommonParameters</span></span>
<span data-ttu-id="b2a77-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2a77-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2a77-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2a77-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2a77-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2a77-158">INPUTS</span></span>

### <span data-ttu-id="b2a77-159">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b2a77-159">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="b2a77-160">System. String</span><span class="sxs-lookup"><span data-stu-id="b2a77-160">System.String</span></span>

### <span data-ttu-id="b2a77-161">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b2a77-161">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="b2a77-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b2a77-162">System.Boolean</span></span>

## <span data-ttu-id="b2a77-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2a77-163">OUTPUTS</span></span>

### <span data-ttu-id="b2a77-164">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b2a77-164">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b2a77-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2a77-165">NOTES</span></span>

## <span data-ttu-id="b2a77-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2a77-166">RELATED LINKS</span></span>

[<span data-ttu-id="b2a77-167">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b2a77-167">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="b2a77-168">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b2a77-168">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="b2a77-169">Neu – AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b2a77-169">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="b2a77-170">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b2a77-170">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)
