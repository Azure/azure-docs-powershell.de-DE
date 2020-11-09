---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: dc8d3a3db0eaa76974e02a62111b022ed81524b0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303723"
---
# <span data-ttu-id="37eb4-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="37eb4-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="37eb4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="37eb4-103">Ruft die Eigenschaften eines Netzwerkmonitors ab.</span><span class="sxs-lookup"><span data-stu-id="37eb4-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="37eb4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37eb4-104">SYNTAX</span></span>

### <span data-ttu-id="37eb4-105">Liste</span><span class="sxs-lookup"><span data-stu-id="37eb4-105">List</span></span>
```
Get-AzNetworkWatcher [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37eb4-106">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="37eb4-106">SetByLocation</span></span>
```
Get-AzNetworkWatcher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37eb4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37eb4-107">DESCRIPTION</span></span>
<span data-ttu-id="37eb4-108">Das Get-AzNetworkWatcher-Cmdlet ruft mindestens eine Azure Network Watcher-Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="37eb4-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="37eb4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37eb4-109">EXAMPLES</span></span>

### <span data-ttu-id="37eb4-110">Beispiel 1: Abrufen eines Netzwerkmonitors</span><span class="sxs-lookup"><span data-stu-id="37eb4-110">Example 1: Get a Network Watcher</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="37eb4-111">Ruft den Netzwerkmonitor mit dem Namen NetworkWatcher_westcentralus in der Ressourcengruppe NetworkWatcherRG ab.</span><span class="sxs-lookup"><span data-stu-id="37eb4-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

### <span data-ttu-id="37eb4-112">Beispiel 2: Auflisten von Netzwerk überwachungsern mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="37eb4-112">Example 2: List Network Watchers using filtering</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher*

Name              : NetworkWatcher_westcentralus1
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus1
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded

Name              : NetworkWatcher_westcentralus2
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus2
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="37eb4-113">Ruft die Netzwerk Beobachter ab, die mit "NetworkWatcher" beginnen.</span><span class="sxs-lookup"><span data-stu-id="37eb4-113">Gets the Network Watchers that start with "NetworkWatcher"</span></span>

## <span data-ttu-id="37eb4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="37eb4-114">PARAMETERS</span></span>

### <span data-ttu-id="37eb4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37eb4-115">-DefaultProfile</span></span>
<span data-ttu-id="37eb4-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="37eb4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37eb4-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="37eb4-117">-Location</span></span>
<span data-ttu-id="37eb4-118">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="37eb4-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="37eb4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="37eb4-119">-Name</span></span>
<span data-ttu-id="37eb4-120">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="37eb4-120">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="37eb4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37eb4-121">-ResourceGroupName</span></span>
<span data-ttu-id="37eb4-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="37eb4-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="37eb4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37eb4-123">CommonParameters</span></span>
<span data-ttu-id="37eb4-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37eb4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37eb4-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37eb4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37eb4-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37eb4-126">INPUTS</span></span>

### <span data-ttu-id="37eb4-127">Keine</span><span class="sxs-lookup"><span data-stu-id="37eb4-127">None</span></span>

## <span data-ttu-id="37eb4-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37eb4-128">OUTPUTS</span></span>

### <span data-ttu-id="37eb4-129">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="37eb4-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="37eb4-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="37eb4-130">NOTES</span></span>
<span data-ttu-id="37eb4-131">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke, Netzwerkmonitor</span><span class="sxs-lookup"><span data-stu-id="37eb4-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="37eb4-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37eb4-132">RELATED LINKS</span></span>

[<span data-ttu-id="37eb4-133">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="37eb4-133">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="37eb4-134">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="37eb4-134">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="37eb4-135">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="37eb4-135">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="37eb4-136">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="37eb4-136">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="37eb4-137">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="37eb4-137">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="37eb4-138">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="37eb4-138">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="37eb4-139">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="37eb4-139">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="37eb4-140">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="37eb4-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="37eb4-141">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="37eb4-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="37eb4-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="37eb4-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="37eb4-143">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="37eb4-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="37eb4-144">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="37eb4-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="37eb4-145">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="37eb4-145">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="37eb4-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="37eb4-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="37eb4-147">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="37eb4-147">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="37eb4-148">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="37eb4-148">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="37eb4-149">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="37eb4-149">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="37eb4-150">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="37eb4-150">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="37eb4-151">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="37eb4-151">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="37eb4-152">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="37eb4-152">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="37eb4-153">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="37eb4-153">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="37eb4-154">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="37eb4-154">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="37eb4-155">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="37eb4-155">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="37eb4-156">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="37eb4-156">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="37eb4-157">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="37eb4-157">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="37eb4-158">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="37eb4-158">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="37eb4-159">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="37eb4-159">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
