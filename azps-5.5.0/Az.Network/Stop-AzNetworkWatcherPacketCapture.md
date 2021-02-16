---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 922026b14531cc1c65f60901914383b402d06889
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146545"
---
# <span data-ttu-id="3fbe9-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3fbe9-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="3fbe9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fbe9-102">SYNOPSIS</span></span>
<span data-ttu-id="3fbe9-103">Beendet eine laufende Paketaufzeichnungssitzung</span><span class="sxs-lookup"><span data-stu-id="3fbe9-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="3fbe9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3fbe9-104">SYNTAX</span></span>

### <span data-ttu-id="3fbe9-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="3fbe9-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fbe9-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3fbe9-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fbe9-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3fbe9-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fbe9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3fbe9-108">DESCRIPTION</span></span>
<span data-ttu-id="3fbe9-109">Die Stop-AzNetworkWatcherPacketCapture beendet eine laufende Paketaufzeichnungssitzung.</span><span class="sxs-lookup"><span data-stu-id="3fbe9-109">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="3fbe9-110">Nach dem Beenden der Sitzung wird die Paketaufzeichnungsdatei in den Speicher hochgeladen und/oder lokal auf der VM gespeichert, je nach Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3fbe9-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="3fbe9-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3fbe9-111">EXAMPLES</span></span>

### <span data-ttu-id="3fbe9-112">Beispiel 1: Beenden einer Paketaufzeichnungssitzung</span><span class="sxs-lookup"><span data-stu-id="3fbe9-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="3fbe9-113">In diesem Beispiel wird eine laufende Paketaufzeichnungssitzung mit dem Namen "PacketCaptureTest" beendet.</span><span class="sxs-lookup"><span data-stu-id="3fbe9-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="3fbe9-114">Nach dem Beenden der Sitzung wird die Paketaufzeichnungsdatei in den Speicher hochgeladen und/oder lokal auf der VM gespeichert, je nach Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3fbe9-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="3fbe9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fbe9-115">PARAMETERS</span></span>

### <span data-ttu-id="3fbe9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fbe9-116">-AsJob</span></span>
<span data-ttu-id="3fbe9-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3fbe9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3fbe9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fbe9-118">-DefaultProfile</span></span>
<span data-ttu-id="3fbe9-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3fbe9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fbe9-120">-Location</span><span class="sxs-lookup"><span data-stu-id="3fbe9-120">-Location</span></span>
<span data-ttu-id="3fbe9-121">Position der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="3fbe9-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3fbe9-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3fbe9-122">-NetworkWatcher</span></span>
<span data-ttu-id="3fbe9-123">Die Netzwerk-Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="3fbe9-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="3fbe9-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3fbe9-124">-NetworkWatcherName</span></span>
<span data-ttu-id="3fbe9-125">Der Name der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="3fbe9-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="3fbe9-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="3fbe9-126">-PacketCaptureName</span></span>
<span data-ttu-id="3fbe9-127">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="3fbe9-127">The packet capture name.</span></span>

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

### <span data-ttu-id="3fbe9-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fbe9-128">-PassThru</span></span>
<span data-ttu-id="3fbe9-129">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="3fbe9-129">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="3fbe9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fbe9-130">-ResourceGroupName</span></span>
<span data-ttu-id="3fbe9-131">Der Name der Ressourcengruppe "Netzwerk-Watcher".</span><span class="sxs-lookup"><span data-stu-id="3fbe9-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3fbe9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3fbe9-132">-Confirm</span></span>
<span data-ttu-id="3fbe9-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3fbe9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fbe9-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3fbe9-134">-WhatIf</span></span>
<span data-ttu-id="3fbe9-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3fbe9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fbe9-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3fbe9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fbe9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fbe9-137">CommonParameters</span></span>
<span data-ttu-id="3fbe9-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fbe9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fbe9-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fbe9-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fbe9-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3fbe9-140">INPUTS</span></span>

### <span data-ttu-id="3fbe9-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3fbe9-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="3fbe9-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3fbe9-142">System.String</span></span>

## <span data-ttu-id="3fbe9-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3fbe9-143">OUTPUTS</span></span>

### <span data-ttu-id="3fbe9-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3fbe9-144">System.Boolean</span></span>

## <span data-ttu-id="3fbe9-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3fbe9-145">NOTES</span></span>
<span data-ttu-id="3fbe9-146">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span><span class="sxs-lookup"><span data-stu-id="3fbe9-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="3fbe9-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3fbe9-147">RELATED LINKS</span></span>

[<span data-ttu-id="3fbe9-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3fbe9-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3fbe9-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3fbe9-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="3fbe9-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3fbe9-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3fbe9-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3fbe9-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3fbe9-152">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3fbe9-152">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="3fbe9-153">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3fbe9-153">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="3fbe9-154">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3fbe9-154">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="3fbe9-155">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3fbe9-155">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="3fbe9-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3fbe9-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="3fbe9-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3fbe9-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3fbe9-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3fbe9-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="3fbe9-159">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3fbe9-159">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3fbe9-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3fbe9-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="3fbe9-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3fbe9-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3fbe9-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3fbe9-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="3fbe9-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3fbe9-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="3fbe9-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3fbe9-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3fbe9-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3fbe9-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3fbe9-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3fbe9-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3fbe9-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3fbe9-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="3fbe9-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3fbe9-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3fbe9-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3fbe9-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3fbe9-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3fbe9-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="3fbe9-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="3fbe9-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="3fbe9-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3fbe9-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="3fbe9-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3fbe9-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="3fbe9-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3fbe9-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
