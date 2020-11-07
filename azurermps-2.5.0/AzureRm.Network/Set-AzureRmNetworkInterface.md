---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 978db7296b9789f738f5b277a4bf3731803fdcd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850304"
---
# <span data-ttu-id="b76f4-101">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b76f4-101">Set-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="b76f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b76f4-102">SYNOPSIS</span></span>
<span data-ttu-id="b76f4-103">Legt den Zielstatus für eine Netzwerkschnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="b76f4-103">Sets the goal state for a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b76f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b76f4-104">SYNTAX</span></span>

```
Set-AzureRmNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b76f4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b76f4-105">DESCRIPTION</span></span>
<span data-ttu-id="b76f4-106">Das **Set-AzureRmNetworkInterface** legt den Zielstatus für eine Azure-Netzwerkschnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="b76f4-106">The **Set-AzureRmNetworkInterface** sets the goal state for an Azure network interface.</span></span>

## <span data-ttu-id="b76f4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b76f4-107">EXAMPLES</span></span>

### <span data-ttu-id="b76f4-108">Beispiel 1: Konfigurieren einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="b76f4-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzureRmNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="b76f4-109">In diesem Beispiel wird eine Netzwerkschnittstelle konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="b76f4-109">This example configures a network interface.</span></span>
<span data-ttu-id="b76f4-110">Der erste Befehl ruft eine Netzwerkschnittstelle mit dem Namen NetworkInterface1 in der Ressourcengruppe ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="b76f4-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="b76f4-111">Der zweite Befehl legt die private IP-Adresse der IP-Konfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="b76f4-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="b76f4-112">Der dritte Befehl legt die private IP-Zuordnungsmethode auf static fest.</span><span class="sxs-lookup"><span data-stu-id="b76f4-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="b76f4-113">Der vierte Befehl legt ein Tag auf der Netzwerkschnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="b76f4-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="b76f4-114">Der fünfte Befehl verwendet die in der $NIC-Variablen gespeicherten Informationen, um die Netzwerkschnittstelle einzurichten.</span><span class="sxs-lookup"><span data-stu-id="b76f4-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="b76f4-115">Beispiel 2: Ändern der DNS-Einstellungen auf einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="b76f4-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="b76f4-116">Der erste Befehl ruft eine Netzwerkschnittstelle mit dem Namen NetworkInterface1 ab, die innerhalb der Ressourcengruppen-ResourceGroup1 vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b76f4-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="b76f4-117">Mit dem zweiten Befehl wird dieser Schnittstelle der DNS-Server 192.168.1.100 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b76f4-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="b76f4-118">Der dritte Befehl wendet diese Änderungen auf die Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="b76f4-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="b76f4-119">Wenn Sie einen DNS-Server entfernen möchten, folgen Sie den oben aufgeführten Befehlen, ersetzen Sie aber ". "Mit" hinzufügen. Remove "im zweiten Befehl.</span><span class="sxs-lookup"><span data-stu-id="b76f4-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="b76f4-120">Beispiel 3: Aktivieren von IP-Forwading auf einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="b76f4-120">Example 3: Enable IP forwading on a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="b76f4-121">Der erste Befehl ruft eine vorhandene Netzwerkschnittstelle namens NetworkInterface1 ab und speichert Sie in der $NIC-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b76f4-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="b76f4-122">Mit dem zweiten Befehl wird der Wert für die IP-Weiterleitung in true geändert.</span><span class="sxs-lookup"><span data-stu-id="b76f4-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="b76f4-123">Schließlich wendet der dritte Befehl die Änderungen auf die Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="b76f4-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="b76f4-124">Wenn Sie die IP-Weiterleitung auf einer Netzwerkschnittstelle deaktivieren möchten, folgen Sie dem Beispiel Beispiel, aber stellen Sie sicher, dass Sie den zweiten Befehl in "$Nic" ändern. EnableIPForwarding = 0 ".</span><span class="sxs-lookup"><span data-stu-id="b76f4-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="b76f4-125">Beispiel 4: Ändern des Subnets einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="b76f4-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzureRmVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzureRmVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="b76f4-126">Der erste Befehl ruft die Netzwerkschnittstellen-NetworkInterface1 ab und speichert Sie in der $NIC-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b76f4-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="b76f4-127">Der zweite Befehl ruft das virtuelle Netzwerk ab, dem das Subnetz zugeordnet ist, dem die Netzwerkschnittstelle zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b76f4-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="b76f4-128">Der zweite Befehl ruft das Subnetz ab und speichert es in der Variablen $Subnet 2.</span><span class="sxs-lookup"><span data-stu-id="b76f4-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="b76f4-129">Der dritte Befehl verknüpfte die primäre private IP-Adresse der Netzwerkschnittstelle mit dem neuen Subnetz.</span><span class="sxs-lookup"><span data-stu-id="b76f4-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="b76f4-130">Schließlich hat der letzte Befehl diese Änderungen auf der Netzwerkschnittstelle übernommen.</span><span class="sxs-lookup"><span data-stu-id="b76f4-130">Finally the last command applied these changes on the network interface.</span></span>

>[!NOTE] 
><span data-ttu-id="b76f4-131">Die IP-Konfigurationen müssen dynamisch sein, bevor Sie das Subnetz ändern können.</span><span class="sxs-lookup"><span data-stu-id="b76f4-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="b76f4-132">Wenn Sie über statische IP-Konfigurationen verfügen, wechseln Sie dann zu Dynamic, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="b76f4-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 

>[!NOTE]
><span data-ttu-id="b76f4-133">Wenn die Netzwerkschnittstelle über mehrere IP-Konfigurationen verfügt, muss der Befehl Forth für alle diese IP-Konfigurationen ausgeführt werden, bevor der endgültige Set-AzureRmNetworkInterface Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b76f4-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzureRmNetworkInterface command is executed.</span></span> <span data-ttu-id="b76f4-134">Dies kann wie im Befehl Forth erfolgen, aber durch Ersetzen von "0" durch die entsprechende Zahl.</span><span class="sxs-lookup"><span data-stu-id="b76f4-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="b76f4-135">Wenn eine Netzwerkschnittstelle über n IP-Konfigurationen verfügt, muss n-1 dieser Befehle vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b76f4-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="b76f4-136">Beispiel 5: zuordnen/distanzieren einer Netzwerksicherheitsgruppe zu einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="b76f4-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="b76f4-137">Der erste Befehl ruft eine vorhandene Netzwerkschnittstelle namens NetworkInterface1 ab und speichert Sie in der $NIC-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b76f4-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="b76f4-138">Der zweite Befehl ruft eine vorhandene Netzwerksicherheitsgruppe namens MyNSG ab und speichert Sie in der $NSG-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b76f4-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="b76f4-139">Mit dem Befehl Forth wird die $NSG dem $NIC zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="b76f4-139">The forth command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="b76f4-140">Schließlich wendet der fünfte Befehl die Änderungen auf die Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="b76f4-140">Finally, the fifth command applies the changes to the Network interface.</span></span> <span data-ttu-id="b76f4-141">Um Netzwerk Sicherheitsgruppen von einer Netzwerkschnittstelle zu trennen, ersetzen Sie einfach $NSG im Befehl Forth durch $Null.</span><span class="sxs-lookup"><span data-stu-id="b76f4-141">To dissociate network security groups from a network interface, simple replace $nsg in the forth command with $null.</span></span>

## <span data-ttu-id="b76f4-142">Parameter</span><span class="sxs-lookup"><span data-stu-id="b76f4-142">PARAMETERS</span></span>

### <span data-ttu-id="b76f4-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b76f4-143">-AsJob</span></span>
<span data-ttu-id="b76f4-144">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b76f4-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b76f4-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b76f4-145">-DefaultProfile</span></span>
<span data-ttu-id="b76f4-146">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b76f4-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b76f4-147">-Network Interface</span><span class="sxs-lookup"><span data-stu-id="b76f4-147">-NetworkInterface</span></span>
<span data-ttu-id="b76f4-148">Gibt ein **Network Interface** -Objekt an, das den Zielstatus für eine Netzwerkschnittstelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="b76f4-148">Specifies a **NetworkInterface** object that represents the goal state for a network interface.</span></span>

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

### <span data-ttu-id="b76f4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b76f4-149">CommonParameters</span></span>
<span data-ttu-id="b76f4-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b76f4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b76f4-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b76f4-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b76f4-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b76f4-152">INPUTS</span></span>

### <span data-ttu-id="b76f4-153">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b76f4-153">PSNetworkInterface</span></span>
<span data-ttu-id="b76f4-154">Der Parameter "Network Interface" akzeptiert den Wert vom Typ "PSNetworkInterface" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b76f4-154">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="b76f4-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b76f4-155">OUTPUTS</span></span>

### <span data-ttu-id="b76f4-156">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b76f4-156">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="b76f4-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="b76f4-157">NOTES</span></span>

## <span data-ttu-id="b76f4-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b76f4-158">RELATED LINKS</span></span>

[<span data-ttu-id="b76f4-159">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b76f4-159">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="b76f4-160">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b76f4-160">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="b76f4-161">Neu – AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b76f4-161">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="b76f4-162">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b76f4-162">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)
