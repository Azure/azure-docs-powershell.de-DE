---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 0afd299103f1595afd100a7e9a72c4045896419d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936704"
---
# <span data-ttu-id="926f8-101">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="926f8-101">Set-AzNetworkInterface</span></span>

## <span data-ttu-id="926f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="926f8-102">SYNOPSIS</span></span>
<span data-ttu-id="926f8-103">Aktualisiert eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="926f8-103">Updates a network interface.</span></span>

## <span data-ttu-id="926f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="926f8-104">SYNTAX</span></span>

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="926f8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="926f8-105">DESCRIPTION</span></span>
<span data-ttu-id="926f8-106">Das **Set-AzNetworkInterface aktualisiert** eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="926f8-106">The **Set-AzNetworkInterface** updates a network interface.</span></span>

## <span data-ttu-id="926f8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="926f8-107">EXAMPLES</span></span>

### <span data-ttu-id="926f8-108">Beispiel 1: Konfigurieren einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="926f8-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="926f8-109">In diesem Beispiel wird eine Netzwerkschnittstelle konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="926f8-109">This example configures a network interface.</span></span>
<span data-ttu-id="926f8-110">Der erste Befehl ruft eine Netzwerkschnittstelle mit dem Namen NetworkInterface1 in der Ressourcengruppe ResourceGroup1 ab.</span><span class="sxs-lookup"><span data-stu-id="926f8-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="926f8-111">Der zweite Befehl legt die private IP-Adresse der IP-Konfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="926f8-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="926f8-112">Der dritte Befehl legt die private IP-Zuweisungsmethode auf Statisch fest.</span><span class="sxs-lookup"><span data-stu-id="926f8-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="926f8-113">Der vierte Befehl legt ein Tag auf der Netzwerkschnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="926f8-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="926f8-114">Der fünfte Befehl verwendet die in der Variablen $Nic gespeicherten Informationen zum Festlegen der Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="926f8-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="926f8-115">Beispiel 2: Ändern von DNS-Einstellungen auf einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="926f8-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="926f8-116">Der erste Befehl ruft eine Netzwerkschnittstelle mit dem Namen NetworkInterface1 ab, die in der Ressourcengruppe ResourceGroup1 vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="926f8-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="926f8-117">Der zweite Befehl fügt dieser Schnittstelle DNS Server 192.168.1.100 hinzu.</span><span class="sxs-lookup"><span data-stu-id="926f8-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="926f8-118">Der dritte Befehl wendet diese Änderungen auf die Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="926f8-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="926f8-119">Um einen DNS-Server zu entfernen, folgen Sie den oben aufgeführten Befehlen, ersetzen Sie aber ". Add" mit ". Remove" im zweiten Befehl.</span><span class="sxs-lookup"><span data-stu-id="926f8-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="926f8-120">Beispiel 3: Aktivieren der IP-Weiterleitung auf einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="926f8-120">Example 3: Enable IP forwarding on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="926f8-121">Der erste Befehl ruft eine vorhandene Netzwerkschnittstelle namens NetworkInterface1 ab und speichert sie in der $nic-Variable.</span><span class="sxs-lookup"><span data-stu-id="926f8-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="926f8-122">Mit dem zweiten Befehl wird der WERT für die IP-Weiterleitung in "true" geändert.</span><span class="sxs-lookup"><span data-stu-id="926f8-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="926f8-123">Schließlich wendet der dritte Befehl die Änderungen auf die Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="926f8-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="926f8-124">Um die IP-Weiterleitung auf einer Netzwerkschnittstelle zu deaktivieren, folgen Sie dem Beispiel, aber achten Sie darauf, den zweiten Befehl in "$nic. EnableIPForwarding = 0".</span><span class="sxs-lookup"><span data-stu-id="926f8-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="926f8-125">Beispiel 4: Ändern des Subnetzes einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="926f8-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="926f8-126">Der erste Befehl ruft die Netzwerkschnittstelle NetworkInterface1 ab und speichert sie in der $nic Variablen.</span><span class="sxs-lookup"><span data-stu-id="926f8-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="926f8-127">Der zweite Befehl ruft das virtuelle Netzwerk ab, das dem Subnetz zugeordnet ist, dem die Netzwerkschnittstelle zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="926f8-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="926f8-128">Der zweite Befehl ruft das Subnetz ab und speichert es in der $subnet 2-Variable.</span><span class="sxs-lookup"><span data-stu-id="926f8-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="926f8-129">Der dritte Befehl verknüpfte die primäre private IP-Adresse der Netzwerkschnittstelle mit dem neuen Subnetz.</span><span class="sxs-lookup"><span data-stu-id="926f8-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="926f8-130">Schließlich hat der letzte Befehl diese Änderungen auf der Netzwerkschnittstelle angewendet.</span><span class="sxs-lookup"><span data-stu-id="926f8-130">Finally the last command applied these changes on the network interface.</span></span>
>[!NOTE] 
><span data-ttu-id="926f8-131">Die IP-Konfigurationen müssen dynamisch sein, bevor Sie das Subnetz ändern können.</span><span class="sxs-lookup"><span data-stu-id="926f8-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="926f8-132">Wenn Sie über statische IP-Konfigurationen verfügen, ändern Sie dann in dynamisch, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="926f8-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 
>[!NOTE]
><span data-ttu-id="926f8-133">Wenn die Netzwerkschnittstelle über mehrere IP-Konfigurationen verfügt, muss der vierte Befehl für alle diese IP-Konfigurationen ausgeführt werden, bevor der Set-AzNetworkInterface ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="926f8-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzNetworkInterface command is executed.</span></span> <span data-ttu-id="926f8-134">Dies kann wie im vierten Befehl geschehen, aber durch Ersetzen von "0" durch die entsprechende Zahl.</span><span class="sxs-lookup"><span data-stu-id="926f8-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="926f8-135">Wenn eine Netzwerkschnittstelle über N-IP-Konfigurationen verfügt, muss N-1 dieser Befehle vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="926f8-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="926f8-136">Beispiel 5: Zuordnen/Trennen einer Netzwerksicherheitsgruppe zu einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="926f8-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="926f8-137">Der erste Befehl ruft eine vorhandene Netzwerkschnittstelle namens NetworkInterface1 ab und speichert sie in der $nic-Variable.</span><span class="sxs-lookup"><span data-stu-id="926f8-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="926f8-138">Der zweite Befehl ruft eine vorhandene Netzwerksicherheitsgruppe namens MyNSG ab und speichert sie in der $nsg-Variable.</span><span class="sxs-lookup"><span data-stu-id="926f8-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="926f8-139">Der dritte Befehl weist die $nsg dem $nic.</span><span class="sxs-lookup"><span data-stu-id="926f8-139">The third command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="926f8-140">Schließlich wendet der vierte Befehl die Änderungen auf die Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="926f8-140">Finally, the forth command applies the changes to the Network interface.</span></span> <span data-ttu-id="926f8-141">Zum Trennen von Netzwerksicherheitsgruppen von einer Netzwerkschnittstelle ersetzen Sie einfach $nsg im dritten Befehl durch $null.</span><span class="sxs-lookup"><span data-stu-id="926f8-141">To dissociate network security groups from a network interface, simple replace $nsg in the third command with $null.</span></span>

## <span data-ttu-id="926f8-142">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="926f8-142">PARAMETERS</span></span>

### <span data-ttu-id="926f8-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="926f8-143">-AsJob</span></span>
<span data-ttu-id="926f8-144">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="926f8-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="926f8-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="926f8-145">-DefaultProfile</span></span>
<span data-ttu-id="926f8-146">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="926f8-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="926f8-147">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="926f8-147">-NetworkInterface</span></span>
<span data-ttu-id="926f8-148">Gibt ein Netzwerkschnittstellenobjekt an, das den Zustand darstellt, auf den die Netzwerkschnittstelle festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="926f8-148">Specifies a network interface object representing the state to which the network interface should be set.</span></span>

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

### <span data-ttu-id="926f8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="926f8-149">CommonParameters</span></span>
<span data-ttu-id="926f8-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="926f8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="926f8-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="926f8-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="926f8-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="926f8-152">INPUTS</span></span>

### <span data-ttu-id="926f8-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="926f8-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="926f8-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="926f8-154">OUTPUTS</span></span>

### <span data-ttu-id="926f8-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="926f8-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="926f8-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="926f8-156">NOTES</span></span>

## <span data-ttu-id="926f8-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="926f8-157">RELATED LINKS</span></span>

[<span data-ttu-id="926f8-158">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="926f8-158">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="926f8-159">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="926f8-159">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="926f8-160">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="926f8-160">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="926f8-161">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="926f8-161">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)
