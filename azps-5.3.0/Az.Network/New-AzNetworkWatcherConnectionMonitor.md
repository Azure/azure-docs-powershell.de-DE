---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: b84d11f259ffbf606bf0538a2ff71f6e9999db0a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385494"
---
# <span data-ttu-id="c4f8b-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c4f8b-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="c4f8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="c4f8b-103">Erstellt eine Verbindungsmonitorressource.</span><span class="sxs-lookup"><span data-stu-id="c4f8b-103">Creates a connection monitor resource.</span></span>

## <span data-ttu-id="c4f8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4f8b-104">SYNTAX</span></span>

### <span data-ttu-id="c4f8b-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c4f8b-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4f8b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c4f8b-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4f8b-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="c4f8b-107">SetByResourceV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4f8b-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="c4f8b-108">SetByNameV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4f8b-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c4f8b-109">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4f8b-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="c4f8b-110">SetByLocationV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4f8b-111">SetByConnectionMonitorV2Object</span><span class="sxs-lookup"><span data-stu-id="c4f8b-111">SetByConnectionMonitorV2Object</span></span>
```
New-AzNetworkWatcherConnectionMonitor [-ConnectionMonitor <PSNetworkWatcherConnectionMonitorObject>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4f8b-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c4f8b-112">DESCRIPTION</span></span>
<span data-ttu-id="c4f8b-113">Das New-AzNetworkWatcherConnectionMonitor erstellt eine Verbindungsüberwachungsressource für die angegebene Quelle und das angegebene Ziel (Monitor für die SingleSourcedestination-Verbindung) oder eine Gruppe von Testgruppen (MultiEndpointConnectionMonitor).</span><span class="sxs-lookup"><span data-stu-id="c4f8b-113">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor resource for specified source and destination (SingleSourcedestination connection monitor) or set of test groups (MultiEndpointConnectionMonitor).</span></span>

## <span data-ttu-id="c4f8b-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c4f8b-114">EXAMPLES</span></span>

### <span data-ttu-id="c4f8b-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c4f8b-115">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80
```

<span data-ttu-id="c4f8b-116">Name: cm-ID: /subscriptions/00000000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag: W/"e86b28cf-b907-1 ProvisioningState: Succeeded Source : { "ResourceId": "/subscriptions/00000000-0000-000000-0000-0000-0000-0000-000000/microsoft. Compute/virtualMachines/vm", "Port": 0 } Destination : { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart : True StartTime : 12.01.2018 7:13:11: MonitoringStatus : Running Location : centraluseuap Type : Microsoft.Network/networkWatchers/connectionMonitors Tags : {}</span><span class="sxs-lookup"><span data-stu-id="c4f8b-116">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft .Compute/virtualMachines/vm", "Port": 0 } Destination                 : { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:13:11 PM MonitoringStatus            : Running Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : {}</span></span>

## <span data-ttu-id="c4f8b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4f8b-117">PARAMETERS</span></span>

### <span data-ttu-id="c4f8b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4f8b-118">-AsJob</span></span>
<span data-ttu-id="c4f8b-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c4f8b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c4f8b-120">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="c4f8b-120">-ConfigureOnly</span></span>
<span data-ttu-id="c4f8b-121">Konfigurieren des Verbindungsmonitors, aber nicht starten</span><span class="sxs-lookup"><span data-stu-id="c4f8b-121">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="c4f8b-122">-ConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c4f8b-122">-ConnectionMonitor</span></span>
<span data-ttu-id="c4f8b-123">Verbindungsmonitorobjekt.</span><span class="sxs-lookup"><span data-stu-id="c4f8b-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="c4f8b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4f8b-124">-DefaultProfile</span></span>
<span data-ttu-id="c4f8b-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4f8b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4f8b-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="c4f8b-126">-DestinationAddress</span></span>
<span data-ttu-id="c4f8b-127">Die Adresse des Ziels des Verbindungsmonitors (IP oder Domänenname).</span><span class="sxs-lookup"><span data-stu-id="c4f8b-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

### <span data-ttu-id="c4f8b-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="c4f8b-128">-DestinationPort</span></span>
<span data-ttu-id="c4f8b-129">Der vom Verbindungsmonitor verwendete Zielport.</span><span class="sxs-lookup"><span data-stu-id="c4f8b-129">The destination port used by connection monitor.</span></span>

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

### <span data-ttu-id="c4f8b-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="c4f8b-130">-DestinationResourceId</span></span>
<span data-ttu-id="c4f8b-131">Die ID der Ressource, die vom Verbindungsmonitor als Ziel verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c4f8b-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

### <span data-ttu-id="c4f8b-132">-Force</span><span class="sxs-lookup"><span data-stu-id="c4f8b-132">-Force</span></span>
<span data-ttu-id="c4f8b-133">Bestätigen Sie sie nicht, wenn Sie eine Ressource überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="c4f8b-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c4f8b-134">-Location</span><span class="sxs-lookup"><span data-stu-id="c4f8b-134">-Location</span></span>
<span data-ttu-id="c4f8b-135">Speicherort der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="c4f8b-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c4f8b-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="c4f8b-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="c4f8b-137">Überwachungsintervall in Sekunden</span><span class="sxs-lookup"><span data-stu-id="c4f8b-137">Monitoring interval in seconds.</span></span> <span data-ttu-id="c4f8b-138">Der Standardwert ist 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="c4f8b-138">Default value is 60 seconds.</span></span>

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

### <span data-ttu-id="c4f8b-139">-Name</span><span class="sxs-lookup"><span data-stu-id="c4f8b-139">-Name</span></span>
<span data-ttu-id="c4f8b-140">Der Name des Verbindungsmonitors.</span><span class="sxs-lookup"><span data-stu-id="c4f8b-140">The connection monitor name.</span></span>

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

### <span data-ttu-id="c4f8b-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c4f8b-141">-NetworkWatcher</span></span>
<span data-ttu-id="c4f8b-142">Die Netzwerk-Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="c4f8b-142">The network watcher resource.</span></span>

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

### <span data-ttu-id="c4f8b-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c4f8b-143">-NetworkWatcherName</span></span>
<span data-ttu-id="c4f8b-144">Der Name der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="c4f8b-144">The name of network watcher.</span></span>

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

### <span data-ttu-id="c4f8b-145">-Note</span><span class="sxs-lookup"><span data-stu-id="c4f8b-145">-Note</span></span>
<span data-ttu-id="c4f8b-146">Notizen, die dem Verbindungsmonitor zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c4f8b-146">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="c4f8b-147">-Output</span><span class="sxs-lookup"><span data-stu-id="c4f8b-147">-Output</span></span>
<span data-ttu-id="c4f8b-148">Beschreibt die Ausgabeziele eines Verbindungsmonitors.</span><span class="sxs-lookup"><span data-stu-id="c4f8b-148">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="c4f8b-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4f8b-149">-ResourceGroupName</span></span>
<span data-ttu-id="c4f8b-150">Der Name der Ressourcengruppe "Netzwerk-Watcher".</span><span class="sxs-lookup"><span data-stu-id="c4f8b-150">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c4f8b-151">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="c4f8b-151">-SourcePort</span></span>
<span data-ttu-id="c4f8b-152">Der vom Verbindungsmonitor verwendete Quellport.</span><span class="sxs-lookup"><span data-stu-id="c4f8b-152">The source port used by connection monitor.</span></span>

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

### <span data-ttu-id="c4f8b-153">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="c4f8b-153">-SourceResourceId</span></span>
<span data-ttu-id="c4f8b-154">Die ID der Ressource, die vom Verbindungsmonitor als Quelle verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c4f8b-154">The ID of the resource used as the source by connection monitor.</span></span>

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

### <span data-ttu-id="c4f8b-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="c4f8b-155">-Tag</span></span>
<span data-ttu-id="c4f8b-156">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="c4f8b-156">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c4f8b-157">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="c4f8b-157">-TestGroup</span></span>
<span data-ttu-id="c4f8b-158">Die Liste der Testgruppen.</span><span class="sxs-lookup"><span data-stu-id="c4f8b-158">The list of test groups.</span></span>

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

### <span data-ttu-id="c4f8b-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4f8b-159">-Confirm</span></span>
<span data-ttu-id="c4f8b-160">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4f8b-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4f8b-161">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c4f8b-161">-WhatIf</span></span>
<span data-ttu-id="c4f8b-162">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4f8b-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4f8b-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4f8b-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4f8b-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4f8b-164">CommonParameters</span></span>
<span data-ttu-id="c4f8b-165">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4f8b-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4f8b-166">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4f8b-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4f8b-167">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c4f8b-167">INPUTS</span></span>

### <span data-ttu-id="c4f8b-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c4f8b-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c4f8b-169">System.String</span><span class="sxs-lookup"><span data-stu-id="c4f8b-169">System.String</span></span>

### <span data-ttu-id="c4f8b-170">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="c4f8b-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c4f8b-171">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="c4f8b-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c4f8b-172">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c4f8b-172">OUTPUTS</span></span>

### <span data-ttu-id="c4f8b-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="c4f8b-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="c4f8b-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="c4f8b-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="c4f8b-175">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c4f8b-175">NOTES</span></span>

## <span data-ttu-id="c4f8b-176">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c4f8b-176">RELATED LINKS</span></span>
