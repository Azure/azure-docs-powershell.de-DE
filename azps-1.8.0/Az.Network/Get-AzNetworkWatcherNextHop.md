---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: 51fea717c352f00b4f356e6bb07b730cdeb60966
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660727"
---
# <span data-ttu-id="2cb8b-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2cb8b-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="2cb8b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2cb8b-102">SYNOPSIS</span></span>
<span data-ttu-id="2cb8b-103">Ruft den nächsten Hop von einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="2cb8b-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="2cb8b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cb8b-104">SYNTAX</span></span>

### <span data-ttu-id="2cb8b-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="2cb8b-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cb8b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2cb8b-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cb8b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2cb8b-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String> -DestinationIPAddress <String>
 -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cb8b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2cb8b-108">DESCRIPTION</span></span>
<span data-ttu-id="2cb8b-109">Das Get-AzNetworkWatcherNextHop-Cmdlet ruft den nächsten Hop von einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="2cb8b-109">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="2cb8b-110">Im nächsten Hop können Sie den Typ der Azure-Ressource, die zugehörige IP-Adresse dieser Ressource und die Routingtabellen Regel anzeigen, die für die Route verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="2cb8b-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="2cb8b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2cb8b-111">EXAMPLES</span></span>

### <span data-ttu-id="2cb8b-112">Beispiel 1: Abrufen des nächsten Hop bei der Kommunikation mit einer Internet-IP</span><span class="sxs-lookup"><span data-stu-id="2cb8b-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
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

<span data-ttu-id="2cb8b-113">Abrufen des nächsten Hop für ausgehende Kommunikation von der primären Netzwerkschnittstelle des angegebenen virtuellen Vachine zu 204.79.197.200 (www.Bing.com)</span><span class="sxs-lookup"><span data-stu-id="2cb8b-113">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="2cb8b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cb8b-114">PARAMETERS</span></span>

### <span data-ttu-id="2cb8b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cb8b-115">-AsJob</span></span>
<span data-ttu-id="2cb8b-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2cb8b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2cb8b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cb8b-117">-DefaultProfile</span></span>
<span data-ttu-id="2cb8b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2cb8b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cb8b-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="2cb8b-119">-DestinationIPAddress</span></span>
<span data-ttu-id="2cb8b-120">Ziel-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="2cb8b-120">Destination IP address.</span></span>

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

### <span data-ttu-id="2cb8b-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="2cb8b-121">-Location</span></span>
<span data-ttu-id="2cb8b-122">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="2cb8b-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2cb8b-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2cb8b-123">-NetworkWatcher</span></span>
<span data-ttu-id="2cb8b-124">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="2cb8b-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="2cb8b-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2cb8b-125">-NetworkWatcherName</span></span>
<span data-ttu-id="2cb8b-126">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="2cb8b-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="2cb8b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cb8b-127">-ResourceGroupName</span></span>
<span data-ttu-id="2cb8b-128">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="2cb8b-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2cb8b-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="2cb8b-129">-SourceIPAddress</span></span>
<span data-ttu-id="2cb8b-130">Quell-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="2cb8b-130">Source IP address.</span></span>

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

### <span data-ttu-id="2cb8b-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="2cb8b-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="2cb8b-132">Zielnetzwerk-Schnittstellenkennung</span><span class="sxs-lookup"><span data-stu-id="2cb8b-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="2cb8b-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="2cb8b-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="2cb8b-134">Die ID des virtuellen Zielcomputers</span><span class="sxs-lookup"><span data-stu-id="2cb8b-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="2cb8b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cb8b-135">CommonParameters</span></span>
<span data-ttu-id="2cb8b-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cb8b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cb8b-137">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cb8b-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cb8b-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2cb8b-138">INPUTS</span></span>

### <span data-ttu-id="2cb8b-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2cb8b-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="2cb8b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2cb8b-140">System.String</span></span>

## <span data-ttu-id="2cb8b-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2cb8b-141">OUTPUTS</span></span>

### <span data-ttu-id="2cb8b-142">Microsoft. Azure. Commands. Network. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="2cb8b-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="2cb8b-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="2cb8b-143">NOTES</span></span>
<span data-ttu-id="2cb8b-144">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk-Watcher, weiter, Hop</span><span class="sxs-lookup"><span data-stu-id="2cb8b-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="2cb8b-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2cb8b-145">RELATED LINKS</span></span>

[<span data-ttu-id="2cb8b-146">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2cb8b-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2cb8b-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2cb8b-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2cb8b-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2cb8b-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2cb8b-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2cb8b-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2cb8b-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2cb8b-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2cb8b-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2cb8b-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2cb8b-152">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2cb8b-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2cb8b-153">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2cb8b-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2cb8b-154">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2cb8b-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2cb8b-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2cb8b-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2cb8b-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2cb8b-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2cb8b-157">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2cb8b-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2cb8b-158">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2cb8b-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2cb8b-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2cb8b-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2cb8b-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2cb8b-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2cb8b-161">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2cb8b-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2cb8b-162">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2cb8b-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2cb8b-163">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2cb8b-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2cb8b-164">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2cb8b-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2cb8b-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2cb8b-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2cb8b-166">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2cb8b-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2cb8b-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2cb8b-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2cb8b-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2cb8b-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2cb8b-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2cb8b-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2cb8b-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2cb8b-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2cb8b-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2cb8b-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="2cb8b-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2cb8b-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
