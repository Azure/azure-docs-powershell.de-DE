---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 83d7da65ad8c525d4c37ab1b5f78eb72bf1d9f49
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473356"
---
# <span data-ttu-id="26625-101">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="26625-101">Start-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="26625-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26625-102">SYNOPSIS</span></span>
<span data-ttu-id="26625-103">Starten eines Verbindungsmonitors</span><span class="sxs-lookup"><span data-stu-id="26625-103">Start a connection monitor</span></span>

## <span data-ttu-id="26625-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26625-104">SYNTAX</span></span>

### <span data-ttu-id="26625-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="26625-105">SetByName (Default)</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26625-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="26625-106">SetByResource</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26625-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="26625-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26625-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="26625-108">SetByResourceId</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26625-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="26625-109">SetByInputObject</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26625-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26625-110">DESCRIPTION</span></span>
<span data-ttu-id="26625-111">Das Start-AzNetworkWatcherConnectionMonitor cmdlet startet den angegebenen Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="26625-111">The Start-AzNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="26625-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="26625-112">EXAMPLES</span></span>

### <span data-ttu-id="26625-113">Beispiel 1: Starten eines Verbindungsmonitors</span><span class="sxs-lookup"><span data-stu-id="26625-113">Example 1: Start a connection monitor</span></span>
```
PS C:\> Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="26625-114">In diesem Beispiel wird ein durch Name und Netzwerküberwachung angegebener Verbindungsmonitor gestartet.</span><span class="sxs-lookup"><span data-stu-id="26625-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="26625-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26625-115">PARAMETERS</span></span>

### <span data-ttu-id="26625-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26625-116">-AsJob</span></span>
<span data-ttu-id="26625-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="26625-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26625-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26625-118">-DefaultProfile</span></span>
<span data-ttu-id="26625-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26625-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26625-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26625-120">-InputObject</span></span>
<span data-ttu-id="26625-121">Verbindungsmonitorobjekt.</span><span class="sxs-lookup"><span data-stu-id="26625-121">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26625-122">-Location</span><span class="sxs-lookup"><span data-stu-id="26625-122">-Location</span></span>
<span data-ttu-id="26625-123">Position der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="26625-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="26625-124">-Name</span><span class="sxs-lookup"><span data-stu-id="26625-124">-Name</span></span>
<span data-ttu-id="26625-125">Der Name des Verbindungsmonitors.</span><span class="sxs-lookup"><span data-stu-id="26625-125">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26625-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="26625-126">-NetworkWatcher</span></span>
<span data-ttu-id="26625-127">Die Netzwerk-Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="26625-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="26625-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="26625-128">-NetworkWatcherName</span></span>
<span data-ttu-id="26625-129">Der Name der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="26625-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="26625-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26625-130">-PassThru</span></span>
<span data-ttu-id="26625-131">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="26625-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="26625-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26625-132">-ResourceGroupName</span></span>
<span data-ttu-id="26625-133">Der Name der Ressourcengruppe "Netzwerk-Watcher".</span><span class="sxs-lookup"><span data-stu-id="26625-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="26625-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26625-134">-ResourceId</span></span>
<span data-ttu-id="26625-135">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="26625-135">Resource ID.</span></span>

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

### <span data-ttu-id="26625-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26625-136">-Confirm</span></span>
<span data-ttu-id="26625-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="26625-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26625-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="26625-138">-WhatIf</span></span>
<span data-ttu-id="26625-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26625-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26625-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26625-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26625-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26625-141">CommonParameters</span></span>
<span data-ttu-id="26625-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26625-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26625-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26625-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26625-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="26625-144">INPUTS</span></span>

### <span data-ttu-id="26625-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="26625-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="26625-146">System.String</span><span class="sxs-lookup"><span data-stu-id="26625-146">System.String</span></span>

### <span data-ttu-id="26625-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="26625-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="26625-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="26625-148">OUTPUTS</span></span>

### <span data-ttu-id="26625-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="26625-149">System.Boolean</span></span>

## <span data-ttu-id="26625-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="26625-150">NOTES</span></span>
<span data-ttu-id="26625-151">Schlüsselwörter: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span><span class="sxs-lookup"><span data-stu-id="26625-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="26625-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="26625-152">RELATED LINKS</span></span>

[<span data-ttu-id="26625-153">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="26625-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="26625-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="26625-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="26625-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="26625-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="26625-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="26625-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="26625-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="26625-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="26625-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="26625-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="26625-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="26625-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="26625-160">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="26625-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="26625-161">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="26625-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="26625-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="26625-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="26625-163">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="26625-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="26625-164">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="26625-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="26625-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="26625-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="26625-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="26625-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="26625-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="26625-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="26625-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="26625-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="26625-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="26625-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="26625-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="26625-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="26625-171">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="26625-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="26625-172">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="26625-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="26625-173">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="26625-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="26625-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="26625-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="26625-175">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="26625-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="26625-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="26625-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="26625-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="26625-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="26625-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="26625-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="26625-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="26625-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
