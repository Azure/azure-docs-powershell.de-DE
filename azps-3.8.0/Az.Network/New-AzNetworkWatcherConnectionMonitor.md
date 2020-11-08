---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: b84d11f259ffbf606bf0538a2ff71f6e9999db0a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995729"
---
# <span data-ttu-id="9469c-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9469c-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="9469c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9469c-102">SYNOPSIS</span></span>
<span data-ttu-id="9469c-103">Erstellt eine Verbindungsmonitor Ressource.</span><span class="sxs-lookup"><span data-stu-id="9469c-103">Creates a connection monitor resource.</span></span>

## <span data-ttu-id="9469c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9469c-104">SYNTAX</span></span>

### <span data-ttu-id="9469c-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9469c-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9469c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9469c-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9469c-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="9469c-107">SetByResourceV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9469c-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="9469c-108">SetByNameV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9469c-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9469c-109">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9469c-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="9469c-110">SetByLocationV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9469c-111">SetByConnectionMonitorV2Object</span><span class="sxs-lookup"><span data-stu-id="9469c-111">SetByConnectionMonitorV2Object</span></span>
```
New-AzNetworkWatcherConnectionMonitor [-ConnectionMonitor <PSNetworkWatcherConnectionMonitorObject>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9469c-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9469c-112">DESCRIPTION</span></span>
<span data-ttu-id="9469c-113">Das New-AzNetworkWatcherConnectionMonitor-Cmdlet erstellt eine Verbindungsmonitor Ressource für angegebene Quelle und Ziel (SingleSourcedestination Connection Monitor) oder Gruppe von Testgruppen (MultiEndpointConnectionMonitor).</span><span class="sxs-lookup"><span data-stu-id="9469c-113">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor resource for specified source and destination (SingleSourcedestination connection monitor) or set of test groups (MultiEndpointConnectionMonitor).</span></span>

## <span data-ttu-id="9469c-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9469c-114">EXAMPLES</span></span>

### <span data-ttu-id="9469c-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9469c-115">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80
```

<span data-ttu-id="9469c-116">Name: cm ID:/Subscriptions/00000000-0000-0000-0000-000000000000/resourceGro UPS/NetworkWatcherRG/Providers/Microsoft. Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionmonitors/T1 ETag: W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState: Nachfolge Quelle: {"Resource-ID": "/Subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/Anbieter/Microsoft. Compute/virtualMachines/VM "," Port ": 0} Ziel: {" Adresse ":" Bing.com "," Port ": 80} MonitoringIntervalInSeconds: 60 Autostart: true Startwert: 1/12/2018 7:13:11 Uhr MonitoringStatus: ausgeführter Speicherort: centraluseuap Typ: Microsoft. Network/networkWatchers/connectionMonitors-Tags: {}</span><span class="sxs-lookup"><span data-stu-id="9469c-116">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft .Compute/virtualMachines/vm", "Port": 0 } Destination                 : { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:13:11 PM MonitoringStatus            : Running Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : {}</span></span>

## <span data-ttu-id="9469c-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="9469c-117">PARAMETERS</span></span>

### <span data-ttu-id="9469c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9469c-118">-AsJob</span></span>
<span data-ttu-id="9469c-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9469c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9469c-120">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="9469c-120">-ConfigureOnly</span></span>
<span data-ttu-id="9469c-121">Konfigurieren des Verbindungs Monitors, aber nicht starten</span><span class="sxs-lookup"><span data-stu-id="9469c-121">Configure connection monitor, but do not start it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9469c-122">-ConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9469c-122">-ConnectionMonitor</span></span>
<span data-ttu-id="9469c-123">Connection Monitor-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9469c-123">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject
Parameter Sets: SetByConnectionMonitorV2Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9469c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9469c-124">-DefaultProfile</span></span>
<span data-ttu-id="9469c-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9469c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9469c-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="9469c-126">-DestinationAddress</span></span>
<span data-ttu-id="9469c-127">Die Adresse des Verbindungsmonitor Ziels (IP-oder Domänenname).</span><span class="sxs-lookup"><span data-stu-id="9469c-127">Address of the connection monitor destination (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9469c-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="9469c-128">-DestinationPort</span></span>
<span data-ttu-id="9469c-129">Der vom Verbindungsmonitor verwendete Ziel-Port.</span><span class="sxs-lookup"><span data-stu-id="9469c-129">The destination port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9469c-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="9469c-130">-DestinationResourceId</span></span>
<span data-ttu-id="9469c-131">Die ID der Ressource, die vom Verbindungsmonitor als Ziel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9469c-131">The ID of the resource used as the destination by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9469c-132">-Force</span><span class="sxs-lookup"><span data-stu-id="9469c-132">-Force</span></span>
<span data-ttu-id="9469c-133">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="9469c-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9469c-134">-Standort</span><span class="sxs-lookup"><span data-stu-id="9469c-134">-Location</span></span>
<span data-ttu-id="9469c-135">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="9469c-135">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation, SetByLocationV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9469c-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="9469c-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="9469c-137">Überwachungsintervall in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="9469c-137">Monitoring interval in seconds.</span></span> <span data-ttu-id="9469c-138">Der Standardwert ist 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="9469c-138">Default value is 60 seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9469c-139">-Name</span><span class="sxs-lookup"><span data-stu-id="9469c-139">-Name</span></span>
<span data-ttu-id="9469c-140">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="9469c-140">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9469c-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9469c-141">-NetworkWatcher</span></span>
<span data-ttu-id="9469c-142">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="9469c-142">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9469c-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9469c-143">-NetworkWatcherName</span></span>
<span data-ttu-id="9469c-144">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="9469c-144">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9469c-145">-Hinweis</span><span class="sxs-lookup"><span data-stu-id="9469c-145">-Note</span></span>
<span data-ttu-id="9469c-146">Notizen, die mit dem Verbindungsmonitor verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="9469c-146">Notes associated with connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9469c-147">-Output</span><span class="sxs-lookup"><span data-stu-id="9469c-147">-Output</span></span>
<span data-ttu-id="9469c-148">Beschreibt eine Ausgabe Ziele für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="9469c-148">Describes a connection monitor output destinations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9469c-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9469c-149">-ResourceGroupName</span></span>
<span data-ttu-id="9469c-150">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="9469c-150">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9469c-151">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="9469c-151">-SourcePort</span></span>
<span data-ttu-id="9469c-152">Der vom Verbindungsmonitor verwendete Quell-Port.</span><span class="sxs-lookup"><span data-stu-id="9469c-152">The source port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9469c-153">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="9469c-153">-SourceResourceId</span></span>
<span data-ttu-id="9469c-154">Die ID der Ressource, die vom Verbindungsmonitor als Quelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9469c-154">The ID of the resource used as the source by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9469c-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="9469c-155">-Tag</span></span>
<span data-ttu-id="9469c-156">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="9469c-156">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9469c-157">-Testgroup</span><span class="sxs-lookup"><span data-stu-id="9469c-157">-TestGroup</span></span>
<span data-ttu-id="9469c-158">Die Liste der Testgruppen.</span><span class="sxs-lookup"><span data-stu-id="9469c-158">The list of test groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9469c-159">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9469c-159">-Confirm</span></span>
<span data-ttu-id="9469c-160">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9469c-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9469c-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9469c-161">-WhatIf</span></span>
<span data-ttu-id="9469c-162">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9469c-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9469c-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9469c-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9469c-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9469c-164">CommonParameters</span></span>
<span data-ttu-id="9469c-165">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9469c-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9469c-166">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9469c-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9469c-167">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9469c-167">INPUTS</span></span>

### <span data-ttu-id="9469c-168">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9469c-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="9469c-169">System. String</span><span class="sxs-lookup"><span data-stu-id="9469c-169">System.String</span></span>

### <span data-ttu-id="9469c-170">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft. Azure. PowerShell. Cmdlets. Network, Version = 2.2.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9469c-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9469c-171">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorOutputObject, Microsoft. Azure. PowerShell. Cmdlets. Network, Version = 2.2.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9469c-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9469c-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9469c-172">OUTPUTS</span></span>

### <span data-ttu-id="9469c-173">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="9469c-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="9469c-174">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="9469c-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="9469c-175">Notizen</span><span class="sxs-lookup"><span data-stu-id="9469c-175">NOTES</span></span>

## <span data-ttu-id="9469c-176">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9469c-176">RELATED LINKS</span></span>
