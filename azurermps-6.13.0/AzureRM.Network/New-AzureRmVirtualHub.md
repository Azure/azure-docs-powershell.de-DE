---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHub.md
ms.openlocfilehash: 4058f9a2ba0de1e5610773ad4af21c8bb788d58c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663359"
---
# <span data-ttu-id="e204d-101">New-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e204d-101">New-AzureRmVirtualHub</span></span>

## <span data-ttu-id="e204d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e204d-102">SYNOPSIS</span></span>
<span data-ttu-id="e204d-103">Erstellt eine Azure VirtualHub-Ressource.</span><span class="sxs-lookup"><span data-stu-id="e204d-103">Creates an Azure VirtualHub resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e204d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e204d-104">SYNTAX</span></span>

### <span data-ttu-id="e204d-105">ByVirtualWanObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="e204d-105">ByVirtualWanObject (Default)</span></span>
```
New-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan>
 -AddressPrefix <String> -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e204d-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="e204d-106">ByVirtualWanResourceId</span></span>
```
New-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e204d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e204d-107">DESCRIPTION</span></span>
<span data-ttu-id="e204d-108">Erstellt eine Azure VirtualHub-Ressource.</span><span class="sxs-lookup"><span data-stu-id="e204d-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="e204d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e204d-109">EXAMPLES</span></span>

### <span data-ttu-id="e204d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e204d-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="e204d-111">Das oben beschriebene erstellt eine Ressourcengruppe "testRG", ein virtuelles WAN und einen virtuellen Hub in West-USA in dieser Ressourcengruppe in Azure.</span><span class="sxs-lookup"><span data-stu-id="e204d-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e204d-112">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="e204d-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="e204d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e204d-113">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -Location "West US"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="e204d-114">Das oben beschriebene erstellt eine Ressourcengruppe "testRG", ein virtuelles WAN und einen virtuellen Hub in West-USA in dieser Ressourcengruppe in Azure.</span><span class="sxs-lookup"><span data-stu-id="e204d-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e204d-115">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="e204d-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="e204d-116">Dieses Beispiel ähnelt dem Beispiel 1, verwendet aber eine Ressourcen-ID, um auf das virtuelle WAN zu verweisen, das zum Erstellen des virtuellen Hubs erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e204d-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="e204d-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e204d-117">Example 3</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $route1 = New-AzureRmVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzureRmVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzureRmVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzureRmVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="e204d-118">Das oben beschriebene erstellt eine Ressourcengruppe "testRG", ein virtuelles WAN und einen virtuellen Hub in West-USA in dieser Ressourcengruppe in Azure.</span><span class="sxs-lookup"><span data-stu-id="e204d-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e204d-119">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24" und eine Routingtabelle angefügt.</span><span class="sxs-lookup"><span data-stu-id="e204d-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="e204d-120">Dieses Beispiel ähnelt dem Beispiel 2, fügt aber auch eine Routingtabelle an den virtuellen Hub an.</span><span class="sxs-lookup"><span data-stu-id="e204d-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="e204d-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="e204d-121">PARAMETERS</span></span>

### <span data-ttu-id="e204d-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e204d-122">-AddressPrefix</span></span>
<span data-ttu-id="e204d-123">Die Adressraum Zeichenfolge für diesen virtuellen Hub.</span><span class="sxs-lookup"><span data-stu-id="e204d-123">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="e204d-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e204d-124">-AsJob</span></span>
<span data-ttu-id="e204d-125">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e204d-125">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e204d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e204d-126">-DefaultProfile</span></span>
<span data-ttu-id="e204d-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e204d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e204d-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e204d-128">-HubVnetConnection</span></span>
<span data-ttu-id="e204d-129">Die virtuellen Hub-Netzwerkverbindungen, die diesem virtuellen Hub zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e204d-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e204d-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="e204d-130">-Location</span></span>
<span data-ttu-id="e204d-131">Lage.</span><span class="sxs-lookup"><span data-stu-id="e204d-131">location.</span></span>

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

### <span data-ttu-id="e204d-132">-Name</span><span class="sxs-lookup"><span data-stu-id="e204d-132">-Name</span></span>
<span data-ttu-id="e204d-133">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="e204d-133">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e204d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e204d-134">-ResourceGroupName</span></span>
<span data-ttu-id="e204d-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e204d-135">The resource group name.</span></span>

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

### <span data-ttu-id="e204d-136">-Routel</span><span class="sxs-lookup"><span data-stu-id="e204d-136">-RouteTable</span></span>
<span data-ttu-id="e204d-137">Die Route-Tabelle, die diesem virtuellen Hub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e204d-137">The route table associated with this Virtual Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e204d-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="e204d-138">-Tag</span></span>
<span data-ttu-id="e204d-139">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="e204d-139">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e204d-140">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="e204d-140">-VirtualWan</span></span>
<span data-ttu-id="e204d-141">Das virtuelle WAN-Objekt, mit dem dieser Hub verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="e204d-141">The virtual wan object this hub is linked to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e204d-142">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="e204d-142">-VirtualWanId</span></span>
<span data-ttu-id="e204d-143">Die ID des virtuellen WAN-Objekts, mit dem dieser Hub verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="e204d-143">The id of virtual wan object this hub is linked to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e204d-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e204d-144">-Confirm</span></span>
<span data-ttu-id="e204d-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e204d-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e204d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e204d-146">-WhatIf</span></span>
<span data-ttu-id="e204d-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e204d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e204d-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e204d-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e204d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e204d-149">CommonParameters</span></span>
<span data-ttu-id="e204d-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e204d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e204d-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e204d-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e204d-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e204d-152">INPUTS</span></span>

### <span data-ttu-id="e204d-153">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e204d-153">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="e204d-154">System. String</span><span class="sxs-lookup"><span data-stu-id="e204d-154">System.String</span></span>

## <span data-ttu-id="e204d-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e204d-155">OUTPUTS</span></span>

### <span data-ttu-id="e204d-156">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e204d-156">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="e204d-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="e204d-157">NOTES</span></span>

## <span data-ttu-id="e204d-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e204d-158">RELATED LINKS</span></span>
