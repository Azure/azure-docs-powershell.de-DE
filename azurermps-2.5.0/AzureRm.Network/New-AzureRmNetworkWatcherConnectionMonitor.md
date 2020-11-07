---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 3e5853d99157fef87c2f02c2be9fab7bb983d1ae
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849575"
---
# <span data-ttu-id="8850f-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8850f-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="8850f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8850f-102">SYNOPSIS</span></span>
<span data-ttu-id="8850f-103">Erstellt einen Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="8850f-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8850f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8850f-104">SYNTAX</span></span>

### <span data-ttu-id="8850f-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="8850f-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8850f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="8850f-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8850f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="8850f-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="8850f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8850f-108">DESCRIPTION</span></span>
<span data-ttu-id="8850f-109">Das New-AzureRmNetworkWatcherConnectionMonitor-Cmdlet rcreates einen Verbindungsmonitor für eine angegebene Quelle und ein angegebenes Ziel.</span><span class="sxs-lookup"><span data-stu-id="8850f-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="8850f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8850f-110">EXAMPLES</span></span>

### <span data-ttu-id="8850f-111">---------------Beispiel 1: Erstellen eines Verbindungs Monitors für ein VM-und Internet Ziel---------------</span><span class="sxs-lookup"><span data-stu-id="8850f-111">---------------  Example 1: Create a connection monitor for a vm and internet destination ---------------</span></span>
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

<span data-ttu-id="8850f-112">Das New-AzureRmNetworkWatcherConnectionMonitor-Cmdlet erstellt einen Verbindungsmonitor für eine angegebene Quelle und ein angegebenes Ziel.</span><span class="sxs-lookup"><span data-stu-id="8850f-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="8850f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8850f-113">PARAMETERS</span></span>

### <span data-ttu-id="8850f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8850f-114">-AsJob</span></span>
<span data-ttu-id="8850f-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8850f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8850f-116">– Autostart</span><span class="sxs-lookup"><span data-stu-id="8850f-116">-AutoStart</span></span>
<span data-ttu-id="8850f-117">Automatischer Start.</span><span class="sxs-lookup"><span data-stu-id="8850f-117">Auto start.</span></span>

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

### <span data-ttu-id="8850f-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8850f-118">-Confirm</span></span>
<span data-ttu-id="8850f-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8850f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8850f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8850f-120">-DefaultProfile</span></span>
<span data-ttu-id="8850f-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8850f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8850f-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="8850f-122">-DestinationAddress</span></span>
<span data-ttu-id="8850f-123">Die IP-Adresse des Verbindungsmonitor Ziels.</span><span class="sxs-lookup"><span data-stu-id="8850f-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="8850f-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="8850f-124">-DestinationPort</span></span>
<span data-ttu-id="8850f-125">Ziel-Port.</span><span class="sxs-lookup"><span data-stu-id="8850f-125">Destination port.</span></span>

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

### <span data-ttu-id="8850f-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="8850f-126">-DestinationResourceId</span></span>
<span data-ttu-id="8850f-127">Die ID des Verbindungsmonitor Ziels.</span><span class="sxs-lookup"><span data-stu-id="8850f-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="8850f-128">-Force</span><span class="sxs-lookup"><span data-stu-id="8850f-128">-Force</span></span>
<span data-ttu-id="8850f-129">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="8850f-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8850f-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="8850f-130">-Location</span></span>
<span data-ttu-id="8850f-131">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="8850f-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="8850f-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="8850f-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="8850f-133">Überwachungsintervall in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="8850f-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="8850f-134">-Name</span><span class="sxs-lookup"><span data-stu-id="8850f-134">-Name</span></span>
<span data-ttu-id="8850f-135">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="8850f-135">The connection monitor name.</span></span>

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

### <span data-ttu-id="8850f-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8850f-136">-NetworkWatcher</span></span>
<span data-ttu-id="8850f-137">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="8850f-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="8850f-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8850f-138">-NetworkWatcherName</span></span>
<span data-ttu-id="8850f-139">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="8850f-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="8850f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8850f-140">-ResourceGroupName</span></span>
<span data-ttu-id="8850f-141">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="8850f-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8850f-142">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="8850f-142">-SourcePort</span></span>
<span data-ttu-id="8850f-143">Quell-Port.</span><span class="sxs-lookup"><span data-stu-id="8850f-143">Source port.</span></span>

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

### <span data-ttu-id="8850f-144">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="8850f-144">-SourceResourceId</span></span>
<span data-ttu-id="8850f-145">Die ID der Verbindungsmonitor Quelle.</span><span class="sxs-lookup"><span data-stu-id="8850f-145">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="8850f-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="8850f-146">-Tag</span></span>
<span data-ttu-id="8850f-147">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="8850f-147">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8850f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8850f-148">-WhatIf</span></span>
<span data-ttu-id="8850f-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8850f-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8850f-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8850f-150">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="8850f-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8850f-151">INPUTS</span></span>

### <span data-ttu-id="8850f-152">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8850f-152">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="8850f-153">System. String</span><span class="sxs-lookup"><span data-stu-id="8850f-153">System.String</span></span>


## <span data-ttu-id="8850f-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8850f-154">OUTPUTS</span></span>

### <span data-ttu-id="8850f-155">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="8850f-155">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="8850f-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="8850f-156">NOTES</span></span>
<span data-ttu-id="8850f-157">Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor, Verbindungsmonitor</span><span class="sxs-lookup"><span data-stu-id="8850f-157">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="8850f-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8850f-158">RELATED LINKS</span></span>
<span data-ttu-id="8850f-159">[Neu – AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="8850f-159">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="8850f-160">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="8850f-160">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="8850f-161">[Neu – AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Neu – AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stopp-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="8850f-161">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="8850f-162">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="8850f-162">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
