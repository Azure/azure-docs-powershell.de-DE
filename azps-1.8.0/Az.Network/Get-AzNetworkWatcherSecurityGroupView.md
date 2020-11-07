---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: f40b7e28bce34ef9e4cc289bed7f8c4524ef49d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660723"
---
# <span data-ttu-id="45565-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="45565-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="45565-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="45565-102">SYNOPSIS</span></span>
<span data-ttu-id="45565-103">Zeigen Sie die konfigurierten und effektiven Netzwerk Sicherheitsgruppen Regeln an, die auf einem virtuellen Computer angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="45565-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="45565-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="45565-104">SYNTAX</span></span>

### <span data-ttu-id="45565-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="45565-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45565-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="45565-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45565-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="45565-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45565-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45565-108">DESCRIPTION</span></span>
<span data-ttu-id="45565-109">Mit dem Get-AzNetworkWatcherSecurityGroupView können Sie die konfigurierten und effektiven Netzwerk Sicherheitsgruppen Regeln anzeigen, die auf einem virtuellen Computer angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="45565-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="45565-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45565-110">EXAMPLES</span></span>

### <span data-ttu-id="45565-111">Beispiel 1: Erstellen eines Anrufs einer Sicherheitsgruppe auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="45565-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="45565-112">Im obigen Beispiel erhalten wir zunächst den regionalen Netzwerkmonitor und dann einen virtuellen Computer in der Region.</span><span class="sxs-lookup"><span data-stu-id="45565-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="45565-113">Anschließend wird ein Aufruf der Sicherheitsgruppen Ansicht für den angegebenen virtuellen Computer durchführen.</span><span class="sxs-lookup"><span data-stu-id="45565-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="45565-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="45565-114">PARAMETERS</span></span>

### <span data-ttu-id="45565-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45565-115">-AsJob</span></span>
<span data-ttu-id="45565-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="45565-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45565-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45565-117">-DefaultProfile</span></span>
<span data-ttu-id="45565-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="45565-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45565-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="45565-119">-Location</span></span>
<span data-ttu-id="45565-120">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="45565-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="45565-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="45565-121">-NetworkWatcher</span></span>
<span data-ttu-id="45565-122">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="45565-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="45565-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="45565-123">-NetworkWatcherName</span></span>
<span data-ttu-id="45565-124">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="45565-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="45565-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45565-125">-ResourceGroupName</span></span>
<span data-ttu-id="45565-126">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="45565-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="45565-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="45565-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="45565-128">Die Ziel-VM-ID</span><span class="sxs-lookup"><span data-stu-id="45565-128">The target VM Id</span></span>

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

### <span data-ttu-id="45565-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45565-129">CommonParameters</span></span>
<span data-ttu-id="45565-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45565-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45565-131">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45565-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45565-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="45565-132">INPUTS</span></span>

### <span data-ttu-id="45565-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="45565-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="45565-134">System. String</span><span class="sxs-lookup"><span data-stu-id="45565-134">System.String</span></span>

## <span data-ttu-id="45565-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="45565-135">OUTPUTS</span></span>

### <span data-ttu-id="45565-136">Microsoft. Azure. Commands. Network. Models. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="45565-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="45565-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="45565-137">NOTES</span></span>
<span data-ttu-id="45565-138">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk-Watcher, Flow, IP</span><span class="sxs-lookup"><span data-stu-id="45565-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="45565-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="45565-139">RELATED LINKS</span></span>

[<span data-ttu-id="45565-140">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="45565-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="45565-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="45565-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="45565-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="45565-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="45565-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="45565-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="45565-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="45565-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="45565-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="45565-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="45565-146">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="45565-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="45565-147">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="45565-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="45565-148">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="45565-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="45565-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="45565-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="45565-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="45565-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="45565-151">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="45565-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="45565-152">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="45565-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="45565-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="45565-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="45565-154">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="45565-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="45565-155">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="45565-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="45565-156">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="45565-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="45565-157">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="45565-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="45565-158">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="45565-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="45565-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="45565-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="45565-160">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="45565-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="45565-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="45565-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="45565-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="45565-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="45565-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="45565-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="45565-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="45565-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="45565-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="45565-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="45565-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="45565-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
