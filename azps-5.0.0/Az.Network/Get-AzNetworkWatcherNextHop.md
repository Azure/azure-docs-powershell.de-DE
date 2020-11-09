---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: cf120e8e9ca9e0dad8f4d430c7f207d40fcfab3b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302080"
---
# <span data-ttu-id="94f75-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="94f75-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="94f75-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="94f75-102">SYNOPSIS</span></span>
<span data-ttu-id="94f75-103">Ruft den nächsten Hop von einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="94f75-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="94f75-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="94f75-104">SYNTAX</span></span>

### <span data-ttu-id="94f75-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="94f75-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94f75-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="94f75-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94f75-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="94f75-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String> -DestinationIPAddress <String>
 -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94f75-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94f75-108">DESCRIPTION</span></span>
<span data-ttu-id="94f75-109">Das Get-AzNetworkWatcherNextHop-Cmdlet ruft den nächsten Hop von einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="94f75-109">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="94f75-110">Im nächsten Hop können Sie den Typ der Azure-Ressource, die zugehörige IP-Adresse dieser Ressource und die Routingtabellen Regel anzeigen, die für die Route verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="94f75-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="94f75-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94f75-111">EXAMPLES</span></span>

### <span data-ttu-id="94f75-112">Beispiel 1: Abrufen des nächsten Hop bei der Kommunikation mit einer Internet-IP</span><span class="sxs-lookup"><span data-stu-id="94f75-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="94f75-113">Ruft den nächsten Hop für ausgehende Kommunikation von der primären Netzwerkschnittstelle auf dem angegebenen virtuellen Computer zu 204.79.197.200 (www.Bing.com) ab.</span><span class="sxs-lookup"><span data-stu-id="94f75-113">Gets the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Machine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="94f75-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="94f75-114">PARAMETERS</span></span>

### <span data-ttu-id="94f75-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94f75-115">-AsJob</span></span>
<span data-ttu-id="94f75-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="94f75-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94f75-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f75-117">-DefaultProfile</span></span>
<span data-ttu-id="94f75-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="94f75-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94f75-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="94f75-119">-DestinationIPAddress</span></span>
<span data-ttu-id="94f75-120">Ziel-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="94f75-120">Destination IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f75-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="94f75-121">-Location</span></span>
<span data-ttu-id="94f75-122">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="94f75-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="94f75-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="94f75-123">-NetworkWatcher</span></span>
<span data-ttu-id="94f75-124">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="94f75-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="94f75-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="94f75-125">-NetworkWatcherName</span></span>
<span data-ttu-id="94f75-126">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="94f75-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="94f75-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f75-127">-ResourceGroupName</span></span>
<span data-ttu-id="94f75-128">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="94f75-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="94f75-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="94f75-129">-SourceIPAddress</span></span>
<span data-ttu-id="94f75-130">Quell-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="94f75-130">Source IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f75-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="94f75-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="94f75-132">Zielnetzwerk-Schnittstellenkennung</span><span class="sxs-lookup"><span data-stu-id="94f75-132">Target network interface Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f75-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="94f75-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="94f75-134">Die ID des virtuellen Zielcomputers</span><span class="sxs-lookup"><span data-stu-id="94f75-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="94f75-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f75-135">CommonParameters</span></span>
<span data-ttu-id="94f75-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94f75-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f75-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94f75-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f75-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="94f75-138">INPUTS</span></span>

### <span data-ttu-id="94f75-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="94f75-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="94f75-140">System. String</span><span class="sxs-lookup"><span data-stu-id="94f75-140">System.String</span></span>

## <span data-ttu-id="94f75-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="94f75-141">OUTPUTS</span></span>

### <span data-ttu-id="94f75-142">Microsoft. Azure. Commands. Network. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="94f75-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="94f75-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="94f75-143">NOTES</span></span>
<span data-ttu-id="94f75-144">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk-Watcher, weiter, Hop</span><span class="sxs-lookup"><span data-stu-id="94f75-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="94f75-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="94f75-145">RELATED LINKS</span></span>

[<span data-ttu-id="94f75-146">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="94f75-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="94f75-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="94f75-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="94f75-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="94f75-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="94f75-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="94f75-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="94f75-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="94f75-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="94f75-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="94f75-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="94f75-152">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="94f75-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="94f75-153">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="94f75-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="94f75-154">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="94f75-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="94f75-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="94f75-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="94f75-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="94f75-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="94f75-157">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="94f75-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="94f75-158">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="94f75-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="94f75-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="94f75-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="94f75-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="94f75-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="94f75-161">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="94f75-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="94f75-162">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="94f75-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="94f75-163">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="94f75-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="94f75-164">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="94f75-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="94f75-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="94f75-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="94f75-166">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="94f75-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="94f75-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="94f75-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="94f75-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="94f75-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="94f75-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="94f75-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="94f75-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="94f75-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="94f75-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="94f75-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="94f75-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="94f75-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
