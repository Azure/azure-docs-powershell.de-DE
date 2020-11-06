---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 87c956769efb41485e43e65ff31d7a9cd7387d9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503230"
---
# <span data-ttu-id="59496-101">Set-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="59496-101">Set-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="59496-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59496-102">SYNOPSIS</span></span>
<span data-ttu-id="59496-103">Speichert eine geänderte Express Route-Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="59496-103">Saves a modified ExpressRoute peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59496-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59496-104">SYNTAX</span></span>

### <span data-ttu-id="59496-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="59496-105">SetByResource (Default)</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59496-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="59496-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59496-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="59496-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59496-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59496-108">DESCRIPTION</span></span>
<span data-ttu-id="59496-109">Die Cmdlets für "AzureRmExpressRouteCircuitPeeringConfig" speichern eine geänderte Express Route **-** Peering-Konfiguration wieder in Azure.</span><span class="sxs-lookup"><span data-stu-id="59496-109">The **Set-AzureRmExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="59496-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59496-110">EXAMPLES</span></span>

### <span data-ttu-id="59496-111">Beispiel 1: Ändern einer vorhandenen Peering-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="59496-111">Example 1: Change an existing peering configuration</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 201
}
Set-AzureRmExpressRouteCircuitPeeringConfig @parameters
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="59496-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="59496-112">PARAMETERS</span></span>

### <span data-ttu-id="59496-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="59496-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="59496-114">Das Express Route-Schaltkreis Objekt, das die zu ändernde Peering-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="59496-114">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="59496-115">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="59496-115">-LegacyMode</span></span>
<span data-ttu-id="59496-116">Der Legacy Modus des Peering</span><span class="sxs-lookup"><span data-stu-id="59496-116">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="59496-117">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="59496-117">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="59496-118">Für eine PeeringType von MicrosoftPeering müssen Sie eine Liste aller Präfixe angeben, die Sie für die BGP-Sitzung ankündigen möchten.</span><span class="sxs-lookup"><span data-stu-id="59496-118">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="59496-119">Es werden nur die Präfixe öffentlicher IP-Adressen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="59496-119">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="59496-120">Sie können eine durch trennzeichengetrennte Liste senden, wenn Sie eine Reihe von Präfixen senden möchten.</span><span class="sxs-lookup"><span data-stu-id="59496-120">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="59496-121">Diese Präfixe müssen in einem Routing Registrierungsnamen (RIR/IRR) für Sie registriert sein.</span><span class="sxs-lookup"><span data-stu-id="59496-121">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="59496-122">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="59496-122">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="59496-123">Wenn Sie Präfixe anzeigen, die nicht für die Peering-Nummer registriert sind, können Sie die als Zahl angeben, in der Sie registriert sind.</span><span class="sxs-lookup"><span data-stu-id="59496-123">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="59496-124">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="59496-124">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="59496-125">Der Routing Registrierungs Name (RIR/IRR), in dem die AS-Nummer und die Präfixe registriert sind.</span><span class="sxs-lookup"><span data-stu-id="59496-125">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="59496-126">-Name</span><span class="sxs-lookup"><span data-stu-id="59496-126">-Name</span></span>
<span data-ttu-id="59496-127">Der Name der zu ändernden Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="59496-127">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="59496-128">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="59496-128">-PeerAddressType</span></span>
<span data-ttu-id="59496-129">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="59496-129">PeerAddressType</span></span>

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

### <span data-ttu-id="59496-130">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="59496-130">-PeerASN</span></span>
<span data-ttu-id="59496-131">Die AS-Nummer Ihres Express Route-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="59496-131">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="59496-132">Dies muss ein öffentlicher ASN sein, wenn PeeringType AzurePublicPeering ist.</span><span class="sxs-lookup"><span data-stu-id="59496-132">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="59496-133">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="59496-133">-PeeringType</span></span>
<span data-ttu-id="59496-134">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="59496-134">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="59496-135">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="59496-135">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="59496-136">Dies ist der IP-Adressbereich für den primären Routingpfad dieser Peering-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="59496-136">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="59496-137">Dies muss ein/30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="59496-137">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="59496-138">Die erste ungerade nummerierte Adresse in diesem Subnetz sollte Ihrer Router-Schnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="59496-138">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="59496-139">Azure konfiguriert die nächste gerade nummerierte Adresse für die Azure-Router-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="59496-139">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="59496-140">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="59496-140">-RouteFilter</span></span>
<span data-ttu-id="59496-141">Hierbei handelt es sich um ein vorhandenes RouteFilter-Objekt.</span><span class="sxs-lookup"><span data-stu-id="59496-141">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="59496-142">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="59496-142">-RouteFilterId</span></span>
<span data-ttu-id="59496-143">Dies ist die Ressourcen-ID eines vorhandenen RouteFilter-Objekts.</span><span class="sxs-lookup"><span data-stu-id="59496-143">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="59496-144">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="59496-144">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="59496-145">Hierbei handelt es sich um den IP-Adressbereich für den sekundären Routingpfad dieser Peering-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="59496-145">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="59496-146">Dies muss ein/30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="59496-146">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="59496-147">Die erste ungerade nummerierte Adresse in diesem Subnetz sollte Ihrer Router-Schnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="59496-147">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="59496-148">Azure konfiguriert die nächste gerade nummerierte Adresse für die Azure-Router-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="59496-148">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="59496-149">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="59496-149">-SharedKey</span></span>
<span data-ttu-id="59496-150">Hierbei handelt es sich um einen optionalen MD5-Hash, der als vorab freigegebener Schlüssel für die Peering-Konfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="59496-150">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="59496-151">-VLAN-Nr</span><span class="sxs-lookup"><span data-stu-id="59496-151">-VlanId</span></span>
<span data-ttu-id="59496-152">Dies ist die ID-Nummer des VLAN, das diesem Peering zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="59496-152">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="59496-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59496-153">-DefaultProfile</span></span>
<span data-ttu-id="59496-154">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="59496-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59496-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59496-155">CommonParameters</span></span>
<span data-ttu-id="59496-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59496-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59496-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59496-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59496-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59496-158">INPUTS</span></span>

### <span data-ttu-id="59496-159">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="59496-159">PSExpressRouteCircuit</span></span>
<span data-ttu-id="59496-160">Der Parameter "ExpressRouteCircuit" akzeptiert den Wert vom Typ "PSExpressRouteCircuit" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="59496-160">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="59496-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59496-161">OUTPUTS</span></span>

### <span data-ttu-id="59496-162">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="59496-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="59496-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="59496-163">NOTES</span></span>

## <span data-ttu-id="59496-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59496-164">RELATED LINKS</span></span>

[<span data-ttu-id="59496-165">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="59496-165">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="59496-166">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="59496-166">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="59496-167">Neu – AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="59496-167">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="59496-168">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="59496-168">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)
