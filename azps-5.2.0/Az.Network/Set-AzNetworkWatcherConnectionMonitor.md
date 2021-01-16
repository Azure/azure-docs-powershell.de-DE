---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5b5d7cff963a8f2a5322f67f31cfb31166f75aa9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300576"
---
# <span data-ttu-id="37053-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="37053-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="37053-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37053-102">SYNOPSIS</span></span>
<span data-ttu-id="37053-103">Aktualisiert die Verbindungsüberwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="37053-103">Updates connection monitor resource.</span></span>

## <span data-ttu-id="37053-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37053-104">SYNTAX</span></span>

### <span data-ttu-id="37053-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="37053-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37053-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="37053-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37053-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="37053-107">SetByResourceV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37053-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="37053-108">SetByNameV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37053-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="37053-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37053-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="37053-110">SetByLocationV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37053-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="37053-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37053-112">SetByResourceIdV2</span><span class="sxs-lookup"><span data-stu-id="37053-112">SetByResourceIdV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String>
 -TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>
 -Output <PSNetworkWatcherConnectionMonitorOutputObject[]> -Note <String> -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37053-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="37053-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37053-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37053-114">DESCRIPTION</span></span>
<span data-ttu-id="37053-115">Die Set-AzNetworkWatcherConnectionMonitor cmdlet aktualisiert die Verbindungsüberwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="37053-115">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates connection monitor resource.</span></span>

## <span data-ttu-id="37053-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="37053-116">EXAMPLES</span></span>

### <span data-ttu-id="37053-117">Beispiel 1: Aktualisieren eines Verbindungsmonitors</span><span class="sxs-lookup"><span data-stu-id="37053-117">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="37053-118">In diesem Beispiel aktualisieren wir den vorhandenen Verbindungsmonitor, indem wir "destinationAddress" ändern und Tags hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="37053-118">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="37053-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37053-119">PARAMETERS</span></span>

### <span data-ttu-id="37053-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37053-120">-AsJob</span></span>
<span data-ttu-id="37053-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="37053-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37053-122">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="37053-122">-ConfigureOnly</span></span>
<span data-ttu-id="37053-123">Konfigurieren des Verbindungsmonitors, aber nicht starten</span><span class="sxs-lookup"><span data-stu-id="37053-123">Configure connection monitor, but do not start it</span></span>

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

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37053-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37053-124">-DefaultProfile</span></span>
<span data-ttu-id="37053-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37053-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37053-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="37053-126">-DestinationAddress</span></span>
<span data-ttu-id="37053-127">Adresse des Ziels des Verbindungsmonitors (IP oder Domänenname).</span><span class="sxs-lookup"><span data-stu-id="37053-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37053-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="37053-128">-DestinationPort</span></span>
<span data-ttu-id="37053-129">Der vom Verbindungsmonitor verwendete Zielport.</span><span class="sxs-lookup"><span data-stu-id="37053-129">The destination port used by connection monitor.</span></span>

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

```yaml
Type: System.Int32
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37053-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="37053-130">-DestinationResourceId</span></span>
<span data-ttu-id="37053-131">Die ID der Ressource, die vom Verbindungsmonitor als Ziel verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="37053-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37053-132">-Force</span><span class="sxs-lookup"><span data-stu-id="37053-132">-Force</span></span>
<span data-ttu-id="37053-133">Bestätigen Sie sie nicht, wenn Sie eine Ressource überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="37053-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="37053-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37053-134">-InputObject</span></span>
<span data-ttu-id="37053-135">Verbindungsmonitorobjekt.</span><span class="sxs-lookup"><span data-stu-id="37053-135">Connection monitor object.</span></span>

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

### <span data-ttu-id="37053-136">-Location</span><span class="sxs-lookup"><span data-stu-id="37053-136">-Location</span></span>
<span data-ttu-id="37053-137">Speicherort der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="37053-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="37053-138">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="37053-138">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="37053-139">Überwachungsintervall in Sekunden</span><span class="sxs-lookup"><span data-stu-id="37053-139">Monitoring interval in seconds.</span></span> <span data-ttu-id="37053-140">Der Standardwert ist 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="37053-140">Default value is 60 seconds.</span></span>

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

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37053-141">-Name</span><span class="sxs-lookup"><span data-stu-id="37053-141">-Name</span></span>
<span data-ttu-id="37053-142">Der Name des Verbindungsmonitors.</span><span class="sxs-lookup"><span data-stu-id="37053-142">The connection monitor name.</span></span>

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

### <span data-ttu-id="37053-143">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="37053-143">-NetworkWatcher</span></span>
<span data-ttu-id="37053-144">Die Netzwerk-Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="37053-144">The network watcher resource.</span></span>

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

### <span data-ttu-id="37053-145">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="37053-145">-NetworkWatcherName</span></span>
<span data-ttu-id="37053-146">Der Name der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="37053-146">The name of network watcher.</span></span>

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

### <span data-ttu-id="37053-147">-Note</span><span class="sxs-lookup"><span data-stu-id="37053-147">-Note</span></span>
<span data-ttu-id="37053-148">Notizen, die dem Verbindungsmonitor zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="37053-148">Notes associated with connection monitor.</span></span>

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

```yaml
Type: System.String
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37053-149">-Output</span><span class="sxs-lookup"><span data-stu-id="37053-149">-Output</span></span>
<span data-ttu-id="37053-150">Beschreibt die Ausgabeziele eines Verbindungsmonitors.</span><span class="sxs-lookup"><span data-stu-id="37053-150">Describes a connection monitor output destinations.</span></span>

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

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37053-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37053-151">-ResourceGroupName</span></span>
<span data-ttu-id="37053-152">Der Name der Ressourcengruppe "Netzwerk-Watcher".</span><span class="sxs-lookup"><span data-stu-id="37053-152">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="37053-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37053-153">-ResourceId</span></span>
<span data-ttu-id="37053-154">ConnectionMonitor-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="37053-154">ConnectionMonitor resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37053-155">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="37053-155">-SourcePort</span></span>
<span data-ttu-id="37053-156">Der vom Verbindungsmonitor verwendete Quellport.</span><span class="sxs-lookup"><span data-stu-id="37053-156">The source port used by connection monitor.</span></span>

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

```yaml
Type: System.Int32
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37053-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="37053-157">-SourceResourceId</span></span>
<span data-ttu-id="37053-158">Die ID der Ressource, die vom Verbindungsmonitor als Quelle verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="37053-158">The ID of the resource used as the source by connection monitor.</span></span>

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

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37053-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="37053-159">-Tag</span></span>
<span data-ttu-id="37053-160">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="37053-160">A hashtable which represents resource tags.</span></span>

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

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByResourceId, SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37053-161">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="37053-161">-TestGroup</span></span>
<span data-ttu-id="37053-162">Die Liste der Testgruppen.</span><span class="sxs-lookup"><span data-stu-id="37053-162">The list of test groups.</span></span>

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

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37053-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37053-163">-Confirm</span></span>
<span data-ttu-id="37053-164">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37053-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37053-165">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="37053-165">-WhatIf</span></span>
<span data-ttu-id="37053-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37053-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37053-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37053-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37053-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37053-168">CommonParameters</span></span>
<span data-ttu-id="37053-169">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37053-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37053-170">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37053-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37053-171">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="37053-171">INPUTS</span></span>

### <span data-ttu-id="37053-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="37053-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="37053-173">System.String</span><span class="sxs-lookup"><span data-stu-id="37053-173">System.String</span></span>

### <span data-ttu-id="37053-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="37053-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="37053-175">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="37053-175">OUTPUTS</span></span>

### <span data-ttu-id="37053-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="37053-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="37053-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="37053-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="37053-178">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="37053-178">NOTES</span></span>

## <span data-ttu-id="37053-179">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="37053-179">RELATED LINKS</span></span>
