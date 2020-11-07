---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 73649f0f04cf1de07d991cb454b44308c4ff6443
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843551"
---
# <span data-ttu-id="5f220-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5f220-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="5f220-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f220-102">SYNOPSIS</span></span>
<span data-ttu-id="5f220-103">Konfiguriert den Zielstatus für eine Subnetz-Konfiguration in einem virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="5f220-103">Configures the goal state for a subnet configuration in a virtual network.</span></span>

## <span data-ttu-id="5f220-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f220-104">SYNTAX</span></span>

### <span data-ttu-id="5f220-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="5f220-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f220-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5f220-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f220-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f220-107">DESCRIPTION</span></span>
<span data-ttu-id="5f220-108">Das Cmdlet " **festlegen-AzVirtualNetworkSubnetConfig** " konfiguriert den Zielstatus für eine Subnetz-Konfiguration in einem virtuellen Azure-Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="5f220-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet configures the goal state for a subnet configuration in an Azure virtual network.</span></span>

## <span data-ttu-id="5f220-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f220-109">EXAMPLES</span></span>

### <span data-ttu-id="5f220-110">1: Ändern des Adresspräfix eines Subnets</span><span class="sxs-lookup"><span data-stu-id="5f220-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="5f220-111">In diesem Beispiel wird ein virtuelles Netzwerk mit einem Subnetz erstellt.</span><span class="sxs-lookup"><span data-stu-id="5f220-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="5f220-112">Dann wird Set-AzVirtualNetworkSubnetConfig aufgerufen, um die AddressPrefix des Subnets zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5f220-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="5f220-113">Dies hat nur Auswirkungen auf die speicherresidente Darstellung des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="5f220-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="5f220-114">Set-AzVirtualNetwork wird dann aufgerufen, um das virtuelle Netzwerk in Azure zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5f220-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="5f220-115">2: Hinzufügen einer Netzwerksicherheitsgruppe zu einem Subnetz</span><span class="sxs-lookup"><span data-stu-id="5f220-115">2: Add a network security group to a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="5f220-116">In diesem Beispiel wird eine Ressourcengruppe mit einem virtuellen Netzwerk erstellt, das nur ein Subnetz enthält.</span><span class="sxs-lookup"><span data-stu-id="5f220-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="5f220-117">Anschließend wird eine Netzwerksicherheitsgruppe mit einer Allow-Regel für RDP-Datenverkehr erstellt.</span><span class="sxs-lookup"><span data-stu-id="5f220-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="5f220-118">Das Set-AzVirtualNetworkSubnetConfig-Cmdlet wird verwendet, um die speicherresidente Darstellung des Frontend-Subnetzes so zu ändern, dass es auf die neu erstellte Netzwerksicherheitsgruppe verweist.</span><span class="sxs-lookup"><span data-stu-id="5f220-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="5f220-119">Das Set-AzVirtualNetwork-Cmdlet wird dann aufgerufen, um den geänderten Zustand zurück in den Dienst zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="5f220-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="5f220-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f220-120">PARAMETERS</span></span>

### <span data-ttu-id="5f220-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5f220-121">-AddressPrefix</span></span>
<span data-ttu-id="5f220-122">Gibt einen Bereich von IP-Adressen für eine Subnetz-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="5f220-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f220-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f220-123">-DefaultProfile</span></span>
<span data-ttu-id="5f220-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5f220-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f220-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5f220-125">-Name</span></span>
<span data-ttu-id="5f220-126">Gibt den Namen einer vom Cmdlet konfigurierten Subnetz-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="5f220-126">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f220-127">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5f220-127">-NetworkSecurityGroup</span></span>
<span data-ttu-id="5f220-128">Gibt ein **NetworkSecurityGroup** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="5f220-128">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f220-129">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="5f220-129">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="5f220-130">Gibt die ID einer Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="5f220-130">Specifies the ID of a network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f220-131">-Routel</span><span class="sxs-lookup"><span data-stu-id="5f220-131">-RouteTable</span></span>
<span data-ttu-id="5f220-132">Gibt das Routingtabellen Objekt an, das der Netzwerksicherheitsgruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5f220-132">Specifies the route table object that is associated with the network security group.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f220-133">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="5f220-133">-RouteTableId</span></span>
<span data-ttu-id="5f220-134">Gibt die ID des Routingtabellen Objekts an, das der Netzwerksicherheitsgruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5f220-134">Specifies the ID of the route table object that is associated with the network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f220-135">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f220-135">-ServiceEndpoint</span></span>
<span data-ttu-id="5f220-136">Dienstendpunkt Wert</span><span class="sxs-lookup"><span data-stu-id="5f220-136">Service Endpoint Value</span></span>

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

### <span data-ttu-id="5f220-137">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5f220-137">-VirtualNetwork</span></span>
<span data-ttu-id="5f220-138">Gibt das **VirtualNetwork** -Objekt an, das die Subnetz-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="5f220-138">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f220-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f220-139">CommonParameters</span></span>
<span data-ttu-id="5f220-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f220-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f220-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f220-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f220-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f220-142">INPUTS</span></span>

### <span data-ttu-id="5f220-143">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5f220-143">PSVirtualNetwork</span></span>
<span data-ttu-id="5f220-144">Der Parameter "VirtualNetwork" akzeptiert den Wert vom Typ "PSVirtualNetwork" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5f220-144">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="5f220-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f220-145">OUTPUTS</span></span>

### <span data-ttu-id="5f220-146">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5f220-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="5f220-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f220-147">NOTES</span></span>

## <span data-ttu-id="5f220-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f220-148">RELATED LINKS</span></span>

[<span data-ttu-id="5f220-149">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5f220-149">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5f220-150">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5f220-150">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5f220-151">Neu – AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5f220-151">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5f220-152">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5f220-152">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)


