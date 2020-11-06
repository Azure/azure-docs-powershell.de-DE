---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
ms.openlocfilehash: 6fc406d0af3ed451fbbf2f14c9ca8943256df744
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505289"
---
# <span data-ttu-id="2f516-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2f516-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="2f516-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2f516-102">SYNOPSIS</span></span>
<span data-ttu-id="2f516-103">Gibt zurück, ob das Paket zu oder von einem bestimmten Ziel zugelassen oder abgelehnt wurde.</span><span class="sxs-lookup"><span data-stu-id="2f516-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f516-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f516-104">SYNTAX</span></span>

### <span data-ttu-id="2f516-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="2f516-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f516-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2f516-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f516-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2f516-107">SetByLocation</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f516-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f516-108">DESCRIPTION</span></span>
<span data-ttu-id="2f516-109">Das Test-AzureRmNetworkWatcherIPFlow-Cmdlet für eine angegebene VM-Ressource und ein Paket mit der angegebenen Richtung unter Verwendung von Local und Remote, IP-Adressen und Ports gibt zurück, ob das Paket zugelassen oder verweigert wurde.</span><span class="sxs-lookup"><span data-stu-id="2f516-109">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="2f516-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f516-110">EXAMPLES</span></span>

### <span data-ttu-id="2f516-111">Beispiel 1: Ausführen von Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2f516-111">Example 1: Run Test-AzureRmNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="2f516-112">Holen Sie sich den Netzwerk-Watcher in West Central US für dieses Abonnement, und rufen Sie dann die VM und die zugehörigen Netzwerkschnittstellen ab.</span><span class="sxs-lookup"><span data-stu-id="2f516-112">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="2f516-113">Dann wird für die erste Netzwerkschnittstelle Test-AzureRmNetworkWatcherIPFlow mit der ersten IP-Adresse von der ersten Netzwerkschnittstelle für eine ausgehende Verbindung mit einer IP im Internet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f516-113">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="2f516-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f516-114">PARAMETERS</span></span>

### <span data-ttu-id="2f516-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f516-115">-AsJob</span></span>
<span data-ttu-id="2f516-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2f516-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f516-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f516-117">-DefaultProfile</span></span>
<span data-ttu-id="2f516-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2f516-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f516-119">-Richtung</span><span class="sxs-lookup"><span data-stu-id="2f516-119">-Direction</span></span>
<span data-ttu-id="2f516-120">Richtung.</span><span class="sxs-lookup"><span data-stu-id="2f516-120">Direction.</span></span>

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

### <span data-ttu-id="2f516-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="2f516-121">-LocalIPAddress</span></span>
<span data-ttu-id="2f516-122">Lokale IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="2f516-122">Local IP Address.</span></span>

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

### <span data-ttu-id="2f516-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="2f516-123">-LocalPort</span></span>
<span data-ttu-id="2f516-124">Lokaler Port.</span><span class="sxs-lookup"><span data-stu-id="2f516-124">Local Port.</span></span>

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

### <span data-ttu-id="2f516-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="2f516-125">-Location</span></span>
<span data-ttu-id="2f516-126">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="2f516-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2f516-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f516-127">-NetworkWatcher</span></span>
<span data-ttu-id="2f516-128">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="2f516-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="2f516-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2f516-129">-NetworkWatcherName</span></span>
<span data-ttu-id="2f516-130">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="2f516-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="2f516-131">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="2f516-131">-Protocol</span></span>
<span data-ttu-id="2f516-132">Protokoll.</span><span class="sxs-lookup"><span data-stu-id="2f516-132">Protocol.</span></span>

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

### <span data-ttu-id="2f516-133">-Remote</span><span class="sxs-lookup"><span data-stu-id="2f516-133">-RemoteIPAddress</span></span>
<span data-ttu-id="2f516-134">Remote-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="2f516-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="2f516-135">-Remoteport</span><span class="sxs-lookup"><span data-stu-id="2f516-135">-RemotePort</span></span>
<span data-ttu-id="2f516-136">Remote-Port.</span><span class="sxs-lookup"><span data-stu-id="2f516-136">Remote port.</span></span>

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

### <span data-ttu-id="2f516-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f516-137">-ResourceGroupName</span></span>
<span data-ttu-id="2f516-138">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="2f516-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2f516-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="2f516-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="2f516-140">Zielnetzwerk-Schnittstellenkennung</span><span class="sxs-lookup"><span data-stu-id="2f516-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="2f516-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="2f516-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="2f516-142">Die ID des virtuellen Zielcomputers</span><span class="sxs-lookup"><span data-stu-id="2f516-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="2f516-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f516-143">CommonParameters</span></span>
<span data-ttu-id="2f516-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f516-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f516-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f516-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f516-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2f516-146">INPUTS</span></span>

### <span data-ttu-id="2f516-147">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f516-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="2f516-148">Parameter: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2f516-148">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="2f516-149">System. String</span><span class="sxs-lookup"><span data-stu-id="2f516-149">System.String</span></span>
<span data-ttu-id="2f516-150">Parameter: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2f516-150">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="2f516-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2f516-151">OUTPUTS</span></span>

### <span data-ttu-id="2f516-152">Microsoft. Azure. Commands. Network. Models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="2f516-152">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="2f516-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="2f516-153">NOTES</span></span>
<span data-ttu-id="2f516-154">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk-Watcher, Flow, IP</span><span class="sxs-lookup"><span data-stu-id="2f516-154">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="2f516-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2f516-155">RELATED LINKS</span></span>

[<span data-ttu-id="2f516-156">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f516-156">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2f516-157">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f516-157">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2f516-158">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f516-158">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2f516-159">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2f516-159">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="2f516-160">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2f516-160">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2f516-161">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2f516-161">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="2f516-162">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2f516-162">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2f516-163">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f516-163">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2f516-164">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2f516-164">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="2f516-165">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f516-165">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2f516-166">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f516-166">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2f516-167">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f516-167">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2f516-168">Neu – AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f516-168">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2f516-169">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2f516-169">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="2f516-170">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2f516-170">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="2f516-171">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f516-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f516-172">Anfang-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f516-172">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f516-173">Satz-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f516-173">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f516-174">Satz-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2f516-174">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2f516-175">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f516-175">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f516-176">Neu – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f516-176">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f516-177">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2f516-177">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2f516-178">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2f516-178">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2f516-179">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2f516-179">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2f516-180">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2f516-180">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2f516-181">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2f516-181">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="2f516-182">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f516-182">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
