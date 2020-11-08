---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
ms.openlocfilehash: 3461d629eac47a1bbf2842d2cb0a913c2734f94e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165750"
---
# <span data-ttu-id="7687f-101">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7687f-101">Get-AzVHubRouteTable</span></span>

## <span data-ttu-id="7687f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7687f-102">SYNOPSIS</span></span>
<span data-ttu-id="7687f-103">Ruft eine Hub-Route-Tabellen Ressource ab, die einem VirtualHub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7687f-103">Retrieves  a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="7687f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7687f-104">SYNTAX</span></span>

### <span data-ttu-id="7687f-105">ByVHubRouteTableName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7687f-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Get-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7687f-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="7687f-106">ByVirtualHubObject</span></span>
```powershell
Get-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7687f-107">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="7687f-107">ByVHubRouteTableResourceId</span></span>
```powershell
Get-AzVHubRouteTable -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7687f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7687f-108">DESCRIPTION</span></span>
<span data-ttu-id="7687f-109">Ruft die angegebene Hub-Routingtabelle ab, die dem angegebenen virtuellen Hub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7687f-109">Gets the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="7687f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7687f-110">EXAMPLES</span></span>

### <span data-ttu-id="7687f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7687f-111">Example 1</span></span>

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

<span data-ttu-id="7687f-112">Dieser Befehl ruft die Hub-Route-Tabelle des virtuellen Hubs ab.</span><span class="sxs-lookup"><span data-stu-id="7687f-112">This command gets the hub route table of the virtual hub.</span></span>

### <span data-ttu-id="7687f-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7687f-113">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName


Name                   : defaultRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : []
AssociatedConnections  : []
PropagatingConnections : []


Name                   : noneRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : []
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="7687f-114">Dieser Befehl listet alle Hub-Route-Tabellen in der angegebenen VirtualHub auf.</span><span class="sxs-lookup"><span data-stu-id="7687f-114">This command lists all the hub route tables in the specified VirtualHub.</span></span>

## <span data-ttu-id="7687f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="7687f-115">PARAMETERS</span></span>

### <span data-ttu-id="7687f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7687f-116">-AsJob</span></span>
<span data-ttu-id="7687f-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7687f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7687f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7687f-118">-DefaultProfile</span></span>
<span data-ttu-id="7687f-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7687f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7687f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7687f-120">-Name</span></span>
<span data-ttu-id="7687f-121">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="7687f-121">The resource name.</span></span>

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

### <span data-ttu-id="7687f-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7687f-122">-ParentObject</span></span>
<span data-ttu-id="7687f-123">Das übergeordnete virtuelle Hub-Objekt dieser Ressource.</span><span class="sxs-lookup"><span data-stu-id="7687f-123">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="7687f-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="7687f-124">-ParentResourceName</span></span>
<span data-ttu-id="7687f-125">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="7687f-125">The parent resource name.</span></span>

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

### <span data-ttu-id="7687f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7687f-126">-ResourceGroupName</span></span>
<span data-ttu-id="7687f-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7687f-127">The resource group name.</span></span>

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

### <span data-ttu-id="7687f-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7687f-128">-ResourceId</span></span>
<span data-ttu-id="7687f-129">Die Ressourcen-ID der abzurufenden vhubroutetable-Ressource.</span><span class="sxs-lookup"><span data-stu-id="7687f-129">The resource id of the vhubroutetable resource to Get.</span></span>

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

### <span data-ttu-id="7687f-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7687f-130">-Confirm</span></span>
<span data-ttu-id="7687f-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7687f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7687f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7687f-132">-WhatIf</span></span>
<span data-ttu-id="7687f-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7687f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7687f-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7687f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7687f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7687f-135">CommonParameters</span></span>
<span data-ttu-id="7687f-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7687f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7687f-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7687f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7687f-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7687f-138">INPUTS</span></span>

### <span data-ttu-id="7687f-139">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7687f-139">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="7687f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7687f-140">System.String</span></span>

## <span data-ttu-id="7687f-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7687f-141">OUTPUTS</span></span>

### <span data-ttu-id="7687f-142">Microsoft. Azure. Commands. Network. Models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7687f-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="7687f-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="7687f-143">NOTES</span></span>

## <span data-ttu-id="7687f-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7687f-144">RELATED LINKS</span></span>

[<span data-ttu-id="7687f-145">Neu – AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="7687f-145">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="7687f-146">Neu – AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7687f-146">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="7687f-147">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7687f-147">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)

[<span data-ttu-id="7687f-148">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7687f-148">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)