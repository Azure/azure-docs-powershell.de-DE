---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: b16206fdcaf775315947ca9fe71f487d1f9d8df1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948571"
---
# <span data-ttu-id="92b1d-101">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="92b1d-101">Add-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="92b1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92b1d-102">SYNOPSIS</span></span>
<span data-ttu-id="92b1d-103">Fügt einer ExpressRoute-Querverbindung eine Peeringkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="92b1d-103">Adds a peering configuration to an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="92b1d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92b1d-104">SYNTAX</span></span>

```
Add-AzExpressRouteCrossConnectionPeering -Name <String>
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-Force] -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefix <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92b1d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92b1d-105">DESCRIPTION</span></span>
<span data-ttu-id="92b1d-106">Das **Add-AzExpressRouteCrossConnectionPeering-Cmdlet** fügt einer ExpressRoute-Querverbindung eine Peeringkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="92b1d-106">The **Add-AzExpressRouteCrossConnectionPeering** cmdlet adds a peering configuration to an ExpressRoute cross connection.</span></span> <span data-ttu-id="92b1d-107">Beachten Sie, dass Sie nach dem Ausführen von **Add-AzExpressRouteCrossConnectionPeering** das cmdlet Set-AzExpressRouteCrossConnection aufrufen müssen, um die Konfiguration zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="92b1d-107">Note that, after running **Add-AzExpressRouteCrossConnectionPeering**, you must call the Set-AzExpressRouteCrossConnection cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="92b1d-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="92b1d-108">EXAMPLES</span></span>

### <span data-ttu-id="92b1d-109">Beispiel 1: Hinzufügen eines Peers zu einer vorhandenen ExpressRoute-Querverbindung</span><span class="sxs-lookup"><span data-stu-id="92b1d-109">Example 1: Add a peer to an existing ExpressRoute cross connection</span></span>
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

## <span data-ttu-id="92b1d-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="92b1d-110">PARAMETERS</span></span>

### <span data-ttu-id="92b1d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b1d-111">-DefaultProfile</span></span>
<span data-ttu-id="92b1d-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92b1d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92b1d-113">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="92b1d-113">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="92b1d-114">Die ExpressRoute-Querverbindung, die geändert wird.</span><span class="sxs-lookup"><span data-stu-id="92b1d-114">The ExpressRoute cross connection being modified.</span></span> <span data-ttu-id="92b1d-115">Dies ist ein Vom **Get-AzExpressRouteCrossConnection-Cmdlet** zurückgegebenes Azure-Objekt.</span><span class="sxs-lookup"><span data-stu-id="92b1d-115">This is Azure object returned by the **Get-AzExpressRouteCrossConnection** cmdlet.</span></span>

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

### <span data-ttu-id="92b1d-116">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="92b1d-116">-Force</span></span>
<span data-ttu-id="92b1d-117">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="92b1d-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="92b1d-118">-MicrosoftConfigAdvertisedPublicPrefix</span><span class="sxs-lookup"><span data-stu-id="92b1d-118">-MicrosoftConfigAdvertisedPublicPrefix</span></span>
<span data-ttu-id="92b1d-119">Für einen PeeringType von MicrosoftPeering müssen Sie eine Liste aller Präfixe bereitstellen, die Sie über die BGP-Sitzung bewerben möchten.</span><span class="sxs-lookup"><span data-stu-id="92b1d-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="92b1d-120">Es werden nur präfixe für öffentliche IP-Adressen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="92b1d-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="92b1d-121">Sie können eine durch Kommas getrennte Liste senden, wenn Sie eine Reihe von Präfixen senden möchten.</span><span class="sxs-lookup"><span data-stu-id="92b1d-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="92b1d-122">Diese Präfixe müssen für Sie in einem Routingregistrierungsnamen (ROUTING Registry Name, RIR/IRR) registriert sein.</span><span class="sxs-lookup"><span data-stu-id="92b1d-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="92b1d-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="92b1d-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="92b1d-124">Wenn Sie Präfixe anzeigen, die nicht für die Peering-AS-Nummer registriert sind, können Sie die AS-Nummer angeben, für die sie registriert sind.</span><span class="sxs-lookup"><span data-stu-id="92b1d-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="92b1d-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="92b1d-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="92b1d-126">Der Routingregistrierungsname (RIR/IRR), für den die AS-Nummer und -Präfixe registriert sind.</span><span class="sxs-lookup"><span data-stu-id="92b1d-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="92b1d-127">-Name</span><span class="sxs-lookup"><span data-stu-id="92b1d-127">-Name</span></span>
<span data-ttu-id="92b1d-128">Der Name der peering-Beziehung, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="92b1d-128">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="92b1d-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="92b1d-129">-PeerAddressType</span></span>
<span data-ttu-id="92b1d-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="92b1d-130">PeerAddressType</span></span>

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

### <span data-ttu-id="92b1d-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="92b1d-131">-PeerASN</span></span>
<span data-ttu-id="92b1d-132">Die AS-Nummer Ihrer ExpressRoute-Querverbindung.</span><span class="sxs-lookup"><span data-stu-id="92b1d-132">The AS number of your ExpressRoute cross connection.</span></span> <span data-ttu-id="92b1d-133">Dies muss ein öffentlicher ASN sein, wenn der PeeringType AzurePublicPeering ist.</span><span class="sxs-lookup"><span data-stu-id="92b1d-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="92b1d-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="92b1d-134">-PeeringType</span></span>
<span data-ttu-id="92b1d-135">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` `AzurePublicPeering` , und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="92b1d-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="92b1d-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="92b1d-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="92b1d-137">Dies ist der IP-Adressbereich für den primären Routingpfad dieser Peeringbeziehung.</span><span class="sxs-lookup"><span data-stu-id="92b1d-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="92b1d-138">Dies muss ein /30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="92b1d-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="92b1d-139">Die erste ungerade Nummerierte Adresse in diesem Subnetz sollte Ihrer Routerschnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="92b1d-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="92b1d-140">Azure konfiguriert die nächste gleichmäßig nummerierte Adresse für die Azure-Routerschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="92b1d-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="92b1d-141">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="92b1d-141">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="92b1d-142">Dies ist der IP-Adressbereich für den sekundären Routingpfad dieser Peeringbeziehung.</span><span class="sxs-lookup"><span data-stu-id="92b1d-142">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="92b1d-143">Dies muss ein /30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="92b1d-143">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="92b1d-144">Die erste ungerade Nummerierte Adresse in diesem Subnetz sollte Ihrer Routerschnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="92b1d-144">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="92b1d-145">Azure konfiguriert die nächste gleichmäßig nummerierte Adresse für die Azure-Routerschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="92b1d-145">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="92b1d-146">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="92b1d-146">-SharedKey</span></span>
<span data-ttu-id="92b1d-147">Dies ist ein optionaler MD5-Hash, der als vorab freigegebener Schlüssel für die Peeringkonfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="92b1d-147">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="92b1d-148">-VlanId</span><span class="sxs-lookup"><span data-stu-id="92b1d-148">-VlanId</span></span>
<span data-ttu-id="92b1d-149">Dies ist die ID-Nummer des für dieses Peering zugewiesenen VLANs.</span><span class="sxs-lookup"><span data-stu-id="92b1d-149">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="92b1d-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="92b1d-150">-Confirm</span></span>
<span data-ttu-id="92b1d-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="92b1d-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92b1d-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92b1d-152">-WhatIf</span></span>
<span data-ttu-id="92b1d-153">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92b1d-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92b1d-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92b1d-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92b1d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b1d-155">CommonParameters</span></span>
<span data-ttu-id="92b1d-156">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92b1d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b1d-157">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92b1d-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b1d-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="92b1d-158">INPUTS</span></span>

### <span data-ttu-id="92b1d-159">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="92b1d-159">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="92b1d-160">Der Parameter "ExpressRouteCrossConnection" akzeptiert den Wert vom Typ "PSExpressRouteCrossConnection" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="92b1d-160">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="92b1d-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="92b1d-161">OUTPUTS</span></span>

### <span data-ttu-id="92b1d-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="92b1d-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="92b1d-163">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="92b1d-163">NOTES</span></span>

## <span data-ttu-id="92b1d-164">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="92b1d-164">RELATED LINKS</span></span>

[<span data-ttu-id="92b1d-165">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="92b1d-165">Get-AzExpressRouteCrossConnectionPeering</span></span>](Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="92b1d-166">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="92b1d-166">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="92b1d-167">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="92b1d-167">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="92b1d-168">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="92b1d-168">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
