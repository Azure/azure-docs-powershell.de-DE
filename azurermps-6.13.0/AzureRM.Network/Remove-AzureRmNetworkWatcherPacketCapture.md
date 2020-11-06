---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 0c0568dc11411e27af1db9d9e3d59c0026b0a39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503521"
---
# <span data-ttu-id="03c01-101">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="03c01-101">Remove-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="03c01-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="03c01-102">SYNOPSIS</span></span>
<span data-ttu-id="03c01-103">Entfernt eine Paket Erfassungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="03c01-103">Removes a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03c01-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="03c01-104">SYNTAX</span></span>

### <span data-ttu-id="03c01-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="03c01-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03c01-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="03c01-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03c01-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="03c01-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03c01-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03c01-108">DESCRIPTION</span></span>
<span data-ttu-id="03c01-109">Die Remove-AzureRmNetworkWatcherPacketCapture entfernt eine Sammlungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="03c01-109">The Remove-AzureRmNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="03c01-110">Es wird empfohlen, Stop-AzureRmNetworkWatcherPacketCapture aufzurufen, bevor Sie Remove-AzureRmNetworkWatcherPacketCapture aufrufen.</span><span class="sxs-lookup"><span data-stu-id="03c01-110">It is recommended to call Stop-AzureRmNetworkWatcherPacketCapture before calling Remove-AzureRmNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="03c01-111">Wenn die Paket Aufnahmesitzung ausgeführt wird, wenn Remove-AzureRmNetworkWatcherPacketCapture aufgerufen wird, wird die Paketerfassung möglicherweise nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="03c01-111">If the packet capture session is running when Remove-AzureRmNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="03c01-112">Wenn die Sitzung vor dem Entfernen angehalten wird, wird die Cap-Datei, die die Aufnahmedaten enthält, nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="03c01-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="03c01-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="03c01-113">EXAMPLES</span></span>

### <span data-ttu-id="03c01-114">Beispiel 1: Entfernen einer Paket erfassungssitzung</span><span class="sxs-lookup"><span data-stu-id="03c01-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="03c01-115">In diesem Beispiel wird eine vorhandene Paket erfassungssitzung mit dem Namen "PacketCaptureTest" entfernt.</span><span class="sxs-lookup"><span data-stu-id="03c01-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="03c01-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="03c01-116">PARAMETERS</span></span>

### <span data-ttu-id="03c01-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03c01-117">-AsJob</span></span>
<span data-ttu-id="03c01-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="03c01-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03c01-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c01-119">-DefaultProfile</span></span>
<span data-ttu-id="03c01-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="03c01-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c01-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="03c01-121">-Location</span></span>
<span data-ttu-id="03c01-122">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="03c01-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="03c01-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="03c01-123">-NetworkWatcher</span></span>
<span data-ttu-id="03c01-124">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="03c01-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="03c01-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="03c01-125">-NetworkWatcherName</span></span>
<span data-ttu-id="03c01-126">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="03c01-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="03c01-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="03c01-127">-PacketCaptureName</span></span>
<span data-ttu-id="03c01-128">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="03c01-128">The packet capture name.</span></span>

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

### <span data-ttu-id="03c01-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03c01-129">-PassThru</span></span>
<span data-ttu-id="03c01-130">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="03c01-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="03c01-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03c01-131">-ResourceGroupName</span></span>
<span data-ttu-id="03c01-132">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="03c01-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="03c01-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="03c01-133">-Confirm</span></span>
<span data-ttu-id="03c01-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="03c01-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03c01-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03c01-135">-WhatIf</span></span>
<span data-ttu-id="03c01-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="03c01-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03c01-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="03c01-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03c01-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c01-138">CommonParameters</span></span>
<span data-ttu-id="03c01-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03c01-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c01-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03c01-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c01-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="03c01-141">INPUTS</span></span>

### <span data-ttu-id="03c01-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="03c01-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="03c01-143">Parameter: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="03c01-143">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="03c01-144">System. String</span><span class="sxs-lookup"><span data-stu-id="03c01-144">System.String</span></span>
<span data-ttu-id="03c01-145">Parameter: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="03c01-145">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="03c01-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="03c01-146">OUTPUTS</span></span>

### <span data-ttu-id="03c01-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="03c01-147">System.Boolean</span></span>

## <span data-ttu-id="03c01-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="03c01-148">NOTES</span></span>
<span data-ttu-id="03c01-149">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerkmonitor, Paket, erfassen, Datenverkehr, entfernen</span><span class="sxs-lookup"><span data-stu-id="03c01-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="03c01-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="03c01-150">RELATED LINKS</span></span>

[<span data-ttu-id="03c01-151">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="03c01-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="03c01-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="03c01-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="03c01-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="03c01-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="03c01-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="03c01-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="03c01-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="03c01-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="03c01-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="03c01-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="03c01-157">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="03c01-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="03c01-158">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="03c01-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="03c01-159">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="03c01-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="03c01-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="03c01-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="03c01-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="03c01-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="03c01-162">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="03c01-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="03c01-163">Neu – AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="03c01-163">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="03c01-164">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="03c01-164">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="03c01-165">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="03c01-165">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="03c01-166">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03c01-166">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="03c01-167">Anfang-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03c01-167">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="03c01-168">Satz-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03c01-168">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="03c01-169">Satz-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="03c01-169">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="03c01-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03c01-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="03c01-171">Neu – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03c01-171">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="03c01-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="03c01-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="03c01-173">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="03c01-173">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="03c01-174">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="03c01-174">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="03c01-175">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="03c01-175">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="03c01-176">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="03c01-176">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="03c01-177">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03c01-177">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
