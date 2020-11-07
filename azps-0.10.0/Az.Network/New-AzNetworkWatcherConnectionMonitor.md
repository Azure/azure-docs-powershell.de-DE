---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: bfdcfbf57f44479ad35a2b9075590a0d40351ec9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841295"
---
# <span data-ttu-id="74fd6-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="74fd6-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="74fd6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="74fd6-102">SYNOPSIS</span></span>
<span data-ttu-id="74fd6-103">Erstellt einen Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="74fd6-103">Creates a connection monitor.</span></span>

## <span data-ttu-id="74fd6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="74fd6-104">SYNTAX</span></span>

### <span data-ttu-id="74fd6-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="74fd6-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="74fd6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="74fd6-106">SetByName</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="74fd6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="74fd6-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="74fd6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74fd6-108">DESCRIPTION</span></span>
<span data-ttu-id="74fd6-109">Das New-AzNetworkWatcherConnectionMonitor-Cmdlet rcreates einen Verbindungsmonitor für eine angegebene Quelle und ein angegebenes Ziel.</span><span class="sxs-lookup"><span data-stu-id="74fd6-109">The New-AzNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="74fd6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="74fd6-110">EXAMPLES</span></span>

### <span data-ttu-id="74fd6-111">---------------Beispiel 1: Erstellen eines Verbindungs Monitors für ein VM-und Internet Ziel---------------</span><span class="sxs-lookup"><span data-stu-id="74fd6-111">---------------  Example 1: Create a connection monitor for a vm and internet destination ---------------</span></span>
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

<span data-ttu-id="74fd6-112">Das New-AzNetworkWatcherConnectionMonitor-Cmdlet erstellt einen Verbindungsmonitor für eine angegebene Quelle und ein angegebenes Ziel.</span><span class="sxs-lookup"><span data-stu-id="74fd6-112">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="74fd6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="74fd6-113">PARAMETERS</span></span>

### <span data-ttu-id="74fd6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74fd6-114">-AsJob</span></span>
<span data-ttu-id="74fd6-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="74fd6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74fd6-116">– Autostart</span><span class="sxs-lookup"><span data-stu-id="74fd6-116">-AutoStart</span></span>
<span data-ttu-id="74fd6-117">Automatischer Start.</span><span class="sxs-lookup"><span data-stu-id="74fd6-117">Auto start.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74fd6-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="74fd6-118">-Confirm</span></span>
<span data-ttu-id="74fd6-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="74fd6-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74fd6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74fd6-120">-DefaultProfile</span></span>
<span data-ttu-id="74fd6-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="74fd6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74fd6-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="74fd6-122">-DestinationAddress</span></span>
<span data-ttu-id="74fd6-123">Die IP-Adresse des Verbindungsmonitor Ziels.</span><span class="sxs-lookup"><span data-stu-id="74fd6-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="74fd6-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="74fd6-124">-DestinationPort</span></span>
<span data-ttu-id="74fd6-125">Ziel-Port.</span><span class="sxs-lookup"><span data-stu-id="74fd6-125">Destination port.</span></span>

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

### <span data-ttu-id="74fd6-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="74fd6-126">-DestinationResourceId</span></span>
<span data-ttu-id="74fd6-127">Die ID des Verbindungsmonitor Ziels.</span><span class="sxs-lookup"><span data-stu-id="74fd6-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="74fd6-128">-Force</span><span class="sxs-lookup"><span data-stu-id="74fd6-128">-Force</span></span>
<span data-ttu-id="74fd6-129">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="74fd6-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="74fd6-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="74fd6-130">-Location</span></span>
<span data-ttu-id="74fd6-131">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="74fd6-131">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74fd6-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="74fd6-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="74fd6-133">Überwachungsintervall in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="74fd6-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="74fd6-134">-Name</span><span class="sxs-lookup"><span data-stu-id="74fd6-134">-Name</span></span>
<span data-ttu-id="74fd6-135">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="74fd6-135">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74fd6-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="74fd6-136">-NetworkWatcher</span></span>
<span data-ttu-id="74fd6-137">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="74fd6-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="74fd6-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="74fd6-138">-NetworkWatcherName</span></span>
<span data-ttu-id="74fd6-139">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="74fd6-139">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74fd6-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74fd6-140">-ResourceGroupName</span></span>
<span data-ttu-id="74fd6-141">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="74fd6-141">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74fd6-142">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="74fd6-142">-SourcePort</span></span>
<span data-ttu-id="74fd6-143">Quell-Port.</span><span class="sxs-lookup"><span data-stu-id="74fd6-143">Source port.</span></span>

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

### <span data-ttu-id="74fd6-144">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="74fd6-144">-SourceResourceId</span></span>
<span data-ttu-id="74fd6-145">Die ID der Verbindungsmonitor Quelle.</span><span class="sxs-lookup"><span data-stu-id="74fd6-145">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="74fd6-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="74fd6-146">-Tag</span></span>
<span data-ttu-id="74fd6-147">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="74fd6-147">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="74fd6-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74fd6-148">-WhatIf</span></span>
<span data-ttu-id="74fd6-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74fd6-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74fd6-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74fd6-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="74fd6-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="74fd6-151">INPUTS</span></span>

### <span data-ttu-id="74fd6-152">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="74fd6-152">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="74fd6-153">System. String</span><span class="sxs-lookup"><span data-stu-id="74fd6-153">System.String</span></span>


## <span data-ttu-id="74fd6-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="74fd6-154">OUTPUTS</span></span>

### <span data-ttu-id="74fd6-155">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="74fd6-155">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="74fd6-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="74fd6-156">NOTES</span></span>
<span data-ttu-id="74fd6-157">Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor, Verbindungsmonitor</span><span class="sxs-lookup"><span data-stu-id="74fd6-157">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="74fd6-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="74fd6-158">RELATED LINKS</span></span>
<span data-ttu-id="74fd6-159">[Neu – AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="74fd6-159">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="74fd6-160">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="74fd6-160">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="74fd6-161">[Neu – AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Neu – AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stopp-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="74fd6-161">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="74fd6-162">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="74fd6-162">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)</span></span>
