---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 5f4322ba81cdae5bdb0b33c2658a6d7934ed638d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165782"
---
# <span data-ttu-id="a6974-101">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="a6974-101">Get-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="a6974-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a6974-102">SYNOPSIS</span></span>
<span data-ttu-id="a6974-103">Ruft eine Flow Log-Ressource oder eine Liste der Flow Log-Ressourcen im angegebenen Abonnement und der angegebenen Region ab.</span><span class="sxs-lookup"><span data-stu-id="a6974-103">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="a6974-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6974-104">SYNTAX</span></span>

### <span data-ttu-id="a6974-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a6974-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6974-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a6974-106">SetByResource</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6974-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a6974-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLog -Location <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6974-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a6974-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherFlowLog -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6974-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6974-109">DESCRIPTION</span></span>
<span data-ttu-id="a6974-110">Ruft eine Flow Log-Ressource oder eine Liste der Flow Log-Ressourcen im angegebenen Abonnement und der angegebenen Region ab.</span><span class="sxs-lookup"><span data-stu-id="a6974-110">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="a6974-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6974-111">EXAMPLES</span></span>

### <span data-ttu-id="a6974-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a6974-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

<span data-ttu-id="a6974-113">Name: pstest-ID:/Subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ERS/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/flowlogs/pstest-ETag: W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState: succeeded Location: eastus TargetResourceId:/Subscriptions/56abfbd6-ec72-4ce9-831F-bc2b6f2c5505/resourceGroups/MyFlowLog/provide RS/Microsoft. Network/networkSecurityGroups/MyNSG-Datei:/Subscriptions/56abfbd6-ec72-4ce9-831F-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/Provider s/Microsoft. Storage/storageAccounts/mein Speicher aktiviert: true RetentionPolicy: {"Tage": 5, "Enabled": true} Format: {"Typ": "JSON"; "Version": 2} FlowAnalyticsConfiguration: {"networkWatcherFlowAnalyticsConfiguration": {"Enabled": wahr, "Arbeitsbereichs-Nr": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb"; "workspaceRegion": "eastus"; "workspaceResourceId": "/Subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr Oups/FlowLogsV2Demo/Anbieter/Microsoft. OperationalInsights/Arbeitsbereiche/Mein Arbeitsbereich"; "trafficAnalyticsInterval": 60}</span><span class="sxs-lookup"><span data-stu-id="a6974-113">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 }</span></span>

## <span data-ttu-id="a6974-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6974-114">PARAMETERS</span></span>

### <span data-ttu-id="a6974-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6974-115">-DefaultProfile</span></span>
<span data-ttu-id="a6974-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a6974-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6974-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="a6974-117">-Location</span></span>
<span data-ttu-id="a6974-118">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="a6974-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a6974-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a6974-119">-Name</span></span>
<span data-ttu-id="a6974-120">Der Name des Fluss Protokolls.</span><span class="sxs-lookup"><span data-stu-id="a6974-120">The flow log name.</span></span>

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

### <span data-ttu-id="a6974-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a6974-121">-NetworkWatcher</span></span>
<span data-ttu-id="a6974-122">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="a6974-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="a6974-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a6974-123">-NetworkWatcherName</span></span>
<span data-ttu-id="a6974-124">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="a6974-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="a6974-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6974-125">-ResourceGroupName</span></span>
<span data-ttu-id="a6974-126">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a6974-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a6974-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a6974-127">-ResourceId</span></span>
<span data-ttu-id="a6974-128">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a6974-128">Resource ID.</span></span>

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

### <span data-ttu-id="a6974-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6974-129">CommonParameters</span></span>
<span data-ttu-id="a6974-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6974-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6974-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6974-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6974-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a6974-132">INPUTS</span></span>

### <span data-ttu-id="a6974-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a6974-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="a6974-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a6974-134">System.String</span></span>

## <span data-ttu-id="a6974-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a6974-135">OUTPUTS</span></span>

### <span data-ttu-id="a6974-136">Microsoft. Azure. Commands. Network. Models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="a6974-136">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="a6974-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="a6974-137">NOTES</span></span>

## <span data-ttu-id="a6974-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a6974-138">RELATED LINKS</span></span>

[<span data-ttu-id="a6974-139">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a6974-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a6974-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a6974-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a6974-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a6974-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a6974-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a6974-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a6974-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a6974-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a6974-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a6974-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a6974-145">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a6974-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a6974-146">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a6974-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a6974-147">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a6974-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a6974-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a6974-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a6974-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a6974-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a6974-150">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a6974-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a6974-151">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6974-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a6974-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a6974-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a6974-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a6974-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a6974-154">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a6974-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a6974-155">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a6974-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a6974-156">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a6974-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a6974-157">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a6974-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a6974-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a6974-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a6974-159">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a6974-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a6974-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a6974-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a6974-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a6974-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a6974-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a6974-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a6974-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a6974-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a6974-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a6974-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="a6974-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a6974-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="a6974-166">Neu – AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="a6974-166">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="a6974-167">Satz-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="a6974-167">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="a6974-168">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="a6974-168">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
