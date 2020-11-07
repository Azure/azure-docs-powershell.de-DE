---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTopology.md
ms.openlocfilehash: 72f5c803c7fa4f4693da3660c41f73eadb464ab7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841556"
---
# <span data-ttu-id="72011-101">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="72011-101">Get-AzNetworkWatcherTopology</span></span>

## <span data-ttu-id="72011-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72011-102">SYNOPSIS</span></span>
<span data-ttu-id="72011-103">Ruft eine Ansicht auf Netzwerkebene von Ressourcen und deren Beziehungen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="72011-103">Gets a network level view of resources and their relationships in a resource group.</span></span>

## <span data-ttu-id="72011-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72011-104">SYNTAX</span></span>

### <span data-ttu-id="72011-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="72011-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTopology -NetworkWatcher <PSNetworkWatcher> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72011-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="72011-106">SetByName</span></span>
```
Get-AzNetworkWatcherTopology -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72011-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72011-107">DESCRIPTION</span></span>
<span data-ttu-id="72011-108">Das Get-AzNetworkWatcherTopology-Cmdlet eine Ansicht auf Netzwerkebene von Ressourcen und deren Beziehungen in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="72011-108">The Get-AzNetworkWatcherTopology cmdlet a network level view of resources and their relationships in a resource group.</span></span> <span data-ttu-id="72011-109">Hinweis: Wenn sich Ressourcen aus mehreren Regionen in der Ressourcengruppe befinden, werden nur die Ressourcen in der gleichen Region wie der Netzwerkmonitor in die JSON-Ausgabe aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="72011-109">Note: If resources from multiple regions reside in the resource group, only the resources in the same region as the Network Watcher will be included in the JSON output.</span></span>

## <span data-ttu-id="72011-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72011-110">EXAMPLES</span></span>

### <span data-ttu-id="72011-111">--------------------------Beispiel 1: Abrufen einer Azure-Topologie--------------------------</span><span class="sxs-lookup"><span data-stu-id="72011-111">--------------------------  Example 1: Get an Azure Topology  --------------------------</span></span>
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

<span data-ttu-id="72011-112">In diesem Beispiel führen wir das Get-AzNetworkWatcherTopology-Cmdlet für eine Ressourcengruppe aus, die eine VM, NIC, NSG und öffentliche IP-Adresse enthält.</span><span class="sxs-lookup"><span data-stu-id="72011-112">In this example we run the Get-AzNetworkWatcherTopology cmdlet on a resource group that contains a VM, Nic, NSG, and public IP.</span></span>

## <span data-ttu-id="72011-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="72011-113">PARAMETERS</span></span>

### <span data-ttu-id="72011-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72011-114">-DefaultProfile</span></span>
<span data-ttu-id="72011-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="72011-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72011-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="72011-116">-NetworkWatcher</span></span>
<span data-ttu-id="72011-117">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="72011-117">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72011-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="72011-118">-NetworkWatcherName</span></span>
<span data-ttu-id="72011-119">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="72011-119">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72011-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72011-120">-ResourceGroupName</span></span>
<span data-ttu-id="72011-121">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="72011-121">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72011-122">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72011-122">-TargetResourceGroupName</span></span>
<span data-ttu-id="72011-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="72011-123">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72011-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72011-124">CommonParameters</span></span>
<span data-ttu-id="72011-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72011-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72011-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72011-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72011-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72011-127">INPUTS</span></span>

### <span data-ttu-id="72011-128">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="72011-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="72011-129">System. String</span><span class="sxs-lookup"><span data-stu-id="72011-129">System.String</span></span>

## <span data-ttu-id="72011-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72011-130">OUTPUTS</span></span>

### <span data-ttu-id="72011-131">Microsoft. Azure. Commands. Network. Models. PSTopology</span><span class="sxs-lookup"><span data-stu-id="72011-131">Microsoft.Azure.Commands.Network.Models.PSTopology</span></span>

## <span data-ttu-id="72011-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="72011-132">NOTES</span></span>
<span data-ttu-id="72011-133">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerkmonitor, Topologie, Ansicht</span><span class="sxs-lookup"><span data-stu-id="72011-133">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, topology, view</span></span> 

## <span data-ttu-id="72011-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72011-134">RELATED LINKS</span></span>

[<span data-ttu-id="72011-135">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="72011-135">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="72011-136">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="72011-136">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="72011-137">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="72011-137">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="72011-138">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="72011-138">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="72011-139">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="72011-139">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="72011-140">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="72011-140">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="72011-141">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="72011-141">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="72011-142">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="72011-142">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="72011-143">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="72011-143">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="72011-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="72011-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="72011-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="72011-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="72011-146">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="72011-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

