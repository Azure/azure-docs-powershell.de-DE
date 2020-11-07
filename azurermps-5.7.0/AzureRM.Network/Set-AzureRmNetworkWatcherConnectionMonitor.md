---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 44f81008b0693a4ff14a80a818e9d2514dfe0ebf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664372"
---
# <span data-ttu-id="331d5-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="331d5-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="331d5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="331d5-102">SYNOPSIS</span></span>
<span data-ttu-id="331d5-103">Aktualisieren eines Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="331d5-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="331d5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="331d5-104">SYNTAX</span></span>

### <span data-ttu-id="331d5-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="331d5-105">SetByName (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="331d5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="331d5-106">SetByResource</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="331d5-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="331d5-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="331d5-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="331d5-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="331d5-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="331d5-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="331d5-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="331d5-110">DESCRIPTION</span></span>
<span data-ttu-id="331d5-111">Das Set-AzureRmNetworkWatcherConnectionMonitor-Cmdlet aktualisiert den angegebenen Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="331d5-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="331d5-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="331d5-112">EXAMPLES</span></span>

### <span data-ttu-id="331d5-113">Beispiel 1: Aktualisieren eines Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="331d5-113">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="331d5-114">In diesem Beispiel wird der vorhandene Verbindungsmonitor aktualisiert, indem destinationAddress geändert und Tags hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="331d5-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="331d5-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="331d5-115">PARAMETERS</span></span>

### <span data-ttu-id="331d5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="331d5-116">-AsJob</span></span>
<span data-ttu-id="331d5-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="331d5-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331d5-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="331d5-118">-Confirm</span></span>
<span data-ttu-id="331d5-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="331d5-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331d5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="331d5-120">-DefaultProfile</span></span>
<span data-ttu-id="331d5-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="331d5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331d5-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="331d5-122">-DestinationAddress</span></span>
<span data-ttu-id="331d5-123">Die IP-Adresse des Verbindungsmonitor Ziels.</span><span class="sxs-lookup"><span data-stu-id="331d5-123">The Ip address of the connection monitor destination.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331d5-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="331d5-124">-DestinationPort</span></span>
<span data-ttu-id="331d5-125">Ziel-Port.</span><span class="sxs-lookup"><span data-stu-id="331d5-125">Destination port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331d5-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="331d5-126">-DestinationResourceId</span></span>
<span data-ttu-id="331d5-127">Die ID des Verbindungsmonitor Ziels.</span><span class="sxs-lookup"><span data-stu-id="331d5-127">The ID of the connection monitor destination.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331d5-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="331d5-128">-InputObject</span></span>
<span data-ttu-id="331d5-129">Connection Monitor-Objekt.</span><span class="sxs-lookup"><span data-stu-id="331d5-129">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="331d5-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="331d5-130">-Location</span></span>
<span data-ttu-id="331d5-131">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="331d5-131">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331d5-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="331d5-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="331d5-133">Überwachungsintervall in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="331d5-133">Monitoring interval in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331d5-134">-Name</span><span class="sxs-lookup"><span data-stu-id="331d5-134">-Name</span></span>
<span data-ttu-id="331d5-135">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="331d5-135">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331d5-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="331d5-136">-NetworkWatcher</span></span>
<span data-ttu-id="331d5-137">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="331d5-137">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="331d5-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="331d5-138">-NetworkWatcherName</span></span>
<span data-ttu-id="331d5-139">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="331d5-139">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331d5-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="331d5-140">-ResourceGroupName</span></span>
<span data-ttu-id="331d5-141">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="331d5-141">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331d5-142">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="331d5-142">-ResourceId</span></span>
<span data-ttu-id="331d5-143">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="331d5-143">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="331d5-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="331d5-144">-SourcePort</span></span>
<span data-ttu-id="331d5-145">Quell-Port.</span><span class="sxs-lookup"><span data-stu-id="331d5-145">Source port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331d5-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="331d5-146">-SourceResourceId</span></span>
<span data-ttu-id="331d5-147">Die ID der Verbindungsmonitor Quelle.</span><span class="sxs-lookup"><span data-stu-id="331d5-147">The ID of the connection monitor source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="331d5-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="331d5-148">-Tag</span></span>
<span data-ttu-id="331d5-149">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="331d5-149">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331d5-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="331d5-150">-WhatIf</span></span>
<span data-ttu-id="331d5-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="331d5-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="331d5-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="331d5-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331d5-153">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="331d5-153">-ConfigureOnly</span></span>
<span data-ttu-id="331d5-154">Konfigurieren des Verbindungs Monitors, aber nicht starten</span><span class="sxs-lookup"><span data-stu-id="331d5-154">Configure connection monitor, but do not start it</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331d5-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="331d5-155">CommonParameters</span></span>
<span data-ttu-id="331d5-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="331d5-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="331d5-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="331d5-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="331d5-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="331d5-158">INPUTS</span></span>

### <span data-ttu-id="331d5-159">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="331d5-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="331d5-160">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="331d5-160">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="331d5-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="331d5-161">OUTPUTS</span></span>

### <span data-ttu-id="331d5-162">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="331d5-162">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="331d5-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="331d5-163">NOTES</span></span>
<span data-ttu-id="331d5-164">Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor, Verbindungsmonitor</span><span class="sxs-lookup"><span data-stu-id="331d5-164">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="331d5-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="331d5-165">RELATED LINKS</span></span>

[<span data-ttu-id="331d5-166">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="331d5-166">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="331d5-167">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="331d5-167">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="331d5-168">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="331d5-168">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="331d5-169">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="331d5-169">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="331d5-170">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="331d5-170">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="331d5-171">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="331d5-171">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="331d5-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="331d5-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="331d5-173">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="331d5-173">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="331d5-174">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="331d5-174">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="331d5-175">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="331d5-175">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="331d5-176">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="331d5-176">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="331d5-177">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="331d5-177">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="331d5-178">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="331d5-178">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="331d5-179">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="331d5-179">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="331d5-180">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="331d5-180">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="331d5-181">Anfang-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="331d5-181">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="331d5-182">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="331d5-182">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="331d5-183">Neu – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="331d5-183">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
