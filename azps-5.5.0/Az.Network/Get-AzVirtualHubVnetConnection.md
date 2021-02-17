---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 688168317a622cb0375bb111050f3e54696047ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147097"
---
# <span data-ttu-id="e3980-101">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e3980-101">Get-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="e3980-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3980-102">SYNOPSIS</span></span>
<span data-ttu-id="e3980-103">Ruft eine virtuelle Netzwerkverbindung in einem virtuellen Hub ab oder listet alle virtuellen Netzwerkverbindungen in einem virtuellen Hub auf.</span><span class="sxs-lookup"><span data-stu-id="e3980-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="e3980-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3980-104">SYNTAX</span></span>

### <span data-ttu-id="e3980-105">ByVirtualHubName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e3980-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3980-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="e3980-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3980-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="e3980-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3980-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3980-108">DESCRIPTION</span></span>
<span data-ttu-id="e3980-109">Ruft eine virtuelle Netzwerkverbindung in einem virtuellen Hub ab oder listet alle virtuellen Netzwerkverbindungen in einem virtuellen Hub auf.</span><span class="sxs-lookup"><span data-stu-id="e3980-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="e3980-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e3980-110">EXAMPLES</span></span>

### <span data-ttu-id="e3980-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e3980-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
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

<span data-ttu-id="e3980-112">Im vorstehenden Beispiel wird eine Ressourcengruppe, ein virtuelles WAN, ein virtuelles Netzwerk und ein virtueller Hub in zentralen USA in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="e3980-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="e3980-113">Anschließend wird eine virtuelle Netzwerkverbindung erstellt, die das virtuelle Netzwerk mit dem virtuellen Hub vergleicht.</span><span class="sxs-lookup"><span data-stu-id="e3980-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="e3980-114">Nachdem die virtuelle Hubnetzwerkverbindung erstellt wurde, ruft sie die virtuelle Hubnetzwerkverbindung unter Verwendung des Ressourcengruppennamens, des Hubnamens und des Verbindungsnamens ab.</span><span class="sxs-lookup"><span data-stu-id="e3980-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="e3980-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e3980-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
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

<span data-ttu-id="e3980-116">Im vorstehenden Beispiel wird eine Ressourcengruppe, ein virtuelles WAN, ein virtuelles Netzwerk und ein virtueller Hub in zentralen USA in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="e3980-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="e3980-117">Anschließend wird eine virtuelle Netzwerkverbindung erstellt, die das virtuelle Netzwerk mit dem virtuellen Hub vergleicht.</span><span class="sxs-lookup"><span data-stu-id="e3980-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="e3980-118">Nachdem die virtuelle Hubnetzwerkverbindung erstellt wurde, werden alle virtuellen Hubnetzwerkverbindungen unter Verwendung des Ressourcengruppennamens und des Hubnamens aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3980-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

### <span data-ttu-id="e3980-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e3980-119">Example 3</span></span>

```powershell
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name test*

Name                 : testvnetconnection1
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection1
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
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

Name                 : testvnetconnection2
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection2
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
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

<span data-ttu-id="e3980-120">Dieses Cmdlet listet alle virtuellen Hubnetzwerkverbindungen auf, beginnend mit "Test", und verwendet dazu den Namen der Ressourcengruppe und den Hubnamen.</span><span class="sxs-lookup"><span data-stu-id="e3980-120">This cmdlet lists all the hub virtual network connections starting with "test" using its resource group name and the hub name.</span></span>

## <span data-ttu-id="e3980-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3980-121">PARAMETERS</span></span>

### <span data-ttu-id="e3980-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3980-122">-DefaultProfile</span></span>
<span data-ttu-id="e3980-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3980-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3980-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e3980-124">-Name</span></span>
<span data-ttu-id="e3980-125">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="e3980-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="e3980-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e3980-126">-ParentObject</span></span>
<span data-ttu-id="e3980-127">Die übergeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="e3980-127">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3980-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e3980-128">-ParentResourceId</span></span>
<span data-ttu-id="e3980-129">Die übergeordnete Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="e3980-129">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3980-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="e3980-130">-ParentResourceName</span></span>
<span data-ttu-id="e3980-131">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="e3980-131">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3980-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3980-132">-ResourceGroupName</span></span>
<span data-ttu-id="e3980-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e3980-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3980-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3980-134">CommonParameters</span></span>
<span data-ttu-id="e3980-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3980-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3980-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3980-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3980-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e3980-137">INPUTS</span></span>

### <span data-ttu-id="e3980-138">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e3980-138">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="e3980-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e3980-139">System.String</span></span>

## <span data-ttu-id="e3980-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e3980-140">OUTPUTS</span></span>

### <span data-ttu-id="e3980-141">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="e3980-141">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="e3980-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e3980-142">NOTES</span></span>

## <span data-ttu-id="e3980-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e3980-143">RELATED LINKS</span></span>

[<span data-ttu-id="e3980-144">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e3980-144">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="e3980-145">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e3980-145">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)
