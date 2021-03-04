---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 1454e3ba3fc3a7e229e064a32146ebddddc19392
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918408"
---
# <span data-ttu-id="dd5fd-101">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="dd5fd-101">Update-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="dd5fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd5fd-102">SYNOPSIS</span></span>
<span data-ttu-id="dd5fd-103">Aktualisiert eine vorhandene HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="dd5fd-103">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="dd5fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd5fd-104">SYNTAX</span></span>

### <span data-ttu-id="dd5fd-105">ByHubVirtualNetworkConnectionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="dd5fd-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd5fd-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="dd5fd-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Update-AzVirtualHubVnetConnection -InputObject <PSHubVirtualNetworkConnection>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd5fd-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="dd5fd-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceId <String> [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd5fd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd5fd-108">DESCRIPTION</span></span>
<span data-ttu-id="dd5fd-109">Aktualisiert eine vorhandene HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="dd5fd-109">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="dd5fd-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dd5fd-110">EXAMPLES</span></span>

### <span data-ttu-id="dd5fd-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dd5fd-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Update-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -EnableInternetSecurity $true
Name                   : testvnetconnection
Id                     : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : True
ProvisioningState      : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }
```

<span data-ttu-id="dd5fd-112">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub in Zentral USA in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="dd5fd-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="dd5fd-113">Außerdem wird eine virtuelle Netzwerkverbindung erstellt, bei der es sich um einen Peer des virtuellen Netzwerks mit dem virtuellen Hub handelt.</span><span class="sxs-lookup"><span data-stu-id="dd5fd-113">A Virtual Network Connection is also created which is peer the Virtual Network to the Virtual Hub.</span></span> <span data-ttu-id="dd5fd-114">Diese virtuelle Netzwerkverbindung wird dann aktualisiert, um die Internetsicherheit zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="dd5fd-114">This Virtual Network Connection is then updated to enable internet security.</span></span>

## <span data-ttu-id="dd5fd-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dd5fd-115">PARAMETERS</span></span>

### <span data-ttu-id="dd5fd-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd5fd-116">-AsJob</span></span>
<span data-ttu-id="dd5fd-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="dd5fd-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd5fd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd5fd-118">-DefaultProfile</span></span>
<span data-ttu-id="dd5fd-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd5fd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5fd-120">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="dd5fd-120">-EnableInternetSecurity</span></span>
<span data-ttu-id="dd5fd-121">Aktivieren Sie die Internetsicherheit für diese Verbindung.</span><span class="sxs-lookup"><span data-stu-id="dd5fd-121">Enable internet security for this connection.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5fd-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd5fd-122">-InputObject</span></span>
<span data-ttu-id="dd5fd-123">Die zu ändernde hubvirtualnetworkconnection-Ressource.</span><span class="sxs-lookup"><span data-stu-id="dd5fd-123">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd5fd-124">-Name</span><span class="sxs-lookup"><span data-stu-id="dd5fd-124">-Name</span></span>
<span data-ttu-id="dd5fd-125">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="dd5fd-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: ResourceName, HubVirtualNetworkConnectionName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5fd-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="dd5fd-126">-ParentResourceName</span></span>
<span data-ttu-id="dd5fd-127">Der übergeordnete Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="dd5fd-127">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: VirtualHubName, ParentVirtualHubName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5fd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd5fd-128">-ResourceGroupName</span></span>
<span data-ttu-id="dd5fd-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dd5fd-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5fd-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd5fd-130">-ResourceId</span></span>
<span data-ttu-id="dd5fd-131">Die Ressourcen-ID der zu ändernden Hubvirtualnetworkconnection-Ressource.</span><span class="sxs-lookup"><span data-stu-id="dd5fd-131">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionResourceId
Aliases: HubVirtualNetworkConnectionId
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd5fd-132">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd5fd-132">-RoutingConfiguration</span></span>
<span data-ttu-id="dd5fd-133">Routingkonfiguration für diese Verbindung</span><span class="sxs-lookup"><span data-stu-id="dd5fd-133">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5fd-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd5fd-134">-Confirm</span></span>
<span data-ttu-id="dd5fd-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd5fd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd5fd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd5fd-136">-WhatIf</span></span>
<span data-ttu-id="dd5fd-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd5fd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd5fd-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd5fd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd5fd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd5fd-139">CommonParameters</span></span>
<span data-ttu-id="dd5fd-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd5fd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd5fd-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd5fd-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd5fd-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dd5fd-142">INPUTS</span></span>

### <span data-ttu-id="dd5fd-143">System.String</span><span class="sxs-lookup"><span data-stu-id="dd5fd-143">System.String</span></span>

### <span data-ttu-id="dd5fd-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="dd5fd-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="dd5fd-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dd5fd-145">OUTPUTS</span></span>

### <span data-ttu-id="dd5fd-146">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="dd5fd-146">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="dd5fd-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dd5fd-147">NOTES</span></span>

## <span data-ttu-id="dd5fd-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dd5fd-148">RELATED LINKS</span></span>

[<span data-ttu-id="dd5fd-149">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd5fd-149">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
