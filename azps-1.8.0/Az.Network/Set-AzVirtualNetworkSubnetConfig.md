---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 4e0356f738bcc0abd52f0ec72c4c6766af8be550
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660156"
---
# <span data-ttu-id="e0553-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e0553-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="e0553-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e0553-102">SYNOPSIS</span></span>
<span data-ttu-id="e0553-103">Aktualisiert eine Subnetz-Konfiguration für ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="e0553-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="e0553-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0553-104">SYNTAX</span></span>

### <span data-ttu-id="e0553-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="e0553-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0553-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e0553-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0553-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0553-107">DESCRIPTION</span></span>
<span data-ttu-id="e0553-108">Das Cmdlet " **Satz-AzVirtualNetworkSubnetConfig** " aktualisiert eine Subnetz-Konfiguration für ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="e0553-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="e0553-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e0553-109">EXAMPLES</span></span>

### <span data-ttu-id="e0553-110">1: Ändern des Adresspräfix eines Subnets</span><span class="sxs-lookup"><span data-stu-id="e0553-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="e0553-111">In diesem Beispiel wird ein virtuelles Netzwerk mit einem Subnetz erstellt.</span><span class="sxs-lookup"><span data-stu-id="e0553-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="e0553-112">Dann wird Set-AzVirtualNetworkSubnetConfig aufgerufen, um die AddressPrefix des Subnets zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e0553-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="e0553-113">Dies hat nur Auswirkungen auf die speicherresidente Darstellung des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="e0553-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="e0553-114">Set-AzVirtualNetwork wird dann aufgerufen, um das virtuelle Netzwerk in Azure zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e0553-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="e0553-115">2: Hinzufügen einer Netzwerksicherheitsgruppe zu einem Subnetz</span><span class="sxs-lookup"><span data-stu-id="e0553-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="e0553-116">In diesem Beispiel wird eine Ressourcengruppe mit einem virtuellen Netzwerk erstellt, das nur ein Subnetz enthält.</span><span class="sxs-lookup"><span data-stu-id="e0553-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="e0553-117">Anschließend wird eine Netzwerksicherheitsgruppe mit einer Allow-Regel für RDP-Datenverkehr erstellt.</span><span class="sxs-lookup"><span data-stu-id="e0553-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="e0553-118">Das Set-AzVirtualNetworkSubnetConfig-Cmdlet wird verwendet, um die speicherresidente Darstellung des Frontend-Subnetzes so zu ändern, dass es auf die neu erstellte Netzwerksicherheitsgruppe verweist.</span><span class="sxs-lookup"><span data-stu-id="e0553-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="e0553-119">Das Set-AzVirtualNetwork-Cmdlet wird dann aufgerufen, um den geänderten Zustand zurück in den Dienst zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="e0553-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="e0553-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0553-120">PARAMETERS</span></span>

### <span data-ttu-id="e0553-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e0553-121">-AddressPrefix</span></span>
<span data-ttu-id="e0553-122">Gibt einen Bereich von IP-Adressen für eine Subnetz-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="e0553-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0553-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0553-123">-DefaultProfile</span></span>
<span data-ttu-id="e0553-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e0553-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0553-125">-Delegation</span><span class="sxs-lookup"><span data-stu-id="e0553-125">-Delegation</span></span>
<span data-ttu-id="e0553-126">Liste der Dienste, die über die Berechtigung zum Ausführen von Vorgängen in diesem Subnetz verfügen</span><span class="sxs-lookup"><span data-stu-id="e0553-126">List of services that have permission to perform operations on this subnet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSDelegation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0553-127">-Name</span><span class="sxs-lookup"><span data-stu-id="e0553-127">-Name</span></span>
<span data-ttu-id="e0553-128">Gibt den Namen einer vom Cmdlet konfigurierten Subnetz-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="e0553-128">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="e0553-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e0553-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="e0553-130">Gibt ein **NetworkSecurityGroup** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e0553-130">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0553-131">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e0553-131">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="e0553-132">Gibt die ID einer Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="e0553-132">Specifies the ID of a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0553-133">-Routel</span><span class="sxs-lookup"><span data-stu-id="e0553-133">-RouteTable</span></span>
<span data-ttu-id="e0553-134">Gibt das Routingtabellen Objekt an, das der Netzwerksicherheitsgruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e0553-134">Specifies the route table object that is associated with the network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0553-135">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="e0553-135">-RouteTableId</span></span>
<span data-ttu-id="e0553-136">Gibt die ID des Routingtabellen Objekts an, das der Netzwerksicherheitsgruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e0553-136">Specifies the ID of the route table object that is associated with the network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0553-137">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e0553-137">-ServiceEndpoint</span></span>
<span data-ttu-id="e0553-138">Dienstendpunkt Wert</span><span class="sxs-lookup"><span data-stu-id="e0553-138">Service Endpoint Value</span></span>

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

### <span data-ttu-id="e0553-139">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e0553-139">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="e0553-140">Dienstendpunkt Richtlinien</span><span class="sxs-lookup"><span data-stu-id="e0553-140">Service Endpoint Policies</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0553-141">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e0553-141">-VirtualNetwork</span></span>
<span data-ttu-id="e0553-142">Gibt das **VirtualNetwork** -Objekt an, das die Subnetz-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="e0553-142">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0553-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0553-143">CommonParameters</span></span>
<span data-ttu-id="e0553-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0553-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0553-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0553-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0553-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e0553-146">INPUTS</span></span>

### <span data-ttu-id="e0553-147">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e0553-147">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="e0553-148">System. String</span><span class="sxs-lookup"><span data-stu-id="e0553-148">System.String</span></span>

### <span data-ttu-id="e0553-149">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e0553-149">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="e0553-150">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="e0553-150">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="e0553-151">System. String []</span><span class="sxs-lookup"><span data-stu-id="e0553-151">System.String[]</span></span>

### <span data-ttu-id="e0553-152">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="e0553-152">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="e0553-153">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="e0553-153">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="e0553-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e0553-154">OUTPUTS</span></span>

### <span data-ttu-id="e0553-155">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e0553-155">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="e0553-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="e0553-156">NOTES</span></span>

## <span data-ttu-id="e0553-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e0553-157">RELATED LINKS</span></span>

[<span data-ttu-id="e0553-158">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e0553-158">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e0553-159">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e0553-159">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e0553-160">Neu – AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e0553-160">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e0553-161">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e0553-161">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)
