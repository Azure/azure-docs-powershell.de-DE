---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: ec7f6f910a50f479a923451fb9b893a5cabb5301
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821528"
---
# <span data-ttu-id="a29e9-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a29e9-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="a29e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a29e9-102">SYNOPSIS</span></span>
<span data-ttu-id="a29e9-103">Erstellt einen Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="a29e9-103">Creates a connection monitor.</span></span>

## <span data-ttu-id="a29e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a29e9-104">SYNTAX</span></span>

### <span data-ttu-id="a29e9-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a29e9-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a29e9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a29e9-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a29e9-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a29e9-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a29e9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a29e9-108">DESCRIPTION</span></span>
<span data-ttu-id="a29e9-109">Das New-AzNetworkWatcherConnectionMonitor-Cmdlet erstellt einen Verbindungsmonitor für eine angegebene Quelle und ein angegebenes Ziel.</span><span class="sxs-lookup"><span data-stu-id="a29e9-109">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="a29e9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a29e9-110">EXAMPLES</span></span>

### <span data-ttu-id="a29e9-111">Beispiel 1: Erstellen eines Verbindungs Monitors für ein VM-und Internet Ziel</span><span class="sxs-lookup"><span data-stu-id="a29e9-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
```
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/t1
Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft
                                .Compute/virtualMachines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "bing.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:13:11 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {}
```

<span data-ttu-id="a29e9-112">Das New-AzNetworkWatcherConnectionMonitor-Cmdlet erstellt einen Verbindungsmonitor für eine angegebene Quelle und ein angegebenes Ziel.</span><span class="sxs-lookup"><span data-stu-id="a29e9-112">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="a29e9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a29e9-113">PARAMETERS</span></span>

### <span data-ttu-id="a29e9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a29e9-114">-AsJob</span></span>
<span data-ttu-id="a29e9-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a29e9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a29e9-116">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="a29e9-116">-ConfigureOnly</span></span>
<span data-ttu-id="a29e9-117">Konfigurieren des Verbindungs Monitors, aber nicht starten</span><span class="sxs-lookup"><span data-stu-id="a29e9-117">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="a29e9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a29e9-118">-DefaultProfile</span></span>
<span data-ttu-id="a29e9-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a29e9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a29e9-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="a29e9-120">-DestinationAddress</span></span>
<span data-ttu-id="a29e9-121">Die IP-Adresse des Verbindungsmonitor Ziels.</span><span class="sxs-lookup"><span data-stu-id="a29e9-121">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="a29e9-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="a29e9-122">-DestinationPort</span></span>
<span data-ttu-id="a29e9-123">Ziel-Port.</span><span class="sxs-lookup"><span data-stu-id="a29e9-123">Destination port.</span></span>

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

### <span data-ttu-id="a29e9-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="a29e9-124">-DestinationResourceId</span></span>
<span data-ttu-id="a29e9-125">Die ID des Verbindungsmonitor Ziels.</span><span class="sxs-lookup"><span data-stu-id="a29e9-125">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="a29e9-126">-Force</span><span class="sxs-lookup"><span data-stu-id="a29e9-126">-Force</span></span>
<span data-ttu-id="a29e9-127">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="a29e9-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a29e9-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="a29e9-128">-Location</span></span>
<span data-ttu-id="a29e9-129">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="a29e9-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a29e9-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a29e9-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="a29e9-131">Überwachungsintervall in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="a29e9-131">Monitoring interval in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a29e9-132">-Name</span><span class="sxs-lookup"><span data-stu-id="a29e9-132">-Name</span></span>
<span data-ttu-id="a29e9-133">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="a29e9-133">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a29e9-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a29e9-134">-NetworkWatcher</span></span>
<span data-ttu-id="a29e9-135">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="a29e9-135">The network watcher resource.</span></span>

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

### <span data-ttu-id="a29e9-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a29e9-136">-NetworkWatcherName</span></span>
<span data-ttu-id="a29e9-137">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="a29e9-137">The name of network watcher.</span></span>

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

### <span data-ttu-id="a29e9-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a29e9-138">-ResourceGroupName</span></span>
<span data-ttu-id="a29e9-139">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a29e9-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a29e9-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="a29e9-140">-SourcePort</span></span>
<span data-ttu-id="a29e9-141">Quell-Port.</span><span class="sxs-lookup"><span data-stu-id="a29e9-141">Source port.</span></span>

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

### <span data-ttu-id="a29e9-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="a29e9-142">-SourceResourceId</span></span>
<span data-ttu-id="a29e9-143">Die ID der Verbindungsmonitor Quelle.</span><span class="sxs-lookup"><span data-stu-id="a29e9-143">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="a29e9-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="a29e9-144">-Tag</span></span>
<span data-ttu-id="a29e9-145">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="a29e9-145">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a29e9-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a29e9-146">-Confirm</span></span>
<span data-ttu-id="a29e9-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a29e9-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a29e9-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a29e9-148">-WhatIf</span></span>
<span data-ttu-id="a29e9-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a29e9-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a29e9-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a29e9-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a29e9-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a29e9-151">CommonParameters</span></span>
<span data-ttu-id="a29e9-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a29e9-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a29e9-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a29e9-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a29e9-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a29e9-154">INPUTS</span></span>

### <span data-ttu-id="a29e9-155">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a29e9-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="a29e9-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a29e9-156">OUTPUTS</span></span>

### <span data-ttu-id="a29e9-157">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="a29e9-157">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="a29e9-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="a29e9-158">NOTES</span></span>
<span data-ttu-id="a29e9-159">Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor, Verbindungsmonitor</span><span class="sxs-lookup"><span data-stu-id="a29e9-159">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="a29e9-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a29e9-160">RELATED LINKS</span></span>

[<span data-ttu-id="a29e9-161">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a29e9-161">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a29e9-162">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a29e9-162">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a29e9-163">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a29e9-163">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a29e9-164">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a29e9-164">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a29e9-165">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a29e9-165">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a29e9-166">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a29e9-166">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a29e9-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a29e9-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a29e9-168">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a29e9-168">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a29e9-169">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a29e9-169">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a29e9-170">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a29e9-170">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a29e9-171">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a29e9-171">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a29e9-172">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a29e9-172">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a29e9-173">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a29e9-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a29e9-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a29e9-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="a29e9-175">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a29e9-175">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a29e9-176">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a29e9-176">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a29e9-177">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a29e9-177">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a29e9-178">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a29e9-178">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a29e9-179">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a29e9-179">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a29e9-180">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a29e9-180">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a29e9-181">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a29e9-181">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a29e9-182">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a29e9-182">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a29e9-183">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a29e9-183">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a29e9-184">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a29e9-184">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a29e9-185">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a29e9-185">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a29e9-186">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a29e9-186">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a29e9-187">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a29e9-187">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
