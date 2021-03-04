---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: a948dc37f778ff7a44a9e1478cfe138f2fefb113
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919816"
---
# <span data-ttu-id="18e96-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="18e96-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="18e96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18e96-102">SYNOPSIS</span></span>
<span data-ttu-id="18e96-103">Ruft den nächsten Hop von einer VM ab.</span><span class="sxs-lookup"><span data-stu-id="18e96-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="18e96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18e96-104">SYNTAX</span></span>

### <span data-ttu-id="18e96-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="18e96-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18e96-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="18e96-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18e96-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="18e96-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String> -DestinationIPAddress <String>
 -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18e96-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18e96-108">DESCRIPTION</span></span>
<span data-ttu-id="18e96-109">Das Get-AzNetworkWatcherNextHop-Cmdlet ruft den nächsten Hop von einer VM ab.</span><span class="sxs-lookup"><span data-stu-id="18e96-109">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="18e96-110">Im nächsten Hop können Sie den Typ der Azure-Ressource, die zugehörige IP-Adresse dieser Ressource und die Routingtabellenregel anzeigen, die für die Route zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="18e96-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="18e96-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="18e96-111">EXAMPLES</span></span>

### <span data-ttu-id="18e96-112">Beispiel 1: Erhalten des nächsten Hops bei der Kommunikation mit einer Internet-IP</span><span class="sxs-lookup"><span data-stu-id="18e96-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
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

<span data-ttu-id="18e96-113">Ruft den nächsten Hop für ausgehende Kommunikation von der primären Netzwerkschnittstelle auf dem angegebenen virtuellen Computer auf 204.79.197.200 (www.bing.com) ab.</span><span class="sxs-lookup"><span data-stu-id="18e96-113">Gets the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Machine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="18e96-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="18e96-114">PARAMETERS</span></span>

### <span data-ttu-id="18e96-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18e96-115">-AsJob</span></span>
<span data-ttu-id="18e96-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="18e96-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18e96-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18e96-117">-DefaultProfile</span></span>
<span data-ttu-id="18e96-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18e96-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18e96-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="18e96-119">-DestinationIPAddress</span></span>
<span data-ttu-id="18e96-120">Ziel-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="18e96-120">Destination IP address.</span></span>

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

### <span data-ttu-id="18e96-121">-Location</span><span class="sxs-lookup"><span data-stu-id="18e96-121">-Location</span></span>
<span data-ttu-id="18e96-122">Speicherort des Netzwerkwächters.</span><span class="sxs-lookup"><span data-stu-id="18e96-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="18e96-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="18e96-123">-NetworkWatcher</span></span>
<span data-ttu-id="18e96-124">Die Netzwerkwächterressource.</span><span class="sxs-lookup"><span data-stu-id="18e96-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="18e96-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="18e96-125">-NetworkWatcherName</span></span>
<span data-ttu-id="18e96-126">Der Name des Netzwerkwächters.</span><span class="sxs-lookup"><span data-stu-id="18e96-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="18e96-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18e96-127">-ResourceGroupName</span></span>
<span data-ttu-id="18e96-128">Der Name der Ressourcengruppe "Netzwerkwächter".</span><span class="sxs-lookup"><span data-stu-id="18e96-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="18e96-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="18e96-129">-SourceIPAddress</span></span>
<span data-ttu-id="18e96-130">Quell-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="18e96-130">Source IP address.</span></span>

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

### <span data-ttu-id="18e96-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="18e96-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="18e96-132">Zielnetzwerkschnittstellen-ID.</span><span class="sxs-lookup"><span data-stu-id="18e96-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="18e96-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="18e96-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="18e96-134">Die Virtuelle Computer-ID des Zielcomputers.</span><span class="sxs-lookup"><span data-stu-id="18e96-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="18e96-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18e96-135">CommonParameters</span></span>
<span data-ttu-id="18e96-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18e96-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18e96-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18e96-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18e96-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="18e96-138">INPUTS</span></span>

### <span data-ttu-id="18e96-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="18e96-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="18e96-140">System.String</span><span class="sxs-lookup"><span data-stu-id="18e96-140">System.String</span></span>

## <span data-ttu-id="18e96-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="18e96-141">OUTPUTS</span></span>

### <span data-ttu-id="18e96-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="18e96-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="18e96-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="18e96-143">NOTES</span></span>
<span data-ttu-id="18e96-144">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span><span class="sxs-lookup"><span data-stu-id="18e96-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="18e96-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="18e96-145">RELATED LINKS</span></span>

[<span data-ttu-id="18e96-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="18e96-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="18e96-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="18e96-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="18e96-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="18e96-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="18e96-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="18e96-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="18e96-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="18e96-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="18e96-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="18e96-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="18e96-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="18e96-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="18e96-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="18e96-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="18e96-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="18e96-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="18e96-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="18e96-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="18e96-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="18e96-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="18e96-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="18e96-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="18e96-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="18e96-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="18e96-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="18e96-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="18e96-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="18e96-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="18e96-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="18e96-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="18e96-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="18e96-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="18e96-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="18e96-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="18e96-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="18e96-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="18e96-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="18e96-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="18e96-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="18e96-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="18e96-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="18e96-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="18e96-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="18e96-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="18e96-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="18e96-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="18e96-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="18e96-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="18e96-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="18e96-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="18e96-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="18e96-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
