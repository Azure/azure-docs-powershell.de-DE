---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5b5d7cff963a8f2a5322f67f31cfb31166f75aa9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009632"
---
# <span data-ttu-id="4b129-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4b129-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="4b129-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4b129-102">SYNOPSIS</span></span>
<span data-ttu-id="4b129-103">Aktualisiert die Ressource für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="4b129-103">Updates connection monitor resource.</span></span>

## <span data-ttu-id="4b129-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b129-104">SYNTAX</span></span>

### <span data-ttu-id="4b129-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4b129-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b129-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4b129-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b129-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="4b129-107">SetByResourceV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b129-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="4b129-108">SetByNameV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b129-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4b129-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b129-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="4b129-110">SetByLocationV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b129-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4b129-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b129-112">SetByResourceIdV2</span><span class="sxs-lookup"><span data-stu-id="4b129-112">SetByResourceIdV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String>
 -TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>
 -Output <PSNetworkWatcherConnectionMonitorOutputObject[]> -Note <String> -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b129-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="4b129-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b129-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b129-114">DESCRIPTION</span></span>
<span data-ttu-id="4b129-115">Das Cmdlet "Set-AzNetworkWatcherConnectionMonitor" aktualisiert die Verbindungsmonitor Ressource.</span><span class="sxs-lookup"><span data-stu-id="4b129-115">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates connection monitor resource.</span></span>

## <span data-ttu-id="4b129-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b129-116">EXAMPLES</span></span>

### <span data-ttu-id="4b129-117">Beispiel 1: Aktualisieren eines Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="4b129-117">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="4b129-118">In diesem Beispiel wird der vorhandene Verbindungsmonitor aktualisiert, indem destinationAddress geändert und Tags hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4b129-118">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="4b129-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b129-119">PARAMETERS</span></span>

### <span data-ttu-id="4b129-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b129-120">-AsJob</span></span>
<span data-ttu-id="4b129-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4b129-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b129-122">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="4b129-122">-ConfigureOnly</span></span>
<span data-ttu-id="4b129-123">Konfigurieren des Verbindungs Monitors, aber nicht starten</span><span class="sxs-lookup"><span data-stu-id="4b129-123">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="4b129-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b129-124">-DefaultProfile</span></span>
<span data-ttu-id="4b129-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4b129-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b129-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="4b129-126">-DestinationAddress</span></span>
<span data-ttu-id="4b129-127">Die Adresse des Verbindungsmonitor Ziels (IP-oder Domänenname).</span><span class="sxs-lookup"><span data-stu-id="4b129-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

### <span data-ttu-id="4b129-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="4b129-128">-DestinationPort</span></span>
<span data-ttu-id="4b129-129">Der vom Verbindungsmonitor verwendete Ziel-Port.</span><span class="sxs-lookup"><span data-stu-id="4b129-129">The destination port used by connection monitor.</span></span>

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

### <span data-ttu-id="4b129-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="4b129-130">-DestinationResourceId</span></span>
<span data-ttu-id="4b129-131">Die ID der Ressource, die vom Verbindungsmonitor als Ziel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4b129-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

### <span data-ttu-id="4b129-132">-Force</span><span class="sxs-lookup"><span data-stu-id="4b129-132">-Force</span></span>
<span data-ttu-id="4b129-133">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="4b129-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4b129-134">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4b129-134">-InputObject</span></span>
<span data-ttu-id="4b129-135">Connection Monitor-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4b129-135">Connection monitor object.</span></span>

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

### <span data-ttu-id="4b129-136">-Standort</span><span class="sxs-lookup"><span data-stu-id="4b129-136">-Location</span></span>
<span data-ttu-id="4b129-137">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="4b129-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="4b129-138">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="4b129-138">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="4b129-139">Überwachungsintervall in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="4b129-139">Monitoring interval in seconds.</span></span> <span data-ttu-id="4b129-140">Der Standardwert ist 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="4b129-140">Default value is 60 seconds.</span></span>

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

### <span data-ttu-id="4b129-141">-Name</span><span class="sxs-lookup"><span data-stu-id="4b129-141">-Name</span></span>
<span data-ttu-id="4b129-142">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="4b129-142">The connection monitor name.</span></span>

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

### <span data-ttu-id="4b129-143">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4b129-143">-NetworkWatcher</span></span>
<span data-ttu-id="4b129-144">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="4b129-144">The network watcher resource.</span></span>

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

### <span data-ttu-id="4b129-145">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4b129-145">-NetworkWatcherName</span></span>
<span data-ttu-id="4b129-146">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="4b129-146">The name of network watcher.</span></span>

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

### <span data-ttu-id="4b129-147">-Hinweis</span><span class="sxs-lookup"><span data-stu-id="4b129-147">-Note</span></span>
<span data-ttu-id="4b129-148">Notizen, die mit dem Verbindungsmonitor verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="4b129-148">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="4b129-149">-Output</span><span class="sxs-lookup"><span data-stu-id="4b129-149">-Output</span></span>
<span data-ttu-id="4b129-150">Beschreibt eine Ausgabe Ziele für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="4b129-150">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="4b129-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b129-151">-ResourceGroupName</span></span>
<span data-ttu-id="4b129-152">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="4b129-152">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4b129-153">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4b129-153">-ResourceId</span></span>
<span data-ttu-id="4b129-154">ConnectionMonitor-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="4b129-154">ConnectionMonitor resource ID.</span></span>

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

### <span data-ttu-id="4b129-155">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="4b129-155">-SourcePort</span></span>
<span data-ttu-id="4b129-156">Der vom Verbindungsmonitor verwendete Quell-Port.</span><span class="sxs-lookup"><span data-stu-id="4b129-156">The source port used by connection monitor.</span></span>

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

### <span data-ttu-id="4b129-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="4b129-157">-SourceResourceId</span></span>
<span data-ttu-id="4b129-158">Die ID der Ressource, die vom Verbindungsmonitor als Quelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4b129-158">The ID of the resource used as the source by connection monitor.</span></span>

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

### <span data-ttu-id="4b129-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="4b129-159">-Tag</span></span>
<span data-ttu-id="4b129-160">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="4b129-160">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4b129-161">-Testgroup</span><span class="sxs-lookup"><span data-stu-id="4b129-161">-TestGroup</span></span>
<span data-ttu-id="4b129-162">Die Liste der Testgruppen.</span><span class="sxs-lookup"><span data-stu-id="4b129-162">The list of test groups.</span></span>

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

### <span data-ttu-id="4b129-163">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4b129-163">-Confirm</span></span>
<span data-ttu-id="4b129-164">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b129-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b129-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b129-165">-WhatIf</span></span>
<span data-ttu-id="4b129-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4b129-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b129-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b129-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b129-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b129-168">CommonParameters</span></span>
<span data-ttu-id="4b129-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b129-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b129-170">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b129-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b129-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b129-171">INPUTS</span></span>

### <span data-ttu-id="4b129-172">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4b129-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="4b129-173">System. String</span><span class="sxs-lookup"><span data-stu-id="4b129-173">System.String</span></span>

### <span data-ttu-id="4b129-174">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="4b129-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="4b129-175">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4b129-175">OUTPUTS</span></span>

### <span data-ttu-id="4b129-176">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="4b129-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="4b129-177">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="4b129-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="4b129-178">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b129-178">NOTES</span></span>

## <span data-ttu-id="4b129-179">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4b129-179">RELATED LINKS</span></span>
