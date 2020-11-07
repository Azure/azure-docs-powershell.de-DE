---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 836973c4b1d95445d905bb41f489c48136e12f6d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660463"
---
# <span data-ttu-id="154fe-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="154fe-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="154fe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="154fe-102">SYNOPSIS</span></span>
<span data-ttu-id="154fe-103">Erstellt eine virtuelle Netzwerk-Subnetz-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="154fe-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="154fe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="154fe-104">SYNTAX</span></span>

### <span data-ttu-id="154fe-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="154fe-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="154fe-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="154fe-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="154fe-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="154fe-107">DESCRIPTION</span></span>
<span data-ttu-id="154fe-108">**Das Cmdlet New-AzVirtualNetworkSubnetConfig** erstellt eine virtuelle Netzwerk-Subnetz-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="154fe-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="154fe-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="154fe-109">EXAMPLES</span></span>

### <span data-ttu-id="154fe-110">1: Erstellen eines virtuellen Netzwerks mit zwei Subnetzen und einer Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="154fe-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="154fe-111">In diesem Beispiel werden zwei neue Subnetz-Konfigurationen mithilfe des New-AzVirtualSubnetConfig-Cmdlets erstellt und dann zum Erstellen eines virtuellen Netzwerks verwendet.</span><span class="sxs-lookup"><span data-stu-id="154fe-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="154fe-112">Die New-AzVirtualSubnetConfig Vorlage erstellt nur eine speicherresidente Darstellung des Subnets.</span><span class="sxs-lookup"><span data-stu-id="154fe-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="154fe-113">In diesem Beispiel hat die frontendSubnet CIDR 10.0.1.0/24 und verweist auf eine Netzwerksicherheitsgruppe, die den Zugriff auf RDP ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="154fe-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="154fe-114">BackendSubnet hat CIDR 10.0.2.0/24 und verweist auf die gleiche Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="154fe-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="154fe-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="154fe-115">PARAMETERS</span></span>

### <span data-ttu-id="154fe-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="154fe-116">-AddressPrefix</span></span>
<span data-ttu-id="154fe-117">Gibt einen Bereich von IP-Adressen für eine Subnetz-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="154fe-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="154fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="154fe-118">-DefaultProfile</span></span>
<span data-ttu-id="154fe-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="154fe-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="154fe-120">-Delegation</span><span class="sxs-lookup"><span data-stu-id="154fe-120">-Delegation</span></span>
<span data-ttu-id="154fe-121">Liste der Dienste, die über die Berechtigung zum Ausführen von Vorgängen in diesem Subnetz verfügen</span><span class="sxs-lookup"><span data-stu-id="154fe-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="154fe-122">-Name</span><span class="sxs-lookup"><span data-stu-id="154fe-122">-Name</span></span>
<span data-ttu-id="154fe-123">Gibt den Namen der zu erstellende Subnet-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="154fe-123">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="154fe-124">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="154fe-124">-NetworkSecurityGroup</span></span>
<span data-ttu-id="154fe-125">Gibt ein NetworkSecurityGroup-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="154fe-125">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="154fe-126">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="154fe-126">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="154fe-127">Gibt die ID einer Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="154fe-127">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="154fe-128">-Routel</span><span class="sxs-lookup"><span data-stu-id="154fe-128">-RouteTable</span></span>
<span data-ttu-id="154fe-129">Gibt die Routentabelle an, die der Subnet-Konfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="154fe-129">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="154fe-130">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="154fe-130">-RouteTableId</span></span>
<span data-ttu-id="154fe-131">Gibt die ID der Routingtabelle an, die der Subnetz-Konfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="154fe-131">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="154fe-132">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="154fe-132">-ServiceEndpoint</span></span>
<span data-ttu-id="154fe-133">Dienstendpunkt Wert</span><span class="sxs-lookup"><span data-stu-id="154fe-133">Service Endpoint Value</span></span>

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

### <span data-ttu-id="154fe-134">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="154fe-134">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="154fe-135">Dienstendpunkt Richtlinien</span><span class="sxs-lookup"><span data-stu-id="154fe-135">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="154fe-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="154fe-136">CommonParameters</span></span>
<span data-ttu-id="154fe-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="154fe-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="154fe-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="154fe-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="154fe-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="154fe-139">INPUTS</span></span>

### <span data-ttu-id="154fe-140">System. String</span><span class="sxs-lookup"><span data-stu-id="154fe-140">System.String</span></span>

### <span data-ttu-id="154fe-141">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="154fe-141">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="154fe-142">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="154fe-142">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="154fe-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="154fe-143">System.String[]</span></span>

### <span data-ttu-id="154fe-144">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="154fe-144">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="154fe-145">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="154fe-145">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="154fe-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="154fe-146">OUTPUTS</span></span>

### <span data-ttu-id="154fe-147">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="154fe-147">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="154fe-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="154fe-148">NOTES</span></span>

## <span data-ttu-id="154fe-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="154fe-149">RELATED LINKS</span></span>

[<span data-ttu-id="154fe-150">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="154fe-150">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="154fe-151">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="154fe-151">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="154fe-152">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="154fe-152">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="154fe-153">Satz-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="154fe-153">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
