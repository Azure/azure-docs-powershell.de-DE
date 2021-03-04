---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
ms.openlocfilehash: a7b8e790892b14e053a07f83e6a27c4ce82c00ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934819"
---
# <span data-ttu-id="1e68c-101">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1e68c-101">New-AzVirtualHub</span></span>

## <span data-ttu-id="1e68c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e68c-102">SYNOPSIS</span></span>
<span data-ttu-id="1e68c-103">Erstellt eine Azure VirtualHub-Ressource.</span><span class="sxs-lookup"><span data-stu-id="1e68c-103">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="1e68c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e68c-104">SYNTAX</span></span>

### <span data-ttu-id="1e68c-105">ByVirtualWanObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="1e68c-105">ByVirtualWanObject (Default)</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e68c-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="1e68c-106">ByVirtualWanResourceId</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e68c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e68c-107">DESCRIPTION</span></span>
<span data-ttu-id="1e68c-108">Erstellt eine Azure VirtualHub-Ressource.</span><span class="sxs-lookup"><span data-stu-id="1e68c-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="1e68c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1e68c-109">EXAMPLES</span></span>

### <span data-ttu-id="1e68c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1e68c-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="1e68c-111">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe "testRG", ein virtuelles WAN und ein virtueller Hub in West USA in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="1e68c-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="1e68c-112">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="1e68c-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="1e68c-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1e68c-113">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -Location "West US"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="1e68c-114">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe "testRG", ein virtuelles WAN und ein virtueller Hub in West USA in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="1e68c-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="1e68c-115">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="1e68c-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="1e68c-116">Dieses Beispiel ähnelt Beispiel 1, verwendet jedoch eine Ressourcen-ID, um auf das virtuelle WAN zu verweisen, das zum Erstellen des virtuellen Hubs erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1e68c-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="1e68c-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="1e68c-117">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="1e68c-118">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe "testRG", ein virtuelles WAN und ein virtueller Hub in West USA in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="1e68c-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="1e68c-119">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24" und eine Routentabelle angefügt.</span><span class="sxs-lookup"><span data-stu-id="1e68c-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="1e68c-120">Dieses Beispiel ähnelt Beispiel 2, fügt aber auch eine Routentabelle an den virtuellen Hub an.</span><span class="sxs-lookup"><span data-stu-id="1e68c-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="1e68c-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1e68c-121">PARAMETERS</span></span>

### <span data-ttu-id="1e68c-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1e68c-122">-AddressPrefix</span></span>
<span data-ttu-id="1e68c-123">Die Adressbereichszeichenfolge für diesen virtuellen Hub.</span><span class="sxs-lookup"><span data-stu-id="1e68c-123">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="1e68c-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e68c-124">-AsJob</span></span>
<span data-ttu-id="1e68c-125">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1e68c-125">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e68c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e68c-126">-DefaultProfile</span></span>
<span data-ttu-id="1e68c-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1e68c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e68c-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="1e68c-128">-HubVnetConnection</span></span>
<span data-ttu-id="1e68c-129">Die virtuellen Hubnetzwerkverbindungen, die diesem virtuellen Hub zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1e68c-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

```yaml
Type: PSHubVirtualNetworkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e68c-130">-Location</span><span class="sxs-lookup"><span data-stu-id="1e68c-130">-Location</span></span>
<span data-ttu-id="1e68c-131">speicherort.</span><span class="sxs-lookup"><span data-stu-id="1e68c-131">location.</span></span>

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

### <span data-ttu-id="1e68c-132">-Name</span><span class="sxs-lookup"><span data-stu-id="1e68c-132">-Name</span></span>
<span data-ttu-id="1e68c-133">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="1e68c-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e68c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e68c-134">-ResourceGroupName</span></span>
<span data-ttu-id="1e68c-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1e68c-135">The resource group name.</span></span>

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

### <span data-ttu-id="1e68c-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="1e68c-136">-RouteTable</span></span>
<span data-ttu-id="1e68c-137">Die routentabelle, die diesem virtuellen Hub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1e68c-137">The route table associated with this Virtual Hub.</span></span>

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e68c-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="1e68c-138">-Sku</span></span>
<span data-ttu-id="1e68c-139">Die Sku des virtuellen Hubs.</span><span class="sxs-lookup"><span data-stu-id="1e68c-139">The sku of the Virtual Hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e68c-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="1e68c-140">-Tag</span></span>
<span data-ttu-id="1e68c-141">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="1e68c-141">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e68c-142">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="1e68c-142">-VirtualWan</span></span>
<span data-ttu-id="1e68c-143">Das virtuelle Wan-Objekt, mit dem dieser Hub verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="1e68c-143">The virtual wan object this hub is linked to.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e68c-144">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="1e68c-144">-VirtualWanId</span></span>
<span data-ttu-id="1e68c-145">Die ID des virtuellen Wan-Objekts, mit dem dieser Hub verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="1e68c-145">The id of virtual wan object this hub is linked to.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e68c-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1e68c-146">-Confirm</span></span>
<span data-ttu-id="1e68c-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e68c-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e68c-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e68c-148">-WhatIf</span></span>
<span data-ttu-id="1e68c-149">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e68c-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e68c-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e68c-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e68c-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e68c-151">CommonParameters</span></span>
<span data-ttu-id="1e68c-152">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e68c-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e68c-153">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e68c-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e68c-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1e68c-154">INPUTS</span></span>

### <span data-ttu-id="1e68c-155">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="1e68c-155">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="1e68c-156">System.String</span><span class="sxs-lookup"><span data-stu-id="1e68c-156">System.String</span></span>

## <span data-ttu-id="1e68c-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1e68c-157">OUTPUTS</span></span>

### <span data-ttu-id="1e68c-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1e68c-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="1e68c-159">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1e68c-159">NOTES</span></span>

## <span data-ttu-id="1e68c-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1e68c-160">RELATED LINKS</span></span>

[<span data-ttu-id="1e68c-161">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1e68c-161">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="1e68c-162">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1e68c-162">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="1e68c-163">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1e68c-163">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
