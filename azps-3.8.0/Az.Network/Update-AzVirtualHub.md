---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
ms.openlocfilehash: a07df2c6330757bf9e5b4f211429f6e2918fea39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845208"
---
# <span data-ttu-id="90aec-101">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="90aec-101">Update-AzVirtualHub</span></span>

## <span data-ttu-id="90aec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90aec-102">SYNOPSIS</span></span>
<span data-ttu-id="90aec-103">Aktualisiert einen virtuellen Hub.</span><span class="sxs-lookup"><span data-stu-id="90aec-103">Updates a virtual hub.</span></span>

## <span data-ttu-id="90aec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90aec-104">SYNTAX</span></span>

### <span data-ttu-id="90aec-105">ByVirtualHubName (Standard)</span><span class="sxs-lookup"><span data-stu-id="90aec-105">ByVirtualHubName (Default)</span></span>
```
Update-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90aec-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="90aec-106">ByVirtualHubResourceId</span></span>
```
Update-AzVirtualHub -ResourceId <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90aec-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="90aec-107">ByVirtualHubObject</span></span>
```
Update-AzVirtualHub -InputObject <PSVirtualHub> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="90aec-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90aec-108">DESCRIPTION</span></span>
<span data-ttu-id="90aec-109">Das Cmdlet **Update-AzVirtualHub** aktualisiert einen virtuellen Hub.</span><span class="sxs-lookup"><span data-stu-id="90aec-109">The **Update-AzVirtualHub** cmdlet updates a virtual hub.</span></span>

## <span data-ttu-id="90aec-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90aec-110">EXAMPLES</span></span>

### <span data-ttu-id="90aec-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="90aec-111">Example 1</span></span>

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

<span data-ttu-id="90aec-112">Das oben beschriebene erstellt eine Ressourcengruppe "testRG", ein virtuelles WAN und einen virtuellen Hub in West-USA in dieser Ressourcengruppe in Azure.</span><span class="sxs-lookup"><span data-stu-id="90aec-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="90aec-113">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="90aec-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="90aec-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="90aec-114">Example 2</span></span>

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

<span data-ttu-id="90aec-115">Das oben beschriebene erstellt eine Ressourcengruppe "testRG", ein virtuelles WAN und einen virtuellen Hub in West-USA in dieser Ressourcengruppe in Azure.</span><span class="sxs-lookup"><span data-stu-id="90aec-115">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="90aec-116">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="90aec-116">The virtual hub will have the address space "10.0.1.0/24".</span></span>
<span data-ttu-id="90aec-117">Dieses Beispiel ähnelt dem Beispiel 1, fügt aber auch eine Routingtabelle an den virtuellen Hub an.</span><span class="sxs-lookup"><span data-stu-id="90aec-117">This example is similar to Example 1, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="90aec-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="90aec-118">PARAMETERS</span></span>

### <span data-ttu-id="90aec-119">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="90aec-119">-AddressPrefix</span></span>
<span data-ttu-id="90aec-120">Die Adressraum Zeichenfolge für diesen virtuellen Hub.</span><span class="sxs-lookup"><span data-stu-id="90aec-120">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="90aec-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90aec-121">-AsJob</span></span>
<span data-ttu-id="90aec-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="90aec-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90aec-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90aec-123">-DefaultProfile</span></span>
<span data-ttu-id="90aec-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="90aec-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90aec-125">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="90aec-125">-HubVnetConnection</span></span>
<span data-ttu-id="90aec-126">Die virtuellen Hub-Netzwerkverbindungen, die diesem virtuellen Hub zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="90aec-126">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="90aec-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="90aec-127">-InputObject</span></span>
<span data-ttu-id="90aec-128">Das virtuelle Hub-Objekt, das geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="90aec-128">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="90aec-129">-Name</span><span class="sxs-lookup"><span data-stu-id="90aec-129">-Name</span></span>
<span data-ttu-id="90aec-130">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="90aec-130">The resource name.</span></span>

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

### <span data-ttu-id="90aec-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90aec-131">-ResourceGroupName</span></span>
<span data-ttu-id="90aec-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="90aec-132">The resource group name.</span></span>

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

### <span data-ttu-id="90aec-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="90aec-133">-ResourceId</span></span>
<span data-ttu-id="90aec-134">Die Ressourcen-ID des virtuellen Hubs, der geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="90aec-134">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="90aec-135">-Routel</span><span class="sxs-lookup"><span data-stu-id="90aec-135">-RouteTable</span></span>
<span data-ttu-id="90aec-136">Die Route-Tabelle, die diesem virtuellen Hub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="90aec-136">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="90aec-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="90aec-137">-Sku</span></span>
<span data-ttu-id="90aec-138">Die SKU des virtuellen Hubs.</span><span class="sxs-lookup"><span data-stu-id="90aec-138">The sku of the Virtual Hub.</span></span>

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

### <span data-ttu-id="90aec-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="90aec-139">-Tag</span></span>
<span data-ttu-id="90aec-140">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="90aec-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="90aec-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="90aec-141">-Confirm</span></span>
<span data-ttu-id="90aec-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90aec-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90aec-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90aec-143">-WhatIf</span></span>
<span data-ttu-id="90aec-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90aec-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90aec-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90aec-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90aec-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90aec-146">CommonParameters</span></span>
<span data-ttu-id="90aec-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90aec-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90aec-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90aec-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90aec-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90aec-149">INPUTS</span></span>

### <span data-ttu-id="90aec-150">System. String</span><span class="sxs-lookup"><span data-stu-id="90aec-150">System.String</span></span>

### <span data-ttu-id="90aec-151">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="90aec-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="90aec-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90aec-152">OUTPUTS</span></span>

### <span data-ttu-id="90aec-153">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="90aec-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="90aec-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="90aec-154">NOTES</span></span>

## <span data-ttu-id="90aec-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90aec-155">RELATED LINKS</span></span>

[<span data-ttu-id="90aec-156">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="90aec-156">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="90aec-157">Neu – AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="90aec-157">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="90aec-158">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="90aec-158">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)
