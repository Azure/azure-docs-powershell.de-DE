---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: dd135f20814f1d2bd5a5a785275659b19a4e628a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919827"
---
# <span data-ttu-id="efee7-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="efee7-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="efee7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efee7-102">SYNOPSIS</span></span>
<span data-ttu-id="efee7-103">Ruft den Status der Flussprotokollierung für eine Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="efee7-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="efee7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="efee7-104">SYNTAX</span></span>

### <span data-ttu-id="efee7-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="efee7-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efee7-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="efee7-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efee7-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="efee7-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -Location <String> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efee7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="efee7-108">DESCRIPTION</span></span>
<span data-ttu-id="efee7-109">Das Get-AzNetworkWatcherFlowLogStatus-Cmdlet Ruft den Status der Flussprotokollierung für eine Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="efee7-109">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="efee7-110">Der Status umfasst, ob die Flussprotokollierung für die bereitgestellte Ressource aktiviert ist, das konfigurierte Speicherkonto zum Senden von Protokollen und die Aufbewahrungsrichtlinie für die Protokolle.</span><span class="sxs-lookup"><span data-stu-id="efee7-110">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="efee7-111">Derzeit werden Netzwerksicherheitsgruppen für die Flussprotokollierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="efee7-111">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="efee7-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="efee7-112">EXAMPLES</span></span>

### <span data-ttu-id="efee7-113">Beispiel 1: Anzeigen des Status der Flussprotokollierung für ein angegebenes NSG</span><span class="sxs-lookup"><span data-stu-id="efee7-113">Example 1: Get the Flow Logging Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                     "Format"         : {
                       "Type ": "Json",
                       "Version": 1
                     }
                   }
```

<span data-ttu-id="efee7-114">In diesem Beispiel wird der Status der Flussprotokollierung für eine Netzwerksicherheitsgruppe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="efee7-114">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="efee7-115">Für das angegebene NSG ist die Flussprotokollierung aktiviert, das Standardformat und kein Aufbewahrungsrichtliniensatz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="efee7-115">The specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="efee7-116">Beispiel 2: Anzeigen des Status "Flussprotokollierung" und "Datenverkehrsanalyse" für ein angegebenes NSG</span><span class="sxs-lookup"><span data-stu-id="efee7-116">Example 2: Get the Flow Logging and Traffic Analytics Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
              "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="efee7-117">In diesem Beispiel wird der Status "Flussprotokollierung" und "Datenverkehrsanalyse" für eine Netzwerksicherheitsgruppe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="efee7-117">In this example we get the flow logging and Traffic Analytics status for a Network Security Group.</span></span> <span data-ttu-id="efee7-118">Das angegebene NSG verfügt über flussprotokollierung und Traffic Analytics aktiviert, Standardformat und keine Aufbewahrungsrichtlinie festgelegt.</span><span class="sxs-lookup"><span data-stu-id="efee7-118">The specified NSG has flow logging and Traffic Analytics enabled, default format and no retention policy set.</span></span>

## <span data-ttu-id="efee7-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="efee7-119">PARAMETERS</span></span>

### <span data-ttu-id="efee7-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efee7-120">-AsJob</span></span>
<span data-ttu-id="efee7-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="efee7-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="efee7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efee7-122">-DefaultProfile</span></span>
<span data-ttu-id="efee7-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="efee7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efee7-124">-Location</span><span class="sxs-lookup"><span data-stu-id="efee7-124">-Location</span></span>
<span data-ttu-id="efee7-125">Speicherort des Netzwerkwächters.</span><span class="sxs-lookup"><span data-stu-id="efee7-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="efee7-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="efee7-126">-NetworkWatcher</span></span>
<span data-ttu-id="efee7-127">Die Netzwerkwächterressource.</span><span class="sxs-lookup"><span data-stu-id="efee7-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="efee7-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="efee7-128">-NetworkWatcherName</span></span>
<span data-ttu-id="efee7-129">Der Name des Netzwerkwächters.</span><span class="sxs-lookup"><span data-stu-id="efee7-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="efee7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efee7-130">-ResourceGroupName</span></span>
<span data-ttu-id="efee7-131">Der Name der Ressourcengruppe "Netzwerkwächter".</span><span class="sxs-lookup"><span data-stu-id="efee7-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="efee7-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="efee7-132">-TargetResourceId</span></span>
<span data-ttu-id="efee7-133">Die Zielressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="efee7-133">The target resource ID.</span></span>

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

### <span data-ttu-id="efee7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efee7-134">CommonParameters</span></span>
<span data-ttu-id="efee7-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efee7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efee7-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="efee7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efee7-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="efee7-137">INPUTS</span></span>

### <span data-ttu-id="efee7-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="efee7-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="efee7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="efee7-139">System.String</span></span>

## <span data-ttu-id="efee7-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="efee7-140">OUTPUTS</span></span>

### <span data-ttu-id="efee7-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="efee7-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="efee7-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="efee7-142">NOTES</span></span>
<span data-ttu-id="efee7-143">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span><span class="sxs-lookup"><span data-stu-id="efee7-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="efee7-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="efee7-144">RELATED LINKS</span></span>

[<span data-ttu-id="efee7-145">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="efee7-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="efee7-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="efee7-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="efee7-147">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="efee7-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="efee7-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="efee7-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="efee7-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="efee7-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="efee7-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="efee7-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="efee7-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="efee7-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="efee7-152">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="efee7-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="efee7-153">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="efee7-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="efee7-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="efee7-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="efee7-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="efee7-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="efee7-156">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="efee7-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="efee7-157">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="efee7-157">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="efee7-158">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="efee7-158">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="efee7-159">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="efee7-159">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="efee7-160">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="efee7-160">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="efee7-161">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="efee7-161">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="efee7-162">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="efee7-162">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="efee7-163">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="efee7-163">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="efee7-164">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="efee7-164">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="efee7-165">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="efee7-165">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="efee7-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="efee7-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="efee7-167">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="efee7-167">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="efee7-168">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="efee7-168">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="efee7-169">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="efee7-169">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="efee7-170">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="efee7-170">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="efee7-171">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="efee7-171">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
