---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchertopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTopology.md
ms.openlocfilehash: 527102bc6ee80215885efc0be42bbf740d21aa06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495934"
---
# <span data-ttu-id="8f495-101">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8f495-101">Get-AzureRmNetworkWatcherTopology</span></span>

## <span data-ttu-id="8f495-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f495-102">SYNOPSIS</span></span>
<span data-ttu-id="8f495-103">Ruft eine Ansicht auf Netzwerkebene von Ressourcen und deren Beziehungen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="8f495-103">Gets a network level view of resources and their relationships in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f495-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f495-104">SYNTAX</span></span>

### <span data-ttu-id="8f495-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f495-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherTopology -NetworkWatcher <PSNetworkWatcher> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f495-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="8f495-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherTopology -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f495-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="8f495-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherTopology -Location <String> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f495-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f495-108">DESCRIPTION</span></span>
<span data-ttu-id="8f495-109">Das Get-AzureRmNetworkWatcherTopology-Cmdlet eine Ansicht auf Netzwerkebene von Ressourcen und deren Beziehungen in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8f495-109">The Get-AzureRmNetworkWatcherTopology cmdlet a network level view of resources and their relationships in a resource group.</span></span> <span data-ttu-id="8f495-110">Hinweis: Wenn sich Ressourcen aus mehreren Regionen in der Ressourcengruppe befinden, werden nur die Ressourcen in der gleichen Region wie der Netzwerkmonitor in die JSON-Ausgabe aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="8f495-110">Note: If resources from multiple regions reside in the resource group, only the resources in the same region as the Network Watcher will be included in the JSON output.</span></span>

## <span data-ttu-id="8f495-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f495-111">EXAMPLES</span></span>

### <span data-ttu-id="8f495-112">Beispiel 1: Abrufen einer Azure-Topologie</span><span class="sxs-lookup"><span data-stu-id="8f495-112">Example 1: Get an Azure Topology</span></span>
```
$networkWatcher = Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG 
Get-AzureRmNetworkWatcherTopology -NetworkWatcher $networkWatcher -ResourceGroupName testresourcegroup

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

<span data-ttu-id="8f495-113">In diesem Beispiel führen wir das Get-AzureRmNetworkWatcherTopology-Cmdlet für eine Ressourcengruppe aus, die eine VM, NIC, NSG und öffentliche IP-Adresse enthält.</span><span class="sxs-lookup"><span data-stu-id="8f495-113">In this example we run the Get-AzureRmNetworkWatcherTopology cmdlet on a resource group that contains a VM, Nic, NSG, and public IP.</span></span>

## <span data-ttu-id="8f495-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f495-114">PARAMETERS</span></span>

### <span data-ttu-id="8f495-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f495-115">-DefaultProfile</span></span>
<span data-ttu-id="8f495-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8f495-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f495-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="8f495-117">-Location</span></span>
<span data-ttu-id="8f495-118">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="8f495-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="8f495-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8f495-119">-NetworkWatcher</span></span>
<span data-ttu-id="8f495-120">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="8f495-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="8f495-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8f495-121">-NetworkWatcherName</span></span>
<span data-ttu-id="8f495-122">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="8f495-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="8f495-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f495-123">-ResourceGroupName</span></span>
<span data-ttu-id="8f495-124">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="8f495-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8f495-125">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f495-125">-TargetResourceGroupName</span></span>
<span data-ttu-id="8f495-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8f495-126">The resource group name.</span></span>

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

### <span data-ttu-id="8f495-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f495-127">CommonParameters</span></span>
<span data-ttu-id="8f495-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f495-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f495-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f495-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f495-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f495-130">INPUTS</span></span>

### <span data-ttu-id="8f495-131">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8f495-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="8f495-132">Parameter: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8f495-132">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="8f495-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8f495-133">System.String</span></span>
<span data-ttu-id="8f495-134">Parameter: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8f495-134">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="8f495-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f495-135">OUTPUTS</span></span>

### <span data-ttu-id="8f495-136">Microsoft. Azure. Commands. Network. Models. PSTopology</span><span class="sxs-lookup"><span data-stu-id="8f495-136">Microsoft.Azure.Commands.Network.Models.PSTopology</span></span>

## <span data-ttu-id="8f495-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f495-137">NOTES</span></span>
<span data-ttu-id="8f495-138">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerkmonitor, Topologie, Ansicht</span><span class="sxs-lookup"><span data-stu-id="8f495-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, topology, view</span></span> 

## <span data-ttu-id="8f495-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f495-139">RELATED LINKS</span></span>

[<span data-ttu-id="8f495-140">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8f495-140">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="8f495-141">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8f495-141">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="8f495-142">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8f495-142">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="8f495-143">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8f495-143">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="8f495-144">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8f495-144">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8f495-145">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8f495-145">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="8f495-146">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8f495-146">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8f495-147">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8f495-147">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8f495-148">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8f495-148">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="8f495-149">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8f495-149">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8f495-150">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8f495-150">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8f495-151">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8f495-151">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8f495-152">Neu – AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f495-152">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="8f495-153">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8f495-153">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="8f495-154">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="8f495-154">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="8f495-155">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8f495-155">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8f495-156">Anfang-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8f495-156">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8f495-157">Satz-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8f495-157">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8f495-158">Satz-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8f495-158">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="8f495-159">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8f495-159">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8f495-160">Neu – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8f495-160">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8f495-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8f495-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="8f495-162">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8f495-162">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="8f495-163">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="8f495-163">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="8f495-164">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8f495-164">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="8f495-165">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8f495-165">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="8f495-166">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8f495-166">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)

