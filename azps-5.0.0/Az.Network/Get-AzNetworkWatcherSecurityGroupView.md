---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 37da72dd26df32dddee0ea28d2378418e9e4922e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180165"
---
# <span data-ttu-id="2a785-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2a785-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="2a785-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2a785-102">SYNOPSIS</span></span>
<span data-ttu-id="2a785-103">Zeigen Sie die konfigurierten und effektiven Netzwerk Sicherheitsgruppen Regeln an, die auf einem virtuellen Computer angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a785-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="2a785-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a785-104">SYNTAX</span></span>

### <span data-ttu-id="2a785-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="2a785-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a785-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2a785-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a785-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2a785-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a785-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2a785-108">DESCRIPTION</span></span>
<span data-ttu-id="2a785-109">Mit dem Get-AzNetworkWatcherSecurityGroupView können Sie die konfigurierten und effektiven Netzwerk Sicherheitsgruppen Regeln anzeigen, die auf einem virtuellen Computer angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a785-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="2a785-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2a785-110">EXAMPLES</span></span>

### <span data-ttu-id="2a785-111">Beispiel 1: Erstellen eines Anrufs einer Sicherheitsgruppe auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="2a785-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="2a785-112">Im obigen Beispiel erhalten wir zunächst den regionalen Netzwerkmonitor und dann einen virtuellen Computer in der Region.</span><span class="sxs-lookup"><span data-stu-id="2a785-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="2a785-113">Anschließend wird ein Aufruf der Sicherheitsgruppen Ansicht für den angegebenen virtuellen Computer durchführen.</span><span class="sxs-lookup"><span data-stu-id="2a785-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="2a785-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a785-114">PARAMETERS</span></span>

### <span data-ttu-id="2a785-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a785-115">-AsJob</span></span>
<span data-ttu-id="2a785-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2a785-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a785-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a785-117">-DefaultProfile</span></span>
<span data-ttu-id="2a785-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2a785-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a785-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="2a785-119">-Location</span></span>
<span data-ttu-id="2a785-120">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="2a785-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2a785-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2a785-121">-NetworkWatcher</span></span>
<span data-ttu-id="2a785-122">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="2a785-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="2a785-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2a785-123">-NetworkWatcherName</span></span>
<span data-ttu-id="2a785-124">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="2a785-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="2a785-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a785-125">-ResourceGroupName</span></span>
<span data-ttu-id="2a785-126">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="2a785-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2a785-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="2a785-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="2a785-128">Die Ziel-VM-ID</span><span class="sxs-lookup"><span data-stu-id="2a785-128">The target VM Id</span></span>

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

### <span data-ttu-id="2a785-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a785-129">CommonParameters</span></span>
<span data-ttu-id="2a785-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a785-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a785-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a785-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a785-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2a785-132">INPUTS</span></span>

### <span data-ttu-id="2a785-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2a785-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="2a785-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2a785-134">System.String</span></span>

## <span data-ttu-id="2a785-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2a785-135">OUTPUTS</span></span>

### <span data-ttu-id="2a785-136">Microsoft. Azure. Commands. Network. Models. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="2a785-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="2a785-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="2a785-137">NOTES</span></span>
<span data-ttu-id="2a785-138">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk-Watcher, Flow, IP</span><span class="sxs-lookup"><span data-stu-id="2a785-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="2a785-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2a785-139">RELATED LINKS</span></span>

[<span data-ttu-id="2a785-140">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2a785-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2a785-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2a785-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2a785-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2a785-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2a785-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2a785-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2a785-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2a785-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2a785-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2a785-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2a785-146">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2a785-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2a785-147">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2a785-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2a785-148">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2a785-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2a785-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2a785-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2a785-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2a785-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2a785-151">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2a785-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2a785-152">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a785-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2a785-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2a785-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2a785-154">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2a785-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2a785-155">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2a785-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2a785-156">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2a785-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2a785-157">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2a785-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2a785-158">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2a785-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2a785-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2a785-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2a785-160">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2a785-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2a785-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2a785-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2a785-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2a785-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2a785-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2a785-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2a785-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2a785-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2a785-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2a785-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="2a785-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2a785-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
