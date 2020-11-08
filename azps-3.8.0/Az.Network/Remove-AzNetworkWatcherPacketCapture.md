---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 6002f420e0e4d1c3a0a61c8524ec6b2022075b52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004272"
---
# <span data-ttu-id="08e37-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="08e37-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="08e37-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08e37-102">SYNOPSIS</span></span>
<span data-ttu-id="08e37-103">Entfernt eine Paket Erfassungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="08e37-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="08e37-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08e37-104">SYNTAX</span></span>

### <span data-ttu-id="08e37-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="08e37-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08e37-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="08e37-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08e37-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="08e37-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08e37-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08e37-108">DESCRIPTION</span></span>
<span data-ttu-id="08e37-109">Die Remove-AzNetworkWatcherPacketCapture entfernt eine Sammlungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="08e37-109">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="08e37-110">Es wird empfohlen, Stop-AzNetworkWatcherPacketCapture aufzurufen, bevor Sie Remove-AzNetworkWatcherPacketCapture aufrufen.</span><span class="sxs-lookup"><span data-stu-id="08e37-110">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="08e37-111">Wenn die Paket Aufnahmesitzung ausgeführt wird, wenn Remove-AzNetworkWatcherPacketCapture aufgerufen wird, wird die Paketerfassung möglicherweise nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="08e37-111">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="08e37-112">Wenn die Sitzung vor dem Entfernen angehalten wird, wird die Cap-Datei, die die Aufnahmedaten enthält, nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="08e37-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="08e37-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08e37-113">EXAMPLES</span></span>

### <span data-ttu-id="08e37-114">Beispiel 1: Entfernen einer Paket erfassungssitzung</span><span class="sxs-lookup"><span data-stu-id="08e37-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="08e37-115">In diesem Beispiel wird eine vorhandene Paket erfassungssitzung mit dem Namen "PacketCaptureTest" entfernt.</span><span class="sxs-lookup"><span data-stu-id="08e37-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="08e37-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="08e37-116">PARAMETERS</span></span>

### <span data-ttu-id="08e37-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08e37-117">-AsJob</span></span>
<span data-ttu-id="08e37-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="08e37-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="08e37-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e37-119">-DefaultProfile</span></span>
<span data-ttu-id="08e37-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="08e37-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08e37-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="08e37-121">-Location</span></span>
<span data-ttu-id="08e37-122">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="08e37-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="08e37-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="08e37-123">-NetworkWatcher</span></span>
<span data-ttu-id="08e37-124">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="08e37-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="08e37-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="08e37-125">-NetworkWatcherName</span></span>
<span data-ttu-id="08e37-126">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="08e37-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="08e37-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="08e37-127">-PacketCaptureName</span></span>
<span data-ttu-id="08e37-128">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="08e37-128">The packet capture name.</span></span>

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

### <span data-ttu-id="08e37-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08e37-129">-PassThru</span></span>
<span data-ttu-id="08e37-130">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="08e37-130">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08e37-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08e37-131">-ResourceGroupName</span></span>
<span data-ttu-id="08e37-132">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="08e37-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="08e37-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="08e37-133">-Confirm</span></span>
<span data-ttu-id="08e37-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08e37-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08e37-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08e37-135">-WhatIf</span></span>
<span data-ttu-id="08e37-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08e37-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08e37-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08e37-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08e37-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e37-138">CommonParameters</span></span>
<span data-ttu-id="08e37-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08e37-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e37-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08e37-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e37-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08e37-141">INPUTS</span></span>

### <span data-ttu-id="08e37-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="08e37-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="08e37-143">System. String</span><span class="sxs-lookup"><span data-stu-id="08e37-143">System.String</span></span>

## <span data-ttu-id="08e37-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08e37-144">OUTPUTS</span></span>

### <span data-ttu-id="08e37-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="08e37-145">System.Boolean</span></span>

## <span data-ttu-id="08e37-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="08e37-146">NOTES</span></span>
<span data-ttu-id="08e37-147">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerkmonitor, Paket, erfassen, Datenverkehr, entfernen</span><span class="sxs-lookup"><span data-stu-id="08e37-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="08e37-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08e37-148">RELATED LINKS</span></span>

[<span data-ttu-id="08e37-149">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="08e37-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="08e37-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="08e37-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="08e37-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="08e37-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="08e37-152">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="08e37-152">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="08e37-153">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="08e37-153">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="08e37-154">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="08e37-154">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="08e37-155">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="08e37-155">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="08e37-156">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="08e37-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="08e37-157">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="08e37-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="08e37-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="08e37-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="08e37-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="08e37-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="08e37-160">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="08e37-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="08e37-161">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="08e37-161">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="08e37-162">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="08e37-162">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="08e37-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="08e37-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="08e37-164">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="08e37-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="08e37-165">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="08e37-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="08e37-166">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="08e37-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="08e37-167">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="08e37-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="08e37-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="08e37-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="08e37-169">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="08e37-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="08e37-170">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="08e37-170">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="08e37-171">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="08e37-171">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="08e37-172">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="08e37-172">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="08e37-173">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="08e37-173">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="08e37-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="08e37-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="08e37-175">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="08e37-175">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
