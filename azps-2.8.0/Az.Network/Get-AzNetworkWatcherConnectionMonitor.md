---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 0c59de4b0c6dfd7da196b4ec67999406a14e0d1a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821788"
---
# <span data-ttu-id="f3c2e-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f3c2e-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="f3c2e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3c2e-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c2e-103">Gibt den Verbindungsmonitor mit dem angegebenen Namen oder der Liste der Verbindungs Monitore zurück.</span><span class="sxs-lookup"><span data-stu-id="f3c2e-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="f3c2e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3c2e-104">SYNTAX</span></span>

### <span data-ttu-id="f3c2e-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f3c2e-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3c2e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f3c2e-106">SetByResource</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3c2e-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f3c2e-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3c2e-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f3c2e-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3c2e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3c2e-109">DESCRIPTION</span></span>
<span data-ttu-id="f3c2e-110">Das Get-AzNetworkWatcherConnectionMonitor-Cmdlet gibt den Verbindungsmonitor mit dem angegebenen Namen/der angegebenen Resourcen-oder der Liste der Verbindungs Monitore zurück, die dem angegebenen Netzwerkmonitor/-Standort entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f3c2e-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="f3c2e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3c2e-111">EXAMPLES</span></span>

### <span data-ttu-id="f3c2e-112">Beispiel 1: Abrufen des Verbindungs Monitors anhand des Namens an der angegebenen Position</span><span class="sxs-lookup"><span data-stu-id="f3c2e-112">Example 1: Get connection monitor by name in the specified location</span></span>
```
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6
                              a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C
                              ompute/virtualMachines/irinavm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Stopped
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="f3c2e-113">In diesem Beispiel wird der Verbindungsmonitor über den Namen an der angegebenen Position abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f3c2e-113">In this example we get connection monitor by name in the specified location.</span></span>

### <span data-ttu-id="f3c2e-114">Beispiel 2: Abrufen von Verbindungs Monitoren mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="f3c2e-114">Example 2: Get connection monitors using filtering</span></span>
```
PS C:\> Get-AzNetworkWatcherConnectionMonitor -ResourceGroupName NetworkWatcherRG -NetworkWatcherName NetworkWatcher_centraluseuap -Name cm*


Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6
                              a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C
                              ompute/virtualMachines/irinavm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Stopped
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="f3c2e-115">In diesem Beispiel erhalten wir alle Verbindungs Monitore in NetworkWatcher_centraluseuap, die mit "cm" beginnen.</span><span class="sxs-lookup"><span data-stu-id="f3c2e-115">In this example we get all connection monitors in NetworkWatcher_centraluseuap that start with "cm"</span></span>

## <span data-ttu-id="f3c2e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3c2e-116">PARAMETERS</span></span>

### <span data-ttu-id="f3c2e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c2e-117">-DefaultProfile</span></span>
<span data-ttu-id="f3c2e-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3c2e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3c2e-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="f3c2e-119">-Location</span></span>
<span data-ttu-id="f3c2e-120">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="f3c2e-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="f3c2e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f3c2e-121">-Name</span></span>
<span data-ttu-id="f3c2e-122">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="f3c2e-122">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="f3c2e-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f3c2e-123">-NetworkWatcher</span></span>
<span data-ttu-id="f3c2e-124">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="f3c2e-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="f3c2e-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f3c2e-125">-NetworkWatcherName</span></span>
<span data-ttu-id="f3c2e-126">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="f3c2e-126">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c2e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3c2e-127">-ResourceGroupName</span></span>
<span data-ttu-id="f3c2e-128">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f3c2e-128">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c2e-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f3c2e-129">-ResourceId</span></span>
<span data-ttu-id="f3c2e-130">Die Ressourcen-ID des Verbindungs Monitors.</span><span class="sxs-lookup"><span data-stu-id="f3c2e-130">Resource ID of the connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c2e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c2e-131">CommonParameters</span></span>
<span data-ttu-id="f3c2e-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3c2e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c2e-133">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3c2e-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c2e-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3c2e-134">INPUTS</span></span>

### <span data-ttu-id="f3c2e-135">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f3c2e-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="f3c2e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f3c2e-136">System.String</span></span>

## <span data-ttu-id="f3c2e-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3c2e-137">OUTPUTS</span></span>

### <span data-ttu-id="f3c2e-138">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="f3c2e-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="f3c2e-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3c2e-139">NOTES</span></span>
<span data-ttu-id="f3c2e-140">Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor, Verbindungsmonitor</span><span class="sxs-lookup"><span data-stu-id="f3c2e-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="f3c2e-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3c2e-141">RELATED LINKS</span></span>

[<span data-ttu-id="f3c2e-142">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f3c2e-142">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f3c2e-143">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f3c2e-143">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f3c2e-144">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f3c2e-144">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f3c2e-145">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f3c2e-145">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f3c2e-146">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f3c2e-146">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f3c2e-147">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f3c2e-147">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f3c2e-148">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f3c2e-148">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f3c2e-149">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f3c2e-149">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f3c2e-150">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f3c2e-150">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f3c2e-151">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f3c2e-151">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f3c2e-152">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f3c2e-152">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f3c2e-153">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f3c2e-153">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f3c2e-154">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f3c2e-154">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f3c2e-155">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f3c2e-155">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="f3c2e-156">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f3c2e-156">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f3c2e-157">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f3c2e-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f3c2e-158">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f3c2e-158">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f3c2e-159">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f3c2e-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f3c2e-160">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3c2e-160">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="f3c2e-161">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f3c2e-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f3c2e-162">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f3c2e-162">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="f3c2e-163">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f3c2e-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f3c2e-164">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f3c2e-164">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f3c2e-165">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f3c2e-165">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="f3c2e-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f3c2e-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="f3c2e-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f3c2e-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="f3c2e-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f3c2e-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
