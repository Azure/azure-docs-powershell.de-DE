---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 16f73c81c13740037131e47d03945d475db12ee9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841244"
---
# <span data-ttu-id="a9ffa-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a9ffa-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="a9ffa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9ffa-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ffa-103">Erstellt eine virtuelle Netzwerk-Subnetz-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a9ffa-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="a9ffa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9ffa-104">SYNTAX</span></span>

### <span data-ttu-id="a9ffa-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9ffa-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9ffa-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a9ffa-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9ffa-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9ffa-107">DESCRIPTION</span></span>
<span data-ttu-id="a9ffa-108">**Das Cmdlet New-AzVirtualNetworkSubnetConfig** erstellt eine virtuelle Netzwerk-Subnetz-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a9ffa-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="a9ffa-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9ffa-109">EXAMPLES</span></span>

### <span data-ttu-id="a9ffa-110">1: Erstellen eines virtuellen Netzwerks mit zwei Subnetzen und einer Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="a9ffa-110">1:  Create a virtual network with two subnets and a network security group</span></span>
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

<span data-ttu-id="a9ffa-111">In diesem Beispiel werden zwei neue Subnetz-Konfigurationen mithilfe des New-AzVirtualSubnetConfig-Cmdlets erstellt und dann zum Erstellen eines virtuellen Netzwerks verwendet.</span><span class="sxs-lookup"><span data-stu-id="a9ffa-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="a9ffa-112">Die New-AzVirtualSubnetConfig Vorlage erstellt nur eine speicherresidente Darstellung des Subnets.</span><span class="sxs-lookup"><span data-stu-id="a9ffa-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="a9ffa-113">In diesem Beispiel hat die frontendSubnet CIDR 10.0.1.0/24 und verweist auf eine Netzwerksicherheitsgruppe, die den Zugriff auf RDP ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="a9ffa-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="a9ffa-114">BackendSubnet hat CIDR 10.0.2.0/24 und verweist auf die gleiche Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a9ffa-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="a9ffa-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9ffa-115">PARAMETERS</span></span>

### <span data-ttu-id="a9ffa-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a9ffa-116">-AddressPrefix</span></span>
<span data-ttu-id="a9ffa-117">Gibt einen Bereich von IP-Adressen für eine Subnetz-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="a9ffa-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="a9ffa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9ffa-118">-DefaultProfile</span></span>
<span data-ttu-id="a9ffa-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9ffa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9ffa-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a9ffa-120">-Name</span></span>
<span data-ttu-id="a9ffa-121">Gibt den Namen der zu erstellende Subnet-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="a9ffa-121">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="a9ffa-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a9ffa-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="a9ffa-123">Gibt ein NetworkSecurityGroup-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a9ffa-123">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="a9ffa-124">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a9ffa-124">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="a9ffa-125">Gibt die ID einer Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="a9ffa-125">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="a9ffa-126">-Routel</span><span class="sxs-lookup"><span data-stu-id="a9ffa-126">-RouteTable</span></span>
<span data-ttu-id="a9ffa-127">Gibt die Routentabelle an, die der Subnet-Konfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a9ffa-127">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="a9ffa-128">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="a9ffa-128">-RouteTableId</span></span>
<span data-ttu-id="a9ffa-129">Gibt die ID der Routingtabelle an, die der Subnetz-Konfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a9ffa-129">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="a9ffa-130">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a9ffa-130">-ServiceEndpoint</span></span>
<span data-ttu-id="a9ffa-131">Dienstendpunkt Wert</span><span class="sxs-lookup"><span data-stu-id="a9ffa-131">Service Endpoint Value</span></span>

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

### <span data-ttu-id="a9ffa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ffa-132">CommonParameters</span></span>
<span data-ttu-id="a9ffa-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9ffa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ffa-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9ffa-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ffa-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9ffa-135">INPUTS</span></span>

## <span data-ttu-id="a9ffa-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9ffa-136">OUTPUTS</span></span>

### <span data-ttu-id="a9ffa-137">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="a9ffa-137">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="a9ffa-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9ffa-138">NOTES</span></span>

## <span data-ttu-id="a9ffa-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9ffa-139">RELATED LINKS</span></span>

[<span data-ttu-id="a9ffa-140">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a9ffa-140">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a9ffa-141">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a9ffa-141">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a9ffa-142">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a9ffa-142">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a9ffa-143">Satz-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a9ffa-143">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


