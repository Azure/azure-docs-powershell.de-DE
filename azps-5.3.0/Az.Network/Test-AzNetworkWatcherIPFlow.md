---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 75b8d976dc4c7be0544f2445ef991723c692edbf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459855"
---
# <span data-ttu-id="a0c2c-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a0c2c-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="a0c2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0c2c-102">SYNOPSIS</span></span>
<span data-ttu-id="a0c2c-103">Gibt zurück, ob das Paket an einem bestimmten Ziel zulässig oder verweigert wurde.</span><span class="sxs-lookup"><span data-stu-id="a0c2c-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="a0c2c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0c2c-104">SYNTAX</span></span>

### <span data-ttu-id="a0c2c-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0c2c-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0c2c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a0c2c-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0c2c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a0c2c-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0c2c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0c2c-108">DESCRIPTION</span></span>
<span data-ttu-id="a0c2c-109">Das Test-AzNetworkWatcherIPFlow cmdlet für eine angegebene VM-Ressource und ein Paket mit einer angegebenen Richtung unter Verwendung von lokalen und Remote-, IP-Adressen und Ports gibt zurück, ob das Paket zulässig oder verweigert wurde.</span><span class="sxs-lookup"><span data-stu-id="a0c2c-109">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="a0c2c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a0c2c-110">EXAMPLES</span></span>

### <span data-ttu-id="a0c2c-111">Beispiel 1: Ausführen Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a0c2c-111">Example 1: Run Test-AzNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where-Object { $vm.NetworkProfile.NetworkInterfaces.Id -contains $_.Id }

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="a0c2c-112">Ruft die Network Watcher in west central US für dieses Abonnement ab, ruft dann die VM und die zugehörigen Netzwerkschnittstellen ab.</span><span class="sxs-lookup"><span data-stu-id="a0c2c-112">Gets the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="a0c2c-113">Führt dann für die erste Netzwerkschnittstelle Test-AzNetworkWatcherIPFlow die erste IP der ersten Netzwerkschnittstelle für eine ausgehende Verbindung zu einer IP im Internet aus.</span><span class="sxs-lookup"><span data-stu-id="a0c2c-113">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="a0c2c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0c2c-114">PARAMETERS</span></span>

### <span data-ttu-id="a0c2c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0c2c-115">-AsJob</span></span>
<span data-ttu-id="a0c2c-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a0c2c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0c2c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0c2c-117">-DefaultProfile</span></span>
<span data-ttu-id="a0c2c-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0c2c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0c2c-119">-Direction</span><span class="sxs-lookup"><span data-stu-id="a0c2c-119">-Direction</span></span>
<span data-ttu-id="a0c2c-120">Richtung.</span><span class="sxs-lookup"><span data-stu-id="a0c2c-120">Direction.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0c2c-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="a0c2c-121">-LocalIPAddress</span></span>
<span data-ttu-id="a0c2c-122">Lokale IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="a0c2c-122">Local IP Address.</span></span>

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

### <span data-ttu-id="a0c2c-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="a0c2c-123">-LocalPort</span></span>
<span data-ttu-id="a0c2c-124">Lokaler Port.</span><span class="sxs-lookup"><span data-stu-id="a0c2c-124">Local Port.</span></span>

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

### <span data-ttu-id="a0c2c-125">-Location</span><span class="sxs-lookup"><span data-stu-id="a0c2c-125">-Location</span></span>
<span data-ttu-id="a0c2c-126">Position der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="a0c2c-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a0c2c-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0c2c-127">-NetworkWatcher</span></span>
<span data-ttu-id="a0c2c-128">Die Netzwerk-Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="a0c2c-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="a0c2c-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a0c2c-129">-NetworkWatcherName</span></span>
<span data-ttu-id="a0c2c-130">Der Name der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="a0c2c-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="a0c2c-131">-Protocol</span><span class="sxs-lookup"><span data-stu-id="a0c2c-131">-Protocol</span></span>
<span data-ttu-id="a0c2c-132">Protokoll.</span><span class="sxs-lookup"><span data-stu-id="a0c2c-132">Protocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0c2c-133">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="a0c2c-133">-RemoteIPAddress</span></span>
<span data-ttu-id="a0c2c-134">Remote-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="a0c2c-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="a0c2c-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="a0c2c-135">-RemotePort</span></span>
<span data-ttu-id="a0c2c-136">Remoteport.</span><span class="sxs-lookup"><span data-stu-id="a0c2c-136">Remote port.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0c2c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0c2c-137">-ResourceGroupName</span></span>
<span data-ttu-id="a0c2c-138">Der Name der Ressourcengruppe "Netzwerk-Watcher".</span><span class="sxs-lookup"><span data-stu-id="a0c2c-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a0c2c-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="a0c2c-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="a0c2c-140">Ziel-Netzwerkschnittstellen-ID.</span><span class="sxs-lookup"><span data-stu-id="a0c2c-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="a0c2c-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="a0c2c-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="a0c2c-142">Die Ziel-ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="a0c2c-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="a0c2c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0c2c-143">CommonParameters</span></span>
<span data-ttu-id="a0c2c-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0c2c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0c2c-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0c2c-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0c2c-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a0c2c-146">INPUTS</span></span>

### <span data-ttu-id="a0c2c-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0c2c-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="a0c2c-148">System.String</span><span class="sxs-lookup"><span data-stu-id="a0c2c-148">System.String</span></span>

## <span data-ttu-id="a0c2c-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a0c2c-149">OUTPUTS</span></span>

### <span data-ttu-id="a0c2c-150">Microsoft.Azure.Commands.Network.Models.FLOWVerifyResult</span><span class="sxs-lookup"><span data-stu-id="a0c2c-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="a0c2c-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a0c2c-151">NOTES</span></span>
<span data-ttu-id="a0c2c-152">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span><span class="sxs-lookup"><span data-stu-id="a0c2c-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="a0c2c-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a0c2c-153">RELATED LINKS</span></span>

[<span data-ttu-id="a0c2c-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0c2c-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a0c2c-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0c2c-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a0c2c-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0c2c-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a0c2c-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a0c2c-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a0c2c-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a0c2c-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a0c2c-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a0c2c-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a0c2c-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a0c2c-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a0c2c-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0c2c-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0c2c-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a0c2c-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a0c2c-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0c2c-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0c2c-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0c2c-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0c2c-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0c2c-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0c2c-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0c2c-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a0c2c-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a0c2c-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a0c2c-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a0c2c-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a0c2c-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0c2c-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a0c2c-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0c2c-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a0c2c-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0c2c-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a0c2c-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a0c2c-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a0c2c-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0c2c-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a0c2c-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0c2c-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a0c2c-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a0c2c-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a0c2c-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a0c2c-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a0c2c-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a0c2c-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a0c2c-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a0c2c-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a0c2c-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a0c2c-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="a0c2c-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0c2c-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
