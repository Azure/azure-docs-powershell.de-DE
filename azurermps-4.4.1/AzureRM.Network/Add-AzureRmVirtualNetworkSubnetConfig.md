---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 9b5718dc7d0931a5a99e8f76ce4376b0753bc571
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663898"
---
# <span data-ttu-id="58f52-101">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="58f52-101">Add-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="58f52-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="58f52-102">SYNOPSIS</span></span>
<span data-ttu-id="58f52-103">Fügt eine Subnetz-Konfiguration zu einem virtuellen Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="58f52-103">Adds a subnet configuration to a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58f52-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="58f52-104">SYNTAX</span></span>

### <span data-ttu-id="58f52-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="58f52-105">SetByResource (Default)</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58f52-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="58f52-106">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58f52-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58f52-107">DESCRIPTION</span></span>
<span data-ttu-id="58f52-108">Das Cmdlet **Add-AzureRmVirtualNetworkSubnetConfig** fügt eine Subnetz-Konfiguration zu einem vorhandenen Azure-virtuellen Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="58f52-108">The **Add-AzureRmVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="58f52-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="58f52-109">EXAMPLES</span></span>

### <span data-ttu-id="58f52-110">1: Hinzufügen eines Subnetzes zu einem vorhandenen virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="58f52-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

  <span data-ttu-id="58f52-111">In diesem Beispiel wird zunächst eine Ressourcengruppe als Container der zu erstellende Ressourcen erstellt.</span><span class="sxs-lookup"><span data-stu-id="58f52-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="58f52-112">Anschließend wird eine Subnetz-Konfiguration erstellt und zum Erstellen eines virtuellen Netzwerks verwendet.</span><span class="sxs-lookup"><span data-stu-id="58f52-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="58f52-113">Die Add-AzureRmVirtualNetworkSubnetConfig wird dann verwendet, um der speicherresidenten Darstellung des virtuellen Netzwerks ein Subnetz hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="58f52-113">The Add-AzureRmVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="58f52-114">Mit dem Befehl Set-AzureRmVirtualNetwork wird das vorhandene virtuelle Netzwerk mit dem neuen Subnetz aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="58f52-114">The Set-AzureRmVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

## <span data-ttu-id="58f52-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="58f52-115">PARAMETERS</span></span>

### <span data-ttu-id="58f52-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="58f52-116">-AddressPrefix</span></span>
<span data-ttu-id="58f52-117">Gibt einen Bereich von IP-Adressen für eine Subnetz-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="58f52-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="58f52-118">-Name</span><span class="sxs-lookup"><span data-stu-id="58f52-118">-Name</span></span>
<span data-ttu-id="58f52-119">Gibt den Namen der hinzuzufügenden Subnet-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="58f52-119">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="58f52-120">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="58f52-120">-NetworkSecurityGroup</span></span>
<span data-ttu-id="58f52-121">Gibt ein **NetworkSecurityGroup** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="58f52-121">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="58f52-122">Mit diesem Cmdlet wird dem Objekt, das dieser Parameter angibt, eine virtuelle Netzwerk-Subnetz-Konfiguration hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="58f52-122">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="58f52-123">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="58f52-123">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="58f52-124">Gibt die ID einer Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="58f52-124">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="58f52-125">-Routel</span><span class="sxs-lookup"><span data-stu-id="58f52-125">-RouteTable</span></span>
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

### <span data-ttu-id="58f52-126">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="58f52-126">-RouteTableId</span></span>
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

### <span data-ttu-id="58f52-127">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="58f52-127">-ServiceEndpoint</span></span>
<span data-ttu-id="58f52-128">Dienstendpunkt Wert</span><span class="sxs-lookup"><span data-stu-id="58f52-128">Service Endpoint Value</span></span>

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

### <span data-ttu-id="58f52-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="58f52-129">-VirtualNetwork</span></span>
<span data-ttu-id="58f52-130">Gibt das **VirtualNetwork** -Objekt an, dem eine Subnetz-Konfiguration hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="58f52-130">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="58f52-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58f52-131">-DefaultProfile</span></span>
<span data-ttu-id="58f52-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="58f52-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58f52-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58f52-133">CommonParameters</span></span>
<span data-ttu-id="58f52-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58f52-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58f52-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58f52-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58f52-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="58f52-136">INPUTS</span></span>

### <span data-ttu-id="58f52-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="58f52-137">PSVirtualNetwork</span></span>
<span data-ttu-id="58f52-138">Der Parameter "VirtualNetwork" akzeptiert den Wert vom Typ "PSVirtualNetwork" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="58f52-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="58f52-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="58f52-139">OUTPUTS</span></span>

### <span data-ttu-id="58f52-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="58f52-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="58f52-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="58f52-141">NOTES</span></span>

## <span data-ttu-id="58f52-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="58f52-142">RELATED LINKS</span></span>

[<span data-ttu-id="58f52-143">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="58f52-143">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="58f52-144">Neu – AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="58f52-144">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="58f52-145">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="58f52-145">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="58f52-146">Satz-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="58f52-146">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


