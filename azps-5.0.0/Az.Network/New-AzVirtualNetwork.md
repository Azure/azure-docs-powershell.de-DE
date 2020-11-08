---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: d131b4aa22f46fed151486ed2d87f32684b6035a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178730"
---
# <span data-ttu-id="c900c-101">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c900c-101">New-AzVirtualNetwork</span></span>

## <span data-ttu-id="c900c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c900c-102">SYNOPSIS</span></span>
<span data-ttu-id="c900c-103">Erstellt ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="c900c-103">Creates a virtual network.</span></span>

## <span data-ttu-id="c900c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c900c-104">SYNTAX</span></span>

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String> -AddressPrefix <String[]>
 [-DnsServer <String[]>] [-Subnet <PSSubnet[]>] [-BgpCommunity <String>] [-Tag <Hashtable>]
 [-EnableDdosProtection] [-DdosProtectionPlanId <String>] [-IpAllocation <PSIpAllocation[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c900c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c900c-105">DESCRIPTION</span></span>
<span data-ttu-id="c900c-106">Mit dem Cmdlet **New-AzVirtualNetwork** wird ein Azure-virtuelles Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="c900c-106">The **New-AzVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="c900c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c900c-107">EXAMPLES</span></span>

### <span data-ttu-id="c900c-108">Beispiel 1: Erstellen eines virtuellen Netzwerks mit zwei Subnetzen</span><span class="sxs-lookup"><span data-stu-id="c900c-108">Example 1: Create a virtual network with two subnets</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="c900c-109">In diesem Beispiel wird ein virtuelles Netzwerk mit zwei Subnetzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="c900c-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="c900c-110">Zunächst wird eine neue Ressourcengruppe in der Region centralus erstellt.</span><span class="sxs-lookup"><span data-stu-id="c900c-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="c900c-111">Anschließend werden im Beispiel in-Memory-Darstellungen von zwei Subnetzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="c900c-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="c900c-112">Das New-AzVirtualNetworkSubnetConfig-Cmdlet erstellt kein Subnetz auf der Serverseite.</span><span class="sxs-lookup"><span data-stu-id="c900c-112">The New-AzVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="c900c-113">Es gibt ein Subnetz namens frontendSubnet und ein Subnetz mit dem Namen backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="c900c-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="c900c-114">Das New-AzVirtualNetwork-Cmdlet erstellt dann ein virtuelles Netzwerk mit dem CIDR-10.0.0.0/16 als Adresspräfix und zwei Subnetzen.</span><span class="sxs-lookup"><span data-stu-id="c900c-114">The New-AzVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="c900c-115">Beispiel 2: Erstellen eines virtuellen Netzwerks mit DNS-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="c900c-115">Example 2: Create a virtual network with DNS settings</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="c900c-116">In diesem Beispiel wird ein virtuelles Netzwerk mit zwei Subnetzen und zwei DNS-Servern erstellt.</span><span class="sxs-lookup"><span data-stu-id="c900c-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="c900c-117">Die Angabe der DNS-Server im virtuellen Netzwerk bewirkt, dass die NICs/VMS, die in diesem virtuellen Netzwerk bereitgestellt werden, diese DNS-Server als Standardwerte erben.</span><span class="sxs-lookup"><span data-stu-id="c900c-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="c900c-118">Diese Standardeinstellungen können pro NIC über eine NIC-Level-Einstellung überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c900c-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="c900c-119">Wenn auf einem VNET keine DNS-Server und keine DNS-Server auf den NICs angegeben sind, werden die standardmäßigen Azure-DNS-Server für die DNS-Auflösung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c900c-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="c900c-120">Beispiel 3: Erstellen eines virtuellen Netzwerks mit einem Subnetz, das auf eine Netzwerksicherheitsgruppe verweist</span><span class="sxs-lookup"><span data-stu-id="c900c-120">Example 3: Create a virtual network with a subnet referencing a network security group</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="c900c-121">In diesem Beispiel wird ein virtuelles Netzwerk mit Subnetzen erstellt, die auf eine Netzwerksicherheitsgruppe verweisen.</span><span class="sxs-lookup"><span data-stu-id="c900c-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="c900c-122">Im Beispiel wird zunächst eine Ressourcengruppe als Container für die zu erstellden Ressourcen erstellt.</span><span class="sxs-lookup"><span data-stu-id="c900c-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="c900c-123">Anschließend wird eine Netzwerksicherheitsgruppe erstellt, die den eingehenden RDP-Zugriff zulässt, aber ansonsten die standardmäßigen Netzwerk Sicherheitsgruppen Regeln erzwingt.</span><span class="sxs-lookup"><span data-stu-id="c900c-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="c900c-124">Das New-AzVirtualNetworkSubnetConfig-Cmdlet erstellt dann in-Memory-Darstellungen von zwei Subnetzen, die beide auf die erstellte Netzwerksicherheitsgruppe verweisen.</span><span class="sxs-lookup"><span data-stu-id="c900c-124">The New-AzVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="c900c-125">Mit dem Befehl New-AzVirtualNetwork wird dann das virtuelle Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="c900c-125">The New-AzVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="c900c-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="c900c-126">PARAMETERS</span></span>

### <span data-ttu-id="c900c-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c900c-127">-AddressPrefix</span></span>
<span data-ttu-id="c900c-128">Gibt einen Bereich von IP-Adressen für ein virtuelles Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="c900c-128">Specifies a range of IP addresses for a virtual network.</span></span>

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

### <span data-ttu-id="c900c-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c900c-129">-AsJob</span></span>
<span data-ttu-id="c900c-130">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c900c-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c900c-131">-BgpCommunity</span><span class="sxs-lookup"><span data-stu-id="c900c-131">-BgpCommunity</span></span>
<span data-ttu-id="c900c-132">Die BGP-Community, die über Express Route angekündigt wurde.</span><span class="sxs-lookup"><span data-stu-id="c900c-132">The BGP Community advertised over ExpressRoute.</span></span>

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

### <span data-ttu-id="c900c-133">-DdosProtectionPlanId</span><span class="sxs-lookup"><span data-stu-id="c900c-133">-DdosProtectionPlanId</span></span>
<span data-ttu-id="c900c-134">Verweis auf die dem virtuellen Netzwerk zugeordnete Ressource für DDoS-Schutzplan.</span><span class="sxs-lookup"><span data-stu-id="c900c-134">Reference to the DDoS protection plan resource associated with the virtual network.</span></span>

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

### <span data-ttu-id="c900c-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c900c-135">-DefaultProfile</span></span>
<span data-ttu-id="c900c-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c900c-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c900c-137">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="c900c-137">-DnsServer</span></span>
<span data-ttu-id="c900c-138">Gibt den DNS-Server für ein Subnetz an.</span><span class="sxs-lookup"><span data-stu-id="c900c-138">Specifies the DNS server for a subnet.</span></span>

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

### <span data-ttu-id="c900c-139">-EnableDdosProtection</span><span class="sxs-lookup"><span data-stu-id="c900c-139">-EnableDdosProtection</span></span>
<span data-ttu-id="c900c-140">Ein Switch-Parameter, der darstellt, ob DDoS-Schutz aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="c900c-140">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

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

### <span data-ttu-id="c900c-141">-Force</span><span class="sxs-lookup"><span data-stu-id="c900c-141">-Force</span></span>
<span data-ttu-id="c900c-142">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c900c-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c900c-143">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="c900c-143">-IpAllocation</span></span>
<span data-ttu-id="c900c-144">Gibt IpAllocations für ein virtuelles Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="c900c-144">Specifies IpAllocations for a virtual network.</span></span>

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

### <span data-ttu-id="c900c-145">-Standort</span><span class="sxs-lookup"><span data-stu-id="c900c-145">-Location</span></span>
<span data-ttu-id="c900c-146">Gibt den Bereich für das virtuelle Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="c900c-146">Specifies the region for the virtual network.</span></span>

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

### <span data-ttu-id="c900c-147">-Name</span><span class="sxs-lookup"><span data-stu-id="c900c-147">-Name</span></span>
<span data-ttu-id="c900c-148">Gibt den Namen des virtuellen Netzwerks an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c900c-148">Specifies the name of the virtual network that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c900c-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c900c-149">-ResourceGroupName</span></span>
<span data-ttu-id="c900c-150">Gibt den Namen einer Ressourcengruppe an, die das virtuelle Netzwerk enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="c900c-150">Specifies the name of a resource group to contain the virtual network.</span></span>

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

### <span data-ttu-id="c900c-151">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="c900c-151">-Subnet</span></span>
<span data-ttu-id="c900c-152">Gibt eine Liste der Subnetze an, die dem virtuellen Netzwerk zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c900c-152">Specifies a list of subnets to associate with the virtual network.</span></span>

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

### <span data-ttu-id="c900c-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="c900c-153">-Tag</span></span>
<span data-ttu-id="c900c-154">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="c900c-154">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c900c-155">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="c900c-155">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c900c-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c900c-156">-Confirm</span></span>
<span data-ttu-id="c900c-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c900c-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c900c-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c900c-158">-WhatIf</span></span>
<span data-ttu-id="c900c-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c900c-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c900c-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c900c-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c900c-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c900c-161">CommonParameters</span></span>
<span data-ttu-id="c900c-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c900c-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c900c-163">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c900c-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c900c-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c900c-164">INPUTS</span></span>

### <span data-ttu-id="c900c-165">System. String</span><span class="sxs-lookup"><span data-stu-id="c900c-165">System.String</span></span>

### <span data-ttu-id="c900c-166">System. String []</span><span class="sxs-lookup"><span data-stu-id="c900c-166">System.String[]</span></span>

### <span data-ttu-id="c900c-167">Microsoft. Azure. Commands. Network. Models. PSSubnet []</span><span class="sxs-lookup"><span data-stu-id="c900c-167">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span></span>

### <span data-ttu-id="c900c-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c900c-168">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c900c-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c900c-169">OUTPUTS</span></span>

### <span data-ttu-id="c900c-170">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c900c-170">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="c900c-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="c900c-171">NOTES</span></span>

## <span data-ttu-id="c900c-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c900c-172">RELATED LINKS</span></span>

[<span data-ttu-id="c900c-173">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c900c-173">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="c900c-174">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c900c-174">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="c900c-175">Satz-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c900c-175">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="c900c-176">Neu – AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="c900c-176">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)
