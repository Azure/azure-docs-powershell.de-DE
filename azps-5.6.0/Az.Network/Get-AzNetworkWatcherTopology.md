---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatchertopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTopology.md
ms.openlocfilehash: 525dff96126c91d2d434d681bd49659513e7ec7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919763"
---
# <span data-ttu-id="4ebcd-101">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4ebcd-101">Get-AzNetworkWatcherTopology</span></span>

## <span data-ttu-id="4ebcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ebcd-102">SYNOPSIS</span></span>
<span data-ttu-id="4ebcd-103">Ruft eine Ansicht auf Netzwerkebene von Ressourcen und deren Beziehungen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="4ebcd-103">Gets a network level view of resources and their relationships in a resource group.</span></span>

## <span data-ttu-id="4ebcd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ebcd-104">SYNTAX</span></span>

### <span data-ttu-id="4ebcd-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="4ebcd-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTopology -NetworkWatcher <PSNetworkWatcher> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ebcd-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4ebcd-106">SetByName</span></span>
```
Get-AzNetworkWatcherTopology -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ebcd-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4ebcd-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTopology -Location <String> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ebcd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ebcd-108">DESCRIPTION</span></span>
<span data-ttu-id="4ebcd-109">Das Get-AzNetworkWatcherTopology cmdlet eine Ansicht auf Netzwerkebene von Ressourcen und deren Beziehungen in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4ebcd-109">The Get-AzNetworkWatcherTopology cmdlet a network level view of resources and their relationships in a resource group.</span></span> <span data-ttu-id="4ebcd-110">Hinweis: Wenn Sich Ressourcen aus mehreren Regionen in der Ressourcengruppe befinden, werden in der JSON-Ausgabe nur die Ressourcen in derselben Region wie die Network Watcher einbezogen.</span><span class="sxs-lookup"><span data-stu-id="4ebcd-110">Note: If resources from multiple regions reside in the resource group, only the resources in the same region as the Network Watcher will be included in the JSON output.</span></span>

## <span data-ttu-id="4ebcd-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4ebcd-111">EXAMPLES</span></span>

### <span data-ttu-id="4ebcd-112">Beispiel 1: Erstellen einer Azure-Topologie</span><span class="sxs-lookup"><span data-stu-id="4ebcd-112">Example 1: Get an Azure Topology</span></span>
```
$networkWatcher = Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG 
Get-AzNetworkWatcherTopology -NetworkWatcher $networkWatcher -ResourceGroupName testresourcegroup

Id                : e33d80cf-4f76-4b8f-b51c-5bb8eba80103
CreatedDateTime   : 0/00/0000 9:21:51 PM
LastModified      : 0/00/0000 4:53:29 AM
TopologyResources : [
                      {
                        "Name": "testresourcegroup-vnet",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "default",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "default",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                        "Location": "westcentralus",
                        "TopologyAssociations": []
                      },
                      {
                        "Name": "VM0",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Compute/virtualMachines/VM0",
                        "TopologyAssociations": [
                          {
                            "Name": "vm0131",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "vm0131",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "VM0",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Compute/virtualMachines/VM0",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "VM0-nsg",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "default",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "VM0-ip",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/publicIPAddresses/VM0-ip",
                            "AssociationType": "Associated"
                          }
                        ]
                      },
                      {
                        "Name": "VM0-nsg",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "default-allow-rdp",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg/securityRules/default-allow-rdp",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "default-allow-rdp",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg/securityRules/default-allow-rdp",
                        "Location": "westcentralus",
                        "TopologyAssociations": []
                      },
                      {
                        "Name": "VM0-ip",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/publicIPAddresses/VM0-ip",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "vm0131",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                            "AssociationType": "Associated"
                          }
                        ]
                      }
                    ]
```

<span data-ttu-id="4ebcd-113">In diesem Beispiel wird das cmdlet Get-AzNetworkWatcherTopology einer Ressourcengruppe ausgeführt, die eine VM, Nic, NSG und öffentliche IP enthält.</span><span class="sxs-lookup"><span data-stu-id="4ebcd-113">In this example we run the Get-AzNetworkWatcherTopology cmdlet on a resource group that contains a VM, Nic, NSG, and public IP.</span></span>

## <span data-ttu-id="4ebcd-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4ebcd-114">PARAMETERS</span></span>

### <span data-ttu-id="4ebcd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ebcd-115">-DefaultProfile</span></span>
<span data-ttu-id="4ebcd-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ebcd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ebcd-117">-Location</span><span class="sxs-lookup"><span data-stu-id="4ebcd-117">-Location</span></span>
<span data-ttu-id="4ebcd-118">Speicherort des Netzwerkwächters.</span><span class="sxs-lookup"><span data-stu-id="4ebcd-118">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ebcd-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4ebcd-119">-NetworkWatcher</span></span>
<span data-ttu-id="4ebcd-120">Die Netzwerkwächterressource.</span><span class="sxs-lookup"><span data-stu-id="4ebcd-120">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ebcd-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4ebcd-121">-NetworkWatcherName</span></span>
<span data-ttu-id="4ebcd-122">Der Name des Netzwerkwächters.</span><span class="sxs-lookup"><span data-stu-id="4ebcd-122">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ebcd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ebcd-123">-ResourceGroupName</span></span>
<span data-ttu-id="4ebcd-124">Der Name der Ressourcengruppe "Netzwerkwächter".</span><span class="sxs-lookup"><span data-stu-id="4ebcd-124">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ebcd-125">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ebcd-125">-TargetResourceGroupName</span></span>
<span data-ttu-id="4ebcd-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4ebcd-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ebcd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ebcd-127">CommonParameters</span></span>
<span data-ttu-id="4ebcd-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ebcd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ebcd-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ebcd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ebcd-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4ebcd-130">INPUTS</span></span>

### <span data-ttu-id="4ebcd-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4ebcd-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="4ebcd-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4ebcd-132">System.String</span></span>

## <span data-ttu-id="4ebcd-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4ebcd-133">OUTPUTS</span></span>

### <span data-ttu-id="4ebcd-134">Microsoft.Azure.Commands.Network.Models.PSTopology</span><span class="sxs-lookup"><span data-stu-id="4ebcd-134">Microsoft.Azure.Commands.Network.Models.PSTopology</span></span>

## <span data-ttu-id="4ebcd-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4ebcd-135">NOTES</span></span>
<span data-ttu-id="4ebcd-136">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, topology, view</span><span class="sxs-lookup"><span data-stu-id="4ebcd-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, topology, view</span></span> 

## <span data-ttu-id="4ebcd-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4ebcd-137">RELATED LINKS</span></span>

[<span data-ttu-id="4ebcd-138">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4ebcd-138">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4ebcd-139">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4ebcd-139">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4ebcd-140">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4ebcd-140">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4ebcd-141">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4ebcd-141">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4ebcd-142">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4ebcd-142">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4ebcd-143">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4ebcd-143">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4ebcd-144">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4ebcd-144">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4ebcd-145">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4ebcd-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4ebcd-146">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4ebcd-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4ebcd-147">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4ebcd-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4ebcd-148">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4ebcd-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4ebcd-149">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4ebcd-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4ebcd-150">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ebcd-150">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="4ebcd-151">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4ebcd-151">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4ebcd-152">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="4ebcd-152">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="4ebcd-153">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4ebcd-153">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4ebcd-154">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4ebcd-154">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4ebcd-155">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4ebcd-155">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4ebcd-156">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4ebcd-156">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4ebcd-157">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4ebcd-157">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4ebcd-158">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4ebcd-158">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4ebcd-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4ebcd-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4ebcd-160">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="4ebcd-160">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="4ebcd-161">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4ebcd-161">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="4ebcd-162">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4ebcd-162">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4ebcd-163">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4ebcd-163">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="4ebcd-164">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4ebcd-164">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

