---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
ms.openlocfilehash: d9c7b4895d05b4f55ef91705062db7c200d702cf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178745"
---
# <span data-ttu-id="8fda9-101">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8fda9-101">New-AzVHubRouteTable</span></span>

## <span data-ttu-id="8fda9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8fda9-102">SYNOPSIS</span></span>
<span data-ttu-id="8fda9-103">Erstellt eine Hub-Route-Tabellen Ressource, die einem VirtualHub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8fda9-103">Creates a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="8fda9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fda9-104">SYNTAX</span></span>

### <span data-ttu-id="8fda9-105">ByVirtualHubName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8fda9-105">ByVirtualHubName (Default)</span></span>

```powershell
New-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fda9-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="8fda9-106">ByVirtualHubObject</span></span>

```powershell
New-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fda9-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="8fda9-107">ByVirtualHubResourceId</span></span>

```powershell
New-AzVHubRouteTable -ParentResourceId <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fda9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8fda9-108">DESCRIPTION</span></span>
<span data-ttu-id="8fda9-109">Erstellt die angegebene Routingtabelle, die dem angegebenen virtuellen Hub mit den bereitgestellten Routen und den Beschriftungen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8fda9-109">Creates the specified route table that is associated with the specified virtual hub with the provided routes and the labels.</span></span>

## <span data-ttu-id="8fda9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8fda9-110">EXAMPLES</span></span>

### <span data-ttu-id="8fda9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8fda9-111">Example 1</span></span>

```powershell
PS C:\> New-AzVirtualWan -ResourceGroupName "testRg" -Name "testWan" -Location "westcentralus" -VirtualWANType "Standard" -AllowVnetToVnetTraffic -AllowBranchToBranchTraffic
PS C:\> $virtualWan = Get-AzVirtualWan -ResourceGroupName "testRg" -Name "testWan"

PS C:\> New-AzVirtualHub -ResourceGroupName "testRg" -Name "testHub" -Location "westcentralus" -AddressPrefix "10.0.0.0/16" -VirtualWan $virtualWan
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName "testRg" -Name "testHub"

PS C:\> $fwIp = New-AzFirewallHubPublicIpAddress -Count 1
PS C:\> $hubIpAddresses = New-AzFirewallHubIpAddress -PublicIP $fwIp
PS C:\> New-AzFirewall -Name "testFirewall" -ResourceGroupName "testRg" -Location "westcentralus" -Sku AZFW_Hub -VirtualHubId $virtualHub.Id -HubIPAddress $hubIpAddresses
PS C:\> $firewall = Get-AzFirewall -Name "testFirewall" -ResourceGroupName "testRg"

PS C:\> $route1 = New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"
PS C:\> New-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable" -Route @($route1) -Label @("testLabel")

Name                   : testRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/testRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : [
                           {
                             "Name": "private-traffic",
                             "DestinationType": "CIDR",
                             "Destinations": [
                               "10.30.0.0/16",
                               "10.40.0.0/16"
                             ],
                             "NextHopType": "ResourceId",
                             "NextHop": "/subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall"
                           }
                         ]
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="8fda9-112">Mit diesem Befehl wird eine Hub-Route-Tabelle des virtuellen Hubs erstellt.</span><span class="sxs-lookup"><span data-stu-id="8fda9-112">This command creates a hub route table of the virtual hub.</span></span>

## <span data-ttu-id="8fda9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fda9-113">PARAMETERS</span></span>

### <span data-ttu-id="8fda9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8fda9-114">-AsJob</span></span>
<span data-ttu-id="8fda9-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8fda9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8fda9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fda9-116">-DefaultProfile</span></span>
<span data-ttu-id="8fda9-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8fda9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fda9-118">-Label</span><span class="sxs-lookup"><span data-stu-id="8fda9-118">-Label</span></span>
<span data-ttu-id="8fda9-119">Die Liste der Beschriftungen.</span><span class="sxs-lookup"><span data-stu-id="8fda9-119">The list of labels.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fda9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8fda9-120">-Name</span></span>
<span data-ttu-id="8fda9-121">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="8fda9-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fda9-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8fda9-122">-ParentObject</span></span>
<span data-ttu-id="8fda9-123">Das übergeordnete virtuelle Hub-Objekt dieser Ressource.</span><span class="sxs-lookup"><span data-stu-id="8fda9-123">The parent virtual hub object of this resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fda9-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="8fda9-124">-ParentResourceName</span></span>
<span data-ttu-id="8fda9-125">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="8fda9-125">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fda9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fda9-126">-ResourceGroupName</span></span>
<span data-ttu-id="8fda9-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8fda9-127">The resource group name.</span></span>

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

### <span data-ttu-id="8fda9-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8fda9-128">-ParentResourceId</span></span>
<span data-ttu-id="8fda9-129">Die Ressourcen-ID der virtuellen Hub-Ressource.</span><span class="sxs-lookup"><span data-stu-id="8fda9-129">The resource id of the virtual hub resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fda9-130">-Route</span><span class="sxs-lookup"><span data-stu-id="8fda9-130">-Route</span></span>
<span data-ttu-id="8fda9-131">Die Liste der Routen für diese Arbeitsplan Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8fda9-131">The list of routes for this route table.</span></span>

```yaml
Type: PSVHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fda9-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8fda9-132">-Confirm</span></span>
<span data-ttu-id="8fda9-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8fda9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fda9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fda9-134">-WhatIf</span></span>
<span data-ttu-id="8fda9-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8fda9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fda9-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8fda9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fda9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fda9-137">CommonParameters</span></span>
<span data-ttu-id="8fda9-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fda9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fda9-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8fda9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fda9-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8fda9-140">INPUTS</span></span>

### <span data-ttu-id="8fda9-141">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="8fda9-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="8fda9-142">Microsoft. Azure. Commands. Network. Models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8fda9-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="8fda9-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8fda9-143">System.String</span></span>

## <span data-ttu-id="8fda9-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8fda9-144">OUTPUTS</span></span>

### <span data-ttu-id="8fda9-145">Microsoft. Azure. Commands. Network. Models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8fda9-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="8fda9-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="8fda9-146">NOTES</span></span>

## <span data-ttu-id="8fda9-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8fda9-147">RELATED LINKS</span></span>

[<span data-ttu-id="8fda9-148">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8fda9-148">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="8fda9-149">Neu – AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="8fda9-149">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="8fda9-150">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8fda9-150">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="8fda9-151">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8fda9-151">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)
