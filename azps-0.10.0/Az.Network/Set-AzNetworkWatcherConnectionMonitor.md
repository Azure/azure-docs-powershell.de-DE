---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 93c54df5cb0976aa0bd8f73881208c1966bbe9d0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843596"
---
# <span data-ttu-id="0e8f1-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0e8f1-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="0e8f1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e8f1-102">SYNOPSIS</span></span>
<span data-ttu-id="0e8f1-103">Aktualisieren eines Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="0e8f1-103">Update a connection monitor.</span></span>

## <span data-ttu-id="0e8f1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e8f1-104">SYNTAX</span></span>

### <span data-ttu-id="0e8f1-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="0e8f1-105">SetByResource (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="0e8f1-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0e8f1-106">SetByName</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="0e8f1-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="0e8f1-107">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="0e8f1-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0e8f1-108">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="0e8f1-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="0e8f1-109">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="0e8f1-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e8f1-110">DESCRIPTION</span></span>
<span data-ttu-id="0e8f1-111">Das Set-AzNetworkWatcherConnectionMonitor-Cmdlet aktualisiert den angegebenen Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-111">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="0e8f1-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e8f1-112">EXAMPLES</span></span>

### <span data-ttu-id="0e8f1-113">---------------Beispiel 1: Aktualisieren eines Verbindungs Monitors---------------</span><span class="sxs-lookup"><span data-stu-id="0e8f1-113">---------------  Example 1: Update a connection monitor ---------------</span></span>
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

<span data-ttu-id="0e8f1-114">In diesem Beispiel wird der vorhandene Verbindungsmonitor aktualisiert, indem destinationAddress geändert und Tags hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="0e8f1-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e8f1-115">PARAMETERS</span></span>

### <span data-ttu-id="0e8f1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e8f1-116">-AsJob</span></span>
<span data-ttu-id="0e8f1-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0e8f1-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e8f1-118">– Autostart</span><span class="sxs-lookup"><span data-stu-id="0e8f1-118">-AutoStart</span></span>
<span data-ttu-id="0e8f1-119">Automatischer Start.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-119">Auto start.</span></span>

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

### <span data-ttu-id="0e8f1-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0e8f1-120">-Confirm</span></span>
<span data-ttu-id="0e8f1-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e8f1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e8f1-122">-DefaultProfile</span></span>
<span data-ttu-id="0e8f1-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e8f1-124">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="0e8f1-124">-DestinationAddress</span></span>
<span data-ttu-id="0e8f1-125">Die IP-Adresse des Verbindungsmonitor Ziels.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-125">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="0e8f1-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="0e8f1-126">-DestinationPort</span></span>
<span data-ttu-id="0e8f1-127">Ziel-Port.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-127">Destination port.</span></span>

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

### <span data-ttu-id="0e8f1-128">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="0e8f1-128">-DestinationResourceId</span></span>
<span data-ttu-id="0e8f1-129">Die ID des Verbindungsmonitor Ziels.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-129">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="0e8f1-130">-Force</span><span class="sxs-lookup"><span data-stu-id="0e8f1-130">-Force</span></span>
<span data-ttu-id="0e8f1-131">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="0e8f1-131">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0e8f1-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0e8f1-132">-InputObject</span></span>
<span data-ttu-id="0e8f1-133">Connection Monitor-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-133">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8f1-134">-Standort</span><span class="sxs-lookup"><span data-stu-id="0e8f1-134">-Location</span></span>
<span data-ttu-id="0e8f1-135">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="0e8f1-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="0e8f1-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="0e8f1-137">Überwachungsintervall in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-137">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="0e8f1-138">-Name</span><span class="sxs-lookup"><span data-stu-id="0e8f1-138">-Name</span></span>
<span data-ttu-id="0e8f1-139">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="0e8f1-139">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8f1-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e8f1-140">-NetworkWatcher</span></span>
<span data-ttu-id="0e8f1-141">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-141">The network watcher resource.</span></span>

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

### <span data-ttu-id="0e8f1-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0e8f1-142">-NetworkWatcherName</span></span>
<span data-ttu-id="0e8f1-143">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-143">The name of network watcher.</span></span>

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

### <span data-ttu-id="0e8f1-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e8f1-144">-ResourceGroupName</span></span>
<span data-ttu-id="0e8f1-145">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-145">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0e8f1-146">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0e8f1-146">-ResourceId</span></span>
<span data-ttu-id="0e8f1-147">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-147">Resource ID.</span></span>

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

### <span data-ttu-id="0e8f1-148">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="0e8f1-148">-SourcePort</span></span>
<span data-ttu-id="0e8f1-149">Quell-Port.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-149">Source port.</span></span>

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

### <span data-ttu-id="0e8f1-150">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="0e8f1-150">-SourceResourceId</span></span>
<span data-ttu-id="0e8f1-151">Die ID der Verbindungsmonitor Quelle.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-151">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="0e8f1-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="0e8f1-152">-Tag</span></span>
<span data-ttu-id="0e8f1-153">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-153">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="0e8f1-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e8f1-154">-WhatIf</span></span>
<span data-ttu-id="0e8f1-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e8f1-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-156">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="0e8f1-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e8f1-157">INPUTS</span></span>

### <span data-ttu-id="0e8f1-158">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e8f1-158">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="0e8f1-159">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="0e8f1-159">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="0e8f1-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e8f1-160">OUTPUTS</span></span>

### <span data-ttu-id="0e8f1-161">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="0e8f1-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="0e8f1-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e8f1-162">NOTES</span></span>
<span data-ttu-id="0e8f1-163">Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor, Verbindungsmonitor</span><span class="sxs-lookup"><span data-stu-id="0e8f1-163">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="0e8f1-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e8f1-164">RELATED LINKS</span></span>
<span data-ttu-id="0e8f1-165">[Neu – AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="0e8f1-165">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="0e8f1-166">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="0e8f1-166">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="0e8f1-167">[Neu – AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Neu – AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stopp-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="0e8f1-167">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="0e8f1-168">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Anfang-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="0e8f1-168">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span></span>

