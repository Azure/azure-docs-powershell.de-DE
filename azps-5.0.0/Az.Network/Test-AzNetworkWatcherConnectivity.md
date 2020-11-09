---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
ms.openlocfilehash: 8d3a714f2798c4866df39cd63c664228f078c37c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303093"
---
# <span data-ttu-id="a4ddd-101">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a4ddd-101">Test-AzNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="a4ddd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a4ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ddd-103">Gibt Verbindungsinformationen für eine angegebene Quell-VM und ein Ziel zurück.</span><span class="sxs-lookup"><span data-stu-id="a4ddd-103">Returns connectivity information for a specified source VM and a destination.</span></span>

## <span data-ttu-id="a4ddd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4ddd-104">SYNTAX</span></span>

### <span data-ttu-id="a4ddd-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="a4ddd-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4ddd-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a4ddd-106">SetByName</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4ddd-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a4ddd-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherConnectivity -Location <String> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4ddd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4ddd-108">DESCRIPTION</span></span>
<span data-ttu-id="a4ddd-109">Das Test-AzNetworkWatcherConnectivity-Cmdlet gibt Verbindungsinformationen für eine angegebene Quell-VM und ein Ziel zurück.</span><span class="sxs-lookup"><span data-stu-id="a4ddd-109">The Test-AzNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="a4ddd-110">Wenn die Verbindung zwischen Quelle und Ziel nicht hergestellt werden kann, gibt das Cmdlet Details zu dem Problem zurück.</span><span class="sxs-lookup"><span data-stu-id="a4ddd-110">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="a4ddd-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a4ddd-111">EXAMPLES</span></span>

### <span data-ttu-id="a4ddd-112">Beispiel 1: Testen der Netzwerk Überwachungs Konnektivität von einem virtuellen Computer zu einer Website</span><span class="sxs-lookup"><span data-stu-id="a4ddd-112">Example 1: Test Network Watcher Connectivity from a VM to a website</span></span>
```powershell
Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="a4ddd-113">In diesem Beispiel wird die Konnektivität von einem virtuellen Computer in Azure zu www.Bing.com getestet.</span><span class="sxs-lookup"><span data-stu-id="a4ddd-113">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

### <span data-ttu-id="a4ddd-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a4ddd-114">Example 2</span></span>

<span data-ttu-id="a4ddd-115">Gibt Verbindungsinformationen für eine angegebene Quell-VM und ein Ziel zurück.</span><span class="sxs-lookup"><span data-stu-id="a4ddd-115">Returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="a4ddd-116">automatisch</span><span class="sxs-lookup"><span data-stu-id="a4ddd-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Test-AzNetworkWatcherConnectivity -DestinationAddress 'bing.com' -DestinationPort 80 -NetworkWatcher <PSNetworkWatcher> -SourceId '/subscriptions/00000000-0000-0000-0000-00000000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0'
```

## <span data-ttu-id="a4ddd-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4ddd-117">PARAMETERS</span></span>

### <span data-ttu-id="a4ddd-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4ddd-118">-AsJob</span></span>
<span data-ttu-id="a4ddd-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a4ddd-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4ddd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ddd-120">-DefaultProfile</span></span>
<span data-ttu-id="a4ddd-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a4ddd-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4ddd-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="a4ddd-122">-DestinationAddress</span></span>
<span data-ttu-id="a4ddd-123">Die IP-Adresse oder der URI, in dem die Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4ddd-123">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="a4ddd-124">-Ziel-Nr</span><span class="sxs-lookup"><span data-stu-id="a4ddd-124">-DestinationId</span></span>
<span data-ttu-id="a4ddd-125">Die ID der Ressource, in der ein Verbindungsversuch erfolgen soll.</span><span class="sxs-lookup"><span data-stu-id="a4ddd-125">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="a4ddd-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="a4ddd-126">-DestinationPort</span></span>
<span data-ttu-id="a4ddd-127">Port, auf dem die Verbindungsprüfung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4ddd-127">Port on which check connectivity will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4ddd-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="a4ddd-128">-Location</span></span>
<span data-ttu-id="a4ddd-129">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="a4ddd-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a4ddd-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a4ddd-130">-NetworkWatcher</span></span>
<span data-ttu-id="a4ddd-131">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="a4ddd-131">The network watcher resource.</span></span>

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

### <span data-ttu-id="a4ddd-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a4ddd-132">-NetworkWatcherName</span></span>
<span data-ttu-id="a4ddd-133">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="a4ddd-133">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4ddd-134">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4ddd-134">-ProtocolConfiguration</span></span>
<span data-ttu-id="a4ddd-135">Protokollkonfiguration, auf der die Verbindungsprüfung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4ddd-135">Protocol configuration on which check connectivity will be performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4ddd-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ddd-136">-ResourceGroupName</span></span>
<span data-ttu-id="a4ddd-137">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a4ddd-137">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a4ddd-138">-Quellpfad</span><span class="sxs-lookup"><span data-stu-id="a4ddd-138">-SourceId</span></span>
<span data-ttu-id="a4ddd-139">Die ID der Ressource, aus der eine Verbindungsüberprüfung initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="a4ddd-139">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="a4ddd-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="a4ddd-140">-SourcePort</span></span>
<span data-ttu-id="a4ddd-141">Der Quell-Port, von dem eine Verbindungsüberprüfung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4ddd-141">The source port from which a connectivity check will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4ddd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ddd-142">CommonParameters</span></span>
<span data-ttu-id="a4ddd-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4ddd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ddd-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4ddd-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ddd-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a4ddd-145">INPUTS</span></span>

### <span data-ttu-id="a4ddd-146">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a4ddd-146">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="a4ddd-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a4ddd-147">System.String</span></span>

### <span data-ttu-id="a4ddd-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a4ddd-148">System.Int32</span></span>

## <span data-ttu-id="a4ddd-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a4ddd-149">OUTPUTS</span></span>

### <span data-ttu-id="a4ddd-150">Microsoft. Azure. Commands. Network. Models. PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="a4ddd-150">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="a4ddd-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="a4ddd-151">NOTES</span></span>
<span data-ttu-id="a4ddd-152">Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor</span><span class="sxs-lookup"><span data-stu-id="a4ddd-152">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="a4ddd-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a4ddd-153">RELATED LINKS</span></span>

<span data-ttu-id="a4ddd-154">[Neu – AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="a4ddd-154">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="a4ddd-155">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="a4ddd-155">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="a4ddd-156">[Neu – AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Neu – AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stopp-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="a4ddd-156">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>


<span data-ttu-id="a4ddd-157">[Anfang-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md) 
 [Neu – AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md) 
 [Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md) 
 [Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md) 
 [Stopp-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md) 
 [Anfang-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md) 
 [Satz-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Satz-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Neu – AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md) 
 [Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md) 
 [Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)</span><span class="sxs-lookup"><span data-stu-id="a4ddd-157">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md)
[New-AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md)
[Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md)
[Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md)
[Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md)
[Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md)
[Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)</span></span>
