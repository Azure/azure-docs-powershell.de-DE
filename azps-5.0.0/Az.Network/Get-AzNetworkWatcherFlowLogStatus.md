---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: dd88c40876bf3ceb5f90a7088f5943fcf5f18ce8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302789"
---
# <span data-ttu-id="fad25-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="fad25-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="fad25-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fad25-102">SYNOPSIS</span></span>
<span data-ttu-id="fad25-103">Ruft den Status der Fluss Protokollierung für eine Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="fad25-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="fad25-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fad25-104">SYNTAX</span></span>

### <span data-ttu-id="fad25-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="fad25-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fad25-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="fad25-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fad25-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="fad25-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -Location <String> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fad25-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fad25-108">DESCRIPTION</span></span>
<span data-ttu-id="fad25-109">Das Get-AzNetworkWatcherFlowLogStatus-Cmdlet ruft den Status der Fluss Protokollierung für eine Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="fad25-109">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="fad25-110">Der Status umfasst, ob die Fluss Protokollierung für die bereitgestellte Ressource aktiviert ist, das konfigurierte Speicherkonto zum Senden von Protokollen und die Aufbewahrungsrichtlinie für die Protokolle.</span><span class="sxs-lookup"><span data-stu-id="fad25-110">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="fad25-111">Zurzeit werden Netzwerk Sicherheitsgruppen für die Fluss Protokollierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fad25-111">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="fad25-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fad25-112">EXAMPLES</span></span>

### <span data-ttu-id="fad25-113">Beispiel 1: Abrufen des Fluss Protokollierungs Status für eine angegebene NSG</span><span class="sxs-lookup"><span data-stu-id="fad25-113">Example 1: Get the Flow Logging Status for a Specified NSG</span></span>
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

<span data-ttu-id="fad25-114">In diesem Beispiel wird der Fluss Protokollierungsstatus für eine Netzwerksicherheitsgruppe abgerufen.</span><span class="sxs-lookup"><span data-stu-id="fad25-114">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="fad25-115">Bei der angegebenen NSG ist die Fluss Protokollierung aktiviert, das Standardformat und keine Aufbewahrungsrichtlinie festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fad25-115">The specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="fad25-116">Beispiel 2: Abrufen der Fluss Protokollierung und des Datenverkehrsanalyse Status für eine angegebene NSG</span><span class="sxs-lookup"><span data-stu-id="fad25-116">Example 2: Get the Flow Logging and Traffic Analytics Status for a Specified NSG</span></span>
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

<span data-ttu-id="fad25-117">In diesem Beispiel wird der Fluss Protokollierungs-und Datenverkehrsanalyse Status für eine Netzwerksicherheitsgruppe abgerufen.</span><span class="sxs-lookup"><span data-stu-id="fad25-117">In this example we get the flow logging and Traffic Analytics status for a Network Security Group.</span></span> <span data-ttu-id="fad25-118">In der angegebenen NSG sind Fluss Protokollierung und Datenverkehrsanalyse aktiviert, Standardformat und keine Aufbewahrungsrichtlinie festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fad25-118">The specified NSG has flow logging and Traffic Analytics enabled, default format and no retention policy set.</span></span>

## <span data-ttu-id="fad25-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="fad25-119">PARAMETERS</span></span>

### <span data-ttu-id="fad25-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fad25-120">-AsJob</span></span>
<span data-ttu-id="fad25-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fad25-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fad25-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fad25-122">-DefaultProfile</span></span>
<span data-ttu-id="fad25-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fad25-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fad25-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="fad25-124">-Location</span></span>
<span data-ttu-id="fad25-125">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="fad25-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="fad25-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fad25-126">-NetworkWatcher</span></span>
<span data-ttu-id="fad25-127">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="fad25-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="fad25-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="fad25-128">-NetworkWatcherName</span></span>
<span data-ttu-id="fad25-129">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="fad25-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="fad25-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fad25-130">-ResourceGroupName</span></span>
<span data-ttu-id="fad25-131">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="fad25-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="fad25-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="fad25-132">-TargetResourceId</span></span>
<span data-ttu-id="fad25-133">Die Ziel Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="fad25-133">The target resource ID.</span></span>

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

### <span data-ttu-id="fad25-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fad25-134">CommonParameters</span></span>
<span data-ttu-id="fad25-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fad25-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fad25-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fad25-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fad25-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fad25-137">INPUTS</span></span>

### <span data-ttu-id="fad25-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fad25-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="fad25-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fad25-139">System.String</span></span>

## <span data-ttu-id="fad25-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fad25-140">OUTPUTS</span></span>

### <span data-ttu-id="fad25-141">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="fad25-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="fad25-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="fad25-142">NOTES</span></span>
<span data-ttu-id="fad25-143">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Netzwerk, Netzwerk, Watcher, Fluss, Protokolle, flowlog, Protokollierung</span><span class="sxs-lookup"><span data-stu-id="fad25-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="fad25-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fad25-144">RELATED LINKS</span></span>

[<span data-ttu-id="fad25-145">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fad25-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="fad25-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fad25-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="fad25-147">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fad25-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="fad25-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="fad25-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="fad25-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="fad25-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="fad25-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="fad25-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="fad25-151">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="fad25-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="fad25-152">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fad25-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fad25-153">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="fad25-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="fad25-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fad25-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fad25-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fad25-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fad25-156">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fad25-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fad25-157">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="fad25-157">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="fad25-158">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="fad25-158">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="fad25-159">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="fad25-159">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="fad25-160">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fad25-160">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fad25-161">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fad25-161">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fad25-162">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fad25-162">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fad25-163">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="fad25-163">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="fad25-164">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fad25-164">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fad25-165">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fad25-165">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fad25-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="fad25-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="fad25-167">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="fad25-167">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="fad25-168">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="fad25-168">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="fad25-169">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="fad25-169">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="fad25-170">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="fad25-170">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="fad25-171">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fad25-171">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
