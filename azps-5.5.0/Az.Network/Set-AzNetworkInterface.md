---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9b851bcbaa545dee99628dc066956854181df7f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154084"
---
# <span data-ttu-id="c6e7c-101">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c6e7c-101">Set-AzNetworkInterface</span></span>

## <span data-ttu-id="c6e7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="c6e7c-103">Aktualisiert eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-103">Updates a network interface.</span></span>

## <span data-ttu-id="c6e7c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6e7c-104">SYNTAX</span></span>

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6e7c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6e7c-105">DESCRIPTION</span></span>
<span data-ttu-id="c6e7c-106">**Set-AzNetworkInterface aktualisiert** eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-106">The **Set-AzNetworkInterface** updates a network interface.</span></span>

## <span data-ttu-id="c6e7c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c6e7c-107">EXAMPLES</span></span>

### <span data-ttu-id="c6e7c-108">Beispiel 1: Konfigurieren einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="c6e7c-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="c6e7c-109">In diesem Beispiel wird eine Netzwerkschnittstelle konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-109">This example configures a network interface.</span></span>
<span data-ttu-id="c6e7c-110">Der erste Befehl ruft eine Netzwerkschnittstelle namens "NetworkInterface1" in der Ressourcengruppe "ResourceGroup1" ab.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="c6e7c-111">Der zweite Befehl legt die private IP-Adresse der IP-Konfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="c6e7c-112">Der dritte Befehl legt die Private -IP-Zuweisungsmethode auf "Static" fest.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="c6e7c-113">Der vierte Befehl legt ein Tag für die Netzwerkschnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="c6e7c-114">Der fünfte Befehl verwendet die in der Variablen $Nic gespeicherten Informationen zum Festlegen der Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="c6e7c-115">Beispiel 2: Ändern von DNS-Einstellungen auf einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="c6e7c-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="c6e7c-116">Der erste Befehl ruft eine Netzwerkschnittstelle namens "NetworkInterface1" ab, die in der Ressourcengruppe "ResourceGroup1" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="c6e7c-117">Mit dem zweiten Befehl wird dieser Schnittstelle der DNS-Server 192.168.1.100 hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="c6e7c-118">Der dritte Befehl wendet diese Änderungen auf die Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="c6e7c-119">Zum Entfernen eines DNS-Servers folgen Sie den oben aufgeführten Befehlen, ersetzen aber ". Hinzufügen" mit ". Remove" im zweiten Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="c6e7c-120">Beispiel 3: Aktivieren der IP-Weiterleitung auf einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="c6e7c-120">Example 3: Enable IP forwarding on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="c6e7c-121">Der erste Befehl ruft eine vorhandene Netzwerkschnittstelle namens "NetworkInterface1" ab und speichert sie in der $nic Variable.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="c6e7c-122">Mit dem zweiten Befehl wird der Wert für die IP-Weiterleitung auf "true" geändert.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="c6e7c-123">Schließlich wendet der dritte Befehl die Änderungen an der Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="c6e7c-124">Um die IP-Weiterleitung auf einer Netzwerkschnittstelle zu deaktivieren, folgen Sie dem Beispielbeispiel. Achten Sie jedoch darauf, den zweiten Befehl in "$nic. EnableIPForwarding = 0".</span><span class="sxs-lookup"><span data-stu-id="c6e7c-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="c6e7c-125">Beispiel 4: Ändern des Subnetzes einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="c6e7c-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="c6e7c-126">Der erste Befehl ruft die Netzwerkschnittstelle "NetworkInterface1" ab und speichert sie in der $nic Variable.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="c6e7c-127">Der zweite Befehl ruft das virtuelle Netzwerk ab, das dem Subnetz zugeordnet ist, dem die Netzwerkschnittstelle zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="c6e7c-128">Der zweite Befehl ruft das Subnetz ab und speichert es in der $subnet 2-Variable.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="c6e7c-129">Der dritte Befehl hat dem neuen Subnetz die primäre private IP-Adresse der Netzwerkschnittstelle zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="c6e7c-130">Zuletzt hat der letzte Befehl diese Änderungen auf der Netzwerkschnittstelle angewendet.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-130">Finally the last command applied these changes on the network interface.</span></span>
>[!NOTE] 
><span data-ttu-id="c6e7c-131">Die IP-Konfigurationen müssen dynamisch sein, bevor Sie das Subnetz ändern können.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="c6e7c-132">Wenn Sie über statische IP-Konfigurationen verfügen, ändern Sie diese in "Dynamisch", bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 
>[!NOTE]
><span data-ttu-id="c6e7c-133">Verfügt die Netzwerkschnittstelle über mehrere IP-Konfigurationen, muss der vierte Befehl für alle diese IP-Konfigurationen ausgeführt werden, bevor der Set-AzNetworkInterface ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzNetworkInterface command is executed.</span></span> <span data-ttu-id="c6e7c-134">Dies kann wie im vierten Befehl geschehen, aber durch Ersetzen von "0" durch die entsprechende Zahl.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="c6e7c-135">Wenn eine Netzwerkschnittstelle über N-IP-Konfigurationen verfügt, müssen N-1 dieser Befehle vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="c6e7c-136">Beispiel 5: Zuordnen/Trennen einer Netzwerksicherheitsgruppe zu einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="c6e7c-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="c6e7c-137">Der erste Befehl ruft eine vorhandene Netzwerkschnittstelle namens "NetworkInterface1" ab und speichert sie in der $nic Variable.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="c6e7c-138">Der zweite Befehl ruft eine vorhandene Netzwerksicherheitsgruppe namens "MyNSG" ab und speichert sie in $nsg Variable.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="c6e7c-139">Der dritte Befehl weist die $nsg dem $nic.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-139">The third command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="c6e7c-140">Schließlich wendet der vierte Befehl die Änderungen auf die Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-140">Finally, the forth command applies the changes to the Network interface.</span></span> <span data-ttu-id="c6e7c-141">Um Netzwerksicherheitsgruppen von einer Netzwerkschnittstelle zu trennen, ersetzen Sie einfach $nsg im dritten Befehl durch $null.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-141">To dissociate network security groups from a network interface, simple replace $nsg in the third command with $null.</span></span>

## <span data-ttu-id="c6e7c-142">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6e7c-142">PARAMETERS</span></span>

### <span data-ttu-id="c6e7c-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6e7c-143">-AsJob</span></span>
<span data-ttu-id="c6e7c-144">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c6e7c-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6e7c-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6e7c-145">-DefaultProfile</span></span>
<span data-ttu-id="c6e7c-146">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6e7c-147">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c6e7c-147">-NetworkInterface</span></span>
<span data-ttu-id="c6e7c-148">Gibt ein Netzwerkschnittstellenobjekt an, das den Zustand darstellt, auf den die Netzwerkschnittstelle festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-148">Specifies a network interface object representing the state to which the network interface should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6e7c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6e7c-149">CommonParameters</span></span>
<span data-ttu-id="c6e7c-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6e7c-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6e7c-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6e7c-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c6e7c-152">INPUTS</span></span>

### <span data-ttu-id="c6e7c-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c6e7c-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="c6e7c-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c6e7c-154">OUTPUTS</span></span>

### <span data-ttu-id="c6e7c-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c6e7c-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="c6e7c-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c6e7c-156">NOTES</span></span>

## <span data-ttu-id="c6e7c-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c6e7c-157">RELATED LINKS</span></span>

[<span data-ttu-id="c6e7c-158">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c6e7c-158">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="c6e7c-159">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c6e7c-159">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="c6e7c-160">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c6e7c-160">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="c6e7c-161">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c6e7c-161">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)
