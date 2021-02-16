---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 3899bfcd607e4d3e5e5b1d92e8a62096037102a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170076"
---
# <span data-ttu-id="5ac6b-101">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="5ac6b-101">Add-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="5ac6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ac6b-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac6b-103">Fügt einer ExpressRoute-Kreuzverbindung eine Peeringkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-103">Adds a peering configuration to an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="5ac6b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ac6b-104">SYNTAX</span></span>

```
Add-AzExpressRouteCrossConnectionPeering -Name <String>
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-Force] -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefix <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ac6b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ac6b-105">DESCRIPTION</span></span>
<span data-ttu-id="5ac6b-106">Das **Cmdlet "Add-AzExpressRouteCrossConnectionPeering"** fügt einer ExpressRoute-Kreuzverbindung eine Peeringkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-106">The **Add-AzExpressRouteCrossConnectionPeering** cmdlet adds a peering configuration to an ExpressRoute cross connection.</span></span> <span data-ttu-id="5ac6b-107">Beachten Sie, dass Sie nach dem Ausführen von **"Add-AzExpressRouteCrossConnectionPeering"** das cmdlet Set-AzExpressRouteCrossConnection aufrufen müssen, um die Konfiguration zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-107">Note that, after running **Add-AzExpressRouteCrossConnectionPeering**, you must call the Set-AzExpressRouteCrossConnection cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="5ac6b-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5ac6b-108">EXAMPLES</span></span>

### <span data-ttu-id="5ac6b-109">Beispiel 1: Hinzufügen eines Peers zu einer vorhandenen ExpressRoute-Kreuzverbindung</span><span class="sxs-lookup"><span data-stu-id="5ac6b-109">Example 1: Add a peer to an existing ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    CrossConnection = $cc
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCrossConnectionPeering @parameters
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="5ac6b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ac6b-110">PARAMETERS</span></span>

### <span data-ttu-id="5ac6b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac6b-111">-DefaultProfile</span></span>
<span data-ttu-id="5ac6b-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ac6b-113">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="5ac6b-113">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="5ac6b-114">Die ExpressRoute-Kreuzverbindung, die geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-114">The ExpressRoute cross connection being modified.</span></span> <span data-ttu-id="5ac6b-115">Dies ist das Azure-Objekt, das vom **Cmdlet "Get-AzExpressRouteCrossConnection"** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-115">This is Azure object returned by the **Get-AzExpressRouteCrossConnection** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac6b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5ac6b-116">-Force</span></span>
<span data-ttu-id="5ac6b-117">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="5ac6b-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac6b-118">-MicrosoftConfigAdvertisedPublicPrefix</span><span class="sxs-lookup"><span data-stu-id="5ac6b-118">-MicrosoftConfigAdvertisedPublicPrefix</span></span>
<span data-ttu-id="5ac6b-119">Für einen PeeringType von MicrosoftPeering müssen Sie eine Liste aller Präfixe bereitstellen, die Über die BGP-Sitzung angekündigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="5ac6b-120">Es werden nur Öffentliche IP-Adresspräfixe akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="5ac6b-121">Sie können eine durch Kommas getrennte Liste senden, wenn Sie eine Gruppe von Präfixen senden möchten.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="5ac6b-122">Diese Präfixe müssen bei Ihnen unter einem Routingregistrierungsnamen (ROUTING Registry Name, RIR/IRR) registriert sein.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="5ac6b-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="5ac6b-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="5ac6b-124">Wenn Sie Präfixe anzeigen, die nicht für die Peering -AS-Nummer registriert sind, können Sie die AS-Nummer angeben, mit der sie registriert sind.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="5ac6b-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="5ac6b-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="5ac6b-126">Der Routingregistrierungsname (ROUTING Registry Name, RIR/IRR), für den die AS-Nummer und -Präfixe registriert sind.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="5ac6b-127">-Name</span><span class="sxs-lookup"><span data-stu-id="5ac6b-127">-Name</span></span>
<span data-ttu-id="5ac6b-128">Der Name der Peeringbeziehung, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-128">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="5ac6b-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="5ac6b-129">-PeerAddressType</span></span>
<span data-ttu-id="5ac6b-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="5ac6b-130">PeerAddressType</span></span>

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

### <span data-ttu-id="5ac6b-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="5ac6b-131">-PeerASN</span></span>
<span data-ttu-id="5ac6b-132">Die AS-Nummer Ihrer ExpressRoute-Kreuzverbindung.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-132">The AS number of your ExpressRoute cross connection.</span></span> <span data-ttu-id="5ac6b-133">Dies muss ein öffentlicher ASN sein, wenn "PeeringType" "AzurePublicPeering" ist.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="5ac6b-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="5ac6b-134">-PeeringType</span></span>
<span data-ttu-id="5ac6b-135">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` `AzurePublicPeering` , und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="5ac6b-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="5ac6b-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5ac6b-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="5ac6b-137">Dies ist der IP-Adressbereich für den primären Routingpfad dieser Peeringbeziehung.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="5ac6b-138">Dies muss ein /30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="5ac6b-139">Die erste Adresse mit ungerader Nummer in diesem Subnetz sollte Ihrer Routerschnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="5ac6b-140">Azure konfiguriert die nächste adresse mit gleichmäßiger Nummer für die Azure-Routerschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="5ac6b-141">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5ac6b-141">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="5ac6b-142">Dies ist der IP-Adressbereich für den sekundären Routingpfad dieser Peeringbeziehung.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-142">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="5ac6b-143">Dies muss ein /30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-143">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="5ac6b-144">Die erste Adresse mit ungerader Nummer in diesem Subnetz sollte Ihrer Routerschnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-144">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="5ac6b-145">Azure konfiguriert die nächste adresse mit gleichmäßiger Nummer für die Azure-Routerschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-145">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="5ac6b-146">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="5ac6b-146">-SharedKey</span></span>
<span data-ttu-id="5ac6b-147">Dies ist ein optionaler MD5-Hash, der als vorab freigegebener Schlüssel für die Peeringkonfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-147">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="5ac6b-148">-YrnId</span><span class="sxs-lookup"><span data-stu-id="5ac6b-148">-VlanId</span></span>
<span data-ttu-id="5ac6b-149">Dies ist die ID-Nummer des FÜR DIESES Peering zugewiesenen ODEREINNs.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-149">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="5ac6b-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ac6b-150">-Confirm</span></span>
<span data-ttu-id="5ac6b-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ac6b-152">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5ac6b-152">-WhatIf</span></span>
<span data-ttu-id="5ac6b-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ac6b-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ac6b-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac6b-155">CommonParameters</span></span>
<span data-ttu-id="5ac6b-156">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ac6b-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac6b-157">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ac6b-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac6b-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5ac6b-158">INPUTS</span></span>

### <span data-ttu-id="5ac6b-159">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="5ac6b-159">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="5ac6b-160">Der Parameter 'ExpressRouteCrossConnection' akzeptiert den Wert des Typs 'PSExpressRouteCrossConnection' aus der Pipeline</span><span class="sxs-lookup"><span data-stu-id="5ac6b-160">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="5ac6b-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5ac6b-161">OUTPUTS</span></span>

### <span data-ttu-id="5ac6b-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="5ac6b-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="5ac6b-163">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5ac6b-163">NOTES</span></span>

## <span data-ttu-id="5ac6b-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5ac6b-164">RELATED LINKS</span></span>

[<span data-ttu-id="5ac6b-165">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="5ac6b-165">Get-AzExpressRouteCrossConnectionPeering</span></span>](Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="5ac6b-166">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="5ac6b-166">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="5ac6b-167">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="5ac6b-167">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="5ac6b-168">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="5ac6b-168">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
