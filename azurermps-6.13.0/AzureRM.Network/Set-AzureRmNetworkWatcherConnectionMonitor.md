---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5c7709c234ba762e5b87418cc0e9b3fc4637ac11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663129"
---
# <span data-ttu-id="809fd-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="809fd-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="809fd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="809fd-102">SYNOPSIS</span></span>
<span data-ttu-id="809fd-103">Aktualisieren eines Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="809fd-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="809fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="809fd-104">SYNTAX</span></span>

### <span data-ttu-id="809fd-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="809fd-105">SetByName (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="809fd-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="809fd-106">SetByResource</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="809fd-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="809fd-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="809fd-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="809fd-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="809fd-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="809fd-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="809fd-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809fd-110">DESCRIPTION</span></span>
<span data-ttu-id="809fd-111">Das Set-AzureRmNetworkWatcherConnectionMonitor-Cmdlet aktualisiert den angegebenen Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="809fd-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="809fd-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="809fd-112">EXAMPLES</span></span>

### <span data-ttu-id="809fd-113">Beispiel 1: Aktualisieren eines Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="809fd-113">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm 
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

<span data-ttu-id="809fd-114">In diesem Beispiel wird der vorhandene Verbindungsmonitor aktualisiert, indem destinationAddress geändert und Tags hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="809fd-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="809fd-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="809fd-115">PARAMETERS</span></span>

### <span data-ttu-id="809fd-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="809fd-116">-AsJob</span></span>
<span data-ttu-id="809fd-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="809fd-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="809fd-118">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="809fd-118">-ConfigureOnly</span></span>
<span data-ttu-id="809fd-119">Konfigurieren des Verbindungs Monitors, aber nicht starten</span><span class="sxs-lookup"><span data-stu-id="809fd-119">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="809fd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="809fd-120">-DefaultProfile</span></span>
<span data-ttu-id="809fd-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="809fd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="809fd-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="809fd-122">-DestinationAddress</span></span>
<span data-ttu-id="809fd-123">Die IP-Adresse des Verbindungsmonitor Ziels.</span><span class="sxs-lookup"><span data-stu-id="809fd-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="809fd-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="809fd-124">-DestinationPort</span></span>
<span data-ttu-id="809fd-125">Ziel-Port.</span><span class="sxs-lookup"><span data-stu-id="809fd-125">Destination port.</span></span>

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

### <span data-ttu-id="809fd-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="809fd-126">-DestinationResourceId</span></span>
<span data-ttu-id="809fd-127">Die ID des Verbindungsmonitor Ziels.</span><span class="sxs-lookup"><span data-stu-id="809fd-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="809fd-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="809fd-128">-InputObject</span></span>
<span data-ttu-id="809fd-129">Connection Monitor-Objekt.</span><span class="sxs-lookup"><span data-stu-id="809fd-129">Connection monitor object.</span></span>

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

### <span data-ttu-id="809fd-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="809fd-130">-Location</span></span>
<span data-ttu-id="809fd-131">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="809fd-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="809fd-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="809fd-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="809fd-133">Überwachungsintervall in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="809fd-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="809fd-134">-Name</span><span class="sxs-lookup"><span data-stu-id="809fd-134">-Name</span></span>
<span data-ttu-id="809fd-135">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="809fd-135">The connection monitor name.</span></span>

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

### <span data-ttu-id="809fd-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="809fd-136">-NetworkWatcher</span></span>
<span data-ttu-id="809fd-137">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="809fd-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="809fd-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="809fd-138">-NetworkWatcherName</span></span>
<span data-ttu-id="809fd-139">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="809fd-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="809fd-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="809fd-140">-ResourceGroupName</span></span>
<span data-ttu-id="809fd-141">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="809fd-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="809fd-142">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="809fd-142">-ResourceId</span></span>
<span data-ttu-id="809fd-143">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="809fd-143">Resource ID.</span></span>

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

### <span data-ttu-id="809fd-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="809fd-144">-SourcePort</span></span>
<span data-ttu-id="809fd-145">Quell-Port.</span><span class="sxs-lookup"><span data-stu-id="809fd-145">Source port.</span></span>

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

### <span data-ttu-id="809fd-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="809fd-146">-SourceResourceId</span></span>
<span data-ttu-id="809fd-147">Die ID der Verbindungsmonitor Quelle.</span><span class="sxs-lookup"><span data-stu-id="809fd-147">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="809fd-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="809fd-148">-Tag</span></span>
<span data-ttu-id="809fd-149">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="809fd-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="809fd-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="809fd-150">-Confirm</span></span>
<span data-ttu-id="809fd-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="809fd-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="809fd-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="809fd-152">-WhatIf</span></span>
<span data-ttu-id="809fd-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="809fd-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="809fd-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="809fd-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="809fd-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="809fd-155">CommonParameters</span></span>
<span data-ttu-id="809fd-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="809fd-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="809fd-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="809fd-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="809fd-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="809fd-158">INPUTS</span></span>

### <span data-ttu-id="809fd-159">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="809fd-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="809fd-160">Parameter: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="809fd-160">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="809fd-161">System. String</span><span class="sxs-lookup"><span data-stu-id="809fd-161">System.String</span></span>

### <span data-ttu-id="809fd-162">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="809fd-162">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="809fd-163">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="809fd-163">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="809fd-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="809fd-164">OUTPUTS</span></span>

### <span data-ttu-id="809fd-165">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="809fd-165">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="809fd-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="809fd-166">NOTES</span></span>
<span data-ttu-id="809fd-167">Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor, Verbindungsmonitor</span><span class="sxs-lookup"><span data-stu-id="809fd-167">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="809fd-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="809fd-168">RELATED LINKS</span></span>

[<span data-ttu-id="809fd-169">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="809fd-169">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="809fd-170">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="809fd-170">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="809fd-171">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="809fd-171">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="809fd-172">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="809fd-172">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="809fd-173">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="809fd-173">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="809fd-174">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="809fd-174">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="809fd-175">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="809fd-175">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="809fd-176">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="809fd-176">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="809fd-177">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="809fd-177">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="809fd-178">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="809fd-178">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="809fd-179">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="809fd-179">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="809fd-180">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="809fd-180">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="809fd-181">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="809fd-181">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="809fd-182">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="809fd-182">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="809fd-183">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="809fd-183">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="809fd-184">Satz-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="809fd-184">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="809fd-185">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="809fd-185">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="809fd-186">Neu – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="809fd-186">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="809fd-187">Neu – AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="809fd-187">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="809fd-188">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="809fd-188">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="809fd-189">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="809fd-189">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="809fd-190">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="809fd-190">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="809fd-191">Anfang-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="809fd-191">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="809fd-192">Satz-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="809fd-192">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="809fd-193">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="809fd-193">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="809fd-194">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="809fd-194">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="809fd-195">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="809fd-195">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
