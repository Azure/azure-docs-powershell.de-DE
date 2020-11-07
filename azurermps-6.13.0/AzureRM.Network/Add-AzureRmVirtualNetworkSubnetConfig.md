---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 1129b24c69dc362ea4d700be28a0823afa860885
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664553"
---
# <span data-ttu-id="d932c-101">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d932c-101">Add-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="d932c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d932c-102">SYNOPSIS</span></span>
<span data-ttu-id="d932c-103">Fügt eine Subnetz-Konfiguration zu einem virtuellen Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="d932c-103">Adds a subnet configuration to a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d932c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d932c-104">SYNTAX</span></span>

### <span data-ttu-id="d932c-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="d932c-105">SetByResource (Default)</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d932c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d932c-106">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d932c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d932c-107">DESCRIPTION</span></span>
<span data-ttu-id="d932c-108">Das Cmdlet **Add-AzureRmVirtualNetworkSubnetConfig** fügt eine Subnetz-Konfiguration zu einem vorhandenen Azure-virtuellen Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="d932c-108">The **Add-AzureRmVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="d932c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d932c-109">EXAMPLES</span></span>

### <span data-ttu-id="d932c-110">1: Hinzufügen eines Subnetzes zu einem vorhandenen virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="d932c-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

  <span data-ttu-id="d932c-111">In diesem Beispiel wird zunächst eine Ressourcengruppe als Container der zu erstellende Ressourcen erstellt.</span><span class="sxs-lookup"><span data-stu-id="d932c-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="d932c-112">Anschließend wird eine Subnetz-Konfiguration erstellt und zum Erstellen eines virtuellen Netzwerks verwendet.</span><span class="sxs-lookup"><span data-stu-id="d932c-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="d932c-113">Die Add-AzureRmVirtualNetworkSubnetConfig wird dann verwendet, um der speicherresidenten Darstellung des virtuellen Netzwerks ein Subnetz hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d932c-113">The Add-AzureRmVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="d932c-114">Mit dem Befehl Set-AzureRmVirtualNetwork wird das vorhandene virtuelle Netzwerk mit dem neuen Subnetz aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d932c-114">The Set-AzureRmVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="d932c-115">2: Hinzufügen einer Delegierung zu einem Subnetz, das einem vorhandenen virtuellen Netzwerk hinzugefügt wird</span><span class="sxs-lookup"><span data-stu-id="d932c-115">2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="d932c-116">In diesem Beispiel wird zunächst ein vorhandenes vnet-Element abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d932c-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="d932c-117">Anschließend wird im Arbeitsspeicher ein Delegierungs Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="d932c-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="d932c-118">Schließlich wird ein neues Subnetz mit dieser Delegierung erstellt, das dem vnet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="d932c-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="d932c-119">Die geänderte Konfiguration wird dann an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="d932c-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="d932c-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="d932c-120">PARAMETERS</span></span>

### <span data-ttu-id="d932c-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d932c-121">-AddressPrefix</span></span>
<span data-ttu-id="d932c-122">Gibt einen Bereich von IP-Adressen für eine Subnetz-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="d932c-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="d932c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d932c-123">-DefaultProfile</span></span>
<span data-ttu-id="d932c-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d932c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d932c-125">-Delegation</span><span class="sxs-lookup"><span data-stu-id="d932c-125">-Delegation</span></span>
<span data-ttu-id="d932c-126">Liste der Dienste, die über die Berechtigung zum Ausführen von Vorgängen in diesem Subnetz verfügen</span><span class="sxs-lookup"><span data-stu-id="d932c-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="d932c-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d932c-127">-Name</span></span>
<span data-ttu-id="d932c-128">Gibt den Namen der hinzuzufügenden Subnet-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="d932c-128">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="d932c-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d932c-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="d932c-130">Gibt ein **NetworkSecurityGroup** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d932c-130">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="d932c-131">Mit diesem Cmdlet wird dem Objekt, das dieser Parameter angibt, eine virtuelle Netzwerk-Subnetz-Konfiguration hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d932c-131">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="d932c-132">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="d932c-132">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="d932c-133">Gibt die ID einer Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="d932c-133">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="d932c-134">-Routel</span><span class="sxs-lookup"><span data-stu-id="d932c-134">-RouteTable</span></span>
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

### <span data-ttu-id="d932c-135">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="d932c-135">-RouteTableId</span></span>
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

### <span data-ttu-id="d932c-136">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="d932c-136">-ServiceEndpoint</span></span>
<span data-ttu-id="d932c-137">Dienstendpunkt Wert</span><span class="sxs-lookup"><span data-stu-id="d932c-137">Service Endpoint Value</span></span>

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

### <span data-ttu-id="d932c-138">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d932c-138">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="d932c-139">Dienstendpunkt Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d932c-139">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="d932c-140">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d932c-140">-VirtualNetwork</span></span>
<span data-ttu-id="d932c-141">Gibt das **VirtualNetwork** -Objekt an, dem eine Subnetz-Konfiguration hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d932c-141">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="d932c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d932c-142">CommonParameters</span></span>
<span data-ttu-id="d932c-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d932c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d932c-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d932c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d932c-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d932c-145">INPUTS</span></span>

### <span data-ttu-id="d932c-146">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d932c-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="d932c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="d932c-147">System.String</span></span>

### <span data-ttu-id="d932c-148">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d932c-148">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="d932c-149">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="d932c-149">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="d932c-150">System. Collections. Generic. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d932c-150">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d932c-151">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d932c-151">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d932c-152">System. Collections. Generic. List ' 1 [[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d932c-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d932c-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d932c-153">OUTPUTS</span></span>

### <span data-ttu-id="d932c-154">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d932c-154">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="d932c-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="d932c-155">NOTES</span></span>

## <span data-ttu-id="d932c-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d932c-156">RELATED LINKS</span></span>

[<span data-ttu-id="d932c-157">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d932c-157">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d932c-158">Neu – AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d932c-158">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d932c-159">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d932c-159">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d932c-160">Satz-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d932c-160">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


