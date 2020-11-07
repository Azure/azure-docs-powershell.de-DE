---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 389a34a5b1c34618339bb7a1752031eaafb9efe9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843611"
---
# <span data-ttu-id="b43d6-101">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b43d6-101">Set-AzNetworkInterface</span></span>

## <span data-ttu-id="b43d6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b43d6-102">SYNOPSIS</span></span>
<span data-ttu-id="b43d6-103">Legt den Zielstatus für eine Netzwerkschnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="b43d6-103">Sets the goal state for a network interface.</span></span>

## <span data-ttu-id="b43d6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b43d6-104">SYNTAX</span></span>

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b43d6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b43d6-105">DESCRIPTION</span></span>
<span data-ttu-id="b43d6-106">Das **Set-AzNetworkInterface** legt den Zielstatus für eine Azure-Netzwerkschnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="b43d6-106">The **Set-AzNetworkInterface** sets the goal state for an Azure network interface.</span></span>

## <span data-ttu-id="b43d6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b43d6-107">EXAMPLES</span></span>

### <span data-ttu-id="b43d6-108">Beispiel 1: Konfigurieren einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="b43d6-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="b43d6-109">In diesem Beispiel wird eine Netzwerkschnittstelle konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="b43d6-109">This example configures a network interface.</span></span>
<span data-ttu-id="b43d6-110">Der erste Befehl ruft eine Netzwerkschnittstelle mit dem Namen NetworkInterface1 in der Ressourcengruppe ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="b43d6-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="b43d6-111">Der zweite Befehl legt die private IP-Adresse der IP-Konfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="b43d6-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="b43d6-112">Der dritte Befehl legt die private IP-Zuordnungsmethode auf static fest.</span><span class="sxs-lookup"><span data-stu-id="b43d6-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="b43d6-113">Der vierte Befehl legt ein Tag auf der Netzwerkschnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="b43d6-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="b43d6-114">Der fünfte Befehl verwendet die in der $NIC-Variablen gespeicherten Informationen, um die Netzwerkschnittstelle einzurichten.</span><span class="sxs-lookup"><span data-stu-id="b43d6-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="b43d6-115">Beispiel 2: Ändern der DNS-Einstellungen auf einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="b43d6-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="b43d6-116">Der erste Befehl ruft eine Netzwerkschnittstelle mit dem Namen NetworkInterface1 ab, die innerhalb der Ressourcengruppen-ResourceGroup1 vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b43d6-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="b43d6-117">Mit dem zweiten Befehl wird dieser Schnittstelle der DNS-Server 192.168.1.100 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b43d6-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="b43d6-118">Der dritte Befehl wendet diese Änderungen auf die Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="b43d6-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="b43d6-119">Wenn Sie einen DNS-Server entfernen möchten, folgen Sie den oben aufgeführten Befehlen, ersetzen Sie aber ". "Mit" hinzufügen. Remove "im zweiten Befehl.</span><span class="sxs-lookup"><span data-stu-id="b43d6-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="b43d6-120">Beispiel 3: Aktivieren von IP-Forwading auf einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="b43d6-120">Example 3: Enable IP forwading on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="b43d6-121">Der erste Befehl ruft eine vorhandene Netzwerkschnittstelle namens NetworkInterface1 ab und speichert Sie in der $NIC-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b43d6-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="b43d6-122">Mit dem zweiten Befehl wird der Wert für die IP-Weiterleitung in true geändert.</span><span class="sxs-lookup"><span data-stu-id="b43d6-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="b43d6-123">Schließlich wendet der dritte Befehl die Änderungen auf die Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="b43d6-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="b43d6-124">Wenn Sie die IP-Weiterleitung auf einer Netzwerkschnittstelle deaktivieren möchten, folgen Sie dem Beispiel Beispiel, aber stellen Sie sicher, dass Sie den zweiten Befehl in "$Nic" ändern. EnableIPForwarding = 0 ".</span><span class="sxs-lookup"><span data-stu-id="b43d6-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="b43d6-125">Beispiel 4: Ändern des Subnets einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="b43d6-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="b43d6-126">Der erste Befehl ruft die Netzwerkschnittstellen-NetworkInterface1 ab und speichert Sie in der $NIC-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b43d6-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="b43d6-127">Der zweite Befehl ruft das virtuelle Netzwerk ab, dem das Subnetz zugeordnet ist, dem die Netzwerkschnittstelle zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b43d6-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="b43d6-128">Der zweite Befehl ruft das Subnetz ab und speichert es in der Variablen $Subnet 2.</span><span class="sxs-lookup"><span data-stu-id="b43d6-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="b43d6-129">Der dritte Befehl verknüpfte die primäre private IP-Adresse der Netzwerkschnittstelle mit dem neuen Subnetz.</span><span class="sxs-lookup"><span data-stu-id="b43d6-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="b43d6-130">Schließlich hat der letzte Befehl diese Änderungen auf der Netzwerkschnittstelle übernommen.</span><span class="sxs-lookup"><span data-stu-id="b43d6-130">Finally the last command applied these changes on the network interface.</span></span>

>[!NOTE] 
><span data-ttu-id="b43d6-131">Die IP-Konfigurationen müssen dynamisch sein, bevor Sie das Subnetz ändern können.</span><span class="sxs-lookup"><span data-stu-id="b43d6-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="b43d6-132">Wenn Sie über statische IP-Konfigurationen verfügen, wechseln Sie dann zu Dynamic, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="b43d6-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 

>[!NOTE]
><span data-ttu-id="b43d6-133">Wenn die Netzwerkschnittstelle über mehrere IP-Konfigurationen verfügt, muss der Befehl Forth für alle diese IP-Konfigurationen ausgeführt werden, bevor der endgültige Set-AzNetworkInterface Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b43d6-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzNetworkInterface command is executed.</span></span> <span data-ttu-id="b43d6-134">Dies kann wie im Befehl Forth erfolgen, aber durch Ersetzen von "0" durch die entsprechende Zahl.</span><span class="sxs-lookup"><span data-stu-id="b43d6-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="b43d6-135">Wenn eine Netzwerkschnittstelle über n IP-Konfigurationen verfügt, muss n-1 dieser Befehle vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b43d6-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="b43d6-136">Beispiel 5: zuordnen/distanzieren einer Netzwerksicherheitsgruppe zu einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="b43d6-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="b43d6-137">Der erste Befehl ruft eine vorhandene Netzwerkschnittstelle namens NetworkInterface1 ab und speichert Sie in der $NIC-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b43d6-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="b43d6-138">Der zweite Befehl ruft eine vorhandene Netzwerksicherheitsgruppe namens MyNSG ab und speichert Sie in der $NSG-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b43d6-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="b43d6-139">Mit dem Befehl Forth wird die $NSG dem $NIC zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="b43d6-139">The forth command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="b43d6-140">Schließlich wendet der fünfte Befehl die Änderungen auf die Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="b43d6-140">Finally, the fifth command applies the changes to the Network interface.</span></span> <span data-ttu-id="b43d6-141">Um Netzwerk Sicherheitsgruppen von einer Netzwerkschnittstelle zu trennen, ersetzen Sie einfach $NSG im Befehl Forth durch $Null.</span><span class="sxs-lookup"><span data-stu-id="b43d6-141">To dissociate network security groups from a network interface, simple replace $nsg in the forth command with $null.</span></span>

## <span data-ttu-id="b43d6-142">Parameter</span><span class="sxs-lookup"><span data-stu-id="b43d6-142">PARAMETERS</span></span>

### <span data-ttu-id="b43d6-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b43d6-143">-AsJob</span></span>
<span data-ttu-id="b43d6-144">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b43d6-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b43d6-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b43d6-145">-DefaultProfile</span></span>
<span data-ttu-id="b43d6-146">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b43d6-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b43d6-147">-Network Interface</span><span class="sxs-lookup"><span data-stu-id="b43d6-147">-NetworkInterface</span></span>
<span data-ttu-id="b43d6-148">Gibt ein **Network Interface** -Objekt an, das den Zielstatus für eine Netzwerkschnittstelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="b43d6-148">Specifies a **NetworkInterface** object that represents the goal state for a network interface.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b43d6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b43d6-149">CommonParameters</span></span>
<span data-ttu-id="b43d6-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b43d6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b43d6-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b43d6-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b43d6-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b43d6-152">INPUTS</span></span>

### <span data-ttu-id="b43d6-153">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b43d6-153">PSNetworkInterface</span></span>
<span data-ttu-id="b43d6-154">Der Parameter "Network Interface" akzeptiert den Wert vom Typ "PSNetworkInterface" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b43d6-154">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="b43d6-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b43d6-155">OUTPUTS</span></span>

### <span data-ttu-id="b43d6-156">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b43d6-156">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="b43d6-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="b43d6-157">NOTES</span></span>

## <span data-ttu-id="b43d6-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b43d6-158">RELATED LINKS</span></span>

[<span data-ttu-id="b43d6-159">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b43d6-159">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="b43d6-160">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b43d6-160">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="b43d6-161">Neu – AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b43d6-161">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="b43d6-162">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b43d6-162">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)
