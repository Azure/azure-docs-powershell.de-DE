---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 42067c978c7791740d10af4df88c51dde3096c0e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409000"
---
# <span data-ttu-id="46f07-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="46f07-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="46f07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46f07-102">SYNOPSIS</span></span>
<span data-ttu-id="46f07-103">Beendet eine laufende Paketaufzeichnungssitzung</span><span class="sxs-lookup"><span data-stu-id="46f07-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="46f07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46f07-104">SYNTAX</span></span>

### <span data-ttu-id="46f07-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="46f07-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46f07-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="46f07-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46f07-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="46f07-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46f07-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46f07-108">DESCRIPTION</span></span>
<span data-ttu-id="46f07-109">Die Stop-AzNetworkWatcherPacketCapture beendet eine laufende Paketaufzeichnungssitzung.</span><span class="sxs-lookup"><span data-stu-id="46f07-109">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="46f07-110">Nach dem Beenden der Sitzung wird die Paketaufzeichnungsdatei in den Speicher hochgeladen und/oder lokal auf der VM gespeichert, je nach Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="46f07-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="46f07-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="46f07-111">EXAMPLES</span></span>

### <span data-ttu-id="46f07-112">Beispiel 1: Beenden einer Paketaufzeichnungssitzung</span><span class="sxs-lookup"><span data-stu-id="46f07-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="46f07-113">In diesem Beispiel wird eine laufende Paketaufzeichnungssitzung mit dem Namen "PacketCaptureTest" beendet.</span><span class="sxs-lookup"><span data-stu-id="46f07-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="46f07-114">Nach dem Beenden der Sitzung wird die Paketaufzeichnungsdatei in den Speicher hochgeladen und/oder lokal auf der VM gespeichert, je nach Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="46f07-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="46f07-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46f07-115">PARAMETERS</span></span>

### <span data-ttu-id="46f07-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46f07-116">-AsJob</span></span>
<span data-ttu-id="46f07-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="46f07-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46f07-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46f07-118">-DefaultProfile</span></span>
<span data-ttu-id="46f07-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46f07-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46f07-120">-Location</span><span class="sxs-lookup"><span data-stu-id="46f07-120">-Location</span></span>
<span data-ttu-id="46f07-121">Speicherort der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="46f07-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="46f07-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="46f07-122">-NetworkWatcher</span></span>
<span data-ttu-id="46f07-123">Die Netzwerk-Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="46f07-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="46f07-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="46f07-124">-NetworkWatcherName</span></span>
<span data-ttu-id="46f07-125">Der Name der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="46f07-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="46f07-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="46f07-126">-PacketCaptureName</span></span>
<span data-ttu-id="46f07-127">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="46f07-127">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f07-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46f07-128">-PassThru</span></span>
<span data-ttu-id="46f07-129">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="46f07-129">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="46f07-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46f07-130">-ResourceGroupName</span></span>
<span data-ttu-id="46f07-131">Der Name der Ressourcengruppe "Netzwerk-Watcher".</span><span class="sxs-lookup"><span data-stu-id="46f07-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="46f07-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46f07-132">-Confirm</span></span>
<span data-ttu-id="46f07-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46f07-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f07-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="46f07-134">-WhatIf</span></span>
<span data-ttu-id="46f07-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46f07-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46f07-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46f07-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f07-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f07-137">CommonParameters</span></span>
<span data-ttu-id="46f07-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46f07-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f07-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46f07-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f07-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="46f07-140">INPUTS</span></span>

### <span data-ttu-id="46f07-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="46f07-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="46f07-142">System.String</span><span class="sxs-lookup"><span data-stu-id="46f07-142">System.String</span></span>

## <span data-ttu-id="46f07-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="46f07-143">OUTPUTS</span></span>

### <span data-ttu-id="46f07-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="46f07-144">System.Boolean</span></span>

## <span data-ttu-id="46f07-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="46f07-145">NOTES</span></span>
<span data-ttu-id="46f07-146">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span><span class="sxs-lookup"><span data-stu-id="46f07-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="46f07-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="46f07-147">RELATED LINKS</span></span>

[<span data-ttu-id="46f07-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="46f07-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="46f07-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="46f07-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="46f07-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="46f07-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="46f07-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="46f07-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="46f07-152">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="46f07-152">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="46f07-153">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="46f07-153">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="46f07-154">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="46f07-154">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="46f07-155">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="46f07-155">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="46f07-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="46f07-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="46f07-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="46f07-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="46f07-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="46f07-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="46f07-159">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="46f07-159">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="46f07-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="46f07-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="46f07-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="46f07-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="46f07-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="46f07-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="46f07-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="46f07-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="46f07-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="46f07-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="46f07-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="46f07-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="46f07-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="46f07-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="46f07-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="46f07-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="46f07-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="46f07-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="46f07-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="46f07-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="46f07-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="46f07-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="46f07-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="46f07-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="46f07-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="46f07-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="46f07-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="46f07-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="46f07-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="46f07-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
