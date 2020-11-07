---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworksubnetconfig
schema: 2.0.0
ms.openlocfilehash: b13a06fbc2bd7f071888dcd0504d3e1963cbedd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850291"
---
# <span data-ttu-id="4bbab-101">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4bbab-101">Set-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="4bbab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4bbab-102">SYNOPSIS</span></span>
<span data-ttu-id="4bbab-103">Konfiguriert den Zielstatus für eine Subnetz-Konfiguration in einem virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="4bbab-103">Configures the goal state for a subnet configuration in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bbab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bbab-104">SYNTAX</span></span>

### <span data-ttu-id="4bbab-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="4bbab-105">SetByResource (Default)</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bbab-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4bbab-106">SetByResourceId</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bbab-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4bbab-107">DESCRIPTION</span></span>
<span data-ttu-id="4bbab-108">Das Cmdlet " **festlegen-AzureRmVirtualNetworkSubnetConfig** " konfiguriert den Zielstatus für eine Subnetz-Konfiguration in einem virtuellen Azure-Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="4bbab-108">The **Set-AzureRmVirtualNetworkSubnetConfig** cmdlet configures the goal state for a subnet configuration in an Azure virtual network.</span></span>

## <span data-ttu-id="4bbab-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4bbab-109">EXAMPLES</span></span>

### <span data-ttu-id="4bbab-110">1: Ändern des Adresspräfix eines Subnets</span><span class="sxs-lookup"><span data-stu-id="4bbab-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="4bbab-111">In diesem Beispiel wird ein virtuelles Netzwerk mit einem Subnetz erstellt.</span><span class="sxs-lookup"><span data-stu-id="4bbab-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="4bbab-112">Dann wird Set-AzureRmVirtualNetworkSubnetConfig aufgerufen, um die AddressPrefix des Subnets zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4bbab-112">Then is calls Set-AzureRmVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="4bbab-113">Dies hat nur Auswirkungen auf die speicherresidente Darstellung des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="4bbab-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="4bbab-114">Set-AzureRmVirtualNetwork wird dann aufgerufen, um das virtuelle Netzwerk in Azure zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4bbab-114">Set-AzureRmVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="4bbab-115">2: Hinzufügen einer Netzwerksicherheitsgruppe zu einem Subnetz</span><span class="sxs-lookup"><span data-stu-id="4bbab-115">2: Add a network security group to a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="4bbab-116">In diesem Beispiel wird eine Ressourcengruppe mit einem virtuellen Netzwerk erstellt, das nur ein Subnetz enthält.</span><span class="sxs-lookup"><span data-stu-id="4bbab-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="4bbab-117">Anschließend wird eine Netzwerksicherheitsgruppe mit einer Allow-Regel für RDP-Datenverkehr erstellt.</span><span class="sxs-lookup"><span data-stu-id="4bbab-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="4bbab-118">Das Set-AzureRmVirtualNetworkSubnetConfig-Cmdlet wird verwendet, um die speicherresidente Darstellung des Frontend-Subnetzes so zu ändern, dass es auf die neu erstellte Netzwerksicherheitsgruppe verweist.</span><span class="sxs-lookup"><span data-stu-id="4bbab-118">The Set-AzureRmVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="4bbab-119">Das Set-AzureRmVirtualNetwork-Cmdlet wird dann aufgerufen, um den geänderten Zustand zurück in den Dienst zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="4bbab-119">The Set-AzureRmVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="4bbab-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bbab-120">PARAMETERS</span></span>

### <span data-ttu-id="4bbab-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4bbab-121">-AddressPrefix</span></span>
<span data-ttu-id="4bbab-122">Gibt einen Bereich von IP-Adressen für eine Subnetz-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="4bbab-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="4bbab-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bbab-123">-DefaultProfile</span></span>
<span data-ttu-id="4bbab-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4bbab-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bbab-125">-Name</span><span class="sxs-lookup"><span data-stu-id="4bbab-125">-Name</span></span>
<span data-ttu-id="4bbab-126">Gibt den Namen einer vom Cmdlet konfigurierten Subnetz-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="4bbab-126">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="4bbab-127">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4bbab-127">-NetworkSecurityGroup</span></span>
<span data-ttu-id="4bbab-128">Gibt ein **NetworkSecurityGroup** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4bbab-128">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="4bbab-129">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="4bbab-129">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="4bbab-130">Gibt die ID einer Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="4bbab-130">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="4bbab-131">-Routel</span><span class="sxs-lookup"><span data-stu-id="4bbab-131">-RouteTable</span></span>
<span data-ttu-id="4bbab-132">Gibt das Routingtabellen Objekt an, das der Netzwerksicherheitsgruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4bbab-132">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="4bbab-133">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="4bbab-133">-RouteTableId</span></span>
<span data-ttu-id="4bbab-134">Gibt die ID des Routingtabellen Objekts an, das der Netzwerksicherheitsgruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4bbab-134">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="4bbab-135">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4bbab-135">-ServiceEndpoint</span></span>
<span data-ttu-id="4bbab-136">Dienstendpunkt Wert</span><span class="sxs-lookup"><span data-stu-id="4bbab-136">Service Endpoint Value</span></span>

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

### <span data-ttu-id="4bbab-137">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4bbab-137">-VirtualNetwork</span></span>
<span data-ttu-id="4bbab-138">Gibt das **VirtualNetwork** -Objekt an, das die Subnetz-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="4bbab-138">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="4bbab-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bbab-139">CommonParameters</span></span>
<span data-ttu-id="4bbab-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bbab-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bbab-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bbab-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bbab-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4bbab-142">INPUTS</span></span>

### <span data-ttu-id="4bbab-143">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4bbab-143">PSVirtualNetwork</span></span>
<span data-ttu-id="4bbab-144">Der Parameter "VirtualNetwork" akzeptiert den Wert vom Typ "PSVirtualNetwork" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4bbab-144">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="4bbab-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4bbab-145">OUTPUTS</span></span>

### <span data-ttu-id="4bbab-146">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4bbab-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="4bbab-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="4bbab-147">NOTES</span></span>

## <span data-ttu-id="4bbab-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4bbab-148">RELATED LINKS</span></span>

[<span data-ttu-id="4bbab-149">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4bbab-149">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4bbab-150">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4bbab-150">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4bbab-151">Neu – AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4bbab-151">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4bbab-152">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4bbab-152">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)


