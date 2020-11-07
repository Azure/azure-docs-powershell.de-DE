---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 01116d3a2ad2636776fe29a0e36e34568624f2c9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841787"
---
# <span data-ttu-id="b0fa9-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b0fa9-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="b0fa9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b0fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="b0fa9-103">Fügt eine Subnetz-Konfiguration zu einem virtuellen Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="b0fa9-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="b0fa9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0fa9-104">SYNTAX</span></span>

### <span data-ttu-id="b0fa9-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="b0fa9-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0fa9-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b0fa9-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0fa9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0fa9-107">DESCRIPTION</span></span>
<span data-ttu-id="b0fa9-108">Das Cmdlet **Add-AzVirtualNetworkSubnetConfig** fügt eine Subnetz-Konfiguration zu einem vorhandenen Azure-virtuellen Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="b0fa9-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="b0fa9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0fa9-109">EXAMPLES</span></span>

### <span data-ttu-id="b0fa9-110">1: Hinzufügen eines Subnetzes zu einem vorhandenen virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="b0fa9-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="b0fa9-111">In diesem Beispiel wird zunächst eine Ressourcengruppe als Container der zu erstellende Ressourcen erstellt.</span><span class="sxs-lookup"><span data-stu-id="b0fa9-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="b0fa9-112">Anschließend wird eine Subnetz-Konfiguration erstellt und zum Erstellen eines virtuellen Netzwerks verwendet.</span><span class="sxs-lookup"><span data-stu-id="b0fa9-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="b0fa9-113">Die Add-AzVirtualNetworkSubnetConfig wird dann verwendet, um der speicherresidenten Darstellung des virtuellen Netzwerks ein Subnetz hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b0fa9-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="b0fa9-114">Mit dem Befehl Set-AzVirtualNetwork wird das vorhandene virtuelle Netzwerk mit dem neuen Subnetz aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b0fa9-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

## <span data-ttu-id="b0fa9-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0fa9-115">PARAMETERS</span></span>

### <span data-ttu-id="b0fa9-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b0fa9-116">-AddressPrefix</span></span>
<span data-ttu-id="b0fa9-117">Gibt einen Bereich von IP-Adressen für eine Subnetz-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="b0fa9-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="b0fa9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0fa9-118">-DefaultProfile</span></span>
<span data-ttu-id="b0fa9-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b0fa9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0fa9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b0fa9-120">-Name</span></span>
<span data-ttu-id="b0fa9-121">Gibt den Namen der hinzuzufügenden Subnet-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="b0fa9-121">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="b0fa9-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b0fa9-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="b0fa9-123">Gibt ein **NetworkSecurityGroup** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b0fa9-123">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="b0fa9-124">Mit diesem Cmdlet wird dem Objekt, das dieser Parameter angibt, eine virtuelle Netzwerk-Subnetz-Konfiguration hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b0fa9-124">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="b0fa9-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b0fa9-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="b0fa9-126">Gibt die ID einer Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="b0fa9-126">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="b0fa9-127">-Routel</span><span class="sxs-lookup"><span data-stu-id="b0fa9-127">-RouteTable</span></span>
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

### <span data-ttu-id="b0fa9-128">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="b0fa9-128">-RouteTableId</span></span>
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

### <span data-ttu-id="b0fa9-129">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0fa9-129">-ServiceEndpoint</span></span>
<span data-ttu-id="b0fa9-130">Dienstendpunkt Wert</span><span class="sxs-lookup"><span data-stu-id="b0fa9-130">Service Endpoint Value</span></span>

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

### <span data-ttu-id="b0fa9-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b0fa9-131">-VirtualNetwork</span></span>
<span data-ttu-id="b0fa9-132">Gibt das **VirtualNetwork** -Objekt an, dem eine Subnetz-Konfiguration hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0fa9-132">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="b0fa9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0fa9-133">CommonParameters</span></span>
<span data-ttu-id="b0fa9-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0fa9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0fa9-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0fa9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0fa9-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b0fa9-136">INPUTS</span></span>

### <span data-ttu-id="b0fa9-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b0fa9-137">PSVirtualNetwork</span></span>
<span data-ttu-id="b0fa9-138">Der Parameter "VirtualNetwork" akzeptiert den Wert vom Typ "PSVirtualNetwork" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b0fa9-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="b0fa9-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b0fa9-139">OUTPUTS</span></span>

### <span data-ttu-id="b0fa9-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b0fa9-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="b0fa9-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="b0fa9-141">NOTES</span></span>

## <span data-ttu-id="b0fa9-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b0fa9-142">RELATED LINKS</span></span>

[<span data-ttu-id="b0fa9-143">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b0fa9-143">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b0fa9-144">Neu – AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b0fa9-144">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b0fa9-145">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b0fa9-145">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b0fa9-146">Satz-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b0fa9-146">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


