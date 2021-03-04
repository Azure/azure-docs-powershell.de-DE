---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: c6138ebe91f682eec8ce3c837829d60dc25f7911
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919819"
---
# <span data-ttu-id="742ba-101">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="742ba-101">Get-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="742ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="742ba-102">SYNOPSIS</span></span>
<span data-ttu-id="742ba-103">Ruft eine Flussprotokollressource oder eine Liste der Flussprotokollressourcen im angegebenen Abonnement und der angegebenen Region ab.</span><span class="sxs-lookup"><span data-stu-id="742ba-103">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="742ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="742ba-104">SYNTAX</span></span>

### <span data-ttu-id="742ba-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="742ba-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="742ba-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="742ba-106">SetByResource</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="742ba-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="742ba-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLog -Location <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="742ba-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="742ba-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherFlowLog -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="742ba-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="742ba-109">DESCRIPTION</span></span>
<span data-ttu-id="742ba-110">Ruft eine Flussprotokollressource oder eine Liste der Flussprotokollressourcen im angegebenen Abonnement und der angegebenen Region ab.</span><span class="sxs-lookup"><span data-stu-id="742ba-110">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="742ba-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="742ba-111">EXAMPLES</span></span>

### <span data-ttu-id="742ba-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="742ba-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

<span data-ttu-id="742ba-113">Name : pstest Id : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState : Succeeded Location : eastus TargetResourceId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled : True RetentionPolicy : { "Days": 5, "Enabled": true } Format : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 }</span><span class="sxs-lookup"><span data-stu-id="742ba-113">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 }</span></span>

## <span data-ttu-id="742ba-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="742ba-114">PARAMETERS</span></span>

### <span data-ttu-id="742ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="742ba-115">-DefaultProfile</span></span>
<span data-ttu-id="742ba-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="742ba-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="742ba-117">-Location</span><span class="sxs-lookup"><span data-stu-id="742ba-117">-Location</span></span>
<span data-ttu-id="742ba-118">Speicherort des Netzwerkwächters.</span><span class="sxs-lookup"><span data-stu-id="742ba-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="742ba-119">-Name</span><span class="sxs-lookup"><span data-stu-id="742ba-119">-Name</span></span>
<span data-ttu-id="742ba-120">Der Name des Flussprotokolls.</span><span class="sxs-lookup"><span data-stu-id="742ba-120">The flow log name.</span></span>

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

### <span data-ttu-id="742ba-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="742ba-121">-NetworkWatcher</span></span>
<span data-ttu-id="742ba-122">Die Netzwerkwächterressource.</span><span class="sxs-lookup"><span data-stu-id="742ba-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="742ba-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="742ba-123">-NetworkWatcherName</span></span>
<span data-ttu-id="742ba-124">Der Name des Netzwerkwächters.</span><span class="sxs-lookup"><span data-stu-id="742ba-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="742ba-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="742ba-125">-ResourceGroupName</span></span>
<span data-ttu-id="742ba-126">Der Name der Ressourcengruppe "Netzwerkwächter".</span><span class="sxs-lookup"><span data-stu-id="742ba-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="742ba-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="742ba-127">-ResourceId</span></span>
<span data-ttu-id="742ba-128">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="742ba-128">Resource ID.</span></span>

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

### <span data-ttu-id="742ba-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="742ba-129">CommonParameters</span></span>
<span data-ttu-id="742ba-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="742ba-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="742ba-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="742ba-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="742ba-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="742ba-132">INPUTS</span></span>

### <span data-ttu-id="742ba-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="742ba-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="742ba-134">System.String</span><span class="sxs-lookup"><span data-stu-id="742ba-134">System.String</span></span>

## <span data-ttu-id="742ba-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="742ba-135">OUTPUTS</span></span>

### <span data-ttu-id="742ba-136">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="742ba-136">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="742ba-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="742ba-137">NOTES</span></span>

## <span data-ttu-id="742ba-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="742ba-138">RELATED LINKS</span></span>

[<span data-ttu-id="742ba-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="742ba-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="742ba-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="742ba-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="742ba-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="742ba-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="742ba-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="742ba-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="742ba-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="742ba-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="742ba-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="742ba-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="742ba-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="742ba-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="742ba-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="742ba-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="742ba-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="742ba-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="742ba-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="742ba-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="742ba-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="742ba-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="742ba-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="742ba-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="742ba-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="742ba-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="742ba-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="742ba-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="742ba-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="742ba-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="742ba-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="742ba-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="742ba-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="742ba-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="742ba-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="742ba-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="742ba-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="742ba-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="742ba-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="742ba-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="742ba-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="742ba-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="742ba-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="742ba-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="742ba-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="742ba-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="742ba-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="742ba-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="742ba-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="742ba-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="742ba-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="742ba-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="742ba-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="742ba-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="742ba-166">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="742ba-166">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="742ba-167">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="742ba-167">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="742ba-168">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="742ba-168">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
