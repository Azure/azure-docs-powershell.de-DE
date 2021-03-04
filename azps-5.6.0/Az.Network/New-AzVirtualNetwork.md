---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: 9608dfd5a780006d2ab050a1ca2e85ee26949f97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923480"
---
# <span data-ttu-id="ab2b9-101">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ab2b9-101">New-AzVirtualNetwork</span></span>

## <span data-ttu-id="ab2b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab2b9-102">SYNOPSIS</span></span>
<span data-ttu-id="ab2b9-103">Erstellt ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-103">Creates a virtual network.</span></span>

## <span data-ttu-id="ab2b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab2b9-104">SYNTAX</span></span>

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String> -AddressPrefix <String[]>
 [-DnsServer <String[]>] [-Subnet <PSSubnet[]>] [-BgpCommunity <String>] [-Tag <Hashtable>]
 [-EnableDdosProtection] [-DdosProtectionPlanId <String>] [-IpAllocation <PSIpAllocation[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab2b9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab2b9-105">DESCRIPTION</span></span>
<span data-ttu-id="ab2b9-106">Das **Cmdlet New-AzVirtualNetwork** erstellt ein virtuelles Azure-Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-106">The **New-AzVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="ab2b9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ab2b9-107">EXAMPLES</span></span>

### <span data-ttu-id="ab2b9-108">Beispiel 1: Erstellen eines virtuellen Netzwerks mit zwei Subnetzen</span><span class="sxs-lookup"><span data-stu-id="ab2b9-108">Example 1: Create a virtual network with two subnets</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="ab2b9-109">In diesem Beispiel wird ein virtuelles Netzwerk mit zwei Subnetzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="ab2b9-110">Zuerst wird eine neue Ressourcengruppe in der Zentralen Region erstellt.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="ab2b9-111">Anschließend werden im Beispiel Arbeitsspeicherdarstellungen von zwei Subnetzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="ab2b9-112">Das New-AzVirtualNetworkSubnetConfig cmdlet erstellt kein Subnetz auf der Serverseite.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-112">The New-AzVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="ab2b9-113">Es gibt ein Subnetz namens frontendSubnet und ein Subnetz mit dem Namen back-EndSubnet.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="ab2b9-114">Das New-AzVirtualNetwork-Cmdlet erstellt dann ein virtuelles Netzwerk mit dem CIDR 10.0.0.0/16 als Adresspräfix und zwei Subnetzen.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-114">The New-AzVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="ab2b9-115">Beispiel 2: Erstellen eines virtuellen Netzwerks mit DNS-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="ab2b9-115">Example 2: Create a virtual network with DNS settings</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="ab2b9-116">In diesem Beispiel wird ein virtuelles Netzwerk mit zwei Subnetzen und zwei DNS-Servern erstellt.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="ab2b9-117">Die Angabe der DNS-Server im virtuellen Netzwerk hat zur Folge, dass die in diesem virtuellen Netzwerk bereitgestellten NICs/VMs diese DNS-Server als Standardwerte erben.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="ab2b9-118">Diese Standardwerte können pro NIC über eine Einstellung auf NIC-Ebene überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="ab2b9-119">Wenn auf einem VNET keine DNS-Server und auf den NICs keine DNS-Server angegeben sind, werden die standardmäßigen Azure -DNS-Server für die DNS-Auflösung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="ab2b9-120">Beispiel 3: Erstellen eines virtuellen Netzwerks mit einem Subnetz, das auf eine Netzwerksicherheitsgruppe bezugt</span><span class="sxs-lookup"><span data-stu-id="ab2b9-120">Example 3: Create a virtual network with a subnet referencing a network security group</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="ab2b9-121">In diesem Beispiel wird ein virtuelles Netzwerk mit Subnetzen erstellt, die auf eine Netzwerksicherheitsgruppe verweisen.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="ab2b9-122">Zunächst erstellt das Beispiel eine Ressourcengruppe als Container für die Ressourcen, die erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="ab2b9-123">Anschließend wird eine Netzwerksicherheitsgruppe erstellt, die den eingehenden RDP-Zugriff zulässt, andernfalls jedoch die standardmäßigen Netzwerksicherheitsgrupperegeln erzwingt.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="ab2b9-124">Das New-AzVirtualNetworkSubnetConfig-Cmdlet erstellt dann Arbeitsspeicherdarstellungen von zwei Subnetzen, die beide auf die erstellte Netzwerksicherheitsgruppe verweisen.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-124">The New-AzVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="ab2b9-125">Der New-AzVirtualNetwork erstellt dann das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-125">The New-AzVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="ab2b9-126">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ab2b9-126">PARAMETERS</span></span>

### <span data-ttu-id="ab2b9-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ab2b9-127">-AddressPrefix</span></span>
<span data-ttu-id="ab2b9-128">Gibt einen Bereich von IP-Adressen für ein virtuelles Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-128">Specifies a range of IP addresses for a virtual network.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab2b9-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab2b9-129">-AsJob</span></span>
<span data-ttu-id="ab2b9-130">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ab2b9-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab2b9-131">-BgpCommunity</span><span class="sxs-lookup"><span data-stu-id="ab2b9-131">-BgpCommunity</span></span>
<span data-ttu-id="ab2b9-132">Die über ExpressRoute angekündigte BGP-Community.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-132">The BGP Community advertised over ExpressRoute.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab2b9-133">-DdosProtectionPlanId</span><span class="sxs-lookup"><span data-stu-id="ab2b9-133">-DdosProtectionPlanId</span></span>
<span data-ttu-id="ab2b9-134">Verweisen Sie auf die dem virtuellen Netzwerk zugeordnete DDoS-Schutzplanressource.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-134">Reference to the DDoS protection plan resource associated with the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab2b9-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab2b9-135">-DefaultProfile</span></span>
<span data-ttu-id="ab2b9-136">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab2b9-137">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="ab2b9-137">-DnsServer</span></span>
<span data-ttu-id="ab2b9-138">Gibt den DNS-Server für ein Subnetz an.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-138">Specifies the DNS server for a subnet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab2b9-139">-EnableDdosProtection</span><span class="sxs-lookup"><span data-stu-id="ab2b9-139">-EnableDdosProtection</span></span>
<span data-ttu-id="ab2b9-140">Ein Schalterparameter, der darstellt, ob der DDoS-Schutz aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-140">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab2b9-141">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="ab2b9-141">-Force</span></span>
<span data-ttu-id="ab2b9-142">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ab2b9-143">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="ab2b9-143">-IpAllocation</span></span>
<span data-ttu-id="ab2b9-144">Gibt IpAllocations für ein virtuelles Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-144">Specifies IpAllocations for a virtual network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab2b9-145">-Location</span><span class="sxs-lookup"><span data-stu-id="ab2b9-145">-Location</span></span>
<span data-ttu-id="ab2b9-146">Gibt den Bereich für das virtuelle Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-146">Specifies the region for the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab2b9-147">-Name</span><span class="sxs-lookup"><span data-stu-id="ab2b9-147">-Name</span></span>
<span data-ttu-id="ab2b9-148">Gibt den Namen des virtuellen Netzwerks an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-148">Specifies the name of the virtual network that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab2b9-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab2b9-149">-ResourceGroupName</span></span>
<span data-ttu-id="ab2b9-150">Gibt den Namen einer Ressourcengruppe an, die das virtuelle Netzwerk enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-150">Specifies the name of a resource group to contain the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab2b9-151">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="ab2b9-151">-Subnet</span></span>
<span data-ttu-id="ab2b9-152">Gibt eine Liste der Subnetze an, die dem virtuellen Netzwerk zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-152">Specifies a list of subnets to associate with the virtual network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab2b9-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="ab2b9-153">-Tag</span></span>
<span data-ttu-id="ab2b9-154">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-154">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ab2b9-155">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="ab2b9-155">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab2b9-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ab2b9-156">-Confirm</span></span>
<span data-ttu-id="ab2b9-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab2b9-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab2b9-158">-WhatIf</span></span>
<span data-ttu-id="ab2b9-159">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab2b9-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab2b9-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab2b9-161">CommonParameters</span></span>
<span data-ttu-id="ab2b9-162">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab2b9-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab2b9-163">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab2b9-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab2b9-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ab2b9-164">INPUTS</span></span>

### <span data-ttu-id="ab2b9-165">System.String</span><span class="sxs-lookup"><span data-stu-id="ab2b9-165">System.String</span></span>

### <span data-ttu-id="ab2b9-166">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ab2b9-166">System.String[]</span></span>

### <span data-ttu-id="ab2b9-167">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span><span class="sxs-lookup"><span data-stu-id="ab2b9-167">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span></span>

### <span data-ttu-id="ab2b9-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ab2b9-168">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ab2b9-169">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ab2b9-169">OUTPUTS</span></span>

### <span data-ttu-id="ab2b9-170">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ab2b9-170">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="ab2b9-171">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ab2b9-171">NOTES</span></span>

## <span data-ttu-id="ab2b9-172">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ab2b9-172">RELATED LINKS</span></span>

[<span data-ttu-id="ab2b9-173">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ab2b9-173">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="ab2b9-174">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ab2b9-174">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="ab2b9-175">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ab2b9-175">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="ab2b9-176">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="ab2b9-176">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)
