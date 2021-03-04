---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 18db8d01bd9c6c54b1fdf3957f25e12848e309ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921883"
---
# <span data-ttu-id="7da94-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7da94-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="7da94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7da94-102">SYNOPSIS</span></span>
<span data-ttu-id="7da94-103">Erstellt eine Verbindungsmonitorressource.</span><span class="sxs-lookup"><span data-stu-id="7da94-103">Creates a connection monitor resource.</span></span>

## <span data-ttu-id="7da94-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7da94-104">SYNTAX</span></span>

### <span data-ttu-id="7da94-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7da94-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7da94-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7da94-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7da94-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="7da94-107">SetByResourceV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7da94-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="7da94-108">SetByNameV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7da94-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7da94-109">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7da94-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="7da94-110">SetByLocationV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7da94-111">SetByConnectionMonitorV2Object</span><span class="sxs-lookup"><span data-stu-id="7da94-111">SetByConnectionMonitorV2Object</span></span>
```
New-AzNetworkWatcherConnectionMonitor [-ConnectionMonitor <PSNetworkWatcherConnectionMonitorObject>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7da94-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7da94-112">DESCRIPTION</span></span>
<span data-ttu-id="7da94-113">Das New-AzNetworkWatcherConnectionMonitor-Cmdlet erstellt eine Verbindungsmonitorressource für die angegebene Quelle und das angegebene Ziel (SingleSourcedestination-Verbindungsmonitor) oder eine Gruppe von Testgruppen (MultiEndpointConnectionMonitor).</span><span class="sxs-lookup"><span data-stu-id="7da94-113">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor resource for specified source and destination (SingleSourcedestination connection monitor) or set of test groups (MultiEndpointConnectionMonitor).</span></span>

## <span data-ttu-id="7da94-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7da94-114">EXAMPLES</span></span>

### <span data-ttu-id="7da94-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7da94-115">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80
```

<span data-ttu-id="7da94-116">Name : cm Id : /subscriptions/000000000-0000-0000-0000-0000-0000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag : W/"e86b28cf-b907-0 4475-a8b7-34d310367694" ProvisioningState : Succeeded Source : { "ResourceId": "/subscriptions/000000000-0000-0000-0000-00000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft . Compute/virtualMachines/vm", "Port": 0 } Destination : { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart : True StartTime : 12.01.2018 7:13:11 Pm MonitoringStatus : Running Location : centraluseuap Type : Microsoft.Network/networkWatchers/connectionMonitors Tags : {}</span><span class="sxs-lookup"><span data-stu-id="7da94-116">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft .Compute/virtualMachines/vm", "Port": 0 } Destination                 : { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:13:11 PM MonitoringStatus            : Running Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : {}</span></span>

## <span data-ttu-id="7da94-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7da94-117">PARAMETERS</span></span>

### <span data-ttu-id="7da94-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7da94-118">-AsJob</span></span>
<span data-ttu-id="7da94-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7da94-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7da94-120">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="7da94-120">-ConfigureOnly</span></span>
<span data-ttu-id="7da94-121">Konfigurieren des Verbindungsmonitors, aber nicht starten</span><span class="sxs-lookup"><span data-stu-id="7da94-121">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="7da94-122">-ConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7da94-122">-ConnectionMonitor</span></span>
<span data-ttu-id="7da94-123">Verbindungsmonitorobjekt.</span><span class="sxs-lookup"><span data-stu-id="7da94-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="7da94-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7da94-124">-DefaultProfile</span></span>
<span data-ttu-id="7da94-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7da94-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7da94-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="7da94-126">-DestinationAddress</span></span>
<span data-ttu-id="7da94-127">Adresse des Ziels des Verbindungsmonitors (IP oder Domänenname).</span><span class="sxs-lookup"><span data-stu-id="7da94-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

### <span data-ttu-id="7da94-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="7da94-128">-DestinationPort</span></span>
<span data-ttu-id="7da94-129">Der vom Verbindungsmonitor verwendete Zielport.</span><span class="sxs-lookup"><span data-stu-id="7da94-129">The destination port used by connection monitor.</span></span>

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

### <span data-ttu-id="7da94-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="7da94-130">-DestinationResourceId</span></span>
<span data-ttu-id="7da94-131">Die ID der Ressource, die vom Verbindungsmonitor als Ziel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7da94-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

### <span data-ttu-id="7da94-132">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="7da94-132">-Force</span></span>
<span data-ttu-id="7da94-133">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="7da94-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7da94-134">-Location</span><span class="sxs-lookup"><span data-stu-id="7da94-134">-Location</span></span>
<span data-ttu-id="7da94-135">Speicherort des Netzwerkwächters.</span><span class="sxs-lookup"><span data-stu-id="7da94-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="7da94-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="7da94-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="7da94-137">Überwachungsintervall in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="7da94-137">Monitoring interval in seconds.</span></span> <span data-ttu-id="7da94-138">Der Standardwert ist 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="7da94-138">Default value is 60 seconds.</span></span>

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

### <span data-ttu-id="7da94-139">-Name</span><span class="sxs-lookup"><span data-stu-id="7da94-139">-Name</span></span>
<span data-ttu-id="7da94-140">Der Name des Verbindungsmonitors.</span><span class="sxs-lookup"><span data-stu-id="7da94-140">The connection monitor name.</span></span>

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

### <span data-ttu-id="7da94-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7da94-141">-NetworkWatcher</span></span>
<span data-ttu-id="7da94-142">Die Netzwerkwächterressource.</span><span class="sxs-lookup"><span data-stu-id="7da94-142">The network watcher resource.</span></span>

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

### <span data-ttu-id="7da94-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7da94-143">-NetworkWatcherName</span></span>
<span data-ttu-id="7da94-144">Der Name des Netzwerkwächters.</span><span class="sxs-lookup"><span data-stu-id="7da94-144">The name of network watcher.</span></span>

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

### <span data-ttu-id="7da94-145">-Hinweis</span><span class="sxs-lookup"><span data-stu-id="7da94-145">-Note</span></span>
<span data-ttu-id="7da94-146">Notizen, die mit dem Verbindungsmonitor verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="7da94-146">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="7da94-147">-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="7da94-147">-Output</span></span>
<span data-ttu-id="7da94-148">Beschreibt die Ausgabeziele eines Verbindungsmonitors.</span><span class="sxs-lookup"><span data-stu-id="7da94-148">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="7da94-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7da94-149">-ResourceGroupName</span></span>
<span data-ttu-id="7da94-150">Der Name der Ressourcengruppe "Netzwerkwächter".</span><span class="sxs-lookup"><span data-stu-id="7da94-150">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7da94-151">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="7da94-151">-SourcePort</span></span>
<span data-ttu-id="7da94-152">Der vom Verbindungsmonitor verwendete Quellport.</span><span class="sxs-lookup"><span data-stu-id="7da94-152">The source port used by connection monitor.</span></span>

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

### <span data-ttu-id="7da94-153">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="7da94-153">-SourceResourceId</span></span>
<span data-ttu-id="7da94-154">Die ID der Ressource, die vom Verbindungsmonitor als Quelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7da94-154">The ID of the resource used as the source by connection monitor.</span></span>

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

### <span data-ttu-id="7da94-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="7da94-155">-Tag</span></span>
<span data-ttu-id="7da94-156">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="7da94-156">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7da94-157">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="7da94-157">-TestGroup</span></span>
<span data-ttu-id="7da94-158">Die Liste der Testgruppen.</span><span class="sxs-lookup"><span data-stu-id="7da94-158">The list of test groups.</span></span>

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

### <span data-ttu-id="7da94-159">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7da94-159">-Confirm</span></span>
<span data-ttu-id="7da94-160">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7da94-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7da94-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7da94-161">-WhatIf</span></span>
<span data-ttu-id="7da94-162">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7da94-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7da94-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7da94-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7da94-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da94-164">CommonParameters</span></span>
<span data-ttu-id="7da94-165">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7da94-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da94-166">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7da94-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da94-167">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7da94-167">INPUTS</span></span>

### <span data-ttu-id="7da94-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7da94-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="7da94-169">System.String</span><span class="sxs-lookup"><span data-stu-id="7da94-169">System.String</span></span>

### <span data-ttu-id="7da94-170">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="7da94-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="7da94-171">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="7da94-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7da94-172">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7da94-172">OUTPUTS</span></span>

### <span data-ttu-id="7da94-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="7da94-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="7da94-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="7da94-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="7da94-175">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7da94-175">NOTES</span></span>

## <span data-ttu-id="7da94-176">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7da94-176">RELATED LINKS</span></span>
