---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 3d2fa4a0d5c98ae468466780cffc2ea6439343f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919800"
---
# <span data-ttu-id="86434-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="86434-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="86434-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86434-102">SYNOPSIS</span></span>
<span data-ttu-id="86434-103">Zeigen Sie die konfigurierten und effektiven Gruppenregeln für Netzwerksicherheit an, die auf einen virtuellen Computer angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="86434-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="86434-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86434-104">SYNTAX</span></span>

### <span data-ttu-id="86434-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="86434-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86434-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="86434-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86434-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="86434-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86434-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86434-108">DESCRIPTION</span></span>
<span data-ttu-id="86434-109">Mit Get-AzNetworkWatcherSecurityGroupView können Sie die konfigurierten und effektiven Gruppenregeln für Netzwerksicherheit anzeigen, die auf einen virtuellen Computer angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="86434-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="86434-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="86434-110">EXAMPLES</span></span>

### <span data-ttu-id="86434-111">Beispiel 1: Erstellen eines Aufrufs der Sicherheitsgruppenansicht auf einer VM</span><span class="sxs-lookup"><span data-stu-id="86434-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="86434-112">Im vorstehenden Beispiel erhalten wir zuerst die regionale Netzwerkwacht und dann eine VM in der Region.</span><span class="sxs-lookup"><span data-stu-id="86434-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="86434-113">Anschließend wird auf der angegebenen VM ein Aufruf der Sicherheitsgruppenansicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="86434-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="86434-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="86434-114">PARAMETERS</span></span>

### <span data-ttu-id="86434-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86434-115">-AsJob</span></span>
<span data-ttu-id="86434-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="86434-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86434-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86434-117">-DefaultProfile</span></span>
<span data-ttu-id="86434-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="86434-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86434-119">-Location</span><span class="sxs-lookup"><span data-stu-id="86434-119">-Location</span></span>
<span data-ttu-id="86434-120">Speicherort des Netzwerkwächters.</span><span class="sxs-lookup"><span data-stu-id="86434-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="86434-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86434-121">-NetworkWatcher</span></span>
<span data-ttu-id="86434-122">Die Netzwerkwächterressource.</span><span class="sxs-lookup"><span data-stu-id="86434-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="86434-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="86434-123">-NetworkWatcherName</span></span>
<span data-ttu-id="86434-124">Der Name des Netzwerkwächters.</span><span class="sxs-lookup"><span data-stu-id="86434-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="86434-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86434-125">-ResourceGroupName</span></span>
<span data-ttu-id="86434-126">Der Name der Ressourcengruppe "Netzwerkwächter".</span><span class="sxs-lookup"><span data-stu-id="86434-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="86434-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="86434-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="86434-128">Die Ziel-VM-ID</span><span class="sxs-lookup"><span data-stu-id="86434-128">The target VM Id</span></span>

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

### <span data-ttu-id="86434-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86434-129">CommonParameters</span></span>
<span data-ttu-id="86434-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86434-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86434-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86434-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86434-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="86434-132">INPUTS</span></span>

### <span data-ttu-id="86434-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86434-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="86434-134">System.String</span><span class="sxs-lookup"><span data-stu-id="86434-134">System.String</span></span>

## <span data-ttu-id="86434-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="86434-135">OUTPUTS</span></span>

### <span data-ttu-id="86434-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="86434-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="86434-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="86434-137">NOTES</span></span>
<span data-ttu-id="86434-138">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span><span class="sxs-lookup"><span data-stu-id="86434-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="86434-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="86434-139">RELATED LINKS</span></span>

[<span data-ttu-id="86434-140">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86434-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="86434-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86434-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="86434-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86434-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="86434-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="86434-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="86434-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="86434-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="86434-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="86434-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="86434-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="86434-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="86434-147">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86434-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86434-148">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="86434-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="86434-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86434-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86434-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86434-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86434-151">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86434-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86434-152">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="86434-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="86434-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="86434-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="86434-154">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="86434-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="86434-155">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86434-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86434-156">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86434-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86434-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86434-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86434-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="86434-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="86434-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86434-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86434-160">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86434-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86434-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="86434-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="86434-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="86434-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="86434-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="86434-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="86434-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="86434-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="86434-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="86434-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="86434-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86434-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
