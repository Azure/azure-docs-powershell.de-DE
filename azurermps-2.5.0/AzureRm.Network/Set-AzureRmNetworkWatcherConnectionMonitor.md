---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
ms.openlocfilehash: e8ebbf4a554ef3dcb13726839ee8b7ebb330bad8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849076"
---
# <span data-ttu-id="eb1a2-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="eb1a2-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="eb1a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eb1a2-102">SYNOPSIS</span></span>
<span data-ttu-id="eb1a2-103">Aktualisieren eines Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="eb1a2-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb1a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb1a2-104">SYNTAX</span></span>

### <span data-ttu-id="eb1a2-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="eb1a2-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="eb1a2-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="eb1a2-106">SetByName</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="eb1a2-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="eb1a2-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="eb1a2-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="eb1a2-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="eb1a2-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="eb1a2-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="eb1a2-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb1a2-110">DESCRIPTION</span></span>
<span data-ttu-id="eb1a2-111">Das Set-AzureRmNetworkWatcherConnectionMonitor-Cmdlet aktualisiert den angegebenen Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="eb1a2-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="eb1a2-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb1a2-112">EXAMPLES</span></span>

### <span data-ttu-id="eb1a2-113">---------------Beispiel 1: Aktualisieren eines Verbindungs Monitors---------------</span><span class="sxs-lookup"><span data-stu-id="eb1a2-113">---------------  Example 1: Update a connection monitor ---------------</span></span>
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

<span data-ttu-id="eb1a2-114">In diesem Beispiel wird der vorhandene Verbindungsmonitor aktualisiert, indem destinationAddress geändert und Tags hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="eb1a2-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="eb1a2-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb1a2-115">PARAMETERS</span></span>

### <span data-ttu-id="eb1a2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb1a2-116">-AsJob</span></span>
<span data-ttu-id="eb1a2-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="eb1a2-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb1a2-118">– Autostart</span><span class="sxs-lookup"><span data-stu-id="eb1a2-118">-AutoStart</span></span>
<span data-ttu-id="eb1a2-119">Automatischer Start.</span><span class="sxs-lookup"><span data-stu-id="eb1a2-119">Auto start.</span></span>

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

### <span data-ttu-id="eb1a2-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eb1a2-120">-Confirm</span></span>
<span data-ttu-id="eb1a2-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eb1a2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb1a2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb1a2-122">-DefaultProfile</span></span>
<span data-ttu-id="eb1a2-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eb1a2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb1a2-124">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="eb1a2-124">-DestinationAddress</span></span>
<span data-ttu-id="eb1a2-125">Die IP-Adresse des Verbindungsmonitor Ziels.</span><span class="sxs-lookup"><span data-stu-id="eb1a2-125">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="eb1a2-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="eb1a2-126">-DestinationPort</span></span>
<span data-ttu-id="eb1a2-127">Ziel-Port.</span><span class="sxs-lookup"><span data-stu-id="eb1a2-127">Destination port.</span></span>

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

### <span data-ttu-id="eb1a2-128">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="eb1a2-128">-DestinationResourceId</span></span>
<span data-ttu-id="eb1a2-129">Die ID des Verbindungsmonitor Ziels.</span><span class="sxs-lookup"><span data-stu-id="eb1a2-129">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="eb1a2-130">-Force</span><span class="sxs-lookup"><span data-stu-id="eb1a2-130">-Force</span></span>
<span data-ttu-id="eb1a2-131">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="eb1a2-131">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="eb1a2-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="eb1a2-132">-InputObject</span></span>
<span data-ttu-id="eb1a2-133">Connection Monitor-Objekt.</span><span class="sxs-lookup"><span data-stu-id="eb1a2-133">Connection monitor object.</span></span>

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

### <span data-ttu-id="eb1a2-134">-Standort</span><span class="sxs-lookup"><span data-stu-id="eb1a2-134">-Location</span></span>
<span data-ttu-id="eb1a2-135">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="eb1a2-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="eb1a2-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="eb1a2-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="eb1a2-137">Überwachungsintervall in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="eb1a2-137">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="eb1a2-138">-Name</span><span class="sxs-lookup"><span data-stu-id="eb1a2-138">-Name</span></span>
<span data-ttu-id="eb1a2-139">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="eb1a2-139">The connection monitor name.</span></span>

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

### <span data-ttu-id="eb1a2-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eb1a2-140">-NetworkWatcher</span></span>
<span data-ttu-id="eb1a2-141">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="eb1a2-141">The network watcher resource.</span></span>

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

### <span data-ttu-id="eb1a2-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="eb1a2-142">-NetworkWatcherName</span></span>
<span data-ttu-id="eb1a2-143">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="eb1a2-143">The name of network watcher.</span></span>

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

### <span data-ttu-id="eb1a2-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb1a2-144">-ResourceGroupName</span></span>
<span data-ttu-id="eb1a2-145">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="eb1a2-145">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="eb1a2-146">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="eb1a2-146">-ResourceId</span></span>
<span data-ttu-id="eb1a2-147">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="eb1a2-147">Resource ID.</span></span>

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

### <span data-ttu-id="eb1a2-148">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="eb1a2-148">-SourcePort</span></span>
<span data-ttu-id="eb1a2-149">Quell-Port.</span><span class="sxs-lookup"><span data-stu-id="eb1a2-149">Source port.</span></span>

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

### <span data-ttu-id="eb1a2-150">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="eb1a2-150">-SourceResourceId</span></span>
<span data-ttu-id="eb1a2-151">Die ID der Verbindungsmonitor Quelle.</span><span class="sxs-lookup"><span data-stu-id="eb1a2-151">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="eb1a2-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="eb1a2-152">-Tag</span></span>
<span data-ttu-id="eb1a2-153">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="eb1a2-153">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="eb1a2-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb1a2-154">-WhatIf</span></span>
<span data-ttu-id="eb1a2-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eb1a2-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb1a2-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb1a2-156">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="eb1a2-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eb1a2-157">INPUTS</span></span>

### <span data-ttu-id="eb1a2-158">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eb1a2-158">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="eb1a2-159">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="eb1a2-159">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="eb1a2-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eb1a2-160">OUTPUTS</span></span>

### <span data-ttu-id="eb1a2-161">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="eb1a2-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="eb1a2-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="eb1a2-162">NOTES</span></span>
<span data-ttu-id="eb1a2-163">Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor, Verbindungsmonitor</span><span class="sxs-lookup"><span data-stu-id="eb1a2-163">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="eb1a2-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eb1a2-164">RELATED LINKS</span></span>
<span data-ttu-id="eb1a2-165">[Neu – AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="eb1a2-165">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="eb1a2-166">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="eb1a2-166">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="eb1a2-167">[Neu – AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Neu – AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stopp-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="eb1a2-167">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="eb1a2-168">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Anfang-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="eb1a2-168">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)
[Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>

