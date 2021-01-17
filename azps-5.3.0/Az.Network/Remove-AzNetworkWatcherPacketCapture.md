---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: e22b9d85bbc17897742fa2ac0cbdf3e2d8187d5b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473462"
---
# <span data-ttu-id="9f917-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9f917-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="9f917-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f917-102">SYNOPSIS</span></span>
<span data-ttu-id="9f917-103">Entfernt eine Paketerfassungsressource.</span><span class="sxs-lookup"><span data-stu-id="9f917-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="9f917-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f917-104">SYNTAX</span></span>

### <span data-ttu-id="9f917-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="9f917-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f917-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="9f917-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f917-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9f917-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f917-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f917-108">DESCRIPTION</span></span>
<span data-ttu-id="9f917-109">Der Remove-AzNetworkWatcherPacketCapture entfernt eine Paketaufnahmeressource.</span><span class="sxs-lookup"><span data-stu-id="9f917-109">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="9f917-110">Es wird empfohlen, die Stop-AzNetworkWatcherPacketCapture, bevor Sie Remove-AzNetworkWatcherPacketCapture aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9f917-110">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="9f917-111">Wenn die Paketaufzeichnungssitzung ausgeführt wird, Remove-AzNetworkWatcherPacketCapture als Paketaufzeichnung bezeichnet wird, wird die Paketaufzeichnung möglicherweise nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9f917-111">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="9f917-112">Wenn die Sitzung vor dem Entfernen beendet wird, wird die CAP-Datei, die Aufnahmedaten enthält, nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="9f917-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="9f917-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9f917-113">EXAMPLES</span></span>

### <span data-ttu-id="9f917-114">Beispiel 1: Entfernen einer Paketaufzeichnungssitzung</span><span class="sxs-lookup"><span data-stu-id="9f917-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="9f917-115">In diesem Beispiel entfernen wir eine vorhandene Paketaufzeichnungssitzung namens "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="9f917-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="9f917-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f917-116">PARAMETERS</span></span>

### <span data-ttu-id="9f917-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f917-117">-AsJob</span></span>
<span data-ttu-id="9f917-118">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9f917-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f917-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f917-119">-DefaultProfile</span></span>
<span data-ttu-id="9f917-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f917-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f917-121">-Location</span><span class="sxs-lookup"><span data-stu-id="9f917-121">-Location</span></span>
<span data-ttu-id="9f917-122">Speicherort der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="9f917-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="9f917-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9f917-123">-NetworkWatcher</span></span>
<span data-ttu-id="9f917-124">Die Netzwerk-Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="9f917-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="9f917-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9f917-125">-NetworkWatcherName</span></span>
<span data-ttu-id="9f917-126">Der Name der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="9f917-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="9f917-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="9f917-127">-PacketCaptureName</span></span>
<span data-ttu-id="9f917-128">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="9f917-128">The packet capture name.</span></span>

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

### <span data-ttu-id="9f917-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f917-129">-PassThru</span></span>
<span data-ttu-id="9f917-130">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="9f917-130">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="9f917-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f917-131">-ResourceGroupName</span></span>
<span data-ttu-id="9f917-132">Der Name der Ressourcengruppe "Netzwerk-Watcher".</span><span class="sxs-lookup"><span data-stu-id="9f917-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9f917-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f917-133">-Confirm</span></span>
<span data-ttu-id="9f917-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f917-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f917-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9f917-135">-WhatIf</span></span>
<span data-ttu-id="9f917-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f917-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f917-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f917-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f917-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f917-138">CommonParameters</span></span>
<span data-ttu-id="9f917-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f917-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f917-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f917-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f917-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9f917-141">INPUTS</span></span>

### <span data-ttu-id="9f917-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9f917-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="9f917-143">System.String</span><span class="sxs-lookup"><span data-stu-id="9f917-143">System.String</span></span>

## <span data-ttu-id="9f917-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9f917-144">OUTPUTS</span></span>

### <span data-ttu-id="9f917-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9f917-145">System.Boolean</span></span>

## <span data-ttu-id="9f917-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9f917-146">NOTES</span></span>
<span data-ttu-id="9f917-147">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span><span class="sxs-lookup"><span data-stu-id="9f917-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="9f917-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9f917-148">RELATED LINKS</span></span>

[<span data-ttu-id="9f917-149">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9f917-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="9f917-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9f917-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="9f917-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9f917-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="9f917-152">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9f917-152">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="9f917-153">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9f917-153">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9f917-154">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9f917-154">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="9f917-155">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9f917-155">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9f917-156">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9f917-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9f917-157">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9f917-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="9f917-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9f917-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9f917-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9f917-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9f917-160">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9f917-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9f917-161">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f917-161">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="9f917-162">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9f917-162">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="9f917-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="9f917-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="9f917-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9f917-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9f917-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9f917-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9f917-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9f917-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9f917-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="9f917-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="9f917-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9f917-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9f917-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9f917-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9f917-170">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9f917-170">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="9f917-171">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9f917-171">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="9f917-172">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="9f917-172">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="9f917-173">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="9f917-173">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="9f917-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="9f917-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="9f917-175">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9f917-175">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
