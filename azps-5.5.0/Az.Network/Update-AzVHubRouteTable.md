---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
ms.openlocfilehash: d330b7e25cc1184a3efaea2c3deb569bf44171b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160516"
---
# <span data-ttu-id="8e888-101">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8e888-101">Update-AzVHubRouteTable</span></span>

## <span data-ttu-id="8e888-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e888-102">SYNOPSIS</span></span>
<span data-ttu-id="8e888-103">Löschen Sie eine Hubroutentabelle, die einem VirtualHub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8e888-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="8e888-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e888-104">SYNTAX</span></span>

### <span data-ttu-id="8e888-105">ByVHubRouteTableName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e888-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Update-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String>[-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e888-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="8e888-106">ByVirtualHubObject</span></span>
```powershell
Update-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e888-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="8e888-107">ByVHubRouteTableObject</span></span>
```powershell
Update-AzVHubRouteTable -InputObject <PSVHubRouteTable> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e888-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="8e888-108">ByVHubRouteTableResourceId</span></span>
```powershell
Update-AzVHubRouteTable -ResourceId <String> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e888-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e888-109">DESCRIPTION</span></span>
<span data-ttu-id="8e888-110">Aktualisiert die angegebene Routentabelle, die dem angegebenen virtuellen Hub mit den bereitgestellten Routen oder Bezeichnungen verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="8e888-110">Updates the specified route table that is associated with the specified virtual hub with the provided routes or the labels.</span></span>

## <span data-ttu-id="8e888-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e888-111">EXAMPLES</span></span>

### <span data-ttu-id="8e888-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8e888-112">Example 1</span></span>
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
PS C:\> Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"

PS C:\> $route2 = New-AzVHubRoute -Name "internet-traffic" -Destination @("0.0.0.0/0") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"
PS C:\> Update-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable" -Route @($route2)
PS C:\> Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"

Name                   : testRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/testRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : [
                           {
                             "Name": "internet-traffic",
                             "DestinationType": "CIDR",
                             "Destinations": [
                               "0.0.0.0/0"
                             ],
                             "NextHopType": "ResourceId",
                             "NextHop": "/subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall"
                           }
                         ]
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="8e888-113">Mit diesem Befehl wird die Hubroutentabelle des virtuellen Hubs gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8e888-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="8e888-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e888-114">PARAMETERS</span></span>

### <span data-ttu-id="8e888-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e888-115">-AsJob</span></span>
<span data-ttu-id="8e888-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8e888-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e888-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e888-117">-DefaultProfile</span></span>
<span data-ttu-id="8e888-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e888-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e888-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e888-119">-InputObject</span></span>
<span data-ttu-id="8e888-120">Die zu aktualisierende vhubroutetable-Ressource.</span><span class="sxs-lookup"><span data-stu-id="8e888-120">The vhubroutetable resource to Update.</span></span>

```yaml
Type: PSVHubRouteTable
Parameter Sets: ByVHubRouteTableObject
Aliases: VHubRouteTable, RouteTable

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e888-121">-Label</span><span class="sxs-lookup"><span data-stu-id="8e888-121">-Label</span></span>
<span data-ttu-id="8e888-122">Die Liste der Etiketten.</span><span class="sxs-lookup"><span data-stu-id="8e888-122">The list of labels.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e888-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8e888-123">-Name</span></span>
<span data-ttu-id="8e888-124">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="8e888-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e888-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8e888-125">-ParentObject</span></span>
<span data-ttu-id="8e888-126">Das übergeordnete virtuelle Hubobjekt dieser Ressource.</span><span class="sxs-lookup"><span data-stu-id="8e888-126">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="8e888-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="8e888-127">-ParentResourceName</span></span>
<span data-ttu-id="8e888-128">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="8e888-128">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e888-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e888-129">-ResourceGroupName</span></span>
<span data-ttu-id="8e888-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8e888-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e888-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e888-131">-ResourceId</span></span>
<span data-ttu-id="8e888-132">Die Ressourcen-ID der zu aktualisierende vhubroutetable-Ressource.</span><span class="sxs-lookup"><span data-stu-id="8e888-132">The resource id of the vhubroutetable resource to Update.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableResourceId
Aliases: VHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e888-133">-Route</span><span class="sxs-lookup"><span data-stu-id="8e888-133">-Route</span></span>
<span data-ttu-id="8e888-134">Die Liste der Routen für diese Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="8e888-134">The list of routes for this route table.</span></span>

```yaml
Type: PSVHubRoute[]
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e888-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e888-135">-Confirm</span></span>
<span data-ttu-id="8e888-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e888-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e888-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8e888-137">-WhatIf</span></span>
<span data-ttu-id="8e888-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e888-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e888-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e888-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e888-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e888-140">CommonParameters</span></span>
<span data-ttu-id="8e888-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e888-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e888-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e888-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e888-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e888-143">INPUTS</span></span>

### <span data-ttu-id="8e888-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="8e888-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="8e888-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8e888-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="8e888-146">System.String</span><span class="sxs-lookup"><span data-stu-id="8e888-146">System.String</span></span>

## <span data-ttu-id="8e888-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e888-147">OUTPUTS</span></span>

### <span data-ttu-id="8e888-148">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8e888-148">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="8e888-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8e888-149">NOTES</span></span>

## <span data-ttu-id="8e888-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8e888-150">RELATED LINKS</span></span>

[<span data-ttu-id="8e888-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8e888-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="8e888-152">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="8e888-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="8e888-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8e888-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="8e888-154">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8e888-154">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)