---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 42592e1d72303c98a27890e2ac7721d95c37f928
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926512"
---
# <span data-ttu-id="ea724-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="ea724-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="ea724-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea724-102">SYNOPSIS</span></span>
<span data-ttu-id="ea724-103">Das New-AzVirtualHubVnetConnection erstellt eine HubVirtualNetworkConnection-Ressource, die ein virtuelles Netzwerk mit dem virtuellen Azure Hub vergleicht.</span><span class="sxs-lookup"><span data-stu-id="ea724-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="ea724-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea724-104">SYNTAX</span></span>

### <span data-ttu-id="ea724-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="ea724-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea724-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="ea724-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea724-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="ea724-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea724-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="ea724-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea724-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="ea724-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea724-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="ea724-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea724-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea724-111">DESCRIPTION</span></span>
<span data-ttu-id="ea724-112">Das New-AzVirtualHubVnetConnection erstellt eine HubVirtualNetworkConnection-Ressource, die ein virtuelles Netzwerk mit dem virtuellen Azure Hub vergleicht.</span><span class="sxs-lookup"><span data-stu-id="ea724-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="ea724-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ea724-113">EXAMPLES</span></span>

### <span data-ttu-id="ea724-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ea724-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : False
ProvisioningState    : Succeeded
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

<span data-ttu-id="ea724-115">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub in Zentral USA in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="ea724-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="ea724-116">Anschließend wird eine virtuelle Netzwerkverbindung erstellt, die das virtuelle Netzwerk mit dem virtuellen Hub vergleicht.</span><span class="sxs-lookup"><span data-stu-id="ea724-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

### <span data-ttu-id="ea724-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ea724-117">Example 2</span></span>

<span data-ttu-id="ea724-118">Das New-AzVirtualHubVnetConnection erstellt eine HubVirtualNetworkConnection-Ressource, die ein virtuelles Netzwerk mit dem virtuellen Azure Hub vergleicht.</span><span class="sxs-lookup"><span data-stu-id="ea724-118">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span> <span data-ttu-id="ea724-119">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="ea724-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVirtualHubVnetConnection -EnableInternetSecurity -Name 'testvnetconnection' -ParentResourceName 'westushub' -RemoteVirtualNetwork <PSVirtualNetwork> -ResourceGroupName 'testRG'
```


### <span data-ttu-id="ea724-120">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ea724-120">Example 3</span></span>
```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName $rgName -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $rt1 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "defaultRouteTable"
PS C:\> $rt2 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "noneRouteTable"
PS C:\> $route1 = New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16")-NextHopIpAddress "10.90.0.5"
PS C:\> $routingconfig = New-AzRoutingConfiguration -AssociatedRouteTable $rt1.Id -Label @("testLabel") -Id @($rt2.Id) -StaticRoute @($route1)

AssociatedRouteTable  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable"
PropagatedRouteTables : {
                          "Labels": [
                            "testLabel"
                          ],
                          "Ids": [
                            {
                              "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "route1",
                              "AddressPrefixes": [
                                "10.20.0.0/16",
                                "10.30.0.0/16"
                              ],
                              "NextHopIpAddress": "10.90.0.5"
                            }
                          ]
                        }
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork -RoutingConfiguration $routingconfig
```
<span data-ttu-id="ea724-121">Mit dem vorstehenden Wird wird eine neue Routingkonfiguration erstellt und statische Routen in der Routingkonfiguration mit dem nächsten Hop als angegebene IP-Adresse erstellt.</span><span class="sxs-lookup"><span data-stu-id="ea724-121">The above will create a new routing configuration and create static routes in the routing config with the next hop as a specified IP address.</span></span> <span data-ttu-id="ea724-122">Diese Routingkonfiguration kann dann als Parameter -RoutingConfiguration an den Befehl New-AzVirtualHubVnetConnection übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="ea724-122">This routing configuration can then be passed into  the New-AzVirtualHubVnetConnection command as the parameter -RoutingConfiguration.</span></span>

## <span data-ttu-id="ea724-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ea724-123">PARAMETERS</span></span>

### <span data-ttu-id="ea724-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea724-124">-AsJob</span></span>
<span data-ttu-id="ea724-125">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ea724-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea724-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea724-126">-DefaultProfile</span></span>
<span data-ttu-id="ea724-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea724-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea724-128">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="ea724-128">-EnableInternetSecurity</span></span>
<span data-ttu-id="ea724-129">Aktivieren der Internetsicherheit für diese Verbindung</span><span class="sxs-lookup"><span data-stu-id="ea724-129">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="ea724-130">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="ea724-130">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="ea724-131">Aktivieren der Internetsicherheit für diese Verbindung</span><span class="sxs-lookup"><span data-stu-id="ea724-131">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="ea724-132">-Name</span><span class="sxs-lookup"><span data-stu-id="ea724-132">-Name</span></span>
<span data-ttu-id="ea724-133">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="ea724-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea724-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ea724-134">-ParentObject</span></span>
<span data-ttu-id="ea724-135">Die übergeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="ea724-135">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea724-136">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ea724-136">-ParentResourceId</span></span>
<span data-ttu-id="ea724-137">Die übergeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="ea724-137">The parent resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea724-138">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="ea724-138">-ParentResourceName</span></span>
<span data-ttu-id="ea724-139">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ea724-139">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea724-140">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ea724-140">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="ea724-141">Das virtuelle Remotenetzwerk, mit dem diese virtuelle Netzwerkverbindung des Hubs verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="ea724-141">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea724-142">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="ea724-142">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="ea724-143">Das virtuelle Remotenetzwerk, mit dem diese virtuelle Netzwerkverbindung des Hubs verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="ea724-143">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea724-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea724-144">-ResourceGroupName</span></span>
<span data-ttu-id="ea724-145">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ea724-145">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea724-146">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea724-146">-RoutingConfiguration</span></span>
<span data-ttu-id="ea724-147">Routingkonfiguration für diese Verbindung</span><span class="sxs-lookup"><span data-stu-id="ea724-147">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="ea724-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ea724-148">-Confirm</span></span>
<span data-ttu-id="ea724-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ea724-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea724-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea724-150">-WhatIf</span></span>
<span data-ttu-id="ea724-151">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea724-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea724-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ea724-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea724-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea724-153">CommonParameters</span></span>
<span data-ttu-id="ea724-154">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea724-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea724-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea724-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea724-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ea724-156">INPUTS</span></span>

### <span data-ttu-id="ea724-157">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ea724-157">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="ea724-158">System.String</span><span class="sxs-lookup"><span data-stu-id="ea724-158">System.String</span></span>

## <span data-ttu-id="ea724-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ea724-159">OUTPUTS</span></span>

### <span data-ttu-id="ea724-160">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="ea724-160">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="ea724-161">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ea724-161">NOTES</span></span>

## <span data-ttu-id="ea724-162">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ea724-162">RELATED LINKS</span></span>

[<span data-ttu-id="ea724-163">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="ea724-163">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="ea724-164">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="ea724-164">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="ea724-165">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea724-165">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
