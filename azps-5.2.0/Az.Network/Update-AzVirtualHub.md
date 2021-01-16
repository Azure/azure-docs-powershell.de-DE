---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
ms.openlocfilehash: a07df2c6330757bf9e5b4f211429f6e2918fea39
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304968"
---
# <span data-ttu-id="80d29-101">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="80d29-101">Update-AzVirtualHub</span></span>

## <span data-ttu-id="80d29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80d29-102">SYNOPSIS</span></span>
<span data-ttu-id="80d29-103">Aktualisiert einen virtuellen Hub.</span><span class="sxs-lookup"><span data-stu-id="80d29-103">Updates a virtual hub.</span></span>

## <span data-ttu-id="80d29-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80d29-104">SYNTAX</span></span>

### <span data-ttu-id="80d29-105">ByVirtualHubName (Standard)</span><span class="sxs-lookup"><span data-stu-id="80d29-105">ByVirtualHubName (Default)</span></span>
```
Update-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80d29-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="80d29-106">ByVirtualHubResourceId</span></span>
```
Update-AzVirtualHub -ResourceId <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80d29-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="80d29-107">ByVirtualHubObject</span></span>
```
Update-AzVirtualHub -InputObject <PSVirtualHub> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80d29-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80d29-108">DESCRIPTION</span></span>
<span data-ttu-id="80d29-109">Das **Cmdlet "Update-AzVirtualHub"** aktualisiert einen virtuellen Hub.</span><span class="sxs-lookup"><span data-stu-id="80d29-109">The **Update-AzVirtualHub** cmdlet updates a virtual hub.</span></span>

## <span data-ttu-id="80d29-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="80d29-110">EXAMPLES</span></span>

### <span data-ttu-id="80d29-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="80d29-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Update-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.2.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.2.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="80d29-112">Im vorstehenden Beispiel wird eine Ressourcengruppe "testRG", ein virtuelles WAN und ein virtueller Hub in West US in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="80d29-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="80d29-113">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="80d29-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="80d29-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="80d29-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> Update-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 192.168.2.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="80d29-115">Im vorstehenden Beispiel wird eine Ressourcengruppe "testRG", ein virtuelles WAN und ein virtueller Hub in West US in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="80d29-115">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="80d29-116">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="80d29-116">The virtual hub will have the address space "10.0.1.0/24".</span></span>
<span data-ttu-id="80d29-117">Dieses Beispiel ähnelt Beispiel 1, fügt aber auch eine Routentabelle an den virtuellen Hub an.</span><span class="sxs-lookup"><span data-stu-id="80d29-117">This example is similar to Example 1, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="80d29-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80d29-118">PARAMETERS</span></span>

### <span data-ttu-id="80d29-119">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="80d29-119">-AddressPrefix</span></span>
<span data-ttu-id="80d29-120">Die Adressraumzeichenfolge für diesen virtuellen Hub.</span><span class="sxs-lookup"><span data-stu-id="80d29-120">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="80d29-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80d29-121">-AsJob</span></span>
<span data-ttu-id="80d29-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="80d29-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80d29-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80d29-123">-DefaultProfile</span></span>
<span data-ttu-id="80d29-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="80d29-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80d29-125">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="80d29-125">-HubVnetConnection</span></span>
<span data-ttu-id="80d29-126">Die diesem virtuellen Hub zugeordneten virtuellen Hub-Netzwerkverbindungen.</span><span class="sxs-lookup"><span data-stu-id="80d29-126">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="80d29-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80d29-127">-InputObject</span></span>
<span data-ttu-id="80d29-128">Das zu ändernde virtuelle Hubobjekt.</span><span class="sxs-lookup"><span data-stu-id="80d29-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80d29-129">-Name</span><span class="sxs-lookup"><span data-stu-id="80d29-129">-Name</span></span>
<span data-ttu-id="80d29-130">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="80d29-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80d29-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80d29-131">-ResourceGroupName</span></span>
<span data-ttu-id="80d29-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="80d29-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80d29-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80d29-133">-ResourceId</span></span>
<span data-ttu-id="80d29-134">Die Ressourcen-ID des virtuellen Hubs, der geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="80d29-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80d29-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="80d29-135">-RouteTable</span></span>
<span data-ttu-id="80d29-136">Die diesem virtuellen Hub zugeordnete Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="80d29-136">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="80d29-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="80d29-137">-Sku</span></span>
<span data-ttu-id="80d29-138">Die SKU des virtuellen Hubs.</span><span class="sxs-lookup"><span data-stu-id="80d29-138">The sku of the Virtual Hub.</span></span>

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

### <span data-ttu-id="80d29-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="80d29-139">-Tag</span></span>
<span data-ttu-id="80d29-140">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="80d29-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="80d29-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80d29-141">-Confirm</span></span>
<span data-ttu-id="80d29-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="80d29-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80d29-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="80d29-143">-WhatIf</span></span>
<span data-ttu-id="80d29-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80d29-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80d29-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="80d29-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80d29-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80d29-146">CommonParameters</span></span>
<span data-ttu-id="80d29-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80d29-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80d29-148">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80d29-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80d29-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="80d29-149">INPUTS</span></span>

### <span data-ttu-id="80d29-150">System.String</span><span class="sxs-lookup"><span data-stu-id="80d29-150">System.String</span></span>

### <span data-ttu-id="80d29-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="80d29-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="80d29-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="80d29-152">OUTPUTS</span></span>

### <span data-ttu-id="80d29-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="80d29-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="80d29-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="80d29-154">NOTES</span></span>

## <span data-ttu-id="80d29-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="80d29-155">RELATED LINKS</span></span>

[<span data-ttu-id="80d29-156">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="80d29-156">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="80d29-157">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="80d29-157">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="80d29-158">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="80d29-158">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)
