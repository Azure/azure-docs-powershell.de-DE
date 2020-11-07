---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 92740ce457c9e7c571f925e1813bc120a88a86a5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660924"
---
# <span data-ttu-id="ed0f9-101">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ed0f9-101">Add-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="ed0f9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed0f9-102">SYNOPSIS</span></span>
<span data-ttu-id="ed0f9-103">Fügt eine Peering-Konfiguration zu einer Express Route-Querverbindung hinzu.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-103">Adds a peering configuration to an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="ed0f9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed0f9-104">SYNTAX</span></span>

```
Add-AzExpressRouteCrossConnectionPeering -Name <String>
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-Force] -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefix <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed0f9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed0f9-105">DESCRIPTION</span></span>
<span data-ttu-id="ed0f9-106">Das Cmdlet **Add-AzExpressRouteCrossConnectionPeering** fügt eine Peering-Konfiguration zu einer Express Route-Querverbindung hinzu.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-106">The **Add-AzExpressRouteCrossConnectionPeering** cmdlet adds a peering configuration to an ExpressRoute cross connection.</span></span> <span data-ttu-id="ed0f9-107">Beachten Sie, dass Sie nach dem Ausführen von **Add-AzExpressRouteCrossConnectionPeering** das Set-AzExpressRouteCrossConnection-Cmdlet aufrufen müssen, um die Konfiguration zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-107">Note that, after running **Add-AzExpressRouteCrossConnectionPeering** , you must call the Set-AzExpressRouteCrossConnection cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="ed0f9-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed0f9-108">EXAMPLES</span></span>

### <span data-ttu-id="ed0f9-109">Beispiel 1: Hinzufügen eines Peers zu einer vorhandenen Express Route-Querverbindung</span><span class="sxs-lookup"><span data-stu-id="ed0f9-109">Example 1: Add a peer to an existing ExpressRoute cross connection</span></span>
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

## <span data-ttu-id="ed0f9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed0f9-110">PARAMETERS</span></span>

### <span data-ttu-id="ed0f9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed0f9-111">-DefaultProfile</span></span>
<span data-ttu-id="ed0f9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed0f9-113">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ed0f9-113">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="ed0f9-114">Die Express Route-Querverbindung wird geändert.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-114">The ExpressRoute cross connection being modified.</span></span> <span data-ttu-id="ed0f9-115">Hierbei handelt es sich um ein Azure-Objekt, das vom Cmdlet **Get-AzExpressRouteCrossConnection** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-115">This is Azure object returned by the **Get-AzExpressRouteCrossConnection** cmdlet.</span></span>

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

### <span data-ttu-id="ed0f9-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ed0f9-116">-Force</span></span>
<span data-ttu-id="ed0f9-117">Keine Bestätigung anfordern, wenn Sie eine Ressource overriten möchten</span><span class="sxs-lookup"><span data-stu-id="ed0f9-117">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="ed0f9-118">-MicrosoftConfigAdvertisedPublicPrefix</span><span class="sxs-lookup"><span data-stu-id="ed0f9-118">-MicrosoftConfigAdvertisedPublicPrefix</span></span>
<span data-ttu-id="ed0f9-119">Für eine PeeringType von MicrosoftPeering müssen Sie eine Liste aller Präfixe angeben, die Sie für die BGP-Sitzung ankündigen möchten.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="ed0f9-120">Es werden nur die Präfixe öffentlicher IP-Adressen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="ed0f9-121">Sie können eine durch trennzeichengetrennte Liste senden, wenn Sie eine Reihe von Präfixen senden möchten.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="ed0f9-122">Diese Präfixe müssen in einem Routing Registrierungsnamen (RIR/IRR) für Sie registriert sein.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="ed0f9-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="ed0f9-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="ed0f9-124">Wenn Sie Präfixe anzeigen, die nicht für die Peering-Nummer registriert sind, können Sie die als Zahl angeben, in der Sie registriert sind.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="ed0f9-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="ed0f9-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="ed0f9-126">Der Routing Registrierungs Name (RIR/IRR), in dem die AS-Nummer und die Präfixe registriert sind.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="ed0f9-127">-Name</span><span class="sxs-lookup"><span data-stu-id="ed0f9-127">-Name</span></span>
<span data-ttu-id="ed0f9-128">Der Name der Peering-Beziehung, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-128">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="ed0f9-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ed0f9-129">-PeerAddressType</span></span>
<span data-ttu-id="ed0f9-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ed0f9-130">PeerAddressType</span></span>

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

### <span data-ttu-id="ed0f9-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="ed0f9-131">-PeerASN</span></span>
<span data-ttu-id="ed0f9-132">Die AS-Nummer Ihrer Express Route-Querverbindung.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-132">The AS number of your ExpressRoute cross connection.</span></span> <span data-ttu-id="ed0f9-133">Dies muss ein öffentlicher ASN sein, wenn PeeringType AzurePublicPeering ist.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="ed0f9-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="ed0f9-134">-PeeringType</span></span>
<span data-ttu-id="ed0f9-135">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` , `AzurePublicPeering` und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="ed0f9-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="ed0f9-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ed0f9-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="ed0f9-137">Dies ist der IP-Adressbereich für den primären Routingpfad dieser Peering-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="ed0f9-138">Dies muss ein/30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="ed0f9-139">Die erste ungerade nummerierte Adresse in diesem Subnetz sollte Ihrer Router-Schnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="ed0f9-140">Azure konfiguriert die nächste gerade nummerierte Adresse für die Azure-Router-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="ed0f9-141">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ed0f9-141">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="ed0f9-142">Hierbei handelt es sich um den IP-Adressbereich für den sekundären Routingpfad dieser Peering-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-142">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="ed0f9-143">Dies muss ein/30 CIDR-Subnetz sein.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-143">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="ed0f9-144">Die erste ungerade nummerierte Adresse in diesem Subnetz sollte Ihrer Router-Schnittstelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-144">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="ed0f9-145">Azure konfiguriert die nächste gerade nummerierte Adresse für die Azure-Router-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-145">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="ed0f9-146">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="ed0f9-146">-SharedKey</span></span>
<span data-ttu-id="ed0f9-147">Hierbei handelt es sich um einen optionalen MD5-Hash, der als vorab freigegebener Schlüssel für die Peering-Konfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-147">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="ed0f9-148">-VLAN-Nr</span><span class="sxs-lookup"><span data-stu-id="ed0f9-148">-VlanId</span></span>
<span data-ttu-id="ed0f9-149">Dies ist die ID-Nummer des VLAN, das diesem Peering zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-149">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="ed0f9-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ed0f9-150">-Confirm</span></span>
<span data-ttu-id="ed0f9-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed0f9-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed0f9-152">-WhatIf</span></span>
<span data-ttu-id="ed0f9-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed0f9-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed0f9-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed0f9-155">CommonParameters</span></span>
<span data-ttu-id="ed0f9-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed0f9-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed0f9-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed0f9-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed0f9-158">INPUTS</span></span>

### <span data-ttu-id="ed0f9-159">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ed0f9-159">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="ed0f9-160">Der Parameter "ExpressRouteCrossConnection" akzeptiert den Wert vom Typ "PSExpressRouteCrossConnection" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ed0f9-160">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="ed0f9-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed0f9-161">OUTPUTS</span></span>

### <span data-ttu-id="ed0f9-162">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ed0f9-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="ed0f9-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed0f9-163">NOTES</span></span>

## <span data-ttu-id="ed0f9-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed0f9-164">RELATED LINKS</span></span>

[<span data-ttu-id="ed0f9-165">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ed0f9-165">Get-AzExpressRouteCrossConnectionPeering</span></span>](Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="ed0f9-166">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ed0f9-166">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="ed0f9-167">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ed0f9-167">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="ed0f9-168">Satz-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ed0f9-168">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
