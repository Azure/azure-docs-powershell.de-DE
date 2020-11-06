---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 37202e0e852f0171ce48c2c3d61d13151b05148c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480301"
---
# <span data-ttu-id="e9f3c-101">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e9f3c-101">New-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="e9f3c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e9f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="e9f3c-103">Erstellt eine virtuelle Netzwerk-Subnetz-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e9f3c-103">Creates a virtual network subnet configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9f3c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9f3c-104">SYNTAX</span></span>

### <span data-ttu-id="e9f3c-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="e9f3c-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9f3c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e9f3c-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9f3c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9f3c-107">DESCRIPTION</span></span>
<span data-ttu-id="e9f3c-108">**Das Cmdlet New-AzureRmVirtualNetworkSubnetConfig** erstellt eine virtuelle Netzwerk-Subnetz-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e9f3c-108">**The New-AzureRmVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="e9f3c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9f3c-109">EXAMPLES</span></span>

### <span data-ttu-id="e9f3c-110">1: Erstellen eines virtuellen Netzwerks mit zwei Subnetzen und einer Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="e9f3c-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="e9f3c-111">In diesem Beispiel werden zwei neue Subnetz-Konfigurationen mithilfe des New-AzureRmVirtualSubnetConfig-Cmdlets erstellt und dann zum Erstellen eines virtuellen Netzwerks verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9f3c-111">This example creates two new subnet configurations using the New-AzureRmVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="e9f3c-112">Die New-AzureRmVirtualSubnetConfig Vorlage erstellt nur eine speicherresidente Darstellung des Subnets.</span><span class="sxs-lookup"><span data-stu-id="e9f3c-112">The New-AzureRmVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="e9f3c-113">In diesem Beispiel hat die frontendSubnet CIDR 10.0.1.0/24 und verweist auf eine Netzwerksicherheitsgruppe, die den Zugriff auf RDP ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="e9f3c-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="e9f3c-114">BackendSubnet hat CIDR 10.0.2.0/24 und verweist auf die gleiche Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e9f3c-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="e9f3c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9f3c-115">PARAMETERS</span></span>

### <span data-ttu-id="e9f3c-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e9f3c-116">-AddressPrefix</span></span>
<span data-ttu-id="e9f3c-117">Gibt einen Bereich von IP-Adressen für eine Subnetz-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="e9f3c-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f3c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9f3c-118">-DefaultProfile</span></span>
<span data-ttu-id="e9f3c-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e9f3c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f3c-120">-Delegation</span><span class="sxs-lookup"><span data-stu-id="e9f3c-120">-Delegation</span></span>
<span data-ttu-id="e9f3c-121">Liste der Dienste, die über die Berechtigung zum Ausführen von Vorgängen in diesem Subnetz verfügen</span><span class="sxs-lookup"><span data-stu-id="e9f3c-121">List of services that have permission to perform operations on this subnet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9f3c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e9f3c-122">-Name</span></span>
<span data-ttu-id="e9f3c-123">Gibt den Namen der zu erstellende Subnet-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="e9f3c-123">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="e9f3c-124">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e9f3c-124">-NetworkSecurityGroup</span></span>
<span data-ttu-id="e9f3c-125">Gibt ein NetworkSecurityGroup-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e9f3c-125">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="e9f3c-126">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e9f3c-126">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="e9f3c-127">Gibt die ID einer Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="e9f3c-127">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="e9f3c-128">-Routel</span><span class="sxs-lookup"><span data-stu-id="e9f3c-128">-RouteTable</span></span>
<span data-ttu-id="e9f3c-129">Gibt die Routentabelle an, die der Subnet-Konfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e9f3c-129">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="e9f3c-130">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="e9f3c-130">-RouteTableId</span></span>
<span data-ttu-id="e9f3c-131">Gibt die ID der Routingtabelle an, die der Subnetz-Konfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e9f3c-131">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="e9f3c-132">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e9f3c-132">-ServiceEndpoint</span></span>
<span data-ttu-id="e9f3c-133">Dienstendpunkt Wert</span><span class="sxs-lookup"><span data-stu-id="e9f3c-133">Service Endpoint Value</span></span>

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

### <span data-ttu-id="e9f3c-134">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e9f3c-134">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="e9f3c-135">Dienstendpunkt Richtlinien</span><span class="sxs-lookup"><span data-stu-id="e9f3c-135">Service Endpoint Policies</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9f3c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9f3c-136">CommonParameters</span></span>
<span data-ttu-id="e9f3c-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9f3c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9f3c-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9f3c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9f3c-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e9f3c-139">INPUTS</span></span>

### <span data-ttu-id="e9f3c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e9f3c-140">System.String</span></span>

### <span data-ttu-id="e9f3c-141">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e9f3c-141">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="e9f3c-142">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="e9f3c-142">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="e9f3c-143">System. Collections. Generic. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e9f3c-143">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e9f3c-144">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e9f3c-144">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e9f3c-145">System. Collections. Generic. List ' 1 [[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e9f3c-145">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e9f3c-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e9f3c-146">OUTPUTS</span></span>

### <span data-ttu-id="e9f3c-147">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="e9f3c-147">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="e9f3c-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="e9f3c-148">NOTES</span></span>

## <span data-ttu-id="e9f3c-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e9f3c-149">RELATED LINKS</span></span>

[<span data-ttu-id="e9f3c-150">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e9f3c-150">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e9f3c-151">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e9f3c-151">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e9f3c-152">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e9f3c-152">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e9f3c-153">Satz-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e9f3c-153">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


