---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 7e3836f2c546c5ba3ad2ee4a2845e7c813601dda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823843"
---
# <span data-ttu-id="a1ecb-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a1ecb-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="a1ecb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a1ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="a1ecb-103">Aktualisieren eines Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="a1ecb-103">Update a connection monitor.</span></span>

## <span data-ttu-id="a1ecb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1ecb-104">SYNTAX</span></span>

### <span data-ttu-id="a1ecb-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a1ecb-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1ecb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a1ecb-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1ecb-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a1ecb-107">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1ecb-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a1ecb-108">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1ecb-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="a1ecb-109">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1ecb-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1ecb-110">DESCRIPTION</span></span>
<span data-ttu-id="a1ecb-111">Das Set-AzNetworkWatcherConnectionMonitor-Cmdlet aktualisiert den angegebenen Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="a1ecb-111">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="a1ecb-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1ecb-112">EXAMPLES</span></span>

### <span data-ttu-id="a1ecb-113">Beispiel 1: Aktualisieren eines Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="a1ecb-113">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm
-DestinationAddress google.com -DestinationPort 80 -Tag @{"key1" = "value1"}

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"5b2b20e8-0ce0-417e-9607-76208149bb67"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMach
                                ines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="a1ecb-114">In diesem Beispiel wird der vorhandene Verbindungsmonitor aktualisiert, indem destinationAddress geändert und Tags hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a1ecb-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="a1ecb-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1ecb-115">PARAMETERS</span></span>

### <span data-ttu-id="a1ecb-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1ecb-116">-AsJob</span></span>
<span data-ttu-id="a1ecb-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a1ecb-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1ecb-118">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="a1ecb-118">-ConfigureOnly</span></span>
<span data-ttu-id="a1ecb-119">Konfigurieren des Verbindungs Monitors, aber nicht starten</span><span class="sxs-lookup"><span data-stu-id="a1ecb-119">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="a1ecb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1ecb-120">-DefaultProfile</span></span>
<span data-ttu-id="a1ecb-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a1ecb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1ecb-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="a1ecb-122">-DestinationAddress</span></span>
<span data-ttu-id="a1ecb-123">Die IP-Adresse des Verbindungsmonitor Ziels.</span><span class="sxs-lookup"><span data-stu-id="a1ecb-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="a1ecb-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="a1ecb-124">-DestinationPort</span></span>
<span data-ttu-id="a1ecb-125">Ziel-Port.</span><span class="sxs-lookup"><span data-stu-id="a1ecb-125">Destination port.</span></span>

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

### <span data-ttu-id="a1ecb-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="a1ecb-126">-DestinationResourceId</span></span>
<span data-ttu-id="a1ecb-127">Die ID des Verbindungsmonitor Ziels.</span><span class="sxs-lookup"><span data-stu-id="a1ecb-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="a1ecb-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a1ecb-128">-InputObject</span></span>
<span data-ttu-id="a1ecb-129">Connection Monitor-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a1ecb-129">Connection monitor object.</span></span>

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

### <span data-ttu-id="a1ecb-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="a1ecb-130">-Location</span></span>
<span data-ttu-id="a1ecb-131">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="a1ecb-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a1ecb-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a1ecb-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="a1ecb-133">Überwachungsintervall in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="a1ecb-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="a1ecb-134">-Name</span><span class="sxs-lookup"><span data-stu-id="a1ecb-134">-Name</span></span>
<span data-ttu-id="a1ecb-135">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="a1ecb-135">The connection monitor name.</span></span>

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

### <span data-ttu-id="a1ecb-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a1ecb-136">-NetworkWatcher</span></span>
<span data-ttu-id="a1ecb-137">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="a1ecb-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="a1ecb-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a1ecb-138">-NetworkWatcherName</span></span>
<span data-ttu-id="a1ecb-139">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="a1ecb-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="a1ecb-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1ecb-140">-ResourceGroupName</span></span>
<span data-ttu-id="a1ecb-141">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a1ecb-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a1ecb-142">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a1ecb-142">-ResourceId</span></span>
<span data-ttu-id="a1ecb-143">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a1ecb-143">Resource ID.</span></span>

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

### <span data-ttu-id="a1ecb-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="a1ecb-144">-SourcePort</span></span>
<span data-ttu-id="a1ecb-145">Quell-Port.</span><span class="sxs-lookup"><span data-stu-id="a1ecb-145">Source port.</span></span>

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

### <span data-ttu-id="a1ecb-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="a1ecb-146">-SourceResourceId</span></span>
<span data-ttu-id="a1ecb-147">Die ID der Verbindungsmonitor Quelle.</span><span class="sxs-lookup"><span data-stu-id="a1ecb-147">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="a1ecb-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="a1ecb-148">-Tag</span></span>
<span data-ttu-id="a1ecb-149">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="a1ecb-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a1ecb-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a1ecb-150">-Confirm</span></span>
<span data-ttu-id="a1ecb-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a1ecb-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1ecb-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1ecb-152">-WhatIf</span></span>
<span data-ttu-id="a1ecb-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1ecb-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1ecb-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1ecb-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1ecb-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1ecb-155">CommonParameters</span></span>
<span data-ttu-id="a1ecb-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1ecb-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1ecb-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1ecb-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1ecb-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a1ecb-158">INPUTS</span></span>

### <span data-ttu-id="a1ecb-159">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a1ecb-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="a1ecb-160">System. String</span><span class="sxs-lookup"><span data-stu-id="a1ecb-160">System.String</span></span>

### <span data-ttu-id="a1ecb-161">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="a1ecb-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="a1ecb-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a1ecb-162">OUTPUTS</span></span>

### <span data-ttu-id="a1ecb-163">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="a1ecb-163">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="a1ecb-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="a1ecb-164">NOTES</span></span>
<span data-ttu-id="a1ecb-165">Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor, Verbindungsmonitor</span><span class="sxs-lookup"><span data-stu-id="a1ecb-165">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="a1ecb-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a1ecb-166">RELATED LINKS</span></span>

[<span data-ttu-id="a1ecb-167">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a1ecb-167">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a1ecb-168">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a1ecb-168">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a1ecb-169">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a1ecb-169">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a1ecb-170">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a1ecb-170">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a1ecb-171">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a1ecb-171">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a1ecb-172">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a1ecb-172">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a1ecb-173">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a1ecb-173">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a1ecb-174">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a1ecb-174">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a1ecb-175">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a1ecb-175">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a1ecb-176">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a1ecb-176">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a1ecb-177">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a1ecb-177">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a1ecb-178">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a1ecb-178">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a1ecb-179">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a1ecb-179">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a1ecb-180">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a1ecb-180">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="a1ecb-181">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a1ecb-181">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a1ecb-182">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a1ecb-182">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a1ecb-183">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a1ecb-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a1ecb-184">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a1ecb-184">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a1ecb-185">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1ecb-185">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a1ecb-186">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a1ecb-186">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a1ecb-187">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a1ecb-187">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a1ecb-188">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a1ecb-188">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a1ecb-189">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a1ecb-189">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a1ecb-190">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a1ecb-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a1ecb-191">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a1ecb-191">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a1ecb-192">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a1ecb-192">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a1ecb-193">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a1ecb-193">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
