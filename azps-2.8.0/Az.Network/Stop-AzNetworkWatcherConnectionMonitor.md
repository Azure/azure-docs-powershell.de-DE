---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: ceb03c58c7f7c3983f89073b5bad2428a32b7934
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823739"
---
# <span data-ttu-id="74fac-101">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="74fac-101">Stop-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="74fac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="74fac-102">SYNOPSIS</span></span>
<span data-ttu-id="74fac-103">Beenden eines Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="74fac-103">Stop a connection monitor</span></span>

## <span data-ttu-id="74fac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="74fac-104">SYNTAX</span></span>

### <span data-ttu-id="74fac-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="74fac-105">SetByName (Default)</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74fac-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="74fac-106">SetByResource</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74fac-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="74fac-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74fac-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="74fac-108">SetByResourceId</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74fac-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="74fac-109">SetByInputObject</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74fac-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74fac-110">DESCRIPTION</span></span>
<span data-ttu-id="74fac-111">Das Stop-AzNetworkWatcherConnectionMonitor-Cmdlet beendet den angegebenen Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="74fac-111">The Stop-AzNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="74fac-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="74fac-112">EXAMPLES</span></span>

### <span data-ttu-id="74fac-113">Beispiel 1: Beenden eines Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="74fac-113">Example 1: Stop a connection monitor</span></span>
```
PS C:\> Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="74fac-114">In diesem Beispiel wird der vom Namen und Netzwerkmonitor angegebene Verbindungsmonitor beendet</span><span class="sxs-lookup"><span data-stu-id="74fac-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="74fac-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="74fac-115">PARAMETERS</span></span>

### <span data-ttu-id="74fac-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74fac-116">-AsJob</span></span>
<span data-ttu-id="74fac-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="74fac-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74fac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74fac-118">-DefaultProfile</span></span>
<span data-ttu-id="74fac-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="74fac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74fac-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="74fac-120">-InputObject</span></span>
<span data-ttu-id="74fac-121">Connection Monitor-Objekt.</span><span class="sxs-lookup"><span data-stu-id="74fac-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="74fac-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="74fac-122">-Location</span></span>
<span data-ttu-id="74fac-123">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="74fac-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="74fac-124">-Name</span><span class="sxs-lookup"><span data-stu-id="74fac-124">-Name</span></span>
<span data-ttu-id="74fac-125">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="74fac-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="74fac-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="74fac-126">-NetworkWatcher</span></span>
<span data-ttu-id="74fac-127">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="74fac-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="74fac-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="74fac-128">-NetworkWatcherName</span></span>
<span data-ttu-id="74fac-129">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="74fac-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="74fac-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74fac-130">-PassThru</span></span>
<span data-ttu-id="74fac-131">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="74fac-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="74fac-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74fac-132">-ResourceGroupName</span></span>
<span data-ttu-id="74fac-133">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="74fac-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="74fac-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="74fac-134">-ResourceId</span></span>
<span data-ttu-id="74fac-135">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="74fac-135">Resource ID.</span></span>

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

### <span data-ttu-id="74fac-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="74fac-136">-Confirm</span></span>
<span data-ttu-id="74fac-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="74fac-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74fac-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74fac-138">-WhatIf</span></span>
<span data-ttu-id="74fac-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74fac-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74fac-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74fac-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74fac-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74fac-141">CommonParameters</span></span>
<span data-ttu-id="74fac-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74fac-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74fac-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74fac-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74fac-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="74fac-144">INPUTS</span></span>

### <span data-ttu-id="74fac-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="74fac-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="74fac-146">System. String</span><span class="sxs-lookup"><span data-stu-id="74fac-146">System.String</span></span>

### <span data-ttu-id="74fac-147">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="74fac-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="74fac-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="74fac-148">OUTPUTS</span></span>

### <span data-ttu-id="74fac-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="74fac-149">System.Boolean</span></span>

## <span data-ttu-id="74fac-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="74fac-150">NOTES</span></span>
<span data-ttu-id="74fac-151">Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor, Verbindungsmonitor</span><span class="sxs-lookup"><span data-stu-id="74fac-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="74fac-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="74fac-152">RELATED LINKS</span></span>

[<span data-ttu-id="74fac-153">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="74fac-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="74fac-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="74fac-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="74fac-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="74fac-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="74fac-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="74fac-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="74fac-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="74fac-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="74fac-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="74fac-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="74fac-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="74fac-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="74fac-160">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="74fac-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="74fac-161">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="74fac-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="74fac-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="74fac-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="74fac-163">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="74fac-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="74fac-164">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="74fac-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="74fac-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="74fac-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="74fac-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="74fac-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="74fac-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="74fac-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="74fac-168">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="74fac-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="74fac-169">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="74fac-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="74fac-170">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="74fac-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="74fac-171">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="74fac-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="74fac-172">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="74fac-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="74fac-173">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="74fac-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="74fac-174">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="74fac-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="74fac-175">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="74fac-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="74fac-176">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="74fac-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="74fac-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="74fac-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="74fac-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="74fac-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="74fac-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="74fac-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
