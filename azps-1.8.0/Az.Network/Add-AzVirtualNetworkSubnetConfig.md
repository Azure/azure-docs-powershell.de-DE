---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 1df94cc14191fcb95e271bf5fef6b1a09fa77060
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660888"
---
# <span data-ttu-id="d7b6d-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d7b6d-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="d7b6d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7b6d-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b6d-103">Fügt eine Subnetz-Konfiguration zu einem virtuellen Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="d7b6d-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="d7b6d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7b6d-104">SYNTAX</span></span>

### <span data-ttu-id="d7b6d-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="d7b6d-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7b6d-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d7b6d-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7b6d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7b6d-107">DESCRIPTION</span></span>
<span data-ttu-id="d7b6d-108">Das Cmdlet **Add-AzVirtualNetworkSubnetConfig** fügt eine Subnetz-Konfiguration zu einem vorhandenen Azure-virtuellen Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="d7b6d-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="d7b6d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7b6d-109">EXAMPLES</span></span>

### <span data-ttu-id="d7b6d-110">1: Hinzufügen eines Subnetzes zu einem vorhandenen virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="d7b6d-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="d7b6d-111">In diesem Beispiel wird zunächst eine Ressourcengruppe als Container der zu erstellende Ressourcen erstellt.</span><span class="sxs-lookup"><span data-stu-id="d7b6d-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="d7b6d-112">Anschließend wird eine Subnetz-Konfiguration erstellt und zum Erstellen eines virtuellen Netzwerks verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7b6d-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="d7b6d-113">Die Add-AzVirtualNetworkSubnetConfig wird dann verwendet, um der speicherresidenten Darstellung des virtuellen Netzwerks ein Subnetz hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7b6d-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="d7b6d-114">Mit dem Befehl Set-AzVirtualNetwork wird das vorhandene virtuelle Netzwerk mit dem neuen Subnetz aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d7b6d-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="d7b6d-115">2: Hinzufügen einer Delegierung zu einem Subnetz, das einem vorhandenen virtuellen Netzwerk hinzugefügt wird</span><span class="sxs-lookup"><span data-stu-id="d7b6d-115">2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="d7b6d-116">In diesem Beispiel wird zunächst ein vorhandenes vnet-Element abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d7b6d-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="d7b6d-117">Anschließend wird im Arbeitsspeicher ein Delegierungs Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="d7b6d-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="d7b6d-118">Schließlich wird ein neues Subnetz mit dieser Delegierung erstellt, das dem vnet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="d7b6d-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="d7b6d-119">Die geänderte Konfiguration wird dann an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="d7b6d-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="d7b6d-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7b6d-120">PARAMETERS</span></span>

### <span data-ttu-id="d7b6d-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d7b6d-121">-AddressPrefix</span></span>
<span data-ttu-id="d7b6d-122">Gibt einen Bereich von IP-Adressen für eine Subnetz-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="d7b6d-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="d7b6d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7b6d-123">-DefaultProfile</span></span>
<span data-ttu-id="d7b6d-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d7b6d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7b6d-125">-Delegation</span><span class="sxs-lookup"><span data-stu-id="d7b6d-125">-Delegation</span></span>
<span data-ttu-id="d7b6d-126">Liste der Dienste, die über die Berechtigung zum Ausführen von Vorgängen in diesem Subnetz verfügen</span><span class="sxs-lookup"><span data-stu-id="d7b6d-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="d7b6d-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d7b6d-127">-Name</span></span>
<span data-ttu-id="d7b6d-128">Gibt den Namen der hinzuzufügenden Subnet-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="d7b6d-128">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="d7b6d-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d7b6d-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="d7b6d-130">Gibt ein **NetworkSecurityGroup** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d7b6d-130">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="d7b6d-131">Mit diesem Cmdlet wird dem Objekt, das dieser Parameter angibt, eine virtuelle Netzwerk-Subnetz-Konfiguration hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d7b6d-131">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="d7b6d-132">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="d7b6d-132">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="d7b6d-133">Gibt die ID einer Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="d7b6d-133">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="d7b6d-134">-Routel</span><span class="sxs-lookup"><span data-stu-id="d7b6d-134">-RouteTable</span></span>
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

### <span data-ttu-id="d7b6d-135">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="d7b6d-135">-RouteTableId</span></span>
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

### <span data-ttu-id="d7b6d-136">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="d7b6d-136">-ServiceEndpoint</span></span>
<span data-ttu-id="d7b6d-137">Dienstendpunkt Wert</span><span class="sxs-lookup"><span data-stu-id="d7b6d-137">Service Endpoint Value</span></span>

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

### <span data-ttu-id="d7b6d-138">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d7b6d-138">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="d7b6d-139">Dienstendpunkt Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d7b6d-139">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="d7b6d-140">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d7b6d-140">-VirtualNetwork</span></span>
<span data-ttu-id="d7b6d-141">Gibt das **VirtualNetwork** -Objekt an, dem eine Subnetz-Konfiguration hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7b6d-141">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="d7b6d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b6d-142">CommonParameters</span></span>
<span data-ttu-id="d7b6d-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7b6d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b6d-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7b6d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b6d-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7b6d-145">INPUTS</span></span>

### <span data-ttu-id="d7b6d-146">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d7b6d-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="d7b6d-147">System. String</span><span class="sxs-lookup"><span data-stu-id="d7b6d-147">System.String</span></span>

### <span data-ttu-id="d7b6d-148">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d7b6d-148">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="d7b6d-149">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="d7b6d-149">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="d7b6d-150">System. String []</span><span class="sxs-lookup"><span data-stu-id="d7b6d-150">System.String[]</span></span>

### <span data-ttu-id="d7b6d-151">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="d7b6d-151">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="d7b6d-152">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="d7b6d-152">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="d7b6d-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7b6d-153">OUTPUTS</span></span>

### <span data-ttu-id="d7b6d-154">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d7b6d-154">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="d7b6d-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7b6d-155">NOTES</span></span>

## <span data-ttu-id="d7b6d-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7b6d-156">RELATED LINKS</span></span>

[<span data-ttu-id="d7b6d-157">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d7b6d-157">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d7b6d-158">Neu – AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d7b6d-158">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d7b6d-159">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d7b6d-159">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d7b6d-160">Satz-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d7b6d-160">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
