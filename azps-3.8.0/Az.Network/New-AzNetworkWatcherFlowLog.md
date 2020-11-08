---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 33441112856ebdbcb12da237542ed3ce62a3944c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996481"
---
# <span data-ttu-id="d6e0f-101">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="d6e0f-101">New-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="d6e0f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d6e0f-102">SYNOPSIS</span></span>
<span data-ttu-id="d6e0f-103">Erstellen oder aktualisieren Sie eine Flow Log-Ressource für die angegebene Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-103">Create or update a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="d6e0f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6e0f-104">SYNTAX</span></span>

### <span data-ttu-id="d6e0f-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d6e0f-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6e0f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d6e0f-106">SetByResource</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6e0f-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="d6e0f-107">SetByResourceWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6e0f-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="d6e0f-108">SetByNameWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6e0f-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d6e0f-109">SetByLocation</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6e0f-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="d6e0f-110">SetByLocationWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6e0f-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6e0f-111">DESCRIPTION</span></span>
<span data-ttu-id="d6e0f-112">New-AzNetworkWatcherFlowLog Befehl erstellt oder aktualisiert eine Flow Log-Ressource für die angegebene Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-112">New-AzNetworkWatcherFlowLog command creates or updates a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="d6e0f-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6e0f-113">EXAMPLES</span></span>

### <span data-ttu-id="d6e0f-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d6e0f-114">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $true -EnableRetention $true -RetentionPolicyDays 5 -FormatVersion 2 -EnableTrafficAnalytics -TrafficAnalyticsWorkspaceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace
```

<span data-ttu-id="d6e0f-115">Name: pstest-ID:/Subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ERS/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/flowlogs/pstest-ETag: W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState: succeeded Location: eastus TargetResourceId:/Subscriptions/56abfbd6-ec72-4ce9-831F-bc2b6f2c5505/resourceGroups/MyFlowLog/provide RS/Microsoft. Network/networkSecurityGroups/MyNSG-Datei:/Subscriptions/56abfbd6-ec72-4ce9-831F-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/Provider s/Microsoft. Storage/storageAccounts/mein Speicher aktiviert: true RetentionPolicy: {"Tage": 5, "Enabled": true} Format: {"Typ": "JSON"; "Version": 2} FlowAnalyticsConfiguration: {"networkWatcherFlowAnalyticsConfiguration": {"Enabled": wahr, "Arbeitsbereichs-Nr": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb"; "workspaceRegion": "eastus"; "workspaceResourceId": "/Subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr Oups/FlowLogsV2Demo/Anbieter/Microsoft. OperationalInsights/Arbeitsbereiche/mein Workspace"; "trafficAnalyticsInterval": 60}}</span><span class="sxs-lookup"><span data-stu-id="d6e0f-115">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 } }</span></span>

### <span data-ttu-id="d6e0f-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d6e0f-116">Example 2</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $false -EnableTrafficAnalytics:$false
```

<span data-ttu-id="d6e0f-117">Wenn Sie die flowLog-Ressource deaktivieren möchten, für die TrafficAnalytics konfiguriert ist, müssen Sie auch TrafficAnalytics deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-117">If you want to disable flowLog resource for which TrafficAnalytics is configured, it is necessary to disable TrafficAnalytics as well.</span></span> <span data-ttu-id="d6e0f-118">Dies kann wie im Beispiel 2 erfolgen.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-118">It can be done like in the example 2.</span></span>

<span data-ttu-id="d6e0f-119">Name: pstest-ID:/Subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ERS/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/flowlogs/pstest ETag: W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState: Nachfolger Standort: eastus TargetResourceId:/Subscriptions/56abfbd6-ec72-4ce9-831F-bc2b6f2c5505/resourceGroups/MyFlowLog/provide RS/Microsoft. Netzwerk-networkSecurityGroups/MyNSG-Speicher-Nr:/Subscriptions/56abfbd6-ec72-4ce9-831F-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/Provider s/Microsoft. Storage/storageAccounts/mystorage aktiviert: false RetentionPolicy: {"Days": 0; "Enabled": false} Format: {"Typ": "JSON"; "Version": 1} FlowAnalyticsConfiguration: {"networkWatcherFlowAnalyticsConfiguration": {"Enabled": falsch; "trafficAnalyticsInterval": 60}}</span><span class="sxs-lookup"><span data-stu-id="d6e0f-119">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : False RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 1 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": false, "trafficAnalyticsInterval": 60 } }</span></span>

## <span data-ttu-id="d6e0f-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6e0f-120">PARAMETERS</span></span>

### <span data-ttu-id="d6e0f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6e0f-121">-DefaultProfile</span></span>
<span data-ttu-id="d6e0f-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6e0f-123">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="d6e0f-123">-Enabled</span></span>
<span data-ttu-id="d6e0f-124">Kennzeichnen, um die Fluss Protokollierung zu aktivieren/deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-124">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="d6e0f-125">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="d6e0f-125">-EnableRetention</span></span>
<span data-ttu-id="d6e0f-126">Flag zum Aktivieren/Deaktivieren der Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-126">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="d6e0f-127">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="d6e0f-127">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="d6e0f-128">Flag zum Aktivieren/Deaktivieren von TrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="d6e0f-128">Flag to enable/disable TrafficAnalytics</span></span>

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

### <span data-ttu-id="d6e0f-129">-Force</span><span class="sxs-lookup"><span data-stu-id="d6e0f-129">-Force</span></span>
<span data-ttu-id="d6e0f-130">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="d6e0f-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d6e0f-131">-Formattyp</span><span class="sxs-lookup"><span data-stu-id="d6e0f-131">-FormatType</span></span>
<span data-ttu-id="d6e0f-132">Der Dateityp des Fluss Protokolls.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-132">The file type of flow log.</span></span>
<span data-ttu-id="d6e0f-133">Der einzige unterstützte Wert ist jetzt "JSON".</span><span class="sxs-lookup"><span data-stu-id="d6e0f-133">The only supported value now is 'JSON'.</span></span>

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

### <span data-ttu-id="d6e0f-134">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="d6e0f-134">-FormatVersion</span></span>
<span data-ttu-id="d6e0f-135">Die Version (Revision) des Fluss Protokolls.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-135">The version (revision) of the flow log.</span></span>

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

### <span data-ttu-id="d6e0f-136">-Standort</span><span class="sxs-lookup"><span data-stu-id="d6e0f-136">-Location</span></span>
<span data-ttu-id="d6e0f-137">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d6e0f-138">-Name</span><span class="sxs-lookup"><span data-stu-id="d6e0f-138">-Name</span></span>
<span data-ttu-id="d6e0f-139">Der Name des Fluss Protokolls.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-139">The flow log name.</span></span>

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

### <span data-ttu-id="d6e0f-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6e0f-140">-NetworkWatcher</span></span>
<span data-ttu-id="d6e0f-141">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-141">The network watcher resource.</span></span>

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

### <span data-ttu-id="d6e0f-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d6e0f-142">-NetworkWatcherName</span></span>
<span data-ttu-id="d6e0f-143">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-143">The name of network watcher.</span></span>

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

### <span data-ttu-id="d6e0f-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6e0f-144">-ResourceGroupName</span></span>
<span data-ttu-id="d6e0f-145">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-145">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d6e0f-146">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="d6e0f-146">-RetentionPolicyDays</span></span>
<span data-ttu-id="d6e0f-147">Die Anzahl der Tage, an denen Fluss Protokolldatensätze beibehalten werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-147">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="d6e0f-148">-Speicher-Nr</span><span class="sxs-lookup"><span data-stu-id="d6e0f-148">-StorageId</span></span>
<span data-ttu-id="d6e0f-149">Die ID des speicherkontos, das zum Speichern des Fluss Protokolls verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-149">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="d6e0f-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="d6e0f-150">-Tag</span></span>
<span data-ttu-id="d6e0f-151">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-151">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d6e0f-152">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="d6e0f-152">-TargetResourceId</span></span>
<span data-ttu-id="d6e0f-153">Die ID der Netzwerksicherheitsgruppe, auf die das Fluss Protokoll angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-153">ID of network security group to which flow log will be applied.</span></span>

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

### <span data-ttu-id="d6e0f-154">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="d6e0f-154">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="d6e0f-155">Das Intervall in Minuten, das entscheiden würde, wie häufig der TA-Dienst Flussanalyse ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-155">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

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

### <span data-ttu-id="d6e0f-156">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="d6e0f-156">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="d6e0f-157">Ressourcen-ID des angefügten Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="d6e0f-157">Resource Id of the attached workspace.</span></span>

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

### <span data-ttu-id="d6e0f-158">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d6e0f-158">-Confirm</span></span>
<span data-ttu-id="d6e0f-159">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6e0f-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6e0f-160">-WhatIf</span></span>
<span data-ttu-id="d6e0f-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6e0f-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6e0f-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6e0f-163">CommonParameters</span></span>
<span data-ttu-id="d6e0f-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6e0f-165">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6e0f-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6e0f-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d6e0f-166">INPUTS</span></span>

### <span data-ttu-id="d6e0f-167">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6e0f-167">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="d6e0f-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d6e0f-168">OUTPUTS</span></span>

### <span data-ttu-id="d6e0f-169">Microsoft. Azure. Commands. Network. Models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="d6e0f-169">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="d6e0f-170">Notizen</span><span class="sxs-lookup"><span data-stu-id="d6e0f-170">NOTES</span></span>

## <span data-ttu-id="d6e0f-171">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d6e0f-171">RELATED LINKS</span></span>

[<span data-ttu-id="d6e0f-172">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6e0f-172">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d6e0f-173">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6e0f-173">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d6e0f-174">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6e0f-174">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d6e0f-175">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d6e0f-175">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d6e0f-176">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d6e0f-176">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d6e0f-177">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d6e0f-177">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d6e0f-178">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d6e0f-178">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d6e0f-179">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6e0f-179">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d6e0f-180">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d6e0f-180">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d6e0f-181">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6e0f-181">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d6e0f-182">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6e0f-182">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d6e0f-183">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6e0f-183">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d6e0f-184">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6e0f-184">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d6e0f-185">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d6e0f-185">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d6e0f-186">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d6e0f-186">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d6e0f-187">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d6e0f-187">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d6e0f-188">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d6e0f-188">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d6e0f-189">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d6e0f-189">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d6e0f-190">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d6e0f-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d6e0f-191">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d6e0f-191">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d6e0f-192">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d6e0f-192">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d6e0f-193">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d6e0f-193">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d6e0f-194">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d6e0f-194">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d6e0f-195">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d6e0f-195">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d6e0f-196">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d6e0f-196">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d6e0f-197">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d6e0f-197">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="d6e0f-198">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d6e0f-198">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="d6e0f-199">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="d6e0f-199">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="d6e0f-200">Satz-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="d6e0f-200">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog)

[<span data-ttu-id="d6e0f-201">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="d6e0f-201">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog)