---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: b8dd04fa4727465ee9b3be3eaf5e5e06a2243338
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664641"
---
# <span data-ttu-id="a286f-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a286f-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="a286f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a286f-102">SYNOPSIS</span></span>
<span data-ttu-id="a286f-103">Erstellt einen Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="a286f-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a286f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a286f-104">SYNTAX</span></span>

### <span data-ttu-id="a286f-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a286f-105">SetByName (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a286f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a286f-106">SetByResource</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a286f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a286f-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a286f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a286f-108">DESCRIPTION</span></span>
<span data-ttu-id="a286f-109">Das New-AzureRmNetworkWatcherConnectionMonitor-Cmdlet rcreates einen Verbindungsmonitor für eine angegebene Quelle und ein angegebenes Ziel.</span><span class="sxs-lookup"><span data-stu-id="a286f-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="a286f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a286f-110">EXAMPLES</span></span>

### <span data-ttu-id="a286f-111">Beispiel 1: Erstellen eines Verbindungs Monitors für ein VM-und Internet Ziel</span><span class="sxs-lookup"><span data-stu-id="a286f-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
```
PS C:\> New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

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

<span data-ttu-id="a286f-112">Das New-AzureRmNetworkWatcherConnectionMonitor-Cmdlet erstellt einen Verbindungsmonitor für eine angegebene Quelle und ein angegebenes Ziel.</span><span class="sxs-lookup"><span data-stu-id="a286f-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="a286f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a286f-113">PARAMETERS</span></span>

### <span data-ttu-id="a286f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a286f-114">-AsJob</span></span>
<span data-ttu-id="a286f-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a286f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a286f-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a286f-116">-Confirm</span></span>
<span data-ttu-id="a286f-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a286f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a286f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a286f-118">-DefaultProfile</span></span>
<span data-ttu-id="a286f-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a286f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a286f-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="a286f-120">-DestinationAddress</span></span>
<span data-ttu-id="a286f-121">Die IP-Adresse des Verbindungsmonitor Ziels.</span><span class="sxs-lookup"><span data-stu-id="a286f-121">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="a286f-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="a286f-122">-DestinationPort</span></span>
<span data-ttu-id="a286f-123">Ziel-Port.</span><span class="sxs-lookup"><span data-stu-id="a286f-123">Destination port.</span></span>

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

### <span data-ttu-id="a286f-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="a286f-124">-DestinationResourceId</span></span>
<span data-ttu-id="a286f-125">Die ID des Verbindungsmonitor Ziels.</span><span class="sxs-lookup"><span data-stu-id="a286f-125">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="a286f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="a286f-126">-Force</span></span>
<span data-ttu-id="a286f-127">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="a286f-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a286f-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="a286f-128">-Location</span></span>
<span data-ttu-id="a286f-129">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="a286f-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a286f-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a286f-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="a286f-131">Überwachungsintervall in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="a286f-131">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="a286f-132">-Name</span><span class="sxs-lookup"><span data-stu-id="a286f-132">-Name</span></span>
<span data-ttu-id="a286f-133">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="a286f-133">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a286f-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a286f-134">-NetworkWatcher</span></span>
<span data-ttu-id="a286f-135">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="a286f-135">The network watcher resource.</span></span>

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

### <span data-ttu-id="a286f-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a286f-136">-NetworkWatcherName</span></span>
<span data-ttu-id="a286f-137">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="a286f-137">The name of network watcher.</span></span>

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

### <span data-ttu-id="a286f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a286f-138">-ResourceGroupName</span></span>
<span data-ttu-id="a286f-139">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a286f-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a286f-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="a286f-140">-SourcePort</span></span>
<span data-ttu-id="a286f-141">Quell-Port.</span><span class="sxs-lookup"><span data-stu-id="a286f-141">Source port.</span></span>

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

### <span data-ttu-id="a286f-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="a286f-142">-SourceResourceId</span></span>
<span data-ttu-id="a286f-143">Die ID der Verbindungsmonitor Quelle.</span><span class="sxs-lookup"><span data-stu-id="a286f-143">The ID of the connection monitor source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a286f-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="a286f-144">-Tag</span></span>
<span data-ttu-id="a286f-145">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="a286f-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a286f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a286f-146">-WhatIf</span></span>
<span data-ttu-id="a286f-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a286f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a286f-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a286f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a286f-149">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="a286f-149">-ConfigureOnly</span></span>
<span data-ttu-id="a286f-150">Konfigurieren des Verbindungs Monitors, aber nicht starten</span><span class="sxs-lookup"><span data-stu-id="a286f-150">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="a286f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a286f-151">CommonParameters</span></span>
<span data-ttu-id="a286f-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a286f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a286f-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a286f-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a286f-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a286f-154">INPUTS</span></span>

### <span data-ttu-id="a286f-155">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a286f-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a286f-156">System. String</span><span class="sxs-lookup"><span data-stu-id="a286f-156">System.String</span></span>

## <span data-ttu-id="a286f-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a286f-157">OUTPUTS</span></span>

### <span data-ttu-id="a286f-158">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="a286f-158">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="a286f-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="a286f-159">NOTES</span></span>
<span data-ttu-id="a286f-160">Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor, Verbindungsmonitor</span><span class="sxs-lookup"><span data-stu-id="a286f-160">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="a286f-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a286f-161">RELATED LINKS</span></span>

[<span data-ttu-id="a286f-162">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a286f-162">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="a286f-163">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a286f-163">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="a286f-164">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a286f-164">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="a286f-165">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a286f-165">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="a286f-166">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a286f-166">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="a286f-167">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a286f-167">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="a286f-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a286f-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="a286f-169">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a286f-169">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="a286f-170">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a286f-170">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="a286f-171">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a286f-171">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="a286f-172">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a286f-172">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="a286f-173">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a286f-173">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="a286f-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a286f-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="a286f-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a286f-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="a286f-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a286f-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="a286f-177">Satz-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a286f-177">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="a286f-178">Anfang-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a286f-178">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="a286f-179">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a286f-179">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
