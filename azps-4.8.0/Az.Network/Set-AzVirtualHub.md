---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
ms.openlocfilehash: 12bf5d24421f79eecb3138a68425968b9b4fbe62
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174267"
---
# <span data-ttu-id="65d5d-101">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="65d5d-101">Set-AzVirtualHub</span></span>

## <span data-ttu-id="65d5d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65d5d-102">SYNOPSIS</span></span>
<span data-ttu-id="65d5d-103">Ändert einen virtuellen Hub, um ihm eine virtuelle Hub-Routingtabelle hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="65d5d-103">Modifies a Virtual Hub to add a Virtual HUb Route Table to it.</span></span>

## <span data-ttu-id="65d5d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65d5d-104">SYNTAX</span></span>

### <span data-ttu-id="65d5d-105">ByVirtualHubName (Standard)</span><span class="sxs-lookup"><span data-stu-id="65d5d-105">ByVirtualHubName (Default)</span></span>
```
Set-AzVirtualHub -ResourceGroupName <String> -Name <String> -RouteTable <PSVirtualHubRouteTable[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65d5d-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="65d5d-106">ByVirtualHubResourceId</span></span>
```
Set-AzVirtualHub -ResourceId <String> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65d5d-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="65d5d-107">ByVirtualHubObject</span></span>
```
Set-AzVirtualHub -InputObject <PSVirtualHub> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65d5d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65d5d-108">DESCRIPTION</span></span>
<span data-ttu-id="65d5d-109">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="65d5d-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="65d5d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65d5d-110">EXAMPLES</span></span>

### <span data-ttu-id="65d5d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="65d5d-111">Example 1</span></span>
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

<span data-ttu-id="65d5d-112">Zunächst erstellen wir ein virtuelles Hub-Routing-Objekt und verwenden es zum Erstellen einer virtuellen Hub-Routing-Tabellen Ressource.</span><span class="sxs-lookup"><span data-stu-id="65d5d-112">First we create a Virtual Hub Route object, and use it to create a Virtual Hub Route Table resource.</span></span> <span data-ttu-id="65d5d-113">Anschließend legen wir diese Routingtabellen Ressource mit dem Befehl Set-AzVirtualHub auf den virtuellen Hub.</span><span class="sxs-lookup"><span data-stu-id="65d5d-113">Then we set this route table resource to the virtual hub using the Set-AzVirtualHub command.</span></span>

## <span data-ttu-id="65d5d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="65d5d-114">PARAMETERS</span></span>

### <span data-ttu-id="65d5d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65d5d-115">-AsJob</span></span>
<span data-ttu-id="65d5d-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="65d5d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65d5d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d5d-117">-DefaultProfile</span></span>
<span data-ttu-id="65d5d-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65d5d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65d5d-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="65d5d-119">-InputObject</span></span>
<span data-ttu-id="65d5d-120">Das virtuelle Hub-Objekt, das geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="65d5d-120">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="65d5d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="65d5d-121">-Name</span></span>
<span data-ttu-id="65d5d-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="65d5d-122">The resource name.</span></span>

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

### <span data-ttu-id="65d5d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65d5d-123">-ResourceGroupName</span></span>
<span data-ttu-id="65d5d-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="65d5d-124">The resource group name.</span></span>

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

### <span data-ttu-id="65d5d-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="65d5d-125">-ResourceId</span></span>
<span data-ttu-id="65d5d-126">Die Ressourcen-ID des virtuellen Hubs, der geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="65d5d-126">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="65d5d-127">-Routel</span><span class="sxs-lookup"><span data-stu-id="65d5d-127">-RouteTable</span></span>
<span data-ttu-id="65d5d-128">Die Routentabellen, die diesem virtuellen Hub zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="65d5d-128">The route tables associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="65d5d-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="65d5d-129">-Tag</span></span>
<span data-ttu-id="65d5d-130">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="65d5d-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="65d5d-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="65d5d-131">-Confirm</span></span>
<span data-ttu-id="65d5d-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="65d5d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65d5d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65d5d-133">-WhatIf</span></span>
<span data-ttu-id="65d5d-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65d5d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65d5d-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="65d5d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65d5d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d5d-136">CommonParameters</span></span>
<span data-ttu-id="65d5d-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65d5d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d5d-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65d5d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d5d-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65d5d-139">INPUTS</span></span>

### <span data-ttu-id="65d5d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="65d5d-140">System.String</span></span>

### <span data-ttu-id="65d5d-141">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="65d5d-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="65d5d-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65d5d-142">OUTPUTS</span></span>

### <span data-ttu-id="65d5d-143">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="65d5d-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="65d5d-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="65d5d-144">NOTES</span></span>

## <span data-ttu-id="65d5d-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65d5d-145">RELATED LINKS</span></span>
