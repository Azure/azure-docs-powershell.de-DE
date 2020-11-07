---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
ms.openlocfilehash: b7dc6c405ae1a5a213cedcb4b9737ff23dcf2b36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663780"
---
# <span data-ttu-id="d79ad-101">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d79ad-101">New-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="d79ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d79ad-102">SYNOPSIS</span></span>
<span data-ttu-id="d79ad-103">Erstellt ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="d79ad-103">Creates a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d79ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d79ad-104">SYNTAX</span></span>

```
New-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-Subnet <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]>]
 [-Tag <Hashtable>] [-EnableDDoSProtection] [-EnableVmProtection] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d79ad-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d79ad-105">DESCRIPTION</span></span>
<span data-ttu-id="d79ad-106">Mit dem Cmdlet **New-AzureRmVirtualNetwork** wird ein Azure-virtuelles Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="d79ad-106">The **New-AzureRmVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="d79ad-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d79ad-107">EXAMPLES</span></span>

### <span data-ttu-id="d79ad-108">1: Erstellen eines virtuellen Netzwerks mit zwei Subnetzen</span><span class="sxs-lookup"><span data-stu-id="d79ad-108">1:  Create a virtual network with two subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="d79ad-109">In diesem Beispiel wird ein virtuelles Netzwerk mit zwei Subnetzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="d79ad-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="d79ad-110">Zunächst wird eine neue Ressourcengruppe in der Region centralus erstellt.</span><span class="sxs-lookup"><span data-stu-id="d79ad-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="d79ad-111">Anschließend werden im Beispiel in-Memory-Darstellungen von zwei Subnetzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="d79ad-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="d79ad-112">Das New-AzureRmVirtualNetworkSubnetConfig-Cmdlet erstellt kein Subnetz auf der Serverseite.</span><span class="sxs-lookup"><span data-stu-id="d79ad-112">The New-AzureRmVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="d79ad-113">Es gibt ein Subnetz namens frontendSubnet und ein Subnetz mit dem Namen backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="d79ad-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="d79ad-114">Das New-AzureRmVirtualNetwork-Cmdlet erstellt dann ein virtuelles Netzwerk mit dem CIDR-10.0.0.0/16 als Adresspräfix und zwei Subnetzen.</span><span class="sxs-lookup"><span data-stu-id="d79ad-114">The New-AzureRmVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="d79ad-115">2: Erstellen eines virtuellen Netzwerks mit DNS-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d79ad-115">2:  Create a virtual network with DNS settings</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="d79ad-116">In diesem Beispiel wird ein virtuelles Netzwerk mit zwei Subnetzen und zwei DNS-Servern erstellt.</span><span class="sxs-lookup"><span data-stu-id="d79ad-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="d79ad-117">Die Angabe der DNS-Server im virtuellen Netzwerk bewirkt, dass die NICs/VMS, die in diesem virtuellen Netzwerk bereitgestellt werden, diese DNS-Server als Standardwerte erben.</span><span class="sxs-lookup"><span data-stu-id="d79ad-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="d79ad-118">Diese Standardeinstellungen können pro NIC über eine NIC-Level-Einstellung überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d79ad-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="d79ad-119">Wenn auf einem VNET keine DNS-Server und keine DNS-Server auf den NICs angegeben sind, werden die standardmäßigen Azure-DNS-Server für die DNS-Auflösung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d79ad-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="d79ad-120">3: Erstellen eines virtuellen Netzwerks mit einem Subnetz, das auf eine Netzwerksicherheitsgruppe verweist</span><span class="sxs-lookup"><span data-stu-id="d79ad-120">3: Create a virtual network with a subnet referencing a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="d79ad-121">In diesem Beispiel wird ein virtuelles Netzwerk mit Subnetzen erstellt, die auf eine Netzwerksicherheitsgruppe verweisen.</span><span class="sxs-lookup"><span data-stu-id="d79ad-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="d79ad-122">Im Beispiel wird zunächst eine Ressourcengruppe als Container für die zu erstellden Ressourcen erstellt.</span><span class="sxs-lookup"><span data-stu-id="d79ad-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="d79ad-123">Anschließend wird eine Netzwerksicherheitsgruppe erstellt, die den eingehenden RDP-Zugriff zulässt, aber ansonsten die standardmäßigen Netzwerk Sicherheitsgruppen Regeln erzwingt.</span><span class="sxs-lookup"><span data-stu-id="d79ad-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="d79ad-124">Das New-AzureRmVirtualNetworkSubnetConfig-Cmdlet erstellt dann in-Memory-Darstellungen von zwei Subnetzen, die beide auf die erstellte Netzwerksicherheitsgruppe verweisen.</span><span class="sxs-lookup"><span data-stu-id="d79ad-124">The New-AzureRmVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="d79ad-125">Mit dem Befehl New-AzureRmVirtualNetwork wird dann das virtuelle Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="d79ad-125">The New-AzureRmVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="d79ad-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="d79ad-126">PARAMETERS</span></span>

### <span data-ttu-id="d79ad-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d79ad-127">-AddressPrefix</span></span>
<span data-ttu-id="d79ad-128">Gibt einen Bereich von IP-Adressen für ein virtuelles Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="d79ad-128">Specifies a range of IP addresses for a virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d79ad-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d79ad-129">-AsJob</span></span>
<span data-ttu-id="d79ad-130">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d79ad-130">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79ad-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d79ad-131">-DefaultProfile</span></span>
<span data-ttu-id="d79ad-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d79ad-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79ad-133">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="d79ad-133">-DnsServer</span></span>
<span data-ttu-id="d79ad-134">Gibt den DNS-Server für ein Subnetz an.</span><span class="sxs-lookup"><span data-stu-id="d79ad-134">Specifies the DNS server for a subnet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d79ad-135">-EnableDDoSProtection</span><span class="sxs-lookup"><span data-stu-id="d79ad-135">-EnableDDoSProtection</span></span>
<span data-ttu-id="d79ad-136">Ein Switch-Parameter, der darstellt, ob DDoS-Schutz aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="d79ad-136">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d79ad-137">-EnableVmProtection</span><span class="sxs-lookup"><span data-stu-id="d79ad-137">-EnableVmProtection</span></span>
<span data-ttu-id="d79ad-138">Ein Switch-Parameter, der darstellt, ob der VM-Schutz aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d79ad-138">A switch parameter which represents if Vm protection is enabled or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d79ad-139">-Force</span><span class="sxs-lookup"><span data-stu-id="d79ad-139">-Force</span></span>
<span data-ttu-id="d79ad-140">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d79ad-140">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79ad-141">-Standort</span><span class="sxs-lookup"><span data-stu-id="d79ad-141">-Location</span></span>
<span data-ttu-id="d79ad-142">Gibt den Bereich für das virtuelle Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="d79ad-142">Specifies the region for the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d79ad-143">-Name</span><span class="sxs-lookup"><span data-stu-id="d79ad-143">-Name</span></span>
<span data-ttu-id="d79ad-144">Gibt den Namen des virtuellen Netzwerks an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d79ad-144">Specifies the name of the virtual network that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d79ad-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d79ad-145">-ResourceGroupName</span></span>
<span data-ttu-id="d79ad-146">Gibt den Namen einer Ressourcengruppe an, die das virtuelle Netzwerk enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="d79ad-146">Specifies the name of a resource group to contain the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d79ad-147">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="d79ad-147">-Subnet</span></span>
<span data-ttu-id="d79ad-148">Gibt eine Liste der Subnetze an, die dem virtuellen Netzwerk zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d79ad-148">Specifies a list of subnets to associate with the virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d79ad-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="d79ad-149">-Tag</span></span>
<span data-ttu-id="d79ad-150">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="d79ad-150">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d79ad-151">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d79ad-151">For example:</span></span>

<span data-ttu-id="d79ad-152">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="d79ad-152">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d79ad-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d79ad-153">-Confirm</span></span>
<span data-ttu-id="d79ad-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d79ad-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79ad-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d79ad-155">-WhatIf</span></span>
<span data-ttu-id="d79ad-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d79ad-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d79ad-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d79ad-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79ad-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d79ad-158">CommonParameters</span></span>
<span data-ttu-id="d79ad-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d79ad-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d79ad-160">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d79ad-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d79ad-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d79ad-161">INPUTS</span></span>

### <span data-ttu-id="d79ad-162">Keine</span><span class="sxs-lookup"><span data-stu-id="d79ad-162">None</span></span>
<span data-ttu-id="d79ad-163">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d79ad-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d79ad-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d79ad-164">OUTPUTS</span></span>

### <span data-ttu-id="d79ad-165">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d79ad-165">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="d79ad-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="d79ad-166">NOTES</span></span>

## <span data-ttu-id="d79ad-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d79ad-167">RELATED LINKS</span></span>

[<span data-ttu-id="d79ad-168">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d79ad-168">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="d79ad-169">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d79ad-169">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="d79ad-170">Satz-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d79ad-170">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)
