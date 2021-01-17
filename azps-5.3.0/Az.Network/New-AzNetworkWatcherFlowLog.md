---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 1fe3cb8227751553ac748fb99cf08baa044a6f0d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459928"
---
# <span data-ttu-id="07791-101">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="07791-101">New-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="07791-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07791-102">SYNOPSIS</span></span>
<span data-ttu-id="07791-103">Erstellen oder aktualisieren Sie eine Flussprotokollressource für die angegebene Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="07791-103">Create or update a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="07791-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07791-104">SYNTAX</span></span>

### <span data-ttu-id="07791-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="07791-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07791-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="07791-106">SetByResource</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07791-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="07791-107">SetByResourceWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07791-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="07791-108">SetByNameWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07791-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="07791-109">SetByLocation</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07791-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="07791-110">SetByLocationWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07791-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07791-111">DESCRIPTION</span></span>
<span data-ttu-id="07791-112">New-AzNetworkWatcherFlowLog Befehl wird eine Flussprotokollressource für die angegebene Netzwerksicherheitsgruppe erstellt oder aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="07791-112">New-AzNetworkWatcherFlowLog command creates or updates a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="07791-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="07791-113">EXAMPLES</span></span>

### <span data-ttu-id="07791-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="07791-114">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $true -EnableRetention $true -RetentionPolicyDays 5 -FormatVersion 2 -EnableTrafficAnalytics -TrafficAnalyticsWorkspaceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace
```

<span data-ttu-id="07791-115">Name : pstest Id : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState : Succeeded Location : eastus TargetResourceId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled : True RetentionPolicy : { "Days": 5, "Enabled": true } Format : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 } }</span><span class="sxs-lookup"><span data-stu-id="07791-115">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 } }</span></span>

### <span data-ttu-id="07791-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="07791-116">Example 2</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $false -EnableTrafficAnalytics:$false
```

<span data-ttu-id="07791-117">Wenn Sie die FlowLog-Ressource deaktivieren möchten, für die TrafficAnalytics konfiguriert ist, muss TrafficAnalytics ebenfalls deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="07791-117">If you want to disable flowLog resource for which TrafficAnalytics is configured, it is necessary to disable TrafficAnalytics as well.</span></span> <span data-ttu-id="07791-118">Dies kann wie im Beispiel 2 geschehen.</span><span class="sxs-lookup"><span data-stu-id="07791-118">It can be done like in the example 2.</span></span>

<span data-ttu-id="07791-119">Name: pstest-Id: /subscriptions/bbbbbb-bbbb-bbbb-bbbb-bbbb-bbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState : Succeeded Location : eastus TargetResourceId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled: False RetentionPolicy : { "Days": 0, "Enabled": false } Format : { "Type": "JSON", "Version": 1 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": false, "trafficAnalyticsInterval": 60 } }</span><span class="sxs-lookup"><span data-stu-id="07791-119">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : False RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 1 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": false, "trafficAnalyticsInterval": 60 } }</span></span>

## <span data-ttu-id="07791-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07791-120">PARAMETERS</span></span>

### <span data-ttu-id="07791-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07791-121">-DefaultProfile</span></span>
<span data-ttu-id="07791-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07791-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07791-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="07791-123">-Enabled</span></span>
<span data-ttu-id="07791-124">Zum Aktivieren/Deaktivieren der Flussprotokollierung kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="07791-124">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07791-125">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="07791-125">-EnableRetention</span></span>
<span data-ttu-id="07791-126">Kennzeichnen, um die Aufbewahrung zu aktivieren/zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="07791-126">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="07791-127">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="07791-127">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="07791-128">Kennzeichnen zum Aktivieren/Deaktivieren von TrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="07791-128">Flag to enable/disable TrafficAnalytics</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07791-129">-Force</span><span class="sxs-lookup"><span data-stu-id="07791-129">-Force</span></span>
<span data-ttu-id="07791-130">Bestätigen Sie sie nicht, wenn Sie eine Ressource überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="07791-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="07791-131">-FormatType</span><span class="sxs-lookup"><span data-stu-id="07791-131">-FormatType</span></span>
<span data-ttu-id="07791-132">Der Dateityp des Flussprotokolls.</span><span class="sxs-lookup"><span data-stu-id="07791-132">The file type of flow log.</span></span>
<span data-ttu-id="07791-133">Der einzige unterstützte Wert ist jetzt "JSON".</span><span class="sxs-lookup"><span data-stu-id="07791-133">The only supported value now is 'JSON'.</span></span>

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

### <span data-ttu-id="07791-134">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="07791-134">-FormatVersion</span></span>
<span data-ttu-id="07791-135">Die Version (Revision) des Flussprotokolls.</span><span class="sxs-lookup"><span data-stu-id="07791-135">The version (revision) of the flow log.</span></span>

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

### <span data-ttu-id="07791-136">-Location</span><span class="sxs-lookup"><span data-stu-id="07791-136">-Location</span></span>
<span data-ttu-id="07791-137">Position der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="07791-137">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation, SetByLocationWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07791-138">-Name</span><span class="sxs-lookup"><span data-stu-id="07791-138">-Name</span></span>
<span data-ttu-id="07791-139">Der Name des Flussprotokolls.</span><span class="sxs-lookup"><span data-stu-id="07791-139">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07791-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07791-140">-NetworkWatcher</span></span>
<span data-ttu-id="07791-141">Die Netzwerk-Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="07791-141">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07791-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="07791-142">-NetworkWatcherName</span></span>
<span data-ttu-id="07791-143">Der Name der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="07791-143">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07791-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07791-144">-ResourceGroupName</span></span>
<span data-ttu-id="07791-145">Der Name der Ressourcengruppe "Netzwerk-Watcher".</span><span class="sxs-lookup"><span data-stu-id="07791-145">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07791-146">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="07791-146">-RetentionPolicyDays</span></span>
<span data-ttu-id="07791-147">Anzahl der Tage, für die Flussprotokolldatensätze beibehalten werden müssen.</span><span class="sxs-lookup"><span data-stu-id="07791-147">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="07791-148">-StorageId</span><span class="sxs-lookup"><span data-stu-id="07791-148">-StorageId</span></span>
<span data-ttu-id="07791-149">DIE ID des Speicherkontos, das zum Speichern des Flussprotokolls verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="07791-149">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="07791-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="07791-150">-Tag</span></span>
<span data-ttu-id="07791-151">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="07791-151">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="07791-152">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="07791-152">-TargetResourceId</span></span>
<span data-ttu-id="07791-153">DIE ID der Netzwerksicherheitsgruppe, auf die das Flussprotokoll angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="07791-153">ID of network security group to which flow log will be applied.</span></span>

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

### <span data-ttu-id="07791-154">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="07791-154">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="07791-155">Das Intervall in Minuten, das entscheiden würde, wie häufig der Ta-Dienst Flussanalysen erstellen soll.</span><span class="sxs-lookup"><span data-stu-id="07791-155">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07791-156">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="07791-156">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="07791-157">Ressourcen-ID des angefügten Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="07791-157">Resource Id of the attached workspace.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07791-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07791-158">-Confirm</span></span>
<span data-ttu-id="07791-159">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="07791-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07791-160">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="07791-160">-WhatIf</span></span>
<span data-ttu-id="07791-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07791-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07791-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07791-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07791-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07791-163">CommonParameters</span></span>
<span data-ttu-id="07791-164">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07791-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07791-165">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07791-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07791-166">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="07791-166">INPUTS</span></span>

### <span data-ttu-id="07791-167">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07791-167">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="07791-168">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="07791-168">OUTPUTS</span></span>

### <span data-ttu-id="07791-169">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="07791-169">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="07791-170">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="07791-170">NOTES</span></span>

## <span data-ttu-id="07791-171">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="07791-171">RELATED LINKS</span></span>

[<span data-ttu-id="07791-172">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07791-172">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="07791-173">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07791-173">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="07791-174">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07791-174">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="07791-175">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="07791-175">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="07791-176">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="07791-176">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="07791-177">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="07791-177">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="07791-178">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="07791-178">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="07791-179">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="07791-179">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="07791-180">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="07791-180">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="07791-181">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="07791-181">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="07791-182">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="07791-182">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="07791-183">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="07791-183">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="07791-184">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="07791-184">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="07791-185">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="07791-185">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="07791-186">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="07791-186">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="07791-187">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07791-187">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="07791-188">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07791-188">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="07791-189">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07791-189">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="07791-190">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="07791-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="07791-191">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07791-191">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="07791-192">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07791-192">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="07791-193">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="07791-193">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="07791-194">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="07791-194">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="07791-195">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="07791-195">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="07791-196">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="07791-196">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="07791-197">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="07791-197">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="07791-198">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07791-198">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="07791-199">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="07791-199">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="07791-200">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="07791-200">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="07791-201">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="07791-201">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
