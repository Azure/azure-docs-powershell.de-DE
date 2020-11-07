---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 1a28b061b10dc28fd5ecc0fe20cd817d7d1699b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660143"
---
# <span data-ttu-id="ed4cb-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ed4cb-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="ed4cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed4cb-102">SYNOPSIS</span></span>
<span data-ttu-id="ed4cb-103">Beendet eine laufende Paket Aufnahmesitzung</span><span class="sxs-lookup"><span data-stu-id="ed4cb-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="ed4cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed4cb-104">SYNTAX</span></span>

### <span data-ttu-id="ed4cb-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed4cb-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed4cb-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ed4cb-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed4cb-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ed4cb-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed4cb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed4cb-108">DESCRIPTION</span></span>
<span data-ttu-id="ed4cb-109">Die Stop-AzNetworkWatcherPacketCapture beendet eine laufende Paket Aufnahmesitzung.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-109">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="ed4cb-110">Nachdem die Sitzung beendet wurde, wird die Paket Erfassungs Datei je nach Konfiguration in den Speicher hochgeladen und/oder lokal auf dem virtuellen Computer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="ed4cb-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed4cb-111">EXAMPLES</span></span>

### <span data-ttu-id="ed4cb-112">Beispiel 1: Beenden einer Paket erfassungssitzung</span><span class="sxs-lookup"><span data-stu-id="ed4cb-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="ed4cb-113">In diesem Beispiel wird eine laufende Packet Capture-Sitzung mit dem Namen "PacketCaptureTest" beendet.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="ed4cb-114">Nachdem die Sitzung beendet wurde, wird die Paket Erfassungs Datei je nach Konfiguration in den Speicher hochgeladen und/oder lokal auf dem virtuellen Computer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="ed4cb-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed4cb-115">PARAMETERS</span></span>

### <span data-ttu-id="ed4cb-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed4cb-116">-AsJob</span></span>
<span data-ttu-id="ed4cb-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ed4cb-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed4cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed4cb-118">-DefaultProfile</span></span>
<span data-ttu-id="ed4cb-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed4cb-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="ed4cb-120">-Location</span></span>
<span data-ttu-id="ed4cb-121">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="ed4cb-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ed4cb-122">-NetworkWatcher</span></span>
<span data-ttu-id="ed4cb-123">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="ed4cb-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ed4cb-124">-NetworkWatcherName</span></span>
<span data-ttu-id="ed4cb-125">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="ed4cb-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="ed4cb-126">-PacketCaptureName</span></span>
<span data-ttu-id="ed4cb-127">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-127">The packet capture name.</span></span>

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

### <span data-ttu-id="ed4cb-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed4cb-128">-PassThru</span></span>
<span data-ttu-id="ed4cb-129">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-129">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="ed4cb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed4cb-130">-ResourceGroupName</span></span>
<span data-ttu-id="ed4cb-131">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ed4cb-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ed4cb-132">-Confirm</span></span>
<span data-ttu-id="ed4cb-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed4cb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed4cb-134">-WhatIf</span></span>
<span data-ttu-id="ed4cb-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed4cb-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed4cb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed4cb-137">CommonParameters</span></span>
<span data-ttu-id="ed4cb-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed4cb-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed4cb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed4cb-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed4cb-140">INPUTS</span></span>

### <span data-ttu-id="ed4cb-141">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ed4cb-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="ed4cb-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ed4cb-142">System.String</span></span>

## <span data-ttu-id="ed4cb-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed4cb-143">OUTPUTS</span></span>

### <span data-ttu-id="ed4cb-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ed4cb-144">System.Boolean</span></span>

## <span data-ttu-id="ed4cb-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed4cb-145">NOTES</span></span>
<span data-ttu-id="ed4cb-146">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk Watcher, Paket, Capture, Traffic</span><span class="sxs-lookup"><span data-stu-id="ed4cb-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="ed4cb-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed4cb-147">RELATED LINKS</span></span>

[<span data-ttu-id="ed4cb-148">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ed4cb-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ed4cb-149">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ed4cb-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ed4cb-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ed4cb-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ed4cb-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ed4cb-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ed4cb-152">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ed4cb-152">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ed4cb-153">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ed4cb-153">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ed4cb-154">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ed4cb-154">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ed4cb-155">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ed4cb-155">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ed4cb-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ed4cb-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ed4cb-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ed4cb-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ed4cb-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ed4cb-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="ed4cb-159">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ed4cb-159">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ed4cb-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ed4cb-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="ed4cb-161">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ed4cb-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ed4cb-162">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed4cb-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="ed4cb-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="ed4cb-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="ed4cb-164">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed4cb-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ed4cb-165">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed4cb-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ed4cb-166">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed4cb-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ed4cb-167">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="ed4cb-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="ed4cb-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed4cb-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ed4cb-169">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed4cb-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ed4cb-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="ed4cb-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="ed4cb-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="ed4cb-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="ed4cb-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="ed4cb-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="ed4cb-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ed4cb-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="ed4cb-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed4cb-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
