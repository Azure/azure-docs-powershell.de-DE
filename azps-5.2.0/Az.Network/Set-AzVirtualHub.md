---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
ms.openlocfilehash: 12bf5d24421f79eecb3138a68425968b9b4fbe62
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357466"
---
# <span data-ttu-id="1559c-101">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1559c-101">Set-AzVirtualHub</span></span>

## <span data-ttu-id="1559c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1559c-102">SYNOPSIS</span></span>
<span data-ttu-id="1559c-103">Ändert einen virtuellen Hub, um eine virtuelle Tabelle "HUb-Route" hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1559c-103">Modifies a Virtual Hub to add a Virtual HUb Route Table to it.</span></span>

## <span data-ttu-id="1559c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1559c-104">SYNTAX</span></span>

### <span data-ttu-id="1559c-105">ByVirtualHubName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1559c-105">ByVirtualHubName (Default)</span></span>
```
Set-AzVirtualHub -ResourceGroupName <String> -Name <String> -RouteTable <PSVirtualHubRouteTable[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1559c-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="1559c-106">ByVirtualHubResourceId</span></span>
```
Set-AzVirtualHub -ResourceId <String> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1559c-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="1559c-107">ByVirtualHubObject</span></span>
```
Set-AzVirtualHub -InputObject <PSVirtualHub> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1559c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1559c-108">DESCRIPTION</span></span>
<span data-ttu-id="1559c-109">{{ Geben Sie die Beschreibung }} ein.</span><span class="sxs-lookup"><span data-stu-id="1559c-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="1559c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1559c-110">EXAMPLES</span></span>

### <span data-ttu-id="1559c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1559c-111">Example 1</span></span>
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

<span data-ttu-id="1559c-112">Zuerst erstellen wir ein Virtual Hub Route-Objekt und verwenden es zum Erstellen einer Ressource der Tabelle "Virtual Hub Route".</span><span class="sxs-lookup"><span data-stu-id="1559c-112">First we create a Virtual Hub Route object, and use it to create a Virtual Hub Route Table resource.</span></span> <span data-ttu-id="1559c-113">Anschließend legen wir diese Routentabelleressource mithilfe des Befehls "Set-AzVirtualHub" auf den virtuellen Set-AzVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="1559c-113">Then we set this route table resource to the virtual hub using the Set-AzVirtualHub command.</span></span>

## <span data-ttu-id="1559c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1559c-114">PARAMETERS</span></span>

### <span data-ttu-id="1559c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1559c-115">-AsJob</span></span>
<span data-ttu-id="1559c-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1559c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1559c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1559c-117">-DefaultProfile</span></span>
<span data-ttu-id="1559c-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1559c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1559c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1559c-119">-InputObject</span></span>
<span data-ttu-id="1559c-120">Das zu ändernde virtuelle Hubobjekt.</span><span class="sxs-lookup"><span data-stu-id="1559c-120">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="1559c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1559c-121">-Name</span></span>
<span data-ttu-id="1559c-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="1559c-122">The resource name.</span></span>

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

### <span data-ttu-id="1559c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1559c-123">-ResourceGroupName</span></span>
<span data-ttu-id="1559c-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1559c-124">The resource group name.</span></span>

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

### <span data-ttu-id="1559c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1559c-125">-ResourceId</span></span>
<span data-ttu-id="1559c-126">Die Ressourcen-ID des virtuellen Hubs, der geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1559c-126">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="1559c-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="1559c-127">-RouteTable</span></span>
<span data-ttu-id="1559c-128">Die diesem virtuellen Hub zugeordneten Routentabellen.</span><span class="sxs-lookup"><span data-stu-id="1559c-128">The route tables associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="1559c-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="1559c-129">-Tag</span></span>
<span data-ttu-id="1559c-130">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="1559c-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1559c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1559c-131">-Confirm</span></span>
<span data-ttu-id="1559c-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1559c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1559c-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1559c-133">-WhatIf</span></span>
<span data-ttu-id="1559c-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1559c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1559c-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1559c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1559c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1559c-136">CommonParameters</span></span>
<span data-ttu-id="1559c-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1559c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1559c-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1559c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1559c-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1559c-139">INPUTS</span></span>

### <span data-ttu-id="1559c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="1559c-140">System.String</span></span>

### <span data-ttu-id="1559c-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1559c-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="1559c-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1559c-142">OUTPUTS</span></span>

### <span data-ttu-id="1559c-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1559c-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="1559c-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1559c-144">NOTES</span></span>

## <span data-ttu-id="1559c-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1559c-145">RELATED LINKS</span></span>
