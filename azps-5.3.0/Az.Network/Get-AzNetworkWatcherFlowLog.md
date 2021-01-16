---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 5f4322ba81cdae5bdb0b33c2658a6d7934ed638d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379866"
---
# <span data-ttu-id="d5d04-101">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="d5d04-101">Get-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="d5d04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5d04-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d04-103">Ruft eine Flussprotokollressource oder eine Liste der Flussprotokollressourcen im angegebenen Abonnement und in der angegebenen Region ab.</span><span class="sxs-lookup"><span data-stu-id="d5d04-103">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="d5d04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5d04-104">SYNTAX</span></span>

### <span data-ttu-id="d5d04-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d5d04-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5d04-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d5d04-106">SetByResource</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5d04-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d5d04-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLog -Location <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5d04-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d5d04-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherFlowLog -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5d04-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5d04-109">DESCRIPTION</span></span>
<span data-ttu-id="d5d04-110">Ruft eine Flussprotokollressource oder eine Liste der Flussprotokollressourcen im angegebenen Abonnement und in der angegebenen Region ab.</span><span class="sxs-lookup"><span data-stu-id="d5d04-110">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="d5d04-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d5d04-111">EXAMPLES</span></span>

### <span data-ttu-id="d5d04-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d5d04-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

<span data-ttu-id="d5d04-113">Name : pstest Id : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState : Succeeded Location : eastus TargetResourceId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled : True RetentionPolicy : { "Days": 5, "Enabled": true } Format : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 }</span><span class="sxs-lookup"><span data-stu-id="d5d04-113">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 }</span></span>

## <span data-ttu-id="d5d04-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5d04-114">PARAMETERS</span></span>

### <span data-ttu-id="d5d04-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d04-115">-DefaultProfile</span></span>
<span data-ttu-id="d5d04-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5d04-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d04-117">-Location</span><span class="sxs-lookup"><span data-stu-id="d5d04-117">-Location</span></span>
<span data-ttu-id="d5d04-118">Position der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="d5d04-118">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d04-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d5d04-119">-Name</span></span>
<span data-ttu-id="d5d04-120">Der Name des Flussprotokolls.</span><span class="sxs-lookup"><span data-stu-id="d5d04-120">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: FlowLogName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d04-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d5d04-121">-NetworkWatcher</span></span>
<span data-ttu-id="d5d04-122">Die Netzwerk-Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="d5d04-122">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5d04-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d5d04-123">-NetworkWatcherName</span></span>
<span data-ttu-id="d5d04-124">Der Name der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="d5d04-124">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d04-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5d04-125">-ResourceGroupName</span></span>
<span data-ttu-id="d5d04-126">Der Name der Ressourcengruppe "Netzwerk-Watcher".</span><span class="sxs-lookup"><span data-stu-id="d5d04-126">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d04-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5d04-127">-ResourceId</span></span>
<span data-ttu-id="d5d04-128">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="d5d04-128">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5d04-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d04-129">CommonParameters</span></span>
<span data-ttu-id="d5d04-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5d04-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d04-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5d04-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d04-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d5d04-132">INPUTS</span></span>

### <span data-ttu-id="d5d04-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d5d04-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d5d04-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d5d04-134">System.String</span></span>

## <span data-ttu-id="d5d04-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d5d04-135">OUTPUTS</span></span>

### <span data-ttu-id="d5d04-136">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="d5d04-136">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="d5d04-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d5d04-137">NOTES</span></span>

## <span data-ttu-id="d5d04-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d5d04-138">RELATED LINKS</span></span>

[<span data-ttu-id="d5d04-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d5d04-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d5d04-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d5d04-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d5d04-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d5d04-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d5d04-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d5d04-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d5d04-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d5d04-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d5d04-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d5d04-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d5d04-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d5d04-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d5d04-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d5d04-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d5d04-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d5d04-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d5d04-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d5d04-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d5d04-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d5d04-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d5d04-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d5d04-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d5d04-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5d04-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d5d04-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d5d04-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d5d04-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d5d04-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d5d04-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d5d04-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d5d04-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d5d04-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d5d04-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d5d04-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d5d04-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d5d04-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d5d04-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d5d04-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d5d04-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d5d04-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d5d04-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d5d04-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d5d04-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d5d04-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d5d04-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d5d04-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d5d04-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d5d04-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d5d04-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d5d04-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="d5d04-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d5d04-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="d5d04-166">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="d5d04-166">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="d5d04-167">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="d5d04-167">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="d5d04-168">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="d5d04-168">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
