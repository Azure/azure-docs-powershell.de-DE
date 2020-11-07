---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchertopology
schema: 2.0.0
ms.openlocfilehash: 54186adcc1b8605ee9b468b59aeef9c25b2f3f46
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850692"
---
# <span data-ttu-id="307e8-101">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="307e8-101">Get-AzureRmNetworkWatcherTopology</span></span>

## <span data-ttu-id="307e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="307e8-102">SYNOPSIS</span></span>
<span data-ttu-id="307e8-103">Ruft eine Ansicht auf Netzwerkebene von Ressourcen und deren Beziehungen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="307e8-103">Gets a network level view of resources and their relationships in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="307e8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="307e8-104">SYNTAX</span></span>

### <span data-ttu-id="307e8-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="307e8-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherTopology -NetworkWatcher <PSNetworkWatcher> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="307e8-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="307e8-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherTopology -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="307e8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="307e8-107">DESCRIPTION</span></span>
<span data-ttu-id="307e8-108">Das Get-AzureRmNetworkWatcherTopology-Cmdlet eine Ansicht auf Netzwerkebene von Ressourcen und deren Beziehungen in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="307e8-108">The Get-AzureRmNetworkWatcherTopology cmdlet a network level view of resources and their relationships in a resource group.</span></span> <span data-ttu-id="307e8-109">Hinweis: Wenn sich Ressourcen aus mehreren Regionen in der Ressourcengruppe befinden, werden nur die Ressourcen in der gleichen Region wie der Netzwerkmonitor in die JSON-Ausgabe aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="307e8-109">Note: If resources from multiple regions reside in the resource group, only the resources in the same region as the Network Watcher will be included in the JSON output.</span></span>

## <span data-ttu-id="307e8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="307e8-110">EXAMPLES</span></span>

### <span data-ttu-id="307e8-111">--------------------------Beispiel 1: Abrufen einer Azure-Topologie--------------------------</span><span class="sxs-lookup"><span data-stu-id="307e8-111">--------------------------  Example 1: Get an Azure Topology  --------------------------</span></span>
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

<span data-ttu-id="307e8-112">In diesem Beispiel führen wir das Get-AzureRmNetworkWatcherTopology-Cmdlet für eine Ressourcengruppe aus, die eine VM, NIC, NSG und öffentliche IP-Adresse enthält.</span><span class="sxs-lookup"><span data-stu-id="307e8-112">In this example we run the Get-AzureRmNetworkWatcherTopology cmdlet on a resource group that contains a VM, Nic, NSG, and public IP.</span></span>

## <span data-ttu-id="307e8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="307e8-113">PARAMETERS</span></span>

### <span data-ttu-id="307e8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="307e8-114">-DefaultProfile</span></span>
<span data-ttu-id="307e8-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="307e8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="307e8-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="307e8-116">-NetworkWatcher</span></span>
<span data-ttu-id="307e8-117">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="307e8-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="307e8-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="307e8-118">-NetworkWatcherName</span></span>
<span data-ttu-id="307e8-119">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="307e8-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="307e8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="307e8-120">-ResourceGroupName</span></span>
<span data-ttu-id="307e8-121">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="307e8-121">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="307e8-122">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="307e8-122">-TargetResourceGroupName</span></span>
<span data-ttu-id="307e8-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="307e8-123">The resource group name.</span></span>

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

### <span data-ttu-id="307e8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="307e8-124">CommonParameters</span></span>
<span data-ttu-id="307e8-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="307e8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="307e8-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="307e8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="307e8-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="307e8-127">INPUTS</span></span>

### <span data-ttu-id="307e8-128">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="307e8-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="307e8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="307e8-129">System.String</span></span>

## <span data-ttu-id="307e8-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="307e8-130">OUTPUTS</span></span>

### <span data-ttu-id="307e8-131">Microsoft. Azure. Commands. Network. Models. PSTopology</span><span class="sxs-lookup"><span data-stu-id="307e8-131">Microsoft.Azure.Commands.Network.Models.PSTopology</span></span>

## <span data-ttu-id="307e8-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="307e8-132">NOTES</span></span>
<span data-ttu-id="307e8-133">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerkmonitor, Topologie, Ansicht</span><span class="sxs-lookup"><span data-stu-id="307e8-133">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, topology, view</span></span> 

## <span data-ttu-id="307e8-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="307e8-134">RELATED LINKS</span></span>

[<span data-ttu-id="307e8-135">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="307e8-135">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="307e8-136">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="307e8-136">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="307e8-137">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="307e8-137">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="307e8-138">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="307e8-138">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="307e8-139">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="307e8-139">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="307e8-140">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="307e8-140">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="307e8-141">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="307e8-141">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="307e8-142">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="307e8-142">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="307e8-143">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="307e8-143">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="307e8-144">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="307e8-144">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="307e8-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="307e8-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="307e8-146">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="307e8-146">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

