---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
ms.openlocfilehash: a23b2ce975a67a87a5edd58b21835e16f812055b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928560"
---
# <span data-ttu-id="8dea0-101">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="8dea0-101">Set-AzVirtualHub</span></span>

## <span data-ttu-id="8dea0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dea0-102">SYNOPSIS</span></span>
<span data-ttu-id="8dea0-103">Ändert einen virtuellen Hub, um ihr eine virtuelle HUb-Routentabelle hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="8dea0-103">Modifies a Virtual Hub to add a Virtual HUb Route Table to it.</span></span>

## <span data-ttu-id="8dea0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8dea0-104">SYNTAX</span></span>

### <span data-ttu-id="8dea0-105">ByVirtualHubName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8dea0-105">ByVirtualHubName (Default)</span></span>
```
Set-AzVirtualHub -ResourceGroupName <String> -Name <String> -RouteTable <PSVirtualHubRouteTable[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8dea0-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="8dea0-106">ByVirtualHubResourceId</span></span>
```
Set-AzVirtualHub -ResourceId <String> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dea0-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="8dea0-107">ByVirtualHubObject</span></span>
```
Set-AzVirtualHub -InputObject <PSVirtualHub> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dea0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8dea0-108">DESCRIPTION</span></span>
<span data-ttu-id="8dea0-109">{{ Ausfüllen der Beschreibung }}</span><span class="sxs-lookup"><span data-stu-id="8dea0-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="8dea0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8dea0-110">EXAMPLES</span></span>

### <span data-ttu-id="8dea0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8dea0-111">Example 1</span></span>
```powershell
PS C:\> $existingHub�=�Get-AzVirtualHub�-ResourceGroupName�"testRg"�-Name�"westushub"
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> $routeTable1�=�Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"
PS C:\> Set-AzVirtualHub�-VirtualHub�$existingHub�-RouteTable�@($routeTable1)

VirtualWan                            : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/testWan
ResourceGroupName                     : testRg
Name                                  : westushub
Id                                    : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubswestushub
AddressPrefix                         : 10.40.0.0/16
RouteTable                            : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkExpressRouteConnections :
RouteTables                           : {routeTable1}
Location                              : westus
Sku                                   : Standard
Type                                  : Microsoft.Network/virtualHubs
ProvisioningState                     : Succeeded
```

<span data-ttu-id="8dea0-112">Zuerst erstellen wir ein Virtual Hub Route-Objekt und verwenden es zum Erstellen einer Virtual Hub-Route-Tabellenressource.</span><span class="sxs-lookup"><span data-stu-id="8dea0-112">First we create a Virtual Hub Route object, and use it to create a Virtual Hub Route Table resource.</span></span> <span data-ttu-id="8dea0-113">Anschließend legen wir diese Routentabellenressource auf den virtuellen Hub mit dem Befehl Set-AzVirtualHub festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8dea0-113">Then we set this route table resource to the virtual hub using the Set-AzVirtualHub command.</span></span>

## <span data-ttu-id="8dea0-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8dea0-114">PARAMETERS</span></span>

### <span data-ttu-id="8dea0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8dea0-115">-AsJob</span></span>
<span data-ttu-id="8dea0-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8dea0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8dea0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dea0-117">-DefaultProfile</span></span>
<span data-ttu-id="8dea0-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8dea0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dea0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dea0-119">-InputObject</span></span>
<span data-ttu-id="8dea0-120">Das zu ändernde Virtual Hub-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8dea0-120">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="8dea0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8dea0-121">-Name</span></span>
<span data-ttu-id="8dea0-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="8dea0-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dea0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dea0-123">-ResourceGroupName</span></span>
<span data-ttu-id="8dea0-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8dea0-124">The resource group name.</span></span>

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

### <span data-ttu-id="8dea0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dea0-125">-ResourceId</span></span>
<span data-ttu-id="8dea0-126">Die Ressourcen-ID des virtuellen Hubs, der geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8dea0-126">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="8dea0-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="8dea0-127">-RouteTable</span></span>
<span data-ttu-id="8dea0-128">Die Routentabellen, die diesem virtuellen Hub zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8dea0-128">The route tables associated with this Virtual Hub.</span></span>

```yaml
Type: PSVirtualHubRouteTable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dea0-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="8dea0-129">-Tag</span></span>
<span data-ttu-id="8dea0-130">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="8dea0-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8dea0-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8dea0-131">-Confirm</span></span>
<span data-ttu-id="8dea0-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8dea0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dea0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dea0-133">-WhatIf</span></span>
<span data-ttu-id="8dea0-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8dea0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dea0-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8dea0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dea0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dea0-136">CommonParameters</span></span>
<span data-ttu-id="8dea0-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dea0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dea0-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8dea0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dea0-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8dea0-139">INPUTS</span></span>

### <span data-ttu-id="8dea0-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8dea0-140">System.String</span></span>

### <span data-ttu-id="8dea0-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="8dea0-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="8dea0-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8dea0-142">OUTPUTS</span></span>

### <span data-ttu-id="8dea0-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="8dea0-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="8dea0-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8dea0-144">NOTES</span></span>

## <span data-ttu-id="8dea0-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8dea0-145">RELATED LINKS</span></span>
